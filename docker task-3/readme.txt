# Docker Task 3 — Custom Nginx Image with Bind Mount

A custom Nginx Docker image built and deployed using Docker Compose on AWS EC2 
with a host bind mount at `/var/opt/nginx`. The image is published to Docker Hub.

## Tech Stack
- AWS EC2 (Amazon Linux 2023)
- Docker
- Docker Compose
- Nginx (Alpine)

## Docker Hub
**Image**: `nishal3098/custom-nginx:v1`  
**Link**: https://hub.docker.com/r/nishal3098/custom-nginx

## Project Files
| File | Description |
|------|-------------|
| `Dockerfile` | Custom Nginx image definition |
| `docker-compose.yml` | Service with bind mount at /var/opt/nginx |
| `index.html` | Webpage served from the bind mount |

## How to Run

### Option A: Build locally
\`\`\`bash
sudo mkdir -p /var/opt/nginx
sudo cp index.html /var/opt/nginx/
docker-compose up -d --build
\`\`\`

### Option B: Pull from Docker Hub
\`\`\`bash
docker pull nishal3098/custom-nginx:v1
docker run -d --name custom-nginx -p 80:80 \\
  -v /var/opt/nginx:/var/opt/nginx \\
  nishal3098/custom-nginx:v1
\`\`\`

Visit `http://<EC2-PUBLIC-IP>` in a browser.

## Screenshots
See the `screenshots/` folder.