---
name: discovery-research-synthesis
description: >
  Synthesize raw user interview notes into structured product insights.
  Use when the user says "synthétise mes interviews", "analyse mes notes de recherche",
  "fais la synthèse de ma discovery", "what did I learn from my interviews", or
  "transforme mes notes en insights".
---

# Research Synthesis

Transforms raw interview notes (bullet points, transcripts, voice-to-text) into a structured insight document ready to feed the product brief.

## Workflow

**Step 1 — Collect inputs**
Ask the user to paste or attach their raw notes. Accept any format: bullet points, full transcripts, voice-to-text dumps, Notion exports. Ask how many interviews were conducted and which user type was interviewed.

**Step 2 — Extract and cluster**
Read all notes and identify recurring patterns across interviews. Cluster findings into themes — don't force a structure upfront, let the themes emerge from the data.

**Step 3 — Produce the synthesis document**

```markdown
# Research Synthesis — [Feature / Topic]

**Interviews conducted:** [N]
**User type(s):** [e.g. Knowledge Manager, Agent, DRC]
**Date:** [date]

---

## Key Themes
[3-5 recurring patterns observed across multiple interviews, each with a short explanation and supporting quotes]

### Theme 1: [Name]
[2-3 sentence explanation]
> "[Direct quote]" — [User type, optionally anonymized]

---

## Pain Points
[Ranked by frequency/severity — what frustrates users most today]

| Pain point | Severity | Frequency | Supporting quote |
|---|---|---|---|
| [description] | High/Med/Low | [N/N interviews] | "[quote]" |

---

## Jobs to Be Done
[What users are actually trying to accomplish, framed as "When I... I want to... so I can..."]

---

## Opportunities
[Specific product opportunities surfaced by the research — actionable, not generic]

---

## Recommended Focus
[Top 1-2 bets based on the data — what to prioritize and why]
```

**Step 4 — Gut-check**
After presenting the synthesis, ask: "Does this match what you heard in the field? Anything missing or misrepresented?"

**Step 5 — Save and link**
Save as `research-synthesis-[topic].md` in the current project folder. Offer to update `project.md` if it exists.

## Quality Bar

- Every pain point and opportunity must be grounded in at least one quote or observation — no invented insights
- Themes should be specific to what was heard, not generic PM observations
- The "Recommended Focus" must follow from the data, not from prior assumptions
