# 💾 Docker Volume Commands Cheat Sheet

A complete reference of Docker volume commands to help you manage persistent data inside containers 🐳

---

## 📦 Volume Basics

| Command | Description |
|---------|-------------|
| `docker volume create` | Create a new volume |
| `docker volume create my-volume` | Create a volume with a custom name |
| `docker volume ls` | List all volumes |
| `docker volume inspect <volume>` | Show detailed info about a volume |
| `docker volume rm <volume>` | Remove a specific volume |
| `docker volume prune` | Remove all **unused** volumes |

---

## 📁 Using Volumes with Containers

| Command | Description |
|---------|-------------|
| `docker run -v my-volume:/app/data alpine` | Mount a volume to a path inside the container |
| `docker run -v $(pwd):/app` | Mount a **host directory** into the container |
| `docker run -v my-volume:/app -it ubuntu bash` | Run an Ubuntu container and attach a named volume |
| `docker run --mount source=my-volume,target=/data` | Modern alternative using `--mount` syntax |

---

## 🧪 Working with Volume Data

| Command | Description |
|---------|-------------|
| `docker run -v my-volume:/data busybox ls /data` | View contents of the volume |
| `docker run -v my-volume:/data busybox sh -c "echo hello > /data/hello.txt"` | Write data into a volume |
| `docker run -v my-volume:/data busybox cat /data/hello.txt` | Read data from a volume |

---

## 🔍 Inspecting Volumes

| Command | Description |
|---------|-------------|
| `docker volume inspect my-volume` | Check mountpoint, driver, usage, etc. |
| `ls /var/lib/docker/volumes/` | (Linux) View stored volume data directly (not portable) |
| `docker inspect <container>` | See how volumes are mounted inside containers |

---

## 🔗 Quick Tips

- Volumes are **managed by Docker** and are safer than binding to host paths
- Volumes **persist data** even if containers are deleted
- You can share volumes between multiple containers

---

## 🔗 Useful Links

- [Docker Volumes - Official Docs](https://docs.docker.com/storage/volumes/)
- [Bind Mounts vs Volumes](https://docs.docker.com/storage/)
- [Docker CLI Reference](https://docs.docker.com/engine/reference/commandline/volume/)

---

Use volumes to keep your data safe, portable, and production-ready! 💾🐳
