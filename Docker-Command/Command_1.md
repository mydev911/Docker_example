```
docker ps
docker ps -a
docker images
docker pull ubuntu
docker run -d ubuntu  ### container will run and exit
docker run -it ubuntu   ### Container will run and you will inside the container
CONTROL+P+Q   #### You will exit form a running container without stop it
docker run -d --name alow  ubuntu  ##### Container will run and exit name will be alow
docker run -it --name alow ubuntu
docker run --name alow -d -it ubuntu  
docker run -it --name alow ubuntu /bin/bash
docker exec -it alow /bin/bash
docker run --it --name alow ubuntu /bin/bash
docker inspect COntainer_ID/ NAme
```

##### Stop all running container and delete the stoped container
```
docker stop $(docker ps -q)
docker rm $(docker ps -a -q)
````
###### Delete all images
```
docker rmi $(docker images -q)
```


### Network
```
docker network container_ID
docker logs Containe_NAMe
docker network ls
docker network inscpect
```


