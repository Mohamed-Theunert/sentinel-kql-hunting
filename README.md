# 🛡 Microsoft Sentinel KQL Hunting Queries

This repository contains practical hunting queries for Microsoft Sentinel and Microsoft Defender, focused on identity threats, privilege escalation, and cloud-native attack techniques.

The goal is to simulate real-world blue team detection scenarios in hybrid environments.

---

## 🎯 Focus Areas

- Identity Threat Detection (Entra ID)
- Privilege Escalation Monitoring
- OAuth & Consent Abuse Detection
- Endpoint-based Attack Techniques (LOLBins, Encoded Payloads)
- Hybrid Cloud Security Monitoring

---

## 📁 Structure


---

## 📂 Query Overview

### 🔎 impossible_travel.kql
Detects users signing in from multiple geographic locations within a short timeframe.

### 🔐 privileged_role_assignment.kql
Monitors role assignments and potential privilege escalation events.

### 🧩 suspicious_oauth_consent.kql
Detects suspicious OAuth consent grants and service principal additions.

### ⚡ suspicious_encoded_powershell.kql
Identifies encoded PowerShell execution attempts in Defender for Endpoint logs.

### 🔗 admin_role_plus_new_location.kql
Correlates privileged role assignments with multi-location login activity within a defined timeframe.

---

## 🧠 Detection Philosophy

These queries are designed to reflect real-world threat hunting approaches:

- Combine identity and endpoint signals
- Detect post-compromise privilege escalation
- Identify abnormal authentication behavior
- Monitor cloud-native attack vectors
- Build correlation logic across multiple log sources

---

## ⚙ Requirements

- Microsoft Sentinel
- Microsoft Defender for Endpoint
- Entra ID AuditLogs and SigninLogs enabled
- Proper log ingestion configuration

---

## 👤 Author

Mohamed Theunert  
Identity & Cloud Security | Microsoft 365 | Entra ID | Active Directory  

---

> “Security is not a product – it is a continuous process.”
