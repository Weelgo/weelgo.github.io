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
* Exemple : ```"uuid":"Mon texte"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : text_widget 
* Exemple : ```"type":"text_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**text** (obligatoire)
* Description : Texte ou valeur à afficher
* Valeurs possibles : texte, chiffre, booléen
* Exemple : ```"text":"Super texte"```, ```"text":"true"```, ```"text":"25"``` 

**font_size**
* Description : Taille du texte en pixel.
* Valeurs possibles : entier positif. Ne pas mettre "px" à la fin.
* Exemple : ```"font_size":"12"```

**font_style**
* Description : Style du text, normal ou italique.
* Valeurs possibles : normal \| italic
* Exemple : ```"font_style":"italic"```

**font_weight**
* Description : poids de la police, normal ou bold.
* Valeurs possibles : normal \| bold
* Exemple : ```"font_weight":"bold"```

**prefix**
* Description : texte placé en préfixe du texte principal.
* Valeurs possibles : simple texte.
* Exemple : ```"prefix":"Nombre de risques :"```

**prefix_font_weight**
* Description : poids de la police du préfixe.
* Valeurs possibles : normal \| bold
* Exemple : ```"prefix_font_weight":"bold"```

**prefix_gap**
* Description : indique si il faut laisser un espace entre le préfix et le texte principal.
* Valeurs possibles : true \| false
* Exemple : ```"prefix_gap":"false"```









