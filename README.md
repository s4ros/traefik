# Traefik basic setup with OAuth2 forwarder

## Prerequirements

You need to have at least:
- docker
- docker-compose

## Create docker networks

```bash
docker network create reverse-proxy
```

## Launch the stack

```bash
docker-compose up -d
```

## Basic Auth

As you could probaly see inside the `docker-compose.yml` file, there's a basic auth for the Traefik frontend dashboard. You'll have to generate new `htpasswd` string for yourself to enter the https://traefik.your-domain.com. The Traefik configuration uses Let's Encrypt to handle the SSL traffic.

There is also a basic auth section for the API entry point - you'll want to generate new `htpasswd` for yourself as well.