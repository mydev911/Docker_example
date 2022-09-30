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
