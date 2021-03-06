---
layout : docs_fr
id : lngh78et45
readingEstimation : 15
---

## Widget Graphique camembert
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
  "uuid": "Camembert",
  "type": "simple_pie_chart_widget",
  "widget_uuid": "uuid du widget à récupéré dans l'IHM",
  "datasets": {
    "columns": [
      {
        "name": "uuid",
        "values": [
          "Nb pommes",
          "Nb patates",
          "Nb carottes"
        ]
      },
      {
        "name": "value",
        "values": [
          "10",
          "15",
          "3"
        ]
      }
    ]
  }
}
```

Exemple de JSON à inclure dans le BPM du widget:
```javascript
{
  "datasets":{
    "columns": [
      {
        "name": "uuid",
        "values": [
          "Nb pommes",
          "Nb patates",
          "Nb carottes"
        ]
      },
      {
        "name": "value",
        "values": [
          "10",
          "15",
          "3"
        ]
      }
    ]
  } 
}
```

Exemple jauge à 180° vert orange rouge
```javascript
{
  "pie_height":"50px",
  "pie_width":"100px",
  "pie_circumference":"180",
  "pie_rotation":"-90",
  "show_needle":"true",
  "needle_height":"40",
  "needle_width":"1",
  "needle_rotation":"-90",
  "needle_position_left":"50",
  "needle_position_top":"7",
  "needle_progress":"0",
   "pie_central_void_size":"0.6",
  "datasets":{
    "columns": [
      {
        "name": "uuid",
        "values": [
          "Bas",
          "Moyen",
          "Haut"
        ]
      },
      {
        "name": "value",
        "values": [
          "1",
          "1",
          "1"
        ]
      },
      {
        "name": "background_color",
        "values": [
          "#41c057",
          "#f59f02",
          "#fa5251"
        ]
      }
    ]
  } 
}
```

Exemple jauge à 180° bleu
```javascript
{
  "pie_height":"50px",
  "pie_width":"100px",
  "pie_circumference":"180",
  "pie_rotation":"-90",
  "show_needle":"true",
  "needle_height":"40",
  "needle_width":"1",
  "needle_rotation":"-90",
  "needle_position_left":"50",
  "needle_position_top":"7",
  "needle_progress":"0",
   "pie_central_void_size":"0.6",
  "datasets":{
    "columns": [
      {
        "name": "uuid",
        "values": [
          "Bas",
          "Moyen",
          "Haut"
        ]
      },
      {
        "name": "value",
        "values": [
          "1",
          "1",
          "1"
        ]
      },
      {
        "name": "background_color",
        "values": [
          "#90dfef",
          "#55cfe9",
          "#1db9db"
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
* Exemple : ```"uuid":"Mon camembert"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : simple_pie_chart_widget 
* Exemple : ```"type":"simple_pie_chart_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**show_legend**
* Description : affiche la légende
* Valeurs possibles : **true** \| false
* Exemple : ```"show_legend":"false"```

**legend_position**
* Description : positino de la légende
* Valeurs possibles : top \| right \| left \| **bottom**
* Exemple : ```"legend_position":"right"```

**pie_height**
* Description : hauteur du camembert en pixel
* Valeurs possibles : entier positif, ajouter "px" à la fin
* Exemple : ```"pie_height":"100px"```

**pie_width**
* Description : largeur du camembert en pixel
* Valeurs possibles : entier positif, ajouter "px" à la fin
* Exemple : ```"pie_width":"100px"```

**pie_circumference**
* Description : circonférence du camembert. 360 = cercle, 180 = demi-cercle
* Valeurs possibles : entier entre 0 et 360
* Exemple : ```"pie_circumference":"180"```

**pie_central_void_size**
* Description : taille du trou dans le camembert, pour faire des donuts.
* Valeurs possibles : réel entre 0 et 1. 0 = pas de trou, 1 = plus de camembert
* Exemple : ```"pie_central_void_size":"0.7"```

**pie_rotation**
* Description : rotation du camembert. -90 (avec pie_circumference:180) pour avoir un arc en ciel. 
* Valeurs possibles : entier entre 0 et 360
* Exemple : ```"pie_rotation":"45"```

**fill_pie_if_zero**
* Description : Si toutes les ligne on une valeur égale à 0, alors on affiche une camambert contenant des quartiers égau 
* Valeurs possibles : **true** \| false
* Exemple : ```"fill_pie_if_zero":"false"```

**show_needle**
* Description : affiche une aiguille
* Valeurs possibles : true \| f**alse**
* Exemple : ```"show_needle":"true"```

**needle_color**
* Description : couleur de l'aiguille
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"needle_color":"#e000e0"```

**needle_height**
* Description : Hauteur de l'aiguille
* Valeurs possibles : entier positif, valeur en pixel. NE PAS ajouter "px" à la fin
* Exemple : ```"needle_height":"200"```

**needle_width**
* Description : Largeur de l'aiguille
* Valeurs possibles : entier positif, valeur en pixel. NE PAS ajouter "px" à la fin
* Exemple : ```"needle_width":"5"```

**needle_rotation**
* Description : rotation de référence de l'aiguille. 
* Valeurs possibles : entier entre 0 et 360
* Exemple : ```"needle_rotation":"45"```

**needle_position_left**
* Description : Position left de l'aiguille
* Valeurs possibles : entier positif, valeur en pixel. NE PAS ajouter "px" à la fin
* Exemple : ```"needle_position_left":"10"```

**needle_position_top**
* Description : Position top de l'aiguille
* Valeurs possibles : entier positif, valeur en pixel. NE PAS ajouter "px" à la fin
* Exemple : ```"needle_position_top":"10"```

**needle_progress**
* Description : Progression de l'aiguille
* Valeurs possibles : réel entre 0 et 1.
* Exemple : ```"needle_progress":"0.25"```

**datasets**
* Description : Définition des données à utiliser dans le graphiqie. Voir exemple plus bas.
* Valeurs possibles : tableau. Voir ci dessous

#### Propriété spécifique au datasets

Ces propriétés sont les colonnes du tableau

**uuid** (obligatoire)
* Description : identifiant de la donnée. Peut-être le label.
* Valeurs possibles : texte libre
* Exemple : ```"Nb actions"```

**value** (obligatoire)
* Description : Valeur du quartier de camambert
* Valeurs possibles : nombre réel
* Exemple : ```"25"```

**name**
* Description : Nom de la donnée. C'est le nom qui sera affiché en légende et dans le camembert. Si non présent, alors c'est l'**id** qui sera utilisé
* Valeurs possibles : texte libre
* Exemple : ```"Nb actions"```

**background_color**
* Description : Couleur du quartier de camembert
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"#e000e0"```


Exemple :

```javascript
{
  "datasets": {
    "columns": [
      {
        "name": "uuid",
        "values": [
          "NBPo",
          "NBPa",
          "NBC"
        ]
      },
      {
        "name": "value",
        "values": [
          "10",
          "15",
          "3"
        ]
      },
      {
        "name": "name",
        "values": [
          "Pommes",
          "Patates",
          "Carottes"
        ]
      },
      {
        "name": "background_color",
        "values": [
          "#e000e0",
          "#3d3dff",
          "#006161"
        ]
      }
    ]
  }
}
```



