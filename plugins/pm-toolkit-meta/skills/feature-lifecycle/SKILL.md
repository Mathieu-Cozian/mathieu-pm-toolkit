---
name: feature-lifecycle
description: >
  Start and track the full PM lifecycle for a feature — from discovery to release.
  Use when the user says "démarre le projet X", "lance une nouvelle feature", "start a PM project",
  "initialise le projet", "où en est ma feature", or "quelle est la prochaine étape".
---

# Feature Lifecycle

Orchestrates the full PM delivery cycle for a feature. Creates a `project.md` in the current directory to track progress and carry context across sessions.

## On First Invocation

Ask the user:
1. Feature name
2. One-line problem it solves
3. Module(s) affected (Knowledge / Selfcare / Academy / AI / Cross-product)

Then create `project.md` in the current working directory:

```markdown
# [Feature Name]

**Module:** [module(s)]
**Problem:** [one-liner]
**Started:** [date]

## Lifecycle

### Discovery
- [ ] Kick-off — `/discovery-kick-off`
- [ ] Interview guide — `/discovery-interview-guide`
- [ ] Research synthesis — `/discovery-research-synthesis`
- [ ] User journey — `/discovery-user-journey`
- [ ] Value proposition — `/discovery-claim-value-prop`
- [ ] Competitive benchmark — `/discovery-competitive-benchmark`
- [ ] First use case — `/discovery-first-use-case`
- [ ] MVP definition — `/discovery-mvp-definition`
- [ ] Prioritization — `/strategy-prioritization`

### Delivery
- [ ] Product brief — `/discovery-product-brief`
- [ ] Spec — `/delivery-spec-writer`
- [ ] Documentation — `/delivery-documentation`
- [ ] Release notes — `/delivery-release-notes`
- [ ] Stakeholder announcement — `/delivery-stakeholder-announcement`

## Artifacts
<!-- Add links to produced files here -->
```

After creating the file, display the lifecycle map and suggest the first step.

## On Subsequent Invocations

Read the existing `project.md` and:
- Show current progress (checked vs unchecked steps)
- Identify the next logical step
- When the user completes a step, mark it as done (`[x]`) and add the artifact link under Artifacts
- If an artifact was produced, ask for the filename to record it

## Principles

- Never skip phases without asking — some features may legitimately skip steps (e.g. no user interviews for a quick internal tool)
- Each phase maps to a specific skill; always name it so the user knows what to invoke
- The sequencer tracks state; the individual skills do the work
- If the user is mid-lifecycle and `project.md` already exists, read it first before suggesting anything
