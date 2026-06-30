# Protein Evolution Explorer

Full-stack bioinformatics platform for protein sequence analysis.

## Architecture

The project is currently organized into three separate components that communicate with each other:

### 🐍 Protein Analyzer
Python + FastAPI

Responsible for:
- FASTA parsing
- physicochemical calculations
- sequence analysis
- generating protein analysis data

Repository:
[(link)](https://github.com/fran9300/protein-evolution-backend)


### ☕ Backend API
Spring Boot + PostgreSQL

Responsible for:
- REST API
- communication between frontend and analyzer
- data persistence
- protein analysis management

Repository:
[(link)](https://github.com/fran9300/protein-evolution-backend)


### ⚛️ Frontend
React + TypeScript + Tailwind

Responsible for:
- protein explorer interface
- visualization of analysis results
- interaction with backend API

Repository:
[(link)](https://github.com/fran9300/protein-evolution-frontend)


## Current Status

The components are already integrated and communicating.

The next step is consolidating the project into a unified environment with:

- Docker Compose
- automated startup
- unified configuration
- easier deployment


## Future Plans

- interactive bioinformatics visualizations
- automated testing
- production deployment
- advanced protein comparison features
