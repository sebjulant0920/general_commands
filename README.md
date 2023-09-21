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
## install heimdall

Use this docker compose to install heimdall directly in portainer as a stack: 
---
version: "2.1"
services:
  heimdall:
    image: lscr.io/linuxserver/heimdall:latest
    container_name: heimdall
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Europe/Stockholm
    volumes:
      - /path/to/appdata/config:/config
    ports:
      - 1080:80
      - 10443:443
    restart: unless-stopped

  ## install Nginx Proxy Manager 

  ## Install Bitwarden

  
