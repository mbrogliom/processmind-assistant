# Data Flow

This document describes how data moves through the ProcessMind Assistant system.

## Document Upload Flow

When a user uploads a document, the following sequence of operations occurs:

1. The document is uploaded through the web interface.
2. The frontend sends the document to the backend API.
3. The backend stores the file in the document storage system.
4. The backend extracts the text from the document.
5. The text is divided into smaller chunks.
6. Each chunk is transformed into an embedding vector.
7. The embeddings are stored in the vector database.

Once this process is completed, the document becomes searchable through semantic queries.

## Question and Answer Flow

When a user asks a question, the following steps occur:

1. The user submits a question through the chat interface.
2. The question is sent to the backend API.
3. The backend generates an embedding for the question.
4. The system searches the vector database for relevant document chunks.
5. The most relevant chunks are selected as context.
6. The context and the question are sent to the language model.
7. The AI generates a response.
8. The response and source references are returned to the user.

---

# Flusso dei dati

Questo documento descrive come i dati si muovono all'interno del sistema ProcessMind Assistant.

## Flusso di caricamento dei documenti

Quando un utente carica un documento, avviene la seguente sequenza di operazioni:

1. Il documento viene caricato tramite l'interfaccia web.
2. Il frontend invia il documento al backend tramite API.
3. Il backend salva il file nel sistema di archiviazione.
4. Il backend estrae il testo dal documento.
5. Il testo viene suddiviso in blocchi più piccoli.
6. Ogni blocco viene trasformato in un embedding vettoriale.
7. Gli embedding vengono salvati nel database vettoriale.

Una volta completato questo processo, il documento diventa ricercabile tramite query semantiche.

## Flusso domanda-risposta

Quando un utente pone una domanda, avvengono i seguenti passaggi:

1. L'utente invia una domanda tramite l'interfaccia di chat.
2. La domanda viene inviata al backend tramite API.
3. Il backend genera un embedding per la domanda.
4. Il sistema cerca nel database vettoriale i blocchi di testo più rilevanti.
5. I blocchi più pertinenti vengono selezionati come contesto.
6. Il contesto e la domanda vengono inviati al modello linguistico.
7. L'AI genera una risposta.
8. La risposta e le fonti vengono restituite all'utente.
