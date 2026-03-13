# Architecture Diagram

The following diagram illustrates the main architecture of ProcessMind Assistant.

Client Layer
    |
    | HTTPS
    v
Frontend Web Application (Next.js)
    |
    v
Backend API (FastAPI)
    |
    |----------------------------|
    |                            |
Document Service         Chat Service
    |                            |
Processing Pipeline      Retrieval Service
    |                            |
Vector Database (pgvector)      |
    |                            |
PostgreSQL Database             |
    |                            |
File Storage                    |
    |
OpenAI API

---

# Diagramma architetturale

Il diagramma seguente illustra l'architettura principale di ProcessMind Assistant.

Livello Client
    |
    | HTTPS
    v
Applicazione Web Frontend (Next.js)
    |
    v
Backend API (FastAPI)
    |
    |----------------------------|
    |                            |
Servizio Documenti       Servizio Chat
    |                            |
Pipeline di elaborazione Servizio Retrieval
    |                            |
Database vettoriale (pgvector)  |
    |                            |
Database PostgreSQL             |
    |                            |
File Storage                    |
    |
OpenAI API
