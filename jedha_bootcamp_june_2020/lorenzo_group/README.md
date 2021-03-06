# Travaux de recherche sur le projet Aura
## Composition du dossier Scripts

Dans ce dossier se trouve l'intégralité des Notebooks que j'ai réalisé pour analyser les données misent à disposition par Aura.
Ce dossier peut être splitter en plusieurs catégories :

1. Exploration des données
  - [Exploration PAN](scripts/exploration_pan.ipynb)
  - [Exploration SWT](scripts/exploration_swt.ipynb)
  - [Exploration XQRS](scripts/exploration_xqrs.ipynb)
  - [Obtention de l'âge et du genre du patient](scripts/get_age_genre.ipynb)
  - [Analyse de la qualité des données par patient](scripts/groupby_patient.ipynb)
  - [Gestion des valeurs manquantes](scripts/impute.ipynb)
  
  <br/>
  
 2. Machine Learning
  - [Réduction de dimensions](scripts/pca.ipynb)
  - [Features Engineering](scripts/features_importances.ipynb)
  - [1ère analyse sur 1 patient donné](scripts/patient_11077.ipynb)
  - [2ème analyse sur 1 patient donné](scripts/patient_9578.ipynb)
  - [1ère analyse individuelle sur plusieurs patients](scripts/loop_over_patient.ipynb)
  - [2ème analyse individuelle sur plusieurs patients](scripts/analyse_of_49_best_patients.ipynb)
   
  <br/>
  
 3. Script / Notebook par Aura
  - [ Analyses des fichiers 'res'](scripts/Cardiac_features_computation_wrapper.py)
  - [ Visualisation des données](scripts/SingleExamAnalysis.ipynb)
    
  <br/>
  
 4. Visualisation de nos résultats de prédictions
  - [DataViz](scripts/vizualisations.ipynb)
    
  <br/>
    
 5. Scripts contenant quelques fonctions pratiques
  - [Fonctions utiles](scripts/functions.py)
    
  <br/>
  
 6. Présentation
  - [PowerPoint](Presentation.pdf)
    
  <br/>
  
 ## Description de la démarche
 Premièrement, nous avons commencé par explorer les données qui étaient à disposition.
 Ensuite, nous avons pu remarquer que la qualité des données de chaque patient/examen variait (beaucoup). Donc nous
 nous sommes basés sur la proportion des valeurs manquantes, ainsi que sur la correlation entre les différents algorithmes (PAN, SWT, XQRS)
 pour séléctionner nos données (cf. [Analyse de la qualité des données par patient](scripts/groupby_patient.ipynb)).
 
 Pour le features engineering, nous avons combiné les méthodes de Forward Selection & Backward Selection (cf. [Features Engineering](scripts/features_importances.ipynb)).
 
 Enfin, nous avons fait tourné plusieurs modèles de Machine Learning sur ces données afin de les comparer. Les résultats sont disponibles
 dans le [PowerPoint](Presentation.pdf). 
 
 L'algorithme de deep learning LSTM semble mieux performer que les autres en globalité. En effet chaque algorithme a été testé 
 sur chaque patient séléctionné individuellement. Cependant, nous avons obtenus de très bonne performance également avec un 
 algorithme DecisionTree et XGBoost.
 
 ## Autres
 J'ai également réalisé quelques [fonctions utiles](scripts/functions.py) pour la création du jeu de données global, ainsi que
 pour l'analyse de celle-ci.
 
 ## Remerciements
 Un grand merci à Jedha et à l'association Aura pour nous avoir permis de travailler sur un tel projet. C'était vraiment une
 expérience enrichissante.
  
  
