# CLAUDE.md

## Project Overview
Baseball analytics app powered by historical Lahman data. Users can explore 
stats through embedded Superset dashboards and ask natural language questions 
via a Claude-powered chat interface.

## Stack
- **BigQuery** — data warehouse (Lahman baseball data)
- **dbt** — transformations on top of Lahman data
- **Superset** — embedded dashboards and charts
- **Clerk** — authentication and user management
- **Chainlit** — chat interface (Claude-powered)
- **FastAPI** — backend API
- **Claude API** — natural language to SQL
- **React** — frontend shell (navigation, auth, Superset embeds)

## Project Layout
- `backend/` — FastAPI app and routers
- `frontend/` — React app
- `dbt/` — dbt project

## Conventions
- Python dependency management via `uv`
- Environment variables in `.env` (never committed)
- Backend runs locally on port 8000
- Frontend runs locally on port 3000

## Current Status
Early stage. Getting bones in place before adding features.

## Key Context
- Chat interface queries BigQuery via Claude API (natural language to SQL)
- Superset dashboards embedded via iframe in React frontend
- Clerk handles all auth — lean on prebuilt components
- Lahman database is the data source (historical baseball stats to present)

## Future Ideas
- Claude chat generating Superset visualizations dynamically
- Dagster orchestration for dbt runs
