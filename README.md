Cloud9 v3 Dockerfile
=============

This repository contains Dockerfile of Cloud9 IDE for Docker's automated build published to the public Docker Hub Registry.

# Base Docker Image
[fengal/docker-cloud9-alpine](https://hub.docker.com/r/fengal/docker-cloud9-alpine/)

# Installation

## Install Docker.

Download automated build from public Docker Hub Registry: docker pull fengal/docker-cloud9-alpine

(alternatively, you can build an image from Dockerfile: docker build -t="fengal/docker-cloud9-alpine" github.com/LoicLemerlus/docker-cloud9-alpine)

## Usage

    docker run -tid -p 80:8000 -p 3000:3000 fengal/docker-cloud9-alpine
    
You can add a workspace as a volume directory with the argument *-v /your-path/workspace/:/workspace/* like this :

    docker run -tid -p 80:8000 -p 3000:3000 -v /your-path/workspace/:/workspace/ fengal/docker-cloud9-alpine

You can specify the username and password as environement variables

    docker run -tid -p 80:8000 -p 3000:3000 -e USERNAME=username -e PASSWORD=password fengal/docker-cloud9-alpine

