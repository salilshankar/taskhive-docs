---
title: Get Tasks API
description: Retrieve a list of all tasks from the database.
---

# Get Tasks API

This API endpoint retrieves a list of all tasks stored in the database. Each task includes its ID, title, and completion status.

## HTTP Method

- **GET**

## Route Path

- `/api/tasks`

## Function Name

- `get_tasks`

## Path Parameters

This endpoint does not require any path parameters.

## Response Status Codes

- **200 OK**: The request was successful, and the list of tasks is returned in the response.

## Response Format

The response is a JSON array of task objects, each containing the following fields:

- `id`: The unique identifier of the task.
- `title`: The title of the task.
- `is_completed`: A boolean indicating whether the task is completed.

## Example Usage

To retrieve the list of tasks, you can use the following `curl` command:

```bash
curl -X GET http://localhost:5000/api/tasks
```

This command will return a JSON array of tasks, for example:

```json
[
  {
    "id": 1,
    "title": "Buy groceries",
    "is_completed": false
  },
  {
    "id": 2,
    "title": "Read a book",
    "is_completed": true
  }
]
```

This endpoint is typically used in frontend applications to display a list of tasks to users or in automated scripts to process task data.