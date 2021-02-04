# Docker

_Note: VERY beta._  
This page is most definitely a WIP.  

## Pre-Run Requirements

fHDHR does not create a config file itself, nor does it come with a default one in place. If enough demand for one is there we may build a check to auto-create it, but at present there is no plan to do so.  
As such, before you run either of the below methods (only one, not both), be sure to create the folder and config file that you'll be passing in to the fHDHR container.  
In this example, we're assuming you're using `/opt/docker/fhdhr/config` as the folder for it. The below commands in SSH should get this done.  

```bash
mkdir -p /opt/docker/fhdhr/config
mkdir -p /opt/docker/fhdhr/plugins
touch /opt/docker/fhdhr/config/config.ini
```

## Docker CLI

```bash
docker run -d --name=fhdhr -v /opt/docker/fhdhr/config:/app/config -v /opt/docker/fhdhr/plugins:/app/plugins --network host --restart=unless-stopped fhdhr/fhdhr:latest
```

## Docker Compose

```yml
version: "2.1"
services:
  fhdhr:
    image: "fhdhr/fhdhr:latest"
    container_name: fhdhr
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Pacific/Auckland
    volumes:
      - /opt/docker/fhdhr/config:/app/config
      - /opt/docker/fhdhr/plugins:/app/plugins
    network_mode: host
    restart: unless-stopped
```
