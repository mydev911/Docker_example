#### How to run a container in interactive and daemon mode
## Defult mode -- 
```
docker container run  --name Detach_mode tomcat
```
##### Container will run and you are inside the terminal. Terminal is not free to use . To use terminal you need to stop the container and exit. Ctl+c 


## Detach mode -- 
```
docker container run -d --name Detach_mode tomcat
```
##### Container will run in background and terminal is free to user. Both Terminal and Container will run seperate

## Interactive mode -- 
```
docker container run -it --name Interactive_mode tomcat /bin/bash
```
##### Container will run and you will inside the container. Terminal is not free to use. First you need to exit from container or stop the container. Interactive mode we need to use bash ... /bin/bash
To exit ther container without stop it ---  Ctl+p+q 




#### How to login to a docker container | How to run commands inside a container
https://youtu.be/7CmV8fpRYYE
```
docker image ls -a
```
```
docker run -d --name <Name_Given> Tomcat
```
#-   -d is detach mode > 
```
docker exec -it <Name_given>  /bin/bash
```
