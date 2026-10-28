---
applyTo: "tests/**"
---

# Test rules
- Unit tests call service functions with `MagicMock` repositories; no database access and no HTTP calls.
- One behaviour per test.
- Name tests as `test_<function>_<situation>`.
- A bug fix starts with a test that fails on the current code.
- Never weaken or delete an existing assertion.
- If the needed behavior is unclear or a required contract is ambiguous, stop and ask instead of guessing.
