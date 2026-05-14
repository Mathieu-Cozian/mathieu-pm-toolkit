---
name: obsidian-kb-update
description: >
  Extract new knowledge from the current conversation and write it to the Obsidian vault, after showing
  a preview and getting user confirmation. Optionally flags contradictions with existing notes.
  Use when the user says "mets ça dans ma KB", "capture ça dans Obsidian", "sauvegarde dans ma base
  de connaissance", "update my KB", "ajoute ça à mes notes", or "obsidian-kb-update".
---

# obsidian-kb-update

## Ce que fait ce skill

Extrait les informations nouvelles et actionnables de la conversation en cours, propose un plan
d'écriture dans Obsidian (quoi + où), attend la validation de l'utilisateur, puis écrit les notes.
En option (Step 2), recherche des contradictions dans la KB de façon autonome.

---

## Étape 1 — Extraction & Preview

### 1a. Scanner la conversation

Identifier tout ce qui mérite d'être capturé :

| Catégorie | Exemples |
|---|---|
| **Décisions** | Choix produit, tech, process arrêtés |
| **Apprentissages** | Insights, synthèses, conclusions de recherche |
| **Actions** | Tâches à faire, next steps |
| **Contexte projet** | Scope, objectifs, contraintes d'une feature |
| **Infos référence** | Contacts, outils, définitions, KPIs |
| **Réunions** | Résumés, verbatims clés |

Ne pas capturer : le contenu déjà présent dans la KB, les échanges de travail sans valeur durable,
les idées non mûres sans signal de confirmation de l'utilisateur.

### 1b. Mapper vers le vault

Pour chaque élément extrait, déterminer :
- Le **chemin de la note cible** (existante à patcher, ou nouvelle à créer)
- La **section** dans laquelle insérer (si patch)
- Le **format** : bullet, paragraph, frontmatter field

S'appuyer sur la connaissance du vault déjà chargée en début de conversation (`_INDEX.md`, `_STRUCTURE.md`, `memory-log.md`) pour choisir les bons chemins. En cas de doute sur l'emplacement, proposer deux options.

### 1c. Afficher le Preview

Présenter un tableau de confirmation **avant toute écriture** :

```
📋 Voici ce que je vais capturer dans ton vault :

| # | Note cible | Type | Contenu (aperçu) |
|---|---|---|---|
| 1 | Projets/mayday-search/decisions.md | Patch – ajout bullet | "Décision : on part sur un index Algolia..." |
| 2 | Claude/memory-log.md | Patch – ajout section | "Sprint 12 : objectif deliver Search v1 avant juin" |
| 3 | Reference/tools.md | Création | Nouvelle note sur l'outil X |

Étape 2 disponible : veux-tu aussi que je vérifie les contradictions avec ta KB existante ?

✅ Je valide → écris tout
✏️ Modifie le #2 → [préciser]
❌ Annule le #3
```

**Ne pas écrire avant confirmation explicite.**

---

## Étape 2 — Détection de contradictions (optionnel)

Déclenché si l'utilisateur dit "oui" à la vérification, ou demande explicitement.

### 2a. Recherche autonome dans le vault

Ne pas se limiter aux notes cibles. Rechercher de façon autonome dans le vault toutes les notes
qui pourraient contenir des informations liées aux sujets capturés :

```
mcp__obsidian__search_notes("<mot-clé ou concept>")
```

Lancer plusieurs recherches avec différents termes pour couvrir les angles possibles
(nom du projet, technologie, décision, personne impliquée, etc.). Lire les notes pertinentes
trouvées pour évaluer leur contenu.

### 2b. Comparer et signaler

Pour chaque contradiction détectée, afficher :

```
⚠️  Contradiction détectée

Note : Projets/mayday-search/decisions.md
Existant : "On utilise Elasticsearch pour l'indexation"
Nouveau   : "Décision : on part sur Algolia"

→ Laquelle est correcte ? Je mets à jour ou j'archive l'ancienne ?
```

Catégories de conflits à détecter :
- **Contradiction directe** : deux affirmations opposées sur le même fait
- **Obsolescence** : info ancienne remplacée par une décision plus récente
- **Doublon** : même info déjà présente, inutile de ré-écrire

### 2c. Résolution

Attendre la réponse de l'utilisateur pour chaque conflit avant d'écrire.
Options proposées : écraser, archiver l'ancienne version, garder les deux avec date.

---

## Étape 3 — Écriture dans Obsidian

Après validation (et résolution des conflits si Étape 2 activée) :

```
# Pour patcher une note existante :
mcp__obsidian__patch_note("<chemin>", contenu, insertAfter="<section>")

# Pour créer une nouvelle note :
mcp__obsidian__write_note("<chemin>", contenu)
```

Confirmer chaque écriture avec un résumé final :

```
✅ Captures enregistrées :
- Projets/mayday-search/decisions.md — mis à jour (section Décisions)
- Claude/memory-log.md — mis à jour (Sprint 12 ajouté)
```

---

## Règles générales

- **Toujours** montrer le preview avant d'écrire
- **Jamais** écraser du contenu sans confirmation
- Garder un style sobre et factuel dans les notes (pas de mise en forme excessive)
- Respecter les conventions de nommage et la structure du vault telle que définie dans `_STRUCTURE.md`
- En cas de doute sur le bon emplacement, proposer deux options à l'utilisateur
- Pour la recherche de contradictions, couvrir large : ne pas se limiter aux notes déjà identifiées
