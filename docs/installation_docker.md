# Docker

## Pre-Run Requirements

fHDHR does not create a config file itself, nor does it come with a default one in place. If enough demand for one is there we may build a check to auto-create it, but at present there is no plan to do so.  
As such, before you run either of the below methods (only one, not both), be sure to create the folder and config file that you'll be passing in to the fHDHR container.  

## Creating Required Paths
The following commands will create the required directories and files. Be sure change the directory path to match your desired location.

```bash
mkdir -p /path/to/config
mkdir -p /path/to/plugins
touch /path/to/config/config.ini
```

> If you wish to keep a persistent cache, you can also create a directory for the cache. This allows channels that were disabled or favorited to be persistent after restarting the container.

## Docker CLI

```bash
docker run -d --name=fhdhr -v /path/to/config:/app/config -v /path/to/plugins:/app/plugins --network host --restart=unless-stopped fhdhr/fhdhr:latest
```

> If you wish to include the persistent cache, simply include `-v /path/to/cache:/app/data/cache` in the above command.

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
      - /path/to/config:/app/config
      - /path/to/plugins:/app/plugins
      - /path/to/cache:/app/data/cache # Optional
    network_mode: host
    restart: unless-stopped
```
