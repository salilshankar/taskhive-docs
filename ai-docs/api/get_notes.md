---
title: Get Notes API
description: Retrieve a list of all notes from the server.
---

# Get Notes API

The Get Notes API endpoint allows clients to retrieve a list of all notes stored on the server. This endpoint is useful for applications that need to display or process a collection of notes.

## HTTP Method

- **GET**

## Route Path

- `/api/notes`

## Function Name

- `get_notes`

## Path Parameters

This endpoint does not accept any path parameters.

## Response Status Codes

- **200 OK**: The request was successful, and the response contains a list of notes.
- **500 Internal Server Error**: An error occurred on the server while processing the request.

## Response Format

The response is a JSON array of note objects. Each note object contains the following fields:
- `id`: The unique identifier of the note.
- `content`: The textual content of the note.

## Usage Example

To retrieve all notes, you can use the following `curl` command:

```bash
curl -X GET http://yourserver.com/api/notes
```

This will return a JSON response similar to the following:

```json
[
  {
    "id": 1,
    "content": "This is the first note."
  },
  {
    "id": 2,
    "content": "This is the second note."
  }
]
```

This endpoint is typically used in scenarios where you need to display a list of notes to the user or perform operations on the collection of notes.