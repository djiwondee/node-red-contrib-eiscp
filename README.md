node-red-contrib-eiscp
==========================

[![codebeat badge](https://codebeat.co/badges/33e94191-3028-4255-82b9-6300cd100c68)](https://codebeat.co/projects/github-com-djiwondee-node-red-contrib-eiscp-master)

# Description

Control your Integra/Onkyo devices (AVR, BD player, etc.) over IP, with help of eISCP protocol right from Node-RED.

PDF of eISCP protocol documentation can be found [here](http://goo.gl/Aa1W8F).

# What's inside?

The package includes three nodes:

'eiscp-controller' : a unique CONFIG node that holds connection configuration for eiscp and will acts as the encapsulator for eiscp access. As a node-red 'config' node, it cannot be added to a graph, but it acts as a singleton object that gets created in the the background when you add an 'eiscp' or 'eiscp-device' node and configure it accordingly.

- 'eiscp-out' : eiscp output node that can send eiscp, so it can be used with function blocks.
- 'eiscp-in': eiscp listener node, who emits flow messages based on activity on the eiscp device.
 The payload contains a string reflecting the command and is a mandatory value.

# Usage

According to official documentation: http://nodered.org/docs/getting-started/adding-nodes.html
 
# Examples

Control your device using Amazon Alexa

![alt text](https://i.gyazo.com/807772f70a330517afc66dd9d2d2747a.png)

1. Drag 'Alexa Local'

2. Drag 'Function' and configure with appopriate command

![alt text](https://i.gyazo.com/1f16509f6773658805168d32826dc296.png)

Command list available here:
https://raw.githubusercontent.com/tillbaks/node-eiscp/master/eiscp-commands.json


3. Drag and configure 'eiscp out' node 

![alt text](https://i.gyazo.com/0674270018e67d34f43fab926f32113e.png)


# License

![Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png "CC BY-NC-SA 4.0")

# ToDo

- Fixing/adjustment of eiscp commands
