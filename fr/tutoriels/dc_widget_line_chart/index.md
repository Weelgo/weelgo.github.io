---
layout : docs_fr
id : 548rty45
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
      "widget_uuid":"uuid du widget à récupéré dans l'IHM",
      "show_legend":"true",
      "legend_position":"top",
      "chart_height":"80px",
      "chart_width":"150px"      
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{      
    
}
```

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
* Valeurs possibles : Se référer à la documentation sur le axes en [cliquant ici](https://jsoneditoronline.org).

**y_axes**
* Description : Définition des axes des Y
* Valeurs possibles : Se référer à la documentation sur le axes en [cliquant ici](https://jsoneditoronline.org).

**datasets**
* Description : Définition des données à utiliser dans le graphiqie
* Valeurs possibles : Se référer à la documentation sur le données en [cliquant ici](https://jsoneditoronline.org).
