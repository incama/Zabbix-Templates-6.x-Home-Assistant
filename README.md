# Zabbix-Templates-6.x-Home-Assistant
Zabbix Templates that interact with Home Assistant using the Zabbix http agent and the Home Assistant long lived API token.

## General Requirements
- Make sure you create a long lived bearer access token within Home Assistant. (User settings and scroll all the way down to "Long-Lived Access Tokens".). Make sure to write down the token because you will need them within the template macro.
- I have tested the templates in all mayor 6 version of Zabbix, it may work in older version, but maybe not.
- You need to create an empty host within Zabbix, you can do so without defining an interface as all work is done by the Zabbix server itself (or proxy for that matter).
- Attach the downloaded template to the newly create host and make sure to change the inherited macro's to the correct values. I use macro's because it make creating templates more flexible.

## Specific Template Requirements
### Category Energy
#### Template: **ZBX-6x-Home-Assistant-Energy.yaml**
Change one or more Macro values as needed. 
| MACRO | DEFAULT VALUE |
| --- | --- |
| {$ENTITY_ID_GAS} | sensor.gas_consumption |
| {$ENTITY_ID_PHASE_L1} | sensor.power_consumption_phase_l1 |
| {$ENTITY_ID_PHASE_L2} | sensor.power_consumption_phase_l2 |
| {$ENTITY_ID_PHASE_L3} | sensor.power_consumption_phase_l3 |
| {$WEBURL} | https://home-assistant.local |
| {$PORT} | 8123 |
| {$BEARER_APIKEY} | **** |

I don't use solar energy yet, but if someone does, please provide me the IDENTITY_ID's so I can integrate them within the template.
I guess the ID's are generic.

##### To Do list
- [x] Grab a beer!
- [ ] Find out if energy id's are generic.
- [ ] Get Solar power id's when generic.
- [ ] Adjust templates when above complies (except the beer).