# docker
docker files and instructions for Dispersão

---------------
## production

### prepare images and files

cd to production/server/

copy dump file dispersao.sql to  production/server/ folder

(the name of the file must be dispersao.sql)

copy images to production/server/cms/uploads/

edit production/server/.env file with the mysql user and pass

### start services for the first time (creates the containers)
```
docker-compose up
```
### stop services
```
docker-compose stop
```

### restart services
```
docker-compose start
```

### stop service and erase containers (data is lost)
```
docker-compose down
