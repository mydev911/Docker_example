### Docker volume
@root-@ec2-user

```
ls
touch file1,file2
vim dockerfile
```
```
FROM ubuntu:latest
VOLUME ["/myvolume"]
```
create image
```
docker build -t myimage .
```
```
docker images
```
create image
```
docker run -it --name container1 myimage /bin/bash
```
```
ls
cd myvolume
touch file-X file-y
ls
```
##### Create another container2 and attach to myvoume we create on container1
```
docker run -it --name container2 --privileged=true --volumes-from container1 ubuntu /bin/bash
```
Container 2
```
ls
cd myvolue
```
