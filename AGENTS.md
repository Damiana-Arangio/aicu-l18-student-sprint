# Repository guidance

This is the student L18 security sprint.

## Product facts

- The server owns `status` and computes `urgencyLabel`.
- Valid priorities are `bassa`, `normale`, and `alta`.
- Valid source channels are `email`, `telefono`, and `chat`.
- Ticket descriptions are plain text product content, not a rich-text feature.
- SQLite queries must remain parameterized.

## Task boundary

- Reproduce and explain the failing ticket-details security test.
- Apply the smallest context-appropriate fix.
- Preserve normal descriptions and existing behavior.
- Do not add dependencies, CSP, authentication, global sanitization, or broad refactors.
- Do not calculate server-owned fields in the client.
- Do not weaken, delete, or rewrite the hostile test to make it green.

## Verification

```bash
pnpm check
pnpm test
pnpm test:e2e
pnpm test:all
```

Review the final diff and be ready to explain why the test became green.
