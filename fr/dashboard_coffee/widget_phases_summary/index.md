---
layout : docs_fr
id : 88465er46
readingEstimation : 15
---

## Widget Vue d'enssemble des phases
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
  "uuid": "Phases",
  "type": "phases_summary",
  "widget_uuid": "uuid du widget à récupéré dans l'IHM",
  "phases":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Phase 1",
          "Phase 2",
          "Phase 3"
        ]
      },
      {
        "name": "progress",
        "values": [
          "1",
          "0.2",
          "0"
        ]
      }
    ]
  } 
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{
  "phases":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Phase 1",
          "Phase 2",
          "Phase 3"
        ]
      },
      {
        "name": "progress",
        "values": [
          "1",
          "0.2",
          "0"
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
* Exemple : ```"uuid":"Phases"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : phases_summary 
* Exemple : ```"type":"phases_summary"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**RESTE A FAIRE**
