---
layout : docs_fr
id : 88465er46
readingEstimation : 15
---

## Widget Evènements significatifs
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
  "uuid": "Evènements significatifs",
  "type": "significant_events_widget",
  "widget_uuid": "uuid du widget à récupéré dans l'IHM",
  "events": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Evènement 1",
          "Evènement 2"
        ]
      },
      {
        "name": "description",
        "values": [
          "Description évènement 1",
          "Description *évènement 2*"
        ]
      },
      {
        "name": "icon",
        "values": [
          "ic_diamond_solid",
          "ic_exclamation_circle_solid"
        ]
      },
      {
        "name": "event_date",
        "values": [
          "1638316800000",
          "1610409600000"
        ]
      }
    ]
  }
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{
  "events": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Evènement 1",
          "Evènement 2"
        ]
      },
      {
        "name": "description",
        "values": [
          "Description évènement 1",
          "Description *évènement 2*"
        ]
      },
      {
        "name": "icon",
        "values": [
          "ic_diamond_solid",
          "ic_exclamation_circle_solid"
        ]
      },
      {
        "name": "event_date",
        "values": [
          "1638316800000",
          "1610409600000"
        ]
      }
    ]
  }
}
```

### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Evènements"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : significant_events_widget 
* Exemple : ```"type":"significant_events_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```


**width**  
* Description : largeur du widget
* Valeurs possibles : nombre entier, ajouter "px" à la fin 
* Exemple : ```"width":"100px"```

**events**  
* Description : tableau contenant les évènements
* Valeurs possibles : voir la description des paramètres ci dessous

#### Colonnes possibles du tableau de **events**

**name**  (obligatoire)
* Description : nom ou label de l'évènement
* Valeurs possibles : texte libre
* Exemple : ```"Evènement important 1"```

**uuid**  
* Description : uuid du sujet
* Valeurs possibles : texte libre
* Exemple : ```"565465-444-8484"```

**order_index**
* Description :
* Valeurs possibles : entier supérieur ou égal à 0
* Exemple : ```"2"```

**description**
* Description : description du sujet
* Valeurs possibles : texte libre en markdown
* Exemple : ```"Super **description**"```

**icon**
* Description : icone de l'évènement
* Valeurs possibles : voir l'enum IconEnum
* Exemple : ```"ic_diamond_solid"```

**event_date**
* Description : date de l'évènement
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 12 janv 2021 0h00 UTC -> 1610409600000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"1638316800000"```

Exemple de JSON :

```javascript
{
  "events":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Sujet important 1",
          "Sujet important 2",
          "Sujet important 3"
        ]
      },
      {
        "name": "description",
        "values": [
          "Description sujet 1",
          "",
          "Description sujet 3"
        ]
      }
    ]
  } 
}
```



