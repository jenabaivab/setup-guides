**Our Inter-Dependencies Amplify Cyber Attacks**

Businesses now share infrastructure, data, and cloud platforms, meaning one breach can trigger ripple effects across entire ecosystems.

Outages in a single supplier or software provider can halt operations for hundreds of downstream organizations.

Cyber resilience now depends on ecosystem awareness, not just internal defenses.

In the 2025 “ToolShell” SharePoint campaign, over 400 organizations were compromised via identity/privilege abuses.

**SharePoint “ToolShell” Compromise**

A zero-day vulnerability in on-premises Microsoft SharePoint servers was exploited in July 2025, compromising the networks of organizations across industries, including the U.S. National Nuclear Security Administration (NNSA).

Attackers exploited the ToolShell vulnerability in a third‑party connector to Harvest cryptographic keys, which they used to access and exfiltrate SharePoint data.

Over 400 organizations were breached, exposing cryptographic tokens and enabling long-term persistence, even after patches. Approximately >1.2 million records were compromised as a part of the campaign.

**What Went wrong**

The attack relied on identity/crypto artifacts rather than just credentials.

Many organizations treated machine-level keys as low-risk and didn’t rotate them often.

Detection systems focused on credential usage, not on anomalous token/key behavior.

**Lessons Learned**

Rotate machine-level keys and tokens regularly as first-class security assets.

Micro-segmentation & zero-trust segmentation to limit damage from token-based escalation.

Implement just-in-time access and short-lived tokens to reduce exposure windows.

Apply continuous token use monitoring / anomaly detection.
