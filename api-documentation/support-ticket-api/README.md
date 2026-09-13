# Support Ticket API — Developer Documentation

**Sample type:** REST API Documentation / Docs-as-Code

## Overview

This sample demonstrates developer-focused documentation for a fictional Support Ticket REST API.

The API enables client applications to create and retrieve support tickets by using standard HTTP methods, request headers, path parameters, JSON request bodies, and JSON responses.

The documentation is organized as a small docs-as-code project using Markdown and GitHub.

## About this sample

I created this fictional Support Ticket API to demonstrate how I would structure and write REST API documentation for developers. The sample covers API fundamentals including authentication, endpoints, request and response formats, parameters, status codes, and error handling.

The documentation is written in Markdown and organized in GitHub using a docs-as-code structure.

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
