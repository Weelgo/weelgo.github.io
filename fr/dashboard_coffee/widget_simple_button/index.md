---
layout : docs_fr
id : ghy78zr56
readingEstimation : 15
---

## Widget Bouton
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
      "uuid":"Bouton",
      "type":"simple_button_widget",
      "widget_uuid":"uuid du widget à récupéré dans l'IHM",
      "name":"Super bouton",
      "icon":"ic_arrow_right",
      "button_type":"circle",
      "style":"success",
      "size":"lg",
      "target_parameters":"545744-754184-544",
      "target_type":"dashboard",
      "open_type":"panel"
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{      
      "name":"Super bouton",
      "icon":"ic_arrow_right",
      "button_type":"circle",
      "style":"success",
      "size":"lg",
      "target_parameters":"545744-754184-544",
      "target_type":"dashboard",
      "open_type":"panel"
}
```

### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Mon bouton"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : simple_button_widget 
* Exemple : ```"type":"simple_button_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**name**
* Description : Nom du bouton
* Valeurs possibles : texte libre, peut être vide
* Exemple : ```"name":"Mon bouton"```

**icon**
* Description : type de l'icon affiché, voir IconEnum
* Valeurs possibles : voir IconEnum 
* Exemple : ```"name":"ic_diamond_solid"```

**icon_size**
* Description : taille de l'icone. Vide par défaut.
* Valeurs possibles : taille en pixel. Ajouter "px" à la fin.
* Exemple : ```"icon_size":"20px"```

**type**
* Description : type du bouton
* Valeurs possibles :  **normal** \| circle
* Exemple : ```"type":"circle"```

**style**
* Description : style d bouton
* Valeurs possibles : **normal** \| transparent \| success \| success_light
* Exemple : ```"size":"lg"```

**size**
* Description : taille du bouton
* Valeurs possibles : xs \| sm \| **nm** \| lg \| xl
* Exemple : ```"size":"lg"```

**target_parameters**
* Description : paramètre du lien du bouton. Dans le cas d'un URL, c'est l'url qu'il fau tmettre. En cas d'un bouton pour ouvrir un autre dashboard, il fut mettre l'uuid du dashboard
* Valeurs possibles : url du lien, ou uuid du dashboard
* Exemple : ```"target_parameters":"https//wwww.weelgo.com"```

**target_type**
* Description : type d'élément à ouvrir.
* Valeurs possibles : url \| dashboard
* Exemple : ```"target_type":"url"```

**open_type**
* Description : indique comment ouvrir la page
* Valeurs possibles : page \| panel \| new_tab
* Exemple : ```"open_type":"panel"```



