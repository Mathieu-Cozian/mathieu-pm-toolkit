# Brand Voice Rewrite

## Overview

Réécriture complète d'un contenu pour le mettre en conformité avec la brand voice Mayday. Affiche le résultat côte à côte (avant / après) avec la liste des modifications appliquées.

## Déclenchement

"Réécris ce texte en brand voice Mayday" / "Mets ce contenu en conformité avec notre brand voice" / "Corrige ce texte pour qu'il respecte la brand voice" / "Rewrite brand voice"

## Workflow

### Étape 1 — Lire les guidelines

Lire le fichier de référence :
`shared/brand-voice/mayday-brand-voice-guidelines.md`
(depuis la racine du repo)

### Étape 2 — Collecter le contenu et le contexte

Demander à l'utilisateur :
1. **Le contenu** à réécrire (texte collé ou chemin de fichier)
2. **Le contexte de publication** si non précisé : homepage / page produit / blog / LinkedIn / newsletter / pitch / autre

Le contexte détermine le niveau de ton (voir section "Ton par contexte" des guidelines).

### Étape 3 — Analyser avant de réécrire

Identifier silencieusement toutes les violations avant de commencer la réécriture :
- Mots interdits à supprimer
- Anglicismes à remplacer
- Formules ampoulées à reformuler
- Ton à ajuster (trop alarmiste, trop informel, trop hyperbole…)
- Majuscules et ponctuation à corriger

### Étape 4 — Réécrire

Règles de réécriture :
- **Conserver l'intention et le message original** — ne pas changer le sens
- **Conserver la structure** (paragraphes, listes, titres) sauf si elle nuit au ton
- **Ton adapté au contexte** déclaré
- **Interventions minimales** : ne modifier que ce qui est non conforme, ne pas reformuler si inutile
- **Emojis** : les conserver si le contexte le permet (LinkedIn, newsletter), les supprimer pour les contextes formels

## Format de sortie

```
## Réécriture Brand Voice — [Contexte de publication]

### Modifications appliquées
- [Modification 1] : "[avant]" → "[après]"
- [Modification 2] : "[avant]" → "[après]"
[etc.]

---

### Avant
[Texte original intégral]

---

### Après
[Texte réécrit intégral]
```

## Règles importantes

- Ne jamais changer le fond, seulement la forme
- Si une phrase est fondamentalement incompatible avec la brand voice (ex : claim non étayé, hyperbole structurelle), signaler à l'utilisateur plutôt que de la réécrire silencieusement
- Si le contenu est déjà conforme, le dire clairement et ne pas réécrire inutilement
- Proposer le fichier markdown en sortie si le contenu est long (>300 mots)
