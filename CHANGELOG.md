# Changelog

## 0.2.0 — 2026-04-06

### New skills
- `feature-lifecycle` (pm-toolkit-meta) — full PM lifecycle sequencer; creates `project.md` in the working directory to track progress across sessions
- `discovery-research-synthesis` (pm-discovery) — synthesizes raw interview notes into themes, pain points, JTBD, and opportunities
- `strategy-prioritization` (pm-strategy) — RICE scoring with qualitative overlay and ranked recommendation
- `delivery-stakeholder-announcement` (pm-delivery) — internal launch comms in two formats (Slack + Notion/email)

### Infrastructure
- Added `CLAUDE.md` at repo root — always-loaded lightweight context index for Claude Code sessions
- Added `shared/product-context/` — 5 on-demand context files covering each Mayday module (Knowledge, Selfcare, Academy, AI, Overview)

### Improvements
- `delivery-documentation`: trimmed from 2,335 to 490 words (−79%); verbose examples removed since reference files already cover them
- `delivery-spec-writer`: removed duplicate terminology section (now in CLAUDE.md); analytics format switched to table; edge cases scoped to functional conflicts only; Notion push asks destination first
- `competitive-intelligence`: Notion push asks destination first; saves to current project folder
- `toolkit-meta`: fixed broken session paths; updated to reflect current repo structure and plugin layout
- `brand-voice-guidelines`: removed visual identity section (typography, colors, tokens) — irrelevant for PM skills
- `CLAUDE.md`: context files load on demand, not upfront on every task

---

## 0.1.x — 2026-03-xx

### New skills
- `brand-voice-check` (pm-brand) — audits content against Mayday brand voice guidelines
- `brand-voice-rewrite` (pm-brand) — rewrites content in Mayday's voice with before/after comparison
- `competitive-intelligence` (pm-strategy) — weekly AI & KM market intelligence report

### Infrastructure
- Added YAML frontmatter to all SKILL.md files for Claude Code skill registration
- Added pre-push hook to auto-update Claude plugins on current machine
- Added GitHub Action to auto-bump plugin patch version on push to main
- Added Notion auto-sync for skill registry on create/update

### Initial release (0.1.0)
- `pm-discovery` plugin: 8 skills covering the full FOCUSED discovery framework (kick-off, interview guide, user journey, value prop, competitive benchmark, first use case, MVP definition, product brief)
- `pm-delivery` plugin: spec writer, documentation generator, release notes
- `pm-toolkit-meta` plugin: toolkit management skill
