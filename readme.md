# 🐳 Docker Playground

<p align="center">
  <img src="https://img.shields.io/badge/Docker-ready-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Ready">
  <img src="https://img.shields.io/badge/Languages-16-informational?style=for-the-badge" alt="16 Languages">
  <img src="https://img.shields.io/badge/License-Unlicensed-lightgrey?style=for-the-badge" alt="No License">
</p>

<p align="center">
  A collection of small, self-contained example projects showing how to <b>containerize applications</b> written in different languages and frameworks using Docker.
</p>

<p align="center">
  Each folder is an independent example — pick a stack, <code>cd</code> in, and build the image.
</p>

---

## 📦 What's inside

| Folder | Stack |
| :-- | :-- |
| [`MyApp`](./MyApp) | 🧩 General example app |
| [`cpp-docker`](./cpp-docker) | ⚙️ C++ |
| [`cpp-fltk`](./cpp-fltk) | 🖼️ C++ with FLTK (GUI toolkit) |
| [`cpp-ftxui`](./cpp-ftxui) | 🖥️ C++ with FTXUI (terminal UI) |
| [`ftxui-wow`](./ftxui-wow) | 🖥️ C++ / FTXUI extended example |
| [`my-java-app`](./my-java-app) | ☕ Java |
| [`my-node-app`](./my-node-app) | 🟢 Node.js |
| [`my-python-app`](./my-python-app) | 🐍 Python |
| [`my-ts-app`](./my-ts-app) | 🔷 TypeScript |
| [`my-website`](./my-website) | 🌐 Static website |
| [`pascal-app`](./pascal-app) | 🅿️ Pascal |
| [`php-docker`](./php-docker) | 🐘 PHP |
| [`qt-docker-app`](./qt-docker-app) | 🎛️ Qt5 |
| [`qt6-docker-app`](./qt6-docker-app) | 🎛️ Qt6 |
| [`ruby-app`](./ruby-app) | 💎 Ruby |
| [`rust-docker`](./rust-docker) | 🦀 Rust |
| [`simple_flask_app`](./simple_flask_app) | 🧪 Python / Flask |

---

## 🚀 Quick start

Every example follows roughly the same workflow:

```bash
# 1. Go into the example you want to run
cd <folder-name>

# 2. Build the image
docker build -t <folder-name> .

# 3. Run the container
docker run --rm -it <folder-name>
```

> 💡 Check each subfolder for its own `Dockerfile` and any extra setup notes (exposed ports, environment variables, etc.) — requirements vary between languages.

---

## 🎯 Purpose

This repository serves as a personal reference and learning playground for:

- ✍️ Writing `Dockerfile`s for a variety of languages and toolchains (compiled, interpreted, GUI, and terminal-based apps)
- 📊 Comparing image size and build strategies across ecosystems
- 📎 Having ready-to-copy boilerplate for future projects

---

## 🛠 Requirements

- [Docker](https://docs.docker.com/get-docker/) installed and running
- For GUI-based examples (FLTK, Qt), an X11 server or equivalent display forwarding set up on your host if you want to run them with a visible window

---

## 📚 Docker theory cheat sheet

<details>
<summary><b>Click to expand — containerization basics & command reference</b></summary>

### Container vs Virtual Machine

| | Container | Virtual Machine |
| :-- | :-- | :-- |
| **Isolation level** | Process-level, shares host OS kernel | Full OS, own kernel |
| **Startup time** | Seconds (or less) | Minutes |
| **Size** | MBs | GBs |
| **Overhead** | Minimal | Significant (hypervisor + guest OS) |
| **Use case** | Fast, lightweight, disposable environments | Full OS isolation, running different kernels |

### Core building blocks

- **Dockerfile** — a text file with step-by-step instructions describing how to build an image (base image, dependencies, files, commands to run).
- **Image** — a read-only, versioned snapshot built from a Dockerfile. Think of it as a blueprint or class.
- **Container** — a running (or stopped) instance of an image. Think of it as an object instantiated from that class.

### `.dockerignore`

Excludes files/folders from the build context (similar to `.gitignore`), keeping images smaller and builds faster — e.g. `node_modules`, `.git`, local env files.

### Volumes

Persistent storage that lives outside a container's writable layer, so data survives container removal/recreation. Useful for databases, uploads, or any state you don't want to lose when a container is torn down.

### Handy command reference

```bash
# Build an image from a Dockerfile in the current directory
docker build -t <image-name> .

# Run a container from an image
docker run --rm -it <image-name>

# List running containers
docker ps

# List all containers (including stopped)
docker ps -a

# List local images
docker images

# Stop a running container
docker stop <container-id>

# Remove a container
docker rm <container-id>

# Remove an image
docker rmi <image-name>

# View container logs
docker logs <container-id>

# Start a shell inside a running container
docker exec -it <container-id> sh

# Compose: start services defined in docker-compose.yml
docker compose up

# Compose: stop and remove containers, networks (and volumes with -v)
docker compose down -v
```

> ⚠️ The `-v` flag on `docker compose down` also removes any named volumes declared in the compose file — use it when you want a truly clean slate (e.g. resetting a database), but skip it if you want to keep persisted data between runs.

</details>

---

## 📄 License

No license specified yet — treat this as personal/example code unless a license file is added.

---

<p align="center">
  <i>Built as a personal learning playground for containerizing everything under the sun.</i> 🐳
</p>