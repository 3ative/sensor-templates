# Template Sensor of Unavailable Sensors

Split your configuration file?, then use this (as shown in my tutorial):
```yaml
- platform: template
  sensors:
    octo_percentage:
      friendly_name: "Octo Print %"
      value_template: >-
        {% if (states('sensor.octoprint_job_percentage')) == "unavailable" %}
          0
        {% else %}
          {{states('sensor.octoprint_job_percentage')}}
        {% endif %}
```

Otherwise, add this to your configuration.yaml:
```yaml
sensor:
  - platform: template
    sensors:
      octo_percentage:
        friendly_name: "Octo Print %"
        value_template: >-
          {% if (states('sensor.octoprint_job_percentage')) == "unavailable" %}
            0
          {% else %}
            {{states('sensor.octoprint_job_percentage')}}
          {% endif %}
```


---
### 🤝 Found this useful, want to say 'Thanks' and support my efforts. CHEERS🍺
| Buy me a Coffee | PATREON |
|-----------------|---------|
| [![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-donate-yellow.svg?style=flat-square&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/3ative) | [![Patreon](https://img.shields.io/badge/Patreon-support-red.svg?style=flat-square&logo=patreon)](https://www.patreon.com/3ative) |
---
