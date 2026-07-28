# Indie Hacker CLI & Developer Command Cheatsheet

> **A high-productivity command-line reference for solo software developers, bootstrappers, and indie founders managing servers, databases, payment webhooks, and deployments.**

---

## 📌 Executive Summary

Solo builders do not have dedicated DevOps or Infrastructure teams. Mastering essential CLI commands for payment webhook testing, zero-downtime server deployments, database backups, and reverse proxies allows a 1-person team to operate with enterprise velocity.

---

## 1. Stripe CLI & Payment Webhook Testing

```bash
# 1. Authenticate Stripe CLI
stripe login

# 2. Listen & forward live webhook events to local dev server
stripe listen --forward-to localhost:8080/api/webhooks

# 3. Trigger simulated subscription events for local debugging
stripe trigger customer.subscription.created
stripe trigger invoice.payment_succeeded
stripe trigger invoice.payment_failed
stripe trigger customer.subscription.deleted
```

---

## 2. Server Deployments & Process Management (Go & Node)

```bash
# Go: Zero-dependency cross-compilation for Linux VPS (64-bit)
CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -ldflags="-w -s" -o app .

# Node.js: PM2 Production Process Management
pm2 start server.js --name "my-saas" --max-memory-restart 300M
pm2 status
pm2 logs my-saas --lines 100
pm2 save && pm2 startup # Persist process across VPS server reboots

# Docker: Container orchestration & cleanup
docker compose up -d --build
docker compose logs -f --tail=100 app
docker system prune -af --volumes # Free up disk space on small $5 VPS
```

---

## 3. Database Backups & Migration CLI (Postgres & SQLite)

```bash
# PostgreSQL: Production Backup & Restore
pg_dump -U postgres -h localhost -d saas_db | gzip > backup_$(date +%Y%m%d).sql.gz
gunzip -c backup_20260728.sql.gz | psql -U postgres -d saas_db

# SQLite: Production WAL Mode Optimization & Backup
sqlite3 app.db "PRAGMA journal_mode=WAL;" # Enable Write-Ahead Logging for high concurrency
sqlite3 app.db ".backup 'backup.sqlite3'"

# Supabase CLI
npx supabase start                    # Run local Postgres/Auth/Storage stack
npx supabase db diff -f add_new_table  # Generate migration file
npx supabase db push                  # Apply migrations to remote Supabase DB
```

---

## 4. Caddy & Nginx Reverse Proxy / AutoSSL

Caddy automatically provisions free Let's Encrypt SSL certificates without complex certbot scripts:

```caddyfile
# Caddyfile (/etc/caddy/Caddyfile)
theinpublic.com {
    reverse_proxy localhost:8080
}
```

```bash
# Caddy CLI commands
caddy reload --config /etc/caddy/Caddyfile  # Zero-downtime config reload
caddy fmt --overwrite                      # Format Caddyfile
```

---

## 5. Network, SSL & Server Diagnostics

```bash
# Inspect SSL certificate expiration & handshake details
curl -Iv https://theinpublic.com

# DNS propagation check
dig +short A theinpublic.com
dig +short MX theinpublic.com

# Check if port 8080 is listening on host
netstat -tulpn | grep 8080
# or
lsof -i :8080
```

---

## 6. Summary

Command-line efficiency eliminates GUI dashboard friction. By automating server builds, database backups, and webhook testing via terminal scripts, solo founders save hours of operational overhead every week.

