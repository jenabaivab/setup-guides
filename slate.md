Perfect, this helps a lot. I’ve got the format clearly now. Below is a Fortinet alert drafted tightly in the same style, length, and tone as your SonicWall and SharePoint examples. No fluff, no overreach.


---

Fortinet FortiCloud SSO Vulnerability Under Active Exploitation – Immediate Patching Recommended

Fortinet has disclosed and patched a critical authentication bypass vulnerability affecting multiple Fortinet products when FortiCloud Single Sign-On (SSO) is enabled. Tracked as CVE-2026-24858, the issue is confirmed to be under active exploitation and could allow unauthorized administrative access to affected devices.

Fortinet has acknowledged real-world abuse of this flaw and confirmed that malicious FortiCloud accounts were used to target customer environments before being disabled. Given the central role Fortinet products play in network security, successful exploitation could lead to configuration tampering, credential exposure, and broader network compromise.

Vulnerability Details

CVE-2026-24858 is an authentication bypass vulnerability (CWE-288) related to FortiCloud SSO. An attacker with a FortiCloud account and a registered device could potentially bypass authentication controls and gain access to other Fortinet devices registered under different customer accounts, provided FortiCloud SSO is enabled.

The vulnerability impacts multiple Fortinet products, including:
• FortiOS
• FortiManager
• FortiAnalyzer
• FortiProxy

FortiCloud SSO is not enabled by default, but is commonly activated during device registration or centralized management workflows. The vulnerability has been added to CISA’s Known Exploited Vulnerabilities (KEV) catalog, highlighting the elevated risk.

Our Guidance

To reduce exposure and limit potential impact, ACA recommends the following actions:

• Apply Fortinet security patches immediately: Upgrade all affected Fortinet products to the latest fixed versions provided by Fortinet.

• Disable FortiCloud SSO if not required: Until patching is confirmed, ensure administrative login via FortiCloud SSO is disabled across all devices.

• Audit administrative access: Review device logs and configurations for signs of unauthorized access, including the creation of new or unexpected local administrator accounts.

• Rotate credentials: Reset administrative credentials and review authentication integrations (LDAP, RADIUS, TACACS+) if compromise is suspected.

• Restrict management access: Limit exposure of management interfaces to trusted networks only and enforce MFA for all administrative access paths.

• Monitor for suspicious activity: Closely monitor firewall and system logs for abnormal login attempts or configuration changes following patch deployment.


---

If you want, I can now:

shorten this further for a “flash alert”, or

align wording exactly with ACA house style (for example tone of “Our Guidance” intro).




Here’s the updated short, in-house style alert with CISA urgency and due date clearly reflected:


---

Fortinet FortiCloud SSO Vulnerability (CVE-2026-24858) Under Active Exploitation – Immediate Patching Required

Fortinet has disclosed a critical authentication bypass vulnerability (CVE-2026-24858) affecting multiple products when FortiCloud Single Sign-On (SSO) is enabled. This flaw is being actively exploited in the wild, and the U.S. Cybersecurity and Infrastructure Security Agency (CISA) has added it to its Known Exploited Vulnerabilities (KEV) catalog, directing federal agencies and organizations to remediate by January 30, 2026. 

Successful exploitation allows attackers with a FortiCloud account and a registered device to bypass authentication and gain unauthorized access to other devices using FortiCloud SSO. Real-world activity observed includes abuse of SSO to log in and create local administrative accounts on targeted systems. 

Vulnerability Details

CVE-2026-24858 is an Authentication Bypass Using an Alternate Path or Channel vulnerability (CWE-288) impacting Fortinet products when FortiCloud SSO is enabled, including: FortiOS, FortiManager, FortiAnalyzer, FortiProxy, and potentially FortiWeb/FortiSwitch Manager. FortiCloud SSO is not enabled by default but is commonly activated during device registration. 

Our Guidance

To protect your environment and mitigate risk, ACA recommends the following actions:

• Patch immediately: Apply the latest Fortinet firmware updates that include fixes for CVE-2026-24858.
• Disable FortiCloud SSO if not yet patched: Turn off “Allow administrative login using FortiCloud SSO” until devices are updated.
• Audit administrative access: Look for unexpected local admin accounts and remove them.
• Rotate credentials: Change administrative and integration credentials for affected systems.
• Restrict management access: Limit administrative interfaces to trusted management networks and enforce strong MFA.
• Monitor logs: Review authentication logs for anomalous access patterns or previously observed malicious SSO use.


---

If you want, I can also generate a very brief (one-paragraph) “flash alert” version for internal distribution or broadcast channels.