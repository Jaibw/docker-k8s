# Install Docker in Debian 
# Source: https://docs.docker.com/engine/install/debian/ 
curl https://raw.githubusercontent.com/Jaibw/docker-k8s/master/install-docker-on-debian.sh --output install-docker-on-debian.sh
sh install-docker-on-debian.sh
sudo docker run hello-world