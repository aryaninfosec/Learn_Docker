# 🐳 Docker Image Commands Cheat Sheet

A handy reference for all essential `docker image` commands. Learn to pull, build, tag, inspect, and manage Docker images like a pro 🚀

---

## 📦 Docker Image Management Commands

| Command | Description |
|---------|-------------|
| `docker pull <image>` | Download an image from Docker Hub |
| `docker images` | List all local images |
| `docker rmi <image_id>` | Remove a local image |
| `docker rmi -f <image_id>` | Force remove an image even if in use |
| `docker image prune` | Remove all unused images |
| `docker image ls` | Alias for `docker images` |
| `docker image rm <image>` | Alias for `docker rmi` |

---

## 🛠️ Build & Tag Images

| Command | Description |
|---------|-------------|
| `docker build .` | Build an image from a Dockerfile in the current directory |
| `docker build -t my-image .` | Build and tag the image as `my-image` |
| `docker build -f path/to/Dockerfile .` | Build using a specific Dockerfile |
| `docker tag <image> <new_name>` | Add a new name/tag to an existing image |
| `docker build -t my-image:v1.0 .` | Build an image and tag with version |

---

## 🔍 Inspect & Analyze Images

| Command | Description |
|---------|-------------|
| `docker inspect <image>` | View detailed JSON metadata about the image |
| `docker history <image>` | Show history of image layers |
| `docker image inspect <image>` | Alias for `docker inspect` (specifically for images) |
| `docker image history <image>` | Alias for `docker history` |

---

## 📤 Export & Load Images

| Command | Description |
|---------|-------------|
| `docker save -o image.tar <image>` | Save image as a tarball archive |
| `docker load -i image.tar` | Load an image from a tarball archive |
| `docker export <container>` | Export a container’s filesystem (not same as image) |
| `docker import <file>` | Import image from a tar archive (alternative to `load`) |

---

## 🔗 Useful Tips

- Images are based on **layers** and are **immutable**
- You can tag images with version numbers for better management
- Use `docker system prune -a` to remove all unused containers, images, networks, and volumes

---

## 🔗 Useful Links

- [Docker Images - Official Docs](https://docs.docker.com/engine/reference/commandline/image/)
- [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)
- [Docker Hub](https://hub.docker.com/)

---

Stay sharp. Tag your images. Prune responsibly. 🐳🔥  
