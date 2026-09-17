# Cyber Threat Intelligence for Android Mobile Application Security

## 1. Introduction

### 1.1. Topic

Cyber Threat Intelligence (CTI) for identifying and analyzing security threats in Android mobile applications

Android applications are widely used for communication, banking, entertainment, education and business. Because mobile applications often process personal information, authentication data, financial information and device data, they can become targets for cybercriminals.

The purpose of this work is to demonstrate how Cyber Threat Intelligence methods can be applied to identify, collect, process and analyze information about potential threats to Android applications.

The main objectives are:

* to study the basic concepts of Cyber Threat Intelligence;
* to classify threats affecting Android applications;
* to collect open-source intelligence about mobile application threats;
* to organize collected information using a data source mapping;
* to enrich and correlate indicators of compromise (IOCs);
* to demonstrate the use of MISP for storing and analyzing threat intelligence;
* to apply filtering and normalization techniques to collected data.

---

# 2. Cyber Threat Intelligence Fundamentals

## 2.1. CTI concepts

Cyber Threat Intelligence is information about cyber threats that has been collected, processed and analyzed to help organizations understand potential attacks and make security decisions.

For Android applications, CTI can provide information about:

* malicious Android applications;
* malware families;
* malicious domains and IP addresses;
* phishing websites;
* compromised accounts;
* malicious APK files;
* command-and-control infrastructure;
* vulnerabilities;
* attack techniques used by threat actors.

CTI can be divided into several levels.

Strategic intelligence provides a high-level understanding of trends and risks. For example, an organization may analyze the growth of Android banking malware.

Tactical intelligence describes techniques and tactics used by attackers. MITRE ATT&CK can be used to classify these techniques.

Operational intelligence focuses on specific campaigns, threat actors and infrastructure.

Technical intelligence contains concrete technical indicators such as IP addresses, domains, URLs, file hashes and malware signatures.

---

## 2.2. CTI Glossary

| Term | Definition |
| ------------------- | -------------------------------------------------------------------------------------------------------- |
| CTI | Cyber Threat Intelligence — information about cyber threats that has been collected and analyzed. |
| IOC | Indicator of Compromise — evidence that may indicate malicious activity. |
| IOA | Indicator of Attack — evidence of an attack technique or malicious behavior. |
| TTP | Tactics, Techniques and Procedures used by attackers. |
| Threat Actor | Person or group responsible for malicious cyber activity. |
| APT | Advanced Persistent Threat — a sophisticated and persistent cyber threat. |
| Malware | Malicious software designed to damage systems, steal information or perform unauthorized actions. |
| Android Malware | Malware specifically designed to operate on Android devices. |
| APK | Android application package used to distribute Android applications. |
| Phishing | A technique used to trick users into providing sensitive information. |
| C2/C&C | Command and Control infrastructure used by malware or attackers to communicate with compromised systems. |
| Threat Hunting | Proactive search for suspicious activity inside an environment. |
| Enrichment | Adding additional information to an existing threat indicator. |
| Correlation | Connecting related pieces of information to identify relationships or patterns. |
| OSINT | Open Source Intelligence collected from publicly available sources. |
| MISP | Malware Information Sharing Platform used for storing and sharing threat intelligence. |
| STIX | Structured Threat Information Expression, a standardized format for representing CTI. |
| TLP | Traffic Light Protocol used to define how information can be shared. |
| False Positive | A legitimate event incorrectly identified as malicious. |
| Confidence | An assessment of how reliable or trustworthy an intelligence result is. |

---

# 3. Classification of Threats Against Android Applications

Android applications can be affected by different categories of cyber threats.

| Threat | Description | Possible Intelligence Sources |
| ----------------------------------- | ----------------------------------------------------------------------------- | -------------------------------------- |
| Malicious APKs | Applications containing malware or unauthorized functionality | VirusTotal, malware databases |
| Banking malware | Malware designed to steal banking credentials or financial information | VirusTotal, security reports |
| Spyware | Software that secretly collects information from a device | VirusTotal, threat reports |
| Phishing applications | Fake applications designed to steal credentials | OSINT, VirusTotal |
| Credential theft | Theft of usernames, passwords or authentication tokens | Threat reports, leaked-data monitoring |
| Malicious domains | Domains used for phishing or malware distribution | VirusTotal, Shodan, OSINT |
| C2 infrastructure | Servers used by malware for communication | VirusTotal, threat intelligence feeds |
| Exploitation of vulnerabilities | Exploitation of weaknesses in applications or Android components | MITRE, CVE databases |
| Supply-chain attacks | Compromise of third-party libraries or development components | Security reports, CVE databases |
| Adware | Applications that display unwanted advertising or perform suspicious tracking | VirusTotal, mobile security reports |

One important characteristic of Android threats is that attackers can combine several techniques. For example, a malicious APK may be distributed through a phishing website and communicate with a remote C2 server after installation.

---

# 4. Recommended CTI Sources

The following resources can be used for studying Android-related cyber threats:

### Recorded Future — The Threat Intelligence Handbook

The Threat Intelligence Handbook provides an introduction to CTI concepts, intelligence processes and the use of threat intelligence in cybersecurity.

### SANS CTI Resources

SANS materials provide information about threat intelligence collection, analysis, threat hunting and intelligence programs.

### MITRE ATT&CK
MITRE ATT&CK provides a knowledge base of attacker tactics and techniques. It can be used to describe how a particular Android threat operates.

### ENISA Threat Landscape

ENISA threat landscape reports provide information about current cybersecurity threats and trends.

### OSINT Framework

OSINT Framework provides a structured collection of publicly available intelligence sources.

### Michael Bazzell — Open Source Intelligence Techniques

This resource describes methods for collecting and analyzing publicly available information.

### MISP Training Documentation

MISP documentation provides information about collecting, storing, correlating and sharing threat intelligence and IOCs.

---

# 5. Data Collection Process

## 5.1. Open Source and Closed Source Intelligence

Threat intelligence can be obtained from open and closed sources.

Open-source intelligence (OSINT) is information that is publicly available. Examples include:

* public websites;
* security blogs;
* public malware databases;
* VirusTotal;
* Shodan;
* public CVE databases;
* GitHub repositories;
* security reports;
* public threat intelligence feeds.

Closed-source intelligence is information available only to authorized organizations or users. Examples include:

* internal SIEM logs;
* EDR telemetry;
* private threat intelligence feeds;
* incident response reports;
* information from security vendors;
* internal firewall and DNS logs.

For this project, OSINT is primarily used because it allows threat intelligence to be collected without accessing private systems.

---

# 6. OSINT Data Collection

## 6.1. VirusTotal

VirusTotal can be used to investigate files, URLs, domains and IP addresses.

For Android security research, it can be used to analyze suspicious APK files or indicators associated with Android malware.

For example, an analyst can investigate:

* SHA-256 hash of an APK;
* suspicious URL;
* suspicious domain;
* IP address;
* malware detection results.

A typical workflow is:

Indicator → VirusTotal search → Detection information → Related indicators → Enrichment

For example, if a suspicious APK hash is found, VirusTotal may provide information about security-engine detection results and relationships with other indicators.

The results should not be interpreted as absolute proof of malicious activity. A detection may sometimes represent a false positive, so additional sources should be used.

---

## 6.2. Shodan

Shodan is a search engine for internet-connected devices and services.

Within an authorized CTI investigation, Shodan can be used to study publicly exposed infrastructure associated with known indicators.

For example, an analyst may investigate an IP address obtained from a public threat intelligence report and examine:

* open ports;
* detected services;
* service banners;
* software information;
* certificates;
* geographic information.

For this academic project, Shodan should be used only for passive intelligence gathering and authorized targets.

The purpose is not to attack or exploit the discovered systems.

---

## 6.3. Maltego

Maltego is an OSINT and link-analysis platform.

It can help visualize relationships between:

* domains;
* IP addresses;
* websites;
* organizations;
* certificates;
* email addresses;
* infrastructure.

For Android threat intelligence, Maltego can be used to visualize relationships between a malicious domain, its IP address and other associated infrastructure.

Example:

Malicious APK → URL → Domain → IP address → Hosting infrastructure

This makes it easier for an analyst to understand the structure of a potential threat.

---

# 7. Data Source Mapping

The collected intelligence can be organized using a data source mapping.

| Source | Data Type | Purpose | Example |
| ------------------- | --------------------------------- | ------------------------------- | ------------------------------- |
| VirusTotal | Files, hashes, URLs, domains, IPs | Malware and IOC investigation | APK SHA-256 |
| Shodan | IPs, ports, services | Infrastructure intelligence | Server IP |
| Maltego | Relationships | Link analysis | Domain → IP |
| MITRE ATT&CK | TTPs | Attack technique classification | Credential Theft |
| ENISA | Threat trends | Strategic intelligence | Mobile malware trends |
| OSINT Framework | Public sources | Source discovery | Security databases |
| SIEM/EDR | Internal telemetry | Detection and investigation | Suspicious application activity |
| MISP | IOCs and relationships | CTI storage and sharing | IP/domain/hash |

The different sources complement each other.

For example, VirusTotal may identify a suspicious APK, while Maltego can help visualize infrastructure associated with the APK and MITRE ATT&CK can be used to classify the observed attacker behavior.

---

# 8. Data Processing and Exploitation

Raw intelligence is often not sufficient for analysis. Data should first be processed, normalized and enriched.

## 8.1. Data Enrichment

Data enrichment means adding additional information to an existing IOC.

For example, suppose the analyst has the following indicator:

IP address: 203.0.113.50

Additional information may include:

* type: IPv4;
* source: public threat report;
* first-seen date;
* last-seen date;
* associated domain;
* associated malware family;
* confidence level;
* threat category.

This creates a more useful intelligence record.

---

## 8.2. Correlation

Correlation means finding relationships between different indicators.

For example:

Android APK → SHA-256 hash → malicious URL → domain → IP address

If several independent sources connect the same domain with malware-related activity, the confidence in the indicator can increase.

However, correlation does not automatically mean that one indicator caused another event. The analyst must consider the source reliability and context.

---

# 9. MISP Deployment and IOC Import

MISP (Malware Information Sharing Platform) can be used as a central platform for storing and analyzing threat intelligence.

For this project, MISP can be deployed in a controlled laboratory environment.

The general deployment process is:

1. Prepare a Linux virtual machine.
2. Install the required dependencies.
3. Install MISP.
4. Configure the MISP instance.
5. Open the MISP web interface.
6. Create an organization or laboratory account.
7. Create an event related to Android application threats.
8. Add indicators of compromise.
9. Assign appropriate IOC types and categories.
10. Add tags and descriptions.
11. Correlate the indicators with existing information.
12. Export or share the intelligence when required.

---

# 10. Example IOC Dataset

For demonstration purposes, the following indicators can be used as synthetic laboratory data rather than real malicious infrastructure.

| IOC | Type | Description | Source |
| ------------------------------------------------------------------ | ------- | ---------------------------------- | ----------- |
| 192.0.2.10 | IPv4 | Synthetic suspicious C2 server | Lab dataset |
| example-threat.test | Domain | Synthetic malicious domain | Lab dataset |
| https://example-threat.test/sample | URL | Synthetic malware-distribution URL | Lab dataset |
| 0000000000000000000000000000000000000000000000000000000000000000 | SHA-256 | Synthetic APK hash | Lab dataset |

The 192.0.2.0/24 network and the example domains are reserved for documentation and examples, so they are suitable for demonstrating the workflow without targeting real infrastructure.

---

# 11. Filtering and Normalization

Before importing information into MISP or another CTI platform, the data should be normalized.

### IP addresses

All IPv4 addresses should use a consistent format:

192.0.2.10

### Domains

Domains should be converted to lowercase:

Example-Threat.Test

becomes:

example-threat.test

### URLs

URLs should use a consistent structure and unnecessary parameters should be removed when they are irrelevant to the investigation.

### Hashes

Hashes should be stored in a standardized hexadecimal format.

For example:

0000000000000000000000000000000000000000000000000000000000000000

### Timestamps

Dates should use a consistent format such as:

2026-09-17T12:00:00Z

### Duplicate removal

If the same IOC is collected from several sources, duplicates should be removed or merged while preserving the list of sources.

---

# 12. Example of a Normalized CTI Record

After processing, an indicator can be represented as:

| Field | Value |
| -------------- | ------------------------------------------------- |
| IOC | example-threat.test |
| Type | Domain |
| Category | Network activity |
| Source | OSINT |
| Related Threat | Android malware |
| Confidence | Medium |
| First Seen | 2026-09-17 |
| Status | Under investigation |
| Description | Synthetic domain used for CTI laboratory analysis |

This format makes the information easier to search, correlate and use in further analysis.

---

# 13. CTI Analytical Workflow

The complete workflow for this Android security project can be represented as:

Requirements → Collection → Validation → Normalization → Enrichment → Correlation → Analysis → Intelligence Production → Dissemination → Feedback

First, the analyst defines what information is required.

Then information is collected from OSINT and other authorized sources.

After collection, the information is validated to determine whether it is reliable.

The data is normalized so that indicators have a consistent format.

Additional information is then added through enrichment.

Correlation connects related indicators.

Finally, the analyst produces intelligence that can be used for security monitoring and detection.

---

# 14. Application of Elastic Stack and Sigma Rules

Elastic Stack can be used to collect and analyze security logs.

For Android-related monitoring, an organization could collect telemetry from mobile applications, backend services, authentication systems and network infrastructure.

Sigma rules can be used to describe suspicious activity in a platform-independent format.

For example, a detection rule could identify repeated authentication failures originating from an unusual source or suspicious communication with a known malicious domain.

The general process is:

Logs → Elastic Stack → Sigma Detection → Alert → IOC Enrichment → MISP → Analyst Investigation

This creates a connection between threat intelligence and security monitoring.

---

# 15. Security Recommendations for Android Applications

Based on the CTI workflow, several security measures can be recommended for Android application developers and users.

Developers should:
* regularly update dependencies;
* remove unnecessary permissions;
* protect sensitive information;
* use secure authentication mechanisms;
* validate network communication;
* avoid storing passwords or sensitive tokens insecurely;
* monitor third-party libraries for vulnerabilities;
* analyze suspicious application behavior;
* use secure HTTPS/TLS communication;
* perform regular security testing.

Users should:

* install applications from trusted sources;
* keep Android and applications updated;
* carefully review application permissions;
* avoid suspicious APK files;
* avoid following suspicious links;
* use additional authentication for sensitive accounts.

---

# 16. Conclusion

Cyber Threat Intelligence provides a structured approach to identifying and analyzing threats against Android mobile applications.

In this project, the CTI lifecycle was applied to the problem of Android application security. Different types of threats were classified, including malicious APKs, spyware, phishing, credential theft, malicious infrastructure and exploitation of vulnerabilities.

OSINT tools such as VirusTotal, Shodan and Maltego can provide different types of information. VirusTotal is useful for investigating files and indicators, Shodan provides information about publicly exposed infrastructure, while Maltego helps visualize relationships between different entities.

MISP can be used as a centralized platform for storing and correlating IOCs. Data normalization and filtering improve the quality of collected intelligence and reduce duplicate or inconsistent information.

The combination of CTI, OSINT, MISP, Elastic Stack and Sigma rules creates a complete workflow for collecting, processing and using threat intelligence to improve the security of Android applications.

---

## References

1. Recorded Future. *The Threat Intelligence Handbook*.
2. SANS Institute. *Cyber Threat Intelligence resources and CTI Summit materials*.
3. MITRE. *MITRE ATT&CK Knowledge Base*.
4. ENISA. *ENISA Threat Landscape*.
5. OSINT Framework. *OSINT Framework*.
6. Michael Bazzell. *Open Source Intelligence Techniques*.
7. MISP Project. *MISP Training and Documentation*.
8. Elastic. *Elastic Stack Documentation*.
9. SigmaHQ. *Sigma Rule Specification and Documentation*.
