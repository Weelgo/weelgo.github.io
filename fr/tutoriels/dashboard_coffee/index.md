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
  "tasks": [
    {
      "uuid": "Pg super",
      "type": "progress_bar_widget",
      "widget_uuid": "56F876EF...",      
    }
  ]
}
```

Explication :

* "tasks" : //Tableaux de tâche
* "uuid" : Uuid de la tâche, c'est l'utilisateur qui doit le saisir. **Obligatoire**
* "type" : Type de la tâche. Certaines tâche ont un role particulier, comme les tâches correspondant aux widget qui s'occupent de formater la donnée pour permettre un afichage dans le widget.
* "widget_uuid" : Uuid du widget, utilisé pour les tâche de type widget. N'est pas obligatoire.

### Utilisation du scripting

Il suffit d'ajouter une propriété **script** à un objet **tâche**.

Cette section est une liste d'instructions.

Exemple de Json type : 

```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "script": [
          [{"integer":"25"},{"to_local_var":"var1"}],
          [{"get":"var1"},{"to_global_var":"globalVar1"}]
        ]
    }
  ]
}
```

Le script exécute chaque ligne d'instructions. Une ligne peut recevoir plusieurs instructions.

Liste des instructions :

**get**
* Description : récupère une variable. La récupération peut se faire à plusieurs niveaux.
	* Extraction de donnée : permet de chercher une donnée dans la source. Cette donnée est localisée grâce à un path. Ce path est par exemple : **programme1_@_comex_@_progress** . Ce path va récupérer la donnée progress dans le reporting comex du programme. Dans la pratique, nous préférons utilise l'uuid du comex durectement pour éviter les problèmes de path lié au changement de structure du projet. Enfin, pour indiquer qu'il s'agit d'une extraction, il faut ajouter le suffixe **path_** au path. Le path serait donc : **path_457575-457_@_progress .
* Exemple :  
	* Extraction de données : {"get":"path_uuidDuReporting_@_progress"}
	* Récupération d'une variable normale : {"get":"nomDeLaVariable"}

**integer**
* Description : récupère l'entier en paramètre
* Exemple :  {"integer":"25"}



