# src/

Application source code.

| Sub-directory | Description |
|---|---|
| `core/` | Cross-cutting concerns: domain models, domain services, and infrastructure adapters (database, API) shared across all feature modules |
| `modules/` | Self-contained feature modules (admissions, academics, finance, student-services) |
| `shared/` | Utility helpers, formatters, validators, and constants reused by every module |
