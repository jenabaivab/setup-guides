Done. I’ve:

tightened the intro to better reflect the nature of the issue (no over-alarmism)

refined Incident Details with clear what was exposed vs not

slightly sharpened Guidance to focus on verification + governance (not technical remediation)


Here’s the updated, publish-ready version:


---

Companies House WebFiling Issue Exposes Company Data – Review Records and Confirm Accuracy

Companies House has identified and remediated a security issue within its WebFiling service that may have allowed users to access and modify company information belonging to other entities. The issue was introduced during a system update in October 2025 and remained active until March 2026, when it was discovered and resolved.

While there is currently no evidence of widespread abuse, the nature of the issue means that certain non-public company data may have been visible and, in some cases, records could have been altered without authorization. Given that Companies House serves as an official source of company records in the UK, organizations should take steps to verify the accuracy of their filings and assess any potential impact.

Incident Details

The issue affected the Companies House WebFiling platform, where a logic flaw allowed authenticated users to access records beyond their authorized scope. This could potentially enable:

• Viewing of non-public company information, including director dates of birth, residential addresses, and company email addresses
• Unauthorized updates to company filings, including director details and other statutory information

Companies House has clarified that the following data was not impacted:

• Passwords were not compromised
• Identity verification data (e.g., passport information) was not accessed
• Existing filed documents (such as accounts or confirmation statements) could not be altered

The issue was not accessible to the general public and required a logged-in user with an authorization code. Any potential access would have been limited to individual company records rather than large-scale data extraction.

Our Guidance

To confirm the integrity of company records and reduce potential risk, ACA recommends the following steps:

• Review company filings and records: Verify that all information held on Companies House is accurate and reflects your organization’s current structure.

• Check for unauthorized changes: Pay close attention to director details, registered addresses, and recent filings that may not have been initiated internally.

• Cross-check against internal records: Validate Companies House filings against internal documentation to ensure consistency and completeness.

• Prepare a response plan: Ensure there are clear procedures to investigate and correct unauthorized filings, including escalation to legal and compliance teams where required.

• Engage governance and compliance functions: Involve legal, compliance, and company secretarial teams to assess any regulatory or reporting implications.

• Monitor for updates: Stay alert for further communications or guidance from Companies House and relevant UK authorities.

Given that many FCA-regulated firms, as well as the FCA itself, rely on Companies House data, ensuring the accuracy and integrity of these records is particularly important from a compliance and reporting perspective.


---

ACA can support organizations in reviewing regulatory dependencies, validating company records, and strengthening governance processes to respond effectively to incidents impacting third-party data sources.


---

If you want a final polish, I’d only suggest trimming ~5% more for sharpness, but this is already very solid and in-family with your published alerts.