# Building From the Plan

With a reviewed plan in source control, delivery becomes the agent's job. Your job is to point it at the plan, keep it honest, and review the result.

### Example

**1. The plan is checked in:** `docs/plans/monitor-health-check.md`

```markdown
## Goal
Add a /health endpoint to the monitor service.

## Tasks
1. Add a health endpoint that reports ingestion-service connectivity.
2. Add unit tests for healthy and unreachable states.
3. Document the endpoint in the service README.

## Acceptance
- `dotnet build` and `dotnet test` pass.
- /health returns 200 when ingestion is reachable, 503 when it isn't.
```

**2. Hand it to the agent:**

> *"Implement `docs/plans/monitor-health-check.md` one task at a time. After each task, build and run the tests, and don't move on until they pass. When you're done, check every item under Acceptance and open a PR that includes the plan and any skill updates. Then watch the PR until CI is green. If it fails, fix the issues, commit, and push. Keep going until CI is fully green or I ask you to stop."*

**3. You review the PR against the plan, not line by line.** Did it meet the acceptance criteria? Did it stay within scope?

### Coming soon: Guardrails Lite

In a future session, I'll demo building from a plan with [**Guardrails Lite**](https://github.com/Servant-Software-LLC/Guardrails/issues/823):

- The plan is broken down into a set of tasks, each with **deterministic guardrails** such as tests, exit codes, and checks.
- Scripts track progress and verdicts. **The agent never grades its own work.**
- The guardrails are locked during a run, so an agent can't weaken a check to get it to pass.
- It's text-only: skills and readable scripts, with no compiled binary to approve.

---

[← Back](06-making-a-plan.md)
