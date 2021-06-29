# Traefik Web Proxy

Traefik is a reverse httpd proxy server.
It automatically detects docker web servers, directs traffic towards them
and automatically generates let's encrypt certificates.

Traefik project site: https://traefik.io 
Traefik documentation: https://docs.traefik.io

This is a ready to use docker-compose configuration with the following features:

* automated web proxy for all docker web services in this gitlab project ( https://gitlab.open-communication.net/docker )
* automatic http to https redirection
* automated Let's encrypt https certificate creation for all web services


## Install

```
# clone repository
git clone https://git.open-communication.net/open-communication/docker/traefik.git

# move into directory
cd traefik

# copy and edit environment file
cp sample.env .env

## edit email address in .env file
```


## Start & Stop Traefik Web Proxy

```
# start traefik
docker-compose up -d

# stop traefik
docker-compose down

# upgrade to new traefik version
docker-compose pull
```

The traefik dashboard is available on port 8080.

