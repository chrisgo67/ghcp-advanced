# Project: duck-emporium

This directory contains the hands-on Rubber Duck Emporium application exercise.

## Stack

- TypeScript and Node.js 20+.
- ES modules.
- Express for HTTP APIs.
- Vitest for automated tests.
- Node.js `node:`-prefixed built-in imports where applicable.
- Keep dependencies and configuration consistent with `package.json`, `package-lock.json`, `tsconfig.json`, and `vitest.config.ts`.

## Project structure

- `src/` contains application source code.
- `public/` contains static frontend assets.
- `tests/` contains automated tests.
- `data/` contains local application data.
- `.env.example` documents environment variables without containing real values.

## Implementation conventions

- Build the implementation incrementally from the relevant stories in `../user-stories/`.
- Read the repository's existing source, tests, and package scripts before making changes.
- Follow existing patterns for modules, routing, storage, validation, and error handling.
- Use environment variables for configuration and secrets.
- Do not commit real secrets or personal data.
- Use local JSON or SQLite-style storage unless a task explicitly requires a different approach.
- Mock payments; never integrate a real payment provider.
- Use a shared admin password from an environment variable for curator actions.
- Do not add real user accounts unless explicitly requested.

## TypeScript conventions

- Prefer explicit types at public boundaries and preserve strictness in `tsconfig.json`.
- Use ES modules and export/import syntax.
- Avoid unnecessary casts and `any`.
- Prefer existing helpers and project patterns over duplicate logic.
- Keep modules focused and changes surgical.

## API and frontend behavior

- Define and preserve clear HTTP status codes and JSON response shapes.
- Validate external input before use.
- Keep customer-facing and curator-facing behavior separate.
- Make navigation and user flows work for the relevant user story.
- Use accessibility-conscious markup and labels.

## Testing

- Run the smallest relevant Vitest test command first.
- Add or update an automated test for every user story implementation and behavior change.
- Cover success paths and meaningful validation or error paths.
- Do not weaken existing tests to make an implementation pass.
- Prefer `npm test -- --runInBand` or the script documented in `package.json` if available; inspect the script before guessing.

## Change quality

- Inspect the diff and existing behavior before editing.
- Keep generated data and sample fixtures fictional.
- Update directly related documentation only when behavior or setup changes.
- Do not change unrelated workshop content.
