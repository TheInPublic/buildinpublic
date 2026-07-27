# Indie Hacker CLI & Developer Command Cheatsheet

> **A high-productivity command-line reference for solo software developers, bootstrappers, and indie founders.**

---

## 1. Stripe CLI & Local Webhook Testing

```bash
# 1. Login to your Stripe developer account
stripe login

# 2. Forward live webhook events to your local dev server
stripe listen --forward-to localhost:8080/api/webhooks

# 3. Trigger simulated subscription events for testing
stripe trigger customer.subscription.created
stripe trigger invoice.payment_succeeded
stripe trigger invoice.payment_failed
```

---

## 2. Deployment & Cloud CLI (Vercel, Cloudflare, Supabase)

```bash
# Vercel Deployment
npx vercel                   # Preview deployment
npx vercel --prod            # Production deployment
npx vercel env pull .env.local # Pull remote environment variables

# Supabase Local Development
npx supabase start           # Start local Postgres, Auth, and Storage stack
npx supabase db diff -f add_users_table # Create DB migration file
npx supabase db push         # Apply migrations to remote Supabase project

# Cloudflare Wrangler
npx wrangler dev             # Run local Cloudflare Worker
npx wrangler deploy          # Deploy Worker to edge network
```

---

## 3. Docker & VPS Production Commands (Hetzner / DigitalOcean)

```bash
# Build and run containerized app in background
docker compose up -d --build

# Inspect live container logs in production
docker compose logs -f --tail=100 app

# Prune unused containers and images to free disk space
docker system prune -af --volumes
```

---

## 4. Git & Release Management Workflows

```bash
# Create a release tag and push to GitHub
git tag -a v1.0.0 -m "Release version 1.0.0"
git push origin v1.0.0

# Undo last local commit while keeping changes staged
git reset --soft HEAD~1

# Clean untracked build files safely
git clean -fd
```

---

## 5. Summary

Mastering essential CLI commands saves hours of repetitive manual clicking in web dashboards, allowing solo founders to ship code faster and maintain maximum operational velocity.
