## Ford Motor Company – Agentic AI Transformation

### Opportunity Overview Information

> MSXID: 7-3FS2XQBWAO (CRM / MSX Opportunity ID) – CRM Account ID 11-22J0X; TPID 639534
>
> CompassOne: Ford Motor Company – ESWO deal; Deal Owner: Phelicia Lee; stage: Contracting; Target Approval Date 6/17/2026; reviews not required
>
> Deal value: $3,908,330.96 USD (~$3.91M; ESWO incl. travel) · sold margin 29.24% · 5.9-month (26-week) time-and-materials engagement, 2026-07-13 – 2027-01-08. Fabric in scope; production pilot.
>
> [CompassOne opportunity](https://compass.microsoft.com/opportunities/7-3FS2XQBWAO/639534)

## Project Overview:

> Microsoft partners with Ford to stand up a secure, enterprise-grade Agentic AI platform on Microsoft Copilot Studio and Azure AI Foundry (Microsoft Foundry). Delivery spans Microsoft AIBS (functional/architecture), IGD (offshore development/test/infra), Data and AI, EAG (AI Security Foundations + Agentic SOC), and ACM (adoption/change management) workstreams, with KPMG as the Microsoft partner delivering two non-production prototype use cases. SOW (Statement of Work) is a DRAFT / NOT BINDING (v4, June 03, 2026), pursuant to a Work Order (WO number TBD).

### Team Involved (ISD, EAG, etc.)

> Pursuit lead: Snehal R / snep
>
> Architect: Francis Moigula / Francis.Moigula
>
> EAG: Lorrin Ferdinand / lferdinand

## Pre-Conditions:

| Criteria | Met (Yes/No) |
|----|----|
| Fabric & Prod but under $10M | **Yes** – Fabric in scope; production pilot; deal value ~$3.91M is under the $10M threshold. |
| Fabric and $10M or above triggers the Fabric SCR | **No** – Deal value is below $10M. |

### Special Conditions Review Criteria

| **SCR Risk Type: Fabric** | **Review Comments** |
|----|----|
| What workloads does this opportunity cover? | A 26-week pilot building a reusable Agentic AI platform on Copilot Studio and Azure AI Foundry (Microsoft Foundry): up to 2 non-production prototype agents (KPMG-built), up to 2 department agents, and 1 production-pilot department agent (Engineering & Product Development) for <20 North American users. Microsoft Fabric (F8) provides OneLake storage, data pipelines, and eventstream ingestion under the solution, with Azure AI Search (RAG), Document Intelligence, Logic Apps, and a React/Static Web Apps human-in-the-loop UI. |
| What cloud integration efforts are required for this opportunity? | Integrations in scope: SAP Ariba, ServiceNow/Dynatrace (outage/SLA events), SharePoint (PDF document access), and Microsoft Fabric/OneLake. Assumed reachable via out-of-the-box Copilot / Power Automate connectors; otherwise sample files are used for demonstration/validation. Real-time Dynatrace/ServiceNow integration (UC1) depends on customer-provided API credentials (SOW prereq #6) and falls back to stubbed data if blocked at Week 1.<br><br>The actual prototype sources are limited to four named systems, all native or pre-mitigated: UC1 draws on SharePoint (SLA contract PDFs — native connector), Dynatrace and ServiceNow (outage events; native ServiceNow connector, Dynatrace via REST with stubbed-data fallback), landing in Microsoft Fabric/OneLake; UC2 draws on SharePoint (vendor quotes/contracts — native connector) and SAP Ariba (supplied as a CSV extract, explicitly in place of API integration), with approved-record lookup in OneLake.<br><br>None of the no-native-connector systems (Oracle HCM, Teamcenter, Nicus) appear in UC1/UC2 — those are evaluated/referenced only (NOT integrated): GCP, BigQuery, Teamcenter, Oracle HCM, Nicus, GitHub, Jira/Confluence/Atlassian. Connector-availability complexity is therefore a conditional, future-phase concern (if any referenced source is promoted in-scope it becomes a custom-integration workstream), not a current-scope risk.<br><br>The prototype validates agent behaviour against stubbed Dynatrace events and an SAP Ariba CSV extract rather than live integrations, so a future production phase must independently scope and estimate those data paths — particularly SAP Ariba, which has no native connector — and should not treat pilot success as evidence of production-integration feasibility or sizing; the deferred complexity (live REST auth, throttling/retry, schema-drift handling, event-volume/F8-capacity load) is bounded to that future phase, not eliminated. Fabric Eventstream connectors for Kafka/Service Bus and SQL-estate CDC reached GA in 2026 [1][5]. |
| Which ISVs are considered for this opportunity and why? | The only ISV/partner engaged on delivery is KPMG — the Microsoft partner subcontracted to build the two non-production prototype use cases (UC1 Supplier Downtime & SLA Credit Automation; UC2 Vendor Quote & Contract Document Management Analysis), ~2,088 hours / ~$442K of the deal, time-boxed to weeks 3–10. KPMG is the relevant entity here because it is the one carrying partner-delivery and scope-attribution exposure; that exposure is bounded by the non-production scope (sample/stubbed-data fallbacks, no production-hardening obligations). [4] |
| Are there any Non-GA product dependencies? | Core platform is GA: Microsoft Fabric (OneLake, Data Factory pipelines, Eventstream, F-SKU capacity) is generally available and Azure-SLA-covered [1][2]. No non-GA or preview-stage product dependencies remain in scope. |
| Any SLAs related to product systems implementation? | No Microsoft SLAs/OLAs are offered by this engagement. The SOW's Exclusions table expressly places "Guarantees and SLAs/OLAs" out of scope: no commitments on system performance, uptime, or service levels are provided or implied [4]. Underlying platform SLAs still apply at the product level — Microsoft Fabric is generally available, runs across Azure availability zones, and offers cross-region disaster recovery for OneLake data, covered by Azure's standard service-level terms [1][2]. No customer-side SLAs are in scope. |

### Review Summary

> Ford – Agentic AI Transformation is a ~$3.91M, 26-week (5.9-month) ESWO pilot with Fabric in scope and a production-pilot component, so it meets the Pre-Conditions for a Special Conditions Review while sitting below the $10M automatic-SCR threshold. Overall risk is moderate and typical for an early Agentic AI pilot. The platform rests on generally-available, Azure-SLA-covered foundations (Microsoft Fabric/OneLake, Azure AI Foundry, GPT-5 family), and the engagement deliberately limits exposure: prototypes are non-production with sample/stubbed-data fallbacks, the production deployment is capped at <20 pilot users, and SLAs/OLAs are expressly out of scope. The principal residual risk is a light confirmation that no production Fabric pipeline hardening is expected in the deployment phase — the Fabric-heavy use cases are non-production prototypes that fall inside the staffed build window, and the data-engineering work is owned by Microsoft IGD. This is not a blocker given the pilot scope, but warrants confirmation before build.
>
> **Key Points considered:**
>
> - The staffing plan was reviewed to confirm data-engineering resources are allocated in the numbers required to deliver the projected Fabric workloads and outcomes (Adequate: one dedicated offshore Data Engineer at 480 h covering build weeks 3–14; the Fabric-heavy use cases are non-production prototypes that fall inside that staffed window, the work is owned by Microsoft IGD, and adjacent Copilot/Foundry and Power Automate developers backstop connector work — only a light confirmation that no production Fabric pipeline hardening is expected in weeks 15–26 remains).
> - Pre-Conditions met: Fabric is in scope and this is a production pilot, with a deal value (~$3.91M) below the $10M automatic-SCR threshold.
> - Platform foundations are generally available and Azure-SLA-covered — Microsoft Fabric/OneLake, Azure AI Foundry (Microsoft Foundry), and the GPT-5 model family [1][2][3].
> - Risk exposure is deliberately bounded: non-production prototypes with sample/stubbed-data fallbacks, a <20-user production pilot, and SLAs/OLAs expressly excluded [4].
> - Authoritative-source check applied to product status — core platform components (Microsoft Fabric/OneLake, Azure AI Foundry, GPT-5 family) are generally available and Azure-SLA-covered [1][2][3]; no product-status items remain unverified.
>
> **Key Risk Factors:**
>
> - Since the use cases that will leverage Fabric are non-production prototypes, this Fabric SCR is not required.
> - Nonetheless, no Fabric-specific risks identified. Fabric (F8) is used only for non-production prototype workloads (UC1 Dynatrace/ServiceNow → OneLake ingestion; UC2 OneLake record lookup) on generally-available, Azure-SLA-covered components, with sample/stubbed-data fallbacks and no production Fabric pipeline in scope.

### References

> 1. What's new in Microsoft Fabric (GA features: OneLake, Eventstream connectors, Data Factory CDC) — https://learn.microsoft.com/en-us/fabric/fundamentals/whats-new (accessed 2026-06-06)
> 2. Reliability in Microsoft Fabric (availability zones; cross-region DR for OneLake) — https://learn.microsoft.com/en-us/azure/reliability/reliability-fabric (accessed 2026-06-06)
> 3. Foundry Models sold by Azure (Azure OpenAI GPT-5 family; Azure-billed, Azure-SLA-covered) — https://learn.microsoft.com/en-us/azure/ai-foundry/foundry-models/concepts/models-sold-directly-by-azure (accessed 2026-06-06)
> 4. Ford – Agentic AI Transformation SOW (DRAFT v4, 2026-06-03), Exclusions: Guarantees and SLAs/OLAs — wip/inputs/DRAFT_NOT BINDING_Statement of Work_Ford_Agentic Al Transformation_v4_June 03, 2026 - Copy.docx (accessed 2026-06-06)
> 5. Supported connectors in Microsoft Fabric Data Factory (Dataflow Gen2 / pipelines / Copy job — connector availability) — https://learn.microsoft.com/en-us/fabric/data-factory/connector-overview (accessed 2026-06-06)

---
*Revision `12` · generated `2026-06-06T00:00:00Z` · rendered `2026-06-06T16:33:27Z` from `wip/output/Ford-scr.data.yml`.*
