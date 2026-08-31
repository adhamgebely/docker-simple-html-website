# 🐳 Containerized HTML Website using Nginx & Docker

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Containerized-2496ED?logo=docker" alt="Docker">
  <img src="https://img.shields.io/badge/Nginx-Web%20Server-009639?logo=nginx" alt="Nginx">
  <img src="https://img.shields.io/badge/HTML-Static%20Website-E34F26?logo=html5" alt="HTML">
</p>

A simple DevOps project demonstrating how to deploy a static HTML website using **Nginx inside a Docker container**.

The project shows the basic workflow of containerizing a web application:

```text
HTML/CSS Files
        |
        ↓
Dockerfile
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

        Static HTML / CSS Website
```

The application flow:

1. User sends an HTTP request from the browser.
2. Nginx running inside Docker receives the request.
3. Nginx serves the static website files.
4. The website is displayed in the browser.

---

# ✨ Features

- Static HTML website deployment
- Nginx web server
- Docker containerization
- Lightweight deployment
- Easy local setup
- Portable environment

---

# 🛠 Technologies Used

- HTML
- CSS
- Nginx
- Docker
- Linux
- Git & GitHub

---

# 📁 Project Structure

```text
docker-simple-html-website/

├── Dockerfile
├── index.html
├── css/
│
├── images/
│
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

## Dockerfile Explanation

| Instruction | Description |
|---|---|
| FROM | Uses the official Nginx image |
| COPY | Copies website files into Nginx web directory |
| EXPOSE | Opens port 80 for HTTP traffic |

---

# 🚀 Run the Project

## 1. Clone Repository

```bash
git clone https://github.com/adhamgebely/docker-simple-html-website.git
```

Move into the project:

```bash
cd docker-simple-html-website
```

---

## 2. Build Docker Image

```bash
docker build -t html-website .
```

Check created images:

```bash
docker images
```

---

## 3. Run Container

Run the website:

```bash
docker run -d -p 8080:80 --name website html-website
```

Check running containers:

```bash
docker ps
```

---

# 🌐 Access Website

Open your browser:

```text
http://localhost:8080
```

---

# 📸 Website Preview

<p align="center">
  <img src="screenshots/website-preview.png" width="850">
</p>

---

# 🐳 Container Management Commands

## View running containers

```bash
docker ps
```

## View container logs

```bash
docker logs website
```

## Stop container

```bash
docker stop website
```

## Remove container

```bash
docker rm website
```

## Remove image

```bash
docker rmi html-website
```

---

# 🧹 Cleanup

Remove stopped containers:

```bash
docker container prune
```

Remove unused images:

```bash
docker image prune
```

---

# 🎯 Learning Objectives

Through this project:

- Learned Docker image creation
- Deployed a static website using Nginx
- Understood container ports mapping
- Learned basic Docker workflow
- Practiced container lifecycle management

---

# 👨‍💻 Author

**Adham Gebely**

GitHub:

https://github.com/adhamgebely

---

⭐ If you found this project useful, consider giving it a star.
