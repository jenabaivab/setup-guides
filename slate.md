SonicWall Cloud Backup Breach: Firewall Configurations Compromised
October 2025 · Cyber Alert · Network Security


---

SonicWall has disclosed a data breach impacting its MySonicWall cloud backup service, exposing firewall configuration backups for all customers using the feature. The company confirmed the incident following an investigation with Mandiant and has published an official advisory urging immediate credential resets and configuration reviews.

While encrypted, the leaked backups contain sensitive details — including network topology, access rules, and service credentials — that could give threat actors valuable intelligence about affected environments. This incident highlights the potential downstream risk of third-party configuration storage and underscores the need for rapid remediation across all SonicWall-managed networks.


---

Vulnerability Details

The breach occurred after unauthorized access to SonicWall’s cloud backup environment, which stored configuration export files (EXP files) for customer firewalls. These files include device settings, VPN definitions, and encrypted credentials. SonicWall has since confirmed that 100% of cloud backup users were affected.

The encryption strength varies by device generation: Gen 7 and later models use AES-256 encryption, while Gen 6 and older models rely on 3DES, which may be more susceptible to brute-force recovery. Although there is no current evidence of exploitation, exposure of detailed configuration data provides attackers with a blueprint of network defenses that can be leveraged for targeted intrusions.


---

Recommended Actions

Immediately rotate all stored credentials, including administrator, VPN, RADIUS, LDAP, SNMP, and API keys.

Rebuild or sanitize configurations before reapplying them to production devices.

Restrict remote management access and enforce MFA for all administrative interfaces.

Monitor firewall and VPN logs for unauthorized access attempts or configuration changes.

Follow SonicWall’s official incident advisory for ongoing updates and guidance.

Engage cybersecurity advisors to validate remediation efforts and assess potential downstream risks.