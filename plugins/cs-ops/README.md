# CS Ops

Outils d'opérations Customer Success pour Mayday — qualification de bugs, et autres workflows CS à venir.

## Skills

### `delivery-bug-qualification` — Loom → Card Notion

Transforme le transcript d'un Loom de qualification de bug en une card Notion standardisée dans la `DB | Product & Tech Backlog`.

**Déclencheurs :** "qualifie ce bug", "crée la card bug", "formate ce bug depuis le Loom", "transforme ce transcript en ticket", "remplis la fiche bug"

#### Problème résolu

Qualifier un bug correctement demande de remplir manuellement une dizaine de champs structurés. C'est long, et le résultat est inégal : environ 50 % des bugs n'ont pas de score de criticité, ce qui casse la priorisation côté Produit/Tech et génère des allers-retours Success ↔ Tech.

#### Principe

La CS qualifie le bug **à l'oral dans un Loom** (flux montré à l'écran, console ouverte), puis colle le transcript dans Claude. Le skill structure le contenu, pose les questions manquantes, calcule le Criticity Score avec la CS, et écrit la card après validation.

> La CS décrit — le skill structure — la CS valide — le skill écrit dans Notion.

#### Workflow

1. **Extraction** du transcript : produit, client, utilisateur, entité, attendu vs constaté, étapes de repro, tests déjà faits.
2. **Questions de complétude** : le skill relance la CS pour tout champ manquant. Si la CS ne l'a pas → `[TO FILL]`.
3. **Tagging** `Feature Concerned` via `delivery-bug-tagger` (1 tag parmi 41 valeurs exactes de la DB).
4. **Criticity Score** : le skill demande les 3 éléments à la CS (impact fonctionnel, tiering client, contexte commercial) et calcule le total avec elle. La property `Criticity` (Low/Medium/High/Highest) se remplit ensuite automatiquement via une automation Notion.
5. **Récap + validation** : le skill produit un fichier `recap-qualif-bug.md` et attend un accord explicite avant d'écrire.
6. **Mise à jour Notion** : la card existe déjà dans la DB — le skill la met à jour (properties + corps). Il ne la crée pas.

#### Criticity Score — barème

`Score = Impact fonctionnel + Tiering client + Contexte commercial`

| Impact | Score | Tiering | Score | Contexte | Bonus |
|---|---|---|---|---|---|
| Critique | 4 | Platinum | 5 | Renewal / insatisfaction | +2 |
| Majeur | 2 | Golden | 4 | L&E / Upsell | +1 |
| Mineur | 1 | Silver | 2 | — | 0 |
| **Bloquant** | **→ incident** | Bronze | 1 | | |

Règles : plafond **4** pour les bugs mineurs · Bug bloquant → process d'incident, ne pas scorer.

| Score | Criticité |
|---|---|
| 9–11 | Très élevée |
| 6–8 | Élevée |
| 4–5 | Moyenne |
| < 4 | Faible |

#### Architecture du skill

```
delivery-bug-qualification/
├── SKILL.md                        # logique : extraction, workflow, garde-fous
├── bug-card-template.md            # template de card (modifiable indépendamment)
└── references/
    ├── criticity-baremes.md        # barème de scoring détaillé
    └── delivery-bug-tagger.md      # classifieur Feature Concerned (41 tags)
```

#### Garde-fous

- Jamais d'écriture dans Notion sans validation explicite de la CS
- Jamais d'identifiant inventé (`userId`, `companyId`, ID entité) — `[TO FILL]` si absent
- Screenshots : dépôt manuel par la CS (le connecteur Notion n'uploade pas d'image brute)
- Ne touche pas à `Status`, `Card Type`, `Tech Owner`, `CSM` — déjà positionnés à l'arrivée

#### Périmètre V1 (hors scope)

- Transcription automatique du Loom (la CS fournit le transcript)
- Upload de screenshots
- Calcul automatique du Criticity Score (saisi via questions)
- Détection de doublons
- Auto-remplissage `Customer` / `Company ID` depuis la DB clients
