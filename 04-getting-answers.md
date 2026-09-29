# Getting Answers: Ask the Agents

Your first stop for a question about the codebase should be an agent, not a teammate's calendar.

### Knowledge skills in Bifrost

The Bifrost repo includes two skills that give agents deep context on the product:

- **`bifrost-dev-knowledge`**: how the code is built, structured, and tested
- **`bifrost-domain-knowledge`**: what the product does and why

Just ask in plain language:

> *"Tell me about the monitor service and how it authenticates to the ingestion service."*

### Skills that improve themselves

These skills are **self-improving**. When an agent learns something new while doing your work, it updates the skill so that the next person, or the next agent, starts out knowing more.

**Commit the updated skills in your PRs.** Knowledge that stays on your machine helps no one.

### Ask the agents to review your plans

Before you hand a plan off for delivery, have agents challenge it:

> *"Have an agent team with the appropriate roles look over my plan for any holes and/or improvements."*

A few minutes of critique catches gaps that are far more expensive to find in code.

---

[← Back](03-team-survey.md) | [Next →](05-organizing-sessions.md)
