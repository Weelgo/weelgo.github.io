---
layout : docs_fr
id : lngh78et45
readingEstimation : 15
---

## Widget Graphique ligne
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
      "uuid":"Graphique",
      "type":"line_chart_widget",
      "widget_uuid":"uuid du widget à récupéré dans l'IHM"
       
}
```

Exemple de JSON à inclure dans le BPM du widget: Voir plus bas.


### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Mon graphique"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : line_chart_widget 
* Exemple : ```"type":"line_chart_widget"```

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
* Exemple : ```"legend_position":"traffic_light"```

**chart_height**
* Description : hauteur du graphique en pixel.
* Valeurs possibles : nombre entier positif. Ajouter "px" à la fin.
* Exemple : ```"chart_height":"150px"```

**chart_width**
* Description : largeur du graphique en pixel.
* Valeurs possibles : nombre entier positif. Ajouter "px" à la fin.
* Exemple : ```"chart_width":"300px"```

**x_axes**
* Description : Définition des axes des X
* Valeurs possibles : Se référer à la documentation sur le axes en [cliquant ici](../dc_widget_chart_data/).

**y_axes**
* Description : Définition des axes des Y
* Valeurs possibles : Se référer à la documentation sur le axes en [cliquant ici](../dc_widget_chart_data/).

**datasets**
* Description : Définition des données à utiliser dans le graphiqie. Voir exemple plus bas.

#### Propriété spécifique au datasets

Ces propriétés doivent être placé dans une cellule du tableau

**name**
* Description : Nom du set de données.
* Valeurs possibles : Text.
* Exemple : Budget total, Situation

**values** (utilisé pour les axes des X de type catégories)
* Description : Valeurs des points de la série.
* Valeurs possibles : tableau numérique.
* Exemple : ```["y","y","y"]``` -> ```["500","800","100"]``` si il y a 3 catégories.

**values2d** (utilisé pour les axes des X de type linéaire ou série temporelles
* Description : Valeurs des points de la série.
* Valeurs possibles : tableau numérique 2d.
* Exemple : ```[["x","y"],["x","y"],["x","y"]]``` -> ```[["3","12"],["8","7"],["25","98"]]```

**background_color**
* Description : Couleur de l'aire sous la courbe.
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : #e000e0

**border_color**
* Description : Couleur de la courbe.
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : #e000e0

**border_width**
* Description : largeur de la courbe en pixel.
* Valeurs possibles : entier, ne pas ajouter "px" à la fin.
* Exemple : 3

**point_background_color**
* Description : Couleur du point de la courbe.
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : #e000e0

**point_border_color**
* Description : Couleur de la bordure du point de la courbe.
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : #e000e0

**point_border_width**
* Description : taille la bordure du point de la courbe en pixel
* Valeurs possibles : entier, ne pas ajouter "px" à la fin.
* Exemple : 1

**point_radius**
* Description : rayon du point en pixel
* Valeurs possibles : entier, ne pas ajouter "px" à la fin.
* Exemple : 4

**point_style**
* Description : style de la forme du point
* Valeurs possibles : circle \| cross \| cross_rot \| rect \| rect_rot \| star \| triangle 
* Exemple : cross

### Exemples

**Type catégories**

Exemple de JSON pour un graphique avec des catégories. Dans le graphique ci dessous il y a 4 courbes, chaque courbe a des style de point différents 
et possède chacune 3 points qui sont les points correspondants à chaque catégories "cat 1", "cat 1" et "cat 1".
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
          ["Cat 1","Cat 2","Cat 3"
          ]
        ]
      }
    ]
  },
  "datasets": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Budget total",
          "Budget engagé",
          "Budget à engager",
          "Situation"
        ]
      },
      {
        "name": "point_style",
        "values": [
          "circle",
          "rect",
          "star",
          "triangle"
        ]
      },
      {
        "name": "point_radius",
        "values": [
          "10",
          "10",
          "10",
          "10"
        ]
      },
      {
        "name": "values",
        "values": [
          [ "500","800","100"],
          ["400","300","50"],
          ["200","400","80"],
          ["-100","-200","-500"]
        ]
      }
    ]
  }
}
```

**Type linéaire**

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
  },
  "datasets": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Série 1",
          "Série 2"
        ]
      },
      {
        "name": "point_style",
        "values": [
          "circle",
          "rect"
        ]
      },
      {
        "name": "point_radius",
        "values": [
          "10",
          "10"
        ]
      },
      {
        "name": "values2d",
        "values": [
          [["6","12"],["8","15"],["25","50"]],
          [["3","12"],["8","7"],["25","98"],["45","58"],["50","58"]]
        ]
      }
    ]
  }
}
```


**Type série temporelle**

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
  },
  "datasets": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Série 1",
          "Série 2"
        ]
      },
      {
        "name": "point_style",
        "values": [
          "circle",
          "rect"
        ]
      },
      {
        "name": "point_radius",
        "values": [
          "10",
          "10"
        ]
      },
      {
        "name": "values2d",
        "values": [
          [["1609459200000","12"],["1609545600000","15"],["1609632000000","50"]],
          [["1609459200000","15"],["1609545600000","7"],["1609632000000","98"],["1609718400000","58"],["1609804800000","58"]]
        ]
      }
    ]
  }
}
```
