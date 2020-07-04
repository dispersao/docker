# docker
docker files and instructions for Dispersão development server with remote code

## prepare images and files

copy dump file dispersao.sql to mysql folder

edit dispersao-master/config.json with the cms user and password

edit .env with the mysql user and password

## start services for the first time (creates the containers)

docker-compose up

## stop services

docker-compose stop

## restart services

docker-compose start

## stop service and erase containers (data is lost)

docker-compose down
