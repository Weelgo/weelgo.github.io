---
layout : docs_fr
id : 548rty45
readingEstimation : 15
---

## Widget Progression générale du projet
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
      "uuid":"Project General Progress",
      "type":"project_general_progress_widget",
      "widget_uuid":"uuid du widget à récupéré dans l'IHM",
      "weather_level":"weather_rain",
      "progress":"0.55",
      "start_date":"1610409600000",
      "end_date":"1611964800000",
      "initial_end_date":"1611532800000",
      "flag_level":"late"
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{      
      "weather_level":"weather_rain",
      "progress":"0.55",
      "start_date":"1610409600000",
      "end_date":"1611964800000",
      "initial_end_date":"1611532800000",
      "flag_level":"late"
}
```

### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Project General Progress"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : project_general_progress_widget 
* Exemple : ```"type":"project_general_progress_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**weather_level** (obligatoire)
* Description : modifie la météo du widget.
* Valeurs possibles : weather_sun \| weather_cloudy \| weather_rain \| weather_thunder
* Exemple : ```"weather_level":"weather_rain"```

**progress** (obligatoire)
* Description : progression du widget
* Valeurs possibles : réel entre 0 et 1
* Exemple : ```"progress":"0.25"```

**start_date**
* Description : date de début du projet.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 12 janv 2021 0h00 UTC -> 1610409600000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"start_date":"1638316800000"```

**end_date**
* Description : date de fin du projet.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 30 janv 2021 0h00 UTC -> 1611964800000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"end_date":"1685577600000"```

**initial_end_date**
* Description : date de fin initiale du projet.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 25 janv 2021 0h00 UTC -> 1611532800000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"initial_end_date":"1672531200000"```

**flag_level** (obligatoire)
* Description : permet d'indiquer si le projet est à l'heure, en retard ou très en retard. Cela affiche un texte spécifique et modifie la couleur du drapeau du widget.
* Valeurs possibles : on_time \| late \| very_late
* Exemple : ```"flag_level":"late"```



