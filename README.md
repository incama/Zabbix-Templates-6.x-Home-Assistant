# Zabbix-Templates-6.x-Home-Assistant
Zabbix Templates that interact with Home Assistant using the http agent and the Home Assistant API.

## General Requirements
- Make sure you create a long lived bearer access token within Home Assistant. (User settings and scroll all the way down to "Long-Lived Access Tokens".). Make sure to write down the token because you will need them within the template macro.
- I have tested the templates in all mayor 6 version of Zabbix, it may work in older version, but maybe not.
- You need to create an empty host within Zabbix, you can do so without defining an interface as all work is done by the Zabbix server itself (or proxy for that matter).
- Attach the downloaded template to the newly create host and make sure to change the inherited macro's to the correct values. I use macro's because it make creating templates more flexible.

## Specific Requirements
### Template: ZBX-6x-Home-Assistant-Energy.yaml
