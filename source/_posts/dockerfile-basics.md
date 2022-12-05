---
title: Dockerfile Command Cheat Sheet
date: 2022-12-05 11:01:07
tags: [docker, dockerfile]
categories: [docker, dockerfile]
banner_img: https://dogefs.s3.ladydaily.com/~/source/unsplash/photo-1605745341112-85968b19335b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=871&q=80
index_img: https://dogefs.s3.ladydaily.com/~/source/unsplash/photo-1605745341112-85968b19335b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=871&q=80
---

## Images

### Dockerfile instructions
```dockerfile
FROM        # to specify the base image
WORKDIR     # to set the working directory
COPY        # to copy files/directories
ADD         # to copy files/directories
RUN         # to run commands
ENV         # to set environment variables
EXPOSE      # to document the port the container is listening on
USER        # to set the user running the app
CMD         # to set the default command/program
ENTRYPOINT  # to set the default command/program
```

### Image commands
```dockerfile
docker build -t <name> .
docker images
docker image ls
docker run -it <image> sh
```

### Starting and stopping containers
```dockerfile
docker stop <containerID>
docker start <containerID>
```

### Removing containers
```dockerfile
docker container rm <containerID>
docker rm <containerID>
docker rm -f <containerID>      # to force the removal
docker container prune          # to remove stopped containers
```

### Volumes
```dockerfile
docker volume ls
docker volume create app-data
docker volume inspect app-data
docker run -v app-data:/app/data <image>
```

### Copying files between the host and containers
```dockerfile
docker cp <containerID>:/app/log.txt .
docker cp secret.txt <containerID>:/app
```

### Sharing source code with containers
```dockerfile
docker run -v $(pwd):/app <image>
```

## Containers
### Running containers
```dockerfile
docker run <image>
docker run -d <image>              # run in the background
docker run —name <name> <image>    # to give a custom name
docker run —p 3000:3000 <image>    # to publish a port HOST:CONTAINER
```

### Listing containers
```dockerfile
docker ps           # to list running containers
docker ps -a        # to list all containers

```


### Viewing the logs
```dockerfile
docker logs <containerID>
docker logs -f <containerID>        # to follow the log
docker logs —t <containerID>        # to add timestamps
docker logs —n 10 <containerID>     # to view the last 10 lines
```

### Executing commands in running containers
```dockerfile
docker exec <containerID> <cmd>
docker exec -it <containerID> sh    # to start a shell
```

### Starting and stopping containers
```dockerfile
docker stop <containerID>
docker start <containerID>
```

### Removing containers
```dockerfile
docker container rm <containerID>
docker rm <containerID>
docker rm -f <containerID>         # to force the removal
docker container prune             # to remove stopped containers
```

### Volumes
```dockerfile
docker volume ls
docker volume create app-data
docker volume inspect app-data
docker run -v app-data:/app/data <image>
```

### Copying files between the host and containers
```dockerfile
docker cp <containerID>:/app/log.txt .
docker cp secret.txt <containerID>:/app
```

### Sharing source code with containers
```dockerfile
docker run -v $(pwd):/app <image>
```

## Multi-containers apps
### Docker Compose commands
```CMD
docker-compose build
docker-compose build --no-cache
docker-compose up
docker-compose up -d
docker-compose up —build
docker-compose down
docker-compose ps
docker-compose logs
```



