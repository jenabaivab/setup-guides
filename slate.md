Microsoft Sharepoint Vulnerability Under Active Exploitation – Urgent Patching Required
Microsoft has released emergency security updates to address two serious vulnerabilities in its on-premises SharePoint Server platform. One of these vulnerabilities, a critical remote code execution flaw tracked as CVE-2025-53770, is already being exploited in the wild by attackers. Organizations using affected SharePoint versions are strongly advised to apply the relevant patches as soon as possible.
Microsoft has confirmed that attackers are actively using these flaws to breach systems. Reports indicate that more than 75 organizations across government, education, energy, and telecom sectors have already been targeted. These vulnerabilities do not affect SharePoint Online (Microsoft 365). The U.S. Cybersecurity and Infrastructure Security Agency (CISA) has issued a public alert in response to ongoing exploitation.

Vulnerability Details

Microsoft has identified two vulnerabilities impacting SharePoint Server:
•	CVE-2025-53770 (Severity Score: 9.8/10) is a critical flaw that could allow attackers to run unauthorized code on a vulnerable server. This could lead to full control of the system, data theft, or further compromise of other connected systems.

•	CVE-2025-53771 (Severity Score: 6.3/10) is a related vulnerability that helps attackers disguise their activity and bypass security controls.

The following versions of SharePoint Server are impacted by these vulnerabilities:
•	SharePoint Server 2016
•	SharePoint Server 2019
•	SharePoint Server Subscription Edition

Security updates are now available for Sharepoint Server 2019 and SharePoint Server Subscription Edition. Patches for SharePoint Server 2016 are still pending and will be released shortly. Organizations with internet-facing SharePoint servers that have not been patched are at especially high risk.

Our Guidance
To protect your environment and limit potential impact, ACA recommends the following steps:
•	Apply Microsoft’s July 2025 security updates immediately:

	For SharePoint Server 2019, apply KB5002754.
	For SharePoint Server Subscription Edition, apply KB5002768.
	For SharePoint Server 2016, monitor Microsoft’s Security Portal for the patch release.

•	If patching cannot be done right away, temporarily disconnect vulnerable SharePoint servers from the internet to prevent external attacks.

•	After patching, Microsoft recommends:

	Rotating ASP.NET machine keys (used to protect authentication and session data).
	Turning on AMSI (Antimalware Scan Interface) to help detect malicious code within SharePoint.
	Using endpoint protection tools (like Microsoft Defender for Endpoint) to monitor suspicious activity.

•	Ask your IT or security teams to review logs for unusual access or behavior. In known attacks, attackers have used specific techniques, such as sending requests to:

/_layouts/15/ToolPane.aspx?DisplayMode=Edit
