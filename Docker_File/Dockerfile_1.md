
![dockerfile](https://user-images.githubusercontent.com/23219981/193393113-1829992f-8627-4a63-879e-51208b88a1cc.jpg)
# How to create dockerfile
```
docker image ls
```
```
docker image history <image_id>
```
#### Create a folder
```
mkdir dockerfileImage
```
```
cd dockerfileImage/
```
#### Create dockerfile 
```
vim Dockerfile -f <dockerfile_name>
```
#### inisde the dockerfile
```
FROM    ubuntu
Run mkdir new_folder
Run apt-get update && apt-get install -y apache2
```

## 2nd dockerfile
```
FROM    ubuntu
Run mkdir new_folder
Run apt-get update && apt-get install -y apache2
Run apt-get tree
Run apt-get openssh-server
```
##3rd dockerfile
```

FROM    ubuntu
Run mkdir new_folder
Run apt-get update && apt-get install -y apache2 tree openssh-server python
```

### How to build image from dockerfile
```
docker image build -t alo:1.1 .
```
#alo is tag or name of image and 1.1 is version  .= current path  

#### Check image is create or not
```
docker lmage ls
```
#### Create container form image
```
docker container run -it --name interactive_alo alo:1
```
```
docker ps
```

