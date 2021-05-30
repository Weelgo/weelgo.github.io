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
      "debug_mode": "true",
      "script": [
          [{"comment":"On met en variable l'uuid du reporting area"}],
          [{"string":"384e85e8-3949-4dd5-aa1a-b47fb78ef013"},{"to_global_var":"area_uuid"}],
          
          [{"get":"src_path:${area_uuid}_@_project_general_status_and_progress_@_weather"},{"to_global_var":"g_general_weather"}],
          [{"get":"src_path:${area_uuid}_@_project_general_status_and_progress_@_progress"},{"to_global_var":"g_general_progress"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data_@_start_date"},{"to_global_var":"g_general_start_date"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data_@_end_date"},{"to_global_var":"g_general_end_date"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data_@_initial_end_date"},{"to_global_var":"g_general_initial_end_date"}],
          [{"get":"src_path:${area_uuid}_@_project_general_data_@_leaders"},{"get_table":""},{"to_global_var":"g_general_leaders"}],
          
          
          [{"real":"86400000"},{"to_global_var":"g_day_in_msec"}],
          [{"real":"30"},{"multiply":"g_day_in_msec"},{"to_local_var":"very_late_limit_in_msec"}],
          [{"real":"15"},{"multiply":"g_day_in_msec"},{"to_local_var":"late_limit_in_msec"}],
          
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
          [{"get":"src_path:${area_uuid}_@_budget_@_summary"},{"create_simple_budget_line_chart_datasets_from_time_series":["#{Total}","#{Engagé}","#{A Engager}","#{situation}"]},{"to_global_var":"g_budget_timeseries"}],
          
          
          [{"get":"src_path:${area_uuid}_@_project_phases"},{"calculate_delay_flag":["very_late_limit_in_msec","late_limit_in_msec"]},{"to_global_var":"g_project_phases"}],
          [{"get":"g_project_phases"},{"get_current_phase":""},{"to_global_var":"g_current_phase"}],
          [{"get":"g_current_phase"},{"get_cell":"name"},{"to_global_var":"g_current_phase_name"}],
          [{"get":"g_current_phase"},{"get_cell":"weather"},{"to_global_var":"g_current_phase_weather"}],
          [{"get":"g_current_phase"},{"get_cell":"progress"},{"to_global_var":"g_current_phase_progress"}],
          [{"get":"g_current_phase"},{"get_cell":"start_date"},{"to_global_var":"g_current_phase_start_date"}],
          [{"get":"g_current_phase"},{"get_cell":"end_date"},{"to_global_var":"g_current_phase_end_date"}],
          [{"get":"g_current_phase"},{"get_cell":"initial_end_date"},{"to_global_var":"g_current_phase_initial_end_date"}],
          [{"get":"g_current_phase"},{"get_cell":"leaders"},{"to_global_var":"g_current_phase_leaders"}],
          [{"get":"g_current_phase"},{"get_cell":"flag_level"},{"to_global_var":"g_current_phase_flag"}],
          
          [{"get":"src_path:${area_uuid}_@_synthesis_@_covered_topics"},{"to_global_var":"g_covered_topics"}],
          [{"get":"src_path:${area_uuid}_@_synthesis_@_significant_events"},{"to_global_var":"g_significant_events"}],
           
          [{"get":"src_path:${area_uuid}_@_customer_relationship_@_nb_requests"},{"to_global_var":"g_customer_satisfaction_nb_requests"}],
          [{"get":"src_path:${area_uuid}_@_customer_relationship_@_nb_requests_done"},{"to_global_var":"g_customer_satisfaction_nb_requests_done"}],
          [{"get":"src_path:${area_uuid}_@_customer_relationship_@_nb_requests_to_do"},{"to_global_var":"g_customer_satisfaction_nb_requests_to_do"}],
          
          [{"create_table":""},{"set_into_cell":["#{0}","uuid","#{Demandes réalisées}"]},{"set_into_cell":["#{0}","value","g_customer_satisfaction_nb_requests_done"]},{"to_global_var":"g_customer_satisfaction_pie_chart"}],
          [{"get":"g_customer_satisfaction_pie_chart"},{"set_into_cell":["#{1}","uuid","#{Demandes restantes}"]},{"set_into_cell":["#{1}","value","g_customer_satisfaction_nb_requests_to_do"]}],
          
          [{"log_debug":"General weather : ${g_general_weather}"}],
          [{"log_debug":"General progress : ${g_general_progress}"}],
          [{"log_debug":"General flag : ${g_general_flag}"}],
          [{"log_debug":"Customer satisfaction : ${g_customer_satisfaction}"}],
          [{"log_debug":"Budget status : ${g_budget_status}"}],
          [{"log_debug":"Planning status : ${g_planning_status}"}],
          [{"log_debug":"Team status : ${g_team_status}"}],
          [{"log_debug":"Total budget : ${g_budget_total}"}],
          [{"log_debug":"Committed budget : ${g_budget_committed}"}],
          [{"log_debug":"To commit budget : ${g_budget_to_commit}"}],
          [{"log_debug":"current phase name : ${g_current_phase_name}"}],
          [{"log_debug":"current phase weather : ${g_current_phase_weather}"}],
          [{"log_debug":"current phase progress : ${g_current_phase_progress}"}],
          [{"log_debug":"current phase start date : ${g_current_phase_start_date}"}],
          [{"log_debug":"current phase end date : ${g_current_phase_end_date}"}],
          [{"log_debug":"current phase initial end date : ${g_current_phase_initial_end_date}"}],
          [{"log_debug":"current phase flag : ${g_current_phase_flag}"}]
          
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



