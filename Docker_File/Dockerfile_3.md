## Use level and 
#### create docker file
```
FROM ubuntu
LABEL Name="swapon"
LABEL EmailID="mydev911@gmail.com"
LABEL Phone="123483838"
RUN touch file1
RUN touch file2
RUN touch file3
RUN touch file4
Run apt-get update -y  &&  apt-get install -y apache2
RUN apt-get update -y  &&  apt-get install -y httpd
RUN apt-get install tree -y
```
#### Now build image with dockerfile
```
docker image build -t alo:1.1 .
```
```
docker image inspect 
```
# Enviroment variable
#### create docker file
```
FROM ubuntu
LABEL Name="swapon"
LABEL EmailID="mydev911@gmail.com"
LABEL Phone="123483838"
ENV Name=cloudknowledge
ENV Pass=docker@2002
RUN touch file1
RUN touch file2
RUN touch file3
RUN touch file4
Run apt-get update -y  &&  apt-get install -y apache2
RUN apt-get update -y  &&  apt-get install -y httpd
RUN apt-get install tree -y
```
#### Now build image with dockerfile
```
docker image build -t alo:11 .
```
#### Create docker container 
```
docker container run -it alo:11
```
```
env
``

