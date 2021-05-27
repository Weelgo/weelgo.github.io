---
layout : docs_fr
id : 548rty45
readingEstimation : 15
---

## Définition des données pour les graphes
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 


### x_axes
 
Permet de définir un ou plusieurs axes des X

#### Axe de type catégorie

Ce JSON permet de créer un axe des X avec 3 catégories, cat1, cat2 et cat3.
```javascript
{
  "x_axes": {
    "columns": [
      {
        "name": "type",
        "values": [
          "category"
        ]
      },
      {
        "name": "categories",
        "values": [
          [
            "Cat 1",
            "Cat 2",
            "Cat 3"
          ]
        ]
      }
    ]
  }
}
```

#### Axe de type linéaire
```javascript
{
  "x_axes": {
    "columns": [
      {
        "name": "type",
        "values": [
          "linear"
        ]
      }
    ]
  }
}
```

#### Axe de type série temporelle
```javascript
{
  "x_axes": {
    "columns": [
      {
        "name": "type",
        "values": [
          "time_series"
        ]
      }
    ]
  }
}
```



