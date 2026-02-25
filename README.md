# Go Boilerplate

A production-ready Go boilerplate designed for building scalable, maintainable backend services with minimal abstraction and maximum control.

---

## 🚀 Tech Stack

### Framework: Echo

We use **Echo**, a lightweight and high-performance Go web framework.

- Focuses on routing and HTTP handling
- Minimal abstraction
- Reduces unnecessary boilerplate
- Keeps the architecture clean and explicit

---

### Database Driver: pgx

We use **pgx** as the PostgreSQL driver.

- No ORM
- No query abstraction layer
- Raw SQL only

This ensures:

- Better performance
- Full query control
- Production-level flexibility

---

### Logging: Zerolog

We use **zerolog** for structured logging.

Although modern Go provides `slog` (native structured logging), we prefer zerolog because:

- Mature ecosystem
- Better integrations (e.g., pgx logging)
- Proven production reliability

---

### Observability: New Relic

We use **New Relic** for application observability.

- Distributed tracing support
- Application logs forwarding
- Runtime performance monitoring
- Better production debugging and visibility

---

### Validation: go-playground/validator

We use `go-playground/validator` for request validation instead of writing custom validation logic.

- Struct-based validation
- Tag-driven rules
- Widely adopted and production-tested

---

### Configuration Management: Koanf

We use **koanf** for configuration management.

Why Koanf over Viper?

- Lightweight
- Modular design
- Cleaner API
- Viper is comparatively heavier

---

### Authentication: Clerk

We use **Clerk** for authentication and user management.

- Secure sign-in and session management
- User and organization management out of the box
- JWT-based auth flows that work well with APIs

This allows us to avoid building and maintaining custom auth infrastructure.

---

### Database Migrations: Tern

We use **Tern** for managing database migrations.

Other popular alternatives include:

- Goose
- golang-migrate

Tern keeps migrations simple and SQL-focused.

---

### Testing: Testify

We use **testify** for:

- Assertions
- Mocking (when required)
- Cleaner test structure

---

### Integration Testing: Testcontainers

We use **Testcontainers** to spin up real Docker containers during tests.

Benefits:

- Avoid mocking databases
- Use real PostgreSQL instances
- Production-like test environment
- Reliable integration testing

---

## 🏗 Philosophy

- No ORM
- Raw SQL only
- Minimal abstraction
- High performance
- Production-first architecture
- Clean and modular structure
