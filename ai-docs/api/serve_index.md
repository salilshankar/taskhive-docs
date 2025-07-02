---
title: Root Endpoint Documentation
description: Detailed API documentation for the root endpoint of the application.
---

# Root Endpoint (`/`)

The root endpoint serves the main HTML file of the application. When accessed, it returns the `index.html` file from the `static` directory, which is typically used to render the homepage of the application.

## HTTP Method

- **GET**

## Route Path

- **/**

## Function Name

- **serve_index**

## Path Parameters

This endpoint does not require any path parameters.

## Response Status Codes

- **200 OK**: The request was successful, and the `index.html` file is returned.
- **404 Not Found**: The `index.html` file could not be found in the `static` directory.

## Usage Example

To access the root endpoint and retrieve the homepage, you can use a tool like `curl`:

```bash
curl http://localhost:5000/
```

This command will initiate a GET request to the root endpoint, and if successful, it will return the contents of the `index.html` file.