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
	* Si le texte est une date : il doit être sous la forme d'un entier qui représente le nombre de miliseconde après le 1 janvier 1970. Exemple : 12 janv 2021 0h00 UTC -> 1610409600000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm)
	* Si le texte est un booléen : il peut prendre les valeurs true \| false \| vrai \| faux \| 1 \| 0 \| oui \| non \| \| on \| off \| \| ok \| nok
	* Si le texte est un nombre, il doit contenir des chiffres. Les chiifres peuvent êtres espacés par des espaces. Le séparateur des décimales peut être une virgule ou un point. Exemple : 1 000 256.997
* Valeurs possibles : texte, chiffre, booléen
* Exemple : ```"text":"Super texte"```, ```"text":"true"```, ```"text":"25"``` 

**text_color**
* Description : Couleur du texte.
* Valeurs possibles : couleur au format hexadécimal précédé d'un #.
* Exemple : ```"text_color":"#e000e0"```

**text_decoration**
* Description : Décoration du texte, souligné, barré.
* Valeurs possibles : none \| underline \| line-through
* Exemple : ```"text_decoration":"underline"```

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

**white_space**
* Description : indique la politique de gestion des espace dans le texte.
* Valeurs possibles : normal \| nowrap
* Exemple : ```"white_space":"nowrap"```

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

**suffix**
* Description : texte placé en suffixe du texte principal.
* Valeurs possibles : simple texte.
* Exemple : ```"suffix":"Euros"```

**suffix_font_weight**
* Description : poids de la police du suffixe.
* Valeurs possibles : normal \| bold
* Exemple : ```"suffix_font_weight":"normal"```

**suffix_gap**
* Description : indique si il faut laisser un espace entre le suffixe et le texte principal.
* Valeurs possibles : true \| false
* Exemple : ```"suffix_gap":"true"```

**format_type**
* Description : indique si le text est un texte, un booléen, un nombre, une date ou du markdown
* Valeurs possibles : text \| number \| date_time \| boolean \| markdown
* Exemple : ```"format_type":"date_time"```


**date_time_format_pattern**
* Description : si le texte est une date alors cette propriété défini comment la date doit être affichée.
* Valeurs possibles : none | dd_MMMM_yyyy_UTC
* Exemple : ```"date_time_format_pattern":"dd_MMMM_yyyy_UTC"```

**boolean_format_pattern**
* Description : si le texte est un booléeb alors cette propriété défini comment il doit être affichée.
* Valeurs possibles :
	* yes_no : écrit Oui ou Non dans la langue d' l'utilisateur.
	* 1_0 : écrit 1 ou 0
	* ok_nok : écrit Ok ou Non Ok dans la langue de l'utilisateur.
	* true_false : écrit Vrai ou Faux dans la langue de l'utilisateur.
	* Mon vrai\|Mon faux : format customisé qui écrit Mon vrai ou Mon faux.
* Exemple : ```"boolean_format_pattern":"Mon vrai|Mon faux"```

