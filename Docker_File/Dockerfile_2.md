# Dockerfile layer file architech
#### inisde the dockerfile
```
FROM centos
Run touch file1
Run touch file2
Run touch file3
Run touch file4
```
### How to build image from dockerfile
```
docker image build -t alo:1.1 .
```
### see step

```
5d0da3dc9764
Step 2/5 : Run touch file1
 ---> Running in b066357c6309
Removing intermediate container b066357c6309
 ---> 99d77e9b57d0
Step 3/5 : Run touch file2
 ---> Running in 0e7dbaff79ab
Removing intermediate container 0e7dbaff79ab
 ---> d3ec3034fce7
Step 4/5 : Run touch file3
 ---> Running in b885f349c835
Removing intermediate container b885f349c835
 ---> 614c5886f8ae
Step 5/5 : Run touch file4
 ---> Running in 6eb6bac7edc4
Removing intermediate container 6eb6bac7edc4
 ---> 7ccc482df10e
Successfully built 7ccc482df10e
Successfully tagged alo:2
```
