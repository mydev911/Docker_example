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






