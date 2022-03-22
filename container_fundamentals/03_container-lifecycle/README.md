# Container Lifecycle

In this training you will learn about the lifecycle of a container

## Create a container

```bash
docker run -d --name my-nginx nginx:1.21.6
```

## Stop a running container

```bash
docker stop my-nginx
```

Stop the started container. The main process inside the container will receive `SIGTERM`, and after a grace period, `SIGKILL`.

Install the tool jq

```bash
sudo apt install -y jq
```

Inspect the ExitCode

```bash
docker inspect my-nginx | jq '.[].State'
```

## Restart a stopped container

```bash
docker restart my-nginx
```

## Kill a container

If you have e.g. an hanging container, it's possible to send the `SIGKILL` signal directly. Try

```bash
docker kill my-nginx
```

Inspect the ExitCode

```bash
docker inspect my-nginx | jq '.[].State'
```

The container is still startable

```bash
docker start my-nginx
```

## Remove a container

```bash
docker rm my-nginx
```

Note that the container has to be stopped before it can be removed. You can also use the `force` flag.

```bash
docker rm -f my-nginx
```

The container cannot be started anymore.

```bash
docker start my-nginx
```

## Using the container id

Start some containers

```bash
docker run -d nginx:1.21.6
docker run -d nginx:1.21.6
docker run -d nginx:1.21.6
```

List all running containers

```
docker ps
```

Note that the containers got some generated names. You can use those names or you can the first letters of the container id to define the container in the commands.

## Cleanup

```bash
docker rm -f $(docker ps -qa)
```
