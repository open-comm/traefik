Traefik Web Proxy
=================

Traefik is a reverse httpd proxy server.
It automatically detects docker web servers, directs traffic towards them
and automatically generates let's encrypt certificates.

Traefik project site: https://traefik.io 
Traefik documentation: https://docs.traefik.io

This is a ready to use docker-compose configuration with the following features:

* automated web proxy for all docker web services in this gitlab project ( https://gitlab.wachter-jud.net/docker )
* automatic http to https redirection
* automated Let's encrypt https certificate creation for all web services


Install
-------

```
# clone repository
git clone

# copy and edit sample configuration files
cd traefik
cp traefik.toml.sample traefik.toml
cp rules.toml.sample rules.toml

# edit email address in traefik.toml file
```


Usage
-----

```
# start traefik
docker-compose up -d

# stop traefik
docker-compose down

# upgrade to new traefik version
docker-compose pull
```

The traefik dashboard is available on port 8080.

