# Docker on AWS EC2

This project demonstrates installing Docker on an AWS EC2 instance and exploring 
core Docker commands: images, containers, volumes, and networks.

## Tech Stack
- AWS EC2 (Amazon Linux 2023)
- Docker

## Steps Performed

### 1. Launched EC2 Instance
![EC2 Running](screenshots/1-ec2-running.png)

### 2. Installed Docker
Commands used:
\`\`\`bash
sudo yum update -y
sudo yum install -y docker
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ec2-user
\`\`\`
![Docker Version](screenshots/2-docker-version.png)

### 3. Docker Images
\`\`\`bash
docker pull nginx
docker images
docker inspect nginx
\`\`\`
![Docker Images](screenshots/3-docker-images.png)

### 4. Docker Containers
\`\`\`bash
docker run -d --name web -p 80:80 nginx
docker ps
docker logs web
\`\`\`
![Docker Containers](screenshots/4-docker-containers.png)

### 5. Docker Volumes
\`\`\`bash
docker volume create mydata
docker volume ls
docker volume inspect mydata
\`\`\`
![Docker Volumes](screenshots/5-docker-volumes.png)

### 6. Docker Networks
\`\`\`bash
docker network create mynet
docker run -d --name c1 --network mynet nginx
docker run -d --name c2 --network mynet nginx
docker exec c1 ping -c 3 c2
\`\`\`
![Docker Network](screenshots/6-docker-network.png)

## Conclusion
Successfully installed Docker on EC2 and explored images, containers, volumes, and networks.
