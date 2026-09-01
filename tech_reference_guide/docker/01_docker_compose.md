# 📦 Docker Compose Cheat Sheet

## 🚀 Common Commands

| Action | Command | Description |
| :--- | :--- | :--- |
| **Start All** | `docker compose up -d` | Create and start containers in background |
| **Stop All** | `docker compose down` | Stop and remove containers, networks |
| **Stop All (Keep Vol)** | `docker compose down -v` | Stop and remove containers AND volumes |
| **Restart** | `docker compose restart` | Restart all services |
| **Build/Rebuild** | `docker compose up -d --build` | Force rebuild images before starting |
| **Check Status** | `docker compose ps` | List status of services in current file |
| **View Logs** | `docker compose logs -f` | Follow logs for all services |
| **Run One-off** | `docker compose exec <service> <cmd>` | Run command in a specific service |

## 📄 docker-compose.yml Example
```yaml
version: '3.8'
services:
  api:
    build: ./api
    ports:
      - "3000:3000"
    environment:
      - DB_HOST=db
    depends_on:
      - db

  db:
    image: postgres:15-alpine
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
      POSTGRES_DB: mydb
    volumes:
      - pgdata:/var/lib/postgresql/data

volumes:
  pgdata:
```
