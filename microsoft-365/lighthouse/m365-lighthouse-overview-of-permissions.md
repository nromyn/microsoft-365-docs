---
title: "Overview of permissions in Microsoft 365 Lighthouse"
f1.keywords: CSH
ms.author: sharik
author: SKjerland
manager: scotv
ms.reviewer: taylorau
ms.date: 06/10/2024
audience: Admin
ms.topic: concept-article
ms.service: microsoft-365-lighthouse
ms.localizationpriority: medium
ms.collection:
- Tier1
- scotvorg
- M365-subscription-management
- Adm_O365
- essentials-get-started
ms.custom:
- AdminSurgePortfolib
- M365-Lighthouse                         
search.appverid: MET150
description: "For Managed Service Providers (MSPs) using Microsoft 365 Lighthouse, learn more about Lighthouse permission requirements."
---

# Overview of permissions in Microsoft 365 Lighthouse

Microsoft 365 Lighthouse permissions are primarily managed by the following:

- Lighthouse role-based access control (RBAC) in the partner tenant
- Granular delegated administrative privileges (GDAP) in the customer tenant

To use Lighthouse, you need a combination of roles assigned via RBAC and GDAP.

## Global Administrator permissions in the partner tenant

Partner tenant users assigned the Global Administrator role in Microsoft Entra ID can do the following:

- Sign up for Lighthouse in the Microsoft 365 admin center. 
- Activate and inactive a tenant. 
- Create, update, and delete tags.
- Assign tags to and remove tags from a customer tenant. 
- Review audit logs. 
- Create, edit, and view alert rules.

## Managing Lighthouse RBAC permissions in the partner tenant

Lighthouse permissions in the partner tenant are managed by assigning RBAC roles. Each role has a set of permissions that determines which data users can access and change within the partner tenant.  

RBAC roles are managed from the Lighthouse permissions page in Lighthouse. To access the Lighthouse permissions page and manage permissions, you must be a Global Administrator in Microsoft Entra ID. To learn more, see [Manage Lighthouse RBAC permissions in Microsoft 365 Lighthouse](m365-lighthouse-manage-lighthouse-rbac-permissions.md).

There's currently only one Lighthouse RBAC role: Lighthouse Account Manager. The following table describes the Lighthouse Account Manager role.

| Lighthouse&nbsp;RBAC&nbsp;role | Description |
|---|---|
| Lighthouse Account Manager | Provides full access to Sales Advisor pages and data across the entire partner tenant. Lighthouse Account Managers can export Sales Advisor data. |

## Lighthouse RBAC roles and capabilities

The following table describes the actions that Lighthouse Account Managers can perform in Lighthouse.

| Area | Actions | Lighthouse&nbsp;Account&nbsp;Manager |
|---|---|:---:|
| **Tenants** | View the Tenants page | &check; |
|  | Manage tags |  |
|  | Activate and inactivate a tenant |  |
|  | View delegated status | &check; |
|  | View baseline assignment |  |
|  | View deployment status | &check; |
|  | View and edit customer contact information and website | &check; |
| **Baselines** | View baselines (default, custom) |  |
|  | Create, edit, and assign baselines |  |
| **Alerts** | View alerts | &check; |
|  | Manage alerts (change severity, status, or assignment) |  |
|  | Create, edit, and delete alert rules |  |
| **Permissions** | Set up and manage Lighthouse permissions |  |
|  | Set up and manage GDAP |  |
|  | View GDAP status detail |  |
| **Audit logs** | View audit logs |  |
| **Sales Advisor** | View Sales Advisor reports and manage data | &check; |
| **Support** | Open and manage service requests |  |
| **Service&nbsp;health** | Monitor service health |  |

## Managing GDAP in the customer tenant

GDAP gives you a high level of control and flexibility by providing access to customer tenants through [Microsoft Entra built-in roles](/azure/active-directory/roles/permissions-reference). Assigning the least-privileged roles by task through GDAP to MSP technicians reduces security risk for both MSPs and customers.  

For more information about setting up a GDAP relationship with a customer tenant in Lighthouse, see [Obtain granular admin permissions to manage a customer's service - Partner Center](/partner-center/gdap-obtain-admin-permissions-to-manage-customer).   

For more information about least-privileged roles by task, see [Least-privileged roles - Partner Center](/partner-center/gdap-least-privileged-roles-by-task) and [Least privileged roles by task in Microsoft Entra ID](/azure/active-directory/roles/delegate-by-task).  

For more information about GDAP or delegated administrative privileges (DAP) deprecation, see [GDAP frequently asked questions - Partner Center](/partner-center/gdap-faq), or search the [Partner Center announcements](/partner-center/announcements/) for dates and timelines.

The following tasks in Lighthouse have specific Microsoft Entra role requirements:

- To create and manage service requests, Lighthouse users must have at least one Microsoft Entra role assigned to them with the following property set: **microsoft.office365.supportTickets/allEntities/allTasks**. 

- To monitor service health, Lighthouse users must have at least one Microsoft Entra role assigned to them with the following property set: **microsoft.office365.serviceHealth/allEntities/allTasks**. 

For a complete list of Microsoft Entra roles, see [Microsoft Entra built-in roles](/azure/active-directory/roles/permissions-reference). For information on how to assign roles, see [Assign Microsoft Entra roles to users](/azure/active-directory/roles/manage-roles-portal).

## Related content

[Requirements for Microsoft 365 Lighthouse](m365-lighthouse-requirements.md) (article)  
[View your Microsoft Entra roles in Microsoft 365 Lighthouse](m365-lighthouse-view-your-roles.md) (article)  
[Assign roles and permissions to users - Partner Center](/partner-center/permissions-overview) (article)  
[Overview of Microsoft 365 Lighthouse](m365-lighthouse-overview.md) (article)  
[Sign up for Microsoft 365 Lighthouse](m365-lighthouse-sign-up.md) (article)  
[Microsoft 365 Lighthouse FAQ](m365-lighthouse-faq.yml) (article)
