# Brand Voice Check

## Overview

Audit du contenu par rapport aux guidelines de la marque Mayday. Détecte les violations, les mots interdits, les anglicismes non autorisés, et les écarts de ton. Produit un rapport structuré avec un score et des corrections concrètes.

## Déclenchement

"Vérifie si ce texte respecte la brand voice" / "Audite ce contenu Mayday" / "Est-ce que ce texte est conforme à notre brand voice ?" / "Check brand voice"

## Workflow

### Étape 1 — Lire les guidelines

Lire le fichier de référence :
`shared/brand-voice/mayday-brand-voice-guidelines.md`
(depuis la racine du repo)

### Étape 2 — Collecter le contenu à auditer

Si l'utilisateur n'a pas fourni de contenu, demander :
- Texte à coller directement, ou
- Chemin vers un fichier à lire

### Étape 3 — Analyser le contenu

Vérifier systématiquement :

1. **Ton général** — Chaleureux mais pas informel ? Audacieux sans hyperbole ?
2. **Mots interdits** — Présence de : incroyable, enchanter, révolutionnaire, inoubliable, cool, super, OK, des tonnes, cheesy, chill, "nous avons le plaisir de", "nous avons l'honneur de", "je me permets de"
3. **Vocabulaire** — Utilisation des termes préférés (ex : "conseiller" vs "agent", "fonctionnalité" vs "feature")
4. **Anglicismes** — Anglicismes non autorisés par la politique (hors exceptions : knowledge management, Knowledge Empowerment, No KM No AI, pure player, snackable)
5. **Majuscules** — Respect des règles FR (pas de majuscule après deux-points, pas de majuscule pour les métiers/mois)
6. **Ponctuation** — Points d'exclamation excessifs ? Tirets/parenthèses en incise (préférer la virgule) ?
7. **Ton par contexte** — Le ton correspond-il au contexte déclaré (homepage, blog, LinkedIn, newsletter…) ?
8. **Formules ampoulées** — Présence de tournures à éviter ("Vous êtes-vous déjà demandé pourquoi…")

### Étape 4 — Produire le rapport

## Format de sortie

```
## Audit Brand Voice — [Titre ou extrait du contenu]

### Résumé
[2-3 phrases de synthèse : globalement conforme / partiellement conforme / non conforme, et pourquoi]

### Score : X/5
[Justification du score]

### Violations détectées

#### [Règle concernée]
- **Passage** : "[citation exacte du texte problématique]"
- **Problème** : [explication courte]
- **Correction suggérée** : "[version corrigée]"

[Répéter pour chaque violation]

### Points positifs
- [Ce qui est bien fait et conforme]

### Recommandations prioritaires
1. [Action concrète à faire en premier]
2. [Action concrète à faire ensuite]
```

Si aucune violation n'est détectée : le dire clairement, donner un score 5/5, et pointer les éléments particulièrement réussis.

## Règles d'audit

- Citer toujours le texte original exact entre guillemets
- Ne pas réécrire le texte en entier dans ce skill (utiliser `brand-voice-rewrite` pour ça)
- Proposer une correction pour chaque violation
- Être précis et actionnable, pas général
