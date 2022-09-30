## How to access container from outside using port mapping
```
docker ls
```
#### Create a new container
```
docker container run -it -p 3600:80 ubuntu /bin/bash
```
```
apt-get update
```
```
apt-get install apache2
```
```
cd /var/www/html/
```
```
echo "welcome to docker container port mapping " > index.html
```
```
service apache2 start
```
#### to exit from container without stop 
## Ctl + p + q

#### Check docker container is running with port mappping

```
docker container ls
```
#### we get  aws ec2 ip address---  and past and past on web with ip:3600 port

