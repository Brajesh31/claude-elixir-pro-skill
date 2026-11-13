# OTP Design Patterns

## Processes
Use a process when independent state, message handling, lifecycle, or fault isolation is required. Otherwise use a function.

## GenServer
- Keep callbacks short and non-blocking.
- Define message and call contracts.
- Set explicit timeouts.
- Avoid unbounded mailbox growth.
- Consider task supervision for concurrent work.

## Supervision
Choose restart strategy based on sibling independence:
- one_for_one: restart only the failed child;
- one_for_all: restart all children when they share coupled state;
- rest_for_one: restart later children that depend on an earlier child.

Define restart intensity and shutdown behavior deliberately.

## Observability
Log meaningful state transitions and failures. Avoid logging secrets or high-volume message payloads.
