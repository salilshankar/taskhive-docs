---
title: Delete Note API
description: API endpoint to delete a specific note by its ID.
---

# Delete Note API

This endpoint allows you to delete a specific note by providing its unique identifier (`note_id`). Once the note is deleted, a confirmation message is returned.

## HTTP Method

- **DELETE**

## Route Path

- `/api/notes/<int:note_id>`

## Function Name

- `delete_note`

## Path Parameters

- **`note_id`**: The unique integer identifier of the note you wish to delete. This parameter is required.

## Response Status Codes

- **200 OK**: The note was successfully deleted. The response will include a JSON message confirming the deletion.
- **404 Not Found**: No note with the specified `note_id` exists.

## Example Usage

To delete a note with the ID of `123`, you can use the following `curl` command:

```bash
curl -X DELETE http://yourapi.com/api/notes/123
```

Upon successful deletion, the server will respond with:

```json
{
  "message": "Note deleted"
}
```

This endpoint is useful for managing notes by allowing users to remove notes that are no longer needed, ensuring that the notes database remains up-to-date and clutter-free.