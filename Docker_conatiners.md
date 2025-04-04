# Learn_Docker

# basic Docker commands:-

1. To see running containers: docker ps
2. To stop conatiner : docker stop <container_id>
3. To delete container: docker rm <container_id>


# 🐳 Docker Run Commands Cheat Sheet

This is a quick reference for common and essential `docker run` commands. Great for beginners and pros alike 🚀

---

## 📦 Basic Docker Run Commands

| Command | Description |
|---------|-------------|
| `docker run hello-world` | Run a test container to verify Docker is installed correctly |
| `docker run -it ubuntu` | Start Ubuntu container with interactive terminal |
| `docker run -it ubuntu /bin/bash` | Open an interactive Bash shell inside Ubuntu |
| `docker run -d nginx` | Run NGINX container in detached (background) mode |
| `docker run --rm ubuntu echo "Hi"` | Auto-remove container after it exits |
| `docker run -p 8080:80 nginx` | Map host port 8080 to container port 80 |
| `docker run -v $(pwd):/app alpine` | Mount current directory into `/app` in container |
| `docker run --name my-container nginx` | Name your container for easier reference |
| `docker run -e VAR=value ubuntu` | Set environment variable inside container |
| `docker run --entrypoint /bin/sh alpine` | Override default entrypoint (e.g., to debug) |
| `docker run --network my-network nginx` | Attach container to a specific Docker network |
| `docker run -u $(id -u):$(id -g) alpine` | Run container as the host user |
| `docker run --cpus="1.5" --memory="512m" ubuntu` | Limit container CPU and memory usage |
| `docker run -it --rm node:18 node` | Start a temporary Node.js REPL container |

---

## 🧹 Container Cleanup Commands

| Command | Description |
|---------|-------------|
| `docker stop <container_id>` | Stop a running container |
| `docker rm <container_id>` | Remove a stopped container |
| `docker container prune` | Remove all stopped containers |

---

## 🧠 Pro Tips

- Use `docker ps` to list running containers  
- Use `docker ps -a` to list all containers (including stopped)  
- Use `docker images` to see downloaded images  
- Use `docker rmi <image_id>` to delete an image  
- Use `docker run --help` to see all available options

---

## 🔗 Useful Links

- [Official Docker Docs](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Play with Docker (Online Sandbox)](https://labs.play-with-docker.com/)

---

Happy Dockering! 🐳✨  
Feel free to fork & star ⭐ this
