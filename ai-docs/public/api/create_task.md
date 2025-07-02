---
title: Create Task API
description: API endpoint to create a new task in the task management system.
---

# Create Task API

This endpoint allows clients to create a new task in the task management system. Clients can specify the task title and its completion status.

## Endpoint Overview

- **HTTP Method**: `POST`
- **Route Path**: `/api/tasks`
- **Function Name**: `create_task`

## Request Body

The request body should be a JSON object containing the following fields:

- **title** (string): The title of the task. This field is required.
- **is_completed** (boolean, optional): The completion status of the task. Defaults to `false` if not provided.

## Response

The endpoint returns a JSON object containing the following fields:

- **id** (integer): The unique identifier of the created task.
- **title** (string): The title of the task.
- **is_completed** (boolean): The completion status of the task.

### Response Status Codes

- **201 Created**: The task was successfully created.

## Usage Example

Here is an example of how to call this endpoint using `curl`:

```bash
curl -X POST http://localhost:5000/api/tasks \
-H "Content-Type: application/json" \
-d '{
  "title": "Finish documentation",
  "is_completed": false
}'
```

In the above example, a new task with the title "Finish documentation" is created with a default completion status of `false`. The server will respond with the task details and a status code of `201 Created`.