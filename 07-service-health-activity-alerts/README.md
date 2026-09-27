# Lab 7 — Service Health and Activity Log Alerts

Hands-on Azure lab covering Azure Monitor, Service Health, Action Groups, and Activity Log alerts.

## What I did

* Created an email action group for operations notifications
* Tested the action group and confirmed the notification test succeeded
* Reviewed Azure Service Health information
* Created a Service Health alert for service issues and planned maintenance
* Created an Activity Log alert for resource group deletion events
* Reviewed both alert rules and their configurations

## Resources

* Resource group: `rg-gp-monitoring-alerts`
* Action group: `ag-gp-ops-email`
* Service Health alert: `ar-gp-service-health`
* Activity Log alert: `ar-gp-activity-delete`

## Alerts

### Service Health

The Service Health alert monitors:

* Service issues
* Planned maintenance

The alert uses the `ag-gp-ops-email` action group and is enabled.

### Activity Log

The Activity Log alert monitors the `Delete resource group` event.

* Severity: `Sev 2 - Warning`
* Action group: `ag-gp-ops-email`
* Alert: `ar-gp-activity-delete`
* Enabled: Yes

## What I learned

This lab gave me practical experience with Azure Monitor alerts, action groups, Service Health, and Activity Log events. I also learned how alerts can notify an operations team about Azure platform issues and important resource management events.

## Evidence

[View the Lab 7 case study (PDF)](Lab-07-Service-Health-Activity-Alerts.pdf)
