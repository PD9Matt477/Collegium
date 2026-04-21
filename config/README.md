# config/

Configuration files for all runtime environments.

| Sub-directory | Description |
|---|---|
| `environments/development/` | Local development overrides (e.g. SQLite, mock mailer) |
| `environments/staging/` | Staging environment settings |
| `environments/production/` | Production settings (secrets injected via environment variables) |
| `schemas/database/` | JSON/YAML schema files for database table definitions |
| `schemas/validation/` | JSON Schema / Joi / Zod schemas for API input validation |
