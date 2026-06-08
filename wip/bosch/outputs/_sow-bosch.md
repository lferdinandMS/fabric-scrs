<img src="media/image2.png" style="width:1.85065in;height:0.67568in" />

<span class="mark">Click icon to insert client logo,</span>

<span class="mark">then delete this text</span>

# Table of contents

1 Project objectives and scope 1

1.1 Introduction 1

1.2 Customer desired business objectives 1

1.3 Targeted scope (Epics) 2

1.4 Areas out of scope 4

2 Delivery approach, completion and timeline 6

2.1 Delivery overview 6

2.2 Delivery approach 6

2.3 Testing and defect remediation 9

2.4 Sprint completion 12

2.5 Project completion 13

2.6 Timeline 13

3 Project organization 14

3.1 Project capacity 14

3.2 Project staffing 14

3.3 Executive steering committee 18

3.4 Product council 18

3.5 Feature team 19

4 Project governance 20

4.1 Project communication 20

4.2 Risk and issue management 20

4.3 Change management process 20

4.4 Escalation path 20

5 Exhibits 21

5.1 Initial targeted product backlog 21

5.2 \<Bosch\>-specific documentation 49

6 Appendix 49

6.1 Definitions and acronyms 49

6.2 Technology requirements 51

6.3 Environment requirements 51

6.4 **\<Bosch\>** responsibilities 52

6.5 Project assumptions 52

# Table of tables

Table 1: \<Bosch\> desired business objectives 2

Table 2: Targeted Epic 2

Table 3: Areas out of scope 4

Table 4: Delivery approach 7

Table 5: Testing in scope 9

Table 6: Sprint review work products 12

Table 7: Project staffing - \<Bosch\> 14

Table 8: Project staffing – \<MSFT\> 16

Table 9: Executive steering committee roles 18

Table 10: Product council roles 19

Table 11: Feature team roles 19

Table 13: Table of abbreviations 49

Table 14: Technology requirements 51

Table 15: Environment requirements 51

# Table of figures

[Figure 1: High-level timeline [15](#_Toc227840189)](#_Toc227840189)

[Figure 2: Product council [21](#_Toc194478203)](#_Toc194478203)

This Statement of Work (SOW) and any exhibits, appendices, schedules, and attachments to it are made pursuant to Work Order (WO) *\[insert WO number\]* and describes the work to be performed (“services”) by Microsoft (“us,” “we”) for \<Bosch\> (“*\[Customer short name if any\]*”, “Customer”, “you”, “your”) relating to \<In Car Voice Assistant\> (“Project”).

This SOW and the associated WO expire 30 days after their publication date (date Microsoft submits to the Customer) unless signed by both parties or formally extended in writing by Microsoft.

# Project objectives and scope 

## Introduction

Bosch is approaching Microsoft (ISD in particular) to build the **of In-Car Voice Assistant Solution,** which is developed on top of latest AI technologies across the Edge and Cloud.

- Short-Term Target: Present the Solution in the CES event in US.

- Long-Term Target: Co-sell the solution to the OEMs, including BMW, Mercedes, Toyota, etc.

## Customer desired business objectives

The business objectives of this project are to build the solution in an AI Box, which is targeted to be presented in CES event. These objectives will be used for planning and overall goals for the project, and not all the objectives may be achieved as a part of this SOW.

The desired business objectives defined in this section and any initial product backlog defined in this SOW do not constitute a fixed scope. There is no guarantee that all desired business objectives and all initial product backlog items will be completed within the contracted capacity. An ongoing governance process, driven by \<Bosch\>’s product owner, that prioritizes product backlog against available capacity is described in the section. If more capacity or duration is needed to deliver the desired business objectives or if additional objectives need to be defined, the section will be followed to increase capacity. \<MSFT\> will continue its efforts based on the priorities and direction provided by \<Bosch\> until such time as all capacity has been consumed.

By fulfilling their responsibilities and requirements listed in this SOW within the timeframes requested by Microsoft, \<Bosch\> can support the completion of the desired business objectives and adherence to the schedule. Should this not be the case, the change management process may be needed to increase capacity or to extend the schedule, as described in the [*Change management process*](#change-management-process) section.

Table 1: \<Bosch\> desired business objectives

<table style="width:95%;">
<colgroup>
<col style="width: 51%" />
<col style="width: 43%" />
</colgroup>
<thead>
<tr>
<th>Desired business objectives</th>
<th>Assumptions</th>
</tr>
</thead>
<tbody>
<tr>
<td>Build end-to-end Voice Assistant Capabilities</td>
<td>Including Online and Offline Capabilities</td>
</tr>
<tr>
<td>Fine tune all the Offline models on the specified device/Box</td>
<td>The specs of the Box will be decided in Sprint 0 of the project</td>
</tr>
<tr>
<td>Fine tune all the online models/agents based on the features in scope</td>
<td></td>
</tr>
<tr>
<td>Build Selected Features targeted for CES</td>
<td><p>The list of features for CES will be agreed in Sprint 0</p>
<p>3<sup>rd</sup> Party APIs need to be prepared by Bosch</p></td>
</tr>
<tr>
<td>Enable Bosch team to add new features to the assistant</td>
<td>Details will be agreed in Sprint 0</td>
</tr>
<tr>
<td></td>
<td></td>
</tr>
</tbody>
</table>

In addition to the objectives listed above, the initial product backlog in the section will be used as input for product baseline planning. As with objectives, not all backlog items will always be delivered. The Agile delivery approach allows \<Bosch\> to prioritize the valuable backlog items and continually adapt the solution.

## Targeted scope (Epics)

The project might address the following areas which might be revised at any time based on direction from \<Bosch\>. There might be additional areas not listed in the following list that might be delivered, as well as areas listed that are prioritized low enough that it might not be built due to contracted capacity.

By the nature of Agile delivery, the scope is variable. When the resource labor category, capacity, or duration of the delivery team needs to be amended to deliver the agreed-upon backlog items, we will use the change management process to allow the project to change the available resources and capacity.

**<span class="mark">Refer to Section 5.1 as the full list of the scoped features.</span>**

<table>
<caption><p>Table 2: Targeted Epic</p></caption>
<colgroup>
<col style="width: 31%" />
<col style="width: 48%" />
<col style="width: 19%" />
</colgroup>
<thead>
<tr>
<th><strong>Epic</strong></th>
<th>Description</th>
<th>Assumptions</th>
</tr>
</thead>
<tbody>
<tr>
<td>Languages to be supported</td>
<td>English, German, Japanese</td>
<td></td>
</tr>
<tr>
<td>Architecture Design</td>
<td><p>Support Multiple individual OEM vehicle architectures:</p>
<p>1.Non AI Box scenario:​</p>
<p>a) AI in the cloud, Cockpit ECU acting just as the user interface layer​</p>
<p>b) Powerful AI cockpit SoC based ECU (e.g. Qualcomm 8797/Renesas X5H/MTK C-X1)​</p>
<p>2.AI Box scenario:​</p>
<p>a) Powerful AI box (100+TOPs) + Regular cockpit ECU(no AI onboard)​</p>
<p>b) Less powerful AI box (~50 TOPs performance) + limited AI cockpit (Qualcomm 8255/8295, Renesas X5B, MTK 2718 with &lt;50TOPs)​</p>
<p>c)Less powerful AI box (~50 TOPs performance) + Regular cockpit ECU (no AI onboard)​</p></td>
<td>We will focus 1 of the supported architectures for the CES demo.</td>
</tr>
<tr>
<td>Offline Capabilities</td>
<td><p>Fully functional Offline Assistant, including:</p>
<ul>
<li><p>Wakeup word Model</p></li>
<li><p>Speech To Text Model</p></li>
<li><p>SLM Model</p></li>
<li><p>Text To Speech Model</p></li>
</ul></td>
<td>All models run offline in the Car/Box</td>
</tr>
<tr>
<td>Online Capabilities</td>
<td><p>Fully functional Online Assistant</p>
<ul>
<li><p>Speech To Text Model</p></li>
<li><p>LLM Model</p></li>
<li><p>Text To Speech Model</p></li>
</ul></td>
<td>ECNR and Wakeup word will be running offline</td>
</tr>
<tr>
<td>STS (speech to speech models)</td>
<td>Features such as emotion detection, tone recognition, and similar capabilities should be part of the model use cases.</td>
<td>Requires 150 Tops Compute resource.</td>
</tr>
<tr>
<td>Configurable system</td>
<td><p>1. Tools can be added, and cloud-bound queries can be routed via configuration, other methods, or models.</p>
<p>2. Workflow A2A; development of new agents is supported by the arbitrator.</p></td>
<td></td>
</tr>
<tr>
<td>Vehicle Manual</td>
<td>Related Models or Vector DB should run completely local, No Cloud Dependency</td>
<td></td>
</tr>
<tr>
<td>Memory/context manager/arbitration</td>
<td><p>1. configurable and changeable as per OEM requirements with full source code.</p>
<p>2. Arbitration should be edge native (decision to involve any agents &amp; decision making to call a cloud agent)</p></td>
<td></td>
</tr>
<tr>
<td>SLM continuous evaluation test framework</td>
<td>Test Framework to evaluate new SLMs for their responsiveness, quality of response, tool calling confidence (might need further discussion to explain)</td>
<td></td>
</tr>
<tr>
<td>CES Demo</td>
<td>A working demo that can be shown at CES</td>
<td>Demo use cases would be decided at Sprint 0.</td>
</tr>
<tr>
<td>Overall test framework</td>
<td>Automated test framework to test the overall system before any new release</td>
<td></td>
</tr>
<tr>
<td>Feature List for Next Phase</td>
<td>Microsoft and Bosch will collaborate and form the feature lists for the next phase of the project.</td>
<td></td>
</tr>
<tr>
<td>Performance Evaluation</td>
<td>With in the project, Microsoft and Bosch team will reach an agreement for how to evaluate the performance and accuracy of all the models.</td>
<td></td>
</tr>
</tbody>
</table>

See [*Appendix*](#appendix) for additional information on technology and environment requirements.

## Areas out of scope

Any area not explicitly included in the <span class="mark"></span>[*Targeted scope*](#targeted-scope-epics) (Epics) section is out of scope for \<MSFT\> during this project. The table below lists known out of scope areas identified, but not limited to, during the construction of this SOW for the project.

**Reference [6.4](#_Ref194409168)[\<Bosch\> responsibilities](#_Ref194409174) for a list of any key customer responsibilities that are critical to project completion yet out of scope for Microsoft.**

| Areas out of scope | Description |
|----|----|
| \<Bosch\> software | Deployment and configuration of \<Bosch\> software is out of scope. |
| Commercially available third-party software | Activities where \<MSFT\> would be designing, configuring, integrating, deploying, or fixing issues in commercially available third-party software (excluding open source) are out of scope. |
| Data cleansing | Data cleansing activities are out of scope. |
| Data migration | Data migration activities are out of scope. |
| Hardware | \<MSFT\> will not provide hardware for this project. |
| Network and storage | Troubleshooting or remediation of existing network and storage systems is out of scope. |
| Organizational change management | Designing—or redesigning— \<Bosch\>’s functional organization is out of scope. |
| Process re-engineering | Designing functional business components and business processes of the solution is out of scope. |
| Product licenses and subscriptions | Product licenses (Microsoft or non-Microsoft) and cloud service subscriptions are out of scope, unless otherwise noted in this SOW. |
| Solution/product adoption | End user change management and adoption. |
| System integration | Modifications to commercially available third-party systems and/or external interfaces to support integration are out of scope. |
| Testing | Testing and configuration of applications and services outside of those required to support the deployment of the solution are out of scope. |
| Training | Formal user training or the creation of training materials is out of scope. |
| Upgrades, updates, patches, and fixes | Product upgrades, updates, patches, fixes, and design change requests for Microsoft products are out of scope. |
| User communications | Planning or undertaking user communications is out of scope. |
| User Browser Testing | Browser compatibility testing has not been included in the project. If desired, backlog items may be added and prioritized for this effort. |

Table 3: Areas out of scope

# Delivery approach, completion and timeline

## Delivery overview

\<MSFT\> will follow an Agile-based delivery approach that adapts to changing requirements and feedback throughout the project. The Agile delivery approach is based on fixed capacity, variable scope known as the scrum process (<http://scrumguides.org>). This organizes the work into small and frequent iterations called sprints.

At the start of the project, \<MSFT\> and \<Bosch\> will jointly define and prioritize the product backlog; this is a list of features and tasks that need to be delivered. The product backlog will be refined and updated throughout the project as new insights and learnings emerge. The product backlog will be used to plan and execute sprints. These are fixed-length periods of time, typically two to four weeks, during which a subset of the product backlog is completed and delivered. The key tenets of the scrum sprint process include:

- Short implementation units (sprints).

- Prioritization of business and technical debt objectives in a product backlog.

- Time-bound planning for each sprint.

- Emphasis on the remaining work.

- Sprints that produce a releasable product increment.

- Sprint demonstrations that are time-restricted and have regular checkpoints.

- Automation approach and pipeline strategy.

- Zero downtime deployment strategy.

- Retrospective meetings that may be used for course correction.

Microsoft and \<Bosch\> will jointly take final decisions on the backlog and priorities for the contracted capacity and agreed sprint duration. At the conclusion of each sprint, there will be a sprint review and retrospective. These aim to demonstrate completed work and identify improvements.

## Delivery approach

The key phases, activities, \<Bosch\> dependencies, and assumptions for the delivery approach are described in the table below.

<table>
<caption><p>Table 4: Delivery approach</p></caption>
<colgroup>
<col style="width: 13%" />
<col style="width: 42%" />
<col style="width: 43%" />
</colgroup>
<thead>
<tr>
<th>Phase</th>
<th>&lt;MSFT&gt; activities</th>
<th>Key &lt;Bosch&gt; activities</th>
</tr>
</thead>
<tbody>
<tr>
<td>Project initiation</td>
<td><p>Initiation starts the project from a delivery perspective. This includes the activities required to effectively initiate, prepare, and plan the project with the &lt;MSFT&gt; and &lt;Bosch&gt; team members. The goals of this phase include:</p>
<ul>
<li><p>Conduct pre-initiation meeting and activities required before project kickoff such as establishing the core team, engagement pre-planning, etc. to confirm readiness of customer for project kickoff.</p></li>
<li><p>Conduct a kick-off meeting.</p></li>
<li><p>Review and confirm alignment with the SOW.</p></li>
<li><p>Document project prerequisites.</p></li>
<li><p>Prepare for product baseline planning.</p></li>
<li><p>Establish access to &lt;Bosch&gt; environment.</p></li>
</ul></td>
<td><ul>
<li><p>Attend and participate in initiation meetings.</p></li>
<li><p>Assign responsibilities to accountable &lt;Bosch&gt; leadership and establish target completion dates.</p></li>
<li><p>Staff the project with the required personnel in the time frames agreed upon during initiation.</p></li>
<li><p>Own and complete any orientation requirements for &lt;MSFT&gt; resources within the &lt;Bosch&gt; environment.</p></li>
<li><p>Provide &lt;MSFT&gt; team access to &lt;Bosch&gt; environment(s).</p></li>
<li><p>Provide &lt;MSFT&gt; team access to suitable work environment (building, internet, etc.).</p></li>
</ul></td>
</tr>
<tr>
<td>Product baseline planning</td>
<td><p>Product baseline planning creates a product roadmap or high-level plan. This may include defining the product objectives, major features, or functionality to be developed. This phase helps align the team on the overall direction, length, and available capacity for sprints to achieve the desired objectives. The goals of this phase include:</p>
<ul>
<li><p>Conduct Agile/scrum workshops.</p></li>
<li><p>Define the goal for the overall solution.</p></li>
<li><p>Define sprint duration, capacity, epics, and features.</p></li>
<li><p>Create a proposed backlog.</p></li>
<li><p>Define SLOs, SLIs, DOR, DOD, ORC, and BWBM.</p></li>
<li><p>Identify any impediments to efficient development.</p></li>
<li><p>Define a test strategy and plan for all in-scope testing (as defined in the <mark></mark><a href="#testing-and-defect-remediation">Testing and defect remediation</a> section).</p></li>
<li><p>Review project assumptions and document in the RAID log so these can be tracked and validated throughout the project. </p></li>
<li><p>Define any agreed upon work products to be delivered during sprints.</p></li>
</ul></td>
<td><ul>
<li><p>Determine who is responsible for environment setup and operations.</p></li>
<li><p>Identify a Product owner and project sponsor.</p></li>
<li><p>Attend and participate in workshops.</p></li>
<li><p>Provide background information, documentation, and business requirements.</p></li>
<li><p>Help remove any impediments.</p></li>
<li><p>Define a user acceptance testing (UAT) process.</p></li>
<li><p>Identify all security procedures and policies.</p></li>
<li><p>Jointly agree with &lt;MSFT&gt; on “definition of done”.</p></li>
</ul></td>
</tr>
<tr>
<td></td>
<td colspan="2"><p>Key assumptions:</p>
<ul>
<li><p>&lt;Bosch&gt; personnel in key roles are available and knowledgeable about the product.</p></li>
<li><p>&lt;Bosch&gt; is able to meet all responsibilities and requirements agreed to during project/sprint planning, in the timeframes agreed to between &lt;MSFT&gt; and &lt;Bosch&gt;.</p></li>
<li><p>The backlog will be refined during product baseline planning. This may result in changes to the overall scope and changes to required capacity.</p></li>
</ul></td>
</tr>
<tr>
<td>Delivery sprints</td>
<td><p>As described above, sprints will be used to deliver the product backlog items. Each delivery sprint will last no longer than four weeks. The final duration for sprints will be determined in collaboration with &lt;Bosch&gt; during product baseline planning. &lt;MSFT&gt; and &lt;Bosch&gt; will review delivered objectives after every sprint to determine whether updates are needed to the backlog or objectives. The goals of this phase include:</p>
<ul>
<li><p>Define clear sprint goals during sprint planning.</p></li>
<li><p>Assess user stories/PBIs for required information and capacity.</p></li>
<li><p>Conduct daily scrum meetings.</p></li>
<li><p>Design, plan, and implement PBIs.</p></li>
<li><p>Create and perform unit, functional, and system tests.</p></li>
<li><p>Assess PBI completion against remaining capacity.</p></li>
<li><p>At the end of a sprint, conduct a sprint review and sprint retrospective (see Section 2.4).</p></li>
</ul></td>
<td><ul>
<li><p>Attend daily scrum meetings.</p></li>
<li><p>Help refine PBIs and provide timely clarifications.</p></li>
<li><p>Collaborate with &lt;MSFT&gt; to update the product backlog for future sprints.</p></li>
<li><p>Support the &lt;MSFT&gt; team with deployments to the agreed-upon environments.</p></li>
<li><p>Provide input into backlog to prioritize solution design features required to meet industry-specific, business, and regulatory requirements.</p></li>
<li><p>If localization support is required, add it to the product backlog.</p></li>
<li><p>Conduct UAT on completed PBIs according to the UAT cycle defined in the release plan.</p></li>
<li><p>Identify items to be handled via automation.</p></li>
<li><p>Attend sprint reviews and provide feedback.</p></li>
</ul></td>
</tr>
<tr>
<td></td>
<td colspan="2"><p>Key assumptions:</p>
<ul>
<li><p>The &lt;Bosch&gt; representatives, especially the product owner, will be present for the entire duration of the sprints.</p></li>
<li><p>The product backlog will be updated as required in each sprint. This may result in changes to the overall scope and changes to required capacity. Any changes to scope or necessary capacity will be managed through the change management process described in this SOW.</p></li>
<li><p>Upon the completion of each delivery sprint, as part of the sprint review activity, the capacity available will be assessed with the &lt;Bosch&gt; product owner against the required capacity as per the backlog items. This might result in a change in contracted capacity/fees. This will be managed through the change management process described in this SOW.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Testing and defect remediation

Testing

The following kinds of testing are included in the project.

<table>
<caption><p>Table 5: Testing in scope</p></caption>
<colgroup>
<col style="width: 13%" />
<col style="width: 38%" />
<col style="width: 15%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr>
<th rowspan="2">Test type</th>
<th rowspan="2">Description</th>
<th colspan="3">Responsibility</th>
</tr>
<tr>
<th>Has responsibility for testing</th>
<th>Provides test data and test cases</th>
<th>Provides guidance and support</th>
</tr>
</thead>
<tbody>
<tr>
<td>Functional testing</td>
<td>Tests performed by a feature team within a delivery sprint to validate that the product features function in accordance with the acceptance criteria defined per PBIs.</td>
<td>Feature team</td>
<td>Feature team</td>
<td>&lt;MSFT&gt;</td>
</tr>
<tr>
<td>Non-functional testing</td>
<td>Tests performed on the system or components of the system to validate their respective adherence to non-functional requirements in different, expected, operational conditions. These include, but are not limited to: performance, load endurance, and stress testing. These tests should exercise the system or component and results should include metrics gathered from monitoring and other operational observability sources.</td>
<td>&lt;MSFT&gt;</td>
<td>&lt;MSFT&gt;</td>
<td>&lt;MSFT&gt;</td>
</tr>
<tr>
<td>System testing</td>
<td>Tests performed to validate that the deployed solution operates as designed, across functionality delivered by different feature teams.</td>
<td>&lt;Bosch&gt;</td>
<td>&lt;Bosch&gt;</td>
<td>&lt;Bosch&gt;</td>
</tr>
<tr>
<td>UAT</td>
<td>UAT will be conducted over the course of the project according to the UAT time frames agreed upon during product baseline planning (as described in the product baseline planning phase in ). Feedback from UAT (defect or additional PBIs) and other product backlog items will be prioritized in the product backlog.</td>
<td>&lt;Bosch&gt;</td>
<td>&lt;Bosch&gt;</td>
<td>&lt;MSFT&gt;</td>
</tr>
</tbody>
</table>

**Defect remediation**

If possible, any defects the feature team finds during a delivery sprint are fixed within the sprint itself. Defects that cannot be resolved during the sprint will be added to the product backlog. Defects found elsewhere, will be prioritized and become part of the product backlog for the feature team.

Microsoft will address any testing scope exceeding available allocated capacity for resources or timeline. This will trigger the change management process.

During testing, <span class="mark">\<Bosch\></span> ​and Microsoft will jointly evaluate solution-related defects and their severity based on the following definitions. Defects in each severity level will be remediated in priority order, where possible. Defects with the same severity will be prioritized in partnership with <span class="mark">\<Bosch\></span>.  

**Priority **

The priority is a rating of the defect as it relates to the business or <span class="mark">\<Bosch\></span> ​ requirements. Priority indicates the order in which code defects should be fixed. 

<table style="width:100%;">
<caption><p>Table 8: Defects priority definitions </p></caption>
<colgroup>
<col style="width: 10%" />
<col style="width: 59%" />
<col style="width: 29%" />
</colgroup>
<thead>
<tr>
<th>Priority </th>
<th>Description </th>
<th>Remediation in scope? </th>
</tr>
</thead>
<tbody>
<tr>
<td>P1 </td>
<td><p>Blocking defect  </p>
<p>Development, testing, or production launch cannot proceed until this type of defect is corrected. A defect of this type blocks further progress in this area. The solution cannot ship, and the project team cannot achieve the next milestone until such a defect is corrected. </p></td>
<td>Yes </td>
</tr>
<tr>
<td>P2 </td>
<td><p>Significant defect </p>
<p>The defect must be fixed prior to moving to production. Such a defect, however, will not affect test plan implementation. </p></td>
<td>Yes </td>
</tr>
<tr>
<td>P3 </td>
<td><p>Important defect </p>
<p>It is important to correct the defect. However, it is possible to move forward into production using a workaround. </p></td>
<td>No; the defect will be logged. Remediation will be performed through an agreed-upon change request only. </td>
</tr>
<tr>
<td>P4 </td>
<td><p>Enhancements and cosmetic defects </p>
<p>Feature enhancement and cosmetic defects, including design requests that vary from original concepts. </p></td>
<td>No; the defect will be logged. Remediation will be performed through an agreed-upon change request only. </td>
</tr>
</tbody>
</table>

**Severity **

A rating of the impact of a defect on the project. 

<table style="width:100%;">
<caption><p>Table 9: Defect severity definitions </p></caption>
<colgroup>
<col style="width: 13%" />
<col style="width: 86%" />
</colgroup>
<thead>
<tr>
<th>Severity </th>
<th>Severity definition </th>
</tr>
</thead>
<tbody>
<tr>
<td>S1 (Severe) </td>
<td>This type of defect causes a crash or stop responding and may destroy files or cause serious data corruption or loss. </td>
</tr>
<tr>
<td>S2 (Major) </td>
<td>This is a serious defect in the functionality of the solution. This type of defect causes the software to operate contrary to the acceptance criteria or may cause data loss. </td>
</tr>
<tr>
<td>S3 (Minor) </td>
<td><p>This is a minor defect, with no risk of data loss or major functionality issues. This type of defect causes the feature to operate contrary to feature specifications to some extent; however, a workaround exists. </p>
<p>It is advisable to fix the defect; however, the solution can perform its intended functionality with a workaround. Therefore, it, can be fixed after going live. </p></td>
</tr>
<tr>
<td>S4 (Trivial-cosmetic) </td>
<td>This type of defect is primarily a cosmetic problem or consists of other small distractions that do not impact the intended functionality. However, the impairment could lead to dissatisfaction from a user experience perspective. </td>
</tr>
</tbody>
</table>

Note: S3 and S4 defects will be logged and <span class="mark">\<Bosch\></span> ​can choose to schedule remediation using the change management process described in in this SOW. S3 and S4 defects, however, will not be corrected by default as part of this SOW. 

Note: Product bugs and design change requests (DCRs) are not in the scope of this SOW. Product-related problems must be addressed separately through a Premier support agreement. 

## Sprint completion

Sprints will end based on the calendar schedule defined during product baseline planning. At the conclusion of each sprint, feature teams will conduct a sprint review and sprint retrospective.

- **Sprint review:** A sprint review meeting, which is a single meeting held at the end of the sprint to evaluate the progress of the sprint and adapt the product backlog if needed. The \<Bosch\> product owner (mandatory) and \<Bosch\> stakeholders (optional but recommended) will attend. During the sprint review, the following work products will be reviewed:

<table style="width:100%;">
<caption><p>Table 6: Sprint review work products</p></caption>
<colgroup>
<col style="width: 20%" />
<col style="width: 79%" />
</colgroup>
<thead>
<tr>
<th>Name </th>
<th>Description </th>
</tr>
</thead>
<tbody>
<tr>
<td>Sprint completion report </td>
<td><p>This report lists the in-scope items that have been completed during the sprint, any planned work that was not completed, and any engagement risks or problems.</p>
<p>Note: The sprint completion report is created from information within Azure DevOps<em>.</em> </p></td>
</tr>
<tr>
<td>Latest Product Roadmap and Burn-Up Chart </td>
<td><p>This row is optional and should be considered for larger programs and where the capacity has been included in project estimates.</p>
<p>This document shows the capacity expended per business objectives desired. It will provide awareness to the project team and stakeholders on where in the roadmap the engagement is and how much capacity has been expended per product objective.   </p></td>
</tr>
<tr>
<td><strong>Capacity Burndown Chart</strong> </td>
<td>A document showing the consumed capacity relative to the total capacity burndown of the project. </td>
</tr>
</tbody>
</table>

- **Sprint retrospective**: A sprint retrospective, which is an opportunity for the scrum team to evaluate its progress and determine if there are any improvements that need to be made during the next sprint. 

At the end of each sprint, \<MSFT\> will provide a sprint completion report. Backlog items do not require formal sign-off or \<Bosch\> acceptance when they are completed by the feature team.

## Project completion

\<MSFT\> will provide services defined in this SOW during the term specified in the WO. If additional services are required, the change management process will be followed, and the contract modified. The project will be considered complete when at least one of the following conditions has been met:

- All available capacity has been utilized for services delivered.

- The term of the project has expired.

- All \<MSFT\> activities and product backlog items have been completed.

- The WO has been terminated.

Due to the nature of Agile delivery, not all backlog items or objectives may be completed during the project. The \<MSFT\> team will rely on the \<Bosch\> product owner in conjunction with the product council to determine priority of the product backlog so that the important backlog items can be completed during the project.

## Timeline

The timeline for this project is relative to the project start date. All dates and durations provided are estimates only. The estimated timeline is based upon the assumption of uninterrupted delivery from the start of the engagement. In addition, it is based on the assumptions outlined throughout this SOW. If there are delays to the schedule of the engagement or if the assumptions are incorrect, a change request may be used following the change control process described in this SOW to extend the timeline and potentially add cost to \<Bosch\>.

\<MSFT\> will provide the \<MSFT\> team described in the <span class="mark"></span>[*Project organization*](#project-organization) section until the capacity defined in the <span class="mark"></span>[*Project capacity*](#project-capacity) section is consumed. The specific timeline will be finalized during product baseline planning with \<Bosch\> and will be updated as part of delivery sprint approach activities.

The high-level timeline of the project is depicted in the following graphic, with an estimated delivery time-frame of 26 weeks:

<img src="media/image5.emf" style="width:6.5in;height:0.50069in" />

<figure>
<img src="media/image6.emf" />
<figcaption><p><span id="_Toc227840189" class="anchor"></span>Figure 1: High-level timeline</p></figcaption>
</figure>

# Project organization

## Project capacity

The role descriptions for each area in the project organization are shown in the roles and responsibilities table in the sections that follow.

Guidance from 4.2.2.1. Fixed Fee Guidelines - Option 1: Capacity as Story Points

## Project staffing

The role descriptions are shown in the table below.

<table>
<caption><p>Table 7: Project staffing - &lt;Bosch&gt;</p></caption>
<colgroup>
<col style="width: 19%" />
<col style="width: 80%" />
</colgroup>
<thead>
<tr>
<th>Role</th>
<th>Responsibilities / notes</th>
</tr>
</thead>
<tbody>
<tr>
<td>&lt;Bosch&gt; executive sponsor</td>
<td><ul>
<li><p>Participates in the executive steering committee.</p></li>
<li><p>Serves as a point of escalation to support clearing project roadblocks.</p></li>
<li><p>Serves as a final arbiter of project issues or escalations.</p></li>
<li><p>Makes decisions about the project strategic direction.</p></li>
<li><p>Approves significant change requests.</p></li>
<li><p>2 hours per week</p></li>
</ul></td>
</tr>
<tr>
<td>Project owner</td>
<td><ul>
<li><p>Serves as the &lt;Bosch&gt; single point of contact and is accountable for the project.</p></li>
<li><p>Interacts with executive sponsors from Microsoft.</p></li>
<li><p>Routinely engages with the Microsoft delivery management executive or program director.</p></li>
<li><p>Make key project decisions, serve as a point of escalation, and work to eliminate the &lt;Bosch&gt;-related issues hindering or impeding implementation.</p></li>
<li><p>1 day per week</p></li>
</ul></td>
</tr>
<tr>
<td>Project manager</td>
<td><ul>
<li><p>Oversees and coordinates the overall program decisions / schedule / budget / status.</p></li>
<li><p>Coordinates &lt;Bosch&gt; resources and drives &lt;Bosch&gt; internal processes necessary to deliver the program.</p></li>
<li><p>Communicates the project efforts and activities to the &lt;Bosch&gt; executive committee members and stakeholders.</p></li>
<li><p>Fulltime</p></li>
</ul></td>
</tr>
<tr>
<td>Product owner</td>
<td><ul>
<li><p>Serves as the single point of contact for decisions about product backlog items and prioritization. </p></li>
<li><p>Takes responsibility for making decisions on services and/or product features.</p></li>
<li><p>Serves as the primary person responsible for user story scope decisions during sprint planning.</p></li>
<li><p>Defines acceptance criteria for work items, especially user stories.</p></li>
<li><p>Actively participates in all sprint reviews.</p></li>
<li><p>Serves as the single point of contact for decisions about product backlog items and prioritization.</p></li>
<li><p>Reviews and approves test scripts to confirm test scripts are accurate, complete, and cover the scenarios required to do functional, E2E, and UAT testing.</p></li>
<li><p>Takes responsibility for planning UAT and providing appropriate &lt;Bosch&gt; resources across sprints for testing.</p></li>
<li><p>Provides &lt;MSFT&gt; teams with prompt answers to questions affecting development activities and, more generally, services to be delivered.</p></li>
<li><p>Fulltime</p></li>
</ul></td>
</tr>
<tr>
<td>Business stakeholders</td>
<td><ul>
<li><p>Provides direction on business objectives.</p></li>
<li><p>Maintains communication with &lt;Bosch&gt; personnel assigned to feature teams (for example, SMEs).</p></li>
<li><p>Responsible for UAT.</p></li>
<li><p>Fulltime during testing</p></li>
</ul></td>
</tr>
<tr>
<td>Development and Test Team</td>
<td><ul>
<li><p>Work MSFT team on development and testing activities</p></li>
<li><p>Extend the Assistant solution to the selected Devices</p></li>
<li><p>Test and Evaluate the solution</p></li>
</ul></td>
</tr>
</tbody>
</table>

<table>
<caption><p>Table 8: Project staffing – &lt;MSFT&gt;</p></caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 74%" />
</colgroup>
<thead>
<tr>
<th>Role</th>
<th>Responsibilities / notes</th>
</tr>
</thead>
<tbody>
<tr>
<td>Microsoft executive sponsor</td>
<td><ul>
<li><p>Participates in the executive steering committee.</p></li>
<li><p>Serves as a point of escalation to support clearing project roadblocks.</p></li>
<li><p>Serves as a final arbiter of project issues or escalations.</p></li>
</ul></td>
</tr>
<tr>
<td>Delivery management executive</td>
<td><ul>
<li><p>Oversees all service delivery projects with &lt;Bosch&gt;.</p></li>
<li><p>Make key project decisions, serve as a point of escalation, and clears project roadblocks.</p></li>
<li><p>Serves as an escalation point for delivery issues to Microsoft senior leadership.</p></li>
<li><p>Approves significant change requests.</p></li>
</ul></td>
</tr>
<tr>
<td>Project manager</td>
<td><ul>
<li><p>Serves as the single point of contact and is accountable for service delivery.</p></li>
<li><p>Leads project quality reviews with the &lt;Bosch&gt; executive sponsor to assist with “conditions of satisfaction.”</p></li>
<li><p>Oversees and coordinates the overall &lt;MSFT&gt; project and delivers it on schedule.</p></li>
<li><p>Takes responsibility for &lt;MSFT&gt; resource allocation, risk management, project priorities, and communication to executive management.</p></li>
<li><p>Coordinates decisions within three business days, or according to an otherwise agreed-upon timeline.</p></li>
</ul></td>
</tr>
<tr>
<td>Data Scientist Lead / Architect</td>
<td rowspan="2"><ul>
<li><p>Defines the product vision and strategy, including OKRs, to provide clarity, focus, and alignment with strategic &lt;Bosch&gt; priorities and desired business objectives. </p></li>
<li><p>Takes responsibility for the alignment with the strategy and objectives communicated by the product council if one is present in the project.</p></li>
<li><p>Manages and prioritizes the product backlog.</p></li>
<li><p>Serves as the primary person responsible for user story/PBI backlog decisions during sprint planning.</p></li>
<li><p>Serves as the single point of contact for decisions about PBIs and prioritization.</p></li>
<li><p>Defines validation criteria for work items, especially user stories.</p></li>
<li><p>Actively participates in all sprint ceremonies.</p></li>
<li><p>Takes responsibility for planning validation testing.</p></li>
<li><p>Serves as a member of the product council, if present.</p></li>
<li><p>Partners with &lt;Bosch&gt; to understand business needs and solution requirements and assists with technical governance.</p></li>
<li><p>Helps evaluate implications of trade-off decisions to prioritize product backlog.</p></li>
<li><p>Sets the strategic direction for the architecture of the products being developed.</p></li>
<li><p>Leads the product council from a technical perspective.</p></li>
<li><p>Within the scope of a feature team and for an individual product, serves as the technical person responsible for user story/PBI decisions during sprint planning and defines validation criteria for work items.</p></li>
<li><p>Facilitates conversations between various product stakeholders so that the product managers can make informed decisions.</p></li>
<li><p>Facilitates DevOps standardization (for example, DevOps taxonomy and DevOps principles and practices).</p></li>
<li><p>Provides &lt;Bosch&gt; with technical advice regarding the Microsoft cloud.</p></li>
<li><p>Collaborates with &lt;Bosch&gt; to define the set of security and data protection principles to which the project must adhere.</p></li>
<li><p>Reviews solution architecture and design to identify design-related security issues.</p></li>
<li><p>Serves as the technical person responsible for user story / PBI backlog decisions during sprint planning and defines validation criteria for work items.</p></li>
<li><p>Helps the product managers prioritize and manage the product backlog.</p></li>
<li><p>Facilitates conversations between product stakeholders so that the product managers can make informed decisions.</p></li>
<li><p>Reviews technical designs from feature teams to determine compliance.</p></li>
<li><p>Reviews results of security tests performed on a working test environment.</p></li>
</ul></td>
</tr>
<tr>
<td></td>
</tr>
<tr>
<td>Engineer</td>
<td><ul>
<li><p>Takes responsibility for design, implementation, test, and deployment to production following DevOps principles.</p></li>
<li><p>Participates in all sprint reviews.</p></li>
<li><p>Designs and builds pipelines and components that pull data from, transform data, and write to persistent storage.</p></li>
<li><p>Monitors and debugs the pipelines.</p></li>
<li><p>Performs unit and data integration testing.</p></li>
<li><p>Designs intuitive and user-friendly interfaces for the application</p></li>
<li><p>Conducts user research and gathers feedback to understand user needs</p></li>
<li><p>Creates prototypes and wireframes to visualize the application's layout and functionality</p></li>
<li><p>Works closely with data scientists, and other stakeholders to validate the design aligns with the application's requirements and user needs.</p></li>
<li><p>Conducts usability testing and validates the application is responsive and works well across different devices and screen sizes.</p></li>
<li><p>Plans, develops, and executes performance test scripts.</p></li>
<li><p>Performance tools and monitoring setup and configuration.</p></li>
<li><p>Shares &lt;MSFT&gt; -preferred practices and guidance</p></li>
</ul>
<p>Note: The mix of feature team engineering skills may vary throughout the project, depending on work requirements.</p></td>
</tr>
<tr>
<td>Data scientist <mark></mark></td>
<td><ul>
<li><p>Works directly with the &lt;Bosch&gt; product planning analyst.</p></li>
<li><p>Creates the scope and design of the analytical solution.</p></li>
<li><p>Provides guidance to the data science team.</p></li>
<li><p>Provides technical oversight of the modeling process.</p></li>
<li><p>Takes responsibility for developing, testing, and validating any custom ML models.</p></li>
<li><p>Works closely with the &lt;MSFT&gt; architect.</p></li>
<li><p>Participates in engagement baseline planning.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Executive steering committee

The executive steering committee provides overall senior management oversight and strategic direction for the project. In addition, it removes obstacles for the project team. The executive steering committee for the project will meet with the frequency defined in the communication plan and will include the roles listed in the following table. This is typically on a monthly or bi-weekly basis.

| Role                                | Responsible party       |
|-------------------------------------|-------------------------|
| Executive sponsor                   | \<Bosch\> and Microsoft |
| Delivery Management Executive (DME) | Microsoft               |
| \<Bosch\> Product Owner             | \<Bosch\>               |
| Project Manager                     | \<MSFT\>                |
| Data Scientist Lead / Architect     | \<MSFT\>                |

Table 9: Executive steering committee roles

## Product council

The product council is the primary mechanism for aligning stakeholders and dealing with competing priorities. It acts as the forum where the strategy is agreed upon so that all key decision makers understand what decisions are being made about the direction of the product and why. The product council allows the feature teams to maintain autonomy while simultaneously determining the overall priorities for business objectives.

<figure>
<img src="media/image7.emf" />
<figcaption><p><span id="_Toc194478203" class="anchor"></span>Figure 2: Product council</p></figcaption>
</figure>

Ultimately, the product council is formed to define and share the product strategy and roadmap. It also makes decisions needed to resolve any conflicting product priorities.

All product managers and technical leads from the individual feature teams are also members of the product council.

| Role                    | Responsible party |
|-------------------------|-------------------|
| \<Bosch\> product owner | \<Bosch\>         |
| Technical lead          | \<MSFT\>          |

Table 10: Product council roles

## Feature team

Following the scrum model, \<MSFT\> uses a feature team approach to deliver a project. All scrum roles will be represented within the feature team. This team is an autonomous and empowered unit that has all the capabilities to design, develop, test, and release features to achieve the \<Bosch\> objectives. A feature team consists of a product manager, scrum master, technical lead, SMEs, and engineers with various development, test, deployment, infrastructure, security, data, and operation skills.

The roles listed below are typical and representative for feature teams, though they may differ, depending on the project. The skill sets of the engineers will also be different, depending on the project.

| Role                            | Responsible party |
|---------------------------------|-------------------|
| Project Manager                 | \<MSFT\>          |
|                                 |                   |
|                                 |                   |
| Data Scientist Lead / Architect | \<MSFT\>          |
| Data Scientist                  | \<MSFT\>          |
| Engineer                        | \<MSFT\>          |

Table 11: Feature team roles

# Project governance

The governance structure and processes the team will abide by for the project are described in the following sections.

## Project communication

In addition to the communications mechanisms built into the delivery approach, the \<MSFT\> team will prepare regular status reports and conduct regular status meetings to review project progress. The frequency of each will be defined in the project communication plan.

## Risk and issue management

Risks and issues will be identified, analyzed, prioritized, managed, escalated, and tracked during the project. Active issues and risks will be monitored and reassessed every week.

## Change management process

During the project either party may request in writing additions, deletions, or modifications to the services described in this document (“change”). We will have no obligation to commence work in connection with any change until the estimated fee and schedule impact of the change is agreed upon in a written amendment signed by the authorized signatories from both parties.

Within three (5) consecutive business days of receipt, you will either indicate acceptance of the proposed change by confirming via email that you will proceed with approval and signature of the amendment, or advise us not to perform the change. If you advise us not to perform the change, then we will proceed only with the original services. In the absence of your acceptance or rejection, we will not perform the proposed change.

## Escalation path

The product managers, executive sponsors, and other designees will work closely together to manage project issues, risks, and change requests as described previously. \<Bosch\> will provide reasonable access to the sponsor or sponsors to expedite resolution. The standard escalation path for review, approval, or dispute resolution is as follows:

- Feature team members

- Project Manager

- \<Bosch\> product owner

- Product council

- \<Bosch\> project owner and Microsoft delivery management executive

- Executive steering committee

# Exhibits

## Initial targeted product backlog

The following files are referenced in this document and are included as part of this SOW, priorities of the items in the feature list can be adjusted during project execution.

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 44%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;">Level 1</th>
<th style="text-align: center;">Level 2</th>
<th style="text-align: center;">Level 3</th>
<th style="text-align: center;">Level 4</th>
<th style="text-align: center;">Level 5</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="14" style="text-align: center;"><strong>Basic</strong></td>
<td rowspan="2">Wakeup</td>
<td style="text-align: center;">Basic Wake-up</td>
<td style="text-align: center;"> </td>
<td>we should able to add custom words like "Hey Bosch" "Hey Lucid" etc</td>
</tr>
<tr>
<td style="text-align: center;">Wake-up Confidence Differentiation</td>
<td style="text-align: center;">Wake-up Confidence Differentiation</td>
<td>Support differentiation of wake-up confidence, configurable different wake-up responses, e.g., when wake-up confidence is not very high, respond "Are you calling me?", high confidence wake-up responds "I'm here"</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Speech Recognition</td>
<td style="text-align: center;">Speech To Text</td>
<td style="text-align: center;">Mix-Language</td>
<td>Supports mix with English (Names)</td>
</tr>
<tr>
<td style="text-align: center;">Dynamic VAD</td>
<td style="text-align: center;">Dynamic VAD</td>
<td>Support intelligent sentence assembly, use model (not rules) to determine if user input is complete, dynamically adjust VAD to wait when user input is incomplete, support intelligent splicing of fragmented sentences for correct semantic understanding. Need to support half-sentence recognition for voice and AI Agent domains.<br />
Example: I want to listen...Jay Chou...songs, turn on...that...wiper<br />
<br />
This will be built only for demo purpose, not ready for production.</td>
</tr>
<tr>
<td rowspan="6" style="text-align: center;">Voice Broadcast</td>
<td rowspan="2" style="text-align: center;">TTS Voice</td>
<td style="text-align: center;">TTS Voice Type</td>
<td>Provide super-realistic TTS voices based on LLM, provide three super-realistic basic voices: female, male, and child, plus other special voices</td>
</tr>
<tr>
<td style="text-align: center;">TTS Voice Consistency</td>
<td>Support other system parties to call TTS voice, making other scenario broadcasts consistent with system voice (e.g., navigation)</td>
</tr>
<tr>
<td style="text-align: center;">Custom Persona</td>
<td style="text-align: center;"> </td>
<td>1) Support user self-creating assistant persona, then pass persona requirements to LLM for persona dialogue generation, user can regenerate if not satisfied<br />
2) Reply in corresponding style based on user interaction content<br />
<br />
Cloud Only</td>
</tr>
<tr>
<td style="text-align: center;">Repeat Broadcast</td>
<td style="text-align: center;">Repeat Broadcast</td>
<td>Allow user to input "say it again" command in various voice broadcast scenarios, after hearing or during broadcast, voice assistant repeats previous or current broadcast, allowing continuous "say it again" commands</td>
</tr>
<tr>
<td style="text-align: center;">Broadcast Style Based on Cabin Member Identity</td>
<td style="text-align: center;">Broadcast Style Based on Cabin Member Identity</td>
<td>① System can remember and auto-switch member's preferred voice broadcast style based on cabin member identity (supporting OMS and voiceprint info). Support multi-dimensional adaptation including broadcast style, speech rate, tone, vocabulary register; personalized config can be manually set or system-learned from interaction history.<br />
② When cabin personnel identity cannot be recognized, support age-based differentiated voice broadcast, using friendly tone, simple wording, slower speed for children, clear pronunciation and appropriately slower speed for elderly, supporting multi-dimensional adaptation</td>
</tr>
<tr>
<td style="text-align: center;">AI Generated NLG</td>
<td style="text-align: center;"> </td>
<td>Use AI-generated NLG scripts in various skills and Agents, combining user identity, input, and status to generate different types of varied NLG reply content, reducing mechanical feel of manually written scripts<br />
<br />
text is generated from edge but NLG voice happy voice is cloud option for different voices</td>
</tr>
<tr>
<td style="text-align: center;">Voice and Vehicle Application Control</td>
<td style="text-align: center;">Voice and Vehicle Application Control</td>
<td style="text-align: center;">Voice and Vehicle Application Control</td>
<td>① Support voice control of vehicle system applications and body functions as much as possible, including vehicle control, navigation, voice settings, Bluetooth phone, system settings, music, video, radio, audiobooks, news, playback control, energy center, schedule management, VPA settings, SR, smart scene creation, comfort mode, AIOT, AVM and related voice control<br />
② Need to support control requirements for different vehicle configurations, such as passenger screen, rear screen, various optional packages, etc.</td>
</tr>
<tr>
<td style="text-align: center;">Voice Q&amp;A Function</td>
<td style="text-align: center;">Voice Q&amp;A Function</td>
<td style="text-align: center;">Voice Q&amp;A Function</td>
<td>Voice Q&amp;A capabilities include: weather, stocks, news, persona Q&amp;A, screenshot image interpretation, fuzzy expression guidance, etc.</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Voice GUI</td>
<td style="text-align: center;">Voice GUI Interface Interaction</td>
<td style="text-align: center;">Voice GUI Interface Interaction</td>
<td rowspan="2">Avatar api sare available Bosch : will develop the ui layer and integration</td>
</tr>
<tr>
<td style="text-align: center;">Voice VPA</td>
<td style="text-align: center;">Voice VPA</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;"><strong>AI Semantic Hub</strong></td>
<td rowspan="2" style="text-align: center;">AI Semantic Hub</td>
<td style="text-align: center;">Fast-Slow Thinking Combination</td>
<td style="text-align: center;">Fast-Slow Thinking Combination</td>
<td>Use fast-slow thinking combination approach:<br />
① Traditional voice commands support fast thinking for quicker parsing and execution;<br />
② Commands requiring LLM parsing use LLM thinking for more comprehensive and accurate responses;<br />
③ Based on user requests, e.g., user actively requests "think carefully..." "your answer is wrong, think again carefully", need to activate LLM deep thinking for higher quality responses after deep thinking</td>
</tr>
<tr>
<td style="text-align: center;">Understanding Coverage</td>
<td style="text-align: center;">Understanding Coverage</td>
<td>① Need to understand traditional voice NLU related semantic content<br />
② Need to understand various AI agent related semantic commands, including other suppliers or Dongfeng Nissan self-developed AI agents, ensure unified understanding and distribution</td>
</tr>
<tr>
<td rowspan="12" style="text-align: center;"><strong> </strong></td>
<td rowspan="12"> </td>
<td rowspan="3" style="text-align: center;">Language Understanding, Emotion, Tone Perception</td>
<td style="text-align: center;">Language Understanding</td>
<td>When understanding different languages, need to support automatic language detection and auto-switch response based on user input language</td>
</tr>
<tr>
<td style="text-align: center;">Emotion Perception</td>
<td>Can recognize emotions in user input audio, including happiness, sadness, anger, surprise, fear, disgust, and extended emotions like relaxation, anxiety, fatigue, boredom, excitement, calm, etc. When user says "stuck in traffic again, so annoying" "can you even understand human speech", automatically adjust emotional expression and speech rate in subsequent responses</td>
</tr>
<tr>
<td style="text-align: center;">Tone Perception</td>
<td>Can recognize different tone expressions under same wording, e.g., "I'm really so lucky today" spoken normally vs sarcastically may have completely opposite meanings, need to combine user's tone for judgment and response</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Multi-modal Input</td>
<td style="text-align: center;">Audio Understanding</td>
<td>Support direct understanding and response based on user's audio input</td>
</tr>
<tr>
<td style="text-align: center;">Websearch Information Integration</td>
<td>Support integration of websearch information for understanding and response</td>
</tr>
<tr>
<td style="text-align: center;">Voice Customization</td>
<td style="text-align: center;">Voice Customization</td>
<td>Understand user's TTS-related requirements in commands, e.g.: "speak quieter, can you be gentler, can you talk like Michael Jackson, can you talk like a kitten", generate corresponding TTS voice, literary style based on understanding of user's expression</td>
</tr>
<tr>
<td rowspan="4" style="text-align: center;">TTS Output</td>
<td style="text-align: center;">TTS Humming &amp; Animal Sound Simulation</td>
<td>Support TTS humming mode and animal sound simulation, can switch display per user request, e.g., "can you hum Hey Jude" "do you know how a groundhog sounds"</td>
</tr>
<tr>
<td style="text-align: center;">Automatic Voice Tone Adjustment</td>
<td>Identify member status through in-car camera (e.g., child sleeping, drowsy), lower voice tone volume (for vehicles without headrest speakers)<br />
<br />
Cloud Only</td>
</tr>
<tr>
<td style="text-align: center;">Whisper Mode</td>
<td>When user speaks to voice assistant in whisper tone, voice assistant also responds in whisper tone<br />
<br />
Cloud Only</td>
</tr>
<tr>
<td style="text-align: center;">TTS Emotion Label Output</td>
<td>Support outputting TTS associated emotion labels to software that needs them during TTS output (e.g., if user is not in good mood today, end-to-end voice interacts with concerned tone, need to output emotion label to VPA for corresponding expression action)<br />
<br />
Cloud Only</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">End-to-End Coverage Scope</td>
<td style="text-align: center;">Casual Chat End-to-End</td>
<td>Step1 Support emotional chat (non-closed domain solution, support free switching with other domains)</td>
</tr>
<tr>
<td style="text-align: center;">Casual Chat + Partial Control End-to-End</td>
<td>Step2 Support casual chat + vehicle control/system control and other high-frequency domain functions (same non-closed domain)</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;"><strong>Encyclopedia Agent</strong></td>
<td rowspan="2" style="text-align: center;">Encyclopedia Q&amp;A</td>
<td rowspan="2" style="text-align: center;">Encyclopedia Q&amp;A</td>
<td style="text-align: center;">Accurate Domain Recognition &amp; Web Search</td>
<td>① Based on user expression, can accurately arbitrate which expressions need web encyclopedia search to give responses that better meet user needs, and support domain intervention and quick fixes per OEM requirements<br />
② Accurately understand domain expressions and actively search web encyclopedia content</td>
</tr>
<tr>
<td style="text-align: center;">Encyclopedia Sources</td>
<td>① Use industry-leading and reliable encyclopedia sources to ensure accuracy and timeliness of encyclopedia content, e.g., "current oil price" needs accurate answer; "important European sports events results in past week" must use latest web info for most current and accurate information<br />
② Based on different encyclopedia question types, can perform targeted search summaries from more professional, more timely websites for different domains, e.g., serious knowledge prioritizes Quora, encyclopedia info prioritizes Wikipedia sites, entertainment info prioritizes entertainment sites, life encyclopedia prioritizes Reddit, company/institution queries prioritize official website content, etc.</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;"><strong>Vehicle Usage Advisor</strong></td>
<td style="text-align: center;"> </td>
<td style="text-align: center;">Knowledge Scope</td>
<td style="text-align: center;"> </td>
<td>Support user questions on 4 types of vehicle-related knowledge:<br />
1. General knowledge: traffic rules, emergency handling, common vehicle knowledge points, Dongfeng Nissan company knowledge, or model marketing highlights, etc.<br />
2. Dedicated model custom knowledge, support user questions with response text, images and videos<br />
3. Model after-sales and maintenance knowledge<br />
4. Any other vehicle usage related questions</td>
</tr>
<tr>
<td style="text-align: center;"> </td>
<td style="text-align: center;">Information Support</td>
<td style="text-align: center;"> </td>
<td>Provide the action to be executed or informaiton to be displayed based on the user's query, e.g.: image for vehicle information</td>
</tr>
<tr>
<td rowspan="10" style="text-align: center;">Vehicle Control</td>
<td rowspan="2" style="text-align: center;">Standard Control</td>
<td style="text-align: center;">Car Control</td>
<td style="text-align: center;"> </td>
<td>All the available car controls (AC, Winodw, Door, Sunroof, Seat, etc.)</td>
</tr>
<tr>
<td style="text-align: center;">Entertainment</td>
<td style="text-align: center;"> </td>
<td>Navigation, Music, Radio, Phone, etc.</td>
</tr>
<tr>
<td rowspan="6" style="text-align: center;">Fuzzy Control</td>
<td rowspan="5" style="text-align: center;">Fuzzy Expression Understanding</td>
<td style="text-align: center;">Temperature Adjustment Expressions</td>
<td>E.g.: "Make it cooler in the car, but don't blow AC wind at the child"<br />
This expression indicates user needs to adjust body temperature, needs to relate to in-car ambient temperature, fan speed, wind direction adjustment capabilities</td>
</tr>
<tr>
<td style="text-align: center;">Volume Adjustment Expressions</td>
<td>E.g.: "It's too noisy in the car now, be quieter"<br />
This expression indicates user needs to adjust in-car ambient noise, need to combine current in-car music volume, navigation volume, speed, window opening to confirm actual noise source, and relate to music volume, navigation volume, window opening adjustment capabilities</td>
</tr>
<tr>
<td style="text-align: center;">Driving Experience Adjustment Expressions</td>
<td>E.g.: Driver says "I'm a bit tired now"<br />
This expression represents user is currently fatigued from driving, needs to relate to navigation service area search, sunroof open/close, window open/close, AC circulation mode, car fragrance machine for adjustment</td>
</tr>
<tr>
<td style="text-align: center;">Entertainment Expressions</td>
<td>"We're a bit bored now, find us some fun"<br />
This expression indicates user needs entertainment services, needs to relate to video, e-books, radio, news, in-car games, voice interactive mini-games and other services</td>
</tr>
<tr>
<td style="text-align: center;">Free-form<br />
Function Commands</td>
<td>1) Vehicle control Agent can quickly understand and respond to user's direct requests for vehicle control functions, not limited to specific vocabulary or command formats.<br />
2) Control scope: seats (ventilation, heating, massage, on/off/mode/level), steering wheel (heating), AC (temperature, fan speed, mode, internal/external circulation, air purification), windows and sunroof (on/off and opening degree), wipers, defog, music, etc.<br />
3) Examples: "open the window a bit", "heat up the seat", "this song is terrible", "wiper move once"</td>
</tr>
<tr>
<td style="text-align: center;">Vehicle Capability Understanding</td>
<td style="text-align: center;">——</td>
<td>1) Vehicle control Agent can understand and respond to user's potential vehicle control needs expressed through describing personal feelings or problems encountered, without requiring user to explicitly point to specific functions. Based on user preferences, vehicle status (seat sensors, seatbelts, etc.), actual in-car/external environment status, Vehicle control Agent needs to quickly decompose the most suitable function combination.<br />
2) Control scope: seats (ventilation, heating, massage, on/off/mode/level), steering wheel (heating), AC (temperature, fan speed, mode, internal/external circulation, air purification), windows and sunroof (on/off and opening degree), wipers, defog, music, etc.<br />
3) Examples: "can't see the glass clearly", "sunlight is blinding", "too sunny", "my butt is burning", "kids are being noisy", "let the air circulate in the car", "don't disturb the child", "hands are cold", "things are going to melt"</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Feedback Adjustment</td>
<td rowspan="2" style="text-align: center;">User Active Feedback Adjustment</td>
<td style="text-align: center;">Service Content Adjustment</td>
<td>Need to present reasoning service content results to user through interface (e.g., list), support user to input limiting conditions again within certain time via commands like "watching movies isn't suitable while driving", adjust service plan, or adjust through touch GUI interaction, and display recommendation plan in list on GUI.</td>
</tr>
<tr>
<td style="text-align: center;">Service Interruption</td>
<td>For proactively popped up and executed services, allow user to interrupt and cancel</td>
</tr>
<tr>
<td rowspan="8" style="text-align: center;"><strong>User Memory</strong></td>
<td rowspan="8" style="text-align: center;">User Memory</td>
<td style="text-align: center;">Memory Framework</td>
<td style="text-align: center;">Memory Framework</td>
<td>Unified, structured, private, extensible, user-controllable AI memory management framework, connecting all cabin user memory data, support cloud + local, long-term + short-term operation and storage, support user modification and deletion, support more application and AI subsequent expansion</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Memory Information</td>
<td style="text-align: center;">User Basic Information</td>
<td>Memory of user's personal basic information, including but not limited to:<br />
① Name, age, gender, occupation, hobbies, marriage and children status, etc.<br />
② Family members and relationships, pet info, other contact relationships, etc.<br />
③ Home and company addresses, etc.</td>
</tr>
<tr>
<td style="text-align: center;">User Scene Information</td>
<td>Differentiated memory for multiple users' multiple types of high-frequency scenarios, including but not limited to:<br />
① Voice &amp; manual initiated map search and navigation, including regular POI, food, parking, charging stations, gas stations, attractions and other POI types, and preferred location selections<br />
② Voice &amp; manual initiated media search and playback, including media type, requested songs, artists, song style tags<br />
③ Voice &amp; manual vehicle body component settings, including AC, seats, windows, sunroof, sun shade, lights, driving mode, fragrance, etc.<br />
④ Voice &amp; manual system settings, including system volume, sound effect mode, etc.<br />
⑤ Support forming corresponding POI memory in memory info, such as "grandma's house" "Mike's home" "the Chinese restaurant from last week" "kid's swimming school", support user voice or manual navigation to corresponding memory locations</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Memory Learning Method</td>
<td style="text-align: center;">Explicit Command</td>
<td>User actively requests to memorize relevant info, e.g., "remember I'm an AI product manager" "remember my cat's name is Milk Tea" "remember my navigation location choice this time"</td>
</tr>
<tr>
<td style="text-align: center;">Implicit Learning</td>
<td>Trigger implicit learning memory when user performs specific operations, inputs specific info, or has consecutive similar operations, including but not limited to:<br />
① When input reveals user basic info like occupation, age, hobbies, AI proactively extracts memory<br />
② When user performs consecutive identical operations, like searching certain addresses, playing certain artists, adjusting body temperature or driving scenarios in specific situations<br />
③ When multi-turn dialogue or multi-step operations have repeated identical operations, like navigation search list selections<br />
④ When a memory forms, need to dynamically add or update original memory (if any)</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">Memory Trigger Method</td>
<td style="text-align: center;">Passive Memory Trigger</td>
<td>Support passive trigger of user memory, including but not limited to:<br />
① Navigate to the coffee shop I went to last week / Navigate to grandma's house<br />
② Recommend preferred food, music, attractions, etc.</td>
</tr>
<tr>
<td style="text-align: center;">Active Memory Trigger</td>
<td>Support active trigger of user memory, including but not limited to:<br />
① When user falls asleep, automatically adjust corresponding position's fan speed, temperature, seat mode, in-car volume, etc. to user's preferred state</td>
</tr>
<tr>
<td style="text-align: center;">Smart Memory Completion</td>
<td>Support intelligent completion of user memory in specific cases, including but not limited to:<br />
① User inputs "navigate to Westfield London", combined with user's past habits, destination auto-completes to "White City Car Park";<br />
② User inputs "find a nearby Chinese restaurant", combined with user memory and preference tags, prioritize showing Chinese cuisine brands user likes or has been to<br />
③ User inputs "play some music", automatically play the playlist user didn't finish last time</td>
</tr>
<tr>
<td rowspan="4" style="text-align: center;"><strong>Music Agent</strong></td>
<td style="text-align: center;">Fuzzy Search</td>
<td style="text-align: center;">Fuzzy Search</td>
<td style="text-align: center;">Fuzzy Search</td>
<td>Support user fuzzy command search for music resources, including fuzzy lyrics, internet memes, artist nicknames, song origins, etc.</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Personalized Recommendation</td>
<td style="text-align: center;">Behavior Recommendation</td>
<td style="text-align: center;">Behavior Recommendation</td>
<td>Combined with user's historical Q&amp;A content and playback behavior (like saved playlists, looped content types, etc.), when user asks for recommendations, personalize music resource recommendations</td>
</tr>
<tr>
<td style="text-align: center;">Scene Recommendation</td>
<td style="text-align: center;">Scene Recommendation</td>
<td>Based on passenger type and age group, driving scenario, etc., proactively recommend music resources. E.g., when child passenger detected and destination is zoo, proactively recommend animal-related children's educational content.</td>
</tr>
<tr>
<td style="text-align: center;">Encyclopedia Query</td>
<td style="text-align: center;">Instant Q&amp;A</td>
<td style="text-align: center;">Instant Q&amp;A</td>
<td>Support voice search for entertainment-related encyclopedia, AI gives summary response and provides resource info mentioned in response for device-side resource matching, support user direct playback.</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;"><strong>Video Agent</strong></td>
<td style="text-align: center;">Fuzzy Search</td>
<td style="text-align: center;">Fuzzy Search</td>
<td style="text-align: center;">Fuzzy Search</td>
<td>Support user fuzzy command search for video resources, including fuzzy plot descriptions, directors, actors, etc.</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Personalized Recommendation</td>
<td style="text-align: center;">Behavior Recommendation</td>
<td style="text-align: center;">Behavior Recommendation</td>
<td>Combined with user's historical Q&amp;A content and playback behavior (like saved shows, watch history, etc.), when user asks for recommendations, personalize video resource recommendations</td>
</tr>
<tr>
<td style="text-align: center;">Scene Recommendation</td>
<td style="text-align: center;">Scene Recommendation</td>
<td>Based on passenger type and age group, driving scenario, etc., proactively recommend video resources. E.g., when child passenger detected and destination is zoo, proactively recommend animal-related children's educational videos.</td>
</tr>
<tr>
<td rowspan="20" style="text-align: center;"><strong>Travel Agent</strong></td>
<td rowspan="3" style="text-align: center;">Smart Itinerary Planning</td>
<td rowspan="3" style="text-align: center;">Smart Itinerary Planning</td>
<td rowspan="3" style="text-align: center;">Smart Itinerary Planning</td>
<td>When user has clear city and clear need for travel planning or tourism guide info, can give detailed travel plan based on user needs, display itinerary planning info<br />
Including but not limited to specified itinerary time, specific conditions/groups, specified itinerary location (need to support provinces, cities or popular routes like Northwest Loop, West Sichuan Loop, etc.), specified travel time, etc.<br />
Need to support manual/voice modification, editing of itinerary<br />
Need to support itinerary sharing<br />
E.g., plan a National Day travel itinerary</td>
</tr>
<tr>
<td>Route planning/adjustment under multi-intent:<br />
1. E.g., "navigate to Arc de Triomphe, avoid highway/avoid small roads"<br />
2. E.g., "navigate to Big Ben, avoid Blackwall Tunnel"</td>
</tr>
<tr>
<td>Destination selection under multi-intent: Chinese restaurant closest to three locations</td>
</tr>
<tr>
<td rowspan="12" style="text-align: center;">Recommendation Function</td>
<td rowspan="5" style="text-align: center;">POI Recommendation</td>
<td style="text-align: center;">Transportation Category</td>
<td>Need to support following transportation POI search recommendations (complex condition search): gas stations/charging stations/charging piles, service areas, etc., and need to distinguish from navigation intent.<br />
E.g.: search for service areas with toilets, recommend charging stations that don't have queues and are cheap, help me navigate to service area with available charging piles along the way, can the service area ahead charge</td>
</tr>
<tr>
<td style="text-align: center;">Accommodation Category</td>
<td>Need to support following accommodation POI search recommendations (complex condition search): hotels, camping sites, etc., and need to distinguish from navigation intent.<br />
E.g.: recommend some internet-famous check-in hotels</td>
</tr>
<tr>
<td style="text-align: center;">Leisure &amp; Entertainment Category</td>
<td>Need to support following leisure &amp; entertainment POI search recommendations (complex condition search): attractions/parks, malls/shopping centers, cinemas, KTV/bars/hot springs/SPA, etc., and need to distinguish from navigation intent.<br />
E.g.: recommend a bar suitable for gathering to watch sports</td>
</tr>
<tr>
<td style="text-align: center;">Vehicle Service Category</td>
<td>Need to support following vehicle service POI search recommendations (complex condition search): 4S shops, car wash shops, auto beauty shops, etc., and need to distinguish from navigation intent.<br />
E.g.: I want to change car wrap, find a shop that does good wraps, find a quick car wash shop near York Way</td>
</tr>
<tr>
<td style="text-align: center;">Public Service Category</td>
<td>Need to support following public service POI search recommendations (complex condition search): hospitals, clinics, public toilets, etc., and need to distinguish from navigation intent.<br />
E.g.: are there any cheap express delivery points for large packages</td>
</tr>
<tr>
<td rowspan="5" style="text-align: center;">POI Information Q&amp;A</td>
<td style="text-align: center;">Transportation Category</td>
<td>Parking lot: parking info, pricing standards, suitable car types, space count, real-time available spaces, queue info<br />
Service area: service facilities<br />
Charging station: service facilities, brand, price, available chargers, queue info<br />
Gas station: service facilities, brand, fuel grades, queue info</td>
</tr>
<tr>
<td style="text-align: center;">Accommodation Category</td>
<td>Phone, business hours, business status, reviews, ratings, price, check-in/out time, facilities &amp; services</td>
</tr>
<tr>
<td style="text-align: center;">Leisure &amp; Entertainment Category</td>
<td>Phone, business hours, business status, opening hours, reviews, ratings, price, feature tags, visit duration, ticket info</td>
</tr>
<tr>
<td style="text-align: center;">Vehicle Service Category</td>
<td>Phone, business hours, business status, reviews, ratings, price, services provided</td>
</tr>
<tr>
<td style="text-align: center;">Public Service Category</td>
<td>Phone, business hours, business status, reviews, ratings, price, services provided</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Fuzzy Address Search</td>
<td style="text-align: center;">Fuzzy Feature &amp; Alias Search</td>
<td>① Break through traditional exact name search, support destination input based on visual features, local nicknames or fuzzy memory (e.g.: "go to that tall iron tower" or "the area with lots of graffiti ahead"). Agent can precisely extract semantic features, directly map to specific POI coordinates and initiate navigation<br />
② Support multiple destinations in one sentence, support modifying individual destinations</td>
</tr>
<tr>
<td style="text-align: center;">Interactive Destination Disambiguation</td>
<td>When fuzzy description matches multiple locations, break through traditional rigid list broadcast. Agent extracts location differentiating features, initiates natural language clarification (e.g.: "Do you mean the one by the river, or the one with outdoor terrace?"), guides user to efficiently lock destination in conversation</td>
</tr>
<tr>
<td style="text-align: center;">Navigation Service</td>
<td style="text-align: center;">Navigation Service</td>
<td style="text-align: center;">Navigation Service</td>
<td>Search results can be bookmarked, start navigation, add waypoints and other navigation operations</td>
</tr>
<tr>
<td style="text-align: center;">Result Display</td>
<td style="text-align: center;">Result Display</td>
<td style="text-align: center;">Result Display</td>
<td>Display with mini-map POI pin markers, map pin display<br />
Display different sources based on intent classification<br />
① Itinerary planning or travel guide type:<br />
Source results display with mini-map POI pins, map pins show POI name and related notes for this POI; support click to view Xiaohongshu note details<br />
② Leisure &amp; entertainment type (attractions/parks, malls/shopping centers, cinemas, KTV/bars/hot springs/SPA, script murder, etc.) POI info query<br />
Source results list display with mini-map POI pins, source results support view details<br />
③ Others<br />
Results list with mini-map POI pins</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">Context Interaction</td>
<td rowspan="3" style="text-align: center;">Context Interaction</td>
<td rowspan="3" style="text-align: center;">Context Interaction</td>
<td>Follow-up questions on recommended content</td>
</tr>
<tr>
<td>Query details of one item in result list</td>
</tr>
<tr>
<td>Secondary arrangement, modification of short-trip itinerary planning</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;"><strong>News Agent</strong></td>
<td rowspan="2" style="text-align: center;">News Content Push</td>
<td style="text-align: center;">Daily News Summary</td>
<td style="text-align: center;">Personalized Daily Digest Push</td>
<td>Support proactively pushing daily AI summary news to user on first entry to vehicle that day, combined with user's historical behavior, preference tags, etc., and support pushing when user actively asks for daily (or specific day) news summary on non-first entries</td>
</tr>
<tr>
<td style="text-align: center;">News Tracking Push</td>
<td style="text-align: center;">News Tracking Push</td>
<td>Support user tracking followed news progress, tracking news listened to in past 3 days, proactively push summary updates when followed news has progress, and support user voice query of historical news progress.</td>
</tr>
<tr>
<td rowspan="9" style="text-align: center;"><strong>Podcast Agent</strong></td>
<td rowspan="7" style="text-align: center;">AI Podcast Generation</td>
<td rowspan="3" style="text-align: center;">Podcast Content Input</td>
<td style="text-align: center;">Third-party Source Acquisition</td>
<td>Support using top podcast sources</td>
</tr>
<tr>
<td style="text-align: center;">User Info Input (Mobile)</td>
<td>URL, text files, audio/video and other user input interconnected with vehicle</td>
</tr>
<tr>
<td style="text-align: center;">Content Topic Selection</td>
<td>Preset content topics, combined multi-perspective topics, user input topics</td>
</tr>
<tr>
<td rowspan="4" style="text-align: center;">Podcast Description Output</td>
<td style="text-align: center;">Expression Mode Selection</td>
<td>Stand-up, two-person interview, multi-person debate, custom and other mode selection</td>
</tr>
<tr>
<td style="text-align: center;">Expression Style Selection</td>
<td>News commentary, leisure entertainment and other style selection</td>
</tr>
<tr>
<td style="text-align: center;">Podcast Duration Selection</td>
<td>Support auto-adapting suitable duration podcast content generation combined with content</td>
</tr>
<tr>
<td style="text-align: center;">Podcast Language Selection</td>
<td>Support different language switching</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">AI Podcast Playback</td>
<td rowspan="2" style="text-align: center;">AI Podcast On-demand</td>
<td rowspan="2" style="text-align: center;">Source Podcast On-demand</td>
<td>Podcast playback control, source on-demand and voice semantic commands</td>
</tr>
<tr>
<td>1. Semantic commands, e.g., "open", "close", "pause", "play", "bookmark";<br />
2. Interrupt anytime: during broadcast, user can ask questions about specific host, and receive response;<br />
3. Breakpoint resume: e.g., "continue explaining yesterday's real estate podcast"<br />
4. From user request to AI podcast starting main content, user has no noticeable waiting perception;</td>
</tr>
<tr>
<td rowspan="4" style="text-align: center;"><strong>Parking Agent</strong></td>
<td rowspan="3" style="text-align: center;">Smart Parking Recommendation</td>
<td style="text-align: center;">Parking Search</td>
<td style="text-align: center;">Personalized Search</td>
<td>AI assistant combines parking sources or parking guide platforms for full-network search, combines parking guide info, whether parking spots have charging piles, car battery status, etc., provides cost-effective, high-availability parking solutions to user, converted to POI<br />
① Parking lot search: support user complex condition search: parking lot type, price, opening hours, charging pile availability, accessibility facilities, etc., e.g., find a parking lot with many spots nearby, find a cheap outdoor parking lot (price + type), help me find parking lot with charging piles and car wash (facilities + services), etc.<br />
② Spot finding: special needs search, e.g., find a spot close to elevator in MixC parking lot, find a spot with no cars on both sides, find a wider spot that's easy to park, etc.<br />
③ In trip planning, plan parking solution in advance and prompt user to avoid on-the-spot decisions</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Parking Recommendation</td>
<td style="text-align: center;">Scene Recommendation</td>
<td>① When battery is low, parking lot search prioritizes recommending parking lots with charging piles<br />
② Special time suggestions: at night or bad weather, prioritize recommending indoor or underground parking lots<br />
③ When navigating to unfamiliar destination, distinguish whether user is temporary parking or long-term parking (predict or ask), fine-tune POI based on selection</td>
</tr>
<tr>
<td style="text-align: center;">Frequent Parking Memory and Recommendation</td>
<td>① Record user's frequent parking lots, like home, office, can trigger quick parking service when entering area<br />
② Remember user selection preferences, like always prioritizing cheap parking lots or prioritizing charging pile parking lots, etc.</td>
</tr>
<tr>
<td style="text-align: center;">Context Interaction</td>
<td style="text-align: center;">Context Interaction</td>
<td style="text-align: center;">Context Interaction</td>
<td>Follow-up questions on recommended content, e.g., too expensive, any closer ones, etc.</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;"><strong>Food Agent</strong></td>
<td rowspan="2" style="text-align: center;">Food Agent</td>
<td rowspan="2" style="text-align: center;">Food Query</td>
<td style="text-align: center;">Info Query</td>
<td>Precisely identify user's food needs (like cuisine type, taste, budget, number of diners, suitable groups, environment, service, queue status, etc.), query food info, restaurant info, and support multi-condition combined query</td>
</tr>
<tr>
<td style="text-align: center;">Food Recommendation</td>
<td>Combined with current time, weather, dining scenario, special periods, location, dietary preferences, physical condition and other scenario factors, provide more precise recommendations, e.g., what to eat since recent health check showed high blood lipids, want unconventional Valentine's Day dinner, what to eat to reduce dampness during recent humid weather</td>
</tr>
<tr>
<td style="text-align: center;">Context Interaction</td>
<td style="text-align: center;">Context Interaction</td>
<td style="text-align: center;">Context Interaction</td>
<td>Support multi-turn interaction, follow-up questions on restaurant info like what's the specialty of the first restaurant, business hours, environment, service, etc.; multi-turn correction when not satisfied with recommendation results, e.g., can't eat spicy recently, stomach isn't well don't want these</td>
</tr>
<tr>
<td rowspan="8" style="text-align: center;"><strong>In-Car<br />
Productivity</strong></td>
<td rowspan="3" style="text-align: center;">Email</td>
<td style="text-align: center;">Read Email</td>
<td style="text-align: center;"> </td>
<td>Summary and Read unread emails, e.g., help to summary my unread emails</td>
</tr>
<tr>
<td style="text-align: center;">Draft Email</td>
<td style="text-align: center;"> </td>
<td>Draft new emails and email responses, e.g., help to draft a response to the first email</td>
</tr>
<tr>
<td style="text-align: center;">Send Email</td>
<td style="text-align: center;"> </td>
<td>Send new emails / repond to emails, e.g., send a new email to John</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">Calendar</td>
<td style="text-align: center;">Read Calendar</td>
<td style="text-align: center;"> </td>
<td>Summary and read calendar information, e.g., tell me what are the events in my calendar for next Monday</td>
</tr>
<tr>
<td style="text-align: center;">Create Calendar Event</td>
<td style="text-align: center;"> </td>
<td>Create new event based on user's input, e.g., create a reminder for me to go to 4S store next Friday</td>
</tr>
<tr>
<td style="text-align: center;">Update Calendar Event</td>
<td style="text-align: center;"> </td>
<td>Update existing Calendar Event</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Meetings</td>
<td style="text-align: center;">Meeting Preparation</td>
<td style="text-align: center;"> </td>
<td>Help the user to proactively prepare next meeting, e.g., when users gets in the car, proactively tell the user that next meeting is in 2 hours, who are the stakeholders, what information need to be prepared, etc.</td>
</tr>
<tr>
<td style="text-align: center;">Navagation Integration</td>
<td style="text-align: center;"> </td>
<td>If it is a physical meeting, proactively start the navigation for the meeting</td>
</tr>
<tr>
<td rowspan="15" style="text-align: center;"><strong>Other</strong></td>
<td rowspan="9" style="text-align: center;">First-Run Onboarding Flow — In-Vehicle AI Assistant</td>
<td style="text-align: center;">Hi, I’m your in-car AI assistant—what would you like me to call you?</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">Should I keep things short and direct, or more conversational?</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">When there’s a vehicle warning like low fuel or tire pressure, should I speak it aloud, show it on the screen, or only speak urgent alerts?</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">If a warning is still active, should I mention it once, repeat it every few minutes, or only repeat it if it gets worse?</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">Safety-critical alerts like collision warnings and brake faults will always be spoken aloud regardless of your settings—got it?</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">Are there any allergies or medical conditions I should be aware of?</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">Where do you start and end your day, such as your home and work locations?</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">How often should I proactively make suggestions—often, sometimes, or only when you ask?</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">Got it, I’ll remember details from our chats to be more helpful, and you can ask me to forget anything or review your settings anytime.</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">Multi-User Memory and Context Design</td>
<td style="text-align: center;"><strong>Passenger and Rear-Seat Passenger Context Separation<br />
</strong>1. Passenger requests (e.g., media or climate control) must only affect their own seat zone—front passenger controls passenger display/climate, and rear passengers control only their Rear Seat Entertainment (RSE) screens and rear climate settings.<br />
2. All interactions, memory, media, and UI state must be strictly isolated per seat or device using identifiers like seat position, mic ID, or user profile, unless explicitly shared</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;"><strong>Interior Camera Detection for Children in Rear Seats<br />
</strong>1. When children are detected in the rear seats, the assistant should adapt behavior with child-safety prompts and continuous alerts if a child is left in the vehicle after shutdown, including checks on cabin temperature, windows, and weather conditions.<br />
2. The system should prioritize child-friendly media and recommendations such as cartoons and educational content and allow the driver to manage Rear Seat Entertainment (RSE) on behalf of children.</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">Proactive Behaviors (run silently in the background)</td>
<td style="text-align: center;"><strong>Not overwhelming the driver with audio signals<br />
</strong>1. Limit voice alerts to avoid distraction and drowsiness.<br />
2. Most warnings appear on UI, with voice only after every 4th warning.</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;"><strong>End-of-trip summary<br />
</strong>1. Optional summary shown when parked based on user preference.<br />
2. Includes drive stats, reminders, and vehicle status.<br />
3. Purpose is to close the trip and suggest quick actions.</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;"><strong>Vehicle health monitoring<br />
</strong>1. Tracks service, tire pressure, battery, and maintenance trends.<br />
2. Examples: service reminders, tire leak alerts, battery warnings.<br />
3. Can book service or place orders via connected agents when needed.<br />
4. Triggering Alert text messages to the user phone.</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
<tr>
<td style="text-align: center;">SLM use cases</td>
<td style="text-align: center;">Can Edge SLM Handle the multi intent queries ?<br />
<br />
1. Can you check if it's going to rain tonight? If not, find a restaurant with a good rating downtown and send a meeting invite with that location information.<br />
2. While the user is driving, they say something like "Hey, take this picture and send it as an email to one of my contacts" (using the edge VLM).</td>
<td style="text-align: center;"> </td>
<td></td>
</tr>
</tbody>
</table>

## \<Bosch\>-specific documentation

*If there are Customer-specific documents that need to be included with the SOW, make a list with purpose and cadence for delivery of these documents.*

# Appendix

## Definitions and acronyms

The following table lists terms, initialisms, and acronyms used in this document.

<table>
<caption><p>Table 13: Table of abbreviations</p></caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 74%" />
</colgroup>
<thead>
<tr>
<th>Term / acronym</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Backlog</td>
<td>The set of epics, features, and user stories that are prioritized and assigned to resources during sprints to direct the effort of the feature teams to work toward the &lt;Bosch&gt; objectives and desired business value.</td>
</tr>
<tr>
<td>BWBM</td>
<td><p>Black and white box monitoring.</p>
<ul>
<li><p>Blackbox monitoring: testing externally visible behavior as a user would see it.</p></li>
<li><p>Whitebox monitoring: monitoring based on metrics exposed by the internals of the system, including logs, interfaces (like the Java virtual machine profiling interface), or an HTTP handler that emits internal statistics.</p></li>
</ul></td>
</tr>
<tr>
<td>DOD</td>
<td>Definition of Done</td>
</tr>
<tr>
<td>DOR</td>
<td>Definition of Ready</td>
</tr>
<tr>
<td>Informal knowledge transfer</td>
<td>The exchange of information between &lt;MSFT&gt; staff and &lt;Bosch&gt; staff as they work together on the project.</td>
</tr>
<tr>
<td>IP</td>
<td>Intellectual Property</td>
</tr>
<tr>
<td>KPI</td>
<td>Key performance indicator</td>
</tr>
<tr>
<td>OKRs</td>
<td>Objectives and key results. A set of measurable goals and metrics used to track progress toward reaching valued business objectives.</td>
</tr>
<tr>
<td>ORC</td>
<td>Operational readiness criteria. Criteria used in the review where customers have a base set of monitors, logs, runbooks, UAT, security, and scans needed to place a service into use (“production readiness review”). Services deemed business-critical also include availability and reliability measurements (availability and serviceability, at a higher level).</td>
</tr>
<tr>
<td>PBI</td>
<td>Product backlog item. An item tracked in DevOps. Also known as a “work item.” Typically, these items can be individual tasks, stories, epics, features, or other custom items as defined for a particular project.</td>
</tr>
<tr>
<td>Product increment</td>
<td>Depending on the type of project, a “product increment” can be any combination of the following (but not limited to): documentation of standards, policies, and procedures; landing zones; security templates; operational playbooks; or user stories completed within a sprint.</td>
</tr>
<tr>
<td>QA</td>
<td>Quality assurance</td>
</tr>
<tr>
<td>SLI</td>
<td>Service-level indicator</td>
</tr>
<tr>
<td>SLO</td>
<td>Service-level objective</td>
</tr>
<tr>
<td>SME</td>
<td>Subject matter expert. A person with specific knowledge or expertise in a particular area. For example, a security SME, or database SME.</td>
</tr>
<tr>
<td>SOW</td>
<td>Statement of work</td>
</tr>
<tr>
<td>Sprint planning</td>
<td>A single meeting held at the start of each sprint to review and assign PBIs that meet DOR and will be delivered during the sprint. In some exceptional cases, planning may extend past the first day. The CPdM and feature team will attend, along with key stakeholders.</td>
</tr>
<tr>
<td>Sprint retrospective</td>
<td>A single meeting held at the end of each sprint to give the feature team an opportunity to review its performance and implement improvements for subsequent sprints. Identified improvements can be enacted during subsequent sprints. The feature team will attend with key stakeholders, if desired.</td>
</tr>
<tr>
<td>Sprint review</td>
<td>A single meeting held at the end of each sprint to evaluate the progress and update the product backlog, if needed. The CPdM and feature team will attend along with key stakeholders.</td>
</tr>
<tr>
<td>Work product</td>
<td>Work products are tangible outcomes or artifacts produced during delivery. They may not always be fully completed scope items, but rather evolving representations of the intended scope, serving as evidence of progress without needing formal &lt;Bosch&gt; review or approval.</td>
</tr>
<tr>
<td>UAT</td>
<td>User acceptance testing</td>
</tr>
<tr>
<td>ESWO</td>
<td>Enterprise Service Work Order</td>
</tr>
</tbody>
</table>

## Technology requirements

The products and technology listed in the following table are required for the project. \<Bosch\> is responsible for obtaining all licenses, products, or subscriptions. This list is subject to change based on adjustments made to desired objectives or direction of the project.

| Product and technology item  | Version        | Ready by         |
|------------------------------|----------------|------------------|
| Microsoft Azure subscription | Not applicable | Start of project |

Table 14: Technology requirements

The following are assumptions related to the products listed above.

- Customer will ensure availability of licenses and provide access for the usage of GitHub Co-pilot by the project team for the full duration of this engagement

- Microsoft will utilize GitHub Copilot to enhance the delivery of service under this statement of work

- Customer consents to the use of GitHub Copilot for delivery services outlined in this statement of work.

## Environment requirements

\<Bosch\> will supply and maintain all environments used for the development and delivery lifecycle during this project. \<Bosch\> will obtain the required Azure subscriptions and provide \<MSFT\> with administrative control to build the development and test environments, as needed.

| Environment | Location | Responsible for configuration and maintenance | Subscription ownership | Ready by |
|----|----|----|----|----|
| Development | Microsoft Azure | \<MSFT\> or \<Bosch\> | \<MSFT\> or \<Bosch\> | Start of project |
| Test | Microsoft Azure | \<MSFT\> or \<Bosch\> | \<MSFT\> or \<Bosch\> | \[Event + X\] |
| Production | Microsoft Azure | \<MSFT\> or \<Bosch\> | \<MSFT\> or \<Bosch\> | \[Event + X\] |

Table 15: Environment requirements

## **\<Bosch\>** responsibilities

In addition to \<Bosch\> activities defined in the <span class="mark"></span>[*Customer desired business*](#customer-desired-business-objectives) *objectives* and <span class="mark"></span>[*Delivery approach, completion and timeline*](#delivery-approach-completion-and-timeline) sections, \<Bosch\> is also required to:

- Provide information:

- This includes accurate, timely (within three business days or as mutually agreed upon), and complete information. Preparing documentation about processes, standards, policies, and existing guidelines.

- Provide access to people and resources.

- This includes access to knowledgeable \<Bosch\> personnel, including business user representatives, and access to funding if additional budget is needed for more capacity.

- Acquire and install the cloud capacity that is needed to support the environments as defined in this SOW. 

- Manage non-\<MSFT\> resources.

- \<Bosch\> will assume responsibility for the management of all \<Bosch\> personnel and vendors who are not managed by \<MSFT\>.

- Manage external dependencies.

- \<Bosch\> will facilitate any interactions with related projects or programs in order to manage external dependencies. Implement modifications to third-party systems and external interfaces to support integration

- Manage organizational change:

- Redesign or re-engineer business processes.

- Design or redesign the functional organization.

- Plan or undertake user communications.

- Drive solution or product adoption.

## Project assumptions

The following are assumptions that apply to this project between \<Bosch\> and \<MSFT\>. During the project, the information and assumptions in this document will be validated, and if a material difference is present, this could result in Microsoft initiating a change request to cover additional work or extending the project duration.

- Workday:

- Local \<MSFT\> employees will follow the standard \<MSFT\> (or appropriate subsidiary) workday and work week based on where the Microsoft employee is located unless otherwise agreed to jointly between the Microsoft employee and \<Bosch\>. Exceptions will be coordinated by the Microsoft project manager.

- Offshore resources that are not part of the factory will be available between 7 AM and 10 PM India Standard Time over an eight-hour continuous window.

- Remote work:

- Based on the T&E budget in the associated WO, with mutual agreement, the Microsoft team may perform services at the \<Bosch\> location, otherwise all services will be performed remotely.  If the \<MSFT\> feature team is required to be present at the \<Bosch\> location every week, resources will typically be on site for three nights and four days, arriving on Monday and leaving on Thursday.

- Language:

- All project communications and documentation will be in English*.* Local language support and translations is out of scope for Microsoft and will be provided by \<Bosch\>.

- Staffing:

- If necessary, \<MSFT\> will make staffing changes. These may include, but are not limited to, resources and project roles.

- Microsoft reserves the right to utilize whichever labor categories, which could include certain vetted and approved subcontractors, in whatever quantities, in our sole discretion, are appropriate to perform the professional services outlined in this SOW. 

- Microsoft employees may be based globally unless \<Bosch\> has specific requirements for where the engagement team members need to be based.  If \<Bosch\> has requirements on where Microsoft resources can be located, those need to be identified by \<Bosch\> before contract signature and outlined in the Statement of Work.

- Project start and/or full Resource mobilization depends upon resource availability, \<Customer Name\> onboarding process, and skills required.

- No required \<Bosch\> onboarding training for Microsoft resources is included in the estimates. If any such training is required, Microsoft will initiate the change request process.

- Security

- If any Security clearances, network access, physical access, or other customer requirements are need, those shall be identified by \<Bosch\> before contract signature and outlined in the Statement of Work. If Security clearance, network access, physical access, or other requirements are required after contract signature, it may cause engagement delays or delays in staffing and engagement start.**   **

- Informal knowledge transfer:

- No formal training materials will be developed or delivered as part of this project. All information transfer will be through informal knowledge transfer.

- Known standards:

- \<MSFT\> expects to use Azure DevOps, Azure Pipelines, and may use GitHub for standard delivery.

- If, Time will be required to learn the \<Bosch\> tooling if there are deviations from \<MSFT\> standards. This time has not been included in project estimates.

- \<MSFT\> will use standard Azure DevOps process templates, as well as other IP designed to speed up delivery, including, but not limited to, standard work items, pipelines, and document templates.

- Other assumptions:

- All work is to be delivered without breaks in the schedule. Any breaks in the project calendar must be scheduled four weeks in advance or will be billed without interruption.

- In addition to project team members, \<Bosch\> shall allow \<MSFT\> internal systems to access the mutually accessible delivery platforms and tools used for this project.

- \<MSFT\> will read, store, and share necessary delivery insights on the work artifacts and products generated as part of this project (for example, test cases, code base, and pipelines) that are hosted on mutually accessible delivery platforms, like Azure DevOps, Jira, and GitHub.

- \<MSFT\> will make available to \<Bosch\> all data and insights gathered during the project. Microsoft will purge said data and insights upon explicit \<Bosch\> request or at the end of the project.

- \<Bosch\> required compliance training will reduce capacity available for execution. This includes:

- Security training

- Internal orientation

- Industry-specific and regulatory compliance training

- Procedures outside of \<MSFT\> standard compliance

- Background checks, fingerprinting, badging, and authentication

- AI Usage:

- Microsoft may use Microsoft-developed or Microsoft-licensed artificial intelligence-assisted materials, including agentic systems, (collectively, “AI Tools”) to perform the Services. Microsoft’s use of AI Tools, whether inside or outside \<Bosch\>’s tenant, will not alter ownership, licensing, or confidential treatment of any Pre-Existing Work, Data, Confidential Information, or Service Deliverables. If Microsoft uses AI Tools to perform the Services, Microsoft will comply with Microsoft’s internal standards, privacy and security requirements, and Responsible AI principles as defined in this Agreement. \<Bosch\> acknowledges and agrees that Microsoft’s use of AI Tools may evolve during the engagement, including through updates, improvements, or the substitution of underlying models, techniques, materials, or system architectures.

- When Microsoft uses AI Tools to perform the Services, Microsoft systems may generate telemetry data related to the AI Tool execution, including system usage metrics. This telemetry data is collected only during Microsoft’s performance of the Services and collection ceases when the engagement concludes. Microsoft will process this telemetry data in accordance with the Microsoft Products and Services Data Protection Addendum. This notice is provided for informational purposes only and does not modify Microsoft’s data handling practices or create additional contractual obligations.

- Any AI Tools installed or deployed in \<Customer Name\> environment as part of this engagement will be removed by Microsoft upon conclusion of the engagement, unless otherwise agreed in writing by the parties.

- AI Usage - Responsible AI:

- \<Bosch\> acknowledges that this engagement includes the development or deployment of an AI system that: (1) is powered by AI and \<Bosch\> is being exposed to and interacting with an AI system, (2) the AI system output may contain sensitive content and/or factual inaccuracies, (3) \<Bosch\> is responsible for determining the accuracy of any content generated by this AI system in relation to \<Bosch\>’s intended use as the user of this AI system, and (4) this AI system does not provide opinions or advice. It is not designed to replace the role of qualified auditors or human reviewers. \<Bosch\> is solely responsible for displaying and/or obtaining appropriate consents, warnings, disclaimers, and acknowledgements to end users of \<Bosch\>’s implementation of the AI system.

- During the course of the engagement under this SOW, if the requested business objective includes Microsoft developing or deploying an AI System for or with \<Bosch\> which may be considered a sensitive use, Microsoft will conduct an internal responsible AI review, to include assessment of and requirements for the potential sensitive use.

- The outcome of Microsoft’s review will be comprehensively discussed with \<Bosch\>, ensuring a transparent understanding of the findings. Microsoft is dedicated to adhering to its RAI principles, and as such, will identify and implement any necessary changes. For more detailed information about Microsoft’s commitment to responsible AI, please refer to [https://aka.ms/RAI](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2FRAI&data=05%7C02%7Cdavidcra%40microsoft.com%7Cd9430fa82c7e4b341bb908dd19f3d3e0%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638695257225235898%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=cLVl5entLjr%2FcCwoUWyNNChh1hLN6bAxQFc2gnkSyIk%3D&reserved=0).

- Should the review uncover any discrepancies between the use-case and the RAI guidelines, Microsoft will engage with \<Bosch\> to co-develop a robust mitigation plan in addressing and resolving potential risks, ensuring that the project is brought into alignment with the RAI standards. The process may lead to modifications of the current project or proposal of an alternative solution that complies with the RAI expectations."

- If \<Bosch\> approves a solution design that uses a product that is not generally available, \<Bosch\> acknowledges this, and accepts that it may affect the project cost and timeline.

- When \<Bosch\> determines that \<MSFT\> or its agents will have access to personal identifiable information, \<Bosch\> is obligated to inform \<MSFT\> within \[10\] days that further access to that information requires the use of equipment owned or supplied by \<Bosch\>.
