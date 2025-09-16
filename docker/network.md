# Docker Networks

## CLI Management of Virtual Networks

- `docker network ls` - show networks
- `docker network inspect <network_name>` – display detailed information on one or more networks
- `docker network create <network_name>` – create a network
- `docker network create --driver <network_name>` (or `-d`) – specify driver to manage the network (default `bridge`)
- `docker network connect <network_name> <container_name>` – attach a container to network
- `docker network connect <network_name> <container_name>` – disconnect a container to network
