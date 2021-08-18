# Ubuntu debugging container

This image and container contains a standard Linux distribution with some tools preinstalled on it.

Create the image from the Dockerfile

```bash
docker build -t alessandro/ubuntu_debug .
```

Start the container from the image in interactive mode, attaching to a network if needed (for example here is attached to the previously created network namede `keycloak-network`)

```bash
docker run --name ubuntu_container --net keycloak-network -it alessandro/ubuntu_debug
```
