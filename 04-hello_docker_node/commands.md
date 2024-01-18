docker build -t 04-hello_docker_node:v1 .
docker run --name neo -p 3000:3000 04-hello_docker_node:v1