+++
title = "The yaml file"
chapter = false
weight = 32
draft = false
+++

### Yaml file purpose

```yaml
status: "{{ status }}"
created_date: "{{ created_date }}"
last_updated_date: 
name: "{{ detection_name }}"
query: "{{ query }}"
author: "{{ detection_author }}"
schedule: "{{ schedule }}"
baseline: "{{ baseline }}"
visualization: "{{ visualization }}"
event_limit: 0
data_source: "{{ data_source }}"
data_location: "{{ data_source }}"
tactic: "{{ tactic }}"
mitre_id: "{{ mitre_id }}"
mitre_url: "{{ mitre_url }}"
incident:
  severity: "numeric, 0-unknown, 0.5 - informational, 1-low,2-medium,3-high,4-critical"
  type: 'Security Incident'
  name: 'string, name of the incident' 
  description: 'inc descr: This detection is monitoring for changes in any of X'
  sla: 'integer - number of minutes added to incident create time(incident sla). example sla: 1440 this means 24h sla'
  ```