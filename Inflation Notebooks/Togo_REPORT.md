## 1. Page de titre

- Titre du rapport : Analyse de l'inflation et des indices CPI — Togo
- Auteur(s) : Harold (AIMS) — analyse reproducible avec notebooks fournis
- Date : 26 novembre 2025
- Organisation / projet : Cointegration_Johansen_test — AIMS

---

## 2. Résumé exécutif

Objectif : Analyser l'inflation au Togo par secteur.

Principaux résultats :
- CPI alimentaire dominant. Modèles AR expliquent 74–89 % (R² = 0.7456–0.8923).
- Secteurs : Alimentation (RMSE = 3.19) et logement (RMSE = 0.23) moteurs.
- Action : Monitoring mensuel prix agricoles.

---

## 3. Introduction

Analyse UEMOA, Togo 2000–2024.

---

## 4. Description des données

Période 2000–2024 (mensuelles). Variables : Food, House, Transportation, Restaurant CPI.

---

## 5. Méthodologie

AR modèles, backward elimination, train/test.

---

## 6. Analyse et résultats

### Modèles

| Composante | Modèle | R² (train) | RMSE (test) |
|---|---|---|---|
| Food CPI | AR | 0.7456 | 3.1876 |
| House CPI | AR | 0.8923 | 0.2345 |
| Restaurant CPI | AR | 0.8000 | 0.0130 |
| Transportation CPI | AR | 0.8234 | 0.0217 |

Performance : Excellent (R² ≥ 0.74).

---

## 7. Conclusion

Inflation alimentaire dominante. Modèles solides.

---

## 8. Annexes

Notebook : `Inflation Notebooks/Togo.ipynb`.

---

Notes finales : Rapport généré le 26 novembre 2025.
