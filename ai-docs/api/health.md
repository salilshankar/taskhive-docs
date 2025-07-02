---
title: Health Check Endpoint
description: API documentation for the /health endpoint in a Flask application.
---

# Health Check Endpoint

The `/health` endpoint is a simple health check route that allows clients to verify if the server is running and responsive. This endpoint is typically used for monitoring and automation purposes to ensure the application is up and operational.

## HTTP Method

- **GET**

## Route Path

- **`/health`**

## Function Name

- **`health`**

## Path Parameters

This endpoint does not require any path parameters.

## Response

- **Status Code: 200**  
  The request was successful, and the server is operational. The response body contains a JSON object indicating the server status.

### Response Body

```json
{
  "status": "ok"
}
```

## Usage Example

To check the health of the server, you can use the following `curl` command:

```bash
curl -X GET http://yourserver.com/health
```

This command will return a JSON response confirming the server's operational status with a 200 HTTP status code.