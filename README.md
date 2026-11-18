<div align="center">
  <img src="./assets/hero-banner.svg" width="100%" alt="Phan Phuc Dat — IT Business Analyst, Digital Transformation & FinTech" />
</div>

<br />

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-phucdatphan.github.io-0F172A?style=flat-square&logo=githubpages&logoColor=white)](https://phucdatphan.github.io)
[![UEH](https://img.shields.io/badge/UEH-B.Sc._Innovation_%26_Technology-005696?style=flat-square)](https://uii.ueh.edu.vn)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-phucdatphan-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/phucdatphan)
[![Email](https://img.shields.io/badge/Email-phucdat.work%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:phucdat.work@gmail.com)

</div>

---

## Executive Summary

I am an **Innovation and Technology** graduate from the **University of Economics Ho Chi Minh City (UEH)** specializing in **IT Business Analysis**, **Digital Transformation**, and **FinTech System Architecture**. Rather than treating business documentation and software engineering as isolated phases, my practice pairs **BABOK-aligned specifications (`BRD`, `SRS`, `User Stories`, `UAT`)** directly with working system prototypes and relational data diagnostics in **Node.js, Python, and SQL**.

Core methodology:
- **Specification-Driven System Design:** Translating complex business domains into unambiguous functional contracts, stakeholder matrices, state transition models, and testable Gherkin (`Given–When–Then`) acceptance criteria.
- **Payment & Distributed Reliability Invariants:** Designing FinTech checkout workflows around strict correctness guarantees—decoupled asynchronous `IPN` webhooks, canonical `HMAC-SHA256` signature verification, timing-safe validation, `Idempotency` anti-replay guards, and inventory reservation locks.
- **Closed-Loop Product & Settlement Analytics:** Applying SQL (`CTEs`, `Window Functions`) and Python pipelines to audit multi-party financial reconciliation flows, diagnose checkout conversion friction, and formulate payment anomaly rules.

---

## Case Study: End-to-End E-Wallet Payment Architecture

<div align="center">
  <img src="./assets/ewallet-metrics.svg" width="100%" alt="End-to-End E-Wallet Payment System Overview" />
</div>

<br />

| Stage | Repository | Focus Area | Architectural Scope & Deliverables |
| :--- | :--- | :--- | :--- |
| **Stage I** | [**`e-wallet-payment-simulator`**](https://github.com/phucdatphan/e-wallet-payment-simulator) | Core Payment Engine & Security Spec | Dual Merchant & Gateway Node.js sandbox, BABOK-aligned BRD/SRS, Order Lifecycle State Machine (`DRAFT → PENDING → SUCCESS / FAILED / EXPIRED`), canonical `HMAC-SHA256` verification, `Idempotency` protection, and inventory reservation holds. |
| **Stage II** | [**`e-wallet-checkout-ux-uat`**](https://github.com/phucdatphan/e-wallet-checkout-ux-uat) | Pre-Launch Checkout UX & UAT Suite | Interactive Figma checkout wireframes, Agile User Stories with Gherkin (`Given–When–Then`) Acceptance Criteria, active status-polling fallback design for network latency, end-to-end UAT test matrix, and automated Postman API collection. |
| **Stage III** | [**`e-wallet-post-launch-analytics`**](https://github.com/phucdatphan/e-wallet-post-launch-analytics) | Post-Launch Funnel, Settlement Recon & Fraud BI | Relational SQL (`CTEs`, `Window Functions`) & Python warehouse modeling checkout conversion funnels, multi-party bank settlement reconciliation (`AMOUNT_MISMATCH`, `MISSING_IPN`), and real-world card payment anomaly / anti-fraud rules. |

<details>
<summary><strong>Expand System Dataflow &amp; Closed-Loop Iteration (Mermaid Diagram)</strong></summary>
<br />

```mermaid
flowchart LR
    subgraph S1["Stage I: Architecture & Core"]
        M["Merchant Service<br/>Inventory Hold + Idempotency"] <-->|"Canonical HMAC-SHA256<br/>Async IPN Webhook"| G["Payment Gateway Core<br/>MoMo / ZaloPay Standard"]
    end
    subgraph S2["Stage II: UX & UAT"]
        UX["Figma Checkout Flows + Agile Stories"] --> UAT["End-to-End UAT Matrix & Postman<br/>Active Status Polling (/pay/query)"]
    end
    subgraph S3["Stage III: Settlement Recon & Fraud BI"]
        SQL["SQL CTEs & Window Functions<br/>Funnel & Multi-Party Reconciliation"] --> FRAUD["Real-World Anomaly EDA<br/>Card-Testing & Off-Peak Risk Rules"]
    end
    S1 --> S2 --> S3
    S3 -.->|"Deep-Link Checkout UX &<br/>Anti-Fraud Rule Backlog"| S1
```

</details>

---

## Technical & Business Analysis Stack

| Domain | Methods, Languages & Tooling |
| :--- | :--- |
| **BA & Product Modeling** | ![BABOK](https://img.shields.io/badge/BABOK-0F172A?style=flat-square) ![BRD/SRS](https://img.shields.io/badge/BRD_%2F_SRS-0F172A?style=flat-square) ![Gherkin](https://img.shields.io/badge/Gherkin_AC-00A818?style=flat-square&logo=cucumber&logoColor=white) ![Mermaid](https://img.shields.io/badge/Mermaid.js-FF3670?style=flat-square&logo=mermaid&logoColor=white) ![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white) ![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=white) ![Airtable](https://img.shields.io/badge/Airtable-18BFFF?style=flat-square&logo=airtable&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=white) |
| **Backend & Data Engineering** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![SQL](https://img.shields.io/badge/SQL_(CTE_%26_Window)-0284C7?style=flat-square&logo=postgresql&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white) |
| **API Verification & Dev** | ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white) ![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white) |
