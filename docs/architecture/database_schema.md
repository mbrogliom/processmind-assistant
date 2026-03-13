# Database Schema

ProcessMind Assistant uses PostgreSQL as the main relational database.

The system also uses pgvector to store embeddings for semantic search.

## Main tables

Users

Stores user accounts.

Fields:

- id
- email
- password_hash
- role
- created_at

---

Organizations

Represents companies using the platform.

Fields:

- id
- name
- plan
- created_at

---

Documents

Stores uploaded documents.

Fields:

- id
- organization_id
- title
- filename
- storage_path
- created_at

---

DocumentChunks

Stores chunks of document text.

Fields:

- id
- document_id
- chunk_text
- embedding
- page_number

---

Chats

Stores chat sessions.

Fields:

- id
- user_id
- created_at

---

ChatMessages

Stores messages in a conversation.

Fields:

- id
- chat_id
- role
- content
- created_at

---

# Schema del database

ProcessMind Assistant utilizza PostgreSQL come database relazionale principale.

Il sistema utilizza anche pgvector per memorizzare gli embeddings necessari alla ricerca semantica.

## Tabelle principali

Users

Memorizza gli account degli utenti.

Campi:

- id
- email
- password_hash
- ruolo
- created_at

---

Organizations

Rappresenta le organizzazioni che utilizzano la piattaforma.

Campi:

- id
- nome
- piano
- created_at

---

Documents

Memorizza i documenti caricati.

Campi:

- id
- organization_id
- titolo
- filename
- storage_path
- created_at

---

DocumentChunks

Memorizza i blocchi di testo dei documenti.

Campi:

- id
- document_id
- chunk_text
- embedding
- page_number

---

Chats

Memorizza le sessioni di chat.

Campi:

- id
- user_id
- created_at

---

ChatMessages

Memorizza i messaggi delle conversazioni.

Campi:

- id
- chat_id
- role
- content
- created_at
