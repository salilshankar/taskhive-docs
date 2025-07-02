---
title: Create Note API
description: API endpoint to create a new note in the system.
---

# Create Note API

This endpoint allows clients to create a new note by sending a JSON payload containing the note's content. Once created, the note is stored in the database, and a response with the note's ID and content is returned.

## HTTP Method

- **POST**

## Route Path

- `/api/notes`

## Function Name

- `create_note`

## Request Body

This endpoint expects a JSON object in the request body with the following property:

- **content** (string): The content of the note to be created.

## Response

- **201 Created**: The request was successful, and the note was created. The response body contains a JSON object with the following properties:
  - **id** (integer): The unique identifier of the created note.
  - **content** (string): The content of the created note.

## Usage Example

Here's an example of how to call this endpoint using `curl`:

```bash
curl -X POST http://yourdomain.com/api/notes \
-H "Content-Type: application/json" \
-d '{"content": "This is a new note."}'
```

This will create a new note with the content "This is a new note." and return a JSON response with the note's ID and content.