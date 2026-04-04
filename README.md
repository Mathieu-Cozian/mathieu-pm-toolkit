# Mathieu PM Toolkit

A Claude plugin marketplace for product management, covering the full product lifecycle from discovery to delivery.

## Plugins

### pm-discovery
Product discovery skills following the FOCUSED framework (Frame > Observe > Claim > Unfold > Steal > Execute > Decide).

| Command | Phase | Description |
|---------|-------|-------------|
| `/pm-discovery:kick-off` | Frame | Start a discovery with kick-off doc + Project Ambition |
| `/pm-discovery:interview-guide` | Observe | Generate a structured user research interview guide |
| `/pm-discovery:first-use-case` | Observe | Synthesize interviews into a First Use Case (FUC) |
| `/pm-discovery:claim` | Claim | Define value prop with Press Release + Launch Tweet |
| `/pm-discovery:user-journey` | Unfold | Map current/future user journeys + key touchpoints |
| `/pm-discovery:competitive-benchmark` | Steal | Run competitive benchmark + extract Gold Nuggets |
| `/pm-discovery:mvp-definition` | Execute | Define MVP scope with OST + RICE prioritization |
| `/pm-discovery:product-brief` | Decide | Write the full PRD / Product Brief |

### pm-delivery
Product delivery skills for specs, documentation, and release communication.

| Command | Description |
|---------|-------------|
| `/pm-delivery:spec` | Transform feature ideas into Notion-optimized product specs |
| `/pm-delivery:documentation` | Create professional French documentation articles |
| `/pm-delivery:release-notes` | Generate Mayday-format release notes in French |

### pm-toolkit-meta
Maintenance skill for managing the toolkit itself.

| Command | Description |
|---------|-------------|
| `/pm-toolkit-meta:manage` | List, create, update, or delete skills |

## Installation

```
/plugin marketplace add Mathieu-Cozian/mathieu-pm-toolkit
/plugin install pm-discovery@mathieu-pm-toolkit
/plugin install pm-delivery@mathieu-pm-toolkit
/plugin install pm-toolkit-meta@mathieu-pm-toolkit
```
