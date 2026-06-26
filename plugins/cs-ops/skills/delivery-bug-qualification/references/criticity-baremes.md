# Barème Criticity Score — référence

`Criticity Score = Scoring Impact + Scoring Tiering + Scoring additionnel`

## 1. Impact fonctionnel
| Impact | Critère | Score |
|---|---|---|
| Bloquant | Connexion / recherche / consultation KO | Hors scoring → process d'incident, alerte immédiate |
| Critique | Fonctionnalité cœur impactée, contournement difficile | 4 |
| Majeur | Fonctionnalité cœur impactée, contournement possible | 2 |
| Mineur | Impact limité, contournement facile | 1 |

## 2. Tiering client
| Tiering | Score |
|---|---|
| Platinum | 5 |
| Golden | 4 |
| Silver | 2 |
| Bronze | 1 |

## 3. Scoring additionnel (contexte commercial)
- Renewal ou insatisfaction générale : **+2**
- L&E / Upsell : **+1**

## Règles
- **Plafond mineur :** un bug mineur ne dépasse jamais **4**, quel que soit le tiering.
- **Bloquant :** ne passe pas par le scoring → process d'incident.

## Niveaux de criticité (auto via automation Notion)
| Score | Niveau |
|---|---|
| 9–11 | Très élevée / Highest |
| 6–8 | Élevée / High |
| 4–5 | Moyenne / Medium |
| <4 | Faible / Low |

> Cas Renewal : pour un score 4–6 en contexte Renewal, possibilité d'alerter Produit/Tech sur Slack.
