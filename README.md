# OMERO.server and OMERO.web (docker-compose)

[![Actions Status](https://github.com/ome/docker-example-omero/workflows/Build/badge.svg)](https://github.com/ome/docker-example-omero/actions)

This is an example of running OMERO.server and OMERO.web in Docker.

OMERO.server is listening on the standard OMERO ports `4063` and `4064`.
OMERO.web is listening on port `4080` (http://localhost:4080/).

## Environment file

Add a .env file using the following template as reference:
```text
OMERO_ROOT_PASSWORD=<value 1>
POSTGRES_PASSWORD=<value 2>
OMERO_DB_PASSWORD=<value 3>
ACME_REGISTRATION_EMAIL=<value 4>
```

## Run

First pull the latest major versions of the containers:

    docker-compose pull

Then start the containers:

    docker-compose up -d
    docker-compose logs -f

For more configuration options see:
- https://github.com/ome/omero-server-docker/blob/master/README.md
- https://github.com/ome/omero-web-docker/blob/master/README.md
