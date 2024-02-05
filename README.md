# Heart attack prediction  

### Ce dataset kaggle répertorie 8763 individus à risque d'attaque cardiaque (35%) ou pas (65%).  
### Chaque individu est identifié par :  
-Son patient_ID  
-Son âge, genre, sexe  
-Des données physiologiques  
-Ses habitudes alimentaires  
-Ses habitudes sportives  
-Des données géographiques  

### On va mettre en place un algorithme de classification binaire (risque d'attaque : 1, pas de risque : 0)

### On va séparer la colonne 'Blood pressure' en 'Systolic' et 'Diastolic'

### Aucun autre préprocessing n'est nécessaire. Pycaret gère automatiquement le hot encoding, les valeurs manquantes, les outliers, les classes déséquilibrées...
### Pycaret va entraîner par cross validation plusieurs modèles.  
### Nous prenons comme indicateur de performance le rappel (recall) qui est le ratio du nombre de prédictions de risque d'attaque correct sur le nombre de risque d'attaque réel. 

### Le meilleur modèle est le KNeighborsClassifier avec un recall de 1 sur les données de test mais la classe 1 a aspiré toute les prédictions ! On peut certainement faire mieux en blendant les 5 meilleurs modèles. 

### Ce dernier modèle obtient une accuracy parfaite de 1 sur l'ensemble des données de test !