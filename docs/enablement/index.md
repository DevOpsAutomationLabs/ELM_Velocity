# Configuring the integration between DevOps Velocity and ELM

## Topics covered in this Enablement exercise
### Overview
1. [DevOps Velocity Overview](#devops-velocity-overview) 
2. [What is a Velocity Plugin](#what-is-a-velocity-plugin) 
3. [DevOps Velocity's value stream map overview](#devops-velocitys-value-stream-map-overview)
### Working with EWM
4. [Configuring the plugin to integrate DevOps Velocity and EWM](#configuring-the-plugin-to-integrate-devops-velocity-and-ewm)
5. [Creating the EWM Value Stream in DevOps Velocity](#creating-the-ewm-value-stream-in-devops-velocity)
6. [Architecting the value stream aligned to the EWM Artifact Workflow](#architecting-the-value-stream-aligned-to-the-ewm-artifact-workflow)
### Working with ERM
7. [Preparing RM projects (reg mgmt and global configurations) for integration with Velocity](#preparing-rm-projects-reg-mgmt-and-global-configurations-for-integration-with-velocity)
8. [Configuring the plugin to integrate DevOps Velocity with ERM (DOORs NG req mgmt project)](#configuring-the-plugin-to-integrate-devops-velocity-with-erm-doors-ng-req-mgmt-project)
9. [Configuring the plugin to integrate DevOps Velocity with ERM (DOORs NG global configuration)](#configuring-the-plugin-to-integrate-devops-velocity-with-erm-doors-ng-global-configuration)
10. [Creating the ERM Value Stream in DevOps Velocity](#creating-the-erm-value-stream-in-devops-velocity)
11. [Architecting the value stream aligned to the ERM Artifact Workflow](#architecting-the-value-stream-aligned-to-the-erm-artifact-workflow)


## Overview 

### DevOps Velocity Overview

DevOps Velocity is a multi-container application installed in a Kubernetes container management system. 
<br/>
<br/>
![Velocity Value Stream screenshot](media/velocity_overview.png)

The DevOps Velocity value stream’s view provides a strategic window into your life-cycle workflow while simultaneously enabling you to drill-down and monitor individual elements with the intent of optimizing pipeline flow. These elements typically represent work items/issues, commits, pull requests, builds, deployments, and tests that are collected from many tools making up your delivery pipeline and integrated into Velocity via plugins. Individual elements are represented graphically by small circles, squares, or triangles, depending on the type, providing information from logically related tools, such as issues managed in an ALM solution linked to one’s source control management (SCM) system. How elements are visualized in a DevOps Velocity value stream can be simple to very complex. You are only limited by your knowledge of how to architect a value stream.

The pipeline capability enables organizations to drive releases by using application-focused methods. Add applications to logical environments and let DevOps Velocity generate basic release plans required to deploy the applications. Use quality gates to implement an enhanced level of automated governance helping organizations reduce business risk as software change moves through the delivery pipeline to the production environment.

DevOps Velocity’s enterprise-scale release management capabilities supports both cloud-native and on-premises deployment. Use DevOps Velocity to move releases through all of your development life-cycle environments including development, testing, and production. Create a predictable schedule of releases for your software applications. Share release statuses with all stakeholders so that they know the schedules, the key milestones, current status, and issues that may delay releases.

The Insights view helps organizations to assess the efficiency of product teams and the speed at which they are able to deliver value to the end users. Teams can measure every aspect of the development lifecycle with the supplied charts. Teams can create their own charts with metric definitions and upload custom data to DevOps Velocity using the Application programming interface (API) endpoints. Since data sources also encompass plug-ins and API calls, project data can come from virtually anywhere, including planning and development tools, testing and building applications, and deployment solutions. 

For more information about DevOps Velocity, visit [Velocity's product documentation page](https://www.ibm.com/docs/en/devops-velocity/5.1.0?topic=high-level-overview).
<br/>

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### What is a Velocity Plugin

Included as part of a Velocity installation are plugins which allow the Velocity Administrator to create connections between delivery pipeline applications and synchronize data between Velocity and the target application source (ELM, Jira, GitHub, DevOps Control, etc). Each plugin defines an expected record type and communication method. Communication can be uni-directional or bi-directional. To use a plug-in, you must configure an integration. There are multiple ways to configure an integration:
- Create an integration definition on the Plugins tab of the Integrations page.
- Install the plug-in and then create an integration definition.
- Add an integration definition to a value stream JSON file.
- Configure a deployment plan task for one of the native integration types.

<img src="media/e1.png" alt="e1" style="width=100%; height:auto;">

In total there are over 45 plugins available.

Once configured and as per that plugin’s synchronization timing, Velocity starts a plugin container image, makes the connection with the target application, and retrieves all data changes from the last sync time. NOTE: that sync time duration will vary depending on the amount of data being added to Velocity’s MongoDB repository.

<br/>

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### DevOps Velocity's value stream map overview

A Value Stream map file is used to describe the phases and stages a work item or artifact will go through from inception to implementation displaying the work items in their current state.

The highest level of a value stream is a phase. Phases represent important, organizational parts of the value stream, such as "Planning," or "Development." On the Value stream view, processing is done in left-right order. For example, your first phase might be for planning and contain items created in an issue tracking system. Your next phase, used for development, can track source control activity related to the issues, and any builds triggered by the activity. Your final phase, used for deployment, might track the related build artifacts as they move through your testing environments toward production.

Phases contain stages that define process flow within a phase. A development phase that integrates a source control tool might contain an In Progress stage followed by In Review and Merged stages. When you customize a value stream, you define the phases and stages and their order.

Stages are containers for dots. Dots represent units of work from DevOps Velocity or tools that are integrated into the value stream. Git commits or Jira issues, to take just two, are represented by individual dots. Work items, such as commits and builds, can be combined into individual dots. A dot's position in the value stream conveys important information about the object. Dots in a stage named Merged might represent items merged into Git repositories. An item's shape and color convey information about the item's type and status. A dot outlined in red, for example, might mean the item is past schedule. When dots change state, they move to new stages in near-real time. Finally, when you click on a dot, the displayed card provides information about the work items, including their history, and provides links to associated tools.

For this purposes of this enablement exercise, a very simple approach was followed in archtitecting the value stream. The phases and stages were mapped to the artifact workflows defined in EWM showing only the current state of the user stories, defects, and tasks.

![Velocity Value Stream map](media/velocity_map.png)

Reviewing the Value Stream Map image, notice the following:
1. Definition of the four phases - Open, In Progress, Approval, Released
2. Within the Open phase there are two stages named New and ReOpened
3. The query statement in the Open stage instructs Velocity to display all work items which are currently in a New state.
4. The query statement in the ReOpened stage instructs Velocity to display only work items of type Defect which in an ReOpened state.
5. And finally the target stanza on each stage helps to visualize the next stage that a work item could be displayed in.

For the purposes of this enablement exercise, a template has been created to help bootstrap creation and configuration of the value stream.

If you would like to review the entire VSM template, open the link in a new browser tab:
[EWM VS map Template](https://github.com/DevOpsAutomationLabs/ELM_Velocity/raw/main/files/EWM_defaultWorkflow-vsm.json)
<br/>

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

## Working with EWM

To visualize EWM artifacts as "DOTS" in a DevOps Velocity value stream, three basic steps must happen:
1. Configure a plugin to allow Velocity to communicate with EWM.
2. Create a Value Stream to provide a "single pane of glass" interface to visualize the "DOTS".
3. Architect the Value Stream by editing the Value Stream Map (json file) to replicate the workflows being used in EWM

### Configuring the plugin to integrate DevOps Velocity and EWM

The purpose of this exercise is to provide instruction on how to setup the integration between DevOps Velocity with EWM. It is assumed that the ELM server has already been setup and that an EWM project has been configured. For this lab exercise we will be using the JKE Banking sample application available with ELM.
<br/> 

| **Step** | **Details**  | **Additional Information** |
| ------------- | ------------- | ------------- |
| 1 | To access the Velocity plugin interface, open Velocity in a browser and log in. <br/> (uid: admin / pwd: admin) |   |
| 2 | Click on the settings icon. (Top RHS browser window) | <img src="media/e2.png" alt="e2" style="width:50%; height:auto;"> |
| 3 | Select Integrations from the LHS navigation bar. | <img src="media/e3.png" alt="e3" style="width:50%; height:auto;"> |
| 4 | Click on the Installed tab and review the many plugins already available. | <img src="media/e4.png" alt="e4" style="width:50%; height:auto;"> |
| **NOTE:** | While this exercise does not cover all topics related to plugins, know that administrator users can install additional plugins from the "Available" tab or upload custom plugins using the "Load Plugin" feature. |  |
| 5 | In the search control, enter “EWM”. | <img src="media/e5.png" alt="e5" style="width:50%; height:auto;"> |
| 6 | Click the twisty icon for the EWM plugin and note that there are multiple versions of this plugin available for installation. | <img src="media/e6.png" alt="e6" style="width:50%; height:auto;"> |
| 7 | Click the "Add Integration" button (RHS of page) for IBM Engineering Workflow Management (EWM) v1.1.37. | <img src="media/e7.png" alt="e7" style="width:100%; height:auto;"> |
| 8 | Working in the pop up window enter the following values into the fields on the form: <br/> <br/> **Integration name:** EWM(JKEBanking)<br/> **Server URL:** TODO: need to update<br/> **Projects (Comma Separated List):** JKE Banking (Change Management)<br/> **User ID:** sysadmin<br/> **Password:** passw0rd<br/> **Show hidden properties:** enabled<br/> **Logging level:** ALL<br/>  | <img src="media/e8.png" alt="e8" style="width:50%; height:auto;"> |
| 9 | Click the "Add" button when done. |  |
| 10 | Click the Configured tab on the Integrations page. | <img src="media/e9.png" alt="e9" style="width:50%; height:auto;"> |
| 11 | After a few seconds, confirm that the integration Status shows online. |  <img src="media/e10.png" alt="e10" style="width:75%; height:auto;"> |
| 12 | Click the 3 dots on RHS integration and select "View Logs" from the options presented. |  <img src="media/e11.png" alt="e11" style="width:100%; height:auto;"> |
| **NOTE:** |  If the status is not showing as Online, ensure the ELM Server is available. If the server is running, check the plugin settings to ensure they are properly set  by selecting Edit. | <img src="media/e12.png" alt="e12" style="width:25%; height:auto;"> |
| 13 | Select the Log file and view output contents. | <img src="media/e13.png" alt="e13" style="width:100%; height:auto;"> |

Congratulations on successfully configuring the EWM Plugin.

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Creating the EWM Value Stream in DevOps Velocity
<br/>

| **Step** | **Details**  | **Additional Information** |
| ------------- | ------------- | ------------- |

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Architecting the value stream aligned to the EWM Artifact Workflow
<br/>

| **Step** | **Details**  | **Additional Information** |
| ------------- | ------------- | ------------- |

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

## Working with ERM

### Preparing RM projects (reg mgmt and global configurations) for integration with Velocity
<br/>

| **Step** | **Details**  | **Additional Information** |
| ------------- | ------------- | ------------- |

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Configuring the plugin to integrate DevOps Velocity with ERM (DOORs NG req mgmt project)
<br/>

| **Step** | **Details**  | **Additional Information** |
| ------------- | ------------- | ------------- |

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Configuring the plugin to integrate DevOps Velocity with ERM (DOORs NG global configuration)
<br/>

| **Step** | **Details**  | **Additional Information** |
| ------------- | ------------- | ------------- |

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Creating the ERM Value Stream in DevOps Velocity
<br/>

| **Step** | **Details**  | **Additional Information** |
| ------------- | ------------- | ------------- |

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

### Architecting the value stream aligned to the ERM Artifact Workflow
<br/>

| **Step** | **Details**  | **Additional Information** |
| ------------- | ------------- | ------------- |

[Return to List of Enablement Topics](#topics-covered-in-this-enablement-exercise)
<br/>

