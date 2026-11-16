# TP1 – Réduction de dimension (LSA)

Travail pratique du cours **Statistiques et data mining** (9.3.1.A), Master Humanités numériques, Centre d'Études Supérieures de la Renaissance (CESR), Université de Tours, 2026-2027.

Enseignant : Farida Zehraoui.

## Objectif

Prétraiter des données textuelles et réduire leur nombre de caractéristiques avec la SVD tronquée, c'est-à-dire réaliser une analyse sémantique latente (LSA).

## Données

Sous-ensemble du jeu de données **20 Newsgroups** (scikit-learn), limité à trois catégories :

- sci.electronics
- sci.med
- sci.space

soit 1778 messages.

## Étapes

1. Chargement et exploration des données
2. Transformation des textes en sac de mots (CountVectorizer)
3. Réduction de dimension avec TruncatedSVD (500 composantes)
4. Visualisation des données réduites en 1D, 2D et 3D
5. Seconde expérience : suppression des en-têtes, signatures et citations, puis pondération TF-IDF (TfidfTransformer)

## Principaux résultats

- Avec le simple comptage des mots, les 500 composantes conservent **93,1 %** de la variance, et **371 composantes** suffisent pour atteindre 90 %. Les sujets restent toutefois mélangés sur les graphiques.
- Après nettoyage et TF-IDF, la variance conservée tombe à **63,2 %**, mais les trois sujets se séparent beaucoup plus nettement.

## Structure du dépôt

```text
tp1_data-mining-reduction-dimension/
├── TP-1_Machine-Learning_v1.ipynb   # notebook du TP
├── figures/                      # figures générées
├── requirements.txt              # dépendances Python
└── README.md
```


## Installation

1. Cloner le dépôt :

```bash
git clone https://github.com/dokanoukok-debug/tp1_data-mining-reduction-dimension.git
cd tp1_data-mining-reduction-dimension
```

2. Créer et activer un environnement virtuel :

```bash
python3 -m venv venv
source venv/bin/activate        # Linux / macOS
# venv\Scripts\activate         # Windows
```

3. Installer les dépendances :

```bash
pip install -r requirements.txt
```

## Lancement

```bash
jupyter notebook
```

Ouvrir `TP-1_Machine-Learning_v1.ipynb` et exécuter les cellules dans l'ordre.


## Auteurs

Projet réalisé en binôme :

- **Kokou DOKANU**
- **Kossi ZANGBE**

Dépôt d'origine : [kossi-ctrl/tp1_data-mining](https://github.com/kossi-ctrl/tp1_data-mining)
