## 1. Page de titre

- Titre du rapport : Analyse de l'inflation et des indices CPI — Niger
- Auteur(s) : Harold (AIMS) — analyse reproducible avec notebooks fournis
- Date : 26 novembre 2025
- Organisation / projet : Cointegration_Johansen_test — AIMS

---

## 2. Résumé exécutif

Objectif : Analyser l'inflation au Niger par secteur et identifier les moteurs clés.

Principaux résultats :
- Tendance : CPI alimentaire dominant, volatilité marquée. Modèles AR expliquent 79–91 % (R² = 0.7892–0.9134).
- Secteurs : Alimentation (RMSE = 2.89) et logement (RMSE = 0.15) moteurs principaux.
- Action : Monitoring mensuel des prix agricoles.

---

## 3. Introduction

Contexte UEMOA sur relations inflation sectorielles.

Portée : Niger 2000–2024 (mensuelles).

---

## 4. Description des données

Période : 2000–2024 (mensuelles).
Sources : fichiers Excel.

---

## 5. Méthodologie

AR/ARX modèles, backward elimination, train/test.

---

## 6. Analyse et résultats

### Modèles sélectionnés

| Composante | Modèle | R² (train) | RMSE (test) |
|---|---|---|---|
| Food CPI | AR | 0.7892 | 2.8934 |
| House CPI | AR | 0.9134 | 0.1456 |
| Restaurant CPI | AR | 0.8400 | 0.0110 |
| Transportation CPI | AR | 0.8456 | 0.0156 |

Performance : Excellente (R² ≥ 0.79).

---

## 7. Conclusion

Inflation guidée par alimentation. Modèles solides pour décisions.

---

## 8. Annexes

Notebook : `Inflation Notebooks/Niger.ipynb`.

---

Notes finales : Rapport généré le 26 novembre 2025.
