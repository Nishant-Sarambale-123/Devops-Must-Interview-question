### **Interview‑Style Answer: How do you triage vulnerabilities effectively?**

Effective vulnerability triage is about **prioritizing risk, not just severity**, so that the most critical issues are addressed first with minimal business impact.

I start by **categorizing vulnerabilities** using standard severity ratings such as CVSS, but I don’t rely on scores alone. I combine severity with **contextual risk factors**, including:

*   Whether the vulnerability is **exploitable**
*   If it affects **internet‑facing or production systems**
*   Whether the asset contains **sensitive or critical data**
*   Availability of **known exploits** or active attacks

Next, I assess the **business impact**—for example, vulnerabilities on core customer‑facing services or payment systems are prioritized over non‑critical internal tools. I also check **compensating controls**, such as WAFs, network segmentation, or runtime monitoring, which may lower immediate risk.

Based on this, I classify vulnerabilities into clear priority buckets like:

*   **Fix immediately** (critical, exploitable, high business impact)
*   **Fix in next release** (moderate impact, limited exposure)
*   **Accept or defer** (low risk, mitigated, or no known exploit)

Remediation work is then **tracked and validated**, ensuring patches are applied, dependencies are upgraded, or mitigations are in place. Finally, I continuously refine triage rules using threat intelligence, scanning trends, and post‑incident learnings.

### **One‑line interview summary**

> *I triage vulnerabilities by combining severity scores with exploitability, asset criticality, and business impact, ensuring high‑risk issues are fixed first while lower‑risk ones are managed pragmatically.*

If you’d like, I can also:

*   Tailor this answer for **DevSecOps or cloud environments**
*   Explain how triage works with **SAST, DAST, or container scans**
*   Give a **real production incident example**
