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
        "name": "id",
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
        "name": "id",
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
* Description : rotation du camembert
* Valeurs possibles : entier entre 0 et 360
* Exemple : ```"pie_rotation":"45"```

**datasets**
* Description : Définition des données à utiliser dans le graphiqie. Voir exemple plus bas.
* Valeurs possibles : tableau. Voir ci dessous

#### Propriété spécifique au datasets

Ces propriétés sont les colonnes du tableau

**id** (obligatoire)
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
        "name": "id",
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



