## 👋 Welcome to forgejo 🚀

Self-hosted Git service with web interface (Gitea fork)

## 📋 Description

Self-hosted Git service with web interface (Gitea fork)

## 🚀 Services

- **forgejo**: codeberg.org/forgejo/forgejo:latest

### Infrastructure Components

- **forgejo-db**: Postgres database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/forgejo/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/forgejo" ~/.local/srv/docker/forgejo
cd ~/.local/srv/docker/forgejo
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install forgejo
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
DB_USER_NAME=forgejo
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:3002

## 📂 Volumes

- `./rootfs/data/forgejo` - Data storage
- `./rootfs/config/forgejo` - Data storage
- `./rootfs/data/db/postgres/forgejo` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f forgejo
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
