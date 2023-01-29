### https://youtu.be/egqSNqNISz0

```
useradd -m alexis -s /bin/bash
cat /etc/passwd
passwd alexis
```
Change password of root
```passwd
```
##### add alexis to sudo and docker
```
groups alexis
usermod -aG suod alexis
usermod aG docker alexis
groups alexis
```
```
su alexis
cd~
pwd
```
#### Create ssh connection to manin host to docker host
###### on root user 
```
ssh-keygen
ls -al .ssh
```
```
ssh-caop-id 
```
#### we need to stop password authentication ( same ansible kebernetes ssh connection)
```
sudo vim /etc/ssh/ssdh_config
```
Cid benchmark
```
lynis audit system
```

### docker security benchmark

```
sudo ./docker-bench-security.sh -c host_configuration
```
benchmak@
```
vim tests/1_host_configuration.sh
```
### linux server audit
```
sudo apt-get install auditd -y
man suditd
sudo auditd version
sudo aureport
tmux
rename docker_bench
```
```
ls
cd docker-bench-security/
sudo ./docker-bench-security.sh -c host_configuration
```
```
sudo vim /etc/ssh/sshd_config
```
#### 1.1.3 ensure auditing is configured for the docker daemon
```
sudo auditctl -w /user/bin/dockerd -k docker
```
```
sudo auditctl -1
```
```
-w /user/bin/dockerd -p rwxa -k docker
-w /run/containerd -p rwxa -k docker
-w /var/lib/docker -p rwxa -k docker
-w /etc/dockerd -p rwxa -k docker
...........................
```
dockerd -v
docker aureport -k
```
```
### save on audit and paste
```
sudo vim /etc/audit/rules.d/audit.rules
```
###### whenever auditd server restart this rules persisted































