# **AWS CloudFormation Sigma Detection Rules**

A curated collection of **Sigma rules** designed to detect suspicious or malicious activity in **AWS CloudFormation (CFN)** events. These rules help security analysts and threat hunters monitor and respond to anomalies within AWS environments using a **platform-agnostic detection format**.

---

## **What is Sigma?**

**[Sigma](https://github.com/SigmaHQ/sigma)** is an open standard for writing SIEM detection rules in a **vendor-agnostic YAML format**.

With Sigma, you can write once and convert to multiple platforms, such as:
- Splunk
- Elastic (ELK)
- AWS Security Lake
- Microsoft Sentinel
- Google Chronicle
- Graylog
- and more

---

##  **Purpose of This Repository**

This repository provides:

✅ **Detection rules** for identifying misconfigurations and threats in AWS CloudFormation  
✅ A **starting point** for security teams building cloud-native detection coverage  
✅ **Platform-independent Sigma YAML rules** ready for conversion

---

##  **Repository Structure**

│
├── rules/ # Sigma rules for AWS CFN
│ ├── unauthorized-resource-creation.yml
│ ├── iam-escalation-via-cfn.yml
│ └── suspicious-stack-deletion.yml
│
├── converters/ # Optional scripts for rule conversion
│ └── convert-to-elastic.sh
│
├── tests/ # Test cases for validation
│
├── LICENSE
└── README.md

##  Testing Rules
You can test or convert rules using sigmac:

sigmac -t es-qs rules/iam-escalation-via-cfn.yml

