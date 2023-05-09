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

Otherwise, add this to you configuration.yaml:
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




___

#### 💖 Found this useful, want to say '*Thanks*' and support my efforts. *CHEERS*🍺
| Buy me a Coffee | PATREON |
|-----------------|---------|
| https://www.buymeacoffee.com/3ative | https://www.patreon.com/3ative |
