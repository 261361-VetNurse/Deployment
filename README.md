# Petlite Deployment

## Quick Setup

1. Copy `.env.example` to `.env` and fill in your environment variables:
   ```sh
   cp .env.example .env
   # Edit .env as needed
   ```
2. Build and start all services:
   ```sh
   docker compose up --build
   ```
3. Access the services:
   - Backend API: http://localhost:8000
   - Frontend: http://localhost:3000
   - Caddy (reverse proxy): http://localhost

## Notes
- Make sure you have Docker and Docker Compose installed.
- Do not commit your real `.env` file with secrets to version control.
- For production, review and adjust environment variables and volumes as needed.

## Directory Structure Required

Make sure the following directories exist in the same folder as `docker-compose.yml`:

- `Backend/`  (backend source code)
- `frontend/` (frontend source code)

Example:

```
Deployment/
├── docker-compose.yml
├── .env
├── Caddyfile
├── Backend/
└── frontend/
```
