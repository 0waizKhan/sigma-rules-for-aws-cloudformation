🛡️ AWS CloudFormation Sigma Detection Rules
A curated collection of Sigma rules designed to detect suspicious or malicious activity in AWS CloudFormation (CFN) events. These rules help security analysts and threat hunters monitor and respond to anomalies within AWS environments using a platform-agnostic detection format.

📌 What is Sigma?
Sigma is an open standard for writing SIEM detection rules in a vendor-agnostic YAML format. Sigma rules can be converted into queries for popular platforms such as:

Splunk

ELK/Elastic

AWS Security Lake

Chronicle

Sentinel

and many more

🚀 Purpose of This Repository
This repository provides:

Detection rules for identifying misconfigurations and potential abuse in AWS CloudFormation.

A starting point for blue teams to implement threat detection in cloud-native environments.

Platform-independent Sigma YAML rules ready for conversion to any supported SIEM or log analysis tool.

📂 Repository Structure

aws-cloudformation-sigma/
│
├── rules/                       # All Sigma rules for AWS CFN
│   ├── unauthorized-resource-creation.yml
│   ├── iam-escalation-via-cfn.yml
│   └── suspicious-stack-deletion.yml
│
├── converters/                 # Optional scripts for Sigma to SIEM rule conversion
│   └── convert-to-elastic.sh
│
├── tests/                      # Sigma rule test cases
│
├── LICENSE
└── README.md

🧪 Testing
You can test rule logic using Sigmac or convert them using your preferred backend.

sigmac -t es-qs rules/iam-escalation-via-cfn.yml

📫 Contact
For suggestions or queries, feel free to open an issue or contact the maintainer.
