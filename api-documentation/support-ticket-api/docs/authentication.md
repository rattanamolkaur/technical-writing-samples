# Authenticate API requests

The Support Ticket API uses bearer token authentication to verify API requests.

Include a valid access token in the `Authorization` header of each request.

## Authorization header

Use the following format:

```http
Authorization: Bearer <access_token>
```

Replace `<access_token>` with your access token.

For example:

```http
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.example-token
```

> **Important:** Keep access tokens secure. Don't include access tokens in source code, public repositories, or other publicly accessible locations.

## Example request

The following example retrieves support ticket `TKT-1001`:

```http
GET /api/v1/tickets/TKT-1001 HTTP/1.1
Host: api.example.com
Authorization: Bearer <access_token>
Accept: application/json
```

If the access token is missing or invalid, the API returns an authentication error.

For information about API errors, see [Error responses](errors.md).
