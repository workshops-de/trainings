# Hello Docker

In this training you will start a container and install a web server into it.

## Run an ubuntu container

```bash
docker run -it -p 8080:80 ubuntu:20.04
```

## Install a web server

```bash
apt update && DEBIAN_FRONTEND=noninteractive apt install -y apache2
```

## Run the web server

```bash
apache2ctl -DFOREGROUND
```

## Visit the welcome page in your browser

Use the webpreview feature of Google Cloud Shell to access the container.

## Stop the process in the Docker container

Press CTRL+C keys.

## Exit the container

```bash
exit
```

## Take a look at the running Docker containers

```bash
docker ps
```

## The Container is already in state `EXITED`. To see the Container do the following

```bash
docker ps -a
```

## Cleanup

```bash
docker rm <TAB>
```
