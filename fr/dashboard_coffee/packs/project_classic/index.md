---
layout : docs_fr
id : 88465er46
readingEstimation : 15
---

## BPM des widgets
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

Le principe est de créer des variables globales qui seront peuplé par le scripting. Il existera une variable qui sera l'UUID du plan de reporting de référence qui devra être modifié pour chaque plan.

### Liste des variables globales

**g_general_weather**

**g_general_progress**

**g_general_start_date**

**g_general_initial_end_date**

**g_general_end_date**

**g_general_flag_level**

### JSON général du dashboard

C'est ici que sera configuré l'uuid du reporting de référence ainsi que tous les scripts qui peuplerons les variables globales. Ces variables globales seront alos utilisé dans les widgets du dashboard.

```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "script": [
          [{"string":"384e85e8-3949-4dd5-aa1a-b47fb78ef013"},{"to_global_var":"g_reporting_area_uuid"}],
          [{"get":"src_path:project_general_status_and_progress_@_weather"},{"to_global_var":"g_general_weather"}],
          [{"get":"src_path:project_general_status_and_progress_@_progress"},{"to_global_var":"g_general_progress"}]
        ]
      
    }
  ]
}
```

### Progression générale du projet

```javascript
{      
      "weather_level":"global_var:g_general_weather",
      "progress":"global_var:g_general_progress",
      "start_date":"global_var:g_general_start_date",
      "end_date":"global_var:g_general_end_date",
      "initial_end_date":"global_var:g_general_initial_end_date",
      "flag_level":"global_var:g_general_flag_level"
}
```



