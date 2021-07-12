---
layout : docs_fr
id : a42vf3g5
readingEstimation : 15
---

## Widget RIDA
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

### Exemple JSON


Exemple de JSON à inclure dans le BPM du widget:

**JSON minimal**

```javascript
{
  "rida_table": {
    "columns": [
      {
        "name": "name",
        "values": [
          "rida1"
        ]
      },
      {
        "name": "rida",
        "values": [
          {
            
            "columns": [
              {
                "name": "risks",
                "values": [
                  {
                     "columns": [
                        {
                          "name": "uuid",
                          "values": [
                              "rsk1",
                              "rsk2"     
                              ]
                        },
                        {
                          "name": "uuid",
                          "values": [
                              "Risque 1",
                              "Risque 2"  
                              ]
                        }
                      ] 
                  }
                ]
              },
              {
                "name": "problems",
                "values": [
                  {
                     "columns": [
                        {
                          "name": "uuid",
                          "values": [
                              "pb1",
                              "pb2" 
                              ]
                        },
                        {
                          "name": "uuid",
                          "values": [
                              "Problème 1",
                              "Problème 2"   
                              ]
                        }
                      ] 
                  }
                ]
              }
            ]
          }
        ]
      }
    ]
  }
}
```


