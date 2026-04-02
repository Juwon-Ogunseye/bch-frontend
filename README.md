# Welcome to your Lovable project

# Bitcoin Culture Hub — Frontend

This repo is the frontend for Bitcoin Culture Hub, built with React, Vite, TypeScript and Tailwind CSS.

## Prerequisites
- Node.js v20+
- Docker and Docker Compose

## Quick Start (Local)
```bash
git clone https://github.com/Bitcoin-Culture-Hub/bch-frontend.git
cd bch-frontend

# Install dependencies
npm i

# Run the app
npm run dev
```

Visit http://localhost:8080 to see the app.

## Quick Start (Docker - Full Stack)

The frontend and backend run together using Docker Compose.
Make sure you have cloned both repos side by side:
```
bch-frontend/   ← docker-compose.yaml lives here
bch-backend/    ← must be cloned at the same level
```

Clone both repos:
```bash
git clone https://github.com/Bitcoin-Culture-Hub/bch-frontend.git
git clone https://github.com/Bitcoin-Culture-Hub/bch-backend.git
```

Set up the backend environment:
```bash
cd bch-backend
cp .env.example .env
# Fill in your real credentials in .env
cd ..
```

Then from the frontend folder:
```bash
cd bch-frontend
docker compose up --build
```

This starts:
- Frontend at http://localhost:8080
- Backend API at http://localhost:8000
- Backend API docs at http://localhost:8000/docs

## Docker Commands
```bash
# Start everything
docker compose up

# Start in background
docker compose up -d

# Stop everything
docker compose down

# Rebuild after code changes
docker compose up --build

# View logs
docker compose logs

# View logs for specific service
docker compose logs frontend
docker compose logs backend
```

## AWS RDS Access
To run the backend locally or in Docker, your machine's IP must be 
whitelisted on the AWS RDS security group on port 3306.

## Tech Stack
- React
- TypeScript
- Vite
- Tailwind CSS
- Shadcn UI
- Docker + Nginx (production)