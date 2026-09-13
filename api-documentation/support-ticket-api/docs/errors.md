# Error responses

The Support Ticket API uses standard HTTP status codes to indicate whether a request succeeded or failed.

When a request fails, the response can include an error code and message that describe the problem.

## Error response format

Error responses use JSON.

```json
{
  "error": {
    "code": "INVALID_REQUEST",
    "message": "The request is invalid."
  }
}
```

## Common error responses

| Status code | Error code | Description |
| --- | --- | --- |
| `400 Bad Request` | `INVALID_REQUEST` | The request is invalid or a required field is missing. |
| `401 Unauthorized` | `UNAUTHORIZED` | Authentication failed or the access token is missing or invalid. |
| `404 Not Found` | `TICKET_NOT_FOUND` | The requested support ticket doesn't exist. |
| `500 Internal Server Error` | `INTERNAL_ERROR` | An unexpected server error occurred. |

## Example: invalid request

The following response can be returned when a required request field is missing:

```json
{
  "error": {
    "code": "INVALID_REQUEST",
    "message": "The short_description field is required."
  }
}
```

## Example: ticket not found

The following response can be returned when the specified ticket doesn't exist:

```json
{
  "error": {
    "code": "TICKET_NOT_FOUND",
    "message": "Support ticket TKT-9999 was not found."
  }
}
```

## Troubleshooting

If a request fails:

1. Review the HTTP status code.
2. Review the error code and message in the response body.
3. Verify that the request includes all required headers, parameters, and fields.
4. Verify that the access token is valid.
5. Correct the request and try again.
