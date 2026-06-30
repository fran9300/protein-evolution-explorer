# Protein Evolution Explorer

Full-stack bioinformatics platform for protein sequence analysis.

---

# Architecture

The project is organized into three independent components that communicate with each other:

## 🐍 Protein Analyzer

**Python + FastAPI**

Responsible for:

- FASTA parsing
- physicochemical calculations
- sequence analysis
- generating protein analysis data

Repository:

[protein-evolution-analyzer](https://github.com/fran9300/protein-evolution-analyzer)

---

## ☕ Backend API

**Spring Boot + PostgreSQL**

Responsible for:

- REST API
- communication between frontend and analyzer
- data persistence
- protein analysis management

Repository:

[protein-evolution-backend](https://github.com/fran9300/protein-evolution-backend)

---

## ⚛️ Frontend

**React + TypeScript + Tailwind**

Responsible for:

- protein explorer interface
- visualization of analysis results
- interaction with backend API

Repository:

[protein-evolution-frontend](https://github.com/fran9300/protein-evolution-frontend)

---

# Project Structure

The main repository works as the orchestrator of the complete application.

The final structure should be:

```

Protein-Evolution-Explorer/
├── docker-compose.yml
├── README.md
│
├── protein-evolution-analyzer/
├── protein-evolution-backend/
└── protein-evolution-frontend/

```

The three component repositories must be cloned inside the main project directory.

---

# Running the Application

## 1. Clone the main repository

Clone the main repository:

```

git clone https://github.com/fran9300/protein-evolution-explorer

```

Move into the project directory:

```

cd Protein-Evolution-Explorer

```

---

## 2. Clone the component repositories

Clone the three required components inside the main project directory:

```

git clone https://github.com/fran9300/protein-evolution-analyzer

git clone https://github.com/fran9300/protein-evolution-backend

git clone https://github.com/fran9300/protein-evolution-frontend

```

The final structure should match:

```

Protein-Evolution-Explorer/
├── docker-compose.yml
├── README.md
│
├── protein-evolution-analyzer/
├── protein-evolution-backend/
└── protein-evolution-frontend/

```

---

## 3. Start the complete environment

From the root project directory run:

```

docker compose up --build

```

Docker Compose will automatically:

- build each service image
- create the internal network
- start PostgreSQL
- start the FastAPI analyzer service
- start the Spring Boot backend
- start the React frontend

---

# Services

Once running:

| Service | Technology | Port |
|-|-|-|
| Frontend | React | 80 |
| Backend API | Spring Boot | 8080 |
| Protein Analyzer | FastAPI | 8000 |
| Database | PostgreSQL | 5432 |

---

# Service Communication

The application uses Docker internal networking.

Communication flow:

```

Frontend
    ↓
Spring Boot Backend
    ↓
FastAPI Analyzer
    ↓
PostgreSQL Database

```

The services communicate using Docker service names instead of `localhost`.

Example:

- Backend communicates with the analyzer using the Docker service name.
- Backend connects to PostgreSQL using the database container name.

---

# Development Workflow

Each component can also be developed independently.

Recommended workflow:

- Use local execution for active development and debugging.
- Use Docker Compose to test the complete integrated environment.

Docker Compose is intended to provide:

- unified environment setup
- easier deployment
- consistent service communication

---

# Current Status

The platform is currently integrated with:

- frontend and backend communication
- backend and analyzer communication
- PostgreSQL persistence
- Docker-based environment setup

The complete system can be started using a single Docker Compose command.

---

# Stopping the Application

To stop all running services:

```

docker compose down

```

To remove containers and stored database data:

```

docker compose down -v

```

---

# Future Plans

- interactive bioinformatics visualizations
- automated testing
- production deployment
- advanced protein comparison features

## Author

**Francisco Kin**

- Bioinformatics Student | Backend Development | Data Analysis
- **GitHub:** [@fran9300](https://github.com/fran9300)
