SonicWall Cloud Backup Breached: Firewall Configurations Compromised

SonicWall has disclosed a data breach impacting its MySonicWall cloud backup service, exposing firewall configuration backups for all customers using the feature. The company confirmed the incident following an investigation with Mandiant and has published an official advisory urging immediate credential resets and configuration reviews.

While encrypted, the leaked backups contain sensitive details, including network topology, access rules, and service credentials, that could give threat actors valuable intelligence about affected environments. This incident highlights the potential downstream risk of third-party configuration storage and underscores the need for rapid remediation across all SonicWall-managed networks.

Breach Details
The breach occurred after unauthorized access to SonicWall’s cloud backup environment, which stored configuration export files (EXP files) for customer firewalls. These files include device settings, VPN definitions, and encrypted credentials. SonicWall has since confirmed that 100% of cloud backup users were affected.
Newer devices (Gen 7+) encrypt backups with stronger encryption standards, while older devices (Gen 6 and earlier) use weaker encryption algorithms, which could be easier to crack. There’s no proof that the data has been abused yet, but the leaked configurations give attackers a clear map of defenses that could enable targeted breaches.

Our Guidance
To protect your environment and limit potential impact, ACA recommends the following steps:
•	Check for Impacted Devices via MySonicWall: Log into MySonicWall and navigate to 'Product Management → Issue List'. If any pending actions are shown, follow the Essential Credential Reset steps, prioritizing active, internet-facing firewalls.

•	Comprehensive Credential and Key Reset: Execute a full credential reset across all affected systems. This includes:

o	Updating passwords for all local users, including administrators.
o	Resetting temporary access codes (TOTP) for local users, requiring a re-bind of authenticator apps.
o	Changing passwords on all LDAP, RADIUS, or TACACS+ servers connected to the devices.
o	Updating the shared secret in all IPSec site-to-site and GroupVPN policies.
o	Changing the passwords for any L2TP/PPPoE/PPTP WAN interfaces.
o	Resetting the Cloud Secure Edge (CSE) API key and any other API keys.

•	Rebuild or Sanitize Configurations: Do not re-use existing configurations. Instead, rebuild or sanitize them thoroughly before re-applying to production devices to remove any malicious code or non-standard settings.

•	Restrict Remote Management and Enforce MFA: Limit remote management access (HTTP/S, SSH) from the WAN and enforce multi-factor authentication (MFA) for all administrative interfaces.

•	Monitor Firewall and VPN Logs: Actively monitor all firewall and VPN logs for unauthorized access attempts or suspicious configuration changes to detect and respond to any lingering threats.

•	Follow Official Guidance: Continue to adhere to SonicWall’s official incident advisory for ongoing updates and guidance throughout the remediation process.

here is the second example

Microsoft SharePoint Vulnerability Under Active Exploitation – Urgent Patching Required

Microsoft has released emergency security updates to address two serious vulnerabilities in its on-premises SharePoint Server platform, one of which is already under active exploitation. Not only do these vulnerabilities conceal attacker activities, they also bypass existing security controls. This can lead to full control of the system, data theft, or further compromise of connected systems.

Organizations using affected SharePoint versions are strongly advised to apply the relevant patches as soon as possible. 
Microsoft has confirmed that attackers are actively using these flaws to breach systems. Reports indicate that more than 75 organizations across government, education, energy, and telecom sectors have already been affected. The U.S. Cybersecurity and Infrastructure Security Agency (CISA) has issued a public alert in response to ongoing exploitation.

Vulnerability Details
Microsoft has identified two vulnerabilities impacting SharePoint Server:
•	CVE-2025-53770 (CVSS Score: 9.8/10) is a critical flaw that could allow attackers to run unauthorized code on a vulnerable server. 

•	CVE-2025-53771 (CVSS Score: 6.3/10) is a related vulnerability that helps attackers conceal their activity and bypass security controls.

The following versions of SharePoint Server are impacted by these vulnerabilities:
•	SharePoint Server 2016
•	SharePoint Server 2019
•	SharePoint Server Subscription Edition
These vulnerabilities do not affect SharePoint Online (Microsoft 365).
Security updates are now available for Sharepoint Server 2019 and SharePoint Server Subscription Edition. Patches for SharePoint Server 2016 are still pending and will be released shortly. Organizations with internet-facing SharePoint servers that have not been patched are at especially high risk.

Our Guidance
To protect your environment and limit potential impact, ACA recommends the following steps:
•	Apply Microsoft’s July 2025 security updates as soon as possible:

o	For SharePoint Server 2019, apply KB5002754.
o	For SharePoint Server Subscription Edition, apply KB5002768.
o	For SharePoint Server 2016, monitor Microsoft’s Security Portal for the patch release.

•	After patching, Microsoft recommends:

o	Rotating ASP.NET machine keys (used to protect authentication and session data).
o	Turning on AMSI (Antimalware Scan Interface) to help detect malicious code within SharePoint.
o	Using endpoint protection tools (like Microsoft Defender for Endpoint) to monitor suspicious activity.
o	Reviewing and updating the organization’s patch management policies to ensure timely application of future patches

•	If patching cannot be done right away, temporarily disconnect vulnerable SharePoint servers from the internet to prevent external attacks. Also, ask your IT or security teams to review logs for unusual access behavior which may indicate an attack has occurred.  
