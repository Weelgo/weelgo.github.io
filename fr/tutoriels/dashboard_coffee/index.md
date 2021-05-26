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
* "widget\_uuid" : Uuid du widget, utilisé pour les tâche de type widget. N'est pas obligatoire.

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
	* Extraction de donnée : permet de chercher une donnée dans la source. Cette donnée est localisée grâce à un path. Ce path est par exemple : **programme1\_@\_comex\_@\_progress** . Ce path va récupérer la donnée progress dans le reporting comex du programme. Dans la pratique, nous préférons utilise l'uuid du comex durectement pour éviter les problèmes de path lié au changement de structure du projet. Enfin, pour indiquer qu'il s'agit d'une extraction, il faut ajouter le suffixe **path\_** au path. Le path serait donc : **path\_457575-457\_@\_progress** . Notez que le séparateur de path est **\_@\_** .
	* Récupération d'une variable : il suffit de mettre le nom de la variable à récupérer.
* Exemple :  
	* Extraction de données : ```{"get":"path_uuidDuReporting_@_progress"}```
	* Récupération d'une variable normale : ```{"get":"nomDeLaVariable"}```

**integer**
* Description : récupère l'entier en paramètre
* Exemple :  ```{"integer":"25"}```

**to\_local\_var**
* Description : met la variable dans le pool de variable locale. Ces variables ne seront accessible que au sein de la tâche. Elles seront supprimée à la fin du tritement dela tâche
* Exemple :  ```{"to_local_var":"var1"}```

**to\_global\_var**
* Description : met la variable dans le pool de variables globales. Ces variables seront accessibles pour toutes les tâches suivante.
* Exemple :  ```{"to_global_var":"var1"}```

**average**
* Description : permet de faire une moyenne des ligne de la variable.
* Paramètre :
	* Param 1 : nom de la colonne pour réaliser la moyenne. Peut être vide, mais doit être présent (eg : ""). Si le nom de la colonne est vide, alors, la fonction utilisera la première colonne du tableau pour faire la moyenne.
	* Param 2 : liste des variables que vous voulez ajouter pour faire la moyenne. Par exemple : "var1" en cas d'une variable. Pour plusieurs variable il suffit de continuer à les lister : "var1","var2"
* Exemple :
	* Cas d'utilisation de l'instruction en début de chaine : ```{"average":["col1","var1","var2"]}``` . Cette instruction réalise la moyenne sur la colonne **col1** des variables **var1** et **var2**
	* Moyenne d'une variable récupéré dans le pool : ```{"get":"var1"},{"average":""},{"to\_local\_var":"var2"}``` . Cette série d'instruction récupère la variable **var1** et ensuite calcule la moyenne sur la première colonne puis met le résultat en variable locale **var2**.

