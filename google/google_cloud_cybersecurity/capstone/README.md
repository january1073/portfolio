# Google Cloud Cybersecurity Certificate - Capstone Project

For the capstone project, in addition to video lectures and multiple-choice questions, I had to complete practical tasks in a Google Cloud lab and create a security incident report.

## Facts (fictitious)

Cymbal Retail (a financial services provider) experienced a significant security incident involving unauthorized access to its cloud environment. The breach resulted in the exposure of sensitive customer
credit card information, including card numbers, usernames, and associated locations. The attack was facilitated by multiple security misconfigurations, including an insecure firewall, an exposed virtual
machine (VM) with open SSH and RDP ports, and a publicly accessible storage bucket. The security team detected unusual activity, which led to an internal investigation. The malicious actor gained initial
access by exploiting open ports on the cc-app-01 VM, executed a brute-force attack, deployed malware, escalated privileges using a compromised service account key, and ultimately exfiltrated data from
BigQuery via a publicly exposed storage bucket.

## Google Cloud Security Command Center

### Findings

In the Google Cloud Security Command Center (SCC), the following findings were displayed:

#### By category:

![findings_by_category](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/1_findings_category.png)

#### By resource:

![findings_by_resource](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/2_findings_resource.png)

This report details the response and remediation actions taken, as well as recommendations to mitigate similar risks in the future.

### Remediation

After I remediated all major threats, the SCC displayed the following findings :

#### By category

![remediation_by_category](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/3_remediation_category.png)

#### By resource

![remediation_by_resource](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/3_remediation_category.png)

## Security Incident Report

To complete the capsone project, I had to document my findings as well as my response and remediation measures and recommendations in a security incident report: ![final_report](google/google_cloud_cybersecurity/capstone/capstone_final_report.pdf)

## Badge

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="8354ef22-6812-422d-80d2-9c62951ed9db" data-share-badge-host="https://www.credly.com"></div><script type="text/javascript" async src="//cdn.credly.com/assets/utilities/embed.js"></script>
