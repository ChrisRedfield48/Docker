# 🐳 Docker Playground

A collection of small, self-contained example projects showing how to containerize applications written in different languages and frameworks using Docker.

Each folder is an independent example — pick the stack you're interested in, `cd` into it, and build the image.

## 📦 What's inside

| Folder | Stack |
| --- | --- |
| [`MyApp`](./MyApp) | General example app |
| [`cpp-docker`](./cpp-docker) | C++ |
| [`cpp-fltk`](./cpp-fltk) | C++ with FLTK (GUI toolkit) |
| [`cpp-ftxui`](./cpp-ftxui) | C++ with FTXUI (terminal UI) |
| [`ftxui-wow`](./ftxui-wow) | C++ / FTXUI extended example |
| [`my-java-app`](./my-java-app) | Java |
| [`my-node-app`](./my-node-app) | Node.js |
| [`my-python-app`](./my-python-app) | Python |
| [`my-ts-app`](./my-ts-app) | TypeScript |
| [`my-website`](./my-website) | Static website |
| [`pascal-app`](./pascal-app) | Pascal |
| [`php-docker`](./php-docker) | PHP |
| [`qt-docker-app`](./qt-docker-app) | Qt5 |
| [`qt6-docker-app`](./qt6-docker-app) | Qt6 |
| [`ruby-app`](./ruby-app) | Ruby |
| [`rust-docker`](./rust-docker) | Rust |
| [`simple_flask_app`](./simple_flask_app) | Python / Flask |

## 🚀 Quick start

Every example follows roughly the same workflow:

```bash
# Go into the example you want to run
cd <folder-name>

# Build the image
docker build -t <folder-name> .

# Run the container
docker run --rm -it <folder-name>
```

Check each subfolder for its own `Dockerfile` and any extra setup notes (exposed ports, environment variables, etc.), since requirements vary between languages.

## 🎯 Purpose

This repository serves as a personal reference and learning playground for:

- Writing `Dockerfile`s for a variety of languages and toolchains (compiled, interpreted, GUI, and terminal-based apps)
- Comparing image size and build strategies across ecosystems
- Having ready-to-copy boilerplate for future projects

## 🛠 Requirements

- [Docker](https://docs.docker.com/get-docker/) installed and running
- For GUI-based examples (FLTK, Qt), an X11 server or equivalent display forwarding set up on your host if you want to run them with a visible window

## 📄 License

No license specified yet — treat this as personal/example code unless a license file is added.