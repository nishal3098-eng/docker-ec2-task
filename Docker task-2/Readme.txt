# Docker Task 2 — Personal Details Website

A static website displaying personal details, containerized using Docker 
and Docker Compose, deployed on AWS EC2.

## Tech Stack
- AWS EC2 (Amazon Linux 2023)
- Docker
- Docker Compose
- Nginx (Alpine)

## Project Files
- `index.html` — Personal details webpage
- `Dockerfile` — Builds an Nginx image with the HTML
- `docker-compose.yml` — Service definition

## How to Run

\`\`\`bash
docker-compose up -d --build
\`\`\`

Visit `http://<EC2-PUBLIC-IP>` in a browser.

## Screenshots
See the `screenshots/` folder.