docker build -t 02-hello_dockerfile:v1 .
docker run -p 8080:80 02-hello_dockerfile:v1