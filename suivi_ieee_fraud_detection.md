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
| notebook final        | Naive Bayes            |                      |                        
|                       | Rapport                |                      |


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

> 14/02/2020 : Cette séance nous a permis de finir avec la partie statistique descriptive et la première partie de traitement des données, vu qu'il y avait beaucoup de missing value dans les données. Ainsi, nous n'avons pas encore réglé le problème des classes non balancées car pour la suite nous avons décider de lancer nos premiers modèles qui sont robustes sur données non banlancée et présentant des missing. Ces derniers sont : le XGBoost, le CatBoost et le LGBM. Ces modèles sont non seulement éfficace pour les données présentant des problèmes de classe non balancée mais aussi pour des données présentant des outliers, des features non standardisées, des features collinéaires et des missing values. Ainsi nous allons dans un premier temps nous focalisé sur les modèles comme XGBOOST et LGBM. Puis dans un second temps, nous allons essayer corriger le problème de classe non balancée en faisant du resampling ou de la stratification, faire le preprocessing necessaire et ensuite faire un apercu sur les autres modèles classiques comme le Logistic regression, Naive Bayes, etc.

![ Approach to Ensemble based Methodologies](https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2017/03/16142904/ICP4.png)

> XGBoost

![](https://miro.medium.com/max/1400/1*FLshv-wVDfu-i54OqvZdHg.png)

---

> 28/02/2020 : Pour cette séance, nous avons reussi à faire notre première soumission kaggle pour le modèle XGBoost avec un accuracy de 97% sur le test. Ainsi nous allons poursuivre avec les autres modèles dérivés du Gradient Boosting et faire les soumissions. Ensuite nous allons attaquer la deuxième partie du preprocessing avec les classes non balancées (resampling ou stratification) et faire tourner les autres modèles et voir les prédictions sur le jeux de données de validation.

---

> 06/03/2020 : Nous avons réussi à faire l'optimisation des paramètres du premier modèle XGBoost et nous obtenu un accuracy de 98% sur le test. Ce modèle a pu amélioré le score public et privé sur Kaggle après soumission. Après ceci, nous avons lancé le modèle LGBM avec optimisation des hyperparamètres pour lequel aussi on a eu un accuracy de 98%. Toutefois puisqu'on est en présence de classe non balancée, on peut s'attendre à ce que l'accuracy surestime la précision. Ainsi pour la suite, nous allons aussi nous basé sur le score AUC pour mesuré le pouvoir prédictif des modèles. En poursuivant la modélisation, nous avons enrichit le modèle XGBOOST, cette fois ci en faisant du local validation et cross validation et en créant de nouvelles features obtenues par aggrégation d'autres features, qui nous a donné un score public de 0.950164 et un score privé de 0.921794 après soumission sur Kaggle. Pour la suite, nous allons poursuivre avec le modèle LGBM en faisant aussi la meme chose comme pour le XGBOOST. En meme temps, nous avons débuter avec la rédaction du rapport.

---

> 16/03/2020 : Nous allons finir avec la modélisation et faire les dernières soumissions Kaggle. Ensuite, nous allons poursuivre avec la rédaction du rapport. Avec le modèle LGBM, nous avons obtenu un accuracy de 99% et un AUC de 97,68%. Ce modèle a pu amélioré le score privé sur Kaggle après soumission qui est ainsi devenu 0.921948 mais n'a pas amélioré le score public. Mais quand meme avec l'aggregation des features, on voit qu'on obtient de très bon résultat. Ainsi, nous allons poursuivre et finir avec les modèles classiques et l'apprentissage profond. Pour cela, nous allons commencer par régler le problème de classe non balancée (resampling ou stratification) et faire quelque preprocessing necessaire (normalisation, etc).

---

> 27/03/2020 : Vu le problème de classe non balancée, il est nous primordial de le corriger avant de s'attaquer aux méthodes d'apprentissages classiques et d'apprentissages profonds. En effet, lorsque les données présentent des classes non équilibrées, il sera pas du tout ingenieux d'utiliser les memes techniques classiques pour résoudre le problème posé. Il est recomandé aux Data Scientist de revoir soit la métrique à utliser pour évaluer la performance des modèles (matrice de confusion, f1_score, precision, recall, etc), soit d'utiliser une technique de resampling, soit d'utiliser les algorithmes ensemblistes (XGBOOST, LGBM, etc) pour contourner le problème de classe non équilibrée. 

![](https://raw.githubusercontent.com/rafjaa/machine_learning_fecib/master/src/static/img/resampling.png)

> Pour ce faire, dans cette séance, nous avons commencé à tester les méthodes de resampling. Premièrement, nous avons fait du oversampling qui consiste à ajouter des exemples sur la classe minoritaire pour équilibrer les classes. Cet ajout d'exemple s'appuie juste sur un tirage avec remise de l'échantillon constituant la classe minoritaire, donc non robuste si on présente beaucoup de données. Cette dernière méthode a été testé mais n'a pas donné de bon résultat. Du coup, en faisant un peu de recherche, on s'est appercu qu'il existe d'autres techniques de resampling plus sophistiquées en utlisant le module imbalanced-learn de Python.

> Au lieu de créer des copies exactes des individus de la classe minoritaire, nous pouvons introduire de petites variations dans ces copies, créant ainsi des échantillons synthétiques plus diversifiés. Mais malheuresement, cette méthode n'a pas aussi marché. Du coup, on s'est tourné à utiliser une autre technique de ré-échantillonnage, le SMOTE.

> Le SMOTE (Synthetic Minority Oversampling TEchnique) consiste à synthétiser des éléments pour la classe minoritaire, en se basant sur ceux qui existent déjà. Elle consiste à choisir au hasard un point de la classe minoritaire et à calculer les voisins les plus proches pour ce point. Les points de synthèse sont ajoutés entre le point choisi et ses voisins.

![](https://raw.githubusercontent.com/rafjaa/machine_learning_fecib/master/src/static/img/smote.png)

---
