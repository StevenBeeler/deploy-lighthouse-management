# GK Azure Lighthouse onboarding templates
The provided ARM-templates will onboard your subscriptions to GK Azure Lighthouse Management. Your GK contact person will provide you with the required information (managedByTenantId, OwnerPrincipalID)

## Onboard GK to your subscription with Contributor Role
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FStevenBeeler%2Fdeploy-lighthouse-management%2Fmain%2Fgk-lighthouse-subscription-onboarding.json)

## Template Features

### Azure Lighthouse Onboarding
This template onboards your subscription to Azure Lighthouse, granting the following role to GK:
- Contributor - For general management of resources
- Managed Services Registration Assignment Delete Role - For offboarding the management

### What This Deployment Creates
When you deploy this template, it will:

- Register your subscription with Azure Lighthouse for GK management after the managed identity is configured


## Parameters

| Parameter Name | Description |
|---------------|------------|
| managedByTenantId | GK's Tenant ID (provided by GK) |
| OwnerPrincipalID | Object ID of GK's Contributor Group (provided by GK) |

## Fixed Values (Not Configurable)

The following values are fixed in the template and cannot be changed:

| Name | Value |
|---------------|------------|
| mspOfferName | glueckkanja Managed Services - Access privilege - v1.0 |
| mspOfferDescription | The solution will grant glueckkanja AG the required Azure RBAC roles for managing Microsoft Ressources in your environment. |

## Prerequisites

To successfully deploy this template, the following prerequisites must be met:

### Required Roles
The user deploying this template must have the following roles:

- **Owner** or **User Access Administrator** at the subscription scope
  - Required to register the subscription with Azure Lighthouse

### Required Information
- GK's Tenant ID (provided by your GK contact)
- GK's Contributor Group Object ID (provided by your GK contact)

### Deployment Process
1. Click the "Deploy to Azure" button above
2. Fill in the required parameters with the values provided by GK
3. Review and create the deployment