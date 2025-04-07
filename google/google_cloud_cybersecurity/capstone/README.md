# Respond and recover from a data breach in Google Cloud
### Capstone project of the Google Cloud Cybersecurity Certificate
For the Google Cloud Cybersecuity Certificate capstone project, in addition to video lectures and multiple-choice questions, I had to complete practical tasks in a Google Cloud lab and create a security incident report.

## Facts (fictitious)
Cymbal Retail (a financial services provider) experienced a significant security incident involving unauthorized access to its cloud environment. The breach resulted in the exposure of sensitive customer
credit card information, including card numbers, usernames, and associated locations. The attack was facilitated by multiple security misconfigurations, including an insecure firewall, an exposed virtual
machine (VM) with open SSH and RDP ports, and a publicly accessible storage bucket. The security team detected unusual activity, which led to an internal investigation. The malicious actor gained initial
access by exploiting open ports on the cc-app-01 VM, executed a brute-force attack, deployed malware, escalated privileges using a compromised service account key, and ultimately exfiltrated data from
BigQuery via a publicly exposed storage bucket.

## Lab

### Findings
The Cloud Security Command Center (SCC), PCI DSS 3.2.1 report, displayed the following critical vulnerabilities, i.e. findings with high and medium severity:

![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot02.png)

#### Insecure firewall
- Open SSH port
- Open RDP port
- Firewall rule logging disabled

#### Exposed compute instance cc-app-01
- Malware bad domain
- Compute secure boot disabled
- Default service account used
- Public IP address
- Full API access

#### Publicly accessible storage bucket
- Public bucket ACL
- Bucket policy only disabled
- Bucket logging disabled

### Remediation
In order to remediate the critical findings, I fixed the compute engine vulnerabilities and cloud storage bucket permissions, limited firewall ports access and, finally, verified compliance.

#### Compute Engine vulnerabilities

- I shut down the vulnerable VM cc-app-01 and created a new VM cc-app-02 from a snapshot.

  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot03.png)

  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot04.png)

- I turned on "Secure Boot" for the new VM.

  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot05.png)

- I deleted the compromised VM cc-app-01.

  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot06.png)

#### Cloud Storage bucket permissions

- I switched the publicly accessible bucket's access control to uniform but ensured that users who rely on basic project roles to access the bucket wouldn't lose their access.

  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot08.png)

- I removed permissions for the "allUsers" principals from the storage bucket to enforce a single set of permissions for the bucket and its objects.

  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot09.png)

#### Firewall ports access

- I restricted ICMP, RDP, and SSH access, ...

  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot12.png)

- ... customized firewall rules, ...

  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot10.png)
  ![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot11.png)

- ... and enabled logging.

![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot13.png)


#### Compliance
After I had taken these remediation actions in Google Cloud, I verified compliance in the PCI DSS 3.2.1 report:

![findings](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/screenshot14.png)

## Security Incident Report

To complete the capsone project, I had to document my findings in a security incident report. This report detailed the response and remediation actions taken, as well as recommendations to mitigate similar risks in the future: ![final report](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/capstone_final_report.pdf)

## Badge

![badge](https://github.com/january1073/training/blob/main/google/google_cloud_cybersecurity/capstone/google_cloud_cybersecurity_badge.png)

Verified by Credly: https://www.credly.com/badges/8354ef22-6812-422d-80d2-9c62951ed9db/public_url
