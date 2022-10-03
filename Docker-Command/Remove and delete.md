# Remove delete
https://typeofnan.dev/how-to-stop-all-docker-containers/

```
docker container rm -f $(docker container ls -aq)
```
