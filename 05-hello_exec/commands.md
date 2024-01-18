docker build -t 05-hello_exec:v1 .
docker run -d --name postgredb -p 5432:5432 05-hello_exec:v1 # -d pour lancer en tâche de fond
docker exec -it postgredb psql -U db -h localhost -p 5432 db
SELECT id, nom FROM personnes WHERE age > 30;