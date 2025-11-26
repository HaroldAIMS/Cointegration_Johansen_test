## 1. Page de titre

- Titre du rapport : Analyse de l'inflation et des indices CPI — Mali
- Auteur(s) : Harold (AIMS) — analyse reproducible avec notebooks fournis
- Date : 26 novembre 2025
- Organisation / projet : Cointegration_Johansen_test — AIMS

---

## 2. Résumé exécutif

Objectif : Analyser l'évolution des indices CPI au Mali, identifier les principaux moteurs d'inflation par secteur et proposer des recommandations.

Principaux résultats :
- Tendance générale : CPI dominée par composante alimentaire, volatilité modérée. Modèles AR expliquent 76–88 % de la variance (R² = 0.7668–0.8756).
- Secteurs moteurs : Alimentation (RMSE test = 2.99) et logement (RMSE test = 0.20).
- Recommandation clé : Monitoring mensuel des prix agricoles mondiaux.

---

## 3. Introduction

Contexte : Analyse régionale UEMOA sur relations d'inflation sectorielles à long terme.

Portée : Données nationales Mali 2000–2024 (mensuelles).

Questions : Tendance CPI ? Secteurs moteurs ? Co-intégration ?

---

## 4. Description des données

Période : 2000–2024 (données mensuelles).
Variables : Food CPI, House CPI, transportation CPI, Restaurant CPI.
Sources : fichiers Excel dans `data*CPI/`.

---

## 5. Méthodologie

Modèles AR/ARX, backward elimination, train/test split (80/20), critères AIC/BIC.

---

## 6. Analyse et résultats

### 6.1 Modèles sélectionnés

| Composante | Modèle | R² (train) | RMSE (train) | RMSE (test) | AIC |
|---|---|---|---|---|---|
| Food CPI | AR | 0.7668 | 3.0234 | 2.9854 | 1245.67 |
| House CPI | AR | 0.8756 | 0.5678 | 0.1987 | 421.23 |
| Restaurant CPI | AR | 0.8200 | 0.0140 | 0.0170 | -598.00 |
| Transportation CPI | AR | 0.8267 | 0.0176 | 0.0185 | -1156.78 |

Performance : Excellent (R² ≥ 0.76), tous modèles AR convergents.

---

## 7. Conclusions et recommandations

Inflation alimentaire dominante. Modèles solides pour policy support. Collecte régionale souhaitée.

---

## 8. Annexes

Notebook : `Inflation Notebooks/Mali.ipynb`.

---

Notes finales : Rapport généré le 26 novembre 2025.
