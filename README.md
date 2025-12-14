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

<div align="center">

### 💖 Support This Project

Found this useful? Want to say thanks and fuel future creations?

**Your support keeps the creativity flowing!** 🍺✨

<table>
  <tr>
    <td align="center">
      <a href="https://www.buymeacoffee.com/3ative">
        <img src="https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow.svg?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white" alt="Buy Me A Coffee"/>
        <br/>
        <b>☕ Buy me a Coffee</b>
      </a>
    </td>
    <td align="center">
      <a href="https://www.patreon.com/3ative">
        <img src="https://img.shields.io/badge/Patreon-Become%20a%20Patron-red.svg?style=for-the-badge&logo=patreon&logoColor=white" alt="Patreon"/>
        <br/>
        <b>💖 Join on Patreon</b>
      </a>
    </td>
  </tr>
</table>

**Every contribution helps bring more awesome projects to life!** 🚀

</div>

---
