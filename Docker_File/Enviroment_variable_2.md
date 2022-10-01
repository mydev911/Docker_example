# Copy command

#[root@ip-172-31-91-4 dockerfileImage]# 
#Create a folder
```
touch AbCopy
```
##### we want to copy Abcopy to new container build by dockerfile 
### Copy on dockerfile
```
COPY AbCopy /var/workingfolder
```
#### build image
```
docker image build -t alo:21 .
```

####cloudknowledge@e3e70335979a:/var/workingfolder$ ls
AbCopy

# Add command

```
ADD AbCopy /var/workingfolder
```
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
RUN apt-get update -y  && apt-get install -y  apache2
WORKDIR /var/www/html
ADD addfile /var/www/html
```
