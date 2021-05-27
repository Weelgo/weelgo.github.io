---
layout : docs_fr
id : 88465er46
readingEstimation : 15
---

## Widget Avancement phase
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
  "uuid": "Avancement phase",
  "type": "phase_progress",
  "widget_uuid": "uuid du widget à récupéré dans l'IHM",
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{
  "weather_level":"weather_cloudy",
  "progress":"0.35",
  "flag_level":"late"
}
```

### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Avancement phase"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : phase_progress 
* Exemple : ```"type":"phase_progress"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**weather_level** (obligatoire)
* Description : Météo
* Valeurs possibles : **weather_sun** \| weather_cloudy \| weather_rain \| weather_thunder
* Exemple : ```"weather_level":"weather_cloudy"```

**progress** (obligatoire)
* Description : Progression
* Valeurs possibles : nombre réel entre 0 et 1
* Exemple : ```"progress":"0.35"```

**flag_level** (obligatoire)
* Description : permet d'indiquer si la phase est à l'heure, en retard ou très en retard. Cela affiche un texte spécifique et modifie la couleur du drapeau du widget.
* Valeurs possibles : on_time \| late \| very_late
* Exemple : ```"flag_level":"late"```

**phase_name**
* Description : nom de la phase.
* Valeurs possibles : texte libre 
* Exemple : ```"phase_name":"Phase de tests"```

**start_date**
* Description : date de début de la phase.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 12 janv 2021 0h00 UTC -> 1610409600000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"start_date":"1638316800000"```

**end_date**
* Description : date de fin de la phase.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 30 janv 2021 0h00 UTC -> 1611964800000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"end_date":"1685577600000"```

**initial_end_date**
* Description : date de fin initiale de la phase.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 25 janv 2021 0h00 UTC -> 1611532800000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"initial_end_date":"1672531200000"```

**leaders**
* Description : responsables de la phase
* Valeurs possibles : tableau contenant les colonnes **name** (obligatoire) et **uuid**. Voir ci-dessous

Exemple de JSON avec responsables (sans uuid) :

```javascript
{
  "weather_level":"weather_cloudy",
  "progress":"0.35",
  "flag_level":"late",
  "leaders":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Paul Dupond",
          "Marc Lupin"
        ]
      }
    ]
  }
}
```

Exemple de JSON avec responsables (avec uuid) :

```javascript
{
  "weather_level":"weather_cloudy",
  "progress":"0.35",
  "flag_level":"late",
  "leaders":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Paul Dupond",
          "Marc Lupin"
        ]
      },
      {
        "name": "uuid",
        "values": [
          [
            "54654-465484-46546",
            "4494-56544"
          ]
        ]
      }
    ]
  }
}
```