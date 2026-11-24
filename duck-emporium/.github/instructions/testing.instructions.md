---
applyTo: "tests/**/*.test.ts"
---

# Testing instructions

This project uses Vitest with Node as the test environment.

## Commands

- Run all tests: `npm test`
- Run one test file: `npx vitest run tests/path/to/file.test.ts`
- Run type checking: `npm run typecheck`
- Run in watch mode: `npx vitest`

Test changes should first be checked with the smallest relevant Vitest file or filter, then with `npm test` and `npm run typecheck` when the change affects shared behavior.

## Test organization

- Keep unit tests under `tests/unit/`.
- Keep HTTP contract tests under `tests/contract/`.
- Keep cross-module or application-level tests under `tests/integration/`.
- Shared test setup belongs in `tests/_helpers/`.
- Use `tests/**/*.test.ts` files recognized by `vitest.config.ts`.

## Test style

- Import Vitest APIs explicitly; globals are disabled.
- Use descriptive `describe` and `test` names that state behavior and scenario.
- Prefer focused assertions over snapshots.
- Use the existing test helpers for app construction and setup.
- Reset mutable state and environment variables between tests.
- Avoid fixed or external ports, real network services, real payment providers, and real credentials.
- Use the test admin secret expected by the Vitest configuration; do not add real secrets to tests.

## Coverage expectations

- Add or update an automated test for each user story behavior implemented.
- Cover both the success path and relevant validation or error path.
- For API changes, test the route response status, content type or JSON shape, and meaningful data.
- For pure business logic, prefer unit tests at the smallest behavioral boundary.
- For changes spanning routing and multiple modules, add integration or contract coverage in addition to focused tests.
- Do not weaken or remove existing assertions to make a failing implementation pass.
