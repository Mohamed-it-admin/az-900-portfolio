# AZ-900 Microsoft Azure Hands-On Portfolio

Welcome to my cloud engineering portfolio. This repository serves as a centralized, structured log of practical deployment environments, architectural implementations, and administrative labs mapped against the **Microsoft AZ-900: Azure Fundamentals** engineering objectives.

---

## 📂 Active Lab Repositories

### 🔐 [Lab 01: Secure Third-Party File Sharing](./README.md)
* **Core Technologies:** Azure Blob Storage, Stored Access Policies (SAP), Shared Access Signatures (SAS), Storage Security.
* **Objective:** Architectural implementation of a zero-trust, business-to-business (B2B) object sharing pattern providing granular, time-limited, and instantly revocable read paths without key exposure.
* **Troubleshooting Logs:** Resolving REST API `PublicAccessNotPermitted` blocks and debugging cross-timezone client/server token de-synchronization drifts (`AuthenticationFailed`).

---

## ⚙️ Engineering & Architecture Reference Logs

### 1. Resource Isolation & Base Infrastructure
* Deployed resource isolation architecture using geographic containment boundaries (`rg-gp-file-exchange`) inside the **North Europe** region.
* Standard-performance storage tier configuration matching locally redundant storage (LRS) replication rules for highly available object lifecycle isolation.
* **Container Hardening:** Provisioned private container constraints (`partner-drop`) enforcing complete anonymous access blocking right at the REST API access layer.

---

## 🔐 Advanced Security Engineering: Stored Access Policies vs. Ad-Hoc SAS
A critical security engineering rule implemented in this environment is the absolute isolation of structural access tokens. Ad-hoc tokens generated directly on individual objects present high business operational risk: if leaked, they cannot be revoked without rotating root storage account keys, causing wide-scale environment downtime.

By anchoring this deployment through a **Stored Access Policy (`partner-read-policy`)**, access authority is abstracted to a container policy layer:
* Immediate, centralized expiration control panels.
* Complete granular visibility isolation.
* Instantly killable access paths without root key manipulation overhead.

---

## 🛠️ Operational Troubleshooting & Remediation

### Rejection Block A: Endpoint Boundary Test
* **Symptom:** Direct object URI browser request returns XML error payloads.
* **Error Identity:** `PublicAccessNotPermitted`
* **Root Cause:** Verified data plane protection posture. Front-end public internet access blocks functioned successfully against unauthenticated raw object parsing.

### Rejection Block B: Time Window De-synchronization
* **Symptom:** Initial signed signature wrapper attempts fail with strict server denial logs.
* **Error Identity:** `AuthenticationFailed` / *Signature not valid in the specified time frame*
* **Analysis:** Structural time zone configuration mismatches between localized browser client runtimes (UTC-8) and regional container data policies (UTC+2).
* **Remediation:** Synchronized localized access policy parameters precisely across the target timeframe, resulting in absolute access parsing verification.

---

## 🧠 Core Competencies Proven
1. Granular implementation of the cloud **Least Privilege Principle**.
2. Advanced parsing and parsing remediation of **Azure REST API XML error syntax logs**.
3. Lifecycle administration controls to automate zero-overhead compliance schedules.
