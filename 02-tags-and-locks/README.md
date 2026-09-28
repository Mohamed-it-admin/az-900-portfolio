# Lab 02 — Tags and Resource Locks

Hands-on Azure lab covering resource tagging, resource locks, lock enforcement, and access restoration.

## What I did

* Created a resource group and two Azure Storage accounts
* Applied organizational tags to the resource group and storage accounts
* Used different department tags to organize resources
* Filtered resources by tag
* Created a **Delete** lock on a storage account
* Created a **Read-only** lock on the resource group
* Tested the locks by attempting blocked operations
* Removed the locks
* Verified that normal write operations were restored

## Resources

* Resource group: `rg-gp-tags-locks`
* Storage account: `stgptagslock65624538`
* Storage account: `stgptagsops65624538`

## Tags

### Resource group

* `department = development`
* `environment = test`

### First storage account

* `department = development`
* `environment = test`

### Second storage account

* `department = operations`
* `environment = test`

## Resource Locks

### Storage account

* Lock: `prevent-delete`
* Type: **Delete**

### Resource group

* Lock: `read-only-rg`
* Type: **Read-only**

The locks were tested during the lab. The Read-only lock blocked changes to the resource group, while the Delete lock prevented the storage account from being deleted.

The locks were then removed and normal write access was verified.

## What I learned

This lab gave me hands-on practice with Azure tags and resource locks. I learned how tags can be used to organize and filter resources and how locks can prevent accidental changes or deletion.

## Evidence

[View the Lab 02 case study (PDF)](Lab-02-Tags-and-Locks.pdf)

Screenshots from the lab are included in the `screenshots` folder.
