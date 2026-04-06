---
name: delivery-stakeholder-announcement
description: >
  Write internal stakeholder announcements for a feature launch.
  Use when the user says "rédige l'annonce interne", "écris le message de lancement",
  "prépare la communication interne", "annonce la feature à l'équipe", or
  "draft the stakeholder announcement".
---

# Stakeholder Announcement

Drafts internal communications for a feature launch — concise enough to be read, specific enough to be useful.

## Workflow

**Step 1 — Collect inputs**
Ask for:
- The feature name and what it does (or link to the spec/brief)
- Who the announcement is for (CS team, Sales, all-hands, specific squad)
- Target date / when it goes live
- Any action required from the audience (e.g. "update your onboarding script", "inform your accounts")

**Step 2 — Produce two formats**

### Format A — Slack message (short)
```
🚀 *[Feature Name]* est en ligne !

[1-2 sentences: what it does and why it matters for the audience]

*Ce que ça change pour vous :*
• [Concrete change 1]
• [Concrete change 2]

📄 Spec : [link] | 📖 Doc : [link]

Des questions ? Pinguez [PM name] ou répondez ici.
```

### Format B — Notion / Email (structured)
```markdown
# [Feature Name] — Lancement [date]

## C'est quoi ?
[2-3 sentences: what the feature does, which module, who it's for]

## Pourquoi on l'a fait ?
[The problem it solves — anchored in user feedback or a business need]

## Ce qui change concrètement
[Bullet list of tangible changes for the audience]

## Comment le tester / l'utiliser
[Short steps or pointer to documentation]

## Liens utiles
- Spec : [link]
- Documentation : [link]
- Contact : [PM name]
```

**Step 3 — Tone check**
Internal announcements use a direct, collegial tone — less formal than external brand voice, but still clear and professional. No hyperbole, no "incredibly exciting." Facts and impact.

**Step 4 — Save**
Save as `announcement-[feature]-[date].md` in the current project folder. Offer to push to Notion and ask which page to post it under.
