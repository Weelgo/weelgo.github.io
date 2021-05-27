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
      "text":"Voici un super texte"    
}
```

Exemple de JSON à inclure dans le BPM du widget:

JSON minimal

```javascript
{      
     "text":"Voici un super texte"
}
```

JSON texte

```javascript
{      
     "text":"Voici un super texte",
     "text_color":"#e000e0",
     "text_decoration":"underline",
     "font_size":"20",
     "font_style":"italic",
     "white_space":"nowrap",
     "prefix":"Nombre de risques :",
     "prefix_font_weight":"bold",
     "prefix_gap":"true",
     "suffix":"Euros",
     "suffix_font_weight":"bold",
     "suffix_gap":"false"
}
```

JSON pour un chiffre, affiche 2 526 400,40
```javascript
{      
     "text":"2526400.4",
     "format_type":"number",
     "nb_minimum_fraction_digits":"2"
}

```

JSON pour un chiffre, affiche 2_526_400*40
```javascript
{      
     "text":"2526400.4",
     "format_type":"number",
     "nb_minimum_fraction_digits":"2",
     "decimal_separator":"*",
     "grouping_separator":"_"
}
```

JSON pour une date, affiche 12 janvier 2021 UTC+02:00
```javascript
{      
     "text":"1610409600000",
     "format_type":"date_time",
     "date_time_format_pattern":"dd_MMMM_yyyy_UTC"
}

```

JSON pour un booléen, affiche Mon faux
```javascript
{      
     "text":"false",
     "format_type":"boolean",
     "boolean_format_pattern":"Mon vrai|Mon faux"
}

```

### Propriétés du widgets

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
* Exemple : ```"text":"Super texte"``` ou alors ```"text":"true"``` ou alors ```"text":"25"``` 

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

**format_type** (obligatoire en cas de nombre, date, booléen ou markdwn)
* Description : indique si le text est un texte, un booléen, un nombre, une date ou du markdown
* Valeurs possibles : text \| number \| date_time \| boolean \| markdown
* Exemple : ```"format_type":"date_time"```


**date_time_format_pattern**
* Description : si le texte est une date alors cette propriété défini comment la date doit être affichée.
* Valeurs possibles : none \| dd_MMMM_yyyy_UTC
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

**decimal_separator**
* Description : séparateur des décimal. Par dafaut, c'est une virgule : 123,56
* Valeurs possibles : virgule, point, texte au choix.
* Exemple : ```"decimal_separator":"."```

**grouping_separator**
* Description : séparateur des groupes de chiffre. Par dafaut c'est un espace : 1 000 000
* Valeurs possibles : espace, virgule, point, texte au choix.
* Exemple : ```"grouping_separator":","```

**use_grouping**
* Description : Indique si il faut grouper par paquet de 3 l'affichage d'un nombre. Par défaut le grouping est activé.
* Valeurs possibles : true \| false
* Exemple : ```"use_grouping":"true"```

**nb_minimum_fraction_digits**
* Description : nombre minimal de chiffre à afficher après la virgule. Par défaut, c'est 0 : 1000. Si cette valeur est 2, alors 1000 sera affiché 100,00.
* Valeurs possibles : entier positif.
* Exemple : ```"nb_minimum_fraction_digits":"2"```

**nb_minimum_integer_digits**
* Description : nombre minimal de chiffre à afficher avant la virgule. Par défaut, c'est 1. Si cette valeur est 3, alors 5 sera affiché 005.
* Valeurs possibles : entier positif.
* Exemple : ```"nb_minimum_integer_digits":"3"```

**multiply_by**
* Description : si le texte est un nombre, alors cette propriété permet de le multiplier avant affichage. La valeur par défaut est 1. Par exemple si la aleur est 0.01, alors le chiffre 50 sera multiplié par 0.01 ce qui donnera 0.5.
* Valeurs possibles : 0.001 \| 0.01 \| 0.1 \| 1 \| 10 \| 100 \| 1000 \| 
* Exemple : ```"multiply_by":"0.01"```




