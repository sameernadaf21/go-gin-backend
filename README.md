# go-gin-backend

Simple Go backend using Gin with improvements: graceful shutdown, request logging, CORS, and health endpoint.

## Run locally

Make sure you have Go installed (1.20+ recommended).

Windows PowerShell example:

```powershell
$env:PORT = "8081"
go run main.go
```

Then visit http://localhost:8080/ and http://localhost:8080/health

## Build Docker image

```powershell
docker build -t go-gin-backend:latest .
docker run -p 8080:8080 -e PORT=8080 go-gin-backend:latest
```

## Environment

- PORT: port to listen on (default 8080)
- GIN_MODE: gin mode (debug/release)

## Notes

This repository contains a minimal API. Consider adding config management, structured logging (e.g., zerolog or zap), metrics, and tests for production readiness.
