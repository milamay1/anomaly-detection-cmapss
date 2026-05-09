# Détection d'anomalies dans des systèmes industriels

**Université de Béjaïa — Département Sciences Exactes — M1 IA — 2025/2026**  
 May Thamila ** Mezemate Leïla 

---

## Description

Ce projet implémente et compare cinq architectures de Deep Learning pour la **détection automatique d'anomalies dans des moteurs turbofan industriels**, à partir du dataset de référence **NASA C-MAPSS FD001**.

Le problème est formulé en **classification binaire** : un moteur est considéré en zone critique lorsque sa durée de vie résiduelle (RUL) est inférieure ou égale à 30 cycles, annonçant une panne imminente.

---

## Dataset

**NASA C-MAPSS FD001** — non inclus dans ce dépôt.  
À télécharger sur Kaggle :  
https://www.kaggle.com/datasets/behrad3d/nasa-cmaps

Placer les fichiers `train_FD001.csv`, `test_FD001.csv`, `RUL_FD001.csv` dans `/content/` avant d'exécuter.

---

## Pipeline

| Cellule | Description |
|---------|-------------|
| Cellule 1 | Importation des librairies et chargement du dataset |
| Cellule 2 | Analyse exploratoire (EDA) |
| Cellule 3 | Prétraitement : calcul RUL, étiquetage, normalisation MinMax |
| Cellule 4 | Construction des séquences temporelles (fenêtres glissantes) |
| Cellule 5 | Entraînement des 5 modèles Deep Learning |
| Cellule 6 | Comparaison et visualisation des résultats |
| Cellule 7 | Interface interactive de diagnostic |

---

## Modèles implémentés

- **LSTM** — mémoire sélective à long terme
- **CNN 1D** — détection de patterns locaux
- **TCN** — convolutions causales dilatées avec connexions résiduelles
- **Transformer Encoder** — mécanisme d'auto-attention multi-tête
- **GRU + Attention** — GRU bicouche avec pondération temporelle

---

## Métriques d'évaluation

- **AUC-ROC** — capacité de discrimination entre classes
- **F1-Score** — métrique principale (données déséquilibrées)
- **Accuracy** — proportion de prédictions correctes

---

## Interface de diagnostic

Deux modes disponibles :
- 🟢 **Mode Simple** — curseurs intuitifs pour opérateurs non spécialistes
- 🔵 **Mode Expert** — valeurs réelles des capteurs normalisées [0–1]

---

## Lancer le projet

Ouvrir `anomaly_detection.ipynb` dans Google Colab et exécuter les cellules dans l'ordre.
