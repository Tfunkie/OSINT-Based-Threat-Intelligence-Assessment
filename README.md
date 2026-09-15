# OSINT-Based Threat Intelligence Assessment of Shopify Inc.

This project presents a **defensive Open-Source Intelligence (OSINT) and threat intelligence assessment of Shopify Inc.**, focusing on its publicly observable digital footprint and potential cyber-risk exposure. The assessment examines domains, subdomains, infrastructure, email exposure, phishing and brand-impersonation risks using passive and publicly available intelligence sources. 

## Table of Contents

* Project Overview
* Network Topology
* Tools and Technologies
* Configuration Steps
* Results and Findings
* Author

## Project Overview

The purpose of this project was to assess the publicly exposed digital footprint of **Shopify Inc.**, a global e-commerce technology company headquartered in Ottawa, Canada. The assessment focused on identifying information that could potentially be useful to threat actors for **phishing, brand impersonation, credential harvesting, social engineering, and reconnaissance**. 

The investigation followed a **passive and ethical OSINT methodology**. No active scanning, exploitation, unauthorized access, credential testing, or direct interaction with Shopify infrastructure was conducted. 

Key intelligence requirements included:

* Identifying **phishing and brand-impersonation threats** targeting Shopify.
* Discovering publicly exposed domains, subdomains, APIs, and other internet-facing resources.
* Assessing potential abuse of the **Shopify brand** in fraudulent websites and campaigns.
* Identifying domains, IP addresses, email addresses, and other digital assets associated with Shopify.
* Evaluating publicly available indicators for potential malicious activity. 

## Network Topology

The source document does **not provide a conventional network topology diagram or internal network architecture**. The assessment instead examines Shopify's publicly observable digital infrastructure and external attack surface.

Identified public-facing infrastructure included:

* **Primary domain:** `shopify.com`
* **Merchant administration:** `admin.shopify.com`
* **Authentication and account management:** `accounts.shopify.com`
* **Customer support:** `help.shopify.com`
* **Developer portal:** `developers.shopify.com`
* **Partner portal:** `partners.shopify.com`
* **Service status:** `status.shopify.com`
* **Developer and application-related subdomains:** `apps.shopify.com`, `themes.shopify.com`, `partners.shopify.com`
* **Observed IP addresses:** `23.227.38.33` and `23.227.39.7`
* **Observed hostnames:** `180.shopify.com` and `dev-shops.shopify.com`
* **Email infrastructure:** `@shopify.com` corporate email addresses using email-security technologies such as **SPF, DKIM, and DMARC**.  

The assessment identified publicly accessible services and infrastructure but **did not confirm an internal network compromise or attacker-controlled infrastructure**. 

## Tools and Technologies

* **Google Search / Google Dork** - Passive collection of publicly available information.
* **Bing** - Search-engine-based OSINT collection.
* **theHarvester** - Collection of publicly available domains, subdomains, email addresses, and related information.
* **Sublist3r** - Passive subdomain enumeration.
* **Shodan** - Identification and analysis of internet-exposed infrastructure and services.
* **VirusTotal** - Domain, IP, URL reputation, and threat-intelligence analysis.
* **AbuseIPDB** - IP reputation and abuse-report validation.
* **Have I Been Pwned** - Historical breach-exposure checking for email addresses.
* **WHOIS/RDAP** - Domain registration and ownership-related information.
* **urlscan.io** - Analysis of publicly accessible URLs, redirects, domains, IPs, and certificates.
* **Wayback Machine** - Examination of historical versions of publicly accessible websites.
* **OSINT Framework** - Reference and discovery of OSINT resources.  

## Configuration Steps

1. **Defined the intelligence requirements** for the Shopify OSINT assessment, including phishing, brand impersonation, exposed assets, and potential abuse indicators.
2. **Established the scope and limitations** by restricting the investigation to passive OSINT and publicly available information.
3. **Collected domain and subdomain intelligence** associated with `shopify.com` using search engines, `theHarvester`, and `Sublist3r`.
4. **Collected publicly associated email and IP information** through passive OSINT techniques.
5. **Investigated internet-exposed infrastructure** using Shodan.
6. **Validated candidate domains and indicators** using VirusTotal.
7. **Checked IP reputation** using AbuseIPDB and validated ownership-related information using WHOIS/RDAP.
8. **Checked historical email exposure** using Have I Been Pwned.
9. **Reviewed publicly accessible URLs and web indicators** using urlscan.io.
10. **Reviewed historical Shopify webpages** using the Wayback Machine to identify changes over time.
11. **Correlated information from multiple OSINT sources** instead of relying on a single indicator.
12. **Assessed the likelihood and potential business impact** of identified exposures.
13. **Developed defensive recommendations** covering brand monitoring, MFA, email security, security awareness, OSINT monitoring, and infrastructure validation.  

## Results and Findings

The assessment identified a **broad publicly observable digital footprint** consisting of domains, subdomains, IP infrastructure, public services, and associated email information. However, **no confirmed compromise of Shopify infrastructure was identified**. 

### Key Findings

* **Phishing and brand impersonation** were identified as the primary potential risks.
* `support@shopify.com` appeared in historical breach datasets through **Have I Been Pwned**, representing a potential social-engineering and phishing target.
* Public Shopify-related domains and subdomains were identified through passive OSINT.
* `23.227.38.33` was identified as publicly associated with Shopify infrastructure and had historical abuse reports; however, the report emphasizes that an IP reputation report alone does **not establish compromise**.
* `checkout.shopify.com` was identified as a legitimate Shopify subdomain associated with checkout services.
* `myshopify.com` was identified as a legitimate Shopify-related domain and did not provide confirmed malicious evidence in the assessment.
* No credentials were reproduced or collected during the investigation.
* No attacker infrastructure was confirmed. 

### Risk Assessment

| Indicator              | Likelihood | Impact | Risk Level  |
| ---------------------- | ---------- | ------ | ----------- |
| `myshopify.com`        | Low        | Medium | Low         |
| `checkout.shopify.com` | Low        | High   | Medium/High |
| `23.227.38.33`         | Low/Medium | Medium | Low/Medium  |
| `support@shopify.com`  | Medium     | Medium | Medium      |

The most significant business risks identified were **financial loss, reputational damage, customer-trust impacts, and potential regulatory exposure** resulting from successful phishing, impersonation, credential theft, account takeover, or fraud. 

### Recommendations

* Implement continuous **brand monitoring and phishing-domain takedown processes**.
* Monitor newly registered domains containing Shopify-related keywords.
* Enforce **Multi-Factor Authentication (MFA)** for employees, administrators, and privileged accounts.
* Strengthen **SPF, DKIM, and DMARC** email-security controls.
* Conduct regular **security-awareness and phishing training**.
* Continuously monitor **VirusTotal, urlscan.io, WHOIS/RDAP, and breach-intelligence sources**.
* Monitor externally visible **IP addresses, domains, certificates, and services**.
* Correlate multiple intelligence sources before classifying an IP or infrastructure component as malicious, particularly when shared cloud or CDN infrastructure is involved. 

Overall, the report assessed Shopify's security posture as **moderate exposure with no confirmed compromise identified from the assessed indicators**. Continuous OSINT monitoring was recommended to detect emerging phishing, impersonation, infrastructure, and breach-related threats earlier. 

## Author

**Awodimibola, Tosin Funke**

* **Cohort:** May 2026 Cohort
* **Assessment Date:** 14 August 2026
* **Project:** OSINT-Based Threat Intelligence Assessment of Shopify Inc.
* **Contact:** Not provided in the source document. 
