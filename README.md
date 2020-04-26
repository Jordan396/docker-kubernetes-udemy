# docker-kubernetes-udemy

## Commands

### Docker
- Create and start a container: `docker run <image-name>`
- Create a container: `docker create <image-name> <image-command>`
- Start a container: `docker start -a <container-id>`
- Remove stopped containers: `docker system prune`
- List all containers: `docker ps --all`
- Retrieving logs: `docker logs <container-id>`
- Stop a container: `docker stop <container-id>`
![stop](/img/docker-stop.png)
- Kill a container: `docker kill <container-id>`
![kill](/img/docker-kill.png)
- Execute a command in a container: `docker exec -it <container-id> <command> / sh(shell)`
- Copy from local to container: `docker cp <local-file> <container-id>:<filepath in container>`
- Port mapping from machine port to container port: `docker run -p <machine-port>:<container-port> <container-id>`

### Docker Compose
- Running multiple containers with networking: `docker-compose up`
![compose](/img/docker-compose.png)
- Rebuild above images: `docker-compose up --build`
- Running multiple containers with networking in background: `docker-compose up -d`
- Stop containers: `docker-compose down`
- List docker compose containers: `docker-compose ps`. Note, this command relies on the docker-compose.yml file.

## Notes
- Use base image with tag alpine for an image with minimal unnecessary packages
- Docker restart policies
![restart policies](/img/docker-restart-policies.png)