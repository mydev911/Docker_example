### How to change docker container name
```
docker container rename CON_id New_name
```
```
docker container ls
```


#### Create a container with new name
```
docker container run -it --name NEW_NAME ubuntu
```
#### Exit

## How to go inside the running container 
#### attach commannd  with CD_id or Name
```
docker container attach
```
## To exit from a running container without stop it
# Ctl +p Ctl  + Q

### How to puse running container
#### pause  ContainerID or Name
```
docker container pause 
```
## How to add tag 

```
docker tag <Containd_id_name> <tag_name>
```
## How to push image to docker hub
```
docker image push hub.docker.com <image _id / rep>
```
