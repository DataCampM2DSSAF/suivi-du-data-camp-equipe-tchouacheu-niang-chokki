 <h1 align="center"> Suivi du Projet </h1>
						
---

> 17/01/2020 : Introduction au projet avec Mme Agathe Guilloux. L'objectif de ce travail et les rendus attendus nous ont 
été présentés. Un suivi hebdomadaire du projet est mis en place.

---

> 24/01/2020 :  Cette séance nous a permis de créer les différents fichiers liés au projet. Vous trouverez une presentation 
globale du projet et de la structure du répertoire dans le fichier Readme. 
Nous avons aussi procédé à une répartition des tâches. Nous n'avons pas choisi un structure avec un chef de groupe mais 
plutôt un responsable pour chacune des parties du projet. Ci dessous, une vision globale de cette répartition :

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

* Mohamed Niang : 
					- Data exploration
					- Missing Data
					- Imbalanced problem
					- Preprocessing 

* Fernanda Tchouacheu :
					- Desciptive Statistics
					- Memory reduction


* Hypolite Chokki :
                                        - XGBoost Classifier
					- CatBoost Classifier
					- LGBM Classifier
					- Neural Network

* Sokhna Penda Toure :
					- Logistic Regression
					- KNearest Neighbors
					- Support Vector Classifier
					- Random Forest 
					- DecisionTree Classifier

---

Nous avons aussi effectué une exploration de nos données. Ces dernières sont subdivisées en 4 : 

- train_transaction & test_transaction
      TransactionDT: timedelta à partir d'un datetime de référence donné (pas un horodatage réel)
      TransactionAMT: montant du paiement de la transaction en USD
      ProductCD: code produit, le produit pour chaque transaction
      card1 - card6: informations de carte de paiement, telles que le type de carte, la catégorie de carte, la banque d'émission, le pays, etc.
      addr: adresse
      dist: distance
      Domaine de messagerie P_ et (R__): domaine de messagerie de l'acheteur et du destinataire
      C1-C14: comptage, par exemple le nombre d'adresses associées à la carte de paiement, etc. La signification réelle est masquée.
      D1-D15: timedelta, comme les jours entre la transaction précédente, etc.
      M1-M9: correspondance, comme les noms sur la carte et l'adresse, etc.
      Vxxx: Vesta a conçu de riches fonctionnalités, notamment le classement, le comptage et d'autres relations d'entité.
      
      Caractéristiques catégoriques:
          ProductCD
          card1 - card6
          addr1, addr2
          Pemaildomain Remaildomain
          M1 - M9


- train_identity & test_identity
      Les variables de ce tableau sont les informations d'identité - les informations de connexion réseau (IP, FAI, proxy, etc.) et la signature numérique (UA / navigateur / os / version, etc.) associées aux transactions.
      Ils sont collectés par le système de protection contre la fraude de Vesta et les partenaires de sécurité numérique.
      (Les noms de champ sont masqués et le dictionnaire par paire ne sera pas fourni pour la protection de la vie privée et l'accord de contrat)

      Caractéristiques catégoriques:
          DeviceType
          DeviceInfo
          id12 - id38
      
---

> 31/01/2019 : cette séance nous a permis de mieux explorer les données.Nous avons commencé par faire une exploration des données, visualiser les problèmes que souffrent nos données. Nous avons aussi fait quelques analyses statistiques et descriptives sur les données afin de comprendre ce que nous avons comme données.

---

> 14/02/2020 : Cette séance nous a permis de finir avec la partie statistique descriptive et la première partie de traitement des données, vu qu'il y avait beaucoup de missing value dans les données. Ainsi, nous n'avons pas encore réglé le problème des classes non balancées car pour la suite nous avons décider de lancer nos premiers modèles qui sont robustes sur données non banlancée et présentant des missing. Ces derniers sont : le XGBoost, le CatBoost et le LGBM. 

---

> 28/02/2020 : Pour cette séance, nous avons reussi à faire notre première soumission kaggle pour le modèle XGBoost avec un accuracy de 97% sur le test. Ainsi nous allons poursuivre avec les autres modèles dérivés du Gradient Boosting et faire les soumissions. Ensuite nous allons attaquer la deuxième partie du preprocessing avec les classes non balancées et faire tourner les autres modèles et voir les prédictions sur le jeux de données Test.

---

> Nous avons réussi à faire l'optimisation des paramètres du premier modèle XGBoost et nous obtenu un accuracy de 98% sur le test. 
