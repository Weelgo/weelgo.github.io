---
layout : docs_fr
id : rg54yh787y
readingEstimation : 15
---

## Définition des données pour les graphes
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 


### Axe des X ou des Y
 
Permet de définir un ou plusieurs axes des X ou Y. La propriété correpondante est **x_axes** ou **y_axes**.

#### Type catégorie

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

#### Type linéaire
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

#### Type série temporelle
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



