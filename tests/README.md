# tests/

Automated test suites.

| Sub-directory | Description |
|---|---|
| `unit/` | Fast, isolated tests for individual classes and functions |
| `integration/` | Tests that exercise multiple components together (API + database) |
| `e2e/` | Full end-to-end flow tests and supporting fixtures |

The directory layout under `unit/` and `integration/` mirrors the `src/` tree so that the corresponding test for `src/modules/finance/tuition/billing/` is located at `tests/unit/modules/finance/tuition/billing/`.
