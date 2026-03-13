# API Endpoints

## Authentication

POST /auth/login  
POST /auth/register

---

## Documents

POST /documents/upload  
GET /documents  
GET /documents/{id}

---

## Chat

POST /chat/ask

Body:

{
  "question": "Which contracts expire this year?"
}

---

## Users

GET /users/me

---

# Endpoint API

## Autenticazione

POST /auth/login  
POST /auth/register

---

## Documenti

POST /documents/upload  
GET /documents  
GET /documents/{id}

---

## Chat

POST /chat/ask

Esempio richiesta:

{
  "question": "Quali contratti scadono quest'anno?"
}

---

## Utenti

GET /users/me
