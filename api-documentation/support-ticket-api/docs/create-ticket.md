# Create a support ticket

Creates a new support ticket.

## Endpoint

```http
POST /api/v1/tickets
```

## Request headers

Include the following headers:

| Header | Required | Description |
| --- | --- | --- |
| `Authorization` | Yes | Bearer token used to authenticate the request. |
| `Content-Type` | Yes | Specifies the request body format. Use `application/json`. |
| `Accept` | No | Specifies the preferred response format. Use `application/json`. |

## Request body

Send the ticket details as JSON in the request body.

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `short_description` | string | Yes | Brief summary of the issue. |
| `description` | string | No | Detailed information about the issue. |
| `priority` | string | Yes | Priority assigned to the ticket. Supported values are `1`, `2`, and `3`. |

### Example request body

```json
{
  "short_description": "Unable to access application",
  "description": "The application returns an access denied message after sign-in.",
  "priority": "2"
}
```

## Example request

```http
POST /api/v1/tickets HTTP/1.1
Host: api.example.com
Authorization: Bearer <access_token>
Content-Type: application/json
Accept: application/json

{
  "short_description": "Unable to access application",
  "description": "The application returns an access denied message after sign-in.",
  "priority": "2"
}
```

## Response

If the request is successful, the API creates the ticket and returns the created ticket details.

### Example response

```json
{
  "ticket_id": "TKT-1001",
  "short_description": "Unable to access application",
  "description": "The application returns an access denied message after sign-in.",
  "priority": "2",
  "status": "open"
}
```

## HTTP status codes

| Status code | Description |
| --- | --- |
| `201 Created` | The ticket was created successfully. |
| `400 Bad Request` | The request is invalid or a required field is missing. |
| `401 Unauthorized` | Authentication failed or the access token is missing. |

For additional error information, see [Error responses](errors.md).
