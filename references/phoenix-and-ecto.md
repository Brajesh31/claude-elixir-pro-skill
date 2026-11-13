# Phoenix and Ecto Practices

## Phoenix
- Keep controllers and LiveViews focused on request/UI orchestration.
- Put reusable business rules in context modules.
- Validate authorization for every resource operation.
- Use PubSub for broadcast events, not as a durable queue.

## Ecto
- Use changesets for casting and validation.
- Enforce critical invariants with database constraints as well as application checks.
- Use transactions for multi-step writes that must succeed together.
- Preload associations intentionally to avoid N+1 queries.
- Treat migrations as production code and review destructive operations.

## Testing
Use ExUnit, DataCase, and ConnCase patterns appropriate to the boundary. Test database constraints and authorization failures, not only happy paths.
