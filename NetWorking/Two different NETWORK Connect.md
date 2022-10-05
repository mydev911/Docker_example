# How to communicated two different network each other
### Flow Networking file....before....
#### dev-team network and prod-team netowrk communicated each other

```
docker container ls
```
```
docker network ls
```
```
docker network inspect <dev-team network ID>
```
### Open duplicate session
```
docker network inspect <prod-team network ID>
```
## dev-team
```
docker container run -it --network=dev-team --ip 10.100.0.100 -p 8000:80 ubuntu:14.04
```
```
ifconfig
```
install apache
```
apt-get update
```
```
apt-get install apache2
```
```
ls
```
```
cd /var/www/html/ echo"welcome to 10.0.100.0.100" > index.html
```
```
service apache2 start
```
```
ifconfig
```

## prod-team
```
docker container run -it --network=prod-team --ip 10.200.0.100 ubuntu:14.04
```
```
ifconfig
```
```
apt-get update
```
```
apt-get install wget
```
### Now we need to head to host eth0 netwoek....
```
wget 172.31.93.47:8000
```
### dev-team
```
apt-get update
```
```
apt-get install wget
```

### prod-team

```
docker container run -it --network=dev-team --ip 10.100.0.100 -p 8001:80 ubuntu:14.04
```
```
install apache
```
apt-get update
```
```
apt-get install apache2
```
```
ls
```
```
cd /var/www/html/ echo"welcome to 10.0.200.0.100" > index.html
```
```
service apache2 start
```
```
ifconfig
```








+
