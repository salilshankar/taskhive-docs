---
title: Update Task
description: API documentation for updating a task by its ID.
---

# Update Task

This API endpoint allows you to update the details of an existing task by specifying its ID. You can modify the task's title and completion status.

## HTTP Method

- **PUT**

## Route Path

- `/api/tasks/<int:task_id>`

## Function

- `update_task`

## Path Parameters

- **task_id**: An integer representing the unique identifier of the task you wish to update.

## Response Status Codes

- **200 OK**: The task was successfully updated. The response will contain the updated task details.
- **404 Not Found**: No task was found with the specified ID.

## Usage Example

To update a task, you can use the following `curl` command:

```bash
curl -X PUT http://example.com/api/tasks/1 \
     -H "Content-Type: application/json" \
     -d '{"title": "Updated Task Title", "is_completed": true}'
```

This command updates the task with ID `1`, setting its title to "Updated Task Title" and marking it as completed.