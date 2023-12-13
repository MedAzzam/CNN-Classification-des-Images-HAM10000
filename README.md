# CNN : Classification d'Images HAM10000

Ce projet vise à construire un modèle de classification d'images HAM10000 en utilisant CNN. Les objectifs majeurs sont d'aborder les défis inhérents aux données et aux ressources disponibles.

## Problèmes de Données et Ressources

Les données présentent un fort biais en faveur d'une classe spécifique (les nevus mélanocytaires [nv]), représentant 67% des données. De plus, des contraintes telles qu'une taille limitée du jeu de données pour la classification d'images, la réduction de la résolution des images (de 600x400 à 160x120), et des limitations de ressources mémoire affectent l'architecture du modèle et ses performances ultérieures.

## Objectifs Principaux

1. Réduire ou éliminer le surajustement (overfitting).
2. Atteindre une précision de test d'au moins 80% sans compromettre le premier objectif.
3. Construire un modèle adapté aux ressources limitées tout en respectant l'objectif 2.

## Table des Matières

1. Chargement des Bibliothèques
2. Lecture et Traitement des Données
   - Examen du contenu du HAM1000
   - Lecture des métadonnées et encodage des labels
   - Fusion des dossiers d'images et création d'un dictionnaire de types de lésions
   - Ajout de nouvelles colonnes
   - Nettoyage des Données
3. Analyse Exploratoire des Données (EDA)
   - Comptage des types de cellules
   - Distribution d'âge
   - Distribution d'âge par sexe
   - Comptage des types de cellules par sexe
   - Types de lésions par âge et sexe
   - CountPlot: Comptage des types de cellules par âge
4. Redimensionnement des Images
   - Comparaison des caractéristiques de taille d'image
   - Redimensionnement des images pour l'entrée du modèle
   - Échantillon d'images de lésions cutanées
5. Prétraitement
   - Entraînement Test Validation
   - Conversion en tableau Numpy
   - Standardisation
   - Encodage one-hot : conversion de l'output to categorical crossentropy
   - Split : train / validation = 0,87 / 0,13
   - Reshape des images en 3 dimensions
6. Test du Modèle (modelT)
   - Test de l'architecture du modèle
   - Entraînement de modelT avec augmentation
   - Évaluation de la précision et de la perte de test de modelT
   - Tracés de l'Accuracy et de Loss Plots du test modèle après l'augmentation

Ce fichier README fournit une vue d'ensemble des étapes principales et des analyses effectuées dans ce projet de classification d'Images HAM10000. 

Pour plus de détails, veuillez consulter les sections spécifiques dans le code du projet.
