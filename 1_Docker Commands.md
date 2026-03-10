---
# 🐳 Docker One-Page Command Cheat Sheet (Top 40)
---
<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/f3d1ae7f-72f6-40a3-8242-bfd9e7e78841" />

# 1️⃣ Docker Setup & Info

| Command            | Purpose                    |
| ------------------ | -------------------------- |
| `docker --version` | Show Docker version        |
| `docker info`      | Display system information |
| `docker help`      | List Docker commands       |

---

# 2️⃣ Image Management

| Command                        | Purpose                     |
| ------------------------------ | --------------------------- |
| `docker search nginx`          | Search images on Docker Hub |
| `docker pull nginx`            | Download an image           |
| `docker images`                | List images                 |
| `docker rmi image_name`        | Remove image                |
| `docker tag image new_tag`     | Tag image                   |
| `docker push image_name`       | Push image to Docker Hub    |
| `docker build -t image_name .` | Build image from Dockerfile |

Example:

```bash
docker pull nginx
docker images
```

Uses the NGINX image.

---

# 3️⃣ Container Creation

| Command                             | Purpose               |
| ----------------------------------- | --------------------- |
| `docker run image`                  | Run container         |
| `docker run -d image`               | Run in background     |
| `docker run --name container image` | Assign container name |
| `docker run -p 8080:80 image`       | Port mapping          |
| `docker run -it image bash`         | Interactive terminal  |
| `docker run -e VAR=value image`     | Environment variable  |
| `docker run -v volume:/data image`  | Attach volume         |

Example:

```bash
docker run -d --name web -p 8080:80 nginx
```

---

# 4️⃣ Container Management

| Command                    | Purpose                 |
| -------------------------- | ----------------------- |
| `docker ps`                | Show running containers |
| `docker ps -a`             | Show all containers     |
| `docker stop container`    | Stop container          |
| `docker start container`   | Start container         |
| `docker restart container` | Restart container       |
| `docker rm container`      | Remove container        |
| `docker rm -f container`   | Force remove container  |

Example:

```bash
docker stop web
docker rm web
```

---

# 5️⃣ Container Debugging

| Command                          | Purpose                       |
| -------------------------------- | ----------------------------- |
| `docker logs container`          | Show logs                     |
| `docker logs -f container`       | Follow logs                   |
| `docker exec -it container bash` | Access container shell        |
| `docker inspect container`       | Detailed container info       |
| `docker top container`           | Show running processes        |
| `docker stats`                   | Show container resource usage |

Example:

```bash
docker logs web
docker exec -it web bash
```

---

# 6️⃣ Networking

| Command                               | Purpose         |
| ------------------------------------- | --------------- |
| `docker network ls`                   | List networks   |
| `docker network create network_name`  | Create network  |
| `docker network inspect network_name` | Inspect network |
| `docker network rm network_name`      | Remove network  |

Example:

```bash
docker network create my-network
```

---

# 7️⃣ Volumes & Storage

| Command                             | Purpose        |
| ----------------------------------- | -------------- |
| `docker volume ls`                  | List volumes   |
| `docker volume create volume_name`  | Create volume  |
| `docker volume inspect volume_name` | Inspect volume |
| `docker volume rm volume_name`      | Remove volume  |

Example:

```bash
docker volume create mysql-data
```

Used with databases like MySQL.

---

# 8️⃣ System Cleanup

| Command                  | Purpose                   |
| ------------------------ | ------------------------- |
| `docker system df`       | Show disk usage           |
| `docker system prune`    | Remove unused data        |
| `docker container prune` | Remove stopped containers |
| `docker image prune`     | Remove unused images      |
| `docker volume prune`    | Remove unused volumes     |

Example:

```bash
docker system prune
```

---

# 9️⃣ Useful Developer Shortcuts

Stop all containers:

```bash
docker stop $(docker ps -q)
```

Remove all containers:

```bash
docker rm $(docker ps -a -q)
```

Remove all images:

```bash
docker rmi $(docker images -q)
```

---

# 🧠 Docker Mental Model

```
Image → Blueprint
Container → Running app
Volume → Persistent storage
Network → Communication
Dockerfile → Build instructions
```

---

✅ **Developer Tip**

Most developers use these **10 commands daily**:

```
docker pull
docker build
docker run
docker ps
docker ps -a
docker stop
docker rm
docker logs
docker exec -it
docker system prune
```

---
