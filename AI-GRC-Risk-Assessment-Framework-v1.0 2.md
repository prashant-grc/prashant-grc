# AI-GRC Risk Assessment Framework

**Version:** 1.0 (initial public draft)  
**Author:** Prashant Upadhyay  
**Project:** CyberSecureHub / AI-GRC-Toolkit  
**Date:** 14 November 2026  
**Status:** Community review draft — not independently validated

## 1. Purpose and scope

This framework provides a repeatable, risk-based method for assessing AI-enabled applications, including internally developed models, third-party AI services, generative AI assistants, and AI-assisted decision-support systems. It is intended for security, risk, compliance, privacy, product and business stakeholders. It does not replace legal advice, formal impact assessments, penetration testing or an organisation's existing governance requirements.

**Assessment unit:** One AI use case, including its data flows, model/service, users, integrations and business decisions. Reassess after material changes and incidents.

## 2. Assessment record (copy for each AI use case)

| Field | Entry |
|---|---|
| Assessment ID / version | |
| AI use case and business purpose | |
| Business owner / technical owner | |
| Model or vendor and version | |
| Deployment environment and integrations | |
| Data types, sources, retention and transfers | |
| Affected people and decisions | |
| Human oversight / appeal or escalation route | |
| Applicable laws, contracts and internal policies | |
| Assessor and review date | |
| Next review / change triggers | |

## 3. Risk categories and assessment prompts

| ID | Risk category | Questions to investigate | Example controls |
|---|---|---|---|
| R1 | Data privacy and confidentiality | Are personal, sensitive or confidential records used, logged or sent to vendors? | Data minimisation, access controls, retention rules, privacy review |
| R2 | Security and adversarial misuse | Could prompt injection, model extraction, malicious inputs or compromised integrations cause harm? | Threat modelling, input boundaries, least privilege, security testing |
| R3 | Accuracy and reliability | Could false or fabricated outputs affect decisions or operations? | Ground-truth evaluation, thresholds, fallback, monitoring |
| R4 | Bias, fairness and human impact | Are error rates materially different across relevant groups or contexts? | Representative testing, fairness review, human challenge route |
| R5 | Explainability and accountability | Can users understand, contest and trace consequential outputs? | Decision records, model documentation, accountable owner |
| R6 | Legal, regulatory and contractual compliance | Are sector, privacy, IP and jurisdictional obligations identified? | Legal mapping, approval gates, supplier terms review |
| R7 | Third-party and supply-chain dependence | Can vendor changes, outages, subprocessors or licensing affect control? | Due diligence, change notifications, exit plan, resilience testing |
| R8 | Operational resilience and model drift | Could performance degrade or controls fail after release? | Monitoring, drift checks, incident response, rollback plan |

## 4. Scoring methodology

Assess each risk scenario separately, not only the category overall.

**Likelihood (L):** 1 Rare; 2 Unlikely; 3 Possible; 4 Likely; 5 Almost certain. Base the score on exposure, threat capability, controls, incident history and uncertainty.

**Impact (I):** 1 Negligible; 2 Minor; 3 Moderate; 4 Major; 5 Severe. Consider effects on people, legal duties, security, operations, reputation and finances. Record the most relevant credible impact, not an automatic worst case.

**Inherent score = L × I**, before proposed safeguards. **Residual score = reassessed L × I**, after implemented and verified safeguards. Do not reduce a score merely because a control is planned.

| Score | Band | Suggested handling |
|---|---|---|
| 1–4 | Low | Record and monitor |
| 5–9 | Moderate | Assign owner and treatment date |
| 10–16 | High | Escalate for management review; mitigate before consequential deployment unless formally authorised |
| 17–25 | Critical | Do not deploy or continue without senior risk decision and verified safeguards; suspend where necessary |

These bands are illustrative and should be calibrated to organisational risk appetite. A legal prohibition or unacceptable harm overrides any numeric score.

## 5. Risk register template

| Risk ID | Scenario / cause / consequence | Category | Existing controls and evidence | Inherent L | Inherent I | Inherent score | Treatment action and owner | Due date | Verified control evidence | Residual L | Residual I | Residual score | Decision / approver | Review date |
|---|---|---|---|---:|---:|---:|---|---|---|---:|---:|---:|---|---|
| AI-001 | | | | | | | | | | | | | | |

For each scenario, document uncertainty, assumptions and any affected stakeholders. The owner should explicitly accept, mitigate, avoid or transfer the residual risk under the organisation's policy.

## 6. Assessment workflow

1. **Register:** Identify use case, owner, vendor, affected people and intended decisions.
2. **Map:** Document data flows, permissions, model boundaries, integrations and dependencies.
3. **Identify:** Capture risk scenarios across R1–R8, including misuse and foreseeable failure.
4. **Score inherent risk:** Record evidence and rationale for likelihood and impact.
5. **Treat:** Specify preventive, detective and corrective controls with owners and deadlines.
6. **Validate:** Test controls and retain verifiable evidence before assigning residual scores.
7. **Decide:** Record approval, restrictions, escalation and accountable risk acceptance.
8. **Monitor:** Track incidents, drift, vendor changes, complaints and control effectiveness; reassess after material change.

## 7. Worked example — fictional fraud detection assistant

**Scenario:** A fictional payment provider uses an AI assistant to flag potentially fraudulent transactions for analyst review. It does not autonomously block accounts.

| Risk | Inherent L × I | Inherent band | Treatment | Residual L × I | Residual band |
|---|---|---|---|---|---|
| AI-001: False positives delay legitimate payments and unfairly burden customers | 4 × 4 = 16 | High | Human review before action, segmented performance tests, appeal route, monitoring of false positives | 2 × 3 = 6 | Moderate |
| AI-002: Sensitive transaction data exposed to an external model provider | 3 × 5 = 15 | High | Contract and data-flow review, minimise fields, encrypt transport, restrict access, verify retention | 2 × 4 = 8 | Moderate |
| AI-003: Model drift reduces fraud detection effectiveness | 4 × 4 = 16 | High | Drift thresholds, back-testing, alerting, rollback and scheduled retraining review | 2 × 4 = 8 | Moderate |

**Important:** These are hypothetical scores for teaching purposes, not evidence of a deployed system or validated effectiveness. Actual residual scores require evidence that safeguards work.

## 8. Minimum evidence checklist

- [ ] Approved business purpose and accountable owner
- [ ] System architecture and data-flow diagram
- [ ] Data inventory, privacy/legal review where applicable
- [ ] Model/vendor documentation and due diligence
- [ ] Threat model and security test results
- [ ] Accuracy, reliability and relevant fairness evaluations
- [ ] Human oversight, challenge and escalation process
- [ ] Risk register with control evidence and residual decisions
- [ ] Incident response, rollback and monitoring plan
- [ ] Approval record and next reassessment date

## 9. Governance and review cadence

**Before deployment:** Complete assessment, test high-impact controls, record accountable approval.  
**After deployment:** Review monitoring signals at an interval proportionate to risk.  
**Reassess promptly:** On model/vendor changes, new data sources, major incidents, changed laws, significant performance drift, or changes in decision autonomy.

## 10. References for further alignment

This independent framework can be mapped, with additional work, to:

- NIST AI Risk Management Framework (AI RMF 1.0): Govern, Map, Measure, Manage.
- ISO/IEC 42001: AI management systems.
- ISO/IEC 27001: Information security management systems.
- Relevant privacy and AI laws, sector requirements and contractual duties in the applicable jurisdiction.

Mentioning these standards does **not** mean this framework is certified, formally compliant or endorsed by their publishers.

## 11. Limitations and community feedback

This is a first-draft educational resource. Scoring thresholds and control examples are illustrative, and the framework has not been externally peer reviewed or independently tested. Organisations should adapt it to their own risk appetite, legal context and operational environment.

To suggest improvements, open an issue in the [AI-GRC-Toolkit repository](https://github.com/prashant-grc/AI-GRC-Toolkit). Do not post confidential information or personal data in public issues.

---

**Project website:** [CyberSecureHub](https://prashant-grc.github.io/CyberSecureHub/)  
**Repository:** [AI-GRC-Toolkit](https://github.com/prashant-grc/AI-GRC-Toolkit)
