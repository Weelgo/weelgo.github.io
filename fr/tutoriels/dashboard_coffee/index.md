---
layout : docs_fr
id : 548rty45
readingEstimation : 15
---

## Infos pour Dashboard Coffee
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

Json type la secion BPM :

```javascript
{
  "tasks": [     //Tableaux de tâche
    {
      "uuid": "Pg super",     //Obligatoire : Uuid de la tâche, c'est l'utilisateur qui doit le saisir
      "type": "progress_bar_widget",		//Type de la tâche.
      "widget_uuid": "56F876EF...",     //Uuid du widget, utilisé pour les tâche de type widget. N'est pas obligatoire      
    }
  ]
}
```

### Utilisation du scripting

Il suffit d'ajouter une propriété **script** à un objet **tâche**.

Cette section est une liste d'instructions.

Exemple de Json type : 

```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "script": [       //Section script
          {"integer":"25"},      //Première instruction, on récupère l'entier 25
          {"to_local_var":"var1"}     //Deuxième instruction, on le met en variable locale
        ]
    }
  ]
}
```

Liste des instructions :

integer : 

* Description : récupère l'entier en paramètre
* Exemple : {"integer":"25"}

