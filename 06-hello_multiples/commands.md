docker network create appnetwork
docker run -d --name postgredb --network appnetwork -p 5432:5432 05-hello_exec:v1

js
const pool = new Pool({
  user: 'db',
  host: 'postgredb',
  database: 'db',
  password: 'db',
  port: 5432,
});

docker build -t 06-hello_multiples:v1 .
docker run -d --name nodeapp --network appnetwork -p 3000:3000 06-hello_multiples:v1
