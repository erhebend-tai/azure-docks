---
title: Resource limits for Azure NetApp Files
description: Describes limits for Azure NetApp Files resources and how to request resource limit increase.
services: azure-netapp-files
author: b-hchen
ms.service: azure-netapp-files
ms.topic: concept-article
ms.date: 06/10/2025
ms.author: anfdocs
# Customer intent: As an IT administrator managing Azure NetApp Files, I want to understand the resource limits and how to request limit increases, so that I can effectively plan and allocate storage resources for my organization’s needs.
---
# Resource limits for Azure NetApp Files

Understanding resource limits for Azure NetApp Files helps you manage your volumes.

## Resource limits

The following table describes resource limits for Azure NetApp Files:

|  Resource  |  Default limit  |  Adjustable via support request  |
|----------------|---------------------|--------------------------------------|
|  [Regional capacity quota per subscription](regional-capacity-quota.md)   |  25 TiB  |  Yes  |
|  Number of NetApp accounts per Azure region per subscription  |  10    |  Yes   |
|  Number of capacity pools per NetApp account   |    25     |   Yes   |
|  Number of volumes per subscription   |    500     |   Yes   |
|  Number of volumes per capacity pool     |    500   |    Yes     |
|  Number of snapshots per volume       |    255     |    No        |
|  Number of IPs in a virtual network (including immediately peered virtual networks [VNets]) accessing volumes in an Azure NetApp Files hosting VNet    |   <ul><li>**Basic**: 1000</li><li>**Standard**: [Same standard limits as VMs](../azure-resource-manager/management/azure-subscription-service-limits.md#azure-resource-manager-virtual-networking-limits)</li></ul>  |    No    |
|  Minimum size of a single capacity pool   |  1 TiB*     |    No  |
|  Maximum size of a single capacity pool    |  2,048 TiB   |   No   |
| Minimum throughput of a Flexible service level capacity pool | 128 MiB/second | No |
| Maximum throughput of a Flexible service level capacity pool | [5 x 128 MiB/second/TiB x Size of capacity pool in TiB](azure-netapp-files-set-up-capacity-pool.md#considerations) | No |
|  Minimum size of a single regular volume    |    50 GiB    |    No    |
|  Maximum size of a single regular volume     |    100 TiB    |    No    |
|  Minimum size of a single [large volume](large-volumes-requirements-considerations.md) | 50 TiB |     No |
| Large volume size increase | 30% of lowest provisioned size | Yes |
|  Maximum size of a single [large volume](large-volumes-requirements-considerations.md)    | 1 PiB |    Yes**    |
| Maximum size of a single large volume on dedicated capacity (preview) | 2 PiB | No |
|  Maximum size of a single file     |    16 TiB    |    No    |    
|  Maximum size of directory metadata in a single directory      |    320 MB    |    No    |    
|  Maximum number of files in a single directory  | *Approximately* 4 million. <br> See [Determine if a directory is approaching the limit size](directory-sizes-concept.md#directory-limit).  |    No    |   
|  Maximum number of `maxfiles` per volume | See [`maxfiles`](maxfiles-concept.md)  | Yes |    
|  Maximum number of export policy rules per volume     |    5  |    No    | 
|  Maximum number of quota rules per volume     |   1,000  |    No    | 
|  Minimum assigned throughput for a manual Quality of Service (QoS) volume     |    1 MiB/s   |    No    |    
|  Maximum assigned throughput for a manual QoS volume     |    4,500 MiB/s    |    No    |    
|  Number of cross-region replication data protection volumes (destination volumes)     |    500    |    Yes    |     
|  Number of cross-zone replication data protection volumes (destination volumes)     |    500    |    Yes    |     
|  Maximum numbers of policy-based (scheduled) backups per volume  | <ul><li> Daily retention count: 2 (minimum) to 1019 (maximum) </li> <li> Weekly retention count: 0 (minimum) to 1019 (maximum) </li> <li> Monthly retention count: 0 (minimum) to 1019 (maximum) </ol></li> <br> The maximum hourly, daily, weekly, and monthly backup retention counts *combined* is 1019.  |  No  |
|  Maximum size of protected volume  |  100 TiB  |  No  |
|  Maximum number of volumes that can be backed up per subscription   |  500  |  No  |
|  Maximum number of manual backups per volume per day |  5  |  No  |
|  Maximum number of volumes supported for cool access per subscription per region |  500  |  Yes  |


\* [!INCLUDE [Limitations for capacity pool minimum of 1 TiB](includes/2-tib-capacity-pool.md)]

\** 2-PiB [large volume](large-volumes-requirements-considerations.md) large volumes are available on request depending on regional dedicated capacity availability. To request 2-PiB large volumes, contact your account team. 

For more information, see [Capacity management FAQs](faq-capacity-management.md).

For limits and constraints related to Azure NetApp Files network features, see [Guidelines for Azure NetApp Files network planning](azure-netapp-files-network-topologies.md#considerations).

## Request limit increase

You can create an Azure support request to increase the adjustable limits from the [Resource Limits](#resource-limits) table. 

>[!NOTE]
> Depending on available resources in the region and the limit increase requested, Azure support may require additional information in order to determine the feasibility of the request.

1. Navigate to **Help** then **Support + troubleshooting**.   
1. Under the **How can we help you** heading, enter "regional capacity quota" in the text field then select **Go**. 

    ![Screenshot that shows the How can we help heading.](./media/azure-netapp-files-resource-limits/support-how-can-we-help.png)
    
1. Under the **Current selection** heading, search for "Service and subscription limits (Quotas)" in the text field for **Which service are you having an issue with?**.
    1. Select **Service and subscription limits (Quotas)** then select **Next**. 

1. Select **Create a support request**. 
    1. For **Issue type**, select **Service and Subscription Limits (Quotas)**.
    2. For **Subscription**, select your subscription. 
    3. For **Quota type**, select **Storage: Azure NetApp Files limits**.
    4. Select **Next**.

    ![Screenshot that shows the Problem Description tab.](./media/shared/support-problem-descriptions.png)
    
1. Under the **Additional details** tab, select **Enter details** in the Request Details field.  

    ![Screenshot that shows the Details tab and the Enter Details field.](./media/shared/quota-additional-details.png)

1. To request limit increase, provide the following information in the Quota details window that appears:
    1. For **Quota type**, search and select **Regional Capacity Quota per Subscription (TiB)**. 
    2. For **Region requested**, select your region.   
    3. For **Quota State**, enter the new request value for the quota type you specified.
    4. Select **Save and continue**. 
    
    ![Screenshot that shows how to display and request increase for regional quota.](./media/azure-netapp-files-resource-limits/quota-details-regional-request.png)

1. Enter the support preference details in the New support request window that appears and select **Next**.
2. Review the details and select **Create** to create the request.

>[!NOTE]
> After the regional capacity quota limit has been increased, perform the capacity pool create and resize operation.

## Next steps  

- [Understand `maxfiles` limits](maxfiles-concept.md)
- [Understand maximum directory sizes](directory-sizes-concept.md)
- [Understand the storage hierarchy of Azure NetApp Files](azure-netapp-files-understand-storage-hierarchy.md)
- [Requirements and considerations for large volumes](large-volumes-requirements-considerations.md)
- [Cost model for Azure NetApp Files](azure-netapp-files-cost-model.md)
- [Regional capacity quota for Azure NetApp Files](regional-capacity-quota.md)
- [Request region access for Azure NetApp Files](request-region-access.md)
- [Application resilience FAQs for Azure NetApp Files](faq-application-resilience.md)
