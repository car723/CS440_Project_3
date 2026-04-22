# Clicker game (microservices)

This project refactors the original monolithic Node clicker game into independent services behind an API gateway, each with its own SQLite database, plus Docker deployment.

**GitHub repository:**  
https://github.com/car723/CS440_Project_3

## Quick start (Docker)

From the repository root:

```bash
docker compose up --build
```

Open http://localhost:3000

## Local development (without Docker)

Install dependencies once per Node app (root + each service), then run all processes:

```bash
npm install
npm install --prefix services/user-service
npm install --prefix services/game-state-service
npm install --prefix services/game-engine-service
npm install --prefix services/api-gateway
npm run dev
```

The UI is served by the API gateway on port 3000.
