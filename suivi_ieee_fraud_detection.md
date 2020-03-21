 <h1 align="center"> Suivi du DataCamp </h1>
						
---

> 17/01/2020 : Introduction au projet avec Mme Agathe Guilloux. L'objectif de ce travail et les rendus attendus nous ont 
été présentés. Un suivi hebdomadaire du projet est mis en place.

---

> 24/01/2020 :  Cette séance nous a permis de créer les différents fichiers liés au projet. Vous trouverez une presentation 
globale du projet et de la structure du répertoire dans le fichier Readme. 
Nous avons aussi procédé à une répartition des tâches. Nous n'avons pas choisi une structure avec un chef de groupe mais 
plutôt un responsable pour chacune des parties du projet. Ci dessous, une vision globale de cette répartition :

| Mohamed Niang         | Fernanda Tchouacheu    | Hypolite Chokki      |  
| :-:                   | :-:                    | :-:                  | 
| Data exploration      | Desciptive Statistics  | LGBM Classifier      |  
| Missing Data Problem  | Memory reduction       | Neural Network       | 
| Imbalanced problem    | Random Forest          | Logistic Regression  |  
| Preprocessing         | KNearest Neighbors     |                      |            
| XGBoost Classifier    | DecisionTree Classifier|                      |
| LGBM Classifier       | Naive Bayes            |                      |                        
|notebook final&rapport | Rapport                |                      |


---

Nous avons aussi effectué une exploration de nos données. Ces dernières sont subdivisées en 4 : 

* train_transaction & test_transaction :

 	1. TransactionDT: qui mesure le temps en seconde
	2. TransactionAMT: montant du paiement de la transaction en USD
	3. ProductCD: code produit, le produit pour chaque transaction
	4. card1 - card6: informations de carte de paiement
	5. addr: adresse
	6. dist: distance
	7. Domaine de messagerie P_ et (R__): domaine de messagerie de l'acheteur et du destinataire
	8. C1-C14: comptage, par exemple le nombre d'adresses associées à la carte de paiement, etc
	9. D1-D15: timedelta, comme les jours entre la transaction précédente, etc
	10. M1-M9: correspondance, comme les noms sur la carte et l'adresse, etc
      
      Caractéristiques catégoriques:
          ProductCD
          card1 - card6
          addr1, addr2
          Pemaildomain Remaildomain
          M1 - M9


* train_identity & test_identity :

```
Les variables de ce tableau sont les informations d'identité - les informations de connexion réseau (IP, FAI, proxy, etc.) et la signature numérique (UA / navigateur / os / version, etc.) associées aux transactions. 
Ils sont collectés par le système de protection contre la fraude de Vesta et les partenaires de sécurité numérique. 
Les noms de champ sont masqués et le dictionnaire par paire ne sera pas fourni pour la protection de la vie privée et l'accord de contrat.
```

      Caractéristiques catégoriques:
          DeviceType
          DeviceInfo
          id12 - id38
      
---

> 31/01/2019 : cette séance nous a permis de mieux explorer les données.Nous avons commencé par faire une exploration des données, visualiser les problèmes que souffrent nos données. Nous avons aussi fait quelques analyses statistiques et descriptives sur les données afin de comprendre ce que nous avons comme données.

---

> 14/02/2020 : Cette séance nous a permis de finir avec la partie statistique descriptive et la première partie de traitement des données, vu qu'il y avait beaucoup de missing value dans les données. Ainsi, nous n'avons pas encore réglé le problème des classes non balancées car pour la suite nous avons décider de lancer nos premiers modèles qui sont robustes sur données non banlancée et présentant des missing. Ces derniers sont : le XGBoost, le CatBoost et le LGBM. Ces modèles sont non seulement éfficace pour les données présentant des problèmes de classe non balancée mais aussi pour des données présentant des outliers, des features non standardisées, des features collinéaires et des missing values. Ainsi nous allons dans un premier temps nous focalisé sur les modèles comme XGBOOST et LGBM. Puis dans un second temps, nous allons essayer corriger le problème de classe non balancée en faisant du resampling, faire le preprocessing necessaire et ensuite faire un apercu sur les autres modèles classiques comme Logistic regression, Naive Bayes, etc.

---

> 28/02/2020 : Pour cette séance, nous avons reussi à faire notre première soumission kaggle pour le modèle XGBoost avec un accuracy de 97% sur le test. Ainsi nous allons poursuivre avec les autres modèles dérivés du Gradient Boosting et faire les soumissions. Ensuite nous allons attaquer la deuxième partie du preprocessing avec les classes non balancées et faire tourner les autres modèles et voir les prédictions sur le jeux de données Test.

---

> 06/03/2020 : Nous avons réussi à faire l'optimisation des paramètres du premier modèle XGBoost et nous obtenu un accuracy de 98% sur le test. Ce modèle a pu amélioré le score public et privé sur Kaggle après soumission. Après ceci, nous avons lancé le modèle LGBM avec optimisation des hyperparamètres pour lequel aussi on a eu un accuracy de 98%. Toutefois puisqu'on est en présence de classe non balancée, on peut s'attendre à ce que l'accuracy surestime la précision. Ainsi pour la suite, nous allons aussi nous basé sur le score AUC pour mesuré le pouvoir prédictif des modèles. En poursuivant la modélisation, nous avons enrichit le modèle XGBOOST, cette fois ci en faisant du local validation et cross validation et en créant de nouvelles features obtenues par aggrégation d'autres features, qui nous a donné un score public de 0.9494 et un score privé de 0.9219 après soumission sur Kaggle. Pour la suite, nous allons poursuivre avec le modèle LGBM en faisant aussi la meme chose comme pour le XGBOOST. En meme temps, nous avons débuter avec la rédaction du rapport.

---

> 16/03/2020 : Nous allons finir avec la modélisation et faire les dernières soumissions Kaggle. Ensuite, nous allons poursuivre avec la rédaction du rapport.

---
