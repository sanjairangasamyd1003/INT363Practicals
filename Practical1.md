# Practical 1 - Docker Basics

## Aim
To understand the basic concepts of Docker and perform fundamental Docker operations.

## Docker Commands Performed

docker --version
docker info
docker search nginx
docker pull ubuntu
docker pull ubuntu:24.04
docker images
docker run hello-world
docker run -it ubuntu bash
docker ps
docker ps -a
docker run --name myubuntu -it ubuntu bash
docker start myubuntu
docker stop myubuntu
docker restart myubuntu
docker rm myubuntu
docker rmi ubuntu
docker run -d nginx
docker run -d -p 8080:80 --name webserver nginx
docker logs webserver
docker logs -f webserver
docker exec webserver ls
docker exec -it webserver sh
docker inspect webserver
docker stats
docker volume create mydata
docker volume ls
docker volume inspect mydata
docker run -it --name volume-demo -v mydata:/data ubuntu bash
docker network ls
docker --help
docker run -d -p 8081:80 --name web2 nginx

## Mini Practical

docker --version
docker info
docker pull ubuntu
docker images
docker run -it --name student-ubuntu ubuntu bash
docker ps
docker ps -a
docker run -d -p 8080:80 --name student-web nginx
docker logs student-web
docker exec -it student-web sh
docker stop student-web
docker rm student-web
docker rm student-ubuntu
