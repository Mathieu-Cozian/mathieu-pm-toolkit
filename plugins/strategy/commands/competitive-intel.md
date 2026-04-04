---
description: Run a weekly competitive intelligence scan on AI and knowledge management
argument-hint: [time period, e.g. "this week" or "March 24-31"]
allowed-tools: Read, WebSearch, WebFetch
---

First, read the following context files from the project folder if they exist:
- USER.md
- BUSINESS.md
- ICP.md

Then read and follow the instructions in @${CLAUDE_PLUGIN_ROOT}/skills/competitive-intelligence/SKILL.md.

Run the competitive intelligence scan for: $ARGUMENTS

If no time period is provided, default to the past 7 days from today.
