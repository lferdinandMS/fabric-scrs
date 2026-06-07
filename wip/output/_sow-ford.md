<img src="media/image1.jpg" style="width:8.5in;height:10.99931in" alt="A close-up of a logo AI-generated content may be incorrect." />

<img src="media/image20.png" style="width:1.50891in;height:0.67861in" />

# Contents

[Introduction [1](#introduction)](#introduction)

[1.1 Solution vision [2](#solution-vision)](#solution-vision)

[1.2 Project goals [2](#project-goals)](#project-goals)

[1.3 Project scope [3](#project-scope)](#project-scope)

[1.4 Technology requirements [7](#technology-requirements)](#technology-requirements)

[1.5 Environment requirements [9](#environment-requirements)](#environment-requirements)

[1.6 Exclusions [9](#exclusions)](#exclusions)

[2 Definitions and acronyms [12](#definitions-and-acronyms)](#definitions-and-acronyms)

[3 Delivery approach, completion, and timeline [14](#delivery-approach-completion-and-timeline)](#delivery-approach-completion-and-timeline)

[3.1 Overview [14](#overview)](#overview)

[3.2 Delivery approach [14](#delivery-approach)](#delivery-approach)

[3.2.1 Sprint process [14](#sprint-process)](#sprint-process)

[3.2.2 Project initiation [15](#project-initiation)](#project-initiation)

[3.2.3 Product baseline planning [17](#product-baseline-planning)](#product-baseline-planning)

[3.2.4 Testing and defect remediation [22](#testing-and-defect-remediation)](#testing-and-defect-remediation)

[3.2.5 Delivery compliance, privacy and security [24](#delivery-compliance-privacy-and-security)](#delivery-compliance-privacy-and-security)

[3.3 Outputs [25](#outputs)](#outputs)

[3.4 Completion and definition of done [26](#completion-and-definition-of-done)](#completion-and-definition-of-done)

[3.4.1 Sprint completion [26](#sprint-completion)](#sprint-completion)

[3.4.2 Backlog item completion [26](#backlog-item-completion)](#backlog-item-completion)

[3.5 Timeline [27](#timeline)](#timeline)

[4 Project organization [28](#project-organization)](#project-organization)

[4.1 Project staffing [28](#project-staffing)](#project-staffing)

[4.1.1 Customer roles [28](#customer-roles)](#customer-roles)

[4.1.2 Microsoft roles [31](#microsoft-roles)](#microsoft-roles)

[4.2 Executive steering committee [34](#executive-steering-committee)](#executive-steering-committee)

[4.3 Product council [35](#product-council)](#product-council)

[4.4 Feature team [36](#feature-team)](#feature-team)

[5 Project governance [37](#project-governance)](#project-governance)

[5.1 Project communication [37](#project-communication)](#project-communication)

[5.2 Risk and issue management [37](#risk-and-issue-management)](#risk-and-issue-management)

[5.3 Change management process [38](#change-management-process)](#change-management-process)

[5.4 Escalation path [38](#escalation-path)](#escalation-path)

[5.5 Project completion [39](#project-completion)](#project-completion)

[6 Customer responsibilities and project assumptions [39](#customer-responsibilities-and-project-assumptions)](#customer-responsibilities-and-project-assumptions)

[6.1 Customer responsibilities [39](#customer-responsibilities)](#customer-responsibilities)

[6.2 Project accountabilities [40](#project-accountabilities)](#project-accountabilities)

[6.3 Scope assumptions [42](#scope-assumptions)](#scope-assumptions)

[6.4 Project assumptions [43](#project-assumptions)](#project-assumptions)

[6.5 Responsible AI assumptions [46](#responsible-ai-assumptions)](#responsible-ai-assumptions)

[6.6 Prototype use case overview [47](#prototype-use-case-overview)](#prototype-use-case-overview)

[**Use Case 3: Vendor Quote & Contract Document Management Analysis** [47](#use-case-1-supplier-downtime-and-sla-credit-automation)](#use-case-1-supplier-downtime-and-sla-credit-automation)

[**Use Case 4: Supplier Downtime and SLA Credit Automation** [48](#use-case-1-supplier-downtime-and-sla-credit-automation)](#use-case-1-supplier-downtime-and-sla-credit-automation)

[6.7 Prototype prerequisites [49](#prototype-prerequisites)](#prototype-prerequisites)

[**Technical Scope** [52](#technical-scope)](#technical-scope)

[7 Exhibits [53](#exhibits)](#exhibits)

[7.1 Organizational readiness [53](#organizational-readiness)](#organizational-readiness)

[7.2 AI security foundation [54](#ai-security-extension)](#ai-security-extension)

[7.3 Agentic SOC [56](#agentic-soc)](#agentic-soc)

[7.4 Department Agents [57](#department-agents)](#department-agents)

[7.5 Solution Overview [57](#solution-overview)](#solution-overview)

[7.6 Agent capabilities [58](#agent-capabilities)](#agent-capabilities)

# Table of tables

[Table 1: Project goals [2](#_Toc231555271)](#_Toc231555271)

[Table 2: Project scope areas [4](#_Toc231555272)](#_Toc231555272)

[Table 3: Project scope [5](#_Toc231555273)](#_Toc231555273)

[Table 4: Technology requirements [7](#_Toc231555274)](#_Toc231555274)

[Table 5: Environment requirements [9](#_Toc231555275)](#_Toc231555275)

[Table 6: Exclusions [9](#_Toc213430935)](#_Toc213430935)

[Table 7: Table of abbreviations [12](#_Toc213430936)](#_Toc213430936)

[Table 8: Project initiation activities [15](#_Toc213430937)](#_Toc213430937)

[Table 9: Product baseline planning activities [17](#_Toc213430938)](#_Toc213430938)

[Table 10: Delivery sprints activities [20](#_Toc213430939)](#_Toc213430939)

[Table 11: Testing in scope [23](#_Toc213430940)](#_Toc213430940)

[Table 12: Defects priority definitions [24](#_Toc215587312)](#_Toc215587312)

[Table 13: Outputs [25](#_Toc213430941)](#_Toc213430941)

[Table 14: Customer roles [28](#_Toc231555284)](#_Toc231555284)

[Table 15: Microsoft roles [31](#_Toc231555285)](#_Toc231555285)

[Table 16: Executive steering committee roles and responsibilities [34](#_Toc213430942)](#_Toc213430942)

[Table 17: Product council roles [36](#_Toc231555287)](#_Toc231555287)

[Table 18: Feature team roles and responsibilities [36](#_Toc213430944)](#_Toc213430944)

[Table 19: Project accountabilities [40](#_Toc231555289)](#_Toc231555289)

[Table 20: Responsible AI assumptions [46](#_Toc231555290)](#_Toc231555290)

[Table 21: Organizational readiness outcomes [53](#_Toc231555291)](#_Toc231555291)

[Table 22: AI security foundation outcomes [54](#_Toc231555292)](#_Toc231555292)

# Table of figures

[Figure 1: Agentic AI solution vision [2](#_Toc231555293)](#_Toc231555293)

[Figure 2: Enterprise AI scope areas [3](#_Toc231555294)](#_Toc231555294)

[Figure 3: Iterative delivery approach - Scrum process [15](#_Toc222472757)](#_Toc222472757)

[Figure 4: High-level timeline [28](#_Toc222472758)](#_Toc222472758)

[Figure 5: Department or business domain agents [57](#_Toc231555297)](#_Toc231555297)

[Figure 6: Solution overview [58](#_Toc231555298)](#_Toc231555298)

[Figure 7: Agent capabilities [59](#_Toc231555299)](#_Toc231555299)

This document is strictly a non-binding draft, intended solely for preliminary review and discussion. It has not been finalized, approved, or accepted by Microsoft, and does not create, imply, or represent any commitment, obligation, or agreement of any kind. All content, terms, and details herein are subject to substantial revision, amendment, or complete removal during the formal approval process at Microsoft. No rights, obligations, or representations should be inferred from this version.

This Statement of Work (SOW) and any exhibits, appendices, schedules, and attachments to it are made pursuant to Work Order (WO) *\[insert WO number\]* and describes the work to be performed (“services”) by Microsoft (“us,” “we”) for **Ford Motor Company** (“**Ford**”, “Customer”, “you”, “your”) relating to **Ford - Agentic AI Transformation** (“Project”).

This SOW and the associated WO expire 30 days after their publication date (date Microsoft submits to the Customer) unless signed by both parties or formally extended in writing by Microsoft.

# Introduction

Ford Motor Company is on a business transformation journey to modernize operations, improve workforce productivity, and accelerate enterprise innovation through the adoption of Agentic AI and intelligent automation capabilities powered by Microsoft technologies. As organizations continue to face increasing operational complexity, disconnected systems, fragmented information, and rising demands for speed and agility, Ford recognizes the need to evolve toward a more connected and AI-enabled operating model that improves how work is performed across the enterprise.

Microsoft will partner with Ford to establish a secure, enterprise-grade Agentic AI platform using Microsoft Copilot Studio and Azure AI Foundry. This project focuses on four key areas: strengthening AI security and governance, building a reusable Agentic AI factory with intelligent agents, deploying a production-ready enterprise agent with Responsible AI controls and operational readiness, and driving adoption through structured change management and user enablement. By embedding AI-driven automation into key business operations, Ford will improve productivity, reduce manual effort, accelerate decision-making, and deliver more efficient, consistent, and scalable business outcomes.

The platform will focus on enabling high-priority business processes and operational workflows where AI-driven automation and intelligent orchestration can deliver the greatest business value. The platform will support **conversational**, **retrieval**, **task-oriented**, and **autonomous** AI agents that enhance productivity, automate repetitive activities, improve knowledge access, and optimize enterprise-wide workflow execution. The solution architecture will be modular, secure, and reusable by design, enabling future expansion across additional business domains, teams, and enterprise initiatives.

Microsoft and Ford will work collaboratively to align strategic business objectives, prioritize high-value use cases, establish governance and Responsible AI standards, and deploy scalable Agentic AI capabilities.

This pilot project will follow a phased, iterative approach designed to accelerate time-to-value while establishing a secure, scalable, and enterprise-ready AI foundation. The initial Pilot phase will focus on deploying a combination of production ready agents and prototype agents, validating measurable business value, and refining integration, security, and governance frameworks. This approach is intentionally structured to support seamless expansion into enterprise-wide adoption.

Ultimately, this initiative will establish a secure, scalable, and enterprise-ready Microsoft Agentic AI platform that enables Ford to deploy intelligent business capabilities at scale, accelerate innovation, improve operational efficiency, enhance decision-making, and deliver measurable business value.

## Solution vision

This diagram below presents a long-term vision for transforming business operations through Agentic AI, where humans and systems interact with AI agents that orchestrate end-to-end processes across business domains. This project focuses on building the foundation to enable Department Agents, and deliver a set of high-impact pilot use cases to demonstrate value, establish reusable capabilities, and integrate with key business applications that will pave the way for a future scaled enterprise expansion.

<img src="media/image5.png" style="width:6.5in;height:3.20139in" />

<span id="_Toc231555293" class="anchor"></span>Figure 1: Agentic AI solution vision

## Project goals

The potential goals related to this project are listed below. They are provided for context and are not statements of accountability or of Services to be performed by Microsoft. The project outcomes and Services to be performed are described within this section and within the remainder of this SOW.

| **Goal** | **Description** |
|----|----|
| **Establish a Secure, Scalable, and Reusable Agentic AI Platform** | Microsoft and Ford will establish a secure, governed, and Azure-native Agentic AI platform designed to support scalable and reusable AI capabilities across the enterprise. The platform will accelerate deployment of multi-agent workflows and reduce one-off solution development through standardized architecture and delivery patterns. |
| **Enhance Operational Efficiency Through Agentic AI** | Microsoft and Ford will establish a business-driven Agentic AI foundation that integrates intelligent automation and AI-powered workflows into high priority business processes. AI agents will securely retrieve information, support decision-making, automate tasks, and execute approved actions across enterprise systems to improve efficiency, reduce manual effort, enhance consistency, strengthen governance, and deliver measurable business value across productivity, quality, compliance, risk, and financial performance metrics. |
| **Facilitate Enterprise Adoption of Agentic AI** | Microsoft and Ford will develop and execute an Organizational readiness strategy to support the adoption of Agentic AI capabilities enabled by the platform. The initiative will focus on improving user readiness, driving behavioral change, and embedding AI-enabled ways of working into day-to-day business processes that will be candidates for AI enablement. |

<span id="_Toc231555271" class="anchor"></span>Table 1: Project goals

## Project scope

This project will focus on the **scope** described below, which will be **prioritized based on** **agreement between Microsoft and Ford**. During baseline planning and throughout the project, Microsoft and **Ford** will review the scope and work together to deliver **high priority** **outcomes** within the available capacity.

<img src="media/image7.png" style="width:6.5in;height:2.90833in" />

<span id="_Toc231555294" class="anchor"></span>Figure 2: Enterprise AI scope areas

<span id="_Toc231555272" class="anchor"></span>

<table>
<caption><p>Table 2: Project scope areas</p></caption>
<colgroup>
<col style="width: 3%" />
<col style="width: 31%" />
<col style="width: 65%" />
</colgroup>
<thead>
<tr>
<th style="text-align: right;">#</th>
<th>Area</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="3"><strong>Foundation &amp; Enablement</strong></td>
</tr>
<tr>
<td style="text-align: right;"><strong>1</strong></td>
<td><strong>Establish</strong> <strong>Platform</strong> <strong>Infrastructure (Foundation)</strong></td>
<td>Implement the foundational platform required to enable Microsoft Copilot Studio and Azure Foundry agentic AI solutions across the enterprise.</td>
</tr>
<tr>
<td style="text-align: right;"><strong>2</strong></td>
<td><strong>Design Solution, Data,</strong> <strong>&amp; Integration Architecture</strong></td>
<td>Define the solutions scope and architect end-to-end systems, data flows, and integration architecture to ensure interoperability across vendor applications and enterprise ecosystems.</td>
</tr>
<tr>
<td style="text-align: right;"><strong>3</strong></td>
<td><strong>Secure the Platform</strong></td>
<td>Implement Agent 365 to establish a secure and governed AI platform that embeds security, audit, compliance, privacy, and risk management controls, safeguarding enterprise data, ensuring regulatory compliance, and enabling trusted AI operations at scale.</td>
</tr>
<tr>
<td colspan="3"><strong>Build &amp; Deliver AI Solutions</strong></td>
</tr>
<tr>
<td style="text-align: right;"><strong>4</strong></td>
<td><strong>Create the AI Factory</strong></td>
<td>Establish standardized processes, tools, and reusable assets to industrialize AI development, enabling rapid design, testing, and scaling of models and intelligent solutions.</td>
</tr>
<tr>
<td style="text-align: right;"><strong>5</strong></td>
<td><strong>Define</strong> <strong>Business Value</strong> <strong>&amp;</strong> <strong>Optimize</strong> <strong>Processes</strong></td>
<td>Identify and prioritize high-value use cases, optimize business processes, and define AI agents to deliver measurable outcomes.</td>
</tr>
<tr>
<td style="text-align: right;"><strong>6</strong></td>
<td><strong>Build &amp; Deploy Agents</strong></td>
<td>Develop, test, and deploy business-aligned AI agents that automate workflows, augment decision-making, and drive measurable outcomes across functional domains.</td>
</tr>
<tr>
<td colspan="3"><strong>Operate &amp; Realize Value</strong></td>
</tr>
<tr>
<td style="text-align: right;"><strong>7</strong></td>
<td><strong>Manage</strong> <strong>&amp; Monitor</strong> <strong>the</strong> <strong>Platform</strong></td>
<td>Design and implement the capabilities and practices required to operate, monitor, and optimize the platform through lifecycle management, observability, cost governance , and performance monitoring.</td>
</tr>
<tr>
<td style="text-align: right;"><strong>8</strong></td>
<td><strong>Drive Adoption &amp; Value Realization</strong></td>
<td>Drive organizational adoption through change management, skilling and training, stakeholder engagement, and value realization to ensure sustained business impact.</td>
</tr>
</tbody>
</table>

This table below defines the project scope and assumptions for developing and deploying the platform. It outlines how **Microsoft** and **Ford** will deliver a combination of **(2)** **Department Agents** and **(2)** **Prototype Agents,** based on four **(4)** **identified** **use cases** that will be used to validate feasibility and value, followed by a limited production deployment to a set of **Pilot** users.

<img src="media/image8.png" style="width:6.5in;height:3.32222in" />

Figure 2: Project scope

<table style="width:96%;">
<caption><p><span id="_Toc231555273" class="anchor"></span>Table 3: Project scope</p></caption>
<colgroup>
<col style="width: 18%" />
<col style="width: 42%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;">Item</th>
<th style="text-align: center;">Scope</th>
<th style="text-align: center;">Assumptions</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;"><strong>Prototype Agents</strong></td>
<td><p>Develop up to two (<strong>2</strong>) Prototype Agents</p>
<ul>
<li><p>The Prototypes will be used to confirm if the proposed use cases will deliver measurable benefits and demonstrate that the technology, integrations, and data sources can support the solution.</p></li>
</ul></td>
<td><ul>
<li><p>The following two (<strong>2</strong>) use cases will be developed by a Microsoft Partner as non-production prototypes:</p></li>
<li><p><strong>Use Case 1</strong>: <strong>Supplier Downtime and SLA Credit Automation</strong></p>
<ul>
<li><p>Monitors supplier outage/downtime events, cross-references SLA contract terms, detects breaches, calculates owed credits, and generates dispute communications for human review and approval.</p></li>
</ul></li>
<li><p><strong>Use Case 2: Vendor Quote &amp; Contract Document Management Analysis</strong></p>
<ul>
<li><p>Extracts information from vendor quotes and contracts, applying business rules, and presenting the results for user review, validation, and approval.</p></li>
</ul></li>
</ul></td>
</tr>
<tr>
<td style="text-align: left;"><strong>Department agents</strong></td>
<td><p>Develop up to two (<strong>2</strong>) Department Agents</p>
<ul>
<li><p><strong>First Pilot Department Agent</strong></p>
<ul>
<li><p><strong>Engineering &amp; Product Development</strong> will be the first candidate for the pilot.</p></li>
</ul></li>
<li><p><strong>Second Pilot Department Agent</strong></p>
<ul>
<li><p>Will be selected based on the outcome of one of the Prototype Agents below.</p></li>
<li><p>Alternatively, another department will be selected, if neither Prototype Agents are ready nor viable to be included as part of a Department Agent.</p></li>
</ul></li>
</ul></td>
<td><ul>
<li><p>The initial solution will be deployed to a limited group of up to twenty (<strong>&lt;20</strong>) North American pilot users for a selected department.</p></li>
<li><p>Up to two (<strong>2</strong>) use cases will be developed as part of the Department Agents:</p>
<ul>
<li><p><strong>Use Case</strong> <strong>3</strong>: Virtual Program Manager (Product Development Coordination). Initial pilot is limited to a smaller North America program (Mid Cycle Action MCA).</p></li>
<li><p><strong>Use Case</strong> <strong>4</strong>: To be determined based on one (1) of the Prototype Agents. Alternatively, a new use case will be selected.</p></li>
</ul></li>
<li><p>Following the development of the above use cases, any available remaining capacity may be utilized to design and develop additional use cases.</p></li>
</ul></td>
</tr>
<tr>
<td style="text-align: left;"><strong>Production Deployment</strong></td>
<td>Deploy one (<strong>1</strong>) of the Department Agents to Production.</td>
<td><ul>
<li><p>The <strong>Engineering &amp; Product Development Agent</strong> will be deployed into Production as a Pilot.</p></li>
</ul></td>
</tr>
<tr>
<td style="text-align: left;"><strong>System Integrations</strong></td>
<td><p>The Agentic AI solutions will initially integrate with the following systems:</p>
<ul>
<li><p>SAP Ariba</p></li>
<li><p>Snow (Service Now/Dynatrace)</p></li>
<li><p>SharePoint (access pdf’s)</p></li>
<li><p>Microsoft Fabric (One Lake)</p></li>
</ul></td>
<td><ul>
<li><p>Assumes existing enterprise systems, APIs, and data sources are accessible via out of the box (OOTB) Copilot / Power Automate connectors, otherwise sample files will be leveraged for solution demonstration and validation.</p></li>
<li><p>The following systems will be evaluated and referenced as part of the solution and system integration architecture &amp; design.</p>
<ul>
<li><p>Google Cloud Platform (GCP), Google (Big Query), Teamcenter, Oracle HCM, Nicus, GitHub, and Jira/Confluence/Atlassian</p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## Technology requirements

The products and technology listed in the following table are required for the project. Ford is responsible for obtaining all licenses, products, or subscriptions. This list is subject to change based on adjustments made to desired outcomes or direction of the project.

| **Product and technology item** | **Description** | **Ready by** | **Responsibility** |
|----|----|----|----|
| **ADO (Azure DevOps)** | Used for work item tracking, backlog management, and source control for solution development and delivery activities. | Start of project | Ford |
| **Power Platform** | Enables low-code/no-code automation, app development, and integration of business processes using Power Apps, Power Automate, and related services. | Start of project | Ford |
| **Copilot Studio** | Platform for building, deploying, and managing custom AI-powered agents and workflows tailored to Ford’s business scenarios. | Start of project | Ford |
| **Dataverse** | Secure, scalable data platform for storing and managing business data, supporting integration with Power Platform apps, automation, and analytics. | Start of project | Ford |
| **Microsoft Azure AI Foundry, Azure AI Agent Services, Azure AI Search, Azure Document Intelligence, Azure Logic Apps, Application Insights** | Provides enterprise AI services for building, orchestrating, searching, and processing intelligent AI solutions, including agent development, document extraction, retrieval, and generative AI capabilities. | Start of project | Ford |
| **Microsoft Fabric** | Microsoft Fabric is a unified data platform that connects, manages, analyzes, and visualizes data in one integrated environment. | Start of project | Ford |
| **Microsoft** **Azure** **subscription** | Cloud platform subscription required to provision, manage, secure, and host Azure services, environments, integrations, and AI workloads supporting the solution. | Start of project | Ford |
| **Microsoft Agent 365** | A centralized control plane that enables organizations to govern, secure, and manage AI agents at scale across the Microsoft 365 ecosystem. | Start of project | Ford |
| **Microsoft 365, Microsoft Teams** | Collaboration and productivity platforms are used for communication, meetings, document collaboration, notifications, and integration with AI-powered business processes and agents. | Start of project | Ford |
| **Microsoft Entra, Microsoft Entra Id** | Identity and access management platforms are used for user authentication, role-based access control, single sign-on, and secure access to applications, services, and AI solutions. | Start of project | Ford |

<span id="_Toc231555274" class="anchor"></span>Table 4: Technology requirements

## Environment requirements

Ford will supply and maintain all environments used for the development and delivery of lifecycles during this project. Ford will obtain the required Azure subscriptions and provide Microsoft with administrative control to build the development and test environments, as needed.

| **Environment** | **Location** | **Responsible for configuration and maintenance** | **Subscription ownership** | **Ready by** |
|----|----|----|----|----|
| **UAT (Acceptance)** | Microsoft Azure, Microsoft 365, Power Platform | Ford | Ford | Start of engagement |
| **Production** | Microsoft Azure, Microsoft 365, Power Platform | Ford | Ford | Start of engagement |
| **Development** | Microsoft Azure, Microsoft 365, Power Platform | Ford | Ford | Start of engagement |
| **QA Test (Functional/System Integration Testing)** | Microsoft Azure, Microsoft 365, Power Platform | Ford | Ford | Start of engagement |
| **Master** | Microsoft Azure, Microsoft 365, Power Platform | Ford | Ford | Start of engagement |

<span id="_Toc231555275" class="anchor"></span>Table 5: Environment requirements

## Exclusions

Any area not explicitly included in the sections above, describing the outcomes and requirements, will not be provided by Microsoft during this project. Exclusions from the Services provided by Microsoft for this project include the following.

<table style="width:95%;">
<caption><p><span id="_Toc213430935" class="anchor"></span>Table 6: Exclusions</p></caption>
<colgroup>
<col style="width: 41%" />
<col style="width: 53%" />
</colgroup>
<thead>
<tr>
<th>Area</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Product licenses and subscriptions</td>
<td>Product licenses (Microsoft or non-Microsoft) and cloud service subscriptions are not included, unless otherwise noted in the <a href="#technology-requirements"><em>Technology requirements</em></a> section.</td>
</tr>
<tr>
<td>Hardware</td>
<td>Microsoft will not provide hardware for this project.</td>
</tr>
<tr>
<td>Client</td>
<td>Deployment and configuration of client software is out of scope for the project.</td>
</tr>
<tr>
<td>Product bugs and upgrades</td>
<td>Product upgrades, bugs, and design change requests for Microsoft products.</td>
</tr>
<tr>
<td>Organizational redesign</td>
<td>Designing or redesigning the Customer’s functional organization is not included.</td>
</tr>
<tr>
<td>Branding</td>
<td>Microsoft will not create or design any graphical elements or corporate branding elements related to this project.</td>
</tr>
<tr>
<td>User communications</td>
<td>Microsoft will not manage any direct user communications associated with the project.</td>
</tr>
<tr>
<td>In-class training</td>
<td>Formal in-class user training or the creation of custom training materials.</td>
</tr>
<tr>
<td>Governance and regulatory compliance</td>
<td>Microsoft will not be responsible for assessment or review of governance or regulatory compliance.</td>
</tr>
<tr>
<td>Deployment, installation, configuration, and testing</td>
<td><p>The following items are not included:</p>
<ul>
<li><p>Deployment and/or configuration of new Azure environments.</p></li>
<li><p>Installation, configuration, and testing of non-Microsoft software other than software identified as within scope.</p></li>
<li><p>Testing and configuration of applications and services outside of those required to support the deployment of the solution.</p></li>
<li><p>On-premises software or hardware installation, this includes software such as Microsoft Data Integration Runtime.</p></li>
</ul></td>
</tr>
<tr>
<td>Network and storage</td>
<td>Troubleshooting or remediation of existing network and storage systems is not in scope.</td>
</tr>
<tr>
<td>Data quality &amp; cleansing</td>
<td><p>Data cleansing is out of scope.</p>
<p>Any data quality issues, remediation and the resulting additional effort are out of scope.</p>
<p>These issues include but are not limited to:</p>
<ul>
<li><p>Duplicate rows.</p></li>
<li><p>Missing or empty data column.</p></li>
<li><p>Variable size schema (i.e. inconsistent or unexpected number of columns).</p></li>
<li><p>Inconsistent timestamps.</p></li>
<li><p>Unexpected data types (i.e. Character strings in numeric columns).</p></li>
<li><p>Unresolved lookups.</p></li>
</ul></td>
</tr>
<tr>
<td>Machine learning</td>
<td>Training or fine-tuning of models using customer data is out of scope.</td>
</tr>
<tr>
<td>Process reengineering</td>
<td>Redesign or re-engineering of the Customer’s business processes is not included.</td>
</tr>
<tr>
<td>Organizational design</td>
<td>Designing – or redesigning – the Customer’s functional organization is not included.</td>
</tr>
<tr>
<td>Information security/application development policies</td>
<td>Information security and application development policies will not be created.</td>
</tr>
<tr>
<td>Application security code review</td>
<td>Security code review of an application or applications outside of the current project scope.</td>
</tr>
<tr>
<td>System integration</td>
<td>Modifications to third-party systems or external interfaces to support integration are not in scope for this project.</td>
</tr>
<tr>
<td>Customer-specific security and compliance</td>
<td>Implementation of Customer-specific security and/or compliance requirements. If the Customer requires Microsoft to assist with implementation of Customer-specific security and/or compliance requirements, then this will be handled via the change management process.</td>
</tr>
<tr>
<td>User support</td>
<td>User issue troubleshooting is out of scope; Customer is responsible for user support.</td>
</tr>
<tr>
<td>Regulatory compliance</td>
<td>Customer is solely responsible for its regulatory compliance and must highlight to Microsoft any technical adjustment required to be compliant. Any unforeseen technical adjustment will follow the change management process as described in section <a href="#change-management-process">Change management process</a>.</td>
</tr>
<tr>
<td>Comprehensive security and compliance assessment, mitigation, or implementation</td>
<td><p>Microsoft security and compliance review is limited to the scope of features within this engagement and is intended to target the commercially reasonable context of this application in view of Customer’s information security, compliance, and data privacy policies.</p>
<p>A complete or comprehensive security and compliance assessment for Customer marketplace and technology environment is out of scope, along with mitigation or security solutions not explicitly included in the scope of the engagement.</p></td>
</tr>
<tr>
<td>Regulatory Standards</td>
<td>Certification of the application solution to any regulatory standards.</td>
</tr>
<tr>
<td>Guarantees and SLAs/OLAs</td>
<td>Performance guarantees, availability commitments, and Service Level Agreements (SLAs) or Operational Level Agreements (OLAs) are expressly out of scope for this project. No commitments regarding system performance, uptime, or service levels are provided or implied as part of this engagement.</td>
</tr>
<tr>
<td>UX/UI (User Experience/Interface)</td>
<td>All functionalities will rely on Microsoft out-of-box (OOB) features and OOB UI. Custom UX development or modification is expressly excluded from scope.</td>
</tr>
<tr>
<td>Organizational readiness for M365 Copilot</td>
<td>Adoption, change management activities specific to M365 Copilot for users are excluded from this scope.</td>
</tr>
</tbody>
</table>

# Definitions and acronyms

The following table lists terms, initialisms, and acronyms used in this document.

| Term / acronym | Description |
|----|----|
| Backlog | The set of epics, features, and user stories that are prioritized and assigned to resources during sprints to direct the effort of the feature teams to work toward the Customer outcomes and desired business value. |
| CPM | Consulting product manager. The role assigned to lead a feature team. Responsibilities are outlined in the <span class="mark"></span>[*Feature team*](#feature-team) section of this document. |
| DOD / DOR | Definition of Done, Definition of Ready |
| Informal knowledge transfer | The exchange of information between Microsoft staff and the Customer staff as they work together on the project. |
| IaC | Infrastructure as Code (IaC)-based (CI/CD) deployment pipeline(s). |
| CI/CD | Continuous Integration and Continuous Deployment automate application build, testing, and deployment processes to improve speed, quality, and reliability. |
| Prototype | A software product with just enough core features to deliver value to early users and gather feedback for future development. The purpose of a prototype is to learn quickly, prove value, reduce risk, and establish the foundation for enterprise-scale deployment. |
| OKRs | Objectives and key results. A set of measurable goals and metrics used to track progress toward reaching valued business outcomes. |
| PBI | Product backlog item. An item tracked in DevOps. Also known as a “work item.” Typically, these items can be individual tasks, stories, epics, features, or other custom items as defined for a particular project. |
| Product increment | Depending on the type of project, a “product increment” can be any combination of the following (but not limited to): documentation of standards, policies, and procedures; landing zones; security templates; operational playbooks; or user stories completed within a sprint. |
| SLI/ SLO | Service-level indicator; Service-level objective |
| SME | Subject matter expert. A person with specific knowledge or expertise in a particular area. For example, a security SME, or database SME. |
| SOC | A SOC (Security Operations Center) is a centralized team or function responsible for monitoring, detecting, and responding to cybersecurity threats across an organization. |
| SOW | Statement of work |
| Sprint planning | A single meeting will be held at the start of each sprint to review and assign PBIs that meet DOR and will be delivered during the sprint. In some exceptional cases, planning may extend past the first day. The consulting product manager (CPM) and feature team will attend, along with key stakeholders. |
| Sprint retrospective | A single meeting will be held at the end of each sprint to give the feature team an opportunity to review its performance and implement improvements for subsequent sprints. Identified improvements can be made during subsequent sprints. |
| Sprint review | A single meeting will be held at the end of each sprint to evaluate the progress and update the product backlog, if needed. The CPM and feature team will attend along with key stakeholders. |
| UAT | User acceptance testing activities used to validate business processes, solution functionality, integrations, and user readiness prior to production deployment. |
| ESWO | Enterprise Service Work Order |

<span id="_Toc213430936" class="anchor"></span>Table 7: Table of abbreviations

# Delivery approach, completion, and timeline

## Overview

This project uses an agile approach based on the scrum framework ([http://scrumguides.org](http://scrumguides.org/)) for delivery.

During baseline planning, Microsoft and the Customer will work together to elaborate and refine the product backlog to the level necessary to plan an initial product release for future delivery sprints.

## Delivery approach

### Sprint process

Microsoft will undertake an iterative delivery approach that is based on a fixed-capacity, fixed-duration, variable-scope process known as the scrum process. The goal of each sprint is a product increment that can be released into production. The key tenets are as follows:

- Joint ownership of decisions

- Short implementation units (sprints)

- Prioritization of business and technical debt objectives in a product backlog

- Time-bound planning for each sprint

- Emphasis on the remaining work

- Sprints that produce a releasable product increment

- Sprint demonstrations that are time-restricted and have regular checkpoints

- An automated approach to build, deployment and configuration of the solution

- Regular retrospective meetings that may be used for course correction

<figure>
<img src="media/image10.png" style="width:6.5in;height:3.65833in" />
<figcaption><p><span id="_Toc222472757" class="anchor"></span>Figure 3: Iterative delivery approach - Scrum process</p></figcaption>
</figure>

At the end of each sprint, the Microsoft project manager, CPM, Customer product owner, and applicable Customer decision makers will review the progress made against the objectives to determine if any adjustments need to be made using the change management process.

Due to the fixed-capacity, fixed-duration nature of the delivery, at the conclusion of the project, some backlog items may not be completed. The Microsoft team will rely on the Customer to keep an updated and prioritized set of objectives so that the most important backlog items can be completed during the project to support the most important outcomes.

### Project initiation

At the beginning of the project, the following prerequisites must be completed. These tasks must be completed before envisioning, baseline planning, and delivery sprints begin.

<table>
<caption><p><span id="_Toc213430937" class="anchor"></span>Table 8: Project initiation activities</p></caption>
<colgroup>
<col style="width: 31%" />
<col style="width: 68%" />
</colgroup>
<thead>
<tr>
<th>Category</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><p><strong>Microsoft activities</strong></p>
<p>The activities to be performed by Microsoft</p></td>
<td><ul>
<li><p>Conduct a pre-initiation call or meeting to initiate team formation and communicate expectations.</p></li>
<li><p>Document the project launch prerequisites using input from this SOW.</p></li>
<li><p>Track the status of launch prerequisites and adjust the project initiation phase start date accordingly.</p></li>
<li><p>Conduct a detailed walk-through of the SOW with the Customer to agree upon an initial project schedule and approach.</p></li>
<li><p>Help the Customer identify the required roles and stakeholders and names for workshops and the initial feature team.</p></li>
<li><p>Work with the Customer to identify the stakeholders and subject matter experts (SMEs) that will function as a feature team.</p></li>
<li><p>Initiate the onboarding of Microsoft resources into the Customer environment.</p></li>
<li><p>Conduct a preparation call with Customer stakeholders to brief them on the envisioning framework and approach and agree on the key focus areas and stakeholders for envisioning.</p></li>
<li><p>Collaborate with the Customer to identify key business and IT stakeholders and SMEs who will participate in discovery and envisioning workshops.</p></li>
<li><p>Deliver an agile/scrum workshop.</p></li>
</ul></td>
</tr>
<tr>
<td><p><strong>Customer activities</strong></p>
<p>The activities to be performed by the Customer</p></td>
<td><ul>
<li><p>Identify Customer team members who will be available for the duration of the project.</p></li>
<li><p>Identify a sponsor who is empowered to prioritize business decisions and act as a single point of contact for questions relating to the product vision and objectives.</p></li>
<li><p>Identify a product owner who will be the single point of contact for questions relating to the product backlog.</p></li>
<li><p>Attend and participate in the pre-initiation call.</p></li>
<li><p>Assign project initiation and launch prerequisites responsibilities to accountable Customer leadership and establish target completion dates.</p></li>
<li><p>Complete the project initiation and launch prerequisites.</p></li>
<li><p>Allocate roles to be filled by the Customer with the required Customer resources in the time frames agreed upon in the pre-initiation call.</p></li>
<li><p>Assisting with any orientation activities Microsoft requires to begin the project.</p></li>
<li><p>Provision the necessary environments, resources and tools as needed to support delivery.</p></li>
<li><p>Provide Microsoft team members with access to required environments and tools.</p></li>
<li><p>Provide Microsoft with the required permissions to manage and configure repositories, pipelines and boards in the Automation environment.</p></li>
<li><p>Provision a new Git repository in the Customer’s Automation environment and provide access for Microsoft team members.</p></li>
<li><p>Provision dedicated resource groups in each of the environments listed in the environments section.</p></li>
<li><p>Create a Microsoft Entra service principal with resource group owner permissions for each of the resource groups that has been provisioned. These service principles will be used by the automated deployment pipelines to deploy and configure the solution including configuring role-based access controls.</p></li>
<li><p>Identify potential data / content to be considered for ingestion into the system and provide samples, as needed by Microsoft.</p></li>
<li><p>Conduct a preparation call with Microsoft to discuss and agree on Discovery and Envisioning Workshop objectives and logistics.</p></li>
<li><p>Assign primary points of contact (business and technical) for the discovery and envisioning activities.</p></li>
<li><p>Identify key business and technical decision makers and SMEs who will participate in the discovery and envisioning workshops.</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Product baseline planning

Baseline planning will be **two weeks (2)** in duration.

During baseline planning, the feature team will construct the initial product backlog for implementing the baseline solution, a high-level architecture and an initial release plan. At the completion of this exercise, the outcomes, assumptions, and dependencies will be verified.

Should there be any material deviations from the initial estimated capacity and/or skills, these and their implications will be discussed. The impact of such changes will be addressed through the change management process.

<table>
<caption><p><span id="_Toc213430938" class="anchor"></span>Table 9: Product baseline planning activities</p></caption>
<colgroup>
<col style="width: 21%" />
<col style="width: 78%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;">Category</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;"><strong>Microsoft activities (The activities to be performed by Microsoft)</strong></td>
<td>• Conduct baseline planning workshops with Customer stakeholders and SMEs to align on <strong>business outcomes</strong>, personas, and the workflows where agentic capabilities will be embedded <strong>in the flow of work</strong>.<br />
<br />
• Collaborate with customers to define success criteria and outcome-oriented measures (e.g., OKRs) for the initial release intent and translate them into <strong>epics/features</strong> (avoid detailed user-story commitments in the SOW).<br />
<br />
• Establish the <strong>platform-centric delivery intent</strong>: define the baseline platform pattern that is <strong>modularized, scalable, secure, and reusable</strong>, enabling repeatable onboarding of multiple use cases over time (not one-off agents).<br />
<br />
• Define the phased roadmap and delivery plan for the engagement (Product Strategy &amp; Envisioning → Foundations &amp; Feasibility → Capability &amp; Advancement → Productionize &amp; Govern) and align this to the initial backlog sequencing.<br />
<br />
• <strong>Model strategy (for orchestration/runtime and workloads):</strong> define the approach for selecting and governing foundation models for targeted workloads, including (as applicable and approved) OpenAI GPT family models (e.g., GPT‑4 class and newer, <strong>GPT‑5 where available</strong>), Anthropic <strong>Claude</strong>, and other approved models. Confirm model selection criteria (quality, safety, latency, cost, regional availability), routing/fallback strategy, and model governance expectations.<br />
<br />
• <strong>Agentic framework strategy:</strong> define the approach for building and orchestrating agents using Microsoft-supported agentic patterns and frameworks (as applicable), including Microsoft agent framework components and/or commonly used agent frameworks such as <strong>Lang Graph</strong> (and similar orchestration frameworks) to support multi-step, multi-agent workflows. Establish guidance for tool-calling patterns, workflow orchestration, and agent handoffs aligned to governance requirements.<br />
<br />
• Define the governance approach for the platform, including evaluation, guardrails &amp; controls, privacy, security, and access management expectations.<br />
<br />
• <strong>Agent 365 (governance/observability):</strong> define how Agent 365 (or equivalent Microsoft governance/observability capability) will be used to support <strong>registry, access control, monitoring/telemetry, observability, and lifecycle visibility</strong> for agents and tools (as applicable to scope).<br />
<br />
• Define an evaluation and validation approach that supports iterative improvement across quality, safety, and performance. Establish how pilot feedback will be captured and used to refine prompts, tools, and agent workflows.<br />
<br />
• Architecture and resource setup (high-level): confirm target environments, required platform services, identity/access approach, and operational constraints. Confirm required access to subscriptions, repos, pipelines, and environments.<br />
<br />
• Data review: inventory candidate data sources (structured/unstructured), identify grounding sources, document access constraints, and identify known gaps and remediation needs (owned by Customer unless explicitly in scope).<br />
<br />
• Team and process alignment: confirm roles/responsibilities, working agreements, ceremony cadence, backlog hygiene, and Definition of Ready / Definition of Done expectations. Populate the initial sprint backlog with planned epics/features for Sprint 1.<br />
<br />
• Collaborate with the Product Owner to confirm the Sprint Goal for the first delivery sprint and identify key risks/impediments that may affect delivery sequencing.<br />
<br />
• Define a test approach and automation pipeline plan for in-scope testing described in the Testing and defect remediation section (as applicable).</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Customer activities (The activities to be performed by the Customer)</strong></td>
<td>• Allocate and make available required Customer roles (sponsor, product owner, SMEs, security/compliance contacts) within the time frames agreed in initiation.<br />
<br />
• Participate in baseline planning workshops; provide workflow context, current-state constraints, policies, and success measures needed to define outcome-oriented priorities.<br />
<br />
• Provide relevant documentation and business requirements; clarify requirements and approve priorities at the epic/feature level.<br />
<br />
• Provision and/or approve access to required environments, tooling, and repositories; complete internal governance steps needed to begin delivery.<br />
<br />
• Identify candidate data sources and ensure appropriate access approvals are in place for planned grounding and integrations (as applicable).<br />
<br />
• Confirm security, compliance, and Responsible AI expectations; provide timely feedback via agreed review channels and decision-makers.<br />
<br />
• Define the UAT/pilot validation approach; identify pilot users for feedback and usability validation (as applicable).<br />
<br />
• Collaborate with Microsoft to validate the initial backlog and initial release intent and to agree the Sprint Goal for the first delivery sprint.</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Key assumptions</strong></td>
<td>• Customer representatives (especially sponsors and product owners) are available throughout baseline planning for timely decisions and prioritization.<br />
<br />
• Key roles (business SMEs, technical SMEs, security/compliance stakeholders) are available and knowledgeable about target workflows and systems relevant to initial scenarios.<br />
<br />
• Required environments, tooling access, and approvals are completed in time to support planned sprint starts.<br />
<br />
• Model availability and usage (including GPT family models, Claude, and other models) is subject to <strong>Customer approvals, licensing, regional availability, quota/capacity constraints, and enterprise policy</strong>.<br />
<br />
• The backlog will be refined during baseline planning, which may change sequencing, scope emphasis, and/or required skills/capacity; material deviations are handled through the change management process.</td>
</tr>
</tbody>
</table>

Each delivery sprint will last **four to six** weeks. Microsoft and the Customer will collaborate to determine the final duration for sprints during baseline planning.

Before sprint planning starts, the product owner will collaborate with the feature team to define a sprint goal and a proposed sprint backlog. This sprint backlog will consist of a set of PBIs that the feature team estimates may be completed during the sprint.

The first half-day of every sprint will be set aside to plan for that sprint. In some exceptional cases, planning may extend past the first half-day. The feature team, the product owner, and the Microsoft project manager will attend. During sprint planning the following activities will take place:

- The feature team will review each PBI. The feature team will determine if there is sufficient information to begin development. The Microsoft team may seek clarification from the product owner. If there is insufficient information to begin work on a PBI and the product owner cannot provide clarification during the meeting, the feature team may defer the story to a later sprint or the product backlog.

- The feature team will determine which PBIs can be accomplished during the sprint. If the proposed sprint backlog is too large, the team will collaborate with the product owner to defer PBIs to a later sprint or the product backlog. If the proposed scope is too small, the team will collaborate with the product owner to add PBIs. The PBIs selected for the sprint are solely determined by the feature team.

- The feature team will determine the technical feasibility of a PBI. If the technical feasibility of a user story requires further investigation, a corresponding PBI may be added to investigate potential solutions. If the feature team determines that a PBI is not feasible, the feature team can remove the story from the backlog.

- The team will work to decide how the work will be accomplished. This may include design discussions, updates to the architecture, and a breakdown of PBIs into tasks.

During the delivery sprint, the feature teams will build out the solution with planned PBIs and architecture, which will be updated, if it is required. The feature team will hold daily standup meetings to keep everyone informed and to report any impediments.

During the sprint, if the feature team determines that a PBI cannot be completed within the sprint, it will be deferred to a later sprint after consultation with the team and the product owner. If the feature team has extra capacity in a sprint, it will collaborate with the product owner to select PBIs to be added to the sprint backlog. Changes to the sprint backlog should not compromise the sprint goal. The Microsoft project manager is the sole decision maker on scope changes during the sprint.

The last day of the sprint is usually dedicated to demonstrating the functionality that has been achieved and to carrying out a retrospective of the sprint. Microsoft and the Customer will review the delivered outcomes after every sprint to determine if changes are needed (for example, updates to the backlog/desired outcomes). Product changes during the sprint should be minimized so delivery times and sprint goals are not affected. Sprint retrospectives help determine where the team succeeded, and where improvements can be made. The product owner reviews the completed stories and marks them as Done or Not Done based on the Definition of Done.

<table>
<caption><p><span id="_Toc213430939" class="anchor"></span>Table 10: Delivery sprints activities</p></caption>
<colgroup>
<col style="width: 31%" />
<col style="width: 68%" />
</colgroup>
<thead>
<tr>
<th>Category</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><p><strong>Microsoft activities</strong></p>
<p>The activities to be performed by Microsoft</p></td>
<td><p>The following activities will be performed during each delivery sprint:</p>
<ul>
<li><p>Collaborate with the Customer to jointly agree the priority of items in the backlog.</p></li>
<li><p>Review the PBIs assigned to a sprint.</p></li>
<li><p>Determine whether sufficient information is available for each PBI. A PBI will be flagged if more clarification is needed; if clarification cannot be provided, the team may decide to defer the PBI to a later sprint.</p></li>
<li><p>Conduct a sprint planning meeting with the Customer at the beginning of each sprint to agree on a sprint goal and plan the PBIs that will be included in the sprint backlog.</p></li>
<li><p>Determine whether the PBIs assigned to a sprint can be completed within that sprint based on available capacity and interdependencies across PBIs.</p></li>
<li><p>Conduct and participate in regular scrum meetings. Collaborate with the Customer to design and plan for the implementation of the PBIs.</p></li>
<li><p>Complete assigned PBIs in the sprint backlog according to the individual PBI acceptance criteria and Definition of Done (DOD).</p></li>
<li><p>Perform testing as defined in ‎the <mark></mark><em><a href="#testing-and-defect-remediation">Testing and defect remediation</a></em> section.</p></li>
<li><p>Collaborate with the product owner to create a proposed scope for future sprints, including a set of PBIs ready to be assigned.</p></li>
<li><p>Collaborate with the product owner to manage the backlog.</p></li>
<li><p>Identify impediments to project delivery progress.</p></li>
<li><p>Provide ongoing refinement of the effort estimate (effort remaining) for PBIs based on the development progress, dependencies, and architectural constraints or needs.</p></li>
<li><p>Explore external dependencies.</p></li>
<li><p>Review and refine the risk list.</p></li>
<li><p>Provide ongoing collaboration with the Customer to reassess the remaining resource capacity based on the progress of delivery, refined product backlog, and understanding of requirements.</p></li>
<li><p>At the end of a sprint, the following activities will be conducted:</p></li>
</ul>
<ul>
<li><p>Sprint review: a single meeting held at the end of the sprint to inspect the outcome of the sprint and determine future adaptations if needed. Attendance by the product owner is mandatory; attendance by Customer Stakeholders is optional but recommended. (See sprint completion section for detail).</p></li>
<li><p>Sprint retrospective: an opportunity for the scrum team to plan ways to increase quality and effectiveness.</p></li>
</ul></td>
</tr>
<tr>
<td><p><strong>Customer activities</strong></p>
<p>The activities to be performed by the Customer</p></td>
<td><ul>
<li><p>Collaborate with Microsoft to jointly agree the priority of items in the backlog.</p></li>
<li><p>Attend and participate in sprint planning meetings and workshops, as necessary.</p></li>
<li><p>Attend and participate in regular scrum meetings, as necessary.</p></li>
<li><p>Help refine PBIs and provide timely clarifications.</p></li>
<li><p>Provide updated background information, documentation, and business requirements.</p></li>
<li><p>Provide all necessary documents, content and information required to implement and test the solution.</p></li>
<li><p>Collaborate with Microsoft to create the proposed scope for future sprints.</p></li>
<li><p>Complete assigned PBIs in the sprint backlog according to the individual PBI acceptance criteria and Definition of Done (DOD).</p></li>
<li><p>Provide the required level of access to Customer systems to allow Microsoft team members to complete assigned PBIs.</p></li>
<li><p>Perform testing as defined in ‎the <mark></mark><a href="#testing-and-defect-remediation"><em>Testing and defect remediation</em></a> section.</p></li>
<li><p>Help to identify and remove any impediments.</p></li>
<li><p>Manage and complete tasks associated with the Customer’s internal governance processes.</p></li>
<li><p>Collaborate with the Microsoft team to deploy the solution into the Development and QA environments.</p></li>
<li><p>Collaborate with Microsoft to implement automated deployment pipelines in the Automation environment that will deploy the baseline solution to each of the other environments listed in the environments section.</p></li>
<li><p>Deploy the solution into the production environment using the automated deployment scripts developed with Microsoft.</p></li>
<li><p>Implement automated jobs for loading content and data into the solution.</p></li>
<li><p>Attend the sprint review meetings and provide feedback.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Key assumptions</strong></td>
<td><ul>
<li><p>Customer representatives, especially the product owner and sponsor, will be available throughout the duration of the sprint.</p></li>
<li><p>The backlog will be continually refined in each sprint, which may result in changes to overall scope and changes to required skills and/or capacity.</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Testing and defect remediation

#### Testing

The following types of testing are included in the project.

<table>
<caption><p><span id="_Toc213430940" class="anchor"></span>Table 11: Testing in scope</p></caption>
<colgroup>
<col style="width: 17%" />
<col style="width: 36%" />
<col style="width: 15%" />
<col style="width: 15%" />
<col style="width: 15%" />
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
<td><strong>Automated unit tests</strong></td>
<td>Automated tests that cover a single component.</td>
<td>Feature team</td>
<td>Feature team</td>
<td>Customer</td>
</tr>
<tr>
<td><strong>Deployment testing</strong></td>
<td>Testing to validate the deployment of the solution to environments other than development.</td>
<td>Customer</td>
<td>Feature team</td>
<td>Microsoft</td>
</tr>
<tr>
<td><strong>Functional testing</strong></td>
<td>Tests performed by a feature team within a delivery sprint to validate that the product features function in accordance with the acceptance criteria defined for features and PBIs.</td>
<td>Feature team</td>
<td>Feature team</td>
<td>Customer</td>
</tr>
<tr>
<td><strong>System integration testing</strong></td>
<td>Tests performed to validate that the deployed solution operates as designed, across functionality delivered by different feature teams.</td>
<td>Feature team</td>
<td>Feature team</td>
<td>Customer</td>
</tr>
<tr>
<td><strong>Iterative prompt refinement /</strong></td>
<td>Testing of different prompt variations and agent logic to validate and refine agent responses.</td>
<td>Feature team</td>
<td>Feature team</td>
<td>Microsoft</td>
</tr>
<tr>
<td><strong>UAT</strong></td>
<td>Tests the user functionality of key real-world scenarios. UAT will be conducted over the course of the project according to the UAT time frames agreed upon during baseline planning (as described in the <a href="#product-baseline-planning">Product baseline planning</a> section). Feedback from UAT (defect or new PBIs) and other backlog items will be added to the product backlog and prioritized alongside other PBIs.</td>
<td>Customer</td>
<td>Customer</td>
<td>Microsoft</td>
</tr>
</tbody>
</table>

#### Defect remediation

If possible, defects found by the feature team during a delivery sprint are fixed within the sprint itself. Defects that cannot be resolved during the sprint will be added to the product backlog. Defects found elsewhere will become part of the product backlog and be prioritized alongside other PBIs.

During testing, ​Customer and Microsoft will jointly evaluate solution-related defects and their priority based on the following definitions.

<table style="width:100%;">
<caption><p><span id="_Toc215587312" class="anchor"></span>Table 12: Defects priority definitions</p></caption>
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
<td><strong>P1 </strong></td>
<td><p><strong>Blocking defect </strong> </p>
<p>Development, testing, or production launch cannot proceed until this type of defect is corrected. A defect of this type blocks further progress in this area. The solution cannot ship, and the project team cannot achieve the next milestone until such a defect is corrected. </p></td>
<td>Yes </td>
</tr>
<tr>
<td><strong>P2 </strong></td>
<td><p><strong>Significant defect</strong> </p>
<p>The defect must be fixed prior to moving to production. Such a defect, however, will not affect test plan implementation. </p></td>
<td>Yes </td>
</tr>
<tr>
<td><strong>P3 </strong></td>
<td><p><strong>Important defect</strong> </p>
<p>It is important to correct the defect. However, it is possible to move forward into production using a workaround. </p></td>
<td>No; the defect will be logged. Remediation will be performed through an agreed-upon change request only. </td>
</tr>
<tr>
<td><strong>P4 </strong></td>
<td><p><strong>Enhancements and cosmetic defects</strong> </p>
<p>Feature enhancement and cosmetic defects, including design requests that vary from original concepts. </p></td>
<td>No; the defect will be logged. Remediation will be performed through an agreed-upon change request only. </td>
</tr>
</tbody>
</table>

### Delivery compliance, privacy and security

Microsoft will support our data protection commitments in the following areas:

<table style="width:100%;">
<colgroup>
<col style="width: 29%" />
<col style="width: 37%" />
<col style="width: 32%" />
</colgroup>
<thead>
<tr>
<th><strong>Area</strong></th>
<th><strong>Description</strong></th>
<th><strong>Assumptions</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Data Protection Questionnaire (DPQ)</td>
<td><ul>
<li><p>Conduct discovery <em>of</em> customer<em>’s</em> data protection environment for engagement delivery.</p></li>
</ul>
<ul>
<li><p>Complete a Microsoft-internal data protection questionnaire (DPQ) that provides a view of current issues and compliance requirements that may be required according to applicable data protection requirements.</p></li>
</ul>
<p>The DPQ covers data discovery, classification, and the applicability of security controls.</p></td>
<td><ul>
<li><p>Customer to provide Microsoft with a baseline understanding of customer<em>’s</em> relevant data protection requirements.</p></li>
<li><p>Customer to provide Microsoft inputs for data classification to determine personal, sensitive personal, confidential, and highly confidential data.</p></li>
</ul></td>
</tr>
<tr>
<td>Solution security design review</td>
<td><ul>
<li><p>Review and assess the solution architecture for design-related security issues.</p></li>
<li><p>Recommend mitigations for identified design-related security issues.</p></li>
</ul></td>
<td><ul>
<li><p>Customer will provide Microsoft with of customer<em>’s</em> relevant security policy documentation.</p></li>
<li><p>Customer Subject Matter Experts (SME)s will participate in the security design review.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Outputs

Microsoft will provide the following outputs.

<table>
<caption><p><span id="_Toc213430941" class="anchor"></span>Table 13: Outputs</p></caption>
<colgroup>
<col style="width: 27%" />
<col style="width: 58%" />
<col style="width: 13%" />
</colgroup>
<thead>
<tr>
<th>Name</th>
<th>Description</th>
<th>Acceptance required</th>
</tr>
</thead>
<tbody>
<tr>
<td>Scenario description document</td>
<td>A Word document or PowerPoint presentation that describes the desired business outcomes (in terms of OKRs) and anticipated business benefits for a mutually agreed AI scenario.</td>
<td>No</td>
</tr>
<tr>
<td>Initial product backlog</td>
<td>An initial product backlog that defines the high-level epics and features for a solution that will address the desired business outcomes for the mutually agreed AI scenario.</td>
<td>No</td>
</tr>
<tr>
<td>Initial release plan</td>
<td>A plan showing the desired outcomes and key features that should be delivered during the initial release of the product.</td>
<td>No</td>
</tr>
<tr>
<td>Sprint completion report</td>
<td>This report lists the PBIs that have been completed during the sprint, any planned work that was not completed, and any project risks or problems. This report is produced as an output of each sprint.</td>
<td>No</td>
</tr>
<tr>
<td>Security Recommendations (PowerPoint)</td>
<td>PowerPoint prioritizing Microsoft recommendations for securing the foundation through native platform features and functionality.</td>
<td>No</td>
</tr>
<tr>
<td>Solution Overview Document (PowerPoint)</td>
<td><p>For each selected Agentic Use Case, Ford will receive the following products:</p>
<ul>
<li><p><strong>Solution Architecture Diagram:</strong> Visual blueprint detailing the technical design and integration points for the agentic solution.</p></li>
<li><p><strong>Application Development Runbook:</strong> Step-by-step documentation of the build process, configuration, and deployment instructions for the developed application.</p></li>
</ul></td>
<td>No</td>
</tr>
<tr>
<td><strong>Prototype Design</strong> <strong>Document</strong> <strong>(Word)</strong></td>
<td>Defines the architecture, core capabilities, and integration of points required to implement a minimally viable AI agent using Microsoft ecosystem services. Documents how the agent ingests data, orchestrates workflows, and produces outputs to support build, iteration, and scaling.</td>
<td>No</td>
</tr>
<tr>
<td><strong>Prototype Code and Configuration</strong> <strong>(Solution Files)</strong></td>
<td>Implements the AI agent(s) through code development and platform configuration using Microsoft services. Establishes the required logic, integrations, and settings to enable data ingestion, workflow orchestration, and output generation.</td>
<td>No</td>
</tr>
</tbody>
</table>

## Completion and definition of done

### Sprint completion

Sprints will end based on the calendar schedule defined during Baseline Planning. At the conclusion of each sprint, feature teams will conduct a sprint review and sprint retrospective. During the sprint review, completed work will be demonstrated. At the end of each sprint, Microsoft will provide a sprint completion report.

### Backlog item completion

Backlog items do not require formal sign-off or Customer acceptance when they are completed by the feature team.

As part of each sprint review, the Customer will review each backlog item (user story or defects) completed in the delivery sprint and confirm whether it is considered done using the Definition of Done agreed during Project Baseline Planning. Each backlog item that is done will be recorded as such in Azure DevOps. The results will also be captured as part of the sprint completion report.

The status of each completed backlog item must be updated in Azure DevOps within five days after the sprint review meeting is complete.

Items that are not considered done at the end of a sprint will be moved to the product backlog and prioritized alongside other backlog items during sprint planning.

Any defects found in a finished backlog item will be added to the product backlog as a defect and prioritized alongside the other backlog items. A finished backlog item may also prompt the Customer product owner to include additional backlog items to enhance the software.

## Timeline

The timeline for this project is relative to the project start date. All dates and durations provided are estimates only. The specific timeline will be finalized during baseline planning and will be updated as part of core project planning activities.

Microsoft will provide the Microsoft team described in the [*Project organization*](#project-organization) section for a period not to exceed ***26 weeks*** or until the capacity defined in the WO is consumed. The Microsoft team will work on the highest priority outcomes, specified by the Customer, as described in the Customer Goals section.

The high-level timeline of the project is depicted in the following image.

<img src="media/image11.png" style="width:6.5in;height:3.97569in" />

<span id="_Toc222472758" class="anchor"></span>Figure 4: High-level timeline

# Project organization

## Project staffing

The role descriptions for each area in the project organization are shown in the roles and responsibilities table in the sections that follow. The capacity available for each Microsoft resource is specified in the WO. If more resource capacity of any role is needed, it can be added through the change management process.

### Customer roles

<table>
<caption><p><span id="_Toc231555284" class="anchor"></span>Table 14: Customer roles</p></caption>
<colgroup>
<col style="width: 16%" />
<col style="width: 66%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr>
<th>Roles</th>
<th>Responsibilities</th>
<th>Commitment</th>
</tr>
</thead>
<tbody>
<tr>
<td>Executive Sponsor</td>
<td><ul>
<li><p>Participates in the steering committee.</p></li>
<li><p>Provides overall strategic direction and project approval.</p></li>
<li><p>Secures and allocates necessary budget and resources.</p></li>
<li><p>Resolves high-level escalations and organizational roadblocks.</p></li>
<li><p>Ensures project aligns with corporate strategic goals.</p></li>
<li><p>Champions the project to all key executive stakeholders.</p></li>
</ul></td>
<td><ul>
<li><p>minimum of 10%</p></li>
</ul></td>
</tr>
<tr>
<td>Project Sponsor</td>
<td><ul>
<li><p>Defines and approves the project charter, scope, and objectives.</p></li>
<li><p>Makes key project decisions, serve as a point of escalation, and clears project roadblocks.</p></li>
<li><p>Provides guidance on business priorities and constraints.<br />
Secures and commits key business resources and subject matter experts.</p></li>
<li><p>Communicates project status and decisions to the Executive Sponsor.</p></li>
</ul></td>
<td><ul>
<li><p>minimum of 25%</p></li>
</ul></td>
</tr>
<tr>
<td>Project Manager</td>
<td><ul>
<li><p>Oversees and coordinates the overall engagement decisions / schedule / budget / status.</p></li>
<li><p>Oversees Customer resource allocation, risk management, engagement priorities, and communication with executive management.</p></li>
<li><p>Coordinates resources and drives internal processes necessary to deliver the program.</p></li>
<li><p>Serves as the primary point of contact for the Microsoft team.</p></li>
<li><p>Supports development of the discovery phase project plan and timeline.</p></li>
<li><p>Coordinates and schedules meetings with all key stakeholders.</p></li>
<li><p>Manages project risks, issues, and dependencies.</p></li>
<li><p>Communicates the project efforts and activities to executive committee members and stakeholders.</p></li>
<li><p>Ensures effective communication and collaboration among all stakeholders.</p></li>
</ul></td>
<td><ul>
<li><p>minimum of 75%</p></li>
</ul></td>
</tr>
<tr>
<td>Product Owner</td>
<td><ul>
<li><p>Serves as the single point of contact for decisions about product backlog items and prioritization.</p></li>
<li><p>Take responsibility for making decisions on services and/or product features.</p></li>
<li><p>Serves as the primary person responsible for user story scope decisions during sprint planning.</p></li>
<li><p>Speaks to business vision, technology roadmap, and project objectives.</p></li>
<li><p>Defines acceptance criteria for work items, especially user stories.</p></li>
<li><p>Serves as the single point of contact for decisions about product backlog items and prioritization.</p></li>
<li><p>Provides Microsoft teams with prompt answers to questions affecting development activities and, more generally, services to be delivered.</p></li>
</ul></td>
<td><ul>
<li><p>Full Time</p></li>
</ul></td>
</tr>
<tr>
<td>Process Owner (s)</td>
<td><ul>
<li><p>Provides knowledge of current business processes.</p></li>
<li><p>Identifies pain points, inefficiencies, and opportunities for improvement.</p></li>
<li><p>Defines the desired future state ("To-Be") business processes.</p></li>
<li><p>Acts as a communication bridge between the project team and subject matter experts.</p></li>
</ul></td>
<td><ul>
<li><p>minimum of 50%</p></li>
</ul></td>
</tr>
<tr>
<td>Subject Matter Experts (SMEs)</td>
<td><ul>
<li><p>Provides in-depth expertise in specific business areas (e.g., finance, supply chain).</p></li>
<li><p>Clarifies functional details and constraints of current systems and processes.</p></li>
<li><p>Participates in workshops and provides input for process discovery.</p></li>
<li><p>Reviews proposed solutions related to their domain.</p></li>
</ul></td>
<td><ul>
<li><p>minimum of 25%</p></li>
</ul></td>
</tr>
<tr>
<td>Architecture Lead</td>
<td><ul>
<li><p>Partner with the Microsoft architecture led to review business needs and objectives.</p></li>
<li><p>Serve as the primary technical point of contact for the Microsoft partner team.</p></li>
<li><p>Provide requirements and make decisions related to the architecture and deployment plan.</p></li>
<li><p>Review engagement work products and provide feedback.</p></li>
<li><p>Advise on prioritization decisions.</p></li>
<li><p>Participate in Architecture Review Board (ARB) sessions to review and approve architectural decisions.</p></li>
</ul></td>
<td><ul>
<li><p>25%~50%</p></li>
</ul></td>
</tr>
<tr>
<td>Integration &amp; Data Architect</td>
<td><ul>
<li><p>Presents and discusses current data sources and data models.</p></li>
<li><p>Attends workshops on the proposed future state data architecture.</p></li>
<li><p>Presents existing system integrations overview diagrams.</p></li>
<li><p>Support the definition of a high-level integration strategy and architecture.</p></li>
<li><p>Presents existing data flow, protocols, and APIs for key integration point.</p></li>
<li><p>Attends workshops on the proposed future state integration architecture.</p></li>
</ul></td>
<td><ul>
<li><p>minimum of 25%</p></li>
</ul></td>
</tr>
<tr>
<td>Infrastructure &amp; Security Lead</td>
<td><ul>
<li><p>Presents the current IT infrastructure and security landscape.</p></li>
<li><p>Support the definition of a future state infrastructure for the solution.</p></li>
<li><p>Supports the requirements for future state system environments (development, testing, production).</p></li>
</ul></td>
<td><ul>
<li><p>minimum of 25%</p></li>
</ul></td>
</tr>
<tr>
<td>Change management lead (including sponsors, leaders, and champions)</td>
<td><ul>
<li><p>Manage and coordinate change management activities, and identify sponsors, leaders, and champions.</p></li>
<li><p>Attend activities, sessions, workshops, or classes relevant to his or her scope of influence and help drive the change program.</p></li>
<li><p>Identify, schedule, and assist with coordinating interviews and gathering organizational information.</p></li>
<li><p>Drive persona group adoption activities, including ongoing business value measurement.</p></li>
</ul></td>
<td><ul>
<li><p>25%~50%</p></li>
</ul></td>
</tr>
<tr>
<td>Training Lead</td>
<td><ul>
<li><p>This member of your organization is responsible for technology training and learning.</p></li>
<li><p>Attend activities, sessions, workshops, or classes relevant to his or her scope of influence and help drive program learning initiatives.</p></li>
</ul></td>
<td><ul>
<li><p>25%</p></li>
</ul></td>
</tr>
<tr>
<td>Community Lead</td>
<td><ul>
<li><p>This member of your organization, usually 1 or 2 individuals, act as leaders and manage the overall Pioneers community.</p></li>
<li><p>Attend activities, sessions, workshops, or classes relevant to his or her scope of influence and help drive program champion engagement initiatives.</p></li>
</ul></td>
<td><ul>
<li><p>25%</p></li>
</ul></td>
</tr>
</tbody>
</table>

### Microsoft roles

This project uses a time and material delivery model. Microsoft will provide Ford with a delivery team staffed as defined below and in the Enterprise Services Work Order (ESWO). If additional capacity and/or skills are needed to deliver the desired project objectives or if additional project objectives need to be defined, the change management process will be followed.

<table>
<caption><p><span id="_Toc231555285" class="anchor"></span>Table 15: Microsoft roles</p></caption>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
</colgroup>
<thead>
<tr>
<th>Role</th>
<th>Responsibilities</th>
</tr>
</thead>
<tbody>
<tr>
<td>Microsoft project sponsor</td>
<td><ul>
<li><p>Make key project decisions, serve as a point of escalation, and clear project roadblocks.</p></li>
</ul></td>
</tr>
<tr>
<td>Delivery Management Executive</td>
<td><ul>
<li><p>Serve as the primary point of contact for overall satisfaction and concerns related to services provided by Microsoft.</p></li>
<li><p>Serve as the single point of contact for billing issues, personnel matters, and contract extensions.</p></li>
<li><p>Facilitate project governance activities.</p></li>
</ul></td>
</tr>
<tr>
<td>Project manager</td>
<td><ul>
<li><p>Manage the Microsoft project delivery and coordinate the overall project to deliver it according to schedule.</p></li>
<li><p>Serve as the primary point of contact for the Microsoft team.</p></li>
<li><p>Serves as the point of contact for contract extensions, personnel matters, and billing.</p></li>
<li><p>Take responsibility for change management, project priorities, status communications, and status meetings.</p></li>
<li><p>Coordinate Microsoft resources and partners subcontracted to Microsoft, including staffing, task assignments, and status reporting.</p></li>
<li><p>Coordinate decisions within three (3) business days, or according to an otherwise agreed-upon timeline.</p></li>
<li><p>Facilitate planning, regular standup meetings, and reviews</p></li>
</ul></td>
</tr>
<tr>
<td>Delivery Lead / Architect</td>
<td><ul>
<li><p>Serve as the primary Microsoft point of contact for business engagement at the project level, ensuring alignment with agreed scope and objectives.</p></li>
<li><p>Facilitate business and technical workshops to explore customer needs, pain points, and strategic priorities.</p></li>
<li><p>Guide use case ideation and prioritization by helping the Customer articulate business scenarios and value drivers that will form the Use Case Inventory.</p></li>
<li><p>Translate business objectives into actionable insights for solution design without performing detailed fit-gap analysis.</p></li>
<li><p>Provide industry and Microsoft best-practice guidance to ensure proposed use cases align with proven patterns and deliver measurable value.</p></li>
<li><p>Collaborate with technical leads to validate feasibility and dependencies for identified use cases.</p></li>
</ul></td>
</tr>
<tr>
<td>Solution architect</td>
<td><ul>
<li><p>Serve as the primary Microsoft point of contact for the respective technical domain or solution area.</p></li>
<li><p>Own solution design and architecture to ensure the proposed solution meets the outcomes of prioritized use cases.</p></li>
<li><p>Collaborate with business / industry architect to translate business requirements into technical specifications and solution components.</p></li>
<li><p>Identify the right Microsoft technologies and patterns to deliver expected business value and align with recommended practices.</p></li>
<li><p>Lead technical workshops and design sessions focused on solution feasibility, integration, and performance.</p></li>
<li><p>Provide guidance on implementation approach, dependencies, and scalability based on Microsoft-recommended practices.</p></li>
<li><p>Ensure technical alignment across all phases and validate that the solution supports agreed KPIs and success criteria.</p></li>
<li><p>Participate in Architecture Review Board (ARB) sessions to review and approve architectural decisions.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Power Platform Consultant</strong></td>
<td><ul>
<li><p>Participate in the agile development of Power Platform solutions, including configuration, customization, and automation of business processes.</p></li>
<li><p>Collaborate with onshore and customer teams to deliver technical components, integrations, and enhancements according to solution architecture.</p></li>
<li><p>Develop and document build tasks, technical specifications, and iterative releases for assigned use cases.</p></li>
<li><p>Support testing activities by preparing test data, executing test scripts, and addressing defects during development cycles.</p></li>
<li><p>Provide technical input for fit-gap analysis, solution design, and implementation planning.</p></li>
<li><p>Coordinate with project managers and architects to track progress, manage dependencies, and address technical issues across workstreams.</p></li>
<li><p>Transfer knowledge and implementation details to customer and project team members as required.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Dev Lead/Scrum Master</strong></td>
<td><ul>
<li><p>Lead the offshore development team</p></li>
<li><p>Serve as Scrum Master, facilitating sprint planning, daily stand-ups, sprint reviews, and retrospectives.</p></li>
<li><p>Coordinate with onshore and offshore teams to align backlog priorities, clarify requirements, and remove impediments.</p></li>
<li><p>Track progress of development tasks, manage sprint commitments, and iterative releases.</p></li>
<li><p>Support the translation of solution architecture into actionable development tasks and oversee their execution.</p></li>
<li><p>Foster a culture of continuous improvement, technical excellence, and agile recommended practices within the offshore team.</p></li>
<li><p>Report status, risks, and issues to the Project Manager and participate in project governance as required.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Tester</strong></td>
<td><ul>
<li><p>Build and execute test scripts for assigned features and user stories.</p></li>
<li><p>Conduct functional, system, and integration testing across project environments.</p></li>
<li><p>Log defects, track resolution status, and retest fixes during development cycles.</p></li>
<li><p>Participate in test case reviews and contribute to test data preparation.</p></li>
<li><p>Provide user acceptance testing (UAT) support and document test results.</p></li>
<li><p>Collaborate with developers, test leads, and project teams to clarify requirements and resolve issues.</p></li>
<li><p>Transfer testing knowledge</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Security Architect</strong></td>
<td><ul>
<li><p>Lead and conduct solution security design reviews for project components.</p></li>
<li><p>Provide guidance on security architecture, risk identification, and mitigation strategies.</p></li>
<li><p>Advise on implementation of security controls, compliance requirements, and data protection standards.</p></li>
<li><p>Collaborate with Ford and Microsoft teams to address high-risk configurations and recommend technical solutions.</p></li>
<li><p>Document security recommendations, decisions, and rationale for project records.</p></li>
<li><p>Participate in Architecture Review Board (ARB) sessions to review and approve security-related architectural decisions.</p></li>
<li><p>Support knowledge transfer on recommended security practices to project stakeholders.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Security Consultant</strong></td>
<td><ul>
<li><p>Conducts the solution security design review</p></li>
<li><p>Provide guidance and assistance to the engagement team to identify high risk configurations and recommend mitigations for the most significant risks of the solution design.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>ACSM Architect</strong></td>
<td><ul>
<li><p>Provide oversight and governance for the Microsoft Organizational Enablement delivery.</p></li>
<li><p>Take responsibility for Microsoft Organizational Enablement resource allocation, risk management, engagement priorities, and communication with executive management.</p></li>
<li><p>Verify that the work is completed according to the plan.</p></li>
<li><p>Provide Organizational Enablement thought leadership.</p></li>
<li><p>Deliver Organizational Enablement sessions, workshops, classes, work products, in accordance with the engagement scope.</p></li>
<li><p>Verify that engagement sponsors are equipped with the knowledge and tools needed to be effective leaders of change.</p></li>
<li><p>Participate in Architecture Review Board (ARB) sessions to review and approve architectural decisions.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>ACSM Consultant/s</strong></td>
<td><ul>
<li><p>Have deep knowledge of, and skills in, specific Organizational Enablement domains.</p></li>
<li><p>Take responsibility for the Organizational Enablement delivery of sessions, workshops, work products related to their areas of expertise.</p></li>
<li><p>Verify that Ford change managers are equipped with the knowledge and tools needed to effectively manage the change network.</p></li>
<li><p>Adoption Content Creation/Curation.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Executive steering committee

The executive steering committee provides overall senior management oversight and strategic direction for the project. In addition, it removes obstacles for the project team. The executive steering committee for the project will meet with the frequency defined in the communication plan and will include the roles listed in the table below.

| **Role**                            | **Organization** |
|-------------------------------------|------------------|
| Executive sponsor                   | Ford             |
| Project sponsor                     | Ford             |
| Project manager                     | Ford             |
| Key Business Stakeholder (s)        | Ford             |
| Product Owner                       | Ford             |
| Delivery Management Executive (DME) | Microsoft        |
| Project manager                     | Microsoft        |
| Architect (Solution)                | Microsoft        |
| Architect (Delivery Lead)           | Microsoft        |

<span id="_Toc213430942" class="anchor"></span>Table 16: Executive steering committee roles and responsibilities

## Product council

The product council is the primary mechanism for aligning stakeholders and dealing with competing priorities. It acts as the forum where the strategy is agreed upon so that all key decision makers understand what decisions are being made about the direction of the product and why. The product council allows the feature teams to maintain autonomy while simultaneously determining the overall priorities for business outcomes.

<figure>
<img src="media/image13.png" style="width:6.5in;height:3.14097in" />
<figcaption><p>Figure 4: Product council</p></figcaption>
</figure>

Ultimately, the product council is formed to define and share the product strategy and roadmap. It also makes decisions needed to resolve any conflicting product priorities.

In addition to the roles listed below, all product managers and technical leads from the individual feature teams are also members of the product council.

| **Role**                             | **Organization** |
|--------------------------------------|------------------|
| Product Owner                        | Ford             |
| Process Owner (s)                    | Ford             |
| Integration & Data Architect         | Ford             |
| Infrastructure & Security Lead       | Ford             |
| Architect (Solution Architect)       | Microsoft        |
| Architect (Delivery Lead)            | Microsoft        |
| Architect (Organizational readiness) | Microsoft        |
| Architect (Security readiness)       | Microsoft        |
| Development Lead                     | Microsoft        |

<span id="_Toc231555287" class="anchor"></span>Table 17: Product council roles

## Feature team

Following the scrum model, Microsoft uses a feature team approach to deliver a project. All scrum roles will be represented within the feature team. This team is an autonomous and empowered unit that has all the capabilities to design, develop, test, and release features to achieve the Customer outcomes. A feature team consists of a product manager, scrum master, technical lead, SMEs, and engineers with various development, test, deployment, infrastructure, security, data, and operation skills.

The roles listed below are typical and representative for feature teams, though they may differ, depending on the project. The skill sets of the engineers will also be different, depending on the project.

| **Role**                                     | **Organization** |
|----------------------------------------------|------------------|
| Business Process owner (s)                   | Ford             |
| Product owner                                | Ford             |
| Subject matter experts (SMEs)                | Ford             |
| Architect (Delivery Lead)                    | Microsoft        |
| Architect (Solution)                         | Microsoft        |
| Developer / Engineer                         | Microsoft        |
|                                              |                  |
|                                              |                  |
| Development Lead                             | Microsoft        |
| Security consultant (s)                      | Microsoft        |
| Adoption and change management consultant(s) | Microsoft        |

<span id="_Toc213430944" class="anchor"></span>Table 18: Feature team roles and responsibilities

# Project governance

The governance structure and processes the team will abide by for the project are described in the following sections.

## Project communication

In addition to the communication mechanisms built into the delivery approach, the following will be used to communicate during the project:

- **Communication plan**: this document will describe the frequency, audience, and content of communication with the team and stakeholders. Microsoft and the Customer will develop it as part of project planning.

- **Status reports**: the Microsoft team will prepare and issue regular status reports to project stakeholders per the frequency defined in the communication plan.

- **Status meetings**: per the frequency defined in the communication plan, the Microsoft team will schedule regular status meetings to review the overall project status, available delivery data, and open problems and risks.

## Risk and issue management

The following general procedure will be used to manage active project issues and risks during the project:

- **Identify**: identify and document project issues (current problems) and risks (potential events that could impact the project).

- **Analyze and prioritize** assess the impact and determine the critical risks and issues that will be actively managed.

- **Plan and schedule**: determine how to manage critical risks and assign responsibility for risk management and issue resolution.

- **Track and report**: monitor and report the status of risks and issues.

- **Escalate**: escalate to project sponsors critical issues and risks the team is unable to resolve without assistance.

- **Control**: review the effectiveness of the risk and issue management actions.

Active issues and risks will be monitored and reassessed every week.

## Change management process

During the project, either party may request modifications to the Services described in this SOW. The agile approach, used by Microsoft, does not guarantee that all items defined in the product backlog will be completed, nor that all outcomes will be achieved. Should the Customer decide to continue work after project completion (described in the <span class="mark"></span>[*Project completion*](#project-completion) section), the Customer may request a change by following the process below.

Requested changes take effect only when the proposed change is agreed upon by both parties. The change management process steps are:

- **The change is documented**: Microsoft will document all change requests in a Microsoft change request form. The change request form includes:

<!-- -->

- A description of the change.

- The estimated effect of implementing the change.

<!-- -->

- **The change is submitted**: Microsoft will provide the change request form to the Customer.

- **The change is accepted or rejected**: the Customer will accept or reject the change within three business days and confirm the following to Microsoft:

<!-- -->

- Acceptance – the Customer must sign and return the change request form.

- Rejection – if the Customer does not want to proceed with the change or does not provide an approval within three business days, no changes will be performed.

## Escalation path

The product managers, executive sponsors, and other designees will work closely together to manage project issues, risks, and change requests as described previously. The Customer will provide reasonable access to the sponsor or sponsors to expedite resolution. The standard escalation path for review, approval, or dispute resolution is as follows:

- Project team member

- Product manager and project managers

- Product Sponsor, council and/or delivery management executive

- Executive steering committee

## Project completion

Microsoft will provide Services defined in this SOW to the extent of the fees available and the term specified in the WO. If additional Services are required, the change management process will be followed, and the contract modified. The project will be considered complete when at least one of the following conditions has been met:

- All available capacity has been utilized for Services delivered.

- The term of the project has expired.

- All Microsoft activities and product backlog items have been completed.

- The WO has been terminated.

Due to the nature of agile delivery, not all backlog items or outcomes may be completed during the project. The Microsoft team will rely on the CPM in conjunction with the product council to determine priority of the product backlog so that the important backlog items can be completed during the project.

# Customer responsibilities and project assumptions

## Customer responsibilities

The Customer is responsible for:

- Providing accurate, timely, and complete information within three business days or as mutually agreed upon.

- Providing access to people, including knowledgeable Customer personnel and business users as required.

- Providing sufficient Customer resources with the requisite skills for testing during the project.

- Providing all requisite information to relevant external parties to obtain clearances for all personnel actively participating in the project, if security clearances are required.

- Providing access to systems for both onsite and remote work.

- Providing a suitable work environment when onsite presence is required.

- Managing all Customer personnel and vendors who are not managed by Microsoft.

- Managing external dependencies for related projects or programs.

- Confirming regulatory compliance, if applicable.

- Providing standard product training for external systems as required.

- Overseeing organizational change management:

- Redesigning or re-engineering business processes.

- Designing or redesigning the functional organization.

- Planning or undertaking user communications.

- Other general Customer responsibilities.

- The Customer first responder organization is responsible for initial triaging after all releases.

- Providing application support.

- Fixing bugs and troubleshooting problems that are related to applications or other third-party software, hardware products, or applications that are not explicitly mentioned as being in scope.

- Preparing documentation about processes, standards, policies, and existing guidelines.

- Designing, configuring, integrating, deploying, or fixing issues in commercially available third-party software.

- Implementing modifications to third-party systems and external interfaces to support integration.

## Project accountabilities

<table>
<caption><p><span id="_Toc231555289" class="anchor"></span>Table 19: Project accountabilities</p></caption>
<colgroup>
<col style="width: 3%" />
<col style="width: 48%" />
<col style="width: 24%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;">#</th>
<th style="text-align: center;">Program &amp; Solution Areas</th>
<th style="text-align: center;">Microsoft</th>
<th style="text-align: center;">Customer</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;"><strong>1</strong></td>
<td><strong>Project Management</strong></td>
<td style="text-align: center;">Responsible<br />
(Overall Project)</td>
<td style="text-align: center;">Responsible<br />
(Client Deliverables)</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><strong>Governance bodies and functions</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Steering committee</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Change control board</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><strong>Program governance and standards</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Provide business direction, accountable for business outcomes</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Manage project communications (meeting cadences)</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Manage scope management and change control</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Manage program schedule</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"><strong>2</strong></td>
<td><strong>Organizational Change Management</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Change Strategy and Guidance</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Change Impact Assessment &amp; Job Impact</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Change Strategy Execution</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Training Strategy Design</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Power / End User Training</p></li>
</ul></td>
<td style="text-align: center;">Informed</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong>3</strong></td>
<td><strong>Business Process &amp; Requirements</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Process Reviews &amp; Design Updates</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Use Case Definition &amp; Requirements</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"><strong>4</strong></td>
<td><strong>Solution Modeling &amp; Configuration</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Provide solution direction, accountable for solution delivery outcomes</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Schedule and facilitate solution, data, and integration architecture workshops</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Define enterprise architecture principles, standards and patterns</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li></li>
</ul></td>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Solution Design &amp; Blueprint (End to End)</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Solution Configuration, Development &amp; Reviews (walkthrough)</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted / Informed</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Solution Deployment (Production)</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Solution Support (Post Go-Live)</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong>5</strong></td>
<td><strong>Solution Testing</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Test Strategy and Schedule Definition</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted / Informed</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Unit &amp; Functional Testing</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted / Informed</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>System Integration &amp; Acceptance Testing</p></li>
</ul></td>
<td style="text-align: center;">Consulted / Informed</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong>6</strong></td>
<td><strong>Infrastructure</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Strategy &amp; Guidance</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Setup &amp; Management</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Release Pipeline Design &amp; Management</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong>7</strong></td>
<td><strong>Security</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Strategy &amp; Guidance</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Configuration &amp; Testing</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong>8</strong></td>
<td><strong>Integrations &amp; Interfaces</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Enterprise Integration Strategy</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>API Development (Co-Pilot &amp; Power Automate)</p></li>
</ul></td>
<td style="text-align: center;">Responsible</td>
<td style="text-align: center;">Consulted</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>API Development (Middleware &amp; Non-Copilot / Power Automate Systems)</p></li>
</ul></td>
<td style="text-align: center;">Informed</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td><ul>
<li><p>Development of middleware services across multiple legacy systems (Centralized APIs)</p></li>
</ul></td>
<td style="text-align: center;">Informed</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong>9</strong></td>
<td><strong>Data</strong></td>
<td style="text-align: center;"><strong> </strong></td>
<td style="text-align: center;"><strong> </strong></td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Data Estate Strategy</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Data Readiness Assessment</p></li>
</ul></td>
<td style="text-align: center;">Consulted</td>
<td style="text-align: center;">Responsible</td>
</tr>
<tr>
<td style="text-align: center;"><strong> </strong></td>
<td><ul>
<li><p>Data Preparation &amp; Cleansing</p></li>
</ul></td>
<td style="text-align: center;">Informed</td>
<td style="text-align: center;">Responsible</td>
</tr>
</tbody>
</table>

## Scope assumptions

<table>
<colgroup>
<col style="width: 54%" />
<col style="width: 45%" />
</colgroup>
<thead>
<tr>
<th><strong>Project Scope</strong></th>
<th><strong>Assumptions</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Secure the platform</strong></td>
</tr>
<tr>
<td><ol type="A">
<li><p><strong>Implement</strong> <strong>AI Security Foundation</strong></p></li>
</ol>
<ul>
<li><p>Advisory and governance services to define and implement a tailored AI security strategy aligned with enterprise architecture, governance standards, and digital transformation objectives.</p></li>
</ul></td>
<td><ul>
<li><p>Ford will designate key stakeholders responsible for security governance and decision-making.</p></li>
<li><p>Ford will identify stakeholder participation in workshops, planning sessions, and project governance activities.</p></li>
</ul></td>
</tr>
<tr>
<td><ol start="2" type="A">
<li><p><strong>Enable the Agentic Security Operations Center (SOC)</strong></p></li>
</ol>
<ul>
<li><p>Deploy agentic threat detection and response capabilities to improve security operations.</p></li>
</ul></td>
<td><ul>
<li><p>Ford will provide security operations and security engineering stakeholders to provide decision-making for agentic SOC capabilities.</p></li>
<li><p>Ford will ensure stakeholder participation in workshops, planning sessions, and project governance activities.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Integrate &amp; productionize</strong></td>
<td></td>
</tr>
<tr>
<td><p>Microsoft will support the deployment of a production-grade enterprise-hardened agent:</p>
<ul>
<li><p>Infrastructure as Code (IaC)-based (CI/CD) deployment pipeline(s).</p></li>
<li><p>Agent performance tuning &amp; autoscaling strategy.</p></li>
</ul></td>
<td><ul>
<li><p><strong>Production approvals:</strong></p>
<ul>
<li><p>Ford completes required production approvals and operational readiness steps.</p></li>
<li><p>Ford will perform IaC deployment to production.</p></li>
</ul></li>
<li><p><strong>Operations ownership:</strong></p>
<ul>
<li><p>Ford identifies ops owners for monitoring, incident response, and runbook execution post-handover.</p></li>
</ul></li>
<li><p><strong>Budgeting &amp; scaling:</strong></p>
<ul>
<li><p>Ford plans for ongoing platform/service usage at scale and agrees with the support/operations model.</p></li>
</ul></li>
</ul></td>
</tr>
<tr>
<td><p><strong>Responsible AI + Evaluation</strong></p>
<ul>
<li><p>Establish Responsible AI and evaluation practices with built-in quality, safety, governance, and accountability controls to support secure, compliant, and reliable AI-driven workflows.</p></li>
</ul></td>
<td><ul>
<li><p><strong>RAI alignment:</strong> Ford aligns on Responsible AI standards, usage boundaries, and governance expectations for targeted use cases and user groups.</p></li>
</ul>
<ul>
<li><p><strong>Validation support:</strong> Ford participates in defining evaluation criteria and provides validation support through test cases, feedback, and review cycles.</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Adoption &amp; change management</strong></td>
<td></td>
</tr>
<tr>
<td><p><strong>Accelerate Adoption (readiness) &amp; Foster Change</strong></p>
<ul>
<li><p>Agent Adoption</p>
<ul>
<li><p>Define a persona-based adoption strategy for the AI solution with key business stakeholders.</p></li>
<li><p>Execute the defined persona-based strategy to drive adoption of AI agents.</p></li>
</ul></li>
<li><p>Adoption strategy for future scale</p>
<ul>
<li><p>Establish a champions network to accelerate AI agent adoption and prepare the organization for broader future adoption.</p></li>
</ul></li>
</ul></td>
<td><ul>
<li><p>Ford will provide organizational change management resources to support adoption activities.</p></li>
<li><p>Ford will provide operational governance resources to support ongoing management and oversight of AI agent-based solutions.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Project assumptions

The following are assumptions that apply to this project between the Customer and Microsoft. During the project, the information and assumptions in this document will be validated, and if a material difference is present, this could result in Microsoft initiating a change request to cover additional work or extend the project duration.

- Workday:

<!-- -->

- Local Microsoft employees will follow the standard Microsoft (or appropriate subsidiary) workday and work week.

- If Microsoft Global Delivery factories are used, then the following also apply:

<!-- -->

- The standard workday for the offshore Microsoft factory team is between 9:30 AM and 6:30 PM India standard time, Monday through Friday, except for scheduled holidays. Limited exceptions can be made with advanced planning to support production-level changes or to address a need that requires a meeting between an offshore resource and the Customer, and which cannot be accomplished during the standard workday. Exceptions will be coordinated by the program manager.

- Offshore resources that are not part of the factory will be available between 7 AM and 10 PM India standard time over an eight-hour continuous window.

<!-- -->

- Remote work:

<!-- -->

- The Microsoft feature team may perform Services remotely.

- If the Microsoft feature team is required to be present at the Customer location every week, resources will typically be on site for three nights and four days, arriving on Monday and leaving on a Thursday.

- The place of performance under the SOW may be at a Microsoft facility, a customer facility, or various remote and off-site locations (including Microsoft employee home offices).

<!-- -->

- Language:

<!-- -->

- All project communications and documentation will be in English. Local language support and translations will be provided by the Customer.

<!-- -->

- Staffing:

<!-- -->

- If necessary, Microsoft will make staffing changes. These may include, but are not limited to, resources and project roles.

- If a security clearance is required, all resources will have the appropriate level of security access required to complete project-related efforts.

- Resource mobilization for staffing the project will be six (***6**) weeks*.

<!-- -->

- Informal knowledge transfer:

<!-- -->

- No formal training materials will be developed or delivered as part of this project. All information transfer will be through informal knowledge transfer.

<!-- -->

- Known standards:

<!-- -->

- Microsoft expects to use Azure DevOps, Azure Pipelines and might use GitHub for standard delivery.

- Time will be required to learn the Customer tooling if there are deviations from Microsoft standards. This time has not been included in project estimates.

- Microsoft will use standard Azure DevOps process templates, and other IP designed to speed up delivery, including, but not limited to, standard work items, pipelines, and document templates.

- Other assumptions:

- In addition to project team members, the Customer shall allow Microsoft internal systems to access the mutually accessible delivery platforms and tools used for this project.

- Microsoft will read, store, and share necessary delivery insights on the work artifacts and products generated as part of this project (for example, test cases, code base, and pipelines) that are hosted on mutually accessible delivery platforms, like Azure DevOps, Jira, and GitHub.

- Microsoft will make available to the Customer all data and insights gathered during the project. Microsoft will purge said data and insights upon explicit Customer requests or at the end of the project.

- Holidays, vacations, and training time have not been factored into this SOW.

- All work is to be contiguously scheduled. Any breaks in the project calendar must be scheduled four weeks in advance, or the time will be billed without interruption.

- The Customer required compliance training for regulated industries is not included in the estimation. This includes:

- Security training

- Internal orientation

- Financial compliance training

- Healthcare compliance training

- Procedures outside of Microsoft standard compliance

- Background checks, fingerprinting, badging, and authentication

- Browser compatibility testing has not been included in the project. If desired, backlog items may be added and prioritized for this effort.

- The Customer will meet the necessary requirements to help make sure the solution design meets regulatory requirements.

- During the project under this SOW, if the requested business outcome includes Microsoft developing or deploying an AI System for or with Customer which may be considered a sensitive use, Microsoft will conduct an internal responsible AI review, to include assessment of and requirements for the potential sensitive use. The outcome of the review will be discussed with the Customer and Microsoft will act in compliance with its responsible AI principles, including making any required modifications. For more information about Microsoft’s responsible AI principles please refer to <https://aka.ms/RAI>**.**

- If localization support is required to support additional languages, it may be added to the product backlog.

- Azure services and technology

- Azure services and Azure-supported Microsoft technologies will be used to develop the solution.

- The components to be developed by Microsoft will be cloud hosted.

- Microsoft will not modify any existing code base that was not produced by the Microsoft delivery team.

- Azure DevOps

- Either the Customer will provide a Microsoft Azure DevOps services account that is accessible by all team members, or Microsoft will provide an account (possibly with limited Customer access).

- If the Customer approves a solution design that uses a product that is not generally available, the Customer acknowledges this, and accepts that it may affect the project cost and timeline.

- When the Customer determines that Microsoft or its agents will have access to personal identifiable information, the Customer is obligated to inform Microsoft within five (**5**) days that further access to that information requires the use of equipment owned or supplied by the Customer.

- Any purchased GitHub Consulting Services are provided by GitHub, Inc., a wholly owned subsidiary of Microsoft Corporation. Notwithstanding anything to the contrary in your Work Order, the GitHub Privacy Statement available at [**https://aka.ms/github_privacy**](https://aka.ms/github_privacy) and the GitHub Data Protection Addendum and Security Exhibit located at [**https://aka.ms/github_dpa**](https://aka.ms/github_dpa) will apply to your procurement of GitHub Consulting Services.

## 

|     |     |     |
|-----|-----|-----|
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |

## Responsible AI assumptions

<table>
<caption><p><span id="_Toc231555290" class="anchor"></span>Table 20: Responsible AI assumptions</p></caption>
<colgroup>
<col style="width: 27%" />
<col style="width: 72%" />
</colgroup>
<thead>
<tr>
<th> <strong>Assumption</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Responsible AI</strong></td>
<td><ul>
<li><p>The Customer acknowledges that this engagement includes the development or deployment of an AI system that:</p>
<ul>
<li><p>(1) is powered by AI and Customer is being exposed to and interacting with an AI system,</p></li>
<li><p>(2) the AI system output may contain sensitive content and/or factual inaccuracies,</p></li>
<li><p>(3) Customer is responsible for determining the accuracy of any content generated by this AI system in relation to Customer’s intended use as the user of this AI system, and</p></li>
<li><p>(4) this AI system does not provide opinions or advice. It is not designed to replace the role of qualified auditors or human reviewers. Customer is solely responsible for displaying and/or obtaining appropriate consents, warnings, disclaimers, and acknowledgements to end users of Customer’s implementation of the AI system.</p></li>
</ul></li>
<li><p>During the engagement under this SOW, if the requested business outcome includes Microsoft developing or deploying an AI System for or with Customer which may be considered a sensitive use, Microsoft will conduct an internal responsible AI review, to include assessment of and requirements for the potential sensitive use.</p></li>
<li><p>The outcome of Microsoft’s review will be comprehensively discussed with AGOC, ensuring a transparent understanding of the findings. Microsoft is dedicated to adhering to its RAI principles, and as such, will identify and implement any necessary changes. For more detailed information about Microsoft’s commitment to responsible AI, please refer to https://aka.ms/RAI .</p>
<p>Should the review uncover any discrepancies between the use-case and the RAI guidelines, Microsoft will engage with Customer to co-develop a robust mitigation plan in addressing and resolving potential risks, ensuring that the project is brought into alignment with the RAI standards. The process may lead to modifications of the current project or proposal of an alternative solution that comply with the RAI expectations.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Prototype use case overview

The following use cases are the initial focus and underlying details for the prototype.

### **Use Case** **1:** **Supplier Downtime and SLA Credit Automation**

This is an AI agent system that monitors supplier outage/downtime events, cross-references SLA contract terms, detects breaches, calculates owed credits, and generates dispute communications for human review and approval.

<table style="width:99%;">
<colgroup>
<col style="width: 97%" />
<col style="width: 1%" />
</colgroup>
<thead>
<tr>
<th colspan="2">Activities</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><ul>
<li><p>Define and confirm business and technical Prototype requirements including key stakeholders, processes, and technologies</p></li>
<li><p>Create SLA contract extraction and indexing pipeline (PDFs → AI Search)</p></li>
<li><p>Support outage event ingestion from Dynatrace/ServiceNow into Microsoft Fabric</p></li>
<li><p>Enable breach detection engine combining deterministic rules + AI judgment</p></li>
<li><p>Create SLA Violation Case generation with unique case ID, evidence links, and estimated credit</p></li>
<li><p>Enable a case review UI (split-pane: source evidence + case summary with severity/confidence)</p></li>
<li><p>Support human-in-the-loop validation (valid/invalid with justification capture for model tuning)</p></li>
<li><p>Enable basic case status tracking (Open → In Progress → Closed)</p></li>
</ul></td>
</tr>
<tr>
<td colspan="2"><strong>Assumptions</strong></td>
</tr>
<tr>
<td><ul>
<li><p>Prototype scope will provide minimum viable product to validate initial requirements, design, process, and core technology. Additional capability, scaling, logic and complexity can be addressed in future phase.</p></li>
<li><p>Data, tooling, and processes required for ingestion and evaluation will be provided with minimal data pipeline definition or augmentation.</p></li>
<li><p>System designed to support a maximum of 50 outage events per day requiring SLA evaluation</p></li>
<li><p>SLA contracts are stored as PDFs in SharePoint and contain structured penalty/uptime clauses</p></li>
<li><p>Historical outage data is available via Dynatrace or ServiceNow</p></li>
<li><p>SLA contracts are extracted via Document Intelligence + Claude and indexed into Azure AI Search for retrieval</p></li>
<li><p>SLA terms are locked to contract version at time of breach</p></li>
<li><p>Detection uses deterministic rules (thresholds, uptime %, duration) and AI judgment for ambiguity and correlation</p></li>
<li><p>Client provides SLA design logic and credit calculation methodology</p></li>
<li><p>Preferred integration with Real-time APIs (DynaTrace/ServiceNow)</p></li>
<li><p>Fallback to API, Batch polling or CSV if needed</p></li>
<li><p>Cases include Unique case IDs, Evidence links, Estimated credits</p></li>
<li><p>Human validation required for confirming breach validity</p></li>
<li><p>Prototype uses basic state tracking: Open → In Progress → Closed</p></li>
<li><p>Contract terms are extracted once during ingestion and queried during breach detection</p></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

### **Use Case** **2:** **Vendor Quote & Contract Document Management Analysis**

This is an AI-powered greenfield application. Vendor quotes and contracts (PDF/Word) are ingested from SharePoint, intelligently extracted using Document Intelligence + Claude AI, enriched with deterministic business rules (cost-center mapping, budget impact calculation), and presented in a review UI for human validation and approval.

<table style="width:97%;">
<colgroup>
<col style="width: 97%" />
</colgroup>
<thead>
<tr>
<th>Activities</th>
</tr>
</thead>
<tbody>
<tr>
<td><ul>
<li><p>Define and confirm business and technical prototype requirements including key stakeholders, processes, and technologies</p></li>
<li><p>Develop a web application (Azure Static Web Apps) with split-pane document review UI</p></li>
<li><p>Implement AI-powered field extraction with per-field confidence scores and source highlighting</p></li>
<li><p>Provide deterministic rules engine for accounting logic, cost-center mapping, and categorization</p></li>
<li><p>Enable inline field editing with approve/edit/reject actions and audit trail</p></li>
<li><p>Create AI-generated value summary narrative (risk/value/justification framing)</p></li>
<li><p>Enable a single-stage approval workflow with structured feedback capture (expandable to multi-stage workflow with approvals tagged to approver Entra IDs in a future phase)</p></li>
<li><p>Automate document ingestion from SharePoint (with manual upload fallback)</p></li>
<li><p>Enable look-up of approved records stored in Microsoft Fabric (One Lake) for downstream use</p></li>
<li><p>Integrate Entra ID authentication with role-based access control</p></li>
<li><p>Use/construct (a) CI/CD pipeline (GitHub Actions → auto-deploy)</p></li>
</ul></td>
</tr>
<tr>
<td><strong>Assumptions</strong></td>
</tr>
<tr>
<td><ul>
<li><p>Prototype scope will provide minimum functionality to validate initial requirements, design, process, and core technology. Additional capability, scaling, logic and complexity can be addressed in future phase.</p></li>
<li><p>Data, tooling, and processes required for ingestion and evaluation will be provided with minimal data pipeline definition or augmentation.</p></li>
<li><p>A representative volume of up to 500 total documents/month across use cases (shared assumption, but directly impacts UC1 extraction volume)</p></li>
<li><p>Documents are assumed to average 20 pages; actual document complexity and variation may impact extract performance</p></li>
<li><p>Document inputs are vendor quotes and contracts in PDF/Word format</p></li>
<li><p>Documents originate from SharePoint document libraries and Ariba data extract (CSV) instead of API integration</p></li>
<li><p>Documents are processed using Document Intelligence (layout extraction), Claude Sonnet 4.6 (semantic extraction)</p></li>
<li><p>Estimated token profile per document: ~20K input tokens, ~8K output tokens</p></li>
<li><p>Extraction accuracy depends on availability of real sample documents for prompt tuning and permissibility of using them the non-production environment where the use case will be developed – it is assumed we can use real documents / data in non-production, although redactions are acceptable</p></li>
<li><p>Cost-center mapping is initially deterministic (rule-based)</p></li>
<li><p>Client provides existing cost-center mapping logic and SME input for edge cases</p></li>
<li><p>~25+ internal users will access the review UI</p></li>
<li><p>Human-in-the-loop validation required for field edits and approval decisions</p></li>
<li><p>Prototype uses single-stage approval workflow.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Prototype prerequisites

<table>
<colgroup>
<col style="width: 5%" />
<col style="width: 27%" />
<col style="width: 66%" />
</colgroup>
<thead>
<tr>
<th>#</th>
<th>Prerequisite</th>
<th>Detail</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Azure Resource Group with Contributor access</td>
<td>Contributor-level access to a dedicated reac-production Resource Group with no pending approval gates, security reviews, or onboarding processes. If Terraform plan review is required, confirm same-day approval cadence.</td>
</tr>
<tr>
<td>2</td>
<td>Microsoft Fabric workspace (F8+ capacity, Admin access)</td>
<td>Capacity is active (not paused). If capacity needs to be purchased or allocated from existing entitlement, this is completed in Week 0.</td>
</tr>
<tr>
<td>3</td>
<td>Architecture sign-off</td>
<td>ARB approval of the proposed architecture before Week 1 begins. Subject to refinement through agile development supporting directional alignment, not a locked specification.</td>
</tr>
<tr>
<td>4</td>
<td>Written Architecture Review Board (ARB)/Change Advisory Board (CAB) exemption for non-production</td>
<td>Signed email or documented decision (not verbal) from an executive with authority over the ARB process, explicitly naming this engagement and its non-production scope as exempt from ARB, security review, and CAB gates.</td>
</tr>
<tr>
<td>5</td>
<td>Sample documents (minimum 10 per use case)</td>
<td>Representative of production format diversity. Cleared for non-production use (no data residency, classification, or legal holds). If redaction is required, completed by client before Week 1. Redaction may result in reduced accuracy.</td>
</tr>
<tr>
<td>6</td>
<td>Dynatrace and/or ServiceNow API credentials (UC2)</td>
<td>Confirmed read access with tested connectivity from Azure. Service account creation, security reviews, or firewall changes completed in Week 0. If blocked on Week 1 Day 1, UC2 proceeds with stubbed data only.</td>
</tr>
<tr>
<td>7</td>
<td>Azure Policy exceptions (if applicable)</td>
<td><p>No restrictive policies blocking deployment of Azure AI services or restricting regions where Foundry + Claude are available.</p>
<p>For the non-production build environment, public PaaS endpoints with Entra ID authentication and TLS encryption are acceptable. Private Endpoint configuration (VNET design, private DNS zones, subnet planning) can add 1–2 weeks and is deferred to production promotion - where it is expected and recommended. If Ford requires Private Endpoints even for non-production, this must be resolved in Week 0 with VNET specs provided by Ford Network Security.</p></td>
</tr>
<tr>
<td>8</td>
<td>GitHub Copilot licenses for delivery team</td>
<td>Business or Enterprise tier with access to Claude Opus 4.6 model (minimum). No throttling or rate caps. Policy allows Chat, Inline, and Agent modes with premium model selection. Team will strive to use more cost-effective models where viable.</td>
</tr>
<tr>
<td>9</td>
<td>Entra ID App Registration</td>
<td>Client Entra ID admin creates one app registration using specs provided by the delivery team (app name, type: SPA, single-tenant, User-Read delegated, ID tokens enabled). Client returns Application (client) ID and Tenant ID — these are Terraform input variables.</td>
</tr>
<tr>
<td>10</td>
<td>SharePoint site with document library access</td>
<td>Non-production SharePoint site where sample documents are stored. Delivery team’s managed identity or service account has read access to the document library.</td>
</tr>
<tr>
<td>11</td>
<td>GitHub repository with write access</td>
<td>Repository where the delivery team can push code with CI/CD pipelines (GitHub Actions). Branch protection rules defined. Write access to main and ability to create branches.</td>
</tr>
<tr>
<td>12</td>
<td>Network and firewall exceptions</td>
<td>Azure PaaS can reach: Microsoft Foundry endpoints, Azure AI Search, SharePoint Online APIs, and (UC2) Dynatrace/ServiceNow API endpoints. No VPN-only restrictions requiring Private Endpoint setup within the delivery window unless provided prior to Week 1.</td>
</tr>
<tr>
<td>13</td>
<td>Delivery team accounts and development environment</td>
<td>Entra ID accounts and virtual desktop or workstation access for delivery team members. Environment must permit installation of: Node.js 20+, Python 3.11+, Azure CLI, Git, VS Code + extensions, and outbound HTTPS to npm/PyPI/GitHub/Azure endpoints. Other potential dependencies will be reviewed by Ford upon request within 48 hours.</td>
</tr>
<tr>
<td>14</td>
<td>Ariba data extract (Use Case 1)</td>
<td>CSV or structured export of historical PO data (minimum 50 records) including: PO number, vendor, amount, cost center, approval status (redactions acceptable if required but may reduce accuracy)</td>
</tr>
<tr>
<td>15</td>
<td>SLA use case design document (Use Case 2)</td>
<td>Existing design documentation: current-state process flows, SLA contract structure, breach identification logic, credit calculation methodology, and any existing templates used for dispute claims.</td>
</tr>
<tr>
<td>16</td>
<td>Claude Sonnet 4.6 availability confirmed</td>
<td>Verified that Claude Sonnet 4.6 (via Microsoft Foundry) is accessible in the client’s Azure region before build begins.</td>
</tr>
<tr>
<td>17</td>
<td>SDLC security policies and dependency governance</td>
<td>Ford’s SCA policy, approved/restricted package registries (npm, PyPI allowlists/blocklists), CI/CD scanning tool requirements (e.g., Checkmarx, Snyk, Black Duck), and vulnerability severity thresholds for blocking deployment. If Ford-internal package mirrors or proxies must be used instead of public registries, provide configuration details.</td>
</tr>
<tr>
<td>18</td>
<td>Cost-center mapping logic (UC1)</td>
<td>Client provides current cost-center mapping rules (spreadsheet, decision tree, or documented logic), the number of active cost centers, and names the SME for edge cases. Rules engine implementation begins Week 2 — mapping logic must be documented by end of Week 1 at latest.</td>
</tr>
<tr>
<td>19</td>
<td>Application Ownership in CMDB</td>
<td>Ford will determine the app ownership details such as EAMS ID, Owners and provide necessary CMDB onboarding approvals timely.</td>
</tr>
</tbody>
</table>

### **Technical Scope**

The follow provides an initial direction for the tools and platforms required to enable the prototype use cases.

| Layer | Technology | Purpose |
|----|----|----|
| AI Reasoning | Claude Sonnet 4.6 (via Microsoft Foundry) | Document extraction, summarization, judgment, breach detection |
| Document AI | Azure Document Intelligence (Prebuilt Layout) | OCR, table detection, structural extraction from PDF/Word |
| Search & Retrieval | Azure AI Search (S1) | SLA clause retrieval, document chatbot (RAG pattern) |
| Data Platform | Microsoft Fabric (F8) | OneLake storage, data pipelines, eventstream ingestion |
| Workflow Engine | Azure Logic Apps Standard | Approval workflows, connector-based integrations, notifications |
| Frontend | React + Azure Static Web Apps | Document review UI, case management, human-in-the-loop validation |
| Identity & Access | Microsoft Entra ID | Authentication, role-based access control, conditional access |
| CI/CD | GitHub Actions | Automated build, test, and deployment on push |
| Monitoring | Application Insights | Logging, tracing, performance telemetry |

# Exhibits

## Organizational readiness 

The section below provides additional details regarding Microsoft’s Organizational readiness scope for this project.

<table style="width:99%;">
<caption><p><span id="_Toc231555291" class="anchor"></span>Table 21: Organizational readiness outcomes</p></caption>
<colgroup>
<col style="width: 49%" />
<col style="width: 49%" />
</colgroup>
<thead>
<tr>
<th colspan="2">Organizational Readiness</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><p><strong>Desired outcome(s)</strong></p>
<ul>
<li><p>Develop the ability to drive adoption and behavioral changes that can positively benefit the organization and measure the potential benefits of the Agentic AI solutions.</p></li>
</ul></td>
</tr>
<tr>
<td>Scope</td>
<td>Customer responsibilities, dependencies, and assumptions</td>
</tr>
<tr>
<td><ul>
<li><p>Align and refine the Organizational Readiness strategy specific to the uses case(s) from the Intake process. </p></li>
<li><p>Create an actionable change plan that drives adoption of the use case agent and change through behavioral insights and sponsorship to drive an enhanced employee experience</p></li>
<li><p>Create a Measurement Scorecard (qualitative and quantitative KPIs) to measure success specific to the use case and define measurement methods and frequency.</p></li>
</ul>
<p>Readiness Outcomes:</p>
<ul>
<li><p>Organizational readiness strategy</p></li>
<li><p>Change plan</p></li>
<li><p>KPI Measurements</p></li>
</ul></td>
<td><p>Customer Responsibilities</p>
<ul>
<li><p>Designate key stakeholders for Organization Change Management, Learning and Development teams</p></li>
<li><p>Participate in workshops and planning sessions</p></li>
<li><p>Provide existing documentation (e.g., AI use cases, policies, risk registers)</p></li>
<li><p>Align on business priorities, compliance obligations, and strategic objectives</p></li>
<li><p>Identify responsible AI risk scenarios relevant to the organization</p></li>
<li><p>Engage cross-functional teams as needed</p></li>
<li><p>Track and report on OKRs and KPIs using provided frameworks</p></li>
</ul>
<p>Dependencies</p>
<ul>
<li><p>Key stakeholders must be available for workshops, reviews, and alignment</p></li>
<li><p>Business objectives and AI use cases must be defined to inform requirements</p></li>
<li><p>Data governance, compliance, and responsible AI frameworks are in place or under development</p></li>
<li><p>Appropriate compliance, data, and legal teams engaged to support planning and alignment</p></li>
<li><p>Tools or platforms for tracking backlog, OKRs, and KPIs</p></li>
</ul>
<p>Assumptions</p>
<ul>
<li><p>Backlog, OKRs, and KPIs are managed using existing customer-owned tools and processes</p></li>
<li><p>This module provides program-level structure and planning, not hands-on implementation of security controls</p></li>
</ul></td>
</tr>
</tbody>
</table>

## AI security extension

The section below provides additional details regarding Microsoft’s security extension scope for this project.

<table style="width:99%;">
<caption><p><span id="_Toc231555292" class="anchor"></span>Table 22: AI security extension outcomes</p></caption>
<colgroup>
<col style="width: 49%" />
<col style="width: 49%" />
</colgroup>
<thead>
<tr>
<th colspan="2"><strong>AI Security</strong> <strong>Extension</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><p><strong>Desired outcome(s)</strong></p>
<ul>
<li><p>Continued alignment between AI security efforts and broader enterprise cybersecurity and governance programs</p></li>
<li><p>Remediation activities to support identified Ford data governance, privacy, and compliance frameworks</p></li>
<li></li>
<li><p>Responsible AI risks identified and mitigation activities integrated into the overall AI security approach</p></li>
</ul></td>
</tr>
<tr>
<td>Scope</td>
<td>Customer responsibilities, dependencies, and assumptions</td>
</tr>
<tr>
<td><ul>
<li><p>Alignment planning with broader cybersecurity and risk programs</p></li>
<li><p>Facilitation of workshops to define AI security program requirements</p></li>
<li><p>Documentation of data governance, privacy, and compliance dependencies</p></li>
<li><p>Identification of responsible AI risks and mitigation approaches</p></li>
<li><p>Security design, architecture and configuration support for the following Microsoft products:</p>
<ul>
<li><p>SharePoint Online</p></li>
<li><p>OneDrive</p></li>
<li><p>Teams</p></li>
<li><p>Microsoft Purview</p></li>
<li><p>M365 CoPIlot</p></li>
<li><p>Agent365</p></li>
<li><p>CoPilot Sudio</p></li>
<li><p>Microsoft Foundry</p></li>
</ul></li>
</ul></td>
<td><p>Customer Responsibilities</p>
<ul>
<li><p>Designate key stakeholders for governance and decision-making</p></li>
<li><p>Participate in workshops and planning sessions</p></li>
<li><p>Provide existing documentation (e.g., AI use cases, policies, risk registers)</p></li>
<li><p>Align on business priorities, compliance obligations, and strategic objectives</p></li>
<li><p>Identify responsible AI risk scenarios relevant to the organization</p></li>
<li><p>Engage cross-functional teams as needed</p></li>
<li><p>Track and report on OKRs and KPIs using provided frameworks</p></li>
<li><p>Implement security recommendations provided by Microsoft</p></li>
</ul>
<p>Dependencies</p>
<ul>
<li><p>Key stakeholders must be available for workshops, reviews, and governance alignment</p></li>
<li><p>Business objectives and AI use cases must be defined to inform requirements</p></li>
<li><p>Data governance, compliance, and responsible AI frameworks are in place or under development</p></li>
<li><p>Appropriate compliance, data, and legal teams engaged to support planning and alignment</p></li>
<li><p>Tools or platforms for tracking backlog, OKRs, and KPIs</p></li>
</ul>
<p>Assumptions</p>
<ul>
<li></li>
<li><p>Remediation timelines and risk decisioning are customer responsibilities</p></li>
<li><p>Not all Microsoft platforms may be remediated during the length of this engagement</p></li>
<li><p>Responsible AI planning focuses on risk identification and planning, not formal audits or legal review</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Agentic SOC

The section below provides additional details regarding Microsoft’s security operations centre scope for this project.

<table style="width:99%;">
<caption><p>Table 21: Agentic SOC</p></caption>
<colgroup>
<col style="width: 49%" />
<col style="width: 49%" />
</colgroup>
<thead>
<tr>
<th colspan="2"><strong>Agentic SOC</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><p><strong>Desired outcome(s)</strong></p>
<ul>
<li><p>Design and pilot an AI agent driven SOC capable of handling L1 operations autonomously, enabling Ford to operate with a small, elite in-house L3 team focused on proactive threat hunting and strategic security.</p></li>
<li><p>Deploy purpose-built AI agents for incident routing, triage, investigation, response, closure QA, and detection tuning. Establish agent infrastructure, governance, and safety controls including kill switches, shadow mode, and audit logging. </p></li>
</ul></td>
</tr>
<tr>
<td>Scope</td>
<td>Customer responsibilities, dependencies, and assumptions</td>
</tr>
<tr>
<td><ul>
<li><p>Pilot a portfolio of purpose-built AI agents, example agents include: </p>
<ul>
<li><p>SOCBot Incident Router (classification and routing)</p></li>
<li><p>Incident Closure Analyst (100% closure QA)</p></li>
<li><p>Detection Tuning Agent (continuous rule optimization)</p></li>
<li><p>Incident Analysis Agent (automated triage)</p></li>
<li><p>Resolution Concierge (bounded autonomous response)</p></li>
<li><p>IOC Actions Agent (IOC lifecycle management)</p></li>
<li><p>MITRE ATT&amp;CK Agent (real-time technique mapping)</p></li>
</ul></li>
<li><p>Establish agent infrastructure on Azure AI Foundry with managed identities, least privilege RBAC, Key Vault integration, and audit logging. </p></li>
</ul></td>
<td><p>Customer Responsibilities</p>
<ul>
<li><p>Designate key stakeholders for governance and decision-making</p></li>
<li><p>Participate in workshops and planning sessions</p></li>
<li><p>Provide existing documentation (e.g., AI use cases, policies, risk registers)</p></li>
<li><p>Align on business priorities, compliance obligations, and strategic objectives</p></li>
<li><p>Provide Google SecurityOps subject matter expertise</p></li>
</ul>
<p>Dependencies</p>
<ul>
<li><p>Key stakeholders must be available for workshops, reviews, and governance alignment</p></li>
<li><p>Business objectives and AI use cases must be defined to inform requirements</p></li>
<li><p>Appropriate compliance, data, and legal teams engaged to support planning and alignment</p></li>
<li><p>Tools or platforms for tracking backlog, OKRs, and KPIs</p></li>
</ul>
<p>Assumptions</p>
<ul>
<li><p>Agentic capabilities will be hosted in a Customer environment provided Azure Foundry instance.</p></li>
<li><p>Not all agents may be piloted during the length of this engagement</p></li>
<li><p>Not all agentic capabilities may integrate with Google SecOps; Sentinel may be a valid pilot target</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Department Agents

The diagram below illustrates a **Department Agent model** where AI agents are organized by departments, and understand the domain’s processes, policies, business systems, data, and personas.

<img src="media/image14.png" style="width:6.5in;height:3.65833in" />

<span id="_Toc231555297" class="anchor"></span>Figure 5: Department or business domain agents

## Solution Overview

The following solution overview diagram shows how a **Microsoft Copilot and Foundry** will act as the central hub of an enterprise AI solution. This solution establishes a secure enterprise AI platform that enables intelligent agents to work across people, processes, data, platform services, and business systems. The agents within this ecosystem will be capable of retrieving information, answering questions, automating tasks, coordinating activities, and supporting decision-making while connecting to existing enterprise systems and data sources. Built on a foundation of security, governance, and compliance, the solution provides a scalable and trusted framework that aims to improve productivity, accelerate business processes, reduce manual effort, and deliver measurable business value across the organization.

<img src="media/image16.png" style="width:6.5in;height:3.65833in" />

<span id="_Toc231555298" class="anchor"></span>Figure 6: Solution overview

## Agent capabilities

The image below highlights **eight** (8) core capabilities that define how agents operate, collaborate, and deliver business value. Together, they enable organizations to standardize intelligent automation, simplify integration, improve governance, and accelerate enterprise-wide adoption of AI-driven solutions.

<img src="media/image17.png" style="width:5.65131in;height:2.93071in" />

<span id="_Toc231555299" class="anchor"></span>Figure 7: Agent capabilities
