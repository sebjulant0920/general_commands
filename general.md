docker rm portainer

docker rmi portainer/portainer-ce:latest

docker volume rm portainer_data

docker volume ls

docker volume create portainer_data

docker ps
