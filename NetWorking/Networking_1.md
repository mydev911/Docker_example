```
docker container ls
```
```
docker network ls
```
```
docker network inspect <NETWORK_ID>
```
##### root@ec349dhfihfe: /# hostname
```
cat /etc/resolv.conf
```
## Create a container with Own_HostName and Own_IP
##### root@
```
docker container run -it --hostname Alow --dns 8.8.8.8 ubuntu:14.04
```
##### Check
```
hostname
```
```
ifconfig
```
```
cat /etc/resolv.conf
```

## Create own netwoek
```
docker network create dev-team
```
```
docker network ls
```
```
docker network inspect dev-team
```
## Delete netwoek 
```
docker network rm -f dev-team 
```
## Create netwoek with NetWork_Name With Subnet
```
docker network create dev-team --subnet=10.100.0.0/24
```
```
docker network ls
```
```
docker network inspect dev-team
```

```
docker network create prod-team --subnet=10.200.0.0/24
```
```
docker network ls
```
```
docker network inspect prod-team
```
# Create new container and connect to dev-team / prod-team 
```
docker container run -it --network=dev-team ubuntu:14.04
```
```
ifconfig
```
```
docker network inspect dev-team
```

### Check dev-team submit and eth0 inet addr are same











