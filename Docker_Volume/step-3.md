#### Create volume on command
```
docker run -it --name container3 -v /volume2 ubuntu /bin/bash
```
```
docker run -it --name container4 --privileged=true --volume-from container3 ubuntu /bin/bash
```
### host to container volume share
```
/home/ec2-user
```
```
docker run -it --name hostcont -v /home/ec2-user:/rajput --privileged=true ubuntu /bin/bash
```
```
docker volume create
docker volume inspect 
docker volume ls
````
```
docker volume prune
``` - 
Remove all unused volumes
docker volume rm
```
- List all the volumes that are not associated with any container
```
docker volume ls -f dangling=true
```
 - List all the volumes that are created with the local driver
 ```
docker volume ls -f driver=local
```
- Inspect a volume and display its details
```
docker volume inspect volume_name 
```
- Remove all the volumes that are not associated with any container
```
docker volume rm $(docker volume ls -qf dangling=true) 
```
- Create and start a container and mount a volume to it
```
docker volume run --mount source=my-vol,target=/app --name my-container -d my-image 
````
