# Backend Modules

## Models

Models represent the database tables using an ORM such as SQLAlchemy.

Examples:

- User
- Organization
- Document
- DocumentChunk
- Chat
- ChatMessage

---

## Schemas

Schemas define the request and response formats used by the API.

They are implemented using Pydantic models.

Examples:

- UserCreate
- DocumentUpload
- ChatRequest
- ChatResponse

---

## Routers

Routers define the REST API endpoints.

Examples:

- /auth
- /documents
- /chat
- /users

Each router corresponds to a specific module.

---

## Services

Services contain the business logic of the application.

Examples:

- document processing
- embedding generation
- semantic retrieval
- chat orchestration

---

## Workers

Workers handle asynchronous tasks such as:

- document parsing
- embedding generation
- background processing

These tasks can be executed using tools such as Celery or background tasks.

---

# Moduli backend

## Models

I modelli rappresentano le tabelle del database tramite un ORM come SQLAlchemy.

Esempi:

- User
- Organization
- Document
- DocumentChunk
- Chat
- ChatMessage

---

## Schemas

Gli schemas definiscono i formati delle richieste e delle risposte API.

Sono implementati con modelli Pydantic.

Esempi:

- UserCreate
- DocumentUpload
- ChatRequest
- ChatResponse

---

## Routers

I routers definiscono gli endpoint REST dell'API.

Esempi:

- /auth
- /documents
- /chat
- /users

Ogni router corrisponde a un modulo specifico.

---

## Services

I servizi contengono la logica applicativa.

Esempi:

- elaborazione documenti
- generazione embeddings
- retrieval semantico
- orchestrazione della chat

---

## Workers

I workers gestiscono attività asincrone come:

- parsing dei documenti
- generazione embeddings
- elaborazioni in background
