# 🐳 Docker Basics Cheat Sheet

## 🚀 Common Commands

### Container Management
| Action | Command | Description |
| :--- | :--- | :--- |
| **Run** | `docker run -d -p 80:80 --name my_app image_name` | Run container in background with port mapping |
| **List Running** | `docker ps` | List all active containers |
| **List All** | `docker ps -a` | List all containers (including stopped) |
| **Stop** | `docker stop <container_id>` | Gracefully stop a container |
| **Start** | `docker start <container_id>` | Start a stopped container |
| **Remove** | `docker rm -f <container_id>` | Force remove a container |
| **Logs** | `docker logs -f <container_id>` | Follow container output |
| **Shell Access** | `docker exec -it <container_id> sh` | Open interactive shell inside container |

### Image Management
| Action | Command | Description |
| :--- | :--- | :--- |
| **Pull** | `docker pull <image>` | Download image from registry |
| **List Images** | `docker images` | List all local images |
| **Build** | `docker build -t <name>:<tag> .` | Build image from Dockerfile in current dir |
| **Remove** | `docker rmi <image_id>` | Remove a local image |
| **Prune** | `docker system prune -a` | Remove all unused containers, networks, and images |

## 🛠️ Dockerfile Quick Reference
```dockerfile
# Base image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy dependencies first for caching
COPY package*.json ./
RUN npm install

# Copy rest of the code
COPY . .

# Expose port
EXPOSE 3000

# Start command
CMD ["npm", "start"]
```
