# Configuring the integration between DevOps Velocity and ELM

### Topics covered in this Enablement exercise
1. [What is a Velocity Plugin](#what-is-a-velocity-plugin) 
2. [Configuring the plugin to integrate DevOps Velocity and EWM](#configuring-the-plugin-to-integrate-devops-velocity-and-ewm)
3. [Preparing RM projects (reg mgmt and global configurations) for integration with Velocity](#preparing-rm-projects-reg-mgmt-and-global-configurations-for-integration-with-velocity)
4. [Configuring the plugin to integrate DevOps Velocity with ERM (DOORs NG req mgmt project)](#configuring-the-plugin-to-integrate-devops-velocity-with-erm-doors-ng-req-mgt-project)
5. [Configuring the plugin to integrate DevOps Velocity with ERM (DOORs NG global configuration)](#configuring-the-plugin-to-integrate-devops-velocity-with-erm-doors-ng-global-configuration)
6. [Creating a Value Stream in DevOps Velocity](#creating-a-value-stream-in-devops-velocity)
7. [Architecting the value stream aligned to the ELM Artifact Workflow](#architecting-the-value-stream-aligned-to-the-elm-artifact-workflow)
8. [Understanding DevOps Velocity's value stream map file](#understanding-devops-velocitys-value-stream-map-file)

### What is a Velocity Plugin

Included as part of a Velocity installation are plugins which allow the Velocity Administrator to create connections between delivery pipeline applications and synchronize data between Velocity and the target application source (ELM, Jira, GitHub, DevOps Control, etc). A plug-in is a software add-on designed to communicate with external services and applications. Each plug-in defines an expected record type and communication method. Communication can be uni-directional or bi-directional. To use a plug-in, you must configure an integration. There are multiple ways to configure an integration:
- Create an integration definition on the Plugins tab of the Integrations page.
- Install the plug-in and then create an integration definition.
- Add an integration definition to a value stream JSON file.
- Configure a deployment plan task for one of the native integration types.

<img src="media/plugin_overview.png" alt="Plugin architecture image" style="width:200%; height:auto;">

In total there are over 45 plugins available.

Once configured and as per that plugin’s synchronization timing, Velocity starts a plugin container image, makes the connection with the target application, and retrieves all data changes from the last sync time. NOTE: that sync time duration will vary depending on the amount of data being added to Velocity’s MongoDB repository.

<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Configuring the plugin to integrate DevOps Velocity and EWM

To access the Velocity plugin interface, log into Velocity (uid: admin / pwd: admin), and click on the <img src="media/setting_icon.png" alt="Setting icon" style="width:50%; height:auto;">![settings icon](media/setting_icon.png) icon (top RHS of the browser window).
<br/>
![settings orientation](media/settings_orientation.png)
<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Preparing RM projects (reg mgmt and global configurations) for integration with Velocity
<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Configuring the plugin to integrate DevOps Velocity with ERM (DOORs NG req mgmt project)
<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Configuring the plugin to integrate DevOps Velocity with ERM (DOORs NG global configuration)
<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Creating a Value Stream in DevOps Velocity
<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Architecting the value stream aligned to the ELM Artifact Workflow
<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Understanding DevOps Velocity's value stream map file
<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>