---
layout : docs_fr
id : lngh78et45
readingEstimation : 15
---

## Widget Graphique Bar chart
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON
```javascript
{
  "show_legend":"false",
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
          [
            "Achat",
            "Commerce",
            "Direction",
            "Finance",
            "Marketing",
            "Production",
            "R&D"
          ]
        ]
      }
    ]
  },
  "y_axes": {
    "columns": [
      {
        "name": "type",
        "values": [
          "linear"
        ]
      }
    ]
  },
  "datasets":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Répartition par département"
        ]
      },
      {
        "name": "values",
        "values": [
          ["20","40","15","35","25","70","43"]
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
* Exemple : ```"uuid":"Mon Bar chart"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : bar_chart_widget 
* Exemple : ```"type":"bar_chart_widget"```

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
* Description : hauteur du graphe en pixel
* Valeurs possibles : entier positif, ajouter "px" à la fin
* Exemple : ```"chart_height":"100px"```

**chart_width**
* Description : largeur du graphe en pixel
* Valeurs possibles : entier positif, ajouter "px" à la fin
* Exemple : ```"chart_width":"100px"```

**stacked**
* Description : indique si il faudra empiler des barres
* Valeurs possibles : true \| **false**
* Exemple : ```"stacked":"true"```

**horizontal_bars**
* Description : indique si l'affichage des barre se fera vertical ou horizontal.
* Valeurs possibles : true \| **false**
* Exemple : ```"horizontal_bars":"true"```



**datasets**
* Description : Définition des données à utiliser dans le graphiqie. Voir exemple plus bas.
* Valeurs possibles : tableau. Voir ci dessous

#### Propriété spécifique au datasets

Ces propriétés sont les colonnes du tableau

**name** (obligatoire)
* Description : Nom du set de données
* Valeurs possibles : texte libre
* Exemple : ```"Femmes"```

**values**
* Description : Valeurs pour chaque catégorie
* Valeurs possibles : tableau
* Exemple : ```"["25","30","40"]"```

**values2d**
* Description : Valeurs pour chaque catégorie
* Valeurs possibles : tableau
* Exemple : ```"[["25","30"],["25","30"]]"```

**background_color**
* Description : Couleur de bond de la barre
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"#e000e0"```

**border_color**
* Description : Couleur de la bordure de la barre
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"#e000e0"```

**border_width**
* Description : Taille de la bordure de la barre
* Valeurs possibles : entier en pixel. Ne pas ajouter "px" à la fin. Par défaut, c'est 0;
* Exemple : ```"2"```

**stack_group**
* Description : Nom du groupe pour pouvoir stacker les barres
* Valeurs possibles : texte libre
* Exemple : ```"gp1"```





