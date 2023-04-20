# PALYIM's OMERO.server and OMERO.web (docker-compose)

[![Actions Status](https://github.com/paleopollen/palyim-omero-docker/workflows/Build/badge.svg)](https://github.com/paleopollen/palyim-omero-docker/actions)

This repository contains configuration for OMERO.server and OMERO.web in Docker.

## Environment file

Add a .env file using the following template as reference. Please note that these values are only priovided as an example and should NOT be used in any deployed instances:
```text
OMERO_ROOT_PASSWORD=omero
POSTGRES_PASSWORD=omero
ACME_REGISTRATION_EMAIL=admin@example.com
ACME_CA_SERVER_URL=https://acme-staging-v02.api.letsencrypt.org/directory
HOSTNAME=web.omero.localhost
```

## Run

First pull the latest major versions of the containers:

    docker-compose pull

Then start the containers:

    docker-compose up -d
    docker-compose logs -f

OMERO.server is listening on the SSL port `4064`.
OMERO.web is listening on port `80` (http://web.omero.localhost/).

For more configuration options see:
- https://github.com/ome/omero-server-docker/blob/master/README.md
- https://github.com/ome/omero-web-docker/blob/master/README.md
