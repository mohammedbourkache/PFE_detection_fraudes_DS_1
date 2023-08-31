# Signification des variables :

 ## 1.variables quantitatives

### a).  int  :

'Unnamed: 0' :------------------- identique à l'index des lignes , donc on supprime cette colonne .(spr)

'accountNumber' ET 'customerId': ces deux colonnes sont identique,fort possible par ce que chaque account est associé à un et un seul customer .(grd='accountNumber' ,'customerId')

'creditLimit':------------------- semble interressant dans le cas de  passer au-delà d'une valeur limite.(grd)

'cardCVV':-----------------------est le code de sécurité de la carte (Card Verification Value).(grd)
'enteredCVV':--------------------Il s'agit du CVV saisi lors de la transaction(grd)
-> il y a une relation entre ces deux variables ; elles sont utilisées pour vérifier l'authenticité d'une transaction. 

'cardLast4Digits':---------------ici cette information est inutile car ce numéro change et on n'a pas une colonne comparable à ce numéro.(spr)
 
 

### b).float :
currentBalance :  a une relation avec availableMoney et transactionAmount

*availableMoney


*transactionAmount  

*posEntryMode 

*posConditionCode 

## 2. Variables Qualitatives : 

### a) object :
       *date : ->transactionDateTime (Y/M/D T:h:min:sec)
              ->currentExpDate(M/Y)
              ->accountOpenDate(Y/M/D)
              ->dateOfLastAddressChange(Y/M/D)
              
       *transactionType:
                     ['PURCHASE'Achat,
                     'ADDRESS_VERIFICATION'Vérification d'Adresse ,
                     'REVERSAL' Annulation ou Remboursement,
                      nan]
                     
       *merchantCountryCode , acqCountry :
                     ['US' 'CAN' nan 'PR' 'MEX']
           
       *merchantName 
       
       *merchantCategoryCode

### b). bool :
       *'cardPresent'
       *'expirationDateKeyInMatch'  
       *'isFraud'                        

# <span style="color:blue">______ Aprés L'analyse et nettoyage de nos données :_______</span>

## 1.variables quantitatives

### a).  int  :

'creditLimit'


### b).float :
currentBalance :  a une relation avec availableMoney et transactionAmount

*availableMoney


*transactionAmount  

*posEntryMode 

*posConditionCode 

## 2. Variables Qualitatives : 

### a) object :
             
       *transactionType:
                     ['PURCHASE',
                     'ADDRESS_VERIFICATION',
                     'REVERSAL']
                     
           
       *merchantName 
       
       *merchantCategoryCode

### b) bool : 
       *'cardPresent'
     
       *'isFraud
       
       *ckecked_cvv
       
       *card_in_country

# Prétraitement de données (pre-processing) :
encodage :
     convertir les données qualitatives en valeurs numériques
     
normalisation :
     mettre sur une meme echelle toutes  les variables quantitatives qui va facilite le ML
     
imputation :
     remplacer les données manquantes par certaines valeurs statistiques
     
selection :
     selectionner les variables les plus utiles pour le modele 
     
extraction :
     generer de nouvelles variables à partir d'informations cachés dans le dataset

nettoyage , filrage

Filtrage : Identifier et supprimer les données qui ne sont pas pertinentes pour votre analyse ou votre modèle. Cela peut inclure des enregistrements qui ne correspondent pas à vos critères d'intérêt ou qui sont des valeurs aberrantes.

Nettoyage : Traiter les données pour éliminer les erreurs, les valeurs aberrantes, les doublons et autres problèmes qui pourraient affecter la qualité de vos données. Cela peut impliquer la correction de valeurs incorrectes, la suppression de données dupliquées et la gestion des valeurs manquantes.


```python

```
