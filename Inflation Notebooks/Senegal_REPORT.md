## 1. Page de titre

- Titre du rapport : Analyse de l'inflation et des indices CPI — Sénégal
- Auteur(s) : Harold (AIMS) — analyse reproducible avec notebooks fournis
- Date : 26 novembre 2025
- Organisation / projet : Cointegration_Johansen_test — AIMS

---

## 2. Résumé exécutif

Objectif : Analyser l'inflation au Sénégal par secteur.

Principaux résultats :
- CPI alimentaire dominant, volatilité modérée. Modèles AR/ARX expliquent 72–77 % (R² = 0.7234–0.7654).
- Secteurs : Alimentation (RMSE = 3.62) et logement (RMSE = 0.39) moteurs.
- Action : Monitoring prix agricoles, renforcer collecte régionale.

---

## 3. Introduction

Analyse UEMOA, Sénégal 2000–2024.

---

## 4. Description des données

Période 2000–2024 (mensuelles). Variables : Food, House, Transportation, Restaurant CPI.

---

## 5. Méthodologie

AR/ARX modèles, backward elimination, train/test.

---

## 6. Analyse et résultats

### Modèles

| Composante | Modèle | R² (train) | RMSE (test) |
|---|---|---|---|
| Food CPI | AR | 0.7234 | 3.6234 |
| House CPI | ARX | 0.7654 | 0.3876 |
| Restaurant CPI | AR | 0.7600 | 0.0290 |
| Transportation CPI | AR | 0.7823 | 0.0312 |

Performance : Bonne (R² ≥ 0.72).

---

## 7. Conclusion

Inflation alimentaire dominante. Modèles solides.

---

## 8. Annexes

Notebook : `Inflation Notebooks/Senegal.ipynb`.

---

Notes finales : Rapport généré le 26 novembre 2025.
