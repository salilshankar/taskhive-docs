---
title: Delete Task API
description: API endpoint to delete a specific task by its ID.
---

# Delete Task API

This API endpoint allows you to delete a specific task from the database using its unique identifier. It is part of the task management functionality and ensures that the specified task is removed permanently.

## HTTP Method

- **DELETE**

## Route Path

- `/api/tasks/<int:task_id>`

## Function Name

- `delete_task`

## Path Parameter

- **`task_id`**: An integer representing the unique identifier of the task you wish to delete. This parameter is required and must be a valid task ID.

## Response Status Codes

- **200 OK**: The task was successfully deleted. The response will include a JSON message confirming the deletion.
- **404 Not Found**: The specified task ID does not exist in the database. This status code is returned if the task cannot be found.

## Usage Example

To delete a task with the ID of 123, you can use the following `curl` command:

```bash
curl -X DELETE http://<your-server-url>/api/tasks/123
```

Upon successful deletion, the server will respond with:

```json
{
  "message": "Task deleted"
}
```

This endpoint is typically used in scenarios where task management is required, such as in project management applications or to-do list services.