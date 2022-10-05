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

## Build and run 
git clone https://github.com/Jaibw/FrozenYogurtShop.git
cd FrozenYogurtShop/
ls
cat Dockerfile 
sudo docker images
sudo docker build -t website .
sudo docker images
sudo docker run -d --name demo website
sudo docker ps 
sudo docker inspect demo | grep -i ipaddress
curl 172.#.#.# | grep -i title

# kubernetes commands 
kubectl get nodes
kubectl run demo01 --image=nginx
kubectl get pods
kubectl get pods -o wide
kubectl describe pod demo01
kubectl logs demo01
kubectl delete pod demo01 

