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
        "name": "risk_categories",
        "values": [
          {
               "columns": [
                  {
                    "name": "name",
                    "values": [
                        "Risque financier",
                        "Risque humain",
                        "Risque temporel",
                        "Risque technique",
                        "Risque juridique",
                        "Risque environnemental",
                        "Risque organisationnel"
                        ]
                  }                  
              ] 
            }
        ]
      },
      {
        "name": "problem_categories",
        "values": [
          {
               "columns": [
                  {
                    "name": "name",
                    "values": [
                        "Problème financier",
                        "Problème humain",
                        "Problème temporel",
                        "Problème technique",
                        "Problème juridique",
                        "Problème environnemental",
                        "Problème organisationnel"
                        ]
                  }                  
              ] 
            }
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
                              "rsk2",
                              "rsk3"
                              ]
                        },
                        {
                          "name": "name",
                          "values": [
                              "Risque 1",
                              "Risque 2",
                              "Risque 3"
                              ]
                        },
                        {
                          "name": "category",
                          "values": [
                              "Risque humain",
                              "Risque juridique",
                              "Risque financier"
                              ]
                        },
                        {
                          "name": "origin",
                          "values": [
                              "internal",
                              "internal",
                              "external"
                              ]
                        },
                        {
                          "name": "status",
                          "values": [
                              "closed",
                              "open",
                              "open"
                              ]
                        },
                        {
                          "name": "impact",
                          "values": [
                              "medium",
                              "critical",
                              "serious"
                              ]
                        },
                        {
                          "name": "probability",
                          "values": [
                              "probable",
                              "probable",
                              "very_probable"
                              ]
                        },
                        {
                          "name": "priority",
                          "values": [
                              "high",
                              "very_high",
                              "very_high"
                              ]
                        },
                        {
                          "name": "strategy",
                          "values": [
                              "transfer",
                              "elimination",
                              "reduction"
                              ]
                        },
                        {
                          "name": "closing_date",
                          "values": [
                              "1635984000000",
                              "1633824000000",
                              "1632528000000"
                              ]
                        },
                        {
                          "name": "leaders",
                          "values": [
                              {
                                 "columns": [
                                    {
                                      "name": "name",
                                      "values": [
                                          "Sophie Ouellet"
                                          ]
                                    }
                                  ] 
                              },
                              {
                                 "columns": [
                                    {
                                      "name": "name",
                                      "values": [
                                          "Mireille Therrien"
                                          ]
                                    }
                                  ] 
                              },
                              {
                                 "columns": [
                                    {
                                      "name": "name",
                                      "values": [
                                          "Benjamin Plante"
                                          ]
                                    }
                                  ] 
                              }
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
                          "name": "name",
                          "values": [
                              "Problème 1",
                              "Problème 2"   
                              ]
                        },
                        {
                          "name": "category",
                          "values": [
                              "Problème technique",
                              "Problème environnemental"
                              ]
                        },
                        {
                          "name": "status",
                          "values": [
                              "closed",
                              "open"
                              ]
                        },
                        {
                          "name": "impact",
                          "values": [
                              "low",
                              "serious"
                              ]
                        },
                        {
                          "name": "priority",
                          "values": [
                              "low",
                              "high"
                              ]
                        },
                        {
                          "name": "closing_date",
                          "values": [
                              "1635984000000",
                              "1633824000000"
                              ]
                        },
                        {
                          "name": "leaders",
                          "values": [
                              {
                                 "columns": [
                                    {
                                      "name": "name",
                                      "values": [
                                          "Sophie Ouellet"
                                          ]
                                    }
                                  ] 
                              },
                              {
                                 "columns": [
                                    {
                                      "name": "name",
                                      "values": [
                                          "Mireille Therrien"
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
        ]
      }
    ]
  }
}
```


