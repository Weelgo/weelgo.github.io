---
layout : docs_fr
id : 88465er46
readingEstimation : 15
---

## Widget Résumé du budget
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON

Exemple de JSON à inclure dans le BPM général:

```javascript
{
  "uuid": "Budget",
  "type": "budget_summary_widget",
  "widget_uuid": "uuid du widget à récupéré dans l'IHM",
  "total_budget": "250000",
  "committed_budget": "100000",
  "to_commit_budget": "120000"
}
```

Exemple de JSON à inclure dans le BPM du widget:

```javascript
{
  "total_budget": "250000",
  "committed_budget": "100000",
  "to_commit_budget": "120000"
}
```

### Propriétés du widget

**uuid** (utilisé **uniquement** pour PBM général) 
* Description : identifiant de la tâche, au choix de l'utilisateur.
* Valeurs possibles : valeur au choix de l'utilisateur. **Ne doit pas être le même qu'une autre tâche du BPM.**
* Exemple : ```"uuid":"Ma budget"```

**type** (utilisé **uniquement** pour PBM général) 
* Description : identifiant permettant au moteur de calcule de savoir que la tâche est du type indiqué.
* Valeurs possibles : budget_summary_widget 
* Exemple : ```"type":"budget_summary_widget"```

**widget_uuid** (utilisé **uniquement** pour PBM général) 
* Description : Uuid du widget ciblé par la tâche
* Valeurs possibles : L'uuid du widget est affiché dans les propriété du widget dans l'IHM. 
* Exemple : ```"widget_uuid":"F5441C4C-BEFF-4E92-B7F3-308DA0"```

**total_budget** (obligatoire)
* Description : budget total.
* Valeurs possibles : nombre réel.
* Exemple : ```"total_budget":"2000000"```

**committed_budget** (obligatoire)
* Description : budget engagé.
* Valeurs possibles : nombre réel.
* Exemple : ```"committed_budget":"50000"```

**to_commit_budget** (obligatoire)
* Description : budget à engager.
* Valeurs possibles : nombre réel.
* Exemple : ```"to_commit_budget":"20000"```

**show_chart**
* Description : affiche le bar chart.
* Valeurs possibles : **true** \| false 
* Exemple : ```"show_chart":"false"```

**show_numbers**
* Description : affiche le tableau des chiffres.
* Valeurs possibles : **true** \| false 
* Exemple : ```"show_numbers":"false"```

**currency**
* Description : devise des montants affichés.
* Valeurs possibles : texte libre
* Exemple : ```"currency":"EUR"```

**currency_first**
* Description : indique d'afficher la devise avant le nombre, par exemple $250 000.
* Valeurs possibles : true \| **false**
* Exemple : ```"currency_first":"true"```


