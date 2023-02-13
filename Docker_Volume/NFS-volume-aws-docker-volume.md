### Create a Nfs volume on aws and mount this volume with a docker container Name=sun , image=ubuntu, drictory on container Name=moon on same ec2 instance..

##### https://youtu.be/cCIbceqACP0

- Create a folder on ec2 for efs
```
mkdir efs
```
- this efs will attach to NFS , we create on aws .( all will be on same zone and ec2 , only for this project)
```
docker run -it --name sun -v /efs:/moon ubuntu
```

### Create a another docker container Name=earth , image=ubuntu, drictory on container Name=water on same ec2 instance..


