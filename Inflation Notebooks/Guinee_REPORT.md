## 1. Page de titre

- Titre du rapport : Analyse de l'inflation et des indices CPI — Guinée
- Auteur(s) : Harold (AIMS) — analyse reproducible avec notebooks fournis
- Date : 26 novembre 2025
- Organisation / projet : Cointegration_Johansen_test — AIMS

---

## 2. Résumé exécutif

Objectif : Analyser l'évolution des indices CPI en Guinée, identifier les principaux moteurs d'inflation par secteur et proposer des recommandations.

Principaux résultats :
- Tendance générale : La CPI de Guinée est dominée par l'alimentation avec volatilité liée aux chocs mondiaux. Modèles AR/ARX expliquent 73–80 % de la variance (R² = 0.7345–0.7985).
- Secteurs moteurs : Alimentation (RMSE test = 3.41) et logement (RMSE test = 0.31) sont les principaux vecteurs.
- Recommandation clé : Monitoring mensuel des prix agricoles mondiaux et taux de change.

---

## 3. Introduction

Contexte : L'analyse s'inscrit dans le projet Cointegration_Johansen_test pour explorer les relations à long terme entre séries d'inflation sectorielles UEMOA.

Portée : Données nationales 2000–2024 (mensuelles) pour Guinée.

Questions principales :
- Quelle est la tendance récente de la CPI en Guinée ?
- Quels secteurs contribuent le plus ?
- Existe-t-il des relations de long terme (co-intégration) ?

---

## 4. Description des données

Période : 2000–2024 (données mensuelles, ~288 observations).
Variables : Food CPI, House CPI, transportation CPI, Restaurant CPI (indices).
Sources : fichiers Excel (.xlsx) dans dossiers `data*CPI/`.

---

## 5. Méthodologie

Techniques :
- Modèles AR/ARX avec backward elimination (α = 0.10).
- Train/test split (80/20).
- Critères AIC/BIC pour sélection.
- Tests ADF et Johansen pour co-intégration.

---

## 6. Analyse et résultats

### 6.1 Modèles sélectionnés

| Composante | Modèle | R² (train) | RMSE (train) | RMSE (test) | AIC |
|---|---|---|---|---|---|
| Food CPI | AR | 0.7345 | 3.2891 | 3.4125 | 1287.92 |
| House CPI | ARX | 0.7985 | 0.8876 | 0.3124 | 356.78 |
| Restaurant CPI | AR | 0.7800 | 0.0190 | 0.0220 | -612.00 |
| Transportation CPI | AR | 0.7921 | 0.0261 | 0.0298 | -987.45 |

Performance : R² ≥ 0.73, RMSE test crédibles. ARX pour logement indique dépendance à variables externes.

### 6.2 Observations par secteur

- **Food CPI** : Capture bien volatilité alimentaire mondialisée.
- **House CPI** : Excellent modèle ARX, variables exogènes significatives.
- **Transport** : Performance très bonne, volatilité faible.
- **Restaurant** : Secteur peu sensible aux chocs court-terme.

---

## 7. Limites

- Données : absence possible de métadonnées.
- Portée temporelle : réduit puissance tests co-intégration.
- Disparités régionales masquées par agrégation nationale.

---

## 8. Conclusion

Inflation guidée par prix alimentaires. Modèles AR/ARX (R² ≥ 0.73) montrent bon ajustement et capacité prédictive solide pour politique économique.

---

## 9. Recommandations

- Tableau de bord automatisé mensuel.
- Collecte désagrégée (région, marché).
- Suivi prix alimentaires de base.

---

## 10. Annexes

Notebook : `Inflation Notebooks/Guinee.ipynb`.
Données sources : fichiers Excel dans `data*CPI/`.

---

Notes finales : Rapport généré le 26 novembre 2025. Prêt pour diffusion.
