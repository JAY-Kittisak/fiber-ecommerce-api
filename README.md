# Fiber E-commerce API

A RESTful E-commerce API built with Go Fiber, GORM, and PostgreSQL.

## Features

- User registration and login with JWT authentication
- Admin registration and dashboard
- User profile endpoint
- Role-based access control (admin, user, moderator)
- Swagger API documentation

## Project Structure

```
cmd/                # Application entrypoints (api, migrate)
docs/               # Swagger docs
internal/           # Application core and adapters
  adapters/
    http/           # HTTP handlers, middleware, routes
    persistence/    # Database models and repositories
  config/           # Configuration, database, seeder
  core/
    domain/         # Domain entities and ports
    services/       # Business logic
pkg/                # Utilities (JWT, password, validator)
```

## Getting Started

### Prerequisites

- Go 1.18+
- Docker (for PostgreSQL)

### Setup

1. **Clone the repository**

   ```sh
   git clone https://github.com/JAY-Kittisak/fiber-ecommerce-api.git
   cd fiber-ecommerce-api
   ```

2. **Copy and edit environment variables**

   ```sh
   cp .env.example .env
   # Edit .env as needed
   ```

3. **Start PostgreSQL with Docker**

   ```sh
   docker-compose up -d
   ```

4. **Run the API server**

   ```sh
   go run cmd/api/main.go
   ```

5. **Run database migrations**

   ```sh
   go run cmd/migrate/main.go -up
   ```

### API Documentation

- Swagger UI: [http://localhost:3000/swagger/index.html](http://localhost:3000/swagger/index.html)

## Environment Variables

See [.env](.env) for all configuration options.

## License

[Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)
