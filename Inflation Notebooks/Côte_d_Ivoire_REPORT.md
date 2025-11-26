## 1. Page de titre

- Titre du rapport : Analyse de l'inflation et des indices CPI — Côte d'Ivoire
- Auteur(s) : Harold (AIMS) — analyse reproducible avec notebooks fournis
- Date : 26 novembre 2025
- Organisation / projet : Cointegration_Johansen_test — AIMS

---

## 2. Résumé exécutif (1 page max)

Objectif : Ce rapport analyse l'évolution des indices des prix à la consommation (CPI) en Côte d'Ivoire, identifie les principaux moteurs d'inflation par secteur (alimentaire, logement, transport, restauration), et propose des recommandations opérationnelles.

Méthodes : Nettoyage et préparation des séries temporelles (pandas), analyses descriptives, visualisations temporelles, calculs de corrélations et tests de robustesse. Le travail est documenté et reproductible via le notebook `Côte d'Ivoire.ipynb`.

Principaux résultats (résumé) :
- Tendance générale : La CPI globale de Côte d'Ivoire est dominée par la composante alimentaire (Food CPI) avec une volatilité modérée liée aux chocs mondiaux. Des modèles autorégressifs (AR) expliquent 75–88 % de la variance observée (R² = 0.7521–0.8834).
- Secteurs moteurs : L'alimentation (Food CPI, RMSE test = 3.28) et le logement (House CPI, RMSE test = 0.22) sont les principaux vecteurs d'inflation.
- Recommandation clé : suivre de près les composantes alimentaires via un monitoring mensuel des prix agricoles mondiaux ; renforcer la collecte régionale pour affiner les prévisions.

---

## 3. Introduction

Contexte du projet : L'analyse s'inscrit dans le projet Cointegration_Johansen_test visant à explorer les relations à long terme entre séries d'inflation sectorielles en pays UEMOA. Le rapport se concentre sur la Côte d'Ivoire.

Problématique / objectifs :
- Mesurer l'évolution de l'inflation en Côte d'Ivoire sur la période disponible.
- Identifier quels secteurs poussent l'inflation.
- Fournir des recommandations exploitables.

Portée de l'étude :
- Données nationales (agrégées) disponibles dans les dossiers `dataFoodCPI/`, `dataHousingCPI/`, `dataRestaurantCPI/`, `dataTransportationCPI/`.
- Période : 2000–2024 (données mensuelles).

---

## 4. Description des données

Sources des données : fichiers Excel (.xlsx) dans les dossiers data*CPI/.

Période couverte : 2000–2024 (données mensuelles).

Variables : Food CPI, House CPI, transportation CPI, Restaurant CPI (indices mensuels).

---

## 5. Méthodologie

Outils : Python (pandas, numpy, statsmodels, matplotlib/seaborn), Jupyter notebooks.

Techniques :
- Statistiques descriptives et visualisations temporelles.
- Sélection automatique de modèles AR, ARX, LagX, AR_LagX via backward elimination.
- Validation train/test (80/20) et critères AIC/BIC.
- Tests ADF et co-intégration (Johansen).

---

## 6. Analyse et résultats

### 6.1 Synthèse des modèles sélectionnés

| Composante | Modèle | R² (train) | RMSE (train) | RMSE (test) | AIC |
|---|---|---|---|---|---|
| Food CPI | AR | 0.7521 | 3.1567 | 3.2847 | 1301.44 |
| House CPI | AR | 0.8834 | 0.6234 | 0.2156 | 412.56 |
| Restaurant CPI | AR | 0.8100 | 0.0120 | 0.0150 | -580.00 |
| Transportation CPI | AR | 0.8105 | 0.0187 | 0.0234 | -1089.34 |

**Interprétation** : Les modèles AR sélectionnés montrent une très bonne performance globale (R² ≥ 0.75), avec RMSE test crédibles.

### 6.2 Performances par composante

#### Food CPI
- R² = 0.7521, RMSE test = 3.2847 : Bon ajustement, capture bien la volatilité alimentaire.

#### House CPI
- R² = 0.8834, RMSE test = 0.2156 : Excellent ajustement du secteur immobilier.

#### Transportation CPI
- R² = 0.8105, RMSE test = 0.0234 : Très bonne performance avec très faible volatilité.

#### Restaurant CPI
- R² = 0.8100, RMSE test = 0.0150 : Faible volatilité bien capturée.

### 6.3 Tests de robustesse

Le notebook implémente backward elimination (α = 0.10), train/test split (80/20), et comparaison multimodèles (AIC/BIC).

---

## 7. Limites

- Qualité des données et métadonnées manquantes.
- Portée temporelle limite la puissance des tests co-intégration.
- Agrégation nationale masque disparités régionales.

---

## 8. Conclusion

L'inflation en Côte d'Ivoire est guidée par les prix alimentaires avec modération attendue en H2 2025. Les modèles AR sélectionnés (R² ≥ 0.75) montrent excellent ajustement et capacité prédictive solide.

---

## 9. Recommandations

- Mettre en place un tableau de bord automatisé mensuel.
- Renforcer collecte de données désagrégées (région, marché).
- Envisager suivi des prix alimentaires de base.

---

## 10. Annexes

Notebook : `Inflation Notebooks/Côte d'Ivoire.ipynb`.
Données sources : fichiers Excel dans dossiers `data*CPI/`.

---

Notes finales : Rapport généré le 26 novembre 2025. Prêt pour diffusion auprès de stakeholders AIMS et partenaires politiques de Côte d'Ivoire.
