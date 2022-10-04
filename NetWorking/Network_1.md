```
docker network --help
```
``` 
docker network ls
```
#### Create New bridge network NAME My_New_bridge_networ
```
docker network create -d bridge My_New_bridge_network
```
```
docker network ls
```
#### If we want to know all about any existing network, we use the ‘inspect’ command as below: –
```
docker network inspect <network_name>
```
#### If we want to attach a specific network while container creation, we use the ‘–net’ option as below: –
```
docker run -d --net=my_br_net --name my_container alpine sleep 3600
```
#### If we want to disconnect the container from any network, we use the ‘disconnect’ command as below: –
```
docker network disconnect <network_name><container_name>
```
#### If we want to connect any network to an existing container, we use the ‘connect’ command as below: –
```
docker network connect <network_name><container_name>
```
#### We can remove any existing network or more than one network at the same time if no longer in use or created by mistake using the ‘rm’ command as below: –
```
docker network rm <network1_name><network2_name>
```
#### We can remove all unused networks using the ‘prune’ command as below: –
```
docker network prune
```


