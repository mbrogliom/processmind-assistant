# Real Database Schema

ProcessMind Assistant uses PostgreSQL as the main relational database and pgvector as the vector extension for semantic search.

The database is designed to support:

- multi-tenant organizations
- user authentication
- document storage metadata
- document chunk indexing
- chat sessions
- audit and usage logs

## Main entities

### Organizations

Represents the companies or teams using the platform.

Main fields:

- id
- name
- slug
- plan
- is_active
- created_at
- updated_at

### Users

Represents users belonging to an organization.

Main fields:

- id
- organization_id
- full_name
- email
- password_hash
- role
- is_active
- created_at
- updated_at

### Documents

Represents uploaded files and their metadata.

Main fields:

- id
- organization_id
- uploaded_by
- title
- filename
- mime_type
- storage_path
- status
- category
- metadata
- created_at
- updated_at

### Document Chunks

Represents chunks extracted from uploaded documents and their embeddings.

Main fields:

- id
- document_id
- organization_id
- chunk_index
- page_number
- heading
- chunk_text
- token_count
- metadata
- embedding
- created_at

### Chats

Represents chat sessions created by users.

Main fields:

- id
- organization_id
- user_id
- title
- created_at
- updated_at

### Chat Messages

Represents individual messages in a chat session.

Main fields:

- id
- chat_id
- role
- content
- source_refs
- model_name
- prompt_tokens
- completion_tokens
- created_at

### Query Logs

Stores audit logs for AI questions and retrieval operations.

Main fields:

- id
- organization_id
- user_id
- chat_id
- question
- retrieved_chunk_ids
- model_name
- response_time_ms
- status
- error_message
- created_at

## Database goals

The schema is designed to provide:

- clear tenant isolation
- traceability of AI answers
- support for semantic retrieval
- support for future billing and analytics

---

# Schema reale del database

ProcessMind Assistant utilizza PostgreSQL come database relazionale principale e pgvector come estensione vettoriale per la ricerca semantica.

Il database è progettato per supportare:

- organizzazioni multi-tenant
- autenticazione utenti
- metadati dei documenti
- indicizzazione dei chunk documentali
- sessioni di chat
- log di audit e utilizzo

## Entità principali

### Organizations

Rappresenta le aziende o i team che utilizzano la piattaforma.

Campi principali:

- id
- name
- slug
- plan
- is_active
- created_at
- updated_at

### Users

Rappresenta gli utenti appartenenti a un'organizzazione.

Campi principali:

- id
- organization_id
- full_name
- email
- password_hash
- role
- is_active
- created_at
- updated_at

### Documents

Rappresenta i file caricati e i relativi metadati.

Campi principali:

- id
- organization_id
- uploaded_by
- title
- filename
- mime_type
- storage_path
- status
- category
- metadata
- created_at
- updated_at

### Document Chunks

Rappresenta i blocchi di testo estratti dai documenti caricati e i relativi embeddings.

Campi principali:

- id
- document_id
- organization_id
- chunk_index
- page_number
- heading
- chunk_text
- token_count
- metadata
- embedding
- created_at

### Chats

Rappresenta le sessioni di chat create dagli utenti.

Campi principali:

- id
- organization_id
- user_id
- title
- created_at
- updated_at

### Chat Messages

Rappresenta i singoli messaggi di una sessione di chat.

Campi principali:

- id
- chat_id
- role
- content
- source_refs
- model_name
- prompt_tokens
- completion_tokens
- created_at

### Query Logs

Memorizza i log di audit relativi alle domande AI e alle operazioni di retrieval.

Campi principali:

- id
- organization_id
- user_id
- chat_id
- question
- retrieved_chunk_ids
- model_name
- response_time_ms
- status
- error_message
- created_at

## Obiettivi del database

Lo schema è progettato per offrire:

- isolamento chiaro tra tenant
- tracciabilità delle risposte AI
- supporto al retrieval semantico
- supporto futuro per billing e analytics
