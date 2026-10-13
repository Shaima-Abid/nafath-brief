Version: NAFATH-V4
Track: Networking

## Overview
A national service provider depends on software, artificial intelligence, mobile applications, internet routing, cybersecurity, and data to deliver reliable services. A weakness in any of these areas can affect the entire system. Exposed software secrets may allow unauthorized access, while manipulated AI training data can lead to incorrect decisions. Insecure mobile applications may expose sensitive information, and BGP route hijacking can redirect internet traffic to unintended destinations. Vulnerabilities in software libraries can also provide attackers with entry points into critical systems. A Software Bill of Materials (SBOM) helps identify software components and investigate known vulnerabilities. Together, these six fields support a layered security strategy. The provider should protect credentials, test systems against attacks, validate network routes, monitor software dependencies, and maintain security throughout development and operation. These measures help reduce risks and improve the reliability and trustworthiness of national digital services.
## Software

According to the Twelve-Factor App methodology, configuration should be stored in environment variables instead of being hardcoded in the source code. Secrets, such as passwords and API keys, must be protected from exposure. Keeping configuration separate from code improves security, allows settings to change without modifying the application, and makes deployment easier across different environments.

Resource: The Twelve-Factor App – III. Config - https://12factor.net/config

## AI

The main categories of adversarial attacks on machine learning systems include evasion, data poisoning, and privacy attacks. Evasion attacks manipulate inputs during model use to cause incorrect predictions. Poisoning attacks compromise training data or the learning process to influence model behaviour. Privacy attacks aim to reveal sensitive information about training data or a model. These attacks occur at different stages of the machine learning lifecycle and require different mitigation strategies.

Resource: NIST AI 100-2 E2025 — Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations — https://csrc.nist.gov/pubs/ai/100/2/e2025/final

## Mobile

The OWASP Mobile Application Security Verification Standard (MASVS) is a security standard that helps developers protect mobile apps on Android and iOS. It covers areas such as data storage, encryption, authentication, and network security. Developers and security testers use MASVS to check whether an app meets security requirements, identify weaknesses through testing, and improve its protection against potential attacks.

Resource: OWASP - Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/

## Networking

BGP route hijacking occurs when a network announces incorrect or unauthorized routes, potentially directing internet traffic through an unintended network. Resource Public Key Infrastructure (RPKI) helps reduce this risk by allowing operators to verify whether an autonomous system is authorized to announce an IP prefix using Route Origin Authorizations (ROAs). However, RPKI origin validation does not verify every network along the route or prevent all interception attacks. Additional routing security measures are still necessary.

Resource: RFC 6811 - BGP Prefix Origin Validation - https://www.rfc-editor.org/info/rfc6811/

## Cybersecurity

Log4Shell (CVE-2021-44228) was a critical remote code execution vulnerability in Apache Log4j 2, a widely used Java logging library. Attackers could exploit vulnerable configurations by sending crafted input that triggered JNDI lookups, potentially allowing arbitrary code execution. The vulnerability affected specific Log4j versions and received a maximum CVSS 3.x severity score of 10.0. Organisations should identify affected applications and upgrade to an appropriate fixed version.

Resource: NIST National Vulnerability Database — CVE-2021-44228 — https://nvd.nist.gov/vuln/detail/CVE-2021-44228

## Data

A Software Bill of Materials (SBOM) is a formal inventory detailing components, libraries, and supply chain relationships used in building software. According to NTIA guidelines, its minimum data fields must contain: Supplier Name, Component Name, Version, Other Unique Identifiers (such as CPE or PURL), Dependency Relationship, Author of SBOM Data, and Timestamp. These elements enable organizations to track components, manage licenses, and quickly identify and mitigate vulnerabilities across the software supply chain. 

Resource: The Minimum Elements For a Software Bill of Materials (SBOM) - 
https://www.ntia.gov/sites/default/files/publications/sbom_minimum_elements_report_0.pdf

## Misconception in My Track
A common misconception in networking is that RPKI makes BGP completely secure. However, this is not true. RPKI helps verify whether a network is authorized to announce a specific IP prefix, but it does not check the entire path that internet traffic follows. Therefore, some routing attacks can still occur even when RPKI is used. Network operators need additional security measures, such as route filtering and network monitoring, to reduce these risks. RFC 6811 explains the limitations of BGP prefix origin validation in its Security Considerations section.

Resource: RFC 6811 - BGP Prefix Origin Validation - https://www.rfc-editor.org/info/rfc6811/

## Open Question
How can a national service provider combine RPKI validation, continuous route monitoring, and incident response to detect and limit the impact of a BGP hijacking event?
