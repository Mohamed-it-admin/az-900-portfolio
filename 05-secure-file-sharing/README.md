# Lab 05: Secure Third-Party File Sharing in Microsoft Azure

## 🏢 Project Overview
This project implements a secure, business-to-business (B2B) file-sharing architecture using **Azure Blob Storage**. The core requirement was to share a sensitive data file (`monthly-report.txt`) with an external partner under strict security constraints: **no public access**, **read-only permissions**, a **highly restricted time window**, and **zero exposure** of root storage account keys.

To achieve this, the project leverages a **Stored Access Policy (SAP)** combined with a **Shared Access Signature (Signature-level SAS)**, providing a fully revocable and auditable sharing solution.

---

## 🏗️ Resource Hierarchy & Architecture
---

## ⚙️ Engineering Reference & Visuals
The deployment includes infrastructure configuration in North Europe with hardened private containers (`partner-drop`) blocking anonymous access. Configuration screenshots are stored in the repository (e.g., `../01-resource-group-creation.png` through `../06-generate-sas-token-url.png`).

---

## 🔐 Security Engineering: Stored Access Policies
Using a **Stored Access Policy (`partner-read-policy`)** avoids ad-hoc SAS risks, allowing centralized expiration control and instant revocation without root key rotation.

---

## 🛠️ Troubleshooting & Remediation
* **Endpoint Boundary Test:** Direct unauthenticated requests return `PublicAccessNotPermitted` (`../07-direct-url-access-denied.png`).
* **Time Synchronization:** Time zone mismatches caused initial `AuthenticationFailed` errors (`../08-sas-url-initially-denied.png`), resolved by synchronizing policy timeframes (`../09-sas-url-access-granted-after-time-fix.png`).
* **Verification:** Successful retrieval is confirmed (`../10-sas-url-access-granted.png`), with automated lifecycle rules applied (`../11-lifecycle-management-rule.png`).

---

## 🧠 Core Competencies Proven
1. Least Privilege Principle implementation.
2. Azure REST API XML error syntax analysis.
3. Automated compliance lifecycle controls.
