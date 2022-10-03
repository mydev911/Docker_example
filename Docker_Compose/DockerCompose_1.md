## Docker_Composer
```
docker-compose info
```
### Install docker_compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```
sudo chmod +x /usr/local/bin/docker-compose
```
```
docker-compose --version
```
Create a compose file.
```
vim docker-compose.yml
```
##### Click the link
https://docs.docker.com/samples/wordpress/

```
version: '3.4'
services:
 db:
   image: mysql:5.7
   volumes:
   - db_data:/var/lib/mysql
   restart: always
   environment:
     MYSQL_ROOT_PASSWORD: somewordpress
     MYSQL_DATABASE: wordpress
     MYSQL_USER: wordpress
     MYSQL_PASSWORD: wordpress

 wordpress:
   depends_on:
    - db
   image: wordpress:latest
   ports:
    - "8000:80"
   restart: always
   environment:
     WORDPRESS_DB_HOST: db:3306
     WORDPRESS_DB_USER: wordpress
     WORDPRESS_DB_PASSWORD: wordpress
     WORDPRESS_DB_NAME: wordpress
volumes:
 db_data: {}
```
```
docker-compose up -d
```
###### Now check aws publice ip:8080

