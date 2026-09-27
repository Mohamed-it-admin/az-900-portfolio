# Lab 6 — Cost Guardrails

Hands-on Azure lab covering resource tags, cost alerts, and Azure Policy.

## What I did

* Created a resource group and storage account
* Added cost-tracking tags
* Created a monthly budget with 80% and 100% alerts
* Assigned the **Allowed locations** policy
* Tested Azure Policy and investigated a deployment issue

## Resources

* Resource group: `rg-gp-cost-guardrails`
* Storage account: `stgpcostguard65579770`
* Region: North Europe
* Storage: Standard LRS
* Budget: `gp-pilot-budget`

## Tags

* `environment = pilot`
* `owner = it-team`

## Policy

I assigned the built-in **Allowed locations** policy and configured **North Europe** as the allowed location.

The existing lab storage account was compliant.

During the temporary storage-account test, the deployment was also affected by a pre-existing lab policy named **AZ-900T00-A: Lab 06**, which restricted the storage account naming pattern. Because of this lab-environment restriction, I could not complete the temporary test exactly as described in the instructions.

I did not modify the pre-existing lab policy.

## What I learned

This lab gave me practice with Azure cost management, resource tagging, budgets, and Azure Policy. I also learned that multiple policies can affect the same resource deployment and that the error message needs to be checked to identify which policy is blocking the deployment.

## Evidence

[View the Lab 6 case study (PDF)](Lab-06-Cost-Guardrails.pdf)
