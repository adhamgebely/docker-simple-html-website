# 🐳 Containerized HTML Website using Nginx & Docker

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Containerized-2496ED?logo=docker" alt="Docker">
  <img src="https://img.shields.io/badge/Nginx-Web%20Server-009639?logo=nginx" alt="Nginx">
  <img src="https://img.shields.io/badge/HTML-Static%20Website-E34F26?logo=html5" alt="HTML">
</p>

A simple DevOps project demonstrating how to deploy a static HTML website using **Nginx inside a Docker container**.

The project covers the complete containerization workflow:

```text
HTML Website
      |
      ↓
Docker Image
      |
      ↓
Nginx Container
      |
      ↓
Web Browser
```

---

# 🏗 Architecture

```text
             User Browser

                  |
                  |
                  ↓

          Nginx Docker Container

                  |
                  |
                  ↓

        Static HTML Website Files
```

---

# ✨ Features

- Static HTML website deployment
- Nginx web server
- Docker image creation
- Container-based deployment
- Portable development environment
- Simple production-style workflow

---

# 🛠 Technologies Used

- HTML
- Nginx
- Docker
- Linux
- Git & GitHub

---

# 📁 Project Structure

```text
docker-simple-html-website/

├── index.html
├── Dockerfile
├── screenshots/
│   ├── website-html-code.png
│   ├── docker-container-running.png
│   └── website-preview.png
└── README.md
```

---

# 🐳 Dockerfile

The project uses the official Nginx image:

```dockerfile
FROM nginx:latest

COPY . /usr/share/nginx/html

EXPOSE 80
```

## Explanation

| Command | Purpose |
|---|---|
| FROM | Uses official Nginx image |
| COPY | Copies website files into Nginx directory |
| EXPOSE | Opens HTTP port |

---

# 📄 Website Files

The website is built using simple HTML files.

<p align="center">
  <img src="screenshots/website-html-code.png" width="850">
</p>

---

# 🚀 Run the Project

## Clone Repository

```bash
git clone https://github.com/adhamgebely/docker-simple-html-website.git
```

Move into project folder:

```bash
cd docker-simple-html-website
```

---

## Build Docker Image

```bash
docker build -t html-website .
```

Check images:

```bash
docker images
```

---

## Create and Run Container

```bash
docker run -d -p 8080:80 --name website html-website
```

Running container:

<p align="center">
  <img src="screenshots/docker-container-running.png" width="850">
</p>

---

# 🌐 Website Preview

Open:

```text
http://localhost:8080
```

<p align="center">
  <img src="screenshots/website-preview.png" width="850">
</p>

---

# 📋 Useful Docker Commands

View containers:

```bash
docker ps
```

View logs:

```bash
docker logs website
```

Stop container:

```bash
docker stop website
```

Remove container:

```bash
docker rm website
```

Remove image:

```bash
docker rmi html-website
```

---

# 🎯 Learning Objectives

Through this project:

- Learned Docker image creation
- Deployed static websites using Nginx
- Practiced container port mapping
- Understood Docker container lifecycle
- Learned basic DevOps deployment workflow

---

# 👨‍💻 Author

**Adham Gebely**

GitHub:
https://github.com/adhamgebely
