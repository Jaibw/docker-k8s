# Install Docker in Debian 
# Source: https://docs.docker.com/engine/install/debian/ 
curl https://raw.githubusercontent.com/Jaibw/docker-k8s/master/install-docker-on-debian.sh --output install-docker-on-debian.sh
sh install-docker-on-debian.sh
sudo docker run hello-world

sudo docker version
sudo which docker   ## docker client binary 
sudo systemctl status docker ## docker engine service ; press q exit 

## working with docker images 
## Refer: https://hub.docker.com/ 
sudo docker images
sudo docker pull python
sudo docker images
sudo docker pull python:2.7.18
sudo docker images
sudo docker pull python:3.9.14
sudo docker images

## creating containers 
# host kernel version 
sudo uname -a
# containers kernel 
sudo docker run ubuntu uname -a
sudo docker run centos uname -a
## Python containers 
sudo docker run python:latest python --version
sudo docker run python python --version
sudo docker run python:2.7.18 python --version
sudo docker run python:2.7.18 python -c "print('hello world')"
sudo docker run python:latest python -c "print(3+4)"
