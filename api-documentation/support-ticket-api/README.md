# Support Ticket API — Developer Documentation

**Sample type:** REST API Documentation / Docs-as-Code

## Overview

This sample provides developer documentation for a fictional Support Ticket REST API.

The API enables client applications to create and retrieve support tickets using standard HTTP methods, request headers, path parameters, JSON request bodies, and JSON responses.

The documentation is written in Markdown and organized in GitHub using a docs-as-code structure.

## API Documentation

- [API overview](docs/overview.md)
- [Authentication](docs/authentication.md)
- [Create a support ticket](docs/create-ticket.md)
- [Retrieve a support ticket](docs/get-ticket.md)
- [Error responses](docs/errors.md)

## Example Endpoints

```http
POST /api/v1/tickets
GET /api/v1/tickets/{ticket_id}
