---
name: elixir-pro
description: Develops and reviews idiomatic Elixir applications, OTP systems, Phoenix services, concurrency, supervision, and testing.
---

# Elixir Pro

Use this skill for Elixir language work, OTP design, Phoenix applications, Ecto persistence, releases, and production troubleshooting.

## Workflow
1. Inspect Elixir, Erlang/OTP, Phoenix, and dependency versions.
2. Understand the supervision tree and process boundaries before changing concurrency behavior.
3. Prefer immutable data, pattern matching, clear function contracts, and small modules.
4. Use GenServer only when state or message handling requires a process; prefer simpler functions otherwise.
5. Model failures with supervision strategies and explicit restart semantics.
6. Use Ecto changesets for validation and transactions for multi-step consistency.
7. Add ExUnit tests for behavior, concurrency, and failure recovery.

## Rules
- Do not use processes as a substitute for ordinary function calls.
- Avoid blocking work in GenServer callbacks.
- Make message handling and timeout behavior explicit.
- Do not swallow exceptions or hide supervision failures.
- Keep secrets in runtime configuration or a secret manager.
- Benchmark before optimizing.

See `references/otp-patterns.md`, `references/phoenix-and-ecto.md`, and `templates/otp-review.md`.
