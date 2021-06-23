---
layout : docs_fr
id : lngh78et45
readingEstimation : 15
---

## Widget Graphique radar
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM du widget:
```javascript
{
  "radar_background_color":"#1db9db2e",
  "radar_border_color":"#1db9db",
  "radar_border_width":"1",
  "radar_point_background_color":"#1db9db2e",
  "radar_point_border_color":"#1db9db",
  "radar_point_border_width":"1",
  "radar_point_border_radius":"3",
  "datasets":{
    "columns": [
      {
        "name": "uuid",
        "values": [
          "Nb pommes",
          "Nb patates",
          "Nb carottes",
          "Nb navets",
          "Nb tomates"
        ]
      },
      {
        "name": "value",
        "values": [
          "10",
          "15",
          "20",
          "15",
          "12"
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
* Exemple : ```"uuid":"Mon radar"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : radar_chart_widget 
* Exemple : ```"type":"radar_chart_widget"```

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

**chart_height**
* Description : hauteur du camembert en pixel
* Valeurs possibles : entier positif, ajouter "px" à la fin
* Exemple : ```"chart_height":"100px"```

**chart_width**
* Description : largeur du camembert en pixel
* Valeurs possibles : entier positif, ajouter "px" à la fin
* Exemple : ```"chart_width":"100px"```


**radar_background_color**
* Description : Couleur de fond de la toile
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.

**radar_border_color**
* Description : Couleur de la ligne de la toile
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.

**radar_border_width**
* Description : taille de la bordure de la toile
* Valeurs possibles : entier, ne pas ajouter "px" à la fin.

**radar_point_background_color**
* Description : Couleur de fond de la toile
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.

**radar_point_border_color**
* Description : Couleur de fond de la toile
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.

**radar_point_border_width**
* Description : taille de la bordure de la toile
* Valeurs possibles : entier, ne pas ajouter "px" à la fin.

**radar_point_border_radius**
* Description : taille de la bordure de la toile
* Valeurs possibles : entier, ne pas ajouter "px" à la fin.


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



