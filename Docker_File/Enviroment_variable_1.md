# Enviroment variable
## user add
```
FROM ubuntu
LABEL Name="swapon"
LABEL EmailID="mydev911@gmail.com"
LABEL Phone="123483838"
ENV Name=cloudknowledge
ENV Pass=docker@2002
RUN useradd $Name && echo "$Name:$Pass" | chpasswd
RUN touch file1
RUN touch file2
RUN touch file3
RUN touch file4
```
#### Now build image with dockerfile
```
docker image build -t alo:21 .
```
#### Create docker container 
```
docker container run -it alo:21
```

#### check user
```
cat /etc/passwd
```
### Check user
```
su - alo
```

# Above container will run by root user
## Change root user to regular user to run container

```
FROM ubuntu
LABEL Name="swapon"
LABEL EmailID="mydev911@gmail.com"
LABEL Phone="123483838"
ENV Name=cloudknowledge
ENV Pass=docker@2002
RUN useradd $Name && echo "$Name:$Pass" | chpasswd
RUN touch file1
RUN touch file2
RUN touch file3
RUN touch file4
USER $Name
```

#### Now build image with dockerfile
```
docker image build -t alo:31 .
```
#### Create docker container 
```
docker container run -it alo:31
```
#### check container run in regular user we mentioned
#cloudknowledge@014d97aa0a0f:/$  

# Change or add working drictory
```
WORKDIR /var/workingfolder
```
#### Build image
#### Create container
```
docker image ls
```
## Check it .. Name and working dirctory is change
##### cloudknowledge@286838d0a899:/var/workingfolderI$


