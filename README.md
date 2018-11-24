# Docker NGINX Gunicorn Flask

Basic Flask application running on Gunicorn, a WSGI HTTP server, with NGINX as a reverse proxy server.

## Requirements

Docker and docker-compose.

## Build images

This will build images based on Alpine Linux for Python. An image for NGINX will be build when the services are started for the first time.

```bash
$ docker-compose build
```
## Start the services

```bash
$ docker-compose up -d # --force-recreate
```

To (stop and) recreate the containers before starting the services, use `--force-recreate`.

## List containers 

```bash
$ docker-compose ps
```

Notice that NGINX runs in the foreground (daemon off).

## Hello World

When both containers are up and running you can test the application.

```bash
$ curl 127.0.0.1
{"message":"Hello World!"}
```

## Stop the services

```bash
$ docker-compose stop
```
