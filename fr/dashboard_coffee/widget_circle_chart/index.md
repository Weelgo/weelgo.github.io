---
layout : docs_fr
id : lngh78et45
readingEstimation : 15
---

## Widget Graphique progression circulaire
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON


Exemple de JSON à inclure dans le BPM du widget:
```javascript
{      
   "progress":"0.2",
   "circle_height":"50px",
   "circle_width":"50px",
   "circle_color":"#e000e0",
   "circle_background_color":"#f0f0f0",
   "circle_circumference":"180",
   "circle_central_void_size":"0.7",
   "circle_rotation":"45",
   "show_progress_number":"true",
   "progress_number_color":"#e000e0",
   "progress_number_font_weight":"bold",
   "progress_number_font_size":"15",
   "style":"special_1",
   "done_label":"Fait",
   "to_do_label":"A Faire"
}
```

Exemple progression demi cercle
```javascript
{      
   "progress":"0.2",
   "circle_height":"50px",
   "circle_width":"50px",   
   "circle_circumference":"180",
   "circle_central_void_size":"0.7",
   "circle_rotation":"45"   
}
```

### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Mon cercle"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : progress_circle_widget 
* Exemple : ```"type":"progress_circle_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**progress** (obligatoire)
* Description : progress
* Valeurs possibles : réel entre 0 et 1
* Exemple : ```"progress":"0.2"```

**circle_height**
* Description : hauteur du cercle en pixel
* Valeurs possibles : entier positif, ajouter "px" à la fin
* Exemple : ```"circle_height":"100px"```

**circle_width**
* Description : largeur du cercle en pixel
* Valeurs possibles : entier positif, ajouter "px" à la fin
* Exemple : ```"circle_width":"100px"```

**circle_color**
* Description : Couleur de la partie réalisée.
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"circle_color":"#e000e0"```

**circle_background_color**
* Description : Couleur de la partie à réaliser.
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"circle_color":"#e000e0"```

**circle_circumference**
* Description : circonférence du cercle. 360 = cercle, 180 = demi-cercle
* Valeurs possibles : entier entre 0 et 360
* Exemple : ```"circle_circumference":"180"```

**circle_central_void_size**
* Description : taille du trou dans le cercle, pour faire des donuts.
* Valeurs possibles : réel entre 0 et 1. 0 = pas de trou, 1 = plus de cercle
* Exemple : ```"circle_central_void_size":"0.7"```

**circle_rotation**
* Description : rotation du cercle. -90 (avec pie_circumference:180) pour avoir un arc en ciel. 
* Valeurs possibles : entier entre 0 et 360
* Exemple : ```"circle_rotation":"45"```

**show_progress_number**
* Description : affiche la progression en chiffre 
* Valeurs possibles : **true** \| false
* Exemple : ```"show_progress_number":"false"```

**progress_number_color**
* Description : Couleur du chiffre
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"progress_number_color":"#e000e0"```

**progress_number_font_weight**
* Description : poids de la police.
* Valeurs possibles : **normal** \| bold
* Exemple : ```"progress_number_font_weight":"normal"```

**progress_number_font_size**
* Description : Taille du texte en pixel.
* Valeurs possibles : entier positif. Ne pas mettre "px" à la fin.
* Exemple : ```"progress_number_font_size":"12"```

**style**
* Description : Style d'affichage. special_1 met un icone done quand la progression est à 100%
* Valeurs possibles : **normal** \| special_1
* Exemple : ```"style":"special_1"```

**done_label**
* Description : Label à afficher au survol de la souris sur la partie réalisée
* Valeurs possibles : Texte libre
* Exemple : ```"done_label":"Réalisé"```

**to_do_label**
* Description : Label à afficher au survol de la souris sur la partie à réalisée
* Valeurs possibles : Texte libre
* Exemple : ```"done_label":"A réaliser"```


