# docker
docker files and instructions for Dispersão

## prepare images and files

copy dump file dispersao.sql to ./development/mysql folder
(the name of the file must be dispersao.sql)

create config.json file in ./development/dispersao-master, with the following content, replacing mastersecret with the master password:

{
"api": {
  "url":"http://localhost:1337",
  "user": "master",
  "password": "mastersecret"
  },
"osc": {
  "url": "ws://localhost",
  "port": 8081
  }
}

### create images
cd development/cms
docker build -t dispersao/cms .

cd development//socket-server
docker build -t dispersao/socket-server .

cd development//dispersao-master
docker build -t dispersao/master .


## start services for the first time (creates the containers)
cd development/
export  export MYSQL_ROOT_PASSWORD=anypass
export MYSQL_DISPERSAO_PASSWORD=supersecret

(use anypass for root, use the correct pass for dipersao db)

docker-compose up -d

## stop services

docker-compose stop

## restart services

docker-compose start

## stop service and erase containers (data is lost)

docker-compose down
