---
id: pg-docs-selfhost
title: Self-Hosting & Production Deployment 🐳
icon: 🐳
tags: [selfhost, docker, deployment, devops, privacy, on-premise]
createdAtDaysAgo: 70
updatedAtDaysAgo: 1
---

> 💡 Doction is designed to be completely sovereign. You can run it on your local machine, deploy it in a private Docker container, or host it on your company's air-gapped intranet server.

---

## 1. Quick Start: Single Container (Localhost / Private VPS)

To spin up a self-hosted instance in seconds:

```bash
docker run -d \
  --name doction \
  -p 3000:3000 \
  --restart unless-stopped \
  doction/doction:latest
```

Open your browser at `http://localhost:3000`. Your workspace is live, fully functional, and ready to use!

---

## 2. Production Deployment: Docker Compose Architecture

For team deployments requiring multi-user synchronization and persistent PostgreSQL storage:

```yaml
version: '3.8'

services:
  # Doction Web & API Gateway
  doction:
    image: doction/doction:latest
    container_name: doction_app
    ports:
      - '3000:3000'
    environment:
      - NODE_ENV=production
      - DATABASE_URL=postgres://doction:secret_db_pass@db:5432/doction
      - REDIS_URL=redis://cache:6379
      - JWT_SECRET=replace_with_a_secure_32_character_random_string
      - VITE_APP_URL=https://docs.yourcompany.com
    depends_on:
      - db
      - cache
    restart: unless-stopped

  # PostgreSQL Primary Database
  db:
    image: postgres:16-alpine
    container_name: doction_postgres
    environment:
      - POSTGRES_USER=doction
      - POSTGRES_PASSWORD=secret_db_pass
      - POSTGRES_DB=doction
    volumes:
      - doction_pgdata:/var/lib/postgresql/data
    restart: unless-stopped

  # Redis Realtime Cache & Fanout
  cache:
    image: redis:7-alpine
    container_name: doction_redis
    restart: unless-stopped

volumes:
  doction_pgdata:
```

### Launching the Stack
```bash
# Start all containers in background
docker compose up -d

# Verify container health
docker compose ps

# View live application logs
docker compose logs -f doction
```

---

## 3. Reverse Proxy & Automatic SSL (Caddy Example)

If you are exposing Doction to your team over a custom domain (e.g., `docs.yourcompany.com`), use Caddy for automatic Let's Encrypt HTTPS:

```caddyfile
docs.yourcompany.com {
    reverse_proxy localhost:3000
    encode zstd gzip
}
```

---

## 4. Production Security Checklist

- [ ] **Strong Secrets:** Generate a 64-character random string for `JWT_SECRET` (`openssl rand -hex 32`).
- [ ] **SSL / TLS:** Never serve plain HTTP over public networks; ensure port 443 with TLS 1.3 is enforced.
- [ ] **Automated Database Dumps:** Schedule a daily cron job running `pg_dump` to an encrypted external backup vault.
- [ ] **Firewall Isolation:** Expose only ports 80 and 443 to the internet; keep Postgres (`5432`) and Redis (`6379`) locked to the Docker internal bridge network.
