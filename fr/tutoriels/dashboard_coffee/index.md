---
layout : docs_fr
id : 548rty45
readingEstimation : 15
---

## Infos pour Dashboard Coffee
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.orgn) 

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
