---
layout : docs_fr
id : 88465er46
readingEstimation : 15
---

## Widget Sujets abordés
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
  "uuid": "Sujets abordés",
  "type": "covered_topics_widget",
  "widget_uuid": "uuid du widget à récupéré dans l'IHM" ,
  "topics":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Sujet important 1",
          "Sujet important 2",
          "Sujet important 3"
        ]
      }
    ]
  } 
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{
  "topics":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Sujet important 1",
          "Sujet important 2",
          "Sujet important 3"
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
* Exemple : ```"uuid":"Sujets abordés"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : covered_topics_widget 
* Exemple : ```"type":"covered_topics_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```


**width**  
* Description : largeur du widget
* Valeurs possibles : nombre entier, ajouter "px" à la fin 
* Exemple : ```"width":"100px"```


**topics**  
* Description : tableau contenant les sujets
* Valeurs possibles : voir la description des paramètres ci dessous

#### Colonnes possibles du tableau de sujets

**name**  (obligatoire)
* Description : nom ou label sujet
* Valeurs possibles : texte libre
* Exemple : ```"Sujet important 1"```

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

**comments**
* Description : commentaires sur le sujet
* Valeurs possibles : texte libre en markdown
* Exemple : ```"Super **commentaire**"```

**decisions_or_actions**
* Description : décisions ou action prises à propos du sujet abordé.
* Valeurs possibles : texte libre en markdown
* Exemple : ```"Super **décision**"```

Exemple de JSON :

```javascript
{
  "topics":{
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



