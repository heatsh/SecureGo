# SecureGo: Robust HTTP Server with TLS Support

## Project Overview

SecureGo is a medium-sized project to explore programming in go.

**Target**: production-ready HTTP server implemented in Go, featuring TLS 1.2 and 1.3 support, JWT authentication, and robust middleware

### Features

- Secure TLS 1.2 and 1.3 Configuration
- JWT-based Authentication
- Flexible Routing
- Comprehensive Logging
- Rate Limiting
- Dockerized Deployment

## Prerequisites

- Go 1.21+
- Docker (optional)
- Make (optional)

## Getting Started

### Installation

```bash
# Initialize Go modules
go mod tidy

# Run the application
go run cmd/main.go
```

### Configuration

Copy `config.example.yml` to `config.yml` and modify as needed:

- Server port
- TLS certificates
- JWT secret
- Database connection (if applicable)

### Running Tests

```bash
# Run all tests
go test ./...

# Check test coverage
go test -coverprofile=coverage.out
```

### Docker Deployment

```bash
# Build Docker image
docker build -t securego .

# Run Docker container
docker run -p 8080:8080 securego
```

## Project Structure

```
securego/
│
├── cmd/           # Main application entry point
├── internal/      # Private packages
│   ├── handlers/  # HTTP request handlers
│   ├── models/    # Data models
│   ├── services/  # Business logic
│   └── middleware/# Request middleware
├── configs/       # Configuration files
├── scripts/       # Utility scripts
└── README.md
```

## Development Roadmap

See [roadmap](/ROADMAP.md)
