Modélisation du Risque de Crédit
Calcul de la PD, LGD, EAD et de la Perte Attendue (EL) avec le Machine Learning en Python

La modélisation du risque de crédit est un enjeu majeur pour les institutions financières.
Elle vise à évaluer la probabilité qu’un emprunteur ne soit pas en mesure de rembourser totalement ou partiellement un prêt (crédit à la consommation, prêt bancaire, carte de crédit, etc.).

En pratique :
  - Le défaut peut être partiel ou total
  - Le capital et les intérêts peuvent être affectés
  - Les volumes de données élevés nécessitent des méthodes statistiques et de machine learning

Ce projet s’inscrit dans une approche réglementaire et opérationnelle, en conformité avec les accords de Bâle II / Bâle III.

Présentation du projet

Ce projet a pour objectif de construire une chaîne complète de modélisation du risque de crédit à partir de données de prêts réels.

Les objectifs principaux sont :
  - Modéliser la Probabilité de Défaut (PD)
  - Estimer la Perte en cas de Défaut (LGD)
  - Prédire l’Exposition au Défaut (EAD)
  - Calculer la Perte Attendue (Expected Loss – EL)
  - Produire un score de crédit interprétable utilisable au quotidien
  - Vérifier la stabilité des modèles dans le temps

Pipeline de modélisation
Le pipeline suit les étapes suivantes :
1. Prétraitement des données
  - Nettoyage des données
  - Fine classing & coarse classing
  - Transformation en variables indicatrices (dummy variables)
2. Modélisation de la PD
  - Régression logistique
  - Sélection de variables
  - Génération d’un scorecard
3. Modélisation de la LGD
  - Étape 1 : Régression logistique (défaut vs recouvrement)
  - Étape 2 : Régression linéaire (taux de recouvrement)
4. Modélisation de l’EAD
  - Régression linéaire
5. Calcul de la Perte Attendue
  - EL = PD × LGD × EAD
6. Suivi et validation des modèles
  - Population Stability Index (PSI)
  - Validation sur données récentes

Documents clés
Le projet est structuré autour de quatre notebooks principaux :
  - L01 – Prétraitement des données et feature engineering
  - L02 – Modélisation de la Probabilité de Défaut (PD), scorecard et seuils de décision
  - L03 – Modélisation de la LGD, de l’EAD et calcul de la Perte Attendue
  - L04 – Analyse de la stabilité de la population (PSI)

Jeux de données
Les données proviennent de Lending Club, une plateforme américaine de prêts entre particuliers.
  - Source : Kaggle
  - Nombre d’observations : plus de 800 000 prêts
  - Période couverte : 2007 – 2015
Stratégie de découpage :
  - 2007 – 2014 : données utilisées pour l’entraînement des modèles
  - 2015 : données utilisées pour la validation et le contrôle de stabilité
Cette approche reproduit un contexte réel de mise en production des modèles de risque.

