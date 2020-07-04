# docker
docker files and instructions for Dispersão development server with local code

## prepare images and files

copy dump file dispersao.sql to mysql folder

edit .env with the mysql user and password

you're supposed to have the code in the folders

- ./dispersao-master https://github.com/dispersao/dispersao-master
- ./cms https://github.com/dispersao/cms

you must edit the user and password in dispersao-master/public/config.json

## start services for the first time (creates the containers)

docker-compose up

## stop services

docker-compose stop

## restart services

docker-compose start

## stop service and erase containers (data is lost)

docker-compose down
