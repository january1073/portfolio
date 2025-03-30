# Google Cloud Cybersecurity Certificate - Capstone Project

For the capstone project, in addition to video lectures and multiple-choice questions, I had to complete practical tasks in a Google Cloud lab and create a security incident report.

The fictional facts for the lab and the report were as follows:

Cymbal Retail (a financial services provider) experienced a significant security incident involving unauthorized access to its cloud environment. The breach resulted in the exposure of sensitive customer
credit card information, including card numbers, usernames, and associated locations. The attack was facilitated by multiple security misconfigurations, including an insecure firewall, an exposed virtual
machine (VM) with open SSH and RDP ports, and a publicly accessible storage bucket. The security team detected unusual activity, which led to an internal investigation. The malicious actor gained initial
access by exploiting open ports on the cc-app-01 VM, executed a brute-force attack, deployed malware, escalated privileges using a compromised service account key, and ultimately exfiltrated data from
BigQuery via a publicly exposed storage bucket.

In the Google Security Command Center, the following findings were displayed:

By category:

![findings_by_category](image_url)

By resource:

![findings_by_resource](image_url)

This report details the response and remediation actions taken, as well as recommendations to mitigate similar risks in the future.
