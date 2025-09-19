# Docker Service Hardening

Deployment Guide for Docker Service Hardening

## Prerequisites
- Docker and Docker Compose installed on your system.
- Superuser (sudo) access to create directories on the host.

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone git@github.com:jrafaelca/docker-service-hardening.git
   cd docker-service-hardening
   ```

2. **Set environment variables:**
   Copy the example file and set your own secure values:
   ```bash
   cp .env.example .env
   # Edit .env and set your own passwords
   ```

## Steps to launch the environment

### 1. Prepare the directory for Traefik SSL certificates
Run the preparation script (on your host machine):

```bash
sudo mkdir -p /opt/docker/letsencrypt
sudo touch /opt/docker/letsencrypt/acme.json
sudo chmod 600 /opt/docker/letsencrypt/acme.json
```

This will create `/opt/docker/letsencrypt/acme.json` on your host with the correct permissions.

### 2. Start the services
From the project root:

```bash
docker compose up -d
```

This will start the defined services (Traefik, MariaDB, Valkey, etc.).

### 3. Check the status
You can view the service logs with:

```bash
docker compose logs -f
```

### 4. Stop the services
```bash
docker compose down
```

---

## Notes
- Make sure ports 80 and 443 are free on your host.
- The `/opt/docker/letsencrypt` directory must exist on the host before starting Traefik.
- If you need to add more services, edit `docker-compose.yml` and update `.env` as needed.

---

Questions? Contact the project administrator.
