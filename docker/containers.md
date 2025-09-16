# Docker Containers

A container is a runtime instance of a docker image. A container will always run the same, regardless of the infrastructure. Containers isolate software from its environment and ensure that it works uniformly despite differences for instance between development and staging.

## Run

Aliases: `docker container run`, `docker run`

- `docker run --name <container_name> <image_name>` – create and run a container from an image, with a custom name
- `docker run --publish <host_port>:<container_port> <image_name>` – run a container and publish a container’s port(s) to the host
- `docker run -p <host_port>:<container_port> <image_name>` – `-p` flag is the same as `--publish`
- `docker run --detach <image_name>` – run a container in the background
- `docker run -d <image_name>` – `-d` flag is the same as `--detach`

## Start and stop

Aliases: `docker container start`, `docker start`

- `docker start <container_name>` (or `<container_id>`) – start an existing container

Aliases: `docker container stop`, `docker stop`

- `docker stop <container_name>` (or `<container_id>`) – stop an existing container

## Remove

Aliases: `docker container remove`, `docker container rm`, `docker rm`

- `docker rm <container_name>` (or `<container_id>`) – remove a stopped container
- `docker rm --force <container_name>` – remove forcefully a running container
- `docker rm -f <container_name>` – `-f` flag is the same as `--force`
- `docker rm <container_name_1> <container_name_2> <container_name_3>` – remove multiple stopped containers

## List

Aliases: `docker container list`, `docker container ls`, `docker container ps`, `docker ps`

- `docker ps` – list all currently running containers
- `docker ps --all` – list all Docker containers (running and stopped)
- `docker ps --a` – `-a` flag is the same as `--all`

## Execute

Execute a command in a running container

Aliases: `docker container exec`, `docker exec`

- `docker exec -it <container_name> sh` – open a shell inside a running container
- `docker run -it <container_name> bash` – run a container in an interactive mode and open a bash inside the running container

## Logs

Aliases: `docker container logs`, `docker logs`

- `docker logs <container_name>` – fetch the logs of a container
- `docker logs --follow <container_name>` – fetch and follow the logs of a container
- `docker logs -f <container_name>` – `-f` flag is the same as `--follow`

## Inspect and display processes

Aliases: `docker container inspect`, `docker inspect`

- `docker inspect <container_name>` – display detailed (low-level) information on one or more containers

Aliases: `docker container top`, `docker top`

- `container top <container_name>` – display the running processes of a container

## View stats

Aliases: `docker container stats`, `docker stats`

- `docker stats` – display a live stream of container(s) resource usage statistics
