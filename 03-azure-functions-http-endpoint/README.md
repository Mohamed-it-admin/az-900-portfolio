# Lab 03 — Azure Functions HTTP Endpoint

Hands-on Azure lab covering Azure Functions, serverless hosting, HTTP triggers, function authorization, and Application Insights monitoring.

## What I did

* Created an Azure Function App using **Flex Consumption**
* Configured a Node.js 22 LTS runtime
* Enabled Application Insights monitoring
* Created a Node.js HTTP-triggered function named `GetStatus`
* Deployed the function using Azure Cloud Shell and Azure Functions Core Tools
* Tested the HTTP endpoint
* Changed the function authorization from anonymous to function-level access
* Verified that unauthenticated requests returned `401 Unauthorized`
* Tested authenticated access using a function key
* Reviewed function invocation telemetry in Application Insights
* Cleaned up the Azure resources after completing the lab

## Resources

* Resource group: `rg-gp-functions-endpoint`
* Function App: `func-gp-endpoint-65635750`
* Function: `GetStatus`
* Region: North Europe
* Hosting: Flex Consumption
* Runtime: Node.js 22 LTS

## Technologies

* Microsoft Azure
* Azure Functions
* Flex Consumption
* Azure Cloud Shell
* Azure Functions Core Tools
* Node.js
* Application Insights

## What I learned

This lab gave me hands-on practice with deploying a serverless HTTP function in Azure. I also practiced changing function authorization, testing HTTP responses, and using Application Insights to review function execution telemetry.

## Evidence

[View the Lab 03 case study (PDF)](Lab-03-Azure-Functions-HTTP-Endpoint.pdf)

Screenshots from the lab are included in the `screenshots` folder.
