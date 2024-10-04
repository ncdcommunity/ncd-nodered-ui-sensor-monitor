# ncd-nodered-ui-sensor-monitor
A Node-RED Dashboard tool to monitor NCD Sensors 

This project is a basic subflow developed by the NCD IoT team based on Node-RED and the new Dashboard 2.0 framework, which allows you to visualize the data provided by the NCD sensors, such as MAC Address, Type, Mode, RSSI (DigiMesh), and the date and time of the last incoming message in an intuitive way.
#
![ncd-ui-monitor-sensor](https://github.com/user-attachments/assets/131e6ab1-08f9-442e-8813-3935c6acd342)

## Requirements/Dependencies:

Before you begin using the NCD-Dashboard, you’ll need to have the following software installed:

- Node-RED
- @ncd-io/node-red-enterprise-sensors Library
- @flowfuse/node-red-dashboard

## Node-RED

Node-RED, is a visual programming tool, It provides a browser-based editor that allows creating applications by wiring predefined black box functions (nodes) . Despite its technical nature, Node-RED offers a user-friendly interface. Node-RED is an open-source project under the OpenJS Foundation. This means it’s free to use, without any monthly subscription fees. You can install and run Node-RED locally on your PC, or, in the case of our Enterprise IIoT Gateway, it comes pre-installed and runs as a service.

## NCD Enterprise Sensor Library
This library handles communication to, and configuration of, the NCD Wireless Sensor Line. It can be used in conjunction with Node-RED to create and manage a Wireless Sensor Network using the Node-RED flow-based development tool on any platform.

> [!NOTE]
> This library is pre-installed on the Enterprise IIoT Gateway and ready to use.

## FlowFuse Dashboard 2

FlowFuse Dashboard 2.0 is an easy to use collection of nodes for Node-RED that allows you to create data-driven Dashboards & data visualizations. Installation procedure is similar to the previous one, FlowFuse’s Node-RED Dashboard 2.0 is also available in the Node-RED Palette Manager.

Source: https://dashboard.flowfuse.com/

### Instalation Procedure

Step 1.- Open the menu in the top-right of Node-RED, then Click “Manage Palette”:

![nodered-menu-1](https://github.com/user-attachments/assets/34964892-72fc-4315-84e4-3abbfa15c02c)

Step 2.- Switch to the “Install” tab, Search “@flowfuse/node-red-dashboard”, Install the  package:

![flow-fuse-dashboard-installation-install](https://github.com/user-attachments/assets/ba49cb81-810a-4f48-be8d-0928a09c89df)

Step 3.- You must confirm the installation by clicking on the Install button in the pop-up window.

![flow-fuse-dashboard-installation-confirm](https://github.com/user-attachments/assets/e43151e5-6482-406f-93b5-74a62cae7584)

Step 4.- You will see a list of the dashboard 2 nodes that have been installed.

![flow-fuse-dashboard-installation-nodes-installed](https://github.com/user-attachments/assets/5f7d308d-3647-45b5-a322-c493ab07dff6)

Step 5.- In workspace you can see the available nodes in the nodes palette, as shown in the following image:

![flow-fuse-dashboard-installation-nodes-pallete](https://github.com/user-attachments/assets/31244a7c-92d9-4f71-b834-0698ec451360)

See the following GIF for a visual demonstration of the installation process:

![nodered-install-flow-fuse-dashboard-2](https://github.com/user-attachments/assets/aae21534-2964-4c1b-a107-09f71352cc58)

## Importing
After successfully installing Dashboard 2.0, you’re ready to import the NCD UI Sensor Monitor. The process is straightforward, but be sure to follow these steps carefully:

Copy the JSON: Locate the "ncd-ui-sensor-monitor" JSON file.
Import the JSON: Within Node-RED, use the import function to bring in the copied JSON file.

This will import the NCD Dashboard elements into your Node-RED workspace, allowing you to visualize and interact with your NCD sensor data.

### Copy JSON File
 1. Go to "https://github.com/ncdcommunity/ncd-nodered-ui-sensor-monitor/blob/main/Node-RED/ncd-ui-sensor-monitor.json" in this repository:
![copy_raw_file](https://github.com/user-attachments/assets/fa47f7c8-9461-4c38-be1a-58f35e887e48)

### Import NCD-UI-Monitor
With the NCD Dashboard source code copied, head back to the Node-RED node editor and follow these next steps carefully.

1. Go to the Main Menu (icon in the upper right corner) then click on “Import” option, as shown in picture:

![manage_palette_](https://github.com/user-attachments/assets/0998f8fc-a42b-455c-9fc6-e2fb4feb7c86)

2. A text-box will be opened. Right click and paste the code you just copied from GitHub, as shown in picture:

 ![Screenshot from 2024-09-20 15-03-59](https://github.com/user-attachments/assets/3b81fc63-ac09-485d-be1f-df06dc0f14bc)

3. You should see the JSON code in text-box, now you can press the red “Import” button at the bottom right (by default the “current flow” option is selected):

![Screenshot from 2024-09-20 15-04-11](https://github.com/user-attachments/assets/9c936814-746b-4d8c-a5ad-99b836fff2aa)

4. In the top of the Node-RED editor, you will see information of the NCD-UI-Monitor you just imported, and automatically you will have the node available inside the node editor, now you can position it inside the editor or workspace by left clicking:

![Screenshot from 2024-09-20 15-05-19](https://github.com/user-attachments/assets/b0794185-94a6-41c3-b355-fd5c31d57717)


> [!NOTE]
> You will need to connect the output of the "Wireless Gateway" node to the input fo the "UI Monitor" node.

![ncd-ui-monitor-sensor-connection](https://github.com/user-attachments/assets/d83cadd1-64d6-4e38-bc23-122cef43ffc7)


5. This flow includes a Wireless Gateway node pre-configured with the Enterprise IIoT Gateway port, you should click on "Deploy" button in order to save and apply the changes:

![Screenshot from 2024-09-20 15-06-04](https://github.com/user-attachments/assets/7650b69f-2d4f-4f12-a49b-2eca3148a255)


6. Then go to "Dashboard 2.0" tab:

![Screenshot from 2024-09-20 15-06-34](https://github.com/user-attachments/assets/83f15f7c-616f-4c12-8420-9804daf89e7c)


7. And click on "Open Dashboard" button, in order to open the Dashboard in a new Web Explorer Tab:

![Screenshot from 2024-09-20 15-06-44](https://github.com/user-attachments/assets/b40b3474-3a8a-438c-9a40-d3edc5ba5c98)


8. You should see something like this, and as soon as a new NCD Sensor data arrive, you should see the info:

![ncd-ui-monitor-sensor-1](https://github.com/user-attachments/assets/07ce0306-be7b-439c-9999-d468f7ab2d08)

Example:

![ncd-ui-monitor-sensor-2](https://github.com/user-attachments/assets/0552a480-b6b1-4330-a7ab-5cfce723716b)
##
![ncd-ui-monitor-sensor-3](https://github.com/user-attachments/assets/4c7fc41a-81df-442f-9158-b1ded6dbe632)


_____________________________________________________________________________________
© 2019-2024 National Control Devices, LLC. All rights reserved.









