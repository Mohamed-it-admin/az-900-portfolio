# Lab 05 — Secure File Sharing

Hands-on Microsoft Azure lab demonstrating private file sharing using **Azure Blob Storage**, a **stored access policy**, a **read-only time-limited SAS**, and **lifecycle management**.

## Objective

Share a file with an external partner without enabling anonymous public access or sharing the storage account's access keys.

## What I Built

* Created a **Standard LRS Azure Storage account**
* Created a private Blob Storage container: `partner-drop`
* Uploaded a sample file: `monthly-report.txt`
* Created a stored access policy: `partner-read-policy`
* Generated a read-only, time-limited SAS for the file
* Verified that direct unauthenticated access was blocked
* Added a lifecycle management rule to automatically delete blobs after 30 days

## Troubleshooting

The SAS URL initially returned an `AuthenticationFailed` error.

I checked the stored access policy and found that I had entered the validity time incorrectly. After correcting the policy's time window and generating the SAS again, the file became accessible.

## Security

* Anonymous/public access was disabled.
* The shared access was read-only and time-limited.
* The storage account's access keys were not shared with the external partner.
* A stored access policy was used to manage the SAS access.
* Lifecycle management was configured to automate cleanup.

## Production Perspective

This was a hands-on training lab rather than a production implementation. In a production environment, SAS generation, secret management, monitoring, and storage redundancy would be designed according to the application's security and business requirements.

## Case Study

**[View the full Lab 05 case study (PDF)](Lab-05-Secure-File-Sharing.pdf)**
