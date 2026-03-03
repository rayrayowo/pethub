# PetHub

PetHub is a CS3200 full-stack project for managing pet care workflows, including appointments, health records, medications, exercise logs, community posts, and analytics.

## Project Overview

This repository includes a Dockerized three-service architecture:
- Streamlit frontend (`app/`)
- Flask REST API (`api/`)
- MySQL database (`database-files/`)

The goal is to demonstrate end-to-end database application development: schema design, API layer implementation, and user-facing dashboards.

## Core Features

- Pet profile and owner data management
- Appointment booking and tracking
- Groomer and veterinarian lookup pages
- Health/checkup/medication/prescription/exercise records
- Community and event pages
- Basic analytics dashboard via API

## Tech Stack

- Python
- Streamlit
- Flask
- MySQL
- Docker / Docker Compose

## Repository Structure

```text
app/                     Streamlit app
api/                     Flask API and backend modules
database-files/          SQL initialization scripts
docker-compose.yaml      Main local run config
docker-compose-testing.yaml  Testing/local variation
```

## Local Run (Docker)

From the repository root:

```bash
docker compose up -d
```

Stop services:

```bash
docker compose down
```

If you only want database service:

```bash
docker compose up db -d
```

## Database Initialization

Database schema/data scripts are in:

- `database-files/initdb.d/*.sql`

They are executed automatically when MySQL container initializes.

## Example API Areas

Routes are organized under `api/backend/routes/`, including:
- `/analytics`
- `/checkups`
- `/community`
- `/events`
- `/exercise`
- `/groomers`
- `/health`
- `/medications`
- `/owners`
- `/pets`
- `/prescriptions`
- `/vets`

## Notes

This repository is an academic project and was built to practice database-centered system design and integration.
