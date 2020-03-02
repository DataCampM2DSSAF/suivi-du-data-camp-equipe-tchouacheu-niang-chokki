# IEEE Fraud Detection

Une Compétition Kaggle [IEEE-CIS Fraud Detection](https://www.kaggle.com/c/ieee-fraud-detection/overview)

## Description

```
Les systèmes de prévention de la fraude permettent aux consommateurs d'économiser des millions de dollars par an. Les chercheurs de l'IEEE CIS souhaitent améliorer ce chiffre tout en améliorant l'expérience client grâce à une détection de fraude plus précise.
Dans ce projet, l'IEEE-CIS s'associent avec la plus grande société de services de paiement au monde, Vesta Corporation, à la recherche des meilleures solutions pour le secteur de la prévention de la fraude.
L’objectif est de comparer les modèles d'apprentissage automatique sur un ensemble de données à grande échelle. Les données proviennent des transactions de commerce électronique de Vesta dans le monde réel et contiennent un large éventail de fonctionnalités, du type d'appareil aux fonctionnalités du produit.
Nous devrons ainsi améliorer l'efficacité des alertes de transactions frauduleuses et donc réduire les pertes liées aux fraudes.
```

## Contenu du projet

Vous trouverez dans ce répertoire l'ensemble des dossier utiles à ce projet :
  - Notebook : l'ensemble du code Python.
  - Fichier de suivi : fichier centralisant l'évolution chronologique du projet et la répartition des tâches du team.
  - Rapport : le rapport expliquant les différentes méthodes utilisées et les résultats obtenus.

## Conditions préalables

- Install [Anaconda](https://www.anaconda.com/download/) >=5.x

- Ensuite, lancez l'application jupyter avec `jupyter notebook` ou avec `jupyter lab`.


## Télécharger ou cloner le projet dans GitHub

- Étape 1 : Entrez l'url de github dans le champ en haut à droite.
- Étape 2 : Appuyez sur la touche "Entrée" ou cliquez sur "Télécharger" pour télécharger directement le fichier zip ou cliquez sur "Rechercher" pour afficher la liste des sous-dossiers et des fichiers.
- Étape 3 : Cliquez sur "Télécharger le fichier zip" ou sur le bouton "cloner le projet" pour obtenir les fichiers.


## Télécharger le jeux de données complet sur Kaggle

- commande --> kaggle competitions download -c ieee-fraud-detection
- Site --> https://www.kaggle.com/c/ieee-fraud-detection/data


# Organisation du projet

    ├── README.md                                        <- Le README pour les développeurs qui utilisent ce projet.
    ├── données
    │   ├── train_{transaction, identity}.csv            <- the training set.
    │   ├── test_{transaction, identity}.csv             <- the test set (you must predict the isFraud value for these observations)
    │   ├── sample_submission.csv                        <- a sample submission file in the correct format
    │   
    │   
    │
    ├── suivi_ieee_fraud_detection                       <- Contenant le suivi et l'avancée du projet
    │
    ├── notebooks (ieee_fraud_detection)                 <- Contenant le fichier du projet sous Jupyter notebooks. 
    │                         t
    │                         
    │
    ├── rapport                                          <- expliquant les différentes méthodes utilisées et les résultats obtenus
    
 
* Meilleure Soumission sur Kaggle

![submission](https://user-images.githubusercontent.com/45575893/75619548-b8f00a00-5b7d-11ea-8082-c5d6d0a21f3b.PNG)

* Importance des variables du modèle ayant la meilleure soumission

![feature_importance_xgboost_tunning](https://user-images.githubusercontent.com/45575893/75619758-403e7d00-5b80-11ea-8932-31015c44200f.PNG)

* Lien GitHub du projet [**Mohamed Niang**,**Hypolite Chokki**, **Fernanda Tchouacheu** & **Sokhna Penda Toure**](https://github.com/DataCampM2DSSAF/suivi-du-data-camp-equipe-tchouacheu_toure_niang_chokki). 

* Lien Kaggle du projet [**Mohamed Niang**,**Hypolite Chokki**, **Fernanda Tchouacheu** & **Sokhna Penda Toure**](https://www.kaggle.com/niangmohamed/ieee-fraud-detection). 
