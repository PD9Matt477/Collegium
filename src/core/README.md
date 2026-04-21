# src/core/

Cross-cutting concerns that every feature module depends on.

| Sub-directory | Description |
|---|---|
| `domain/` | Pure business logic: domain models and domain services with no framework dependencies |
| `infrastructure/` | Adapter layer connecting the domain to the outside world (database, REST API, GraphQL) |
