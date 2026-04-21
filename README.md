# Collegium

> **Collegium** (Latin, *n.*) – a body of colleagues; a college or guild organized around a shared purpose.

Collegium is a modular academic-management platform covering the full lifecycle of a higher-education institution: admissions, academics, finance, and student services.

---

## Repository Structure

```
Collegium/
├── src/                          # Application source code
│   ├── core/                     # Cross-cutting concerns
│   │   ├── domain/               # Domain logic (models + services)
│   │   │   ├── models/
│   │   │   │   ├── academic/
│   │   │   │   │   ├── courses/
│   │   │   │   │   │   └── assessments/        ← 7 levels deep
│   │   │   │   │   └── programs/
│   │   │   │   │       └── requirements/
│   │   │   │   └── administrative/
│   │   │   │       ├── staff/
│   │   │   │       │   └── roles/
│   │   │   │       └── facilities/
│   │   │   │           └── rooms/
│   │   │   └── services/
│   │   │       ├── enrollment/
│   │   │       │   └── workflows/
│   │   │       └── scheduling/
│   │   │           └── conflicts/
│   │   └── infrastructure/       # Persistence & transport adapters
│   │       ├── database/
│   │       │   ├── migrations/
│   │       │   └── seeds/
│   │       └── api/
│   │           ├── rest/
│   │           │   ├── v1/
│   │           │   └── v2/
│   │           └── graphql/
│   │               └── schemas/
│   ├── modules/                  # Feature modules
│   │   ├── admissions/
│   │   │   ├── application/
│   │   │   │   ├── forms/
│   │   │   │   └── review/
│   │   │   └── enrollment/
│   │   │       └── onboarding/
│   │   ├── academics/
│   │   │   ├── curriculum/
│   │   │   │   ├── design/
│   │   │   │   └── delivery/
│   │   │   │       └── resources/
│   │   │   └── grading/
│   │   │       ├── rubrics/
│   │   │       └── reports/
│   │   ├── finance/
│   │   │   ├── tuition/
│   │   │   │   └── billing/
│   │   │   └── financial-aid/
│   │   │       ├── scholarships/
│   │   │       └── grants/
│   │   └── student-services/
│   │       ├── advising/
│   │       │   └── appointments/
│   │       └── counseling/
│   │           └── resources/
│   └── shared/                   # Shared utilities & constants
│       ├── utils/
│       │   ├── formatters/
│       │   └── validators/
│       └── constants/
├── docs/                         # Documentation
│   ├── architecture/
│   │   ├── diagrams/
│   │   │   ├── system/
│   │   │   └── data-flow/
│   │   └── decisions/
│   │       └── adr/              # Architecture Decision Records
│   ├── api/
│   │   ├── rest/
│   │   │   └── endpoints/
│   │   └── graphql/
│   │       └── schemas/
│   └── user-guides/
│       ├── admin/
│       │   └── operations/
│       └── student/
│           └── getting-started/
├── tests/                        # Automated tests
│   ├── unit/
│   │   ├── core/
│   │   │   ├── domain/
│   │   │   │   └── models/
│   │   │   └── infrastructure/
│   │   └── modules/
│   │       ├── admissions/
│   │       ├── academics/
│   │       ├── finance/
│   │       └── student-services/
│   ├── integration/
│   │   ├── api/
│   │   │   ├── rest/
│   │   │   └── graphql/
│   │   └── database/
│   └── e2e/
│       ├── flows/
│       │   ├── admissions/
│       │   └── academics/
│       └── fixtures/
├── config/                       # Environment & schema configuration
│   ├── environments/
│   │   ├── development/
│   │   ├── staging/
│   │   └── production/
│   └── schemas/
│       ├── database/
│       └── validation/
└── scripts/                      # Operational scripts
    ├── build/
    │   ├── ci/
    │   └── release/
    ├── deploy/
    │   ├── staging/
    │   └── production/
    └── maintenance/
        ├── backup/
        └── migration/
```

---

## Top-level Sections

| Directory  | Purpose |
|------------|---------|
| `src/`     | All application source code, split between `core/` (shared domain + infrastructure) and `modules/` (feature areas) |
| `docs/`    | Architecture diagrams, API references, and end-user guides |
| `tests/`   | Unit, integration, and end-to-end test suites mirroring the `src/` layout |
| `config/`  | Environment-specific settings and JSON/YAML schema files |
| `scripts/` | CI build, deploy, backup, and migration automation scripts |

---

## Depth Reference

| Path example | Depth |
|---|---|
| `src/` | 1 |
| `src/core/` | 2 |
| `src/core/domain/` | 3 |
| `src/core/domain/models/` | 4 |
| `src/core/domain/models/academic/` | 5 |
| `src/core/domain/models/academic/courses/` | 6 |
| `src/core/domain/models/academic/courses/assessments/` | **7** |