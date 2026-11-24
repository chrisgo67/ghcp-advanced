---
name: run-and-fix-tests
description: Run the test suite and fix any failures. Use when asked to run tests, verify changes, or ensure tests pass.
---

# Run and fix tests

1. Run `npm test`.
2. If all tests pass, report success and stop.
3. If tests fail, fix the **source code** (not the tests).
4. Re-run. Repeat up to 3 cycles, then report remaining failures.
