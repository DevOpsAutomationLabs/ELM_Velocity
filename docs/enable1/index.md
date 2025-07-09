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

Included as part of a Velocity installation are plugins which allow the Velocity Administrator to create connections between delivery pipeline applications and synchronize data between Velocity and the target application source (ELM, Jira, GitHub, DevOps Control, etc). Each plugin defines an expected record type and communication method. Communication can be uni-directional or bi-directional. To use a plug-in, you must configure an integration. There are multiple ways to configure an integration:
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
<br/>
1. To access the Velocity plugin interface, log into Velocity (uid: admin / pwd: admin), and click on the settings icon. (Top RHS browser window)
<img src="media/settings_orientation.png" alt="settings icon orientation" style="width:25%; height:auto;">
2. Select Integrations from the LHS navigation bar.
<img src="media/integrations.png" alt="integrations orientation" style="width:25%; height:auto;">
3. Click on the Installed tab and review the many plugins already available.
<img src="media/integrations_image.png" alt="integrations" style="width:25%; height:auto;">

[!Note]
While this exercise does not cover all topics related to plugins, know that administrator users can install additional plugins from the "Available" tab or upload custom plugins using the "Load Plugin" feature. <br/>

4. In the search control, enter “EWM”.
<img src="media/search.png" alt="search" style="width:25%; height:auto;">
5. Click the twisty icon for the EWM plugin and note that there are multiple versions of this plugin available for installation.
<img src="media/ewm_plugins.png" alt="ewm plugins" style="width:25%; height:auto;">
6. Click the "Add Integration" button (RHS of page) for IBM Engineering Workflow Management (EWM) v1.1.37
<img src="media/add_ewm.png" alt="add ewm integration" style="width:75%; height:auto;">
7. Working in the pop up window enter the following values into the fields on the form:<br/>

**Integration name:** EWM(JKEBanking)<br/>
**Server URL:** need to update<br/>
**Projects (Comma Separated List):** JKE Banking (Change Management)<br/>
**User ID:** sysadmin<br/>
**Password:** passw0rd<br/>
**Show hidden properties:** enabled<br/>
**Logging level:** ALL<br/>

<img src="media/ewm_setup.png" alt="ewm integration" style="width:25%; height:auto;">

<br/>

[Return to List of Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Preparing RM projects (reg mgmt and global configurations) for integration with Velocity
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