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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
