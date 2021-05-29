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



