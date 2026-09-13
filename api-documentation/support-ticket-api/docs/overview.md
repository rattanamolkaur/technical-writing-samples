# Support Ticket API overview

The Support Ticket API is a REST API that enables client applications to create and retrieve support tickets.

Use the API to integrate support-ticket functionality with applications, portals, and automated workflows without requiring users to create or retrieve tickets manually.

## Base URL

Send API requests to the following base URL:

```text
https://api.example.com/api/v1
```

> **Note:** This URL is provided for documentation purposes only. The Support Ticket API is a fictional API created as a portfolio sample.

## Supported operations

The API supports the following operations:

| Method | Endpoint | Description |
| --- | --- | --- |
| `POST` | `/tickets` | Creates a support ticket. |
| `GET` | `/tickets/{ticket_id}` | Retrieves a support ticket by its unique identifier. |

## Request format

Send requests over HTTPS.

Requests that include a body use JSON. Specify the following header:

```http
Content-Type: application/json
```

Authenticated requests also require an authorization header. For authentication requirements, see [Authentication](authentication.md).

## Response format

The API returns response data in JSON.

A successful request to retrieve a support ticket can return a response similar to the following example:

```json
{
  "ticket_id": "TKT-1001",
  "short_description": "Unable to access application",
  "priority": "2",
  "status": "open"
}
```

The HTTP status code indicates whether the request succeeded or failed. For information about error responses, see [Error responses](errors.md).

## Next steps

- [Authenticate API requests](authentication.md)
- [Create a support ticket](create-ticket.md)
- [Retrieve a support ticket](get-ticket.md)
- [Handle error responses](errors.md)
