---
layout : docs_fr
id : 548rty45
readingEstimation : 15
---

## Widget Texte
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
      "uuid":"Météo",
      "type":"weather_widget",
      "widget_uuid":"uuid du widget à récupéré dans l'IHM",
      "weather_level":"weather_rain",
      "weather_type":"weather",
      "image_height":"50px",
      "image_width":"50px"      
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{      
     "weather_level":"weather_rain",
     "weather_type":"weather",
     "image_height":"50px",
     "image_width":"50px"
}
```

### Propriétés des widgets

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Project General Progress"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : weather_widget 
* Exemple : ```"type":"weather_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**weather_level** (obligatoire)
* Description : modifie la météo du widget.
* Valeurs possibles : weather_sun \| weather_cloudy \| weather_rain \| weather_thunder
* Exemple : ```"weather_level":"weather_rain"```

**weather_type**
* Description : Type d'affichage du widget. 3 types possibles : météo, feux de signalisation ou smiley.
* Valeurs possibles : weather \| traffic_light \| smiley
* Exemple : ```"weather_type":"traffic_light"```

**image_height**
* Description : hauteur de l'image en pixel.
* Valeurs possibles : nombre entier positif. 
* Exemple : ```"image_height":"50px"```

**image_width**
* Description : largeur de l'image en pixel.
* Valeurs possibles : nombre entier positif. 
* Exemple : ```"image_width":"50px"```



