## 🐳 Useful Docker Commands

### 🔹 Container Lifecycle

| Command | Description |
|--------|-------------|
| `docker run -it ubuntu` | Run a container interactively from the `ubuntu` image |
| `docker start <container>` | Start a stopped container |
| `docker stop <container>` | Stop a running container |
| `docker restart <container>` | Restart a container |
| `docker rm <container>` | Remove a stopped container |
| `docker kill <container>` | Force-stop a running container |
| `docker exec -it <container> bash` | Run a command (e.g., `bash`) inside a running container |
| `docker attach <container>` | Attach terminal to a running container |

---

### 🔹 Images

| Command | Description |
|--------|-------------|
| `docker pull <image>` | Download an image from Docker Hub |
| `docker build -t myimage .` | Build an image from a Dockerfile in the current directory |
| `docker images` | List all local images |
| `docker rmi <image>` | Remove an image |
| `docker tag <image> user/repo:tag` | Tag an image for upload to registry |
| `docker push user/repo:tag` | Push an image to a Docker registry |

---

### 🔹 Container Info and Logs

| Command | Description |
|--------|-------------|
| `docker ps` | List running containers |
| `docker ps -a` | List all containers (including stopped) |
| `docker logs <container>` | Show logs from a container |
| `docker inspect <container>` | Show detailed info about container or image |
| `docker top <container>` | Show running processes inside container |
| `docker stats` | Show live resource usage stats of containers |

---

### 🔹 Volumes and Networks

| Command | Description |
|--------|-------------|
| `docker volume create myvol` | Create a named volume |
| `docker volume ls` | List volumes |
| `docker volume rm myvol` | Remove a volume |
| `docker network ls` | List networks |
| `docker network inspect <network>` | Show details of a Docker network |

---

### 🔹 System Cleanup

| Command | Description |
|--------|-------------|
| `docker system df` | Show disk usage by images, containers, etc. |
| `docker system prune` | Remove unused containers, networks, images |
| `docker image prune` | Remove unused images |
| `docker container prune` | Remove all stopped containers |
| `docker volume prune` | Remove all unused volumes |

---

### 🔹 Compose (if using `docker-compose`)

| Command | Description |
|--------|-------------|
| `docker-compose up` | Start services defined in `docker-compose.yml` |
| `docker-compose up -d` | Start services in the background |
| `docker-compose down` | Stop and remove services, networks, etc. |
| `docker-compose logs` | Show logs for all services |
| `docker-compose exec <service> bash` | Execute command inside a service container |