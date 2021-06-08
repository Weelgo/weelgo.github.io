---
layout : docs_fr
id : 5468r84g54tg
readingEstimation : 15
---

## Widget Drapeau de fin
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
      "uuid":"Drapeau de fin",
      "type":"finish_line_flag",
      "widget_uuid":"uuid du widget à récupéré dans l'IHM",
      "end_date":"1613779200000",
      "flag_level":"on_time",
      "vertical_style":"true",
      "flag_size":"28px"      
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{
      "end_date":"1613779200000",
      "flag_level":"on_time",
      "vertical_style":"true",
      "flag_size":"28px"      
}
```

### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Drapeau de fin"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : weather_widget 
* Exemple : ```"type":"finish_line_flag"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**flag_level** (obligatoire)
* Description : permet d'indiquer si le drapeau est à l'heure, en retard ou très en retard. Cela affiche un texte spécifique et modifie la couleur du drapeau du widget.
* Valeurs possibles : on_time \| late \| very_late
* Exemple : ```"flag_level":"late"```

**end_date**
* Description : date de fin affiché.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 30 janv 2021 0h00 UTC -> 1611964800000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"end_date":"1613779200000"```

**vertical_style**
* Description : Style vertical si à true. Sinon horizontal
* Valeurs possibles : **true** \| false 
* Exemple : ```"vertical_style":"true"```

**flag_size**
* Description : Taille du drapeau en pixels
* Valeurs possibles : nombre entier positif. Ajouter "px" à la fin.
* Exemple : ```"flag_size":"30px"```


