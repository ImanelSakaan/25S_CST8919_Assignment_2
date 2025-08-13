# 🔒 CST8919 DevOps – Security and Compliance

## ☁️ Cloud Security & Compliance Services Comparison (Azure vs AWS vs GCP)   

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

---

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
