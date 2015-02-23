## Pushpin Dockerfile


This repository contains **Dockerfile** of [Pushpin](http://www.pushpin.org/) for [Docker](https://www.docker.com/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [dockerfile/ubuntu](http://dockerfile.github.io/#/ubuntu)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/johnjelinek/pushpin/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull johnjelinek/pushpin`

   (alternatively, you can build an image from Dockerfile: `docker build -t="johnjelinek/pushpin" github.com/johnjelinek/pushpin-docker`)


### Usage

    docker run -d -P johnjelinek/pushpin

#### Attach app to forward traffic

  1. Start an app container that exposes on port 8080.

  2. Start a container by linking to the app container:

    ```sh
    docker run -d -P --link app:app johnjelinek/pushpin
    ```

Open `http://<host>:<assigned_port>` to see the result.
