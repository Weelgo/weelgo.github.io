---
layout : docs_fr
id : 548rty45
readingEstimation : 15
---

## Infos pour Dashboard Coffee
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

Exemple de Json pour la section BPM générale :

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

### Récupération de variable directement dans les valeurs des propriété

Si vous avez créé une variable à l'aide du scripting, vous pouvez la récupérer directement pour la mettre dans une propriété d'un widget. Vous pouvez récupérer soit des variables globales, soit des extractions de données.

Exemple d'une extraction de donnée directement en paramètre : 
```javascript
{
  "progress":"src_path:uuidDuReporting_@_progress"
}
```  

Exemple de récupération d'une variable globale directement en paramètre : 
```javascript
{
  "progress":"global_var:ma_variable_1"
}
```

Il est également possible de récupérer la valeur sous format String d'une variable au milieu d'un paramètre. Pour cela utilisez ```${nom_de_la_variable}``` au milieu d'un path.

C'est pratique quand on a veut constituer des path relatigs de récupération de données.

Par exemple le script suivant :
```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "script": [
          [{"string":"384e85e8-3949-4dd5-aa1a-b47fb78ef013"},{"to_global_var":"area_uuid"}],
          [{"get":"src_path:${area_uuid}_@_project_general_status_and_progress_@_weather"},{"to_global_var":"g_general_weather"}]          
        ]
      
    }
  ]
}
```
1 : On place une variable de type String en variable global.

2 : on récupère la météo dans une source de donnée. Notez le   ```${area_uuid}``` qui permet de concaténer l'uuid du reporting directement dans le path. Ainsi vous pouvez podifier l'uuid du rapport sans avoir a changer
tous les path des variables.

Autre exemple :

```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "debug_mode": "true",
      "script": [
          [{"string":"384e85e8-3949-4dd5-aa1a-b47fb78ef013"},{"to_global_var":"area_uuid"}],
          [{"string":"méga top text"},{"to_global_var":"top_text"}],
          [{"string":"Spok${area_uuid}pipo max${top_text}toto"},{"to_global_var":"test"}],
          [{"log_debug":"${test} + ${top_text} + ${area_uuid}"}]
        ]
      
    }
  ]
}
```

Ici nous actifons l'affichage du mode debug. Par défaut, le mode débug est désactivé, cad que aucun affichage sera produit coté IHM.

### Utilisation du scripting

Il suffit d'ajouter une propriété **script** à un objet **tâche**.

Variables globale :

**disable_all_scripts** : si true alors les scrips sont désactivés.

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

**comment**
* Description : permet de mettre un commentaire. Ne fait rien de particulier, n'exécute aucune fonction.
* Exemple :  ```{"comment":"J'écris un comentaire pour commenter mon code"}```

**get**
* Description : récupère une variable. La récupération peut se faire à plusieurs niveaux.
	* Extraction de donnée : permet de chercher une donnée dans la source. Cette donnée est localisée grâce à un path. Ce path est par exemple : **programme1\_@\_comex\_@\_progress** . Ce path va récupérer la donnée progress dans le reporting comex du programme1. Dans la pratique, nous préférons utilise l'uuid du comex durectement pour éviter les problèmes de path lié au changement de structure du projet. Enfin, pour indiquer qu'il s'agit d'une extraction, il faut ajouter le suffixe **src_path:** au path. Le path serait donc : **src_path:457575-457\_@\_progress** . Notez que le séparateur de path est **\_@\_** .
	* Récupération d'une variable : il suffit de mettre le nom de la variable à récupérer.
* Exemple :  
	* Extraction de données : ```{"get":"src_path:uuidDuReporting_@_progress"}```
	* Récupération d'une variable normale : ```{"get":"nomDeLaVariable"}```

**integer**
* Description : récupère l'entier en paramètre
* Exemple :  ```{"integer":"25"}```

**string**
* Description : récupère la chaine de caractère en paramètre. Notez que vous pouvez utiliser ```${nom_de_variable}``` dans le paramètre pour concaténer directement la valeur de la variable dans la chaine.
* Exemple :  ```{"string":"Mon texte"}``` ou encore ```{"string":"Je m'apelle ${user_name}"}```

**log_error**
* Description : permet d'écrire dans le log d'erreur une information. Utile pour le débuggage.  Notez que vous pouvez utiliser ```${nom_de_variable}``` dans le paramètre pour concaténer directement la valeur de la variable dans la chaine.
* Exemple :  ```{"log_error":"Une erreur"}``` ou encore ```{"log_error":"Une erreur sur l'utilisateur  ${user_name}"}``` 

**to\_local\_var**
* Description : met la variable dans le pool de variable locale. Ces variables ne seront accessible que au sein de la tâche. Elles seront supprimée à la fin du tritement dela tâche
* Exemple :  ```{"to_local_var":"var1"}```

**to\_global\_var**
* Description : met la variable dans le pool de variables globales. Ces variables seront accessibles pour toutes les tâches suivante.
* Exemple :  ```{"to_global_var":"var1"}```

**get\_table**
* Description : Permet de récupéere les données de certaines variables extraites de la source de données, en particulier les tableau.
En effet si on extrait par exemple une source de données de type ```human_resources```, cette donnée possède une liste d'utilisateurs. mais également une référence
vers la série temporelle accumulée sur les rapports. Pour récupérer le tableau des utilisateurs, il font donc utiliser cette fonction
* Paramètre : pas de paramètre.
* Exemple :  dans l'exemple ci dessous, un récupère les leaders de la données source, puis on sélectionne le contenu qui est une liste d'utilisateurs puis on met cette liste en variable globale.
```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "script": [
           [{"get":"src_path:7817-785_@_project_general_data_@_leaders"},{"get_table":""},{"to_global_var":"g_general_leaders"}]
        ]
    }
  ]
}
```

L'utilisation de ```get_table``` est utile pour les extractions de type tableau. Quand il s'agit d'extraction de type texte, nombre, booléen, il n'est pas utile d'utiliser cette fonction.

**average**
* Description : permet de faire une moyenne des ligne de la variable.
* Paramètre :
	* Param 1 : nom de la colonne pour réaliser la moyenne. Peut être vide, mais doit être présent (eg : ""). Si le nom de la colonne est vide, alors, la fonction utilisera la première colonne du tableau pour faire la moyenne.
	* Param 2 : liste des variables que vous voulez ajouter pour faire la moyenne. Par exemple : "var1" en cas d'une variable. Pour plusieurs variable il suffit de continuer à les lister : "var1","var2"
* Exemple :
	* Cas d'utilisation de l'instruction en début de chaine : ```{"average":["col1","var1","var2"]}``` . Cette instruction réalise la moyenne sur la colonne **col1** des variables **var1** et **var2**
	* Moyenne d'une variable récupéré dans le pool : ```{"get":"var1"},{"average":""},{"to\_local\_var":"var2"}``` . Cette série d'instruction récupère la variable **var1** et ensuite calcule la moyenne sur la première colonne puis met le résultat en variable locale **var2**.
	* Calcule la moyenne de 50 et 25 ( (50+25)/2 ) et met le résultat dans var 3 ;

```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "script": [
          [{"integer":"25"},{"to_local_var":"var1"}],
          [{"integer":"50"},{"to_local_var":"var2"}],
          [{"average":["","var1","var2"]},{"to_local_var":"var3"}]
        ]
    }
  ]
}
```

### La section JSON BPM des widgets

Pour tous les widget il existe des variables par défaut :

**real_data** (true par défaut): indique si les données du widget sont des données par défaut ou des données réelles. Si c'est des données par défaut, alors l'affichage du widget affichera un message pour indiquer que les données ne sont
pas des données récupérés mais des données par défaut d'exemple.

Cette section permet de spécifier des valeurs pour certains paramètre des widgets que vous allez utiliser. Vous pourrez indiquer des couleurs, des valeurs, des tailles.

Dans l'ordre de priorité d'exécution des section BPM, les sections des widgets sont effectués en dernier, après le BPM général du dashboard.

Ce JSON BPM fonctionne de la même manière que celle de la section générale à la différence qu'il ne faut pas indiquer la propriété **"tasks"**. Ici nous allons directement dans la spécification des propriété du widget.

Exemple de JSON : 

```javascript
 {   
   "bar_color":"red",
   "bar_background_color":"pink",
   "script": [
          [{"integer":"1"},{"to_local_var":"var1"}],
          [{"integer":"1"},{"to_local_var":"var2"}],
          [{"integer":"0"},{"to_local_var":"var3"}],
          [{"average":["","var1","var2","var3"]},{"to_local_var":"bar_progress"}]
        ]
    
}
```

Ici nous allons customizer un widget de type **progress_bar**. Nous allons lui indiquer de mettre la barre en rouge et son background en rose. Nous pouvons également indiquer une section script qui permet de réaliser un calcul.

Autre exemple ou on récupère la progression directement à partir de la source de données:

```javascript
{   
   "bar_color":"red",
   "bar_background_color":"pink",
   "bar_progress": "src_path:d2548bd1-472a-441c-8dce-6681d6b7fe0f_@_2 - Avancement_@_progress"    
}
```

Ici, la progression est récupéré dirctement depuis la source en utilisant la progression présente dans le rapport **548645-847-4445** dans la section **2 - Avancement**.

Il est possible également de mettre une variable globale directement dans la valeur de la propriété : ```"bar_progress": "global_var:var1"``` . Ici la variable **var1** stockée en global sera utilisé pour la propriété **bar_progress**.



Exemple de script avec des if

```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "script": [
          [{"real":"86400000"},{"to_global_var":"g_day_in_msec"}],
          [{"real":"30"},{"multiply":"g_day_in_msec"},{"to_local_var":"very_late_limit_in_msec"}],
          [{"real":"15"},{"multiply":"g_day_in_msec"},{"to_local_var":"late_limit_in_msec"}],
          
          [{"comment":"En fonction des dates, on va mettre le flag on_time, late ou very_late"}],
          [{"if_time_def":["g_general_end_date","g_general_initial_end_date"]},{"substract":["g_general_end_date","g_general_initial_end_date"]},{"to_local_var":"dateDelta"},{"end_if":""}],
          
           [{"if_greater_than":["dateDelta","very_late_limit_in_msec"]},{"string":"very_late"},{"to_global_var":"g_general_flag_if"},{"else":""},{"if_greater_than":["dateDelta","late_limit_in_msec"]},{"string":"late"},{"to_global_var":"g_general_flag_if"},{"else":""},{"string":"on_time"},{"to_global_var":"g_general_flag_if"},{"end_if":""}]
        ]
    }
  ]
}
```

### La section JSON BPM des widgets