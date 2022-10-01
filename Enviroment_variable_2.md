# Copy command

#[root@ip-172-31-91-4 dockerfileImage]# 
#Create a folder
```
touch AbCopy
```
##### we want to copy Abcopy to new container build by dockerfile 
### Add on dockerfile
```
COPY AbCopy /var/workingfolder
```
#### build image
```
docker image build -t alo:21 .
```

####cloudknowledge@e3e70335979a:/var/workingfolder$ ls
AbCopy
