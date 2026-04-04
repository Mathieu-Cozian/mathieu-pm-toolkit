---
name: toolkit-meta
description: Manage the Mathieu PM Toolkit — list, create, update, or delete skills. Trigger when the user says "mets à jour le skill", "ajoute un nouveau skill", "crée un skill", "supprime le skill", "liste mes skills", "montre-moi mes skills", "gère mon toolkit".
---

# toolkit-meta

## Description

Skill de maintenance du plugin Mathieu PM Toolkit. Permet à Mathieu de modifier des skills existants, d'en créer de nouveaux, de les supprimer, ou d'obtenir un état des lieux complet du plugin — directement depuis une conversation Cowork, sans avoir à toucher GitHub manuellement.

## Triggers

Ce skill se déclenche quand Mathieu dit :
- "Mets à jour le skill [nom]"
- "Modifie le skill [nom]"
- "Améliore le skill [nom]"
- "Ajoute un nouveau skill"
- "Crée un skill pour [X]"
- "Supprime le skill [nom]"
- "Liste mes skills"
- "Montre-moi mes skills"
- "C'est quoi mes skills ?"
- "Qu'est-ce que le toolkit contient ?"
- "Met à jour mon plugin"
- "Gère mon toolkit"

## Contexte du plugin

- **Repo GitHub :** `https://github.com/Mathieu-Cozian/mathieu-pm-toolkit`
- **Repo local (session) :** `/sessions/optimistic-happy-meitner/mayday-skills/`
- **Structure des skills :** `skills/<nom-du-skill>/SKILL.md`
- **Credentials Git :** `~/.git-credentials` (PAT GitHub)

## Instructions

### 1. Identifier l'intention

Avant toute action, détermine ce que Mathieu veut faire :

**A) Modifier un skill existant**
→ Demander : quel skill ? quels changements ?
→ Lire le SKILL.md concerné
→ Appliquer les modifications
→ Committer + pusher
→ Rappeler de refresh le plugin dans Cowork

**B) Créer un nouveau skill**
→ Demander : nom du skill, phase/contexte, livrable attendu, déclencheurs naturels
→ Créer `skills/<nouveau-skill>/SKILL.md` en suivant la structure standard (voir ci-dessous)
→ Committer + pusher
→ Proposer d'ajouter une entrée dans le registre Notion `claude_skills`

**C) Supprimer un skill**
→ Confirmer avec Mathieu avant de supprimer
→ Supprimer le dossier `skills/<nom-du-skill>/`
→ Committer + pusher

**D) Lister les skills**
→ Faire un `ls skills/` pour lister les dossiers
→ Lire chaque SKILL.md pour extraire : nom, phase, trigger principal, livrable
→ Afficher un tableau récapitulatif propre

### 2. Structure standard d'un SKILL.md

Quand tu crées un nouveau skill, utilise cette structure :

```markdown
# <nom-du-skill>

## Description
[1-2 phrases : à quoi sert ce skill, dans quel contexte]

## Triggers
[Liste des phrases naturelles qui déclenchent ce skill]

## Contexte requis
[Ce que Mathieu doit fournir pour que le skill fonctionne bien]

## Livrable
[Ce que produit le skill : document, tableau, liste, etc.]

## Instructions
[Instructions détaillées pour Claude — étape par étape]

## Format de sortie
[Structure précise du livrable produit]
```

### 3. Commandes Git à utiliser

**Pour committer et pusher :**
```bash
cd /sessions/optimistic-happy-meitner/mayday-skills
git add <fichiers modifiés>
git commit -m "<type>: <description courte>"
git push origin main
```

Types de commit : `update` (modification), `feat` (nouveau skill), `remove` (suppression), `fix` (correction)

**Si le repo local n'est pas à jour :**
```bash
cd /sessions/optimistic-happy-meitner/mayday-skills
git pull origin main
```

### 4. Après chaque modification

Toujours rappeler à Mathieu :

> "C'est pushé sur GitHub ✅ Pour que les changements soient actifs dans Cowork, va dans **Customize → ton plugin → Refresh** (ou désinstalle/réinstalle le plugin)."

### 5. Registre Notion

Si un nouveau skill est créé, proposer d'ajouter une entrée dans la base Notion `claude_skills`. Les champs à remplir :
- **Nom** : nom du skill
- **Description** : 1 phrase
- **Phase** : Frame / Observe / Claim / Unfold / Steal / Execute / Decide / Meta / Delivery / Strategy
- **Trigger principal** : la phrase déclenchante principale
- **Livrable** : le document/output produit
- **Statut** : Actif

### 6. Bonnes pratiques pour les skills

Quand tu améliores ou crées un skill, garde en tête :
- Les instructions doivent être **actionnables et précises** — Claude doit savoir exactement quoi produire
- Les triggers doivent être **naturels** — ce que Mathieu dirait spontanément
- Le livrable doit être **concret** — un document, un tableau, une liste structurée
- Les skills Discovery suivent le **framework FOCUSED** : Frame → Observe → Claim → Unfold → Steal → Execute → Decide
- Toujours inclure un **format de sortie** explicite pour que l'output soit cohérent
