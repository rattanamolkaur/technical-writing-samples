# Retrieve a support ticket

Retrieves an existing support ticket by its unique ticket identifier.

## Endpoint

```http
GET /api/v1/tickets/{ticket_id}
```

## Path parameters

| Parameter | Type | Required | Description |
| --- | --- | --- | --- |
| `ticket_id` | string | Yes | Unique identifier of the support ticket to retrieve. |

## Request headers

Include the following headers:

| Header | Required | Description |
| --- | --- | --- |
| `Authorization` | Yes | Bearer token used to authenticate the request. |
| `Accept` | No | Specifies the preferred response format. Use `application/json`. |

## Example request

The following example retrieves ticket `TKT-1001`:

```http
GET /api/v1/tickets/TKT-1001 HTTP/1.1
Host: api.example.com
Authorization: Bearer <access_token>
Accept: application/json
```

## Response

If the request is successful, the API returns the ticket details.

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
| `200 OK` | The ticket was retrieved successfully. |
| `401 Unauthorized` | Authentication failed or the access token is missing. |
| `404 Not Found` | A ticket with the specified `ticket_id` was not found. |

For additional error information, see [Error responses](errors.md).
