# Week 9 Journal

## Task 1 : Completed knowledge test.
![Github](./images/week9-task1-knowledge-test)

## Task 2 : CIA Protections

### Asset 1: Customer information

- **Protection:** Confidentiality
- **Reason:** Customer information should only be accessible to authorised staff. Unauthorised access may lead to the leakage of private customer information. This will be embedded within business documents and files.

### Asset 2: Business documents and files

- **Protection:** Integrity
- **Reason:** Business files should not be changed or modified by unauthorised users. Miscalculations may lead to business issues.

### Asset 3: Business website

- **Protection:** Availability
- **Reason:** Customers should have access to the website to receive information about the business and services. When the website is not available, the customers can't access this information.

### Asset 4: OpenWRT router/firewall

- **Protection:** Integrity
- **Reason:** Unauthorised users should not alter the firewall rules and network settings as this will compromise the security of the network.

### Asset 5: Staff Windows workstations

- **Protection:** Availability
- **Reason:** Staff require access to computers to do their everyday work. Normal business operations could be disrupted if computers are not available.

### Asset 6: Network configuration

- **Protection:** Integrity
- **Reason:** Network settings and configurations must remain correct. If changes aren't authorised, they could let attackers in to the business network.

### Asset 7: Business website content

- **Protection:** Integrity
- **Reason:** The information on the internet should be correct. If an attacker alters the content, he might be able to give false information to customers.

### Asset 8: Network traffic

- **Protection:** Confidentiality
- **Reason:** If someone intercepts the traffic, it is not supposed to be readable by unauthorised users, which is why it is sensitive information.

## Task 3 : Threat Sources and Motivation

### Threat Source 1: Cybercriminals

- **Motivation:** Cybercriminals may want to steal business or customer information, obtain money, or gain unauthorised access to the business network.

### Threat Source 2: External attackers

- **Motivation:** External attackers may try to gain unauthorised access to the network or website by exploiting security weaknesses.

### Threat Source 3: Competitor company

- **Motivation:** A competitor may try to obtain confidential business information or customer information to gain an advantage over the business.

### Threat Source 4: Disgruntled employee

- **Motivation:** A dissatisfied employee may intentionally damage systems, change information, or access business data without permission.

### Threat Source 5: Former employee

- **Motivation:** A former employee may try to use old knowledge or access credentials to enter the business network or obtain confidential information.


## CVE 1 – Critical Severity

**CVE ID:** CVE-2026-4702

The JavaScript Engine component of Mozilla Firefox is vulnerable to miscompilation attack. Firefox 149 and Firefox ESR 140.9 have addressed the vulnerability.

**Date:** 24 March 2026

**CVSS Version 3 Score:** 9.8 (Critical)

**CIA Impact:** CIA = Confidentiality: High, Integrity: High, Availability: High. CVSS vector:CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H.

**CWE:** CWE-843 – Access of Resource Using Incompatible Type (Type Confusion).

**Company:** Mozilla Corporation

**Product:** Mozilla Firefox

**Firefox:** Web Browser for computers and other devices to view websites and web applications.

**Simple Explanation:** The vulnerability is related to the JavaScript engine used by Firefox. JavaScript code can be treated incorrectly if there is a problem with the JIT compiler. An attacker can exploit this issue by creating malicious content in the web and execute unwanted code.

**Detect and Mitigate:** Users are advised to install Firefox 149 or later, or Firefox ESR 140.9 or later. Main mitigation is ensuring that the browser is current as Mozilla patched the vulnerability in these versions.

## CVE 2 – High Severity

**CVE ID:** CVE-2026-34769

**CVE Description:** Electron versions before 38.8.6, 39.8.0, 40.7.0 and 41.0.0-beta.8 have an undocumented commandLineSwitches option that can allow arbitrary switches to be added to the renderer process command line. Applications when they create webPreferences with untrusted input.

**Date:** 4 April 2026

According to the NVD assessment, **CVSS Version 3 Score is 8.8 (High).** CVSS vector: CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H.

**CIA Impact:** Confidentiality – High, Integrity – High, Availability – High.

**CWE:** CWE-88 – Improper Neutralization of Argument Delimiters in a Command (Argument Injection). Another CWE listed by this NVD is CWE-912 – Hidden Functionality.

**Company:** Electron / OpenJS Foundation

**Product:** Electron

**Product Description:** Electron is the framework to create desktop applications with JavaScript, HTML and CSS cross-platform. It is a combination of Chromium and Node.js, allowing applications to run on Windows, macOS and Linux.

**Simple Explanation:** The vulnerability may occur when the Electron app uses a source of untrusted information to set its webPreferences. An attacker might be able to include unwanted command-line switches. Such switches may make security aspects like the renderer sandbox less resilient.

**Detection and Mitigation:** Upgrade Electron to version 38.8.6, 39.8.0, 40.7.0, 41.0.0-beta.8 or later. WebPreferences should also not be used directly by developers with untrusted input, and an allowlist of allowed options should be used.

## CVE 3 – Medium Severity

**CVE ID:** CVE-2026-12590

A vulnerable body-parser version can have a request body size check be skipped due to an invalid limit value. This can enable very large requests and may lead to too much memory and CPU usage, thus causing denial of service.

**Date:** 9 July 2026

**CVSS Version 3 Score:** 5.9 (Medium) (according to NVD). The CVSS score is CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N/A:H.

Confidentiality – None, Integrity – None, Availability – High (CIA Impact: Confidentiality is not at all important, Integrity is not at all important, and Availability is very important).

**CWE:** CWE-770 – Allocation of Resources Without Limits or Throttling.

**Company:** OpenJS Foundation

**Product:** body-parser

**body-parser:** body-parser is a node.js package that is widely used in web applications for parsing data in the body of HTTP requests.

**Simple Explanation:** The issue is if the application provides an invalid request-size limit to body-parser. The check is not performed correctly, it may be skipped. An attacker could then send enormous requests that would use up too much memory and CPU and thus make the application useless.

**Detection and Mitigation:** Ensure that body-parser is installed at version 1.20.6 or 2.3.0 or any higher. Another mitigation is to check the limit value before sending to body-parser.

## Summary

| CVE | Severity | CVSS Version 3 Score | CIA Impact |
|---|---|---|---|
| CVE-2026-4702 | Critical | 9.8 | Confidentiality: High, Integrity: High, Availability: High |
| CVE-2026-34769 | High | 8.8 | Confidentiality: High, Integrity: High, Availability: High |
| CVE-2026-12590 | Medium | 5.9 | Confidentiality: None, Integrity: None, Availability: High |

- The three CVEs show different types of security vulnerabilities. CVE-2026-4702 is an issue with the Firefox JavaScript engine that may enable an attacker to execute code. CVE-2026-34769 is an Electron application vulnerability based on the use of untrusted input with command-line arguments and switches. CVE-2026-12590 is for body-parser and it can cause a denial of service, due to unapproved massive requests. CVEs have varying impacts on the CIA triad and severities.

## Task 5 : Vulnerability Disclosures

- Vulnerability disclosure refers to the process of notifying the company or vendor of a security vulnerability in order to allow the company to investigate and fix the vulnerability.

- I believe that it may take a vendor a while before it is made public, as they have to understand the issue, write a patch, test it to ensure that it does not cause any other issues. They also might require time to communicate with their customers and to develop instructions for updating the impacted product.

- I'm of the opinion that the disclosure period should be long enough to allow the vendor to create and publish a patch, but not too long. This period should be approximately 90 days as this will allow the vendor time to investigate and fix the vulnerability and limit the delay.

- I believe it would be best for the security researcher to contact the vendor once again and warn them again before releasing the vulnerability, if the vendor does not fix or advertise the vulnerability within a reasonable time. Users can benefit from public disclosure to educate them of the risk, but it can also giving attackers ahead of users time to apply a security fix.

- Exploiting vulnerabilities responsibly and with coordination can be beneficial since it provides for the cooperation of both the researcher and the vendor. The researcher can give technical information about the vulnerability, and the vendor can come up with and test a solution. Once the open vulnerability is resolved, details of the vulnerability will be shared publicly and other affected users will be aware of the vulnerability and will update their systems as necessary.

- Bug bounty programs can also help incentivize responsible reporting of vulnerabilities by security researchers. They are a structured approach for researchers to report security issues and can offer rewards for legitimate discoveries.

- In general I believe there needs to be a balance between the obligations of the security researcher to alert the world and the vendor's need for some time to correct the issue. The primary objective should be to minimize the threat to users and ensure vulnerabilities aren't left unknown for an unnecessarily long time.
