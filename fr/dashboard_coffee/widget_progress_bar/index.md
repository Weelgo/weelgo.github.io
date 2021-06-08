---
layout : docs_fr
id : ghy78zr56
readingEstimation : 15
---

## Widget Barre de progression
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
      "uuid":"Barre de progression",
      "type":"progress_bar_widget",
      "widget_uuid":"uuid du widget à récupéré dans l'IHM",
      "progress":"0.2",
      "bar_color":"#e000e0",
      "bar_background_color":"#e000e0",
      "bar_height":"15px",
      "bar_width":"150px",
      "show_progress_number":"true"
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{      
     "bar_progress":"0.2",
      "bar_color":"#e000e0",
      "bar_background_color":"#e000e0",
      "bar_height":"15px",
      "bar_width":"150px",
      "show_progress_number":"true"
}
```

### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Barre de progression"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : weather_widget 
* Exemple : ```"type":"progress_bar_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**progress** (obligatoire)
* Description : Progression
* Valeurs possibles : nombre réel entre 0 et 1
* Exemple : ```"progress":"0.35"```

**bar_height**
* Description : hauteur de la barre en pixel
* Valeurs possibles : nombre entier positif. Ajouter "px" à la fin.
* Exemple : ```"bar_height":"50px"```

**bar_width**
* Description : largeur de la barre en pixel.
* Valeurs possibles : nombre entier positif. Ajouter "px" à la fin.
* Exemple : ```"bar_width":"50px"```

**bar_color**
* Description : Couleur de la barre de progression.
* Valeurs possibles : couleur au format hexadécimal précédé d'un #.
* Exemple : ```"bar_color":"#e000e0"```

**bar_background_color**
* Description : Couleur du background de la barre.
* Valeurs possibles : couleur au format hexadécimal précédé d'un #.
* Exemple : ```"bar_background_color":"#e000e0"```

**show_progress_number**
* Description : indique si il faut afficher le nombre de progression à droite de la barre
* Valeurs possibles : **true** \| false
* Exemple : ```"show_progress_number":"false"```

