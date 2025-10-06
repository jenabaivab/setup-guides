1.	Opening & Objectives
•	Purpose and attendee takeaways (detect trends early, practical advice)
•	Brief agenda overview

2.	Combined Trends + Case Studies (each trend followed immediately by the mapped case)

Trend 1 - Ecosystem amplification (SaaS & shared tooling)
•	A single compromised SaaS app or MFT platform can cascade across many tenants, increasing systemic risk.
Case: Salesloft / Drift SaaS compromise
•	Timeline & impact: attacker compromises vendor/SaaS integration which cedes cross-tenant data access and pipeline corruption.
•	Detection/response timeline: Vendor notification often arrives too late, and missing tenant telemetry slows containment.
•	Communication/regulatory notes: coordinated vendor/tenant disclosures, regulatory breach reporting where PII exposed.

Trend 2 - Legitimate tool abuse via human targeting
•	Attackers favour social engineering to gain access to sanctioned export/admin tools, making activity appear legitimate.
Case: Allianz CRM export / Salesforce compromise
•	Timeline & impact: social-engineered admin access enables large-scale CRM exports.
•	Detection/response timeline: activity mimics admin behaviour leading to delayed anomaly detection.
•	Communication/regulatory notes: customer notification, contractual breach management, potential fines for insufficient controls.

Trend 3 - Identity & token compromise as primary vector
•	Stolen refresh/session tokens and abused IdP sessions bypass network controls and enable broad lateral access.
Case: NNSA / SharePoint tenant compromise
•	Timeline & impact: compromised tokens/SSO sessions used to access sensitive tenant SharePoint sites.
•	Detection/response timeline: session-based access evades network-based alarms; token revocation critical but slow.
•	Communication/regulatory notes: classified/data sensitivity escalates regulatory and inter-agency coordination needs.

Trend 4 - Extortion economics and targeted data exfiltration
•	Ransomware groups increasingly perform selective theft and leverage extortion, increasing pressure to respond quickly and privately.
Case: Marks & Spencer ransomware + operational disruptions
•	Timeline & impact: targeted exfiltration + encryption leads to operational outages and brand damage.
•	Detection/response timeline: extortion negotiations complicate technical recovery and legal response.
•	Communication/regulatory notes: customer/employee notices, possible regulatory reporting, insurer and legal coordination.

Trend 5 - Visibility & operational readiness gaps
•	Lack of tenant-level telemetry, export/detection alerts, and clear vendor revocation authority delays containment.
Case: TransUnion consumer data exposure
•	Timeline & impact: limited telemetry and slow vendor action amplify consumer data exposure.
•	Detection/response timeline: discovery delayed by insufficient export logs and alerting.
•	Communication/regulatory notes: mass-notification requirements, credit-reporting remediation, regulatory scrutiny.

3.	Predictions for 2026
   
•	Increased social engineering attacks: Adversaries will use deepfakes, spear-phishing, and voice coercion to exploit human trust as technical defences have improved over time (increasing number of security software have moved to behaviour-based detection from signature-based detection). Mitigate with targeted training, red-team exercises, and authenticated secondary verification for high-risk requests.

•	Escalation of ransomware-as-a-service with double/triple extortion: Operators will combine encryption, data exfiltration, and service disruption (DDoS/leak sites) while offering ready-to-use toolkits to inexperienced bad actors. Defend with fast detection, offline/immutable backups, and coordinated legal/insurer response.

•	Human oversight as a critical factor in LLM governance: Model alignment gaps and pipeline risks make human-in-the-loop review essential for high-risk outputs. Implement role-based review gates, log audits, and continuous monitoring.

5.	Live Q&A

6.	Closing
