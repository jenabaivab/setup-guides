# Node2Shell Exploitation Prompts Urgent Patching of Node.js Systems

Organizations are urged to immediately address Node2Shell (CVE-2026-111497), a high-severity vulnerability affecting Node.js that could allow unauthenticated remote attackers to execute code on vulnerable systems. Security researchers have demonstrated remote code execution, and exploitation attempts have been observed in the wild. With public exploit code available, the risk of further exploitation is elevated, making prompt remediation a priority.

On October 27, 2026, the U.S. Cybersecurity and Infrastructure Security Agency (CISA) added the vulnerability to its Known Exploited Vulnerabilities (KEV) catalog and set a November 10 remediation deadline for U.S. federal civilian agencies. Although this deadline applies specifically to federal agencies, the confirmed exploitation activity warrants the same urgency across all organizations. Organizations should identify vulnerable systems and apply the available security updates without delay.

## Vulnerability Details

Node2Shell affects Brotli, a compression component used by Node.js and other software to process compressed data. The vulnerability can allow specially crafted data to exploit a flaw in the component, potentially enabling remote code execution, exposure of sensitive information, or service disruption. Applications may be vulnerable even if they do not directly use Brotli, as other application components can expose the same attack path.

The following Node.js release lines are affected:

- **Node.js 22.x:** Versions before 22.23.4
- **Node.js 24.x:** Versions before 24.22.1
- **Node.js 26.x:** Versions before 26.12.1

Unsupported Node.js versions, including 20.x and 25.x, are also affected and do not receive security fixes. Organizations running these versions should migrate to a supported release containing the patch. Other software incorporating the vulnerable Brotli component may also be affected, including Bun, .NET, Python Brotli packages, Envoy Proxy, and Istio. Organizations should consult the relevant vendor advisories to determine their exposure.

## Recommended Actions

ACA recommends that organizations take the following actions to address this vulnerability:

1. **Identify affected systems:** Review software inventories and dependency records to identify Node.js deployments across production servers, internet-facing applications, containers, cloud workloads, serverless environments, and development pipelines. Include applications that bundle their own runtimes or third-party components that incorporate Brotli.

2. **Apply security updates immediately:** Upgrade Node.js 22.x to version 22.23.4 or later, 24.x to 24.22.1 or later, and 26.x to 26.12.1 or later. Migrate unsupported versions to a supported release containing the fix. Apply the appropriate vendor updates to other affected products.

3. **Verify remediation:** Restart or redeploy affected applications and rebuild container images where necessary. Confirm that patched versions are running across all affected environments.

4. **Implement interim safeguards:** Where immediate patching is not possible, restrict access to vulnerable services and prevent the processing of untrusted compressed data where operationally feasible. These measures provide only partial protection and must not replace the security updates.

5. **Investigate potential exploitation:** Review application and network logs for suspicious requests, unexpected process execution, unusual outbound connections, and unexplained service crashes. Investigate suspected compromise and initiate incident response procedures as appropriate.

Given the availability of public exploit code and reports of exploitation attempts, organizations should prioritize remediation and verify that all affected systems have been addressed.

**References**

- [Node.js October 2026 Security Releases](https://nodejs.org/en/blog/vulnerability/october-2026-security-releases)
- [CISA Known Exploited Vulnerabilities Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
- [Akamai: Inside Node2Shell](https://www.akamai.com/blog/security-research/2026/oct/inside-node2shell-closer-look-cve-2026-111497)
- [Canadian Centre for Cyber Security Advisory](https://www.cyber.gc.ca/en/alerts-advisories/al26-027-critical-vulnerability-impacting-google-brotli-cve-2026-111497)
