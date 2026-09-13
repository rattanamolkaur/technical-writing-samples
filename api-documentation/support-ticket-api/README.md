# Support Ticket API — Developer Documentation

**Sample type:** REST API Documentation / Docs-as-Code

## Overview

This sample demonstrates developer-focused documentation for a fictional Support Ticket REST API.

The API enables client applications to create and retrieve support tickets by using standard HTTP methods, request headers, path parameters, JSON request bodies, and JSON responses.

The documentation is organized as a small docs-as-code project using Markdown and GitHub.

## What This Sample Demonstrates

- REST API documentation
- Developer-focused technical writing
- HTTP methods and endpoints
- Authentication and request headers
- Path parameters
- JSON request and response examples
- HTTP status codes and error handling
- Markdown authoring
- GitHub-based docs-as-code structure

## API Documentation

The sample includes the following topics:

- [API overview](docs/overview.md)
- [Authentication](docs/authentication.md)
- [Create a support ticket](docs/create-ticket.md)
- [Retrieve a support ticket](docs/get-ticket.md)
- [Error responses](docs/errors.md)

## Example Endpoints

```http
POST /api/v1/tickets
GET /api/v1/tickets/{ticket_id}
```

## Documentation Structure

```text
support-ticket-api/
├── README.md
└── docs/
    ├── overview.md
    ├── authentication.md
    ├── create-ticket.md
    ├── get-ticket.md
    └── errors.md
```

> **Portfolio note:** This is an original fictional API created solely to demonstrate REST API documentation and docs-as-code practices. It is not associated with an actual product or service.
