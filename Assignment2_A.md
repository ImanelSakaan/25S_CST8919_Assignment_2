# 🔒 CST8919 DevOps – Security and Compliance

## ☁️ Cloud Security & DevSecOps Service Comparison (Azure vs AWS vs GCP)

## Overview

This repository provides a detailed comparison of key **Microsoft Azure** security, compliance, and DevSecOps services with their closest equivalents in **Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)**.

### Scope
The comparison focuses on five major security and DevSecOps service categories:
1. **Identity & Access Management (SSO, IAM)** – Workforce and customer identity, SSO, and access control.
2. **Monitoring & Logging** – Metrics, logs, traces, and audit trails.
3. **Policy & Governance** – Cloud resource compliance, guardrails, and automated remediation.
4. **Cloud Security Posture & Workload Protection** – CSPM, CNAPP, vulnerability management, and threat detection.
5. **SIEM / SOAR** – Security information and event management, plus automation and orchestration.

<img width="836" height="824" alt="ChatGPT Image Aug 13, 2025, 03_21_04 PM" src="https://github.com/user-attachments/assets/126c15da-a250-4130-b3f9-1f3e7a4952f0" />

## Table of Contents

1. [Quick Mapping](#quick-mapping)
2. [1) Identity & Access Management (SSO, IAM)](#1-identity--access-management-sso-iam)
   - [Azure — Microsoft Entra ID (Azure AD)](#azure--microsoft-entra-id-azure-active-directory)
   - [AWS — IAM Identity Center (+ IAM) / Amazon Cognito](#aws--iam-identity-center--iam--amazon-cognito)
   - [GCP — Cloud Identity / Cloud IAM / Identity Platform](#gcp--cloud-identity--cloud-iam--identity-platform)
3. [2) Monitoring & Logging](#2-monitoring--logging)
   - [Azure — Azure Monitor & Log Analytics](#azure--azure-monitor--log-analytics)
   - [AWS — Amazon CloudWatch (+ CloudTrail)](#aws--amazon-cloudwatch--cloudtrail)
   - [GCP — Cloud Monitoring & Cloud Logging (+ Cloud Audit Logs)](#gcp--cloud-monitoring--cloud-logging--cloud-audit-logs)
4. [3) Policy & Governance](#3-policy--governance)
   - [Azure — Azure Policy](#azure--azure-policy)
   - [AWS — AWS Config + Organizations SCPs](#aws--aws-config--organizations-scps)
   - [GCP — Organization Policy Service (+ Policy Controller/Config Validator)](#gcp--organization-policy-service--policy-controllerconfig-validator)
5. [4) Cloud Security Posture / Threat & Workload Protection](#4-cloud-security-posture--threat--workload-protection)
   - [Azure — Microsoft Defender for Cloud](#azure--microsoft-defender-for-cloud)
   - [AWS — Security Hub + GuardDuty + Inspector (+ Macie)](#aws--security-hub--guardduty--inspector--macie)
   - [GCP — Security Command Center (SCC)](#gcp--security-command-center-scc)
6. [5) SIEM / SOAR](#5-siem--soar)
   - [Azure — Microsoft Sentinel (SIEM/SOAR)](#azure--microsoft-sentinel-siemsoar)
   - [AWS — Closest Alternatives (No fully managed SIEM)](#aws--closest-alternatives-no-fully-managed-siem)
   - [GCP — Chronicle SIEM (with SOAR options)](#gcp--chronicle-siem-with-soar-options)
7. [Decision Points & Notes](#decision-points--notes)
8. [DevSecOps Integration Cheatsheet](#devsecops-integration-cheatsheet)
9. [Repository Structure](#repository-structure)
10. [CSV Matrix (for spreadsheets)](#csv-matrix-for-spreadsheets)
11. [How to Publish to GitHub](#how-to-publish-to-github)

---

## 1. Identity & Access Management (SSO, IAM) - Azure, AWS, GCP

| **Feature** | **Microsoft Azure** | **Amazon Web Services (AWS)** | **Google Cloud Platform (GCP)** |
|-------------|--------------------|------------------------------|----------------------------------|
| **Primary IAM Service** | Azure Active Directory (Entra ID) | AWS Identity and Access Management (IAM) | Identity and Access Management (IAM) |
| **Single Sign-On (SSO)** | Azure AD Single Sign-On | AWS Single Sign-On (AWS IAM Identity Center) | Cloud Identity / Google Workspace SSO |
| **User Federation** | Azure AD B2B/B2C | AWS IAM Federation with SAML / OIDC | Cloud Identity Federation with SAML / OIDC |
| **Role-Based Access Control (RBAC)** | Azure RBAC | AWS IAM Roles & Policies | IAM Roles & Policies |
| **Multi-Factor Authentication (MFA)** | Azure MFA (Microsoft Authenticator, SMS, Voice) | AWS MFA (Virtual MFA App, U2F Key, SMS) | 2-Step Verification (Google Authenticator, Security Keys) |
| **Privileged Access Management (PAM)** | Azure AD Privileged Identity Management (PIM) | IAM Access Analyzer + AWS SSO Permission Sets | IAM Recommender + Policy Analyzer |
| **Conditional Access** | Azure Conditional Access Policies | AWS IAM Policy Conditions | Context-Aware Access (Google) |
| **Audit & Activity Logs** | Azure AD Sign-in Logs, Audit Logs | AWS CloudTrail, IAM Access Analyzer Logs | Cloud Audit Logs |
| **Passwordless Authentication** | FIDO2 Security Keys, Windows Hello for Business | U2F/FIDO2 Security Keys | Titan Security Key, Google Prompt |
| **Integration with On-Premises AD** | Azure AD Connect | AD Connector for AWS Directory Service | Google Cloud Directory Sync (GCDS) |

---

## 2. Monitoring & Logging Services Comparison

## Overview
This table compares **Monitoring & Logging** services across Microsoft Azure, Amazon Web Services (AWS), and Google Cloud Platform (GCP).

| Cloud Provider | Service Name | Overview | Core Features | Security & Compliance | Pricing Model | DevSecOps Integration |
|----------------|--------------|----------|---------------|-----------------------|---------------|-----------------------|
| **Azure** | Azure Monitor | Comprehensive platform for collecting, analyzing, and acting on telemetry from cloud and on-premises environments. | Metrics & logs collection, Application Insights, Alerts, Dashboards, Workbooks | ISO 27001, SOC, GDPR, HIPAA, FedRAMP | Pay-as-you-go based on data ingestion & retention | Integrates with Azure DevOps, GitHub Actions, REST API, Logic Apps |
| **Azure** | Log Analytics | Service for querying and analyzing log data collected by Azure Monitor. | Kusto Query Language (KQL), data correlation, visualization | ISO 27001, SOC, GDPR, HIPAA, FedRAMP | Charged per GB ingested and retention duration | Works with CI/CD for automated diagnostics and monitoring |
| **AWS** | Amazon CloudWatch | Monitoring and observability service for AWS and on-prem resources. | Metrics, logs, events, alarms, dashboards | ISO 27001, SOC, PCI DSS, GDPR, FedRAMP | Pay-as-you-go per metric, log ingestion, and dashboard usage | Integrates with CodePipeline, CodeBuild, Lambda, EventBridge |
| **GCP** | Cloud Monitoring | Provides visibility into performance, uptime, and health of cloud-powered apps. | Metrics, alerts, dashboards, uptime checks | ISO 27001, SOC, GDPR, HIPAA | Free tier, then pay per API call and metric volume | Integrates with Cloud Build, Cloud Functions, Pub/Sub |
| **GCP** | Cloud Logging | Centralized logging service for GCP and hybrid environments. | Log ingestion, querying, routing, alerting | ISO 27001, SOC, GDPR, HIPAA | Pay-as-you-go based on log ingestion & storage | Integrates with Cloud Operations Suite, Pub/Sub, CI/CD pipelines |

---

## Key Notes
- **Azure Monitor + Log Analytics** work together; Monitor handles collection and analysis, Log Analytics specializes in querying.
- **AWS CloudWatch** combines metrics, logs, and events, but detailed log querying may require CloudWatch Logs Insights.
- **GCP Cloud Monitoring + Logging** integrate under the Operations Suite, allowing seamless metric-log correlation.

---

## 3) Policy & Governance
# Policy & Governance
# Cloud Security & Compliance Services Comparison

We have implemented security, compliance, and DevSecOps practices using Microsoft Azure services. Below is a comparison of equivalent services in AWS and GCP.

## 1. Identity & Access Management (SSO, IAM)

| Feature / Aspect            | Azure                                 | AWS Equivalent                    | GCP Equivalent                    |
|-----------------------------|--------------------------------------|----------------------------------|----------------------------------|
| Core Features               | Azure Active Directory (AAD): SSO, IAM, MFA, Conditional Access | AWS Identity and Access Management (IAM), AWS Single Sign-On | Google Identity, Cloud IAM, Identity-Aware Proxy |
| Security & Compliance       | ISO 27001, SOC 1/2/3, GDPR, HIPAA   | ISO 27001, SOC 1/2/3, GDPR, HIPAA | ISO 27001, SOC 1/2/3, GDPR, HIPAA |
| Pricing Model               | Free tier + per-user/licensed features | Free tier + per-user/licensed features | Free tier + per-user/licensed features |
| DevSecOps Integration       | Supports CI/CD integration, API access, Terraform, GitHub Actions | Supports Terraform, CloudFormation, CI/CD pipelines | Supports Terraform, Cloud Build, CI/CD pipelines |

## 2. Monitoring & Logging

| Feature / Aspect            | Azure                                 | AWS Equivalent                    | GCP Equivalent                    |
|-----------------------------|--------------------------------------|----------------------------------|----------------------------------|
| Core Features               | Azure Monitor & Log Analytics: metrics, logs, alerts, dashboards | Amazon CloudWatch: metrics, logs, alarms, dashboards | Google Cloud Monitoring & Logging: metrics, logs, alerts, dashboards |
| Security & Compliance       | SOC, ISO, GDPR, HIPAA                 | SOC, ISO, GDPR, HIPAA            | SOC, ISO, GDPR, HIPAA            |
| Pricing Model               | Pay-per-use (ingested data, alerts)  | Pay-per-use (metrics, logs, dashboards) | Pay-per-use (metrics, logs, dashboards) |
| DevSecOps Integration       | CI/CD pipelines, API access, Terraform | Supports CloudFormation, Terraform, CI/CD | Supports Terraform, Cloud Build, CI/CD |

## 3. Policy & Governance

| Feature / Aspect            | Azure                                 | AWS Equivalent                    | GCP Equivalent                    |
|-----------------------------|--------------------------------------|----------------------------------|----------------------------------|
| Core Features               | Azure Policy: enforce standards and compliance | AWS Config & AWS Organizations   | Google Cloud Policy Intelligence & Organization Policy |
| Security & Compliance       | ISO, SOC, HIPAA, GDPR                 | ISO, SOC, HIPAA, GDPR            | ISO, SOC, HIPAA, GDPR            |
| Pricing Model               | Pay-per-policy evaluation             | Pay-per-rule evaluation           | Free tier + pay-per-policy evaluations |
| DevSecOps Integration       | CI/CD automation, ARM templates, Terraform | CloudFormation, Terraform, CI/CD | Terraform, Deployment Manager, CI/CD |

## 4. Threat Protection

| Feature / Aspect            | Azure                                 | AWS Equivalent                    | GCP Equivalent                    |
|-----------------------------|--------------------------------------|----------------------------------|----------------------------------|
| Core Features               | Microsoft Defender for Cloud: threat detection, vulnerability management | AWS GuardDuty, AWS Security Hub  | Google Cloud Security Command Center |
| Security & Compliance       | SOC, ISO, HIPAA, GDPR                 | SOC, ISO, HIPAA, GDPR            | SOC, ISO, HIPAA, GDPR            |
| Pricing Model               | Pay-as-you-go per resource            | Pay-per-findings, resource count | Pay-as-you-go per resource       |
| DevSecOps Integration       | Integrates with Azure Sentinel, CI/CD pipelines | Integrates with CloudWatch, CI/CD | Integrates with Cloud Logging, CI/CD |

## 5. SIEM / SOAR

| Feature / Aspect            | Azure                                 | AWS Equivalent                    | GCP Equivalent                    |
|-----------------------------|--------------------------------------|----------------------------------|----------------------------------|
| Core Features               | Azure Sentinel: SIEM & SOAR, analytics, automated response | AWS Security Hub + Amazon Detective | Chronicle Security (SIEM), Security Command Center (SOAR) |
| Security & Compliance       | SOC, ISO, HIPAA, GDPR                 | SOC, ISO, HIPAA, GDPR            | SOC, ISO, HIPAA, GDPR            |
| Pricing Model               | Pay-per-data-ingested + alerts        | Pay-per-finding & volume-based   | Pay-per-ingested event/log        |
| DevSecOps Integration       | APIs, playbooks, connectors, Terraform | Integrates with CI/CD & automation | APIs, SIEM integrations, Terraform |








| Category                     | Azure Services / Features                         | Purpose / Description                                                                 |
|-------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------|
| Governance & Management       | Azure Policy                                     | Define, enforce, and monitor compliance of resources with organizational standards.  |
|                               | Azure Blueprints                                 | Create repeatable environments with governance, policies, and resource templates.   |
|                               | Management Groups                                | Organize subscriptions into hierarchical groups for unified policy and access.      |
|                               | Azure Resource Graph                             | Explore and query resources at scale for governance and auditing.                    |
| Compliance & Audit            | Microsoft Compliance Manager                     | Assess compliance with regulatory standards and manage controls.                     |
|                               | Azure Security Center / Microsoft Defender      | Continuous security posture assessment and recommendations for compliance.           |
|                               | Azure Monitor & Log Analytics                    | Track resource activity and audit logs for governance and regulatory requirements.   |
| Access Control & IAM Policies | Azure Active Directory Conditional Access        | Enforce access policies based on user, device, location, and risk.                  |
|                               | Role-Based Access Control (RBAC)                | Assign granular permissions to users, groups, and applications.                      |
|                               | Privileged Identity Management (PIM)            | Manage and control privileged accounts with just-in-time access.                     |
| Cost & Resource Management    | Azure Cost Management + Billing                  | Monitor usage, enforce budgets, and optimize cloud spend.                            |
|                               | Tags & Resource Naming Conventions               | Implement organizational standards for easier governance and reporting.             |


### Azure — Azure Policy
**Overview.** Declarative policy engine to **audit**, **deny**, or **deployIfNotExists** across subscriptions/management groups.  
**Core Features.** Built‑in definitions, initiatives, remediation tasks, guest‑config for VMs, compliance dashboard; integrates with **Defender for Cloud** and **Blueprints**.  
**Security & Compliance.** Helps enforce guardrails aligned to standards (CIS, NIST, PCI) using built‑ins.  
**Pricing Model.** No direct charge for evaluation; remediation uses underlying resources (e.g., deployments/guest config).  
**Integration for DevSecOps.** ARM/Bicep/Terraform; GitHub Actions/Azure DevOps; compliance data to Log Analytics/Sentinel; policy-as-code patterns.

### AWS — AWS Config + Organizations SCPs
**Overview.** **Config** records resource state and evaluates against rules; **SCPs** set account guardrails at org level.  
**Core Features.** Managed rules, custom rules (Lambda), conformance packs, remediation, drift detection; SCP service‑control deny/allow patterns.  
**Security & Compliance.** Supports mapping to CIS/NIST via conformance packs.  
**Pricing Model.** Per configuration item recorded and rule evaluation; remediation actions incur provider costs.  
**Integration for DevSecOps.** CloudFormation/CDK/Terraform; findings to **Security Hub**/**Security Lake**; EventBridge automations; Config data to S3.

### GCP — Organization Policy Service (+ Policy Controller/Config Validator)
**Overview.** Org Policy enforces constraints (allowed services, locations, CMEK, external IPs). **Policy Controller** (OPA/Gatekeeper) validates Kubernetes configs.  
**Core Features.** Hierarchical constraints (org/folder/project), dry‑run, audit; Config Validator for CI/CD checks.  
**Security & Compliance.** Enforces guardrails that align with CIS/NIST blueprints.  
**Pricing Model.** No direct charge for Org Policy; enforcement/validation uses underlying services.  
**Integration for DevSecOps.** Terraform; Cloud Build/GitHub Actions; Audit to Cloud Logging/BigQuery; combinations with **SCC** and **Forseti (legacy)** patterns.

---

## 4) Cloud Security Posture / Threat & Workload Protection

### Azure — Microsoft Defender for Cloud
**Overview.** CSPM + CNAPP covering multi‑cloud; vulnerability assessment, threat detection, hardening recommendations.  
**Core Features.** Secure score, regulatory compliance, VM/container/DB protection, agentless scanning, Defender for Containers/Kubernetes, Just‑in‑Time (JIT) VM access, workload‑specific plans.  
**Security & Compliance.** Built‑in standards mappings (CIS, NIST, PCI).  
**Pricing Model.** Free tier (recommendations/secure score); paid plans priced per resource type (VM/vCore/k8s/DB) per hour or vCPU.  
**Integration for DevSecOps.** Alerts to **Sentinel**, Logic Apps playbooks, GitHub/Azure DevOps, REST/Graph APIs, multi‑cloud connectors (AWS/GCP).

### AWS — Security Hub + GuardDuty + Inspector (+ Macie)
**Overview.** Aggregated security posture (**Security Hub**) with findings from native/partner tools; **GuardDuty** for threat detection; **Inspector** for vuln scans; **Macie** for data security.  
**Core Features.** Security standards (CIS, Foundational), centralized findings, automated response via EventBridge/Step Functions, agentless ECR/EC2 scanning.  
**Security & Compliance.** Aligns with AWS best practices and CIS; supports multi‑account via Organizations.  
**Pricing Model.** Security Hub billed per security check and ingested finding; GuardDuty per analyzed event/GB; Inspector per instance/image; Macie per GB of data classification.  
**Integration for DevSecOps.** Findings to **Security Lake**/**OpenSearch**/**SIEM**; IaC via CloudFormation/CDK/Terraform; automation with EventBridge, Systems Manager, Lambda.

### GCP — Security Command Center (SCC)
**Overview.** GCP‑native CNAPP: asset inventory, misconfig & vuln detection, threat intel (Premium), container and VM insights.  
**Core Features.** Security Health Analytics, Event Threat Detection, VM/Container scanning, sensitive data discovery integrations. Tiers: **Standard** and **Premium**.  
**Security & Compliance.** Findings mapped to common frameworks (CIS/NIST).  
**Pricing Model.** Standard (no cost); Premium paid — typically per vCPU/resource footprint (varies by detector).  
**Integration for DevSecOps.** Findings to **Chronicle**, **Pub/Sub**, **Cloud Logging**, BigQuery; Terraform; automation via Cloud Functions/Workflows.

---

## 5) SIEM / SOAR

### Azure — Microsoft Sentinel (SIEM/SOAR)
**Overview.** Cloud‑native SIEM with built‑in SOAR playbooks (Logic Apps). KQL analytics over Log Analytics.  
**Core Features.** Data connectors (Microsoft 365, Defender suite, AWS/GCP, Syslog/CEF), analytics rules, UEBA, hunting, notebooks, automation rules, content hub.  
**Security & Compliance.** Inherits Azure certifications; supports customer‑managed keys and data residency options.  
**Pricing Model.** Per‑GB ingestion and retention; commitment tiers and basic logs options; entity behavior priced per vCore in some regions.  
**Integration for DevSecOps.** Hundreds of connectors, GitHub Actions for IaC/content, Logic Apps for SOAR, REST APIs, export to external storage.

### AWS — Closest Alternatives (No fully managed SIEM)
**Overview.** Combine **Security Lake** (centralized security data), **OpenSearch**/**Partner SIEM** for analytics, **Security Hub** for findings, **Detective** for investigations, and **EventBridge/Step Functions** for SOAR‑like automation.  
**Core Features.** Central lake (OTel/OCSF), dashboards/queries in OpenSearch or partner SIEM, graph analytics in Detective.  
**Pricing Model.** Charges across Security Lake (ingest/storage), OpenSearch (compute/storage), and any partner SIEM licensing.  
**Integration for DevSecOps.** Extensive EventBridge integrations, Lambda, Systems Manager; IaC via CDK/CloudFormation/Terraform.

### GCP — Chronicle SIEM (with SOAR options)
**Overview.** Google’s SaaS SIEM (Chronicle) with high‑scale log retention and analytics; SOAR via Chronicle playbooks/partners and Cloud Workflows.  
**Core Features.** OCSF parsers, UDM graph, threat intel, detections, case mgmt (via integrations), long‑term retention.  
**Pricing Model.** Subscription or ingestion‑based (varies by plan/partner).  
**Integration for DevSecOps.** Native sinks from Cloud Logging/SCC, connectors for AWS/Azure, APIs, BigQuery integration.

---

## Decision Points & Notes

- **Identity (workforce vs customer).** Azure AD/Entra spans both; in AWS/GCP, split between workforce SSO (Identity Center/Cloud Identity) and customer identity (Cognito/Identity Platform).  
- **SIEM.** Azure has a first‑party SIEM (**Sentinel**). GCP offers **Chronicle**. AWS relies on **Security Lake + OpenSearch or partner SIEM**; plan for architecture/operations accordingly.  
- **Policy Controls.** Azure Policy supports **deny/deployIfNotExists**; AWS uses **SCPs** for org‑wide guardrails and **Config** for evaluation & remediation; GCP’s **Org Policy** enforces hierarchical constraints.  
- **Cost.** All platforms charge primarily on **ingestion/retention/scan volume** for logs and security analytics. Commitment/usage tiers can materially reduce cost. Always model projected ingest and retention.

---

## DevSecOps Integration Cheatsheet

- **IaC:** Azure (ARM/Bicep/Terraform), AWS (CloudFormation/CDK/Terraform), GCP (Deployment Manager/Terraform).  
- **Pipelines:** GitHub Actions, Azure DevOps, AWS CodePipeline, Cloud Build.  
- **Eventing/Automation:** Azure (Logic Apps/Event Grid), AWS (EventBridge/Lambda/Step Functions), GCP (Eventarc/Cloud Functions/Workflows).  
- **Data Flow to SIEM:** Use native connectors/sinks (e.g., Diagnostics settings → Log Analytics/Sentinel; CloudWatch/CloudTrail → Security Lake/OpenSearch; Cloud Logging → Chronicle/BigQuery).

---

## Repository Structure

```
cloud-security-devsecops-comparison/
├─ README.md  ← This document
├─ docs/
│  └─ matrices/
│     └─ quick-mapping.csv
└─ LICENSE (MIT)
```

---

## CSV Matrix (for spreadsheets)

A machine‑readable version of the quick mapping is included at `docs/matrices/quick-mapping.csv`.

---

## How to Publish to GitHub

```bash
# 1) Initialize the repo locally
git init cloud-security-devsecops-comparison
cd cloud-security-devsecops-comparison

# 2) Copy files from this folder into the repo directory

# 3) Commit
git add .
git commit -m "Add Azure/AWS/GCP security & DevSecOps comparison"

# 4) Create a new GitHub repo (via UI or gh CLI) and push
# Using GitHub CLI:
gh repo create your-org/cloud-security-devsecops-comparison --public --source=. --remote=origin --push
```

---

> **Disclaimer.** Service names, features, and pricing change frequently. Validate specifics (SKUs, regional availability, and compliance attestations) with the official cloud documentation for your target region and date.
