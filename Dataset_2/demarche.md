# 1. Exploratory Data Analysis

## Objectif :
- Comprendre du mieux possible nos données (un petit pas en avant vaut mieux qu'un grand pas en arriere)
- Développer une premiere stratégie de modélisation 

## Checklist de base
#### Analyse de Forme :
- **variable target** : isFraud
- **lignes et colonnes** : 786363, 30
- **types de variables** :  nbr_qualitatives(object ,bool)= 12 | nbr_quantitatives(float , int) = 18
- **Analyse des valeurs manquantes** :
  - 3 groupes : 
    - groupe comptétement de NaN (6 variables = 100% de NaN) :
    
         {merchantCity                
          merchantState               
          merchantZip                 
          posOnPremises              
          recurringAuthInd            
          echoBuffer  }
         
    - groupe de données de 00.052%  à  00.58% de NaN(5 variables):
    
        {posConditionCode           
         transactionType             
         merchantCountryCode         
         posEntryMode                
         acqCountry }
    
    -  groupe :il n'ya aucune valeur manquante 0% de NaN (19 variables) : 
        
        {Unnamed: 0       
        cardPresent       
        currentBalance     
        cardLast4Digits    
        enteredCVV         
        cardCVV            
        dateOfLastAddressChange  
        expirationDateKeyInMatch 
        currentExpDate
        merchantCategoryCode    
        accountOpenDate         
        isFraud                 
        accountNumber           
        customerId              
        merchantName            
        transactionAmount       
        transactionDateTime    
        availableMoney         
        creditLimit }
       

#### Analyse de Fond :
 
- **Visualisation de la target** :
    - 1.579% de True (12417 /  773946)
    
    { isFraud__mean  |   nbr-occ
    
    False____0.98421  |  773946
    
     True____0.01579 | 12417
     
    }
    
 ➜ nos classes ne sont pas équilibrées(on doit utiliser des metriques comme : score F1 ,sensibilité ,précision )
      

- **Signification des variables** :
    - Dans un fichier spéciale



- **Relation Variables / Target** :
       
    - target / cardPresent : si la carte est présente et sinon 
    - target/amount :  ➜ 
    - target / type :  ➜
    
 'pour savoir les relations entre int et target(T/F)-> sns.countplot'
 'pour savoir les relations entre vars catégoriels et target(T/F)-> pd.crosstab'
 
    
    
## Analyse plus détaillée


-a). j'ai eu l'idée de combiner ces deux colonnes: 
 
       -acqCountry (Pays d'Acquisition) : Il s'agit du pays où la carte de crédit a été émise. C'est le pays d'origine de la                                   carte de crédit utilisée pour effectuer la transaction.
        -merchantCountryCode (Code de Pays du Marchand) : Il s'agit du pays dans lequel le commerçant (merchant) effectue la                                     transaction. C'est le pays où l'achat réel a lieu.
        
   ➜la relation entre ces deux variables ;pour indiquer si la transaction s'est déroulée dans le même pays que celui où la carte a été émise(si la transaction a eu lieu conformément à l'endroit où la carte a été émise).
        
b). et de combiner ces deux colonnes:
'cardCVV'(Card Verification Value):-----------------------est le code de sécurité de la carte .
'enteredCVV':--------------------Il s'agit du CVV saisi lors de la transaction.

   ➜ la relation entre ces deux variables ; elles sont utilisées pour vérifier l'authenticité d'une transaction. 

- **NaN analyse** 







```python

```
