# Common Docker Commands

## Image Commands

### Build an image from a Dockerfile
```bash
docker build -t image_name:tag .
```

### List all locally available images
```bash
docker images
```

### Remove an image
```bash
docker rmi image_name:tag
```

## Container Commands

### Run a container from an image
```bash
docker run -it --name container_name image_name:tag
```

### List all running containers
```bash
docker ps
```

### List all containers (including stopped ones)
```bash
docker ps -a
```

### Stop a running container
```bash
docker stop container_name_or_id
```

### Start a stopped container
```bash
docker start container_name_or_id
```

### Remove a stopped container
```bash
docker rm container_name_or_id
```

### Execute a command in a running container
```bash
docker exec -it container_name_or_id command
```

### Inspect container details
```bash
docker inspect container_name_or_id
```

### Change port forwarding

The above, test02 is a new image that is constructed from the test01 container.

```bash
docker stop test01
docker commit test01 test02
docker run -it --name test02 -p 8080:80 -td test02
```bash

## Volume Commands

### Create a named volume
```bash
docker volume create volume_name
```

### List all volumes
```bash
docker volume ls
```

### Remove a volume
```bash
docker volume rm volume_name
```

## Network Commands

### List all networks
```bash
docker network ls
```

### Inspect network details
```bash
docker network inspect network_name
```

## Compose Commands

### Start containers defined in a Docker Compose file
```bash
docker-compose up
```

### Stop and remove containers defined in a Docker Compose file
```bash
docker-compose down
```

### List containers defined in a Docker Compose file
```bash
docker-compose ps
```