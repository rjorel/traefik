# Traefik

A Docker Compose stack featuring Traefik as a reverse proxy, automatic HTTPS with Let's Encrypt, Dozzle for container
logs, and custom error pages.

## Setup

1. Create your environment file from the example:

   ```bash
   cp .env.example .env
   ```

2. Generate HTTP Basic Auth credentials using `htpasswd`:

   ```bash
   htpasswd -nb username password
   ```

   Escape `$` characters as `$$` in the generated hash before adding it to `.env`.

3. Edit `.env` and configure the required values, including `TRAEFIK_BASIC_AUTH`.

## Services

- **Traefik** — Reverse proxy, automatic HTTPS, and dashboard.
- **Dozzle** — Real-time Docker container logs.
- **Nginx** — Custom error pages.
