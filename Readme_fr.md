# Fraud Detection with Machine Learning On Bank system Data

Des comportements frauduleux peuvent être observés dans de nombreux domaines différents tels que le e-commerce, assurance maladie  les systèmes de paiement et bancaires. La fraude coûte des millions d'euros aux entreprises chaque année.[pwc report]

La détection automatisée des comportements frauduleux peut être réalisée de différentes manières, notamment par des approches basées sur des règles metiers et par l'apprentissage automatique. Cette demo utilise cette dernière approche pour la classification des transactions frauduleuses.

Pour une analyse approfondie, vous pouvez consulter mon notebook sur mon github ci-dessous :
https://github.com/userilyo/

Le jeu de données généré synthétiquement comprend des paiements de différents clients effectués à différentes périodes et avec différents montants. 
Si vous souhaitez plus d'informations sur le jeu de données, vous pouvez vous référer ci-dessous au titre Dataset pour le lien et les informations sur le jeu de données, et vous pouvez trouver plus deteail en ligne.
Pour ceux qui ne souhaitent pas exécuter le script pour obtenir les résultats, voici un bref récapitulatif des résultats de classification des modèles d'apprentissage automatique utilisés dans le script :

!Note: Ces résultats sont sans la technique de suréchantillonnage SMOTE. 
J'ai également ajouté un notebook Jupyter avec plus d'analyses et utilisé SMOTE pour équilibrer le jeu de données. Les résultats globaux semblent meilleurs, il suffit de consulter le fichier appelé Fraud Detection on Bank Payments.ipynb à l'intérieur du dépôt."


<br/>Classification Report for K-Nearest Neighbours (1:fraudulent,0:non-fraudulent) :

|class | precision | recall | f1-score | support|
| ---- | --------- | ------ | -------- | -------|        
|  0   |   1.00    |   1.00 |  1.00    | 176233 |
|  1   |   0.83    |   0.61 |  0.70    |  2160  |
           
Confusion Matrix of K-Nearest Neigbours:
<br/> [175962    271]
<br/> [   845   1315] 



<br/>Classification Report for XGBoost : 

class | precision | recall | f1-score | support|
| ---- | --------- | ------ | -------- | -------|        
|  0   |   1.00    |   1.00 |  1.00    | 176233 |
|  1   |   0.89    |   0.76 |  0.82    |  2160  |
           
           
Confusion Matrix of XGBoost: 
<br/> [176029    204] 
<br/> [   529   1631] 




<br/>Classification Report for Random Forest Classifier : 

class | precision | recall | f1-score | support|
| ---- | --------- | ------ | -------- | -------|        
|  0   |   1.00    |   0.96 |  0.98    | 176233 |
|  1   |   0.24    |   0.98 |  0.82    |  2160  |
           
         
 Confusion Matrix of Random Forest Classifier: 
<br/> [169552   6681]
<br/> [    39   2121]



<br/>Classification Report for Ensembled Models(RandomForest+KNN+XGBoost) : 

class | precision | recall | f1-score | support|
| ---- | --------- | ------ | -------- | -------|        
|  0   |   1.00    |   1.00 |  1.00    | 176233 |
|  1   |   0.73    |   0.81 |  0.77    |  2160  |
           

Confusion Matrix of Ensembled Models: 
<br/> [175604    629]
<br/> [   417   1743]



