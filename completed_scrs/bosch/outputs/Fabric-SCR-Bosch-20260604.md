## Robert Bosch GmbH – In-Car Voice Assistant

### Opportunity Overview Information

> MSXID: 7-3GPRF6IMBF (CRM / MSX Opportunity ID) – CRM Account ID 9-RR54L57OP; TPID 1059493; Work Order UCM0265-499493-645827
>
> CompassOne: Robert Bosch GmbH – ESWO deal; Deal Owner: Allyson Weede; stage: Contracting; Target Approval Date 6/3/2026; reviews not required
>
> Deal value: $3,558,882.92 USD (~$3.56M; signed ESWO Total Fees excl. tax) + ~$140K T&E reimbursable expenses · sold margin 29.54% · 6.10-month (26-week) engagement, 2026-07-06 – 2027-01-08. Fabric NOT in scope; no production pilot (development / CES demo).
>
> [CompassOne opportunity](https://compassone.microsoft.com/deal/499493/customer/645827/)

## Project Overview:

> Microsoft partners with Robert Bosch to build an In-Car Voice Assistant targeting the CES demo, spanning an online path on Azure AI Foundry (GPT-family LLM, Azure OpenAI Speech-to-Text and Text-to-Speech) and an offline (edge) path of custom SLM / STT / TTS / wake-word (VAD) models fine-tuned to run on an in-car AI Box (50–150+ TOPs). Delivery is organized into three ESWO service packages — Governance Team; In-Vehicle (Edge) Agentic Solution – AI SLM / Model Tuning; and Delivery Compliance, Privacy and Security — staffed across Microsoft ISD, GD Offshore, AI Landing Zone / Infra, RAI Security, and Secure-by-Default (SBD), with Bosch's own development and test team. The SOW (Statement of Work) is a DRAFT (v1, June 04, 2026), pursuant to signed Work Order UCM0265-499493-645827.

### Team Involved (ISD, EAG, etc.)

> Pursuit lead: Snehal R / snep
>
> Architect: TBD
>
> EAG: Lorrin Ferdinand / lferdinand

## Pre-Conditions:

| Criteria | Met (Yes/No) |
|----|----|
| Fabric & Prod but under $10M | **No** – Microsoft Fabric is NOT in scope for this engagement (not referenced in the SOW, ESWO, or technology requirements); this pre-condition does not apply. |
| Fabric and $10M or above triggers the Fabric SCR | **No** – Contracted ESWO value ~$3.56M (all source figures are below $10M) and Fabric is not in scope. |

### Special Conditions Review Criteria

| **SCR Risk Type: Fabric** | **Review Comments** |
|----|----|
| What workloads does this opportunity cover? | This is an Agile, 26-week engagement (ESWO contracted ~$3.56M + ~$140K T&E; staffing plan ~$6.5M) to build an In-Car Voice Assistant for Bosch targeting the CES demo. The solution spans an edge (offline) path — custom SLMs, STT, TTS, and wake-word/VAD models fine-tuned on a 50–150+ TOPs AI Box — and an online path via Azure AI Foundry (GPT-family LLM, Azure OpenAI STT/TTS). An edge-native arbitrator routes requests between offline and online agents. Supporting workloads include a Vehicle Manual RAG (local vector DB), user memory manager, STS emotion/tone, automated test framework, Azure Landing Zone, DevOps/MLOps CI-CD, RAI review, and Delivery Compliance/Privacy/Security (SBD). Microsoft Fabric is not referenced in the SOW or ESWO. [3][4] |
| What cloud integration efforts are required for this opportunity? | The online path uses Azure AI Foundry (GPT-family LLM, STT, TTS via Azure OpenAI API) and Azure subscription infrastructure (CAF Enterprise-Scale Landing Zone). No non-Azure cloud services are in scope. Third-party API integrations (e.g., mapping, POI, media) are a future-phase item — the SOW notes "3rd Party APIs need to be prepared by Bosch" and modifications to third-party systems are out of scope for Microsoft. The CES demo scope is agreed in Sprint 0; connector-level complexity is deferred to that sprint. Offline components (SLMs, STT, TTS, wake-word, vector DB) run entirely on the edge device with no cloud dependency, so there is no Fabric or data-pipeline connector risk. [3][4] |
| Which ISVs are considered for this opportunity and why? | No ISV/partner is named in the SOW or ESWO for delivery. Bosch has its own development and test team working alongside Microsoft. Third-party API providers (e.g., for mapping, media, calendar) are referenced as Bosch's responsibility ("3rd Party APIs need to be prepared by Bosch") and are out of scope for Microsoft integration during this SOW. [3][4] |
| Are there any Non-GA product dependencies? | The online path relies on Azure OpenAI models via Azure AI Foundry (Microsoft Foundry). The core GA models suitable for production use are gpt-4o (2024-11-20), gpt-4o-mini, the gpt-5 family (gpt-5, gpt-5-mini, gpt-5-nano), the GPT-4.1 series, and o-series (o3, o4-mini) — all GA, Azure-SLA-covered, billed through the Azure subscription; Azure OpenAI Whisper (STT) and gpt-4o-mini-tts (TTS) are GA [1]. Several newer/preview models exist (gpt-5-chat, gpt-chat-latest, gpt-5.3-chat, etc.) — Microsoft explicitly cautions against using preview models in production [1]. For the CES demo (non-production) any GA or preview model is acceptable; if the engagement progresses to production, pin to GA model versions only. The offline SLMs (wake-word, STT, TTS, SLM) are custom-trained edge models — not Azure-hosted services — so Azure product GA/preview classifications do not apply. No non-GA product dependencies are a current blocker; preview-model risk is confined to the online Azure AI path and bounded by the non-production CES demo scope. [1][2] |
| Any SLAs related to product systems implementation? | No Microsoft SLAs or OLAs are offered. The ESWO (WO UCM0265-499493-645827) is a fixed-fee, milestone-billed Work Order: "Any total fee stated is an estimate only," fees exclude Products/licenses, and Customer pays within 30 days of invoice. The SOW adds an Agile fixed-capacity / variable-scope model — the project is deemed complete when capacity is consumed or the WO term (7/6/2026–1/8/2027) expires. Termination for convenience requires 60 days' notice; a delay to the Consulting Commencement Date without ≥10 business days' notice can expose Customer to up to the full fee. No customer-side SLAs are in scope. Underlying Azure service-level terms apply to the Azure subscription at the product level only. [3][4] |

### Review Summary

> The Robert Bosch – In-Car Voice Assistant engagement (ESWO-contracted ~$3.56M + ~$140K T&E, 26 weeks, 2026-07-06 – 2027-01-08) does NOT meet the Pre-Conditions for a Fabric Special Conditions Review (SCR = Special Conditions Review): Microsoft Fabric is not referenced anywhere in the SOW, ESWO, technology requirements, or staffing plan. The platform is Azure AI Foundry (online LLM/agent path) plus custom edge SLMs running on an in-car AI Box. This Fabric SCR is therefore not required. For completeness: the contracted deal value (~$3.56M, and the alternate $3.82M CompassOne / $6.5M staffing-plan figures) is below the $10M automatic-SCR threshold, and the engagement is scoped as a development / CES demo project — no production pilot or production deployment is defined in the current DRAFT SOW v1. The signed ESWO is a fixed-fee, milestone-billed Work Order with no Microsoft SLAs/OLAs and a High Risk Use disclaimer that places automotive-safety responsibility on the Customer. The online Azure AI path uses GA Azure OpenAI models (gpt-4o, gpt-5 family, GPT-4.1, o-series, Whisper STT, gpt-4o-mini-tts) — all Azure-SLA-covered and billed through the Azure subscription [1][2]. No third-party ISVs are engaged for Microsoft delivery.
>
> **Key Points considered:**
>
> - The staffing plan was reviewed to confirm data-engineering resources are allocated in the numbers required to deliver the projected workloads and outcomes (N/A: Fabric is not in scope; the staffing plan has no Data-Engineering capacity bucket, and the AI bucket of 6,024 h is staffed with Data Scientists for ML model fine-tuning, not data-pipeline engineering).
> - Microsoft Fabric is NOT in scope — not referenced in the SOW, ESWO, technology requirements, or staffing plan. Pre-Conditions for a Fabric SCR are not met; this review is informational only.
> - Commercial value differs by source: signed ESWO ~$3.56M (+ ~$140K T&E, ~13,414 hr), CompassOne $3.82M, staffing plan $6.5M (25,594 hr). All are below the $10M automatic-SCR threshold; confirm which scope is authoritative as the staffing plan is ~2x the contracted ESWO.
> - The online Azure AI path (Azure AI Foundry, GPT-family LLM, Whisper STT, TTS) uses GA, Azure-SLA-covered models [1]. Preview-model risk is bounded by the non-production CES demo scope.
> - No Microsoft SLAs/OLAs are offered; the ESWO is a fixed-fee, milestone-billed Work Order excluding Products/licenses, and the SOW excludes performance/service-level commitments [3][4].
> - The ESWO includes a High Risk Use disclaimer and Customer indemnification — material for an in-vehicle (potentially safety-relevant) assistant; Bosch bears responsibility for safe deployment [4].
> - No third-party ISVs are engaged for Microsoft delivery; Bosch's own team works alongside Microsoft, and third-party API integrations are Bosch's responsibility and out of Microsoft scope.
>
> **Key Risk Factors:**
>
> - Fabric SCR not applicable — Fabric is not in scope. No Fabric-specific risks identified.
> - Automotive safety / High Risk Use: the ESWO disclaims High Risk Use and shifts safety responsibility plus indemnification to Bosch. An in-car voice assistant may operate in a safety-relevant context; ensure Bosch owns the safety design and that deliverables are not relied on for safety-critical functions [4].
> - Commercial scope ambiguity: the staffing plan (~$6.5M / 25,594 hr) is ~2x the contracted ESWO (~$3.56M / 13,414 hr). Confirm the authoritative scope/capacity so delivery expectations match the signed Work Order.
> - Edge SLM model quality risk: custom fine-tuned offline models (wake-word/VAD, STT, TTS, SLM) on the AI Box must meet the CES demo quality bar; AI Box hardware specs (TOPs) are to be confirmed in Sprint 0. Delivery risk, not a Fabric risk.
> - Scope variability: the SOW is DRAFT v1 (DRAFT NOT BINDING), an Agile fixed-capacity / variable-scope model; CES demo use cases and the final feature list are deferred to the Sprint 0 baseline. Not all objectives may be completed within contracted capacity.

### References

> 1. Foundry Models sold by Azure (Azure OpenAI GA model list, audio models, fine-tuning models) — https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/models-sold-directly-by-azure (accessed 2026-06-07)
> 2. Azure OpenAI in Microsoft Foundry — overview — https://learn.microsoft.com/en-us/azure/ai-services/openai/overview (accessed 2026-06-07)
> 3. Statement of Work — Robert Bosch LLC, In-Car Voice Assistant, v1, June 04 2026 (DRAFT NOT BINDING) — completed_scrs/bosch/inputs/Statement of Work_Robert Bosch LLC_In Car Voice Assistant_v1_June 04, 2026_DRAFT.docx (accessed 2026-06-07)
> 4. Enterprise Services Work Order — Robert Bosch LLC (Work Order UCM0265-499493-645827) — completed_scrs/bosch/inputs/Enterprise Services Work Order for Robert Bosch LLC.docx (accessed 2026-06-07)

---
*Revision `1` · generated `2026-06-07T17:30:00Z` · rendered `2026-06-08T00:00:00Z` from `completed_scrs/bosch/outputs/Bosch-scr.data.yml`.*
