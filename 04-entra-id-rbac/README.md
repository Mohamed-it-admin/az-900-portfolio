# Lab 04 — Entra ID and RBAC

Hands-on Azure lab covering Microsoft Entra ID, security groups, Azure RBAC, role assignment scope, access verification, and least-privilege permissions.

## What I did

* Created an Azure resource group and test storage account
* Created a Microsoft Entra ID security group
* Added a test user to the security group
* Assigned the **Reader** role to the security group
* Applied the role assignment at the resource group scope
* Used **Check access** to verify inherited permissions
* Reviewed the Azure Activity Log for the role assignment
* Signed in as the test user to verify read access
* Tested resource creation and confirmed it was denied with Reader permissions

## Resources

* Resource group: `rg-gp-access-model`
* Storage account: `stgpaccessmodel65680763`
* Security group: `gp-rg-readers65680763`
* RBAC role: **Reader**
* Scope: Resource group

## Access Model

The Reader role was assigned to the security group rather than directly to the user.

This allowed the test user to inherit read permissions through group membership while preventing resource creation or modification.

## What I learned

This lab gave me hands-on practice with Microsoft Entra ID groups and Azure RBAC. I learned how role assignments can be applied at a specific scope and how group-based access can be verified using Check access and the Activity Log.

I also tested the resulting permissions by signing in as the test user and confirming that read access worked while resource creation was denied.

## Evidence

[View the Lab 04 case study (PDF)](Lab-04-Entra-ID-and-RBAC.pdf)

Screenshots from the lab are included in the `screenshots` folder.
