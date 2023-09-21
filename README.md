# general_commands
## Install Portainer
Follow this guide: https://docs.portainer.io/start/install-ce/server/docker/linux

If there are any issues when starting portainer, remove image, volume and restart 
´´´
docker rm portainer

docker rmi portainer/portainer-ce:latest

docker volume rm portainer_data

docker volume ls

docker volume create portainer_data

docker ps
´´´
