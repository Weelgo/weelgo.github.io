---
layout : docs_fr
id : 88465er46
readingEstimation : 15
---

## BPM des widgets
------------------------

Lien vers un éditeur JSON en ligne : [cliquez ici](https://jsoneditoronline.org) 

Lien vers le fichier JSON qu'il est possible de copier directement dans le dashboard : [cliquez ici](project_classic_board.json)


### JSON général du dashboard

C'est ici que sera configuré l'uuid du reporting de référence ainsi que tous les scripts qui peuplerons les variables globales. Ces variables globales seront alos utilisé dans les widgets du dashboard.

```javascript
{
  "tasks": [
    {
      "uuid": "main",
      "debug_mode": "false",
      "script": [
          [{"comment":"On met en variable l'uuid du reporting area"}],
          [{"string":"6e6d0356-cfd4-4bf9-a2bc-aac2cbe7ff2a"},{"to_global_var":"area_uuid"}],
          
          [{"if_variable_exists":"src_path:${area_uuid}_@_timetables"},{"boolean":"false"},{"to_global_var":"disable_all_scripts"},{"else":""},{"boolean":"true"},{"to_global_var":"disable_all_scripts"},{"break":""},{"end_if":""}],
          
          [{"get":"src_path:${area_uuid}_@_project_general_status_and_progress_@_weather"},{"to_global_var":"g_general_weather"}],
          [{"get":"src_path:${area_uuid}_@_project_general_status_and_progress_@_progress"},{"to_global_var":"g_general_progress"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data_@_start_date"},{"to_global_var":"g_general_start_date"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data_@_end_date"},{"to_global_var":"g_general_end_date"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data_@_initial_end_date"},{"to_global_var":"g_general_initial_end_date"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data_@_leaders"},{"get_table":""},{"to_global_var":"g_general_leaders"},{"to_global_var":"page_leaders"}],
          
          [{"real":"30"},{"multiply":"#{86400000}"},{"to_local_var":"very_late_limit_in_msec"}],
          [{"real":"15"},{"multiply":"#{86400000}"},{"to_local_var":"late_limit_in_msec"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data"},{"calculate_delay_flag":["very_late_limit_in_msec","late_limit_in_msec"]},{"get_cell":"flag_level"},{"to_global_var":"g_general_flag"}],
          
          [{"get":"src_path:${area_uuid}_@_customer_relationship_@_customer_satisfaction"},{"to_global_var":"g_customer_satisfaction"}],
          [{"get":"src_path:${area_uuid}_@_budget_@_status"},{"to_global_var":"g_budget_status"}],
          [{"get":"src_path:${area_uuid}_@_planning_status"},{"to_global_var":"g_planning_status"}],
          [{"get":"src_path:${area_uuid}_@_team_@_mood"},{"to_global_var":"g_team_status"}],
          
          [{"string":"Date de fin"},{"to_local_var":"l_end_date_name"}],
          [{"create_line_chart_datasets_from_time_series":["g_general_end_date","l_end_date_name"]},{"to_global_var":"g_general_end_date_time_series_dataset"}],
          
          [{"get":"src_path:${area_uuid}_@_budget_@_summary_@_total_budget"},{"to_global_var":"g_budget_total"}],
          [{"get":"src_path:${area_uuid}_@_budget_@_summary_@_committed_budget"},{"to_global_var":"g_budget_committed"}],
          [{"get":"src_path:${area_uuid}_@_budget_@_summary_@_to_commit_budget"},{"to_global_var":"g_budget_to_commit"}],
          [{"get":"src_path:${area_uuid}_@_budget_@_summary_@_situation"},{"to_global_var":"g_budget_situation"}],
          [{"get":"src_path:${area_uuid}_@_budget_@_summary"},{"create_simple_budget_line_chart_datasets_from_time_series":["#{Total}","#{Engagé}","#{A Engager}","#{situation}"]},{"to_global_var":"g_budget_timeseries"}],
          
          [{"string":"#2f3433"},{"to_global_var":"g_budget_total_color"}],
          [{"string":"#1db9db"},{"to_global_var":"g_budget_committed_color"}],
          [{"string":"#cccccc"},{"to_global_var":"g_budget_to_commit_color"}],
          [{"string":"#41c057"},{"to_global_var":"g_budget_situation_color"}],
          
          [{"if_greater_than_or_equal_to":["g_budget_situation","#{0}"]},{"string":"#41c057"},{"to_global_var":"g_budget_situation_color"},{"else":""},{"string":"#f92423"},{"to_global_var":"g_budget_situation_color"},{"end_if":""}],
          
          [{"get":"g_budget_timeseries"},{"set_into_cell":["#{0}","#{border_color}","g_budget_total_color"]},{"set_into_cell":["#{1}","#{border_color}","g_budget_committed_color"]},{"set_into_cell":["#{2}","#{border_color}","g_budget_to_commit_color"]},{"set_into_cell":["#{3}","#{border_color}","g_budget_situation_color"]}],
          
          
          [{"get":"src_path:${area_uuid}_@_project_phases"},{"calculate_delay_flag":["very_late_limit_in_msec","late_limit_in_msec"]},{"to_global_var":"g_project_phases"}],
          [{"get":"g_project_phases"},{"get_current_phase":""},{"to_global_var":"g_current_phase"}],
          [{"get":"g_current_phase"},{"get_cell":"name"},{"to_global_var":"g_current_phase_name"}],
          [{"get":"g_current_phase"},{"get_cell":"weather"},{"to_global_var":"g_current_phase_weather"}],
          [{"get":"g_current_phase"},{"get_cell":"progress"},{"to_global_var":"g_current_phase_progress"}],
          [{"get":"g_current_phase"},{"get_cell":"start_date"},{"to_global_var":"g_current_phase_start_date"}],
          [{"get":"g_current_phase"},{"get_cell":"end_date"},{"to_global_var":"g_current_phase_end_date"}],
          [{"get":"g_current_phase"},{"get_cell":"initial_end_date"},{"to_global_var":"g_current_phase_initial_end_date"}],
          [{"get":"g_current_phase"},{"get_cell":"leaders"},{"get_table":""},{"to_global_var":"g_current_phase_leaders"}],
          [{"get":"g_current_phase"},{"get_cell":"flag_level"},{"to_global_var":"g_current_phase_flag"}],
          
          [{"get":"src_path:${area_uuid}_@_synthesis_@_covered_topics"},{"get_table":""},{"to_global_var":"g_covered_topics"}],
          [{"get":"src_path:${area_uuid}_@_synthesis_@_significant_events"},{"get_table":""},{"to_global_var":"g_significant_events"}],
          
          [{"get":"src_path:${area_uuid}_@_customer_relationship_@_nb_requests"},{"to_global_var":"g_customer_satisfaction_nb_requests"}],
          [{"get":"src_path:${area_uuid}_@_customer_relationship_@_nb_requests_done"},{"to_global_var":"g_customer_satisfaction_nb_requests_done"}],
          [{"get":"g_customer_satisfaction_nb_requests"},{"substract":"g_customer_satisfaction_nb_requests_done"},{"to_global_var":"g_customer_satisfaction_nb_requests_to_do"}],
          
          [{"create_table":""},{"set_into_cell":["#{0}","#{uuid}","#{Demandes réalisées} : ${g_customer_satisfaction_nb_requests_done}"]},{"set_into_cell":["#{0}","#{value}","g_customer_satisfaction_nb_requests_done"]},{"to_global_var":"g_customer_satisfaction_pie_chart"}],
          [{"get":"g_customer_satisfaction_pie_chart"},{"set_into_cell":["#{1}","#{uuid}","#{Demandes restantes} : ${g_customer_satisfaction_nb_requests_to_do}"]},{"set_into_cell":["#{1}","#{value}","g_customer_satisfaction_nb_requests_to_do"]}],
          
          [{"string":"#2f3433"},{"to_global_var":"g_planned_workload_color"}],
          [{"string":"#1db9db"},{"to_global_var":"g_workload_done_color"}],
          [{"string":"#cccccc"},{"to_global_var":"g_workload_to_do_color"}],
          [{"string":"#41c057"},{"to_global_var":"g_workload_situation_color"}],
          
          [{"get":"src_path:${area_uuid}_@_workload_plan_@_planned_workload"},{"to_global_var":"g_planned_workload"}],
          [{"get":"src_path:${area_uuid}_@_workload_plan_@_workload_done"},{"to_global_var":"g_workload_done"}],
          [{"get":"src_path:${area_uuid}_@_workload_plan_@_workload_to_do"},{"to_global_var":"g_workload_to_do"}],
          [{"get":"g_planned_workload"},{"substract":"g_workload_done"},{"substract":"g_workload_to_do"},{"to_global_var":"g_workload_situation"}],
          
          [{"if_greater_than_or_equal_to":["g_workload_situation","#{0}"]},{"string":"#41c057"},{"to_global_var":"g_workload_situation_color"},{"else":""},{"string":"#f92423"},{"to_global_var":"g_workload_situation_color"},{"end_if":""}],
          
          [{"get":"g_planned_workload"},{"create_line_chart_datasets_from_time_series":"#{Charge planifiée}"},{"set_into_cell":["#{0}","#{border_color}","g_planned_workload_color"]},{"to_global_var":"g_planned_workload_timeseries"}],
          [{"get":"g_workload_done"},{"create_line_chart_datasets_from_time_series":"#{Charge consommée}"},{"set_into_cell":["#{0}","#{border_color}","g_workload_done_color"]},{"to_global_var":"g_workload_done_timeseries"}],
          [{"get":"g_workload_to_do"},{"create_line_chart_datasets_from_time_series":"#{Reste à faire}"},{"set_into_cell":["#{0}","#{border_color}","g_workload_to_do_color"]},{"to_global_var":"g_workload_to_do_timeseries"}],
          
          [{"combine_variables":["g_planned_workload_timeseries","g_workload_done_timeseries","g_workload_to_do_timeseries"]},{"to_global_var":"g_workload_timeseries"}],
          
          [{"get":"src_path:${area_uuid}_@_workload_plan_@_nb_tasks"},{"to_global_var":"g_nb_tasks"}],
          [{"get":"src_path:${area_uuid}_@_workload_plan_@_nb_tasks_done"},{"to_global_var":"g_nb_tasks_done"}],
          [{"get":"g_nb_tasks"},{"substract":"g_nb_tasks_done"},{"to_global_var":"g_nb_tasks_to_do"}],
          
          [{"create_table":""},{"set_into_cell":["#{0}","#{uuid}","#{Nb tâches réalisées} : ${g_nb_tasks_done}"]},{"set_into_cell":["#{0}","#{value}","g_nb_tasks_done"]},{"to_global_var":"g_tasks_pie_chart"}],
          [{"get":"g_tasks_pie_chart"},{"set_into_cell":["#{1}","#{uuid}","#{Nb tâches restantes} : ${g_nb_tasks_to_do}"]},{"set_into_cell":["#{1}","#{value}","g_nb_tasks_to_do"]}],
          
          [{"get":"src_path:${area_uuid}_@_project_roadmap"},{"to_global_var":"g_project_roadmap"}],
          
          [{"log_debug":"Fin"}]
          
        ]
      
    }
  ]
}
```
## BPM des widgets

### Progression générale du projet

```javascript
{
  "weather_level":"weather_sun",
  "progress":"0.1",
  "start_date":"1610409600000",
  "end_date":"1611964800000",
  "initial_end_date":"1611532800000",
  "flag_level":"on_time",
  "real_data":"false",
  "script": [
      [{"get":"g_general_weather"},{"to_local_var":"weather_level"}],
      [{"get":"g_general_progress"},{"to_local_var":"progress"}],
      [{"get":"g_general_start_date"},{"to_local_var":"start_date"}],
      [{"get":"g_general_end_date"},{"to_local_var":"end_date"}],
      [{"get":"g_general_initial_end_date"},{"to_local_var":"initial_end_date"}],
      [{"get":"g_general_flag"},{"to_local_var":"flag_level"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Météo satisfaction client

```javascript
{
  "weather_level":"weather_sun",
  "weather_type":"smiley",
  "image_height":"35px",
  "image_width":"35px",
  "real_data":"false",
  "script": [
      [{"get":"g_customer_satisfaction"},{"to_local_var":"weather_level"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Météo situation financière

```javascript
{
  "weather_level":"weather_sun",
  "weather_type":"weather",
  "image_height":"45px",
  "image_width":"45px",
  "real_data":"false",
  "script": [
      [{"get":"g_budget_status"},{"to_local_var":"weather_level"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Météo planning

```javascript
{
  "weather_level":"weather_sun",
  "weather_type":"weather",
  "image_height":"45px",
  "image_width":"45px",
  "real_data":"false",
  "script": [
      [{"get":"g_planning_status"},{"to_local_var":"weather_level"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Météo équipe

```javascript
{
  "weather_level":"weather_sun",
  "weather_type":"weather",
  "image_height":"45px",
  "image_width":"45px",
  "real_data":"false",
  "script": [
      [{"get":"g_team_status"},{"to_local_var":"weather_level"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Droite 45 générale

```javascript
{
  "chart_height":"190px",
  "chart_width":"484px",
  "date_date_curve":"true",
  "x_axes": {
    "columns": [
      {
        "name": "type",
        "values": [
          "time_series"
        ]
      }
    ]
  },
  "y_axes": {
    "columns": [
      {
        "name": "type",
        "values": [
          "time_series"
        ]
      }
    ]
  },
  "datasets": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Date de fin"
        ]
      },
      {
        "name": "point_radius",
        "values": [
          "2"
        ]
      },
      {
        "name": "values2d",
        "values": [
          [["1609459200000","1611100800000"],["1609545600000","1611100800000"],["1609632000000","1611100800000"],["1609718400000","1611532800000"],["1609804800000","1611532800000"],["1610841600000","1611532800000"]]
        ]
      }
    ]
  },
  "real_data":"false",
  "script": [
      [{"get":"g_general_end_date_time_series_dataset"},{"to_local_var":"datasets"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Budget

```javascript
{
  "total_budget": "250000",
  "committed_budget": "100000",
  "to_commit_budget": "120000",
  "real_data":"false",
  "script": [
      [{"get":"g_budget_total"},{"to_local_var":"total_budget"}],
      [{"get":"g_budget_committed"},{"to_local_var":"committed_budget"}],
      [{"get":"g_budget_to_commit"},{"to_local_var":"to_commit_budget"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Phase en cours

```javascript
{
  "weather_level":"weather_sun",
  "progress":"0.35",
  "flag_level":"on_time",
  "phase_name":"Phase 1",
  "start_date":"1610236800000",
  "end_date":"1613779200000",
  "initial_end_date":"1613779200000",
  "leaders":{
    "columns": [
      {
        "name": "name",
        "values": [          
            "Paul Dupond"          
        ]
      },
      {
        "name": "uuid",
        "values": [          
            "54654-465484-46546"          
        ]
      }
    ]
  },
  "real_data":"false",
  "script": [
      [{"get":"g_current_phase_weather"},{"to_local_var":"weather_level"}],
      [{"get":"g_current_phase_progress"},{"to_local_var":"progress"}],
      [{"get":"g_current_phase_flag"},{"to_local_var":"flag_level"}],
      [{"get":"g_current_phase_name"},{"to_local_var":"phase_name"}],
      [{"get":"g_current_phase_start_date"},{"to_local_var":"start_date"}],
      [{"get":"g_current_phase_end_date"},{"to_local_var":"end_date"}],
      [{"get":"g_current_phase_initial_end_date"},{"to_local_var":"initial_end_date"}],
      [{"get":"g_current_phase_leaders"},{"to_local_var":"leaders"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}

```

### Tableau des phases
```javascript
{
  "progress":"0.2",
  "phases":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Phase 1",
          "Phase 2",
          "Phase 3",
          "Phase 4"
        ]
      },
      {
        "name": "progress",
        "values": [
          "1",
          "0.2",
          "0",
          "0"
        ]
      },
      {
        "name": "weather",
        "values": [
          "weather_cloudy ",
          "weather_rain",
          "weather_sun",
          "weather_sun"
        ]
      }
    ]
  },
  "real_data":"false",
  "script": [
      [{"get":"g_general_progress"},{"to_local_var":"progress"}],
      [{"get":"g_project_phases"},{"to_local_var":"phases"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Sujets abordés
```javascript
{
  "topics":{
    "columns": [
      {
        "name": "name",
        "values": [
          "Sujet important 1",
          "Sujet important 2",
          "Sujet important 3"
        ]
      },
      {
        "name": "description",
        "values": [
          "Description sujet 1",
          "",
          "Description sujet 3"
        ]
      }
    ]
  },
  "real_data":"false",
  "script": [
      [{"get":"g_covered_topics"},{"to_local_var":"topics"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Evènements significatifs
```javascript
{
  "events": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Evènement 1",
          "Evènement 2"
        ]
      },
      {
        "name": "description",
        "values": [
          "Description évènement 1",
          "Description *évènement 2*"
        ]
      },
      {
        "name": "icon",
        "values": [
          "ic_diamond_solid",
          "ic_exclamation_circle_solid"
        ]
      },
      {
        "name": "event_date",
        "values": [
          "1638316800000",
          "1610409600000"
        ]
      }
    ]
  },
  "real_data":"false",
  "script": [
      [{"get":"g_significant_events"},{"to_local_var":"events"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Camembert relation client
```javascript
{
  "legend_position":"right",
  "pie_height":"70px",
  "pie_width":"70px",
  "datasets":{
    "columns": [
      {
        "name": "uuid",
        "values": [
          "Demandes réalisées : 50",
          "Demandes restantes : 30"
        ]
      },
      {
        "name": "value",
        "values": [
          "50",
          "30"
        ]
      }
    ]
  } ,
  "real_data":"false",
  "script": [
      [{"get":"g_customer_satisfaction_pie_chart"},{"to_local_var":"datasets"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Nb total demande relation client
```javascript
{
  "text":"80",
  "prefix":"Nb total de demandes :",
  "prefix_gap":"true",
  "format_type":"number",
  "real_data":"false",
  "script": [
      [{"get":"g_customer_satisfaction_nb_requests"},{"to_local_var":"text"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Budget 2 (dans artie détail)

```javascript
{
  "total_budget": "250000",
  "committed_budget": "100000",
  "to_commit_budget": "120000",
  "show_chart":"false",
  "real_data":"false",
  "script": [
      [{"get":"g_budget_total"},{"to_local_var":"total_budget"}],
      [{"get":"g_budget_committed"},{"to_local_var":"committed_budget"}],
      [{"get":"g_budget_to_commit"},{"to_local_var":"to_commit_budget"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Budget graphe (dans artie détail)

```javascript
{
  "chart_height":"160px",
  "chart_width":"360px",
  "show_legend":"false",
  "x_axes": {
    "columns": [
      {
        "name": "type",
        "values": [
          "time_series"
        ]
      }
    ]
  },
  "datasets": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Total",
          "Engagé",
          "A Engager",
          "Situation"
        ]
      },
      {
        "name": "border_color",
        "values": [
          "#2f3433",
          "#1db9db",
          "#cccccc",
          "#41c057"
        ]
      },
      {
        "name": "values2d",
        "values": [
          [["1609459200000","100000"],["1609545600000","120000"],["1609632000000","150000"]],
          [["1609459200000","60000"],["1609545600000","60000"],["1609632000000","70000"]],
          [["1609459200000","20000"],["1609545600000","20000"],["1609632000000","40000"]],
          [["1609459200000","20000"],["1609545600000","60000"],["1609632000000","40000"]]
        ]
      }
    ]
  },
  "real_data":"false",
  "script": [
      [{"get":"g_budget_timeseries"},{"to_local_var":"datasets"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Charge planifiée

```javascript
{
  "text":"300",
  "suffix":"J/H",
  "suffix_gap":"true",
  "format_type":"number",
  "real_data":"false",
  "script": [
      [{"get":"g_planned_workload"},{"to_local_var":"text"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Charge consommée

```javascript
{
  "text":"170",
  "suffix":"J/H",
  "suffix_gap":"true",
  "format_type":"number",
  "real_data":"false",
  "script": [
      [{"get":"g_workload_done"},{"to_local_var":"text"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Charge reste à faire

```javascript
{
  "text":"200",
  "suffix":"J/H",
  "suffix_gap":"true",
  "format_type":"number",
  "real_data":"false",
  "script": [
      [{"get":"g_workload_to_do"},{"to_local_var":"text"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Charge situation

```javascript
{
  "text":"-70",
  "text_color":"red",
  "suffix":"J/H",
  "suffix_gap":"true",
  "format_type":"number",
  "real_data":"false",
  "script": [
      [{"get":"g_workload_situation"},{"to_local_var":"text"}],
      [{"get":"g_workload_situation_color"},{"to_local_var":"text_color"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Charge graphe

```javascript
{
  "chart_height":"160px",
  "chart_width":"360px",
  "show_legend":"true",
  "x_axes": {
    "columns": [
      {
        "name": "type",
        "values": [
          "time_series"
        ]
      }
    ]
  },
  "datasets": {
    "columns": [
      {
        "name": "name",
        "values": [
          "Planifié",
          "Consommé",
          "Reste à faire"
        ]
      },
      {
        "name": "border_color",
        "values": [
          "#2f3433",
          "#1db9db",
          "#cccccc"
        ]
      },
      {
        "name": "values2d",
        "values": [
          [["1609459200000","200"],["1609545600000","250"],["1609632000000","300"]],
          [["1609459200000","100"],["1609545600000","110"],["1609632000000","170"]],
          [["1609459200000","70"],["1609545600000","100"],["1609632000000","200"]]          
        ]
      }
    ]
  },
  "real_data":"false",
  "script": [
      [{"get":"g_workload_timeseries"},{"to_local_var":"datasets"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Camembert nb tâches
```javascript
{
  "legend_position":"right",
  "pie_height":"70px",
  "pie_width":"70px",
  "datasets":{
    "columns": [
      {
        "name": "uuid",
        "values": [
          "Nb tâches réalisées : 30",
          "Nb tâches restantes : 10"
        ]
      },
      {
        "name": "value",
        "values": [
          "30",
          "10"
        ]
      }
    ]
  } ,
  "real_data":"false",
  "script": [
      [{"get":"g_tasks_pie_chart"},{"to_local_var":"datasets"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Nb total de tâches
```javascript
{
  "text":"40",
  "prefix":"Nb total de tâches :",
  "prefix_gap":"true",
  "format_type":"number",
  "real_data":"false",
  "script": [
      [{"get":"g_nb_tasks"},{"to_local_var":"text"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}
```

### Roadmap
```javascript
{
 "width":"960px",
  "lines": {
    "columns": [
      {
        "name": "uuid",
        "values": [
          "gp1",
          "ph1",
          "ml1",
          "gp2"
        ]
      },
      {
        "name": "name",
        "values": [
          "Groupe 1",
          "Phase 1",
          "Jalon 1",
          "Groupe 2"
        ]
      },
      {
        "name": "parent_uuid",
        "values": [
          "",
          "gp1",
          "gp2",
          "gp1"
        ]
      },
      {
        "name": "object_type",
        "values": [
          "group",
          "phase",
          "milestone",
          "group"
        ]
      },
      {
        "name": "background_color",
        "values": [
          "#ff4da6",
          "#9e1fff",
          "#009e9e",
          "#e0e000"
        ]
      },
      {
        "name": "start_date",
        "values": [
          "",
          "1609804800000",
          "",
          ""
        ]
      },
      {
        "name": "end_date",
        "values": [
          "",
          "1611100800000",
          "1611100800000",
          ""
        ]
      },
      {
        "name": "icon",
        "values": [
          "",
          "",
          "ic_diamond_solid",
          ""
        ]
      }
    ]
  },
  "real_data":"false",
  "script": [
      [{"get":"g_project_roadmap"},{"to_local_var":"lines"}],
      [{"boolean":"true"},{"to_local_var":"real_data"}]
    ]
}

```

