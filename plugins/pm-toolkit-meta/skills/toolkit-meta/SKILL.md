---
name: toolkit-meta
description: >
  Manage the Mathieu PM Toolkit — list, create, update, or delete skills directly from a conversation.
  Use when the user wants to modify the toolkit, says "gère le toolkit", "ajoute un skill",
  "modifie ce skill", "liste les skills", or "manage the PM toolkit".
---

# toolkit-meta

## Description

Skill de maintenance du PM Toolkit. Permet de modifier des skills existants, d'en créer de nouveaux, de les supprimer, ou d'obtenir un état des lieux complet — directement depuis une conversation, sans toucher GitHub manuellement.

## Repo

- **Local :** `/Users/mathieucozian/claude/mathieu-pm-toolkit/`
- **GitHub :** `https://github.com/Mathieu-Cozian/mathieu-pm-toolkit`

## Structure

```
plugins/
  <plugin-name>/
    .claude-plugin/plugin.json   ← plugin metadata (name, version, description)
    skills/
      <skill-name>/
        SKILL.md                 ← skill instructions
        references/              ← optional reference files
```

Plugins actuels : `pm-brand`, `pm-delivery`, `pm-discovery`, `pm-strategy`, `pm-toolkit-meta`

## Instructions

### A) Modifier un skill existant
1. Lire le SKILL.md concerné
2. Appliquer les modifications
3. Committer + pusher (voir commandes Git ci-dessous)

### B) Créer un nouveau skill
1. Demander : dans quel plugin ? quel nom de skill ? quel livrable ? quels déclencheurs naturels ?
2. Créer `plugins/<plugin>/skills/<skill-name>/SKILL.md` en suivant la structure standard
3. Committer + pusher

### C) Supprimer un skill
1. Confirmer avec l'utilisateur
2. Supprimer le dossier `plugins/<plugin>/skills/<skill-name>/`
3. Committer + pusher

### D) Lister les skills
Lire chaque SKILL.md et afficher un tableau : nom, plugin, trigger principal, livrable.

### E) Bumper la version d'un plugin
Modifier le champ `version` dans `plugins/<plugin>/.claude-plugin/plugin.json`. Conventions : patch (fix/trim), minor (nouveau skill), major (refonte).

## Structure standard d'un SKILL.md

```markdown
---
name: <skill-name>
description: >
  [Ce que fait le skill en 1-2 phrases.]
  [Triggers : "Use when the user says X, Y, Z."]
---

# <Titre>

[Instructions pour Claude — workflow, règles, format de sortie]
```

## Commandes Git

```bash
cd /Users/mathieucozian/claude/mathieu-pm-toolkit
git add plugins/<plugin>/skills/<skill>/SKILL.md
git commit -m "<feat|update|fix|remove>: <description courte>"
git push origin main
```

## Notion — Registre des skills

Si l'utilisateur veut synchroniser un nouveau skill dans Notion :
- **Demander** dans quelle page/DB Notion créer l'entrée avant d'agir
- Champs à remplir : Nom, Plugin, Description, Triggers, GitHub URL, Statut (`Active`)
- GitHub URL format : `https://github.com/Mathieu-Cozian/mathieu-pm-toolkit/blob/main/plugins/<plugin>/skills/<skill>/SKILL.md`

Ne jamais créer de page Notion sans avoir confirmé la destination avec l'utilisateur.

## Bonnes pratiques pour les skills

- Instructions **actionnables et précises** — Claude doit savoir exactement quoi produire
- Triggers **naturels** — ce que l'utilisateur dirait spontanément
- Livrable **concret** — un document, un tableau, une liste structurée
- Garder les skills **lean** — pas d'exemples verbeux si des fichiers de référence existent
- Référencer `shared/product-context/` et `shared/brand-voice/` plutôt que dupliquer le contexte
