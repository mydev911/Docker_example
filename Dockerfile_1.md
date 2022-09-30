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
```
### How to build image from dockerfile
```
docker image build -t taggg:1.1 .
```
#taggg is tag or name of image and 1.1 is version  .= current path  

#### Check image is create or not
```
docker lmage ls
'``
