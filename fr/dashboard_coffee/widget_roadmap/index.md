---
layout : docs_fr
id : 88465er46
readingEstimation : 15
---

## Widget Roadmap
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
  "uuid": "Roadmap",
  "type": "roadmap_widget",
  "widget_uuid": "uuid du widget à récupéré dans l'IHM",
  "lines":"Mettre ici la structure des lignes comme ci dessous"
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{
  "lines": {
    "columns": [
      {
        "name": "uuid",
        "values": [
          "gp1",
          "ph1",
          "ml1",
          "gp2"
        ]
      },
      {
        "name": "name",
        "values": [
          "Groupe 1",
          "Phase 1",
          "Jalon 1",
          "Groupe 2"
        ]
      },
      {
        "name": "parent_uuid",
        "values": [
          "",
          "gp1",
          "gp2",
          "gp1"
        ]
      },
      {
        "name": "object_type",
        "values": [
          "group",
          "phase",
          "milestone",
          "group"
        ]
      },
      {
        "name": "background_color",
        "values": [
          "#ff4da6",
          "#9e1fff",
          "#009e9e",
          "#e0e000"
        ]
      },
      {
        "name": "start_date",
        "values": [
          "",
          "1609804800000",
          "",
          ""
        ]
      },
      {
        "name": "end_date",
        "values": [
          "",
          "1611100800000",
          "1611100800000",
          ""
        ]
      },
      {
        "name": "icon",
        "values": [
          "",
          "",
          "ic_diamond_solid",
          ""
        ]
      }
    ]
  }
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{
  "width":"960px",
  "lines": {
    "columns": [
      {
        "name": "uuid",
        "values": [
          "jalons",
          "infrastructure",
          "fibre",
          "servers",
          "applicatif",
          "app1",
          "contractualisation",
          "v105",
          "v110",
          "v120",
          "fin_projet",
          "creuser_tranchees",
          "installer_fibre",
          "verif_ok",
          "test synchro 1",
          "test synchro 2",
          "test synchro 3",
          "conception",
          "pre_dev",
          "dev",
          "MEP V1"
        ]
      },
      {
        "name": "name",
        "values": [
          "Jalons",
          "Infrastructure",
          "Fibre",
          "Servers",
          "Applicatif",
          "App 1",
          "Contractualisation",
          "V1.0.5",
          "V1.1.0",
          "V1.2.0",
          "Fin Projet",
          "Creuser_tranchées",
          "Installer fibre",
          "Verification OK",
          "Test synchro 1",
          "Test synchro 2",
          "Test synchro 3",
          "Conception",
          "Pré Dev",
          "Dev",
          "MEP V1"
        ]
      },
      {
        "name": "parent_uuid",
        "values": [
          "",
          "",
          "infrastructure",
          "infrastructure",
          "",
          "applicatif",
          "jalons",
          "jalons",
          "jalons",
          "jalons",
          "jalons",
          "fibre",
          "fibre",
          "fibre",
          "servers",
          "servers",
          "servers",
          "app1",
          "app1",
          "app1",
          "app1"
        ]
      },
      {
        "name": "object_type",
        "values": [
          "group",
          "group",
          "group",
          "group",
          "group",
          "group",
          "milestone",
          "milestone",
          "milestone",
          "milestone",
          "milestone",
          "phase",
          "phase",
          "milestone",
          "milestone",
          "milestone",
          "milestone",
          "phase",
          "phase",
          "phase",
          "milestone"
        ]
      },
      {
        "name": "background_color",
        "values": [
          "#f0e200",
          "#0085bc",
          "#7bcff3",
          "#b7e5f8",
          "#ba41ed",
          "#e5b7f8",
          "#baaf00",
          "#baaf00",
          "#baaf00",
          "#baaf00",
          "#baaf00",
          "#41baed",
          "#41baed",
          "#41baed",
          "#e70000",
          "#e70000",
          "#e70000",
          "#cf7bf3",
          "#cf7bf3",
          "#cf7bf3",
          "#a300e7"
        ]
      },
      {
        "name": "name_color",
        "values": [
          "",
          "white",
          "",
          "",
          "white",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          ""
        ]
      },
      {
        "name": "style",
        "values": [
          "v_block",
          "v_block",
          "",
          "",
          "v_block",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          ""
        ]
      }, 
      {
        "name": "start_date",
        "values": [
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "",
          "1633046400000",
          "1639526400000",
          "",
          "",
          "",
          "",
          "1635724800000",
          "1637798400000",
          "1639526400000",
          ""
        ]
      },
      {
        "name": "end_date",
        "values": [
          "",
          "",
          "",
          "",
          "",
          "",
          "1633046400000",
          "1635724800000",
          "1638316800000",
          "1640995200000",
          "1643673600000",
          "1636934400000",
          "1642204800000",
          "1639526400000",
          "1635724800000",
          "1638316800000",
          "1640995200000",
          "1637798400000",
          "1639526400000",
          "1642204800000",
          "1643068800000"
        ]
      },
      {
        "name": "icon",
        "values": [
          "",
          "",
          "",
          "",
          "",
          "",
          "ic_hand_shake_solid",
          "ic_diamond_solid",
          "ic_diamond_solid",
          "ic_diamond_solid",
          "ic_glass_cheers_solid",
          "",
          "",
          "ic_flag_solid",
          "ic_star_solid",
          "ic_star_solid",
          "ic_star_solid",
          "",
          "",
          "",
          "ic_trophy_solid"
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
* Exemple : ```"uuid":"Ma roadmap"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : roadmap_widget 
* Exemple : ```"type":"roadmap_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**width**  
* Description : largeur du widget
* Valeurs possibles : nombre entier, ajouter "px" à la fin 
* Exemple : ```"width":"100px"```

**lines**
* Description : Définition des données à utiliser dans la roadmap
* Valeurs possibles : tableau. Voir ci dessous

#### Propriété spécifique à la propriété **lines**

Ces propriétés sont les colonnes du tableau

Les lignes du tableau sont communes pour les Groupe, les Phases et les Jalons

**uuid**  (obligatoire)
* Description : Uuid de la ligne. Est utilisé pour mapper les parent/enfante entre eux
* Valeurs possibles : texte libre
* Exemple : ```"4565-548-456"```

**name**  (obligatoire)
* Description : Nom de la ligne.
* Valeurs possibles : texte libre
* Exemple : ```"4565-548-456"```

**object_type** (obligatoire)
* Description : Type de l'objet : groupe, phase ou milestone
* Valeurs possibles : group \| phase \| milestone
* Exemple : ```"milestone"```

**parent_uuid**
* Description : Uuid du parent. Si non présent, alors le parent est le groupe racine
* Valeurs possibles : texte libre
* Exemple : ```"4565-548-456"```

**order_index**
* Description : Ordre d'affichage dans les groupe
* Valeurs possibles : entier supérieur ou égal à 0
* Exemple : ```"2"```

**background_color**
* Description : Pour le groupe : couleur du fond. Pour une phase ou un milestone : couleur de la phase ou de l'icone du milestone.
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"#e000e0"```

**bold_name**
* Description : Nom en gras ou pas
* Valeurs possibles : true \| ***false***
* Exemple : ```"true"```

**name_color** (uniquement pour les groupes)
* Description : Couleur du nom
* Valeurs possibles : couleur au format hexadécimal précédé d’un #.
* Exemple : ```"#e000e0"```

**style** (pour les groupe uniquement)
* Description : affichage horizontal ou vertical du nom
* Valeurs possibles : **h_block** \| v_block
* Exemple : ```"v_block"```

**start_date** (pour les phases uniquement)
* Description : date de début de la phase.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 12 janv 2021 0h00 UTC -> 1610409600000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"1638316800000"```

**end_date** (pour les phases et les jalons uniquement)
* Description : date de fin de la phase ou du jalon.
* Valeurs possibles : nb miliseconde après le 1 janvier 1970. Exemple : 30 janv 2021 0h00 UTC -> 1611964800000. Lien vers un convertisseur en ligne : [cliquez ici](https://www.fileformat.info/tip/java/date2millis.htm) 
* Exemple : ```"1685577600000"```

**icon**(pour les jalons uniquement)
* Description : icone du jalon
* Valeurs possibles : voir IconEnum 
* Exemple : ```"ic_diamond_solid"```

**show_date** (pour les jalons uniquement)
* Description : Affiche la date dans la roadmap
* Valeurs possibles : true \| ***false***
* Exemple : ```"true"```


