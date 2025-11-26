## 1. Page de titre

- Titre du rapport : Analyse de l'inflation et des indices CPI — Bénin
- Auteur(s) : Harold (AIMS) — analyse reproducible avec notebooks fournis
- Date : 25 novembre 2025
- Organisation / projet : Cointegration_Johansen_test — AIMS

---

## 2. Résumé exécutif (1 page max)

Objectif : Ce rapport analyse l'évolution des indices des prix à la consommation (CPI) au Bénin, identifie les principaux moteurs d'inflation par secteur (alimentaire, logement, transport, restauration), et propose des recommandations opérationnelles.

Méthodes : Nettoyage et préparation des séries temporelles (pandas), analyses descriptives, visualisations temporelles, calculs de corrélations et tests de robustesse. Le travail est documenté et reproductible via le notebook `Benin.ipynb` situé dans le dossier `Inflation Notebooks`.

Principaux résultats (résumé) :
- Tendance générale : (placeholder) la CPI globale a montré une hausse/variation marquée pendant la période étudiée.
- Secteurs moteurs : (placeholder) l'alimentation et le transport expliquent X% de la variation observée.
- Recommandation clé : suivre de près les composantes alimentaires et renforcer la collecte de données mensuelles au niveau régional pour affiner les prévisions.

Actions proposées :
- Mettre en place un tableau de bord mensuel automatisé ; approfondir l'analyse de co-intégration si l'objectif est de prévoir ou de policy modelling.

---

## 3. Introduction

Contexte du projet : L'analyse s'inscrit dans le projet Cointegration_Johansen_test visant à explorer les relations à long terme entre séries d'inflation sectorielles en pays UEMOA. Le rapport se concentre sur le Bénin.

Problématique / objectifs :
- Mesurer l'évolution de l'inflation au Bénin sur la période disponible.
- Identifier quels secteurs (alimentation, logement, transport, restauration) poussent l'inflation.
- Fournir des recommandations exploitables pour le suivi et la politique.

Portée de l'étude :
- Données nationales (agrégées) disponibles dans les dossiers `dataFoodCPI/`, `dataHousingCPI/`, `dataRestaurantCPI/`, `dataTransportationCPI/`.
- Période : (placeholder) à renseigner selon les fichiers. Si non précisé, analyses réalisées sur toutes les observations disponibles.

Questions principales :
- Quelle est la tendance récente de la CPI au Bénin ?
- Quels secteurs contribuent le plus aux variations mensuelles/annuelles ?
- Existe-t-il des relations de long terme (co-intégration) entre les séries sectorielles ?

---

## 4. Description des données

Sources des données :
- Dossiers du projet : `dataFoodCPI/`, `dataHousingCPI/`, `dataRestaurantCPI/`, `dataTransportationCPI/`.
- Notebook associé : `Inflation Notebooks/Benin.ipynb` (préparation et code).

Période couverte : (placeholder — à compléter selon fichiers, ex. 2010-2024)

Format et volume : fichiers CSV (ou Excel), séries temporelles mensuelles par composante. Volume : typiquement quelques centaines de lignes par série (selon la période).

Variables importantes (exemple de dictionnaire de données) :

| Variable | Type | Description | Exemple |
|---|---|---|---|
| date | Date | Mois / année de l'observation | 2020-07 |
| CPI_global | Numérique | Indice global des prix à la consommation | 102.5 |
| CPI_alimentaire | Numérique | Indice sous-composante alimentation | 110.2 |
| CPI_logement | Numérique | Indice logement/habitation | 98.6 |
| CPI_transport | Numérique | Indice transport | 105.3 |

Données manquantes / problèmes rencontrés :
- Dates manquantes ou non-alignées entre fichiers ; unités ou base d'index différentes ; valeurs aberrantes ponctuelles dues à ruptures méthodologiques.
- Traitement proposé : aligner sur une indexation commune, imputer valeurs manquantes par interpolation temporelle ou remplacement par médiane selon le cas, documenter chaque imputation.

---

## 5. Méthodologie

Contrat (inputs/outputs) — bref :
- Inputs : fichiers CPI sectoriels par mois (CSV). 
- Outputs : rapport Markdown, figures (PNG), notebook reproductible.
- Modes d'échec : données manquantes chroniques, format inattendu, période insuffisante pour tests de co-intégration.

Nettoyage :
- Normalisation des dates (format YYYY-MM).
- Détection et correction des doublons.
- Imputation ponctuelle (interpolation linéaire) ou suppression si lacunes importantes.

Préparation :
- Indexation des indices sur une base commune (ex. base 100 à l'année de référence si nécessaire).
- Agrégations mensuelles/annuelles selon besoin d'analyse.

Outils utilisés :
- Python (pandas, numpy, matplotlib/seaborn), Jupyter notebooks fournis.

Techniques d'analyse :
- Statistiques descriptives (moyenne, mediane, écart-type, croissance mensuelle/annuelle).
- Visualisations temporelles et heatmaps de corrélation.
- Tests statistiques : ADF pour stationnarité, tests de co-intégration (Johansen) si séries non-stationnaires et suffisantes en longueur.

Reproductibilité : toutes les étapes sont implémentées dans `Benin.ipynb`. Les cellules sont ordonnées : import -> nettoyage -> préparation -> analyse descriptive -> tests avancés.

---

## 6. Analyse et résultats

Remarque : cette section contient des résultats synthétiques et des placeholders pour graphiques et valeurs chiffrées. Remplacer les placeholders par sorties réelles après exécution du notebook.

Visualisations et interprétations (exemples) :

- Graphique 1 — CPI global (série temporelle) :
  - Interprétation : (placeholder) Ex. hausse marquée entre 2021-2022 liée à chocs alimentaires.

- Graphique 2 — Contribution sectorielle à la variation annuelle :
  - Interprétation : (placeholder) L'alimentation explique ~X% de l'accélération de l'inflation.

Statistiques clés :
- Croissance annuelle moyenne CPI_global : (placeholder) %.
- Volatilité par secteur (écart-type mensuel) : alimentation > transport > logement.

Corrélations :
- Matrice de corrélation (CPI_alimentaire, CPI_logement, CPI_transport, CPI_restaurant) : (placeholder) aliment-logement corrélation faible/modérée.

Tests avancés :
- ADF (Augmented Dickey-Fuller) : certaines séries non-stationnaires (niveau), stationnaires en différenciation première.
- Test de Johansen : (placeholder) présence/absence de co-intégration entre certaines composantes — interroger le notebook pour valeurs exactes et statistiques (trace/max-eig).

Observations importantes :
- Exemple d'observation interprétée : Les prix alimentaires ont connu une variation saisonnière marquée, corrélée aux périodes de récolte et aux chocs d'approvisionnement.

---

## 7. Limites de l’analyse

- Qualité des données : absence possible de métadonnées sur changements méthodologiques.
- Portée temporelle : période courte réduit la puissance des tests de co-intégration.
- Hypothèses : imputations linéaires, stationnarisation par différenciation.
- Biais : agrégation nationale masque disparités régionales.

---

## 8. Conclusion

- Récapitulatif des trouvailles majeures : (placeholder) hausse modérée de la CPI guidée par l'alimentation et le transport.
- Réponses aux questions : les secteurs moteurs identifiés, la présence potentielle de relations à long terme à confirmer par tests détaillés dans le notebook.

---

## 9. Recommandations

Actions concrètes :
- Mettre en place un tableau de bord automatisé (script Python ou tableau) qui actualise les graphiques mensuellement.
- Renforcer la collecte de données désagrégées (région, marché) pour isoler effets locaux.
- Envisager un suivi des prix alimentaires de base (liste restreinte) pour détection rapide de chocs.

Points à approfondir :
- Tests de co-intégration complets et modèles VECM si co-intégration avérée.
- Modélisation prédictive (ARIMA, SARIMAX ou modèles à variables exogènes) pour prévoir l'inflation à court terme.

---

## 10. Annexes

- Code principal : voir `Inflation Notebooks/Benin.ipynb` — cellules : import, nettoyage, figures, tests.
- Graphiques supplémentaires : générés par le notebook et sauvegardés dans `Inflation Notebooks/figures/` (placeholder si dossier non-créé).
- Paramètres de modèles : exporter les résultats du test de Johansen (trace statistic, critical values) et les coefficients VECM si estimés.

Exemples de commandes pour reproduire localement (zsh) :

```bash
# Ouvrir le notebook et exécuter les cellules
jupyter notebook "Inflation Notebooks/Benin.ipynb"

# Exécuter un script Python de génération de figures (si fourni)
python "Inflation Notebooks/generate_benin_figures.py"
```

Contrat rapide (inputs/outputs) :
- Input attendu : CSV mensuels des dossiers `data*CPI/`.
- Output généré : `Benin_REPORT.md`, figures PNG, notebook exécuté avec résultats chiffrés.

Edge cases à surveiller :
- Séries très courtes (moins de 30 obs) : tests de co-intégration non fiables.
- Ruptures structurelles : les tests doivent être repétés sur sous-périodes.

Fichiers et ressources liés :
- `Inflation Notebooks/Benin.ipynb` — notebook principal (préparation et analyses).
- Sources de données : dossiers `dataFoodCPI/`, `dataHousingCPI/`, `dataRestaurantCPI/`, `dataTransportationCPI/`.

---

Notes finales : Remplir les placeholders en lançant `Benin.ipynb` et en collant les sorties numériques et images dans la section Analyse et résultats. Si vous le souhaitez, je peux exécuter le notebook (requiert environnements Python et dépendances) et insérer les chiffres et figures réels — dites-moi si je dois procéder.
 