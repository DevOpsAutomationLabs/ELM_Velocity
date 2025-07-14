# Integrating DevOps Velocity with ELM to achieve Business Outcomes

## Business Scenarios covered by this demonstration:
### * [Visualize and Optimize the flow of work to improve team productivity](#business-scenario-1-visualize-and-optimize-the-flow-of-work-to-improve-team-productivity)
### * [Eliminate guess work and use data to make better investment decision for process improvement](#business-scenario-2-eliminate-guess-work-and-use-data-to-make-better-investment-decisions-for-process-improvement)


## Understanding the Business Problem

Many DevOps organizations use Dora metrics or Flow metrics to measure the efficiency of their software delivery pipeline. While flow metrics focus on the stream of work items and the efficiency of processes, Dora metrics provide insights into the effectiveness of software development and delivery practices. Regardless of which KPIs are adopted, both provide a high level measure of the end to end software delivery process.

**DORA Metrics**

1. Deployment Frequency - How often production releases occur?
2. Lead Time to Change - What is the length of time it takes for code changes to be made available in production?
3. Change Failure Rate - What is the frequency of deployments which cause an issue in production?
4. Mean Time to Recovery - What is the length of time it takes to recover from the production issue?

**Flow Metrics**

1. Flow Time - Is time-to-market getting shorter?
2. Flow Velocity - Is value delivery accelerating? 
3. Flow Efficiency - Is upstream work holding up delivery?
4. Flow Load - Is demand vs capacity being balanced?
5. Flow Distribution - Are we investing in both value generation and protection?

Now it is a well know fact that any process is only as fast as its slowest point. And all processes have a least slow point. The "trick" is to find the slow bottleneck, take action to improve, and measure the outcome to understand if the desired outcome was achieved.

Using these high level vanity metrics and armed with a desire to improve, the next typical step would be for the organization to execute a Value Stream Mapping exercise assembling a team of people to share their opinions on how long each step of the end to end process takes and recording their input on a value stream map - value add time, non-value add time, process efficiency for each individual step in their process. This can be a very expensive and laboreous process where the outcome is only valid until some improvement action is implemented. Because, once the fix is implemented, the bottleneck has probably moved to another location in the delivery pipeline.

![Value Stream Map](media/value_stream_map.png)

The alternative is to Value Stream Mapping is Value Stream Management. A Value Stream Management solution, like DevOps Velocity, is continuously ingesting data from the tools used in the software delivery pipeline and presenting them in a holistic value stream providing insight, in almost real time, on not only how efficient the software delivery pipeline is but where in the pipeline opportunities for improvement exist. Making Value Stream Management a much more scientific approach eliminating the guess work and taking action based on data instead of opinion.

![Value Stream](media/value_stream.png)

## Introducing DevOps Velocity

DevOps Velocity is a multi-container application installed in a Kubernetes container management system. 
<br/><br/>![Velocity Value Stream screenshot](media/velocity_overview.png)

The DevOps Velocity value stream’s view provides a strategic window into your life-cycle workflow while simultaneously enabling you to drill-down and monitor individual elements with the intent of optimizing pipeline flow. These elements typically represent work items/issues, commits, pull requests, builds, deployments, and tests that are collected from many tools making up your delivery pipeline and integrated into Velocity via plugins. Individual elements are represented graphically by small circles, squares, or triangles, depending on the type, providing information from logically related tools, such as issues managed in an ALM solution linked to one’s source control management (SCM) system. How elements are visualized in a DevOps Velocity value stream can be simple to very complex. You are only limited by your knowledge of how to architect a value stream.

The pipeline capability enables organizations to drive releases by using application-focused methods. Add applications to logical environments and let DevOps Velocity generate basic release plans required to deploy the applications. Use quality gates to implement an enhanced level of automated governance helping organizations reduce business risk as software change moves through the delivery pipeline to the production environment.

DevOps Velocity’s enterprise-scale release management capabilities supports both cloud-native and on-premises deployment. Use DevOps Velocity to move releases through all of your development life-cycle environments including development, testing, and production. Create a predictable schedule of releases for your software applications. Share release statuses with all stakeholders so that they know the schedules, the key milestones, current status, and issues that may delay releases.

The Insights view helps organizations to assess the efficiency of product teams and the speed at which they are able to deliver value to the end users. Teams can measure every aspect of the development lifecycle with the supplied charts. Teams can create their own charts with metric definitions and upload custom data to DevOps Velocity using the Application programming interface (API) endpoints. Since data sources also encompass plug-ins and API calls, project data can come from virtually anywhere, including planning and development tools, testing and building applications, and deployment solutions.

In this demonstration, you will focus on the Value Stream and Insights views.

For more information about DevOps Velocity, visit [Velocity's product documentation page](https://www.ibm.com/docs/en/devops-velocity/5.1.0?topic=high-level-overview).

## Business Scenario 1: Visualize and Optimize the flow of work to improve team productivity.

### 1.1 DevOps Velocity and the value stream data

The value stream is architected to align with a software development team's phases and stages making up the software delivery pipeline. DevOps Velocity tracks the number of work items and average time a work item spends in each one of the stages. It is DevOps Velocity's ability to present this type of information in a single control plane which allows teams to focus on improvement over wasting time trying to determine which stage is the software delivery pipeline is the slowest point.

| **Step** | **Details**  | **Additional Information** |
|:-------------:|:------------- |:------------- |
| 1 |   | <img src="media/d1.png" alt="d1" style="width:50%; height:auto;"> |


### 1.2 Working with DevOps Velocity KPIs and Metrics

| **Step** | **Details**  | **Additional Information** |
|:-------------:|:------------- |:------------- |
| 1 |   | <img src="media/d1.png" alt="d1" style="width:50%; height:auto;"> |


### 1.3 Understanding DevOps Velocity's Alert capabilities

| **Step** | **Details**  | **Additional Information** |
|:-------------:|:------------- |:------------- |
| 1 |   | <img src="media/d1.png" alt="d1" style="width:50%; height:auto;"> |


### 1.4 DevOps Velocity and the Swimlane View

| **Step** | **Details**  | **Additional Information** |
|:-------------:|:------------- |:------------- |
| 1 |   | <img src="media/d1.png" alt="d1" style="width:50%; height:auto;"> |


Congratulations on successfully configuring the DevOps Velocity value stream to visualize ERM artifacts.

[Return to Top of Demonstration Page](#integrating-devops-velocity-with-elm-to-achieve-business-outcomes)
<br/>

## Business Scenario 2: Eliminate guess work and use data to make better investment decisions for process improvement

### 2.1 Adding DevOps Velocity's Bottleneck Detection capability

| **Step** | **Details**  | **Additional Information** |
|:-------------:|:------------- |:------------- |
| 1 |   | <img src="media/d1.png" alt="d1" style="width:50%; height:auto;"> |


### 2.2 Working with DevOps Velocity's DashBoards and Charts

| **Step** | **Details**  | **Additional Information** |
|:-------------:|:------------- |:------------- |
| 1 |   | <img src="media/d1.png" alt="d1" style="width:50%; height:auto;"> |


<br/>

[Return to Top of Demonstration Page](#integrating-devops-velocity-with-elm-to-achieve-business-outcomes)