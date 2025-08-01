---
title: Support matrix for Azure Blobs backup
description: Provides a summary of support settings and limitations when backing up Azure Blobs.
ms.topic: reference
ms.date: 07/02/2025
ms.custom: references_regions, engagement-fy24
ms.service: azure-backup
author: jyothisuri
ms.author: jsuri
# Customer intent: "As a cloud administrator, I want to understand the support matrix for backing up Azure Blobs so that I can ensure compliance with regional limitations and operational requirements when implementing backup solutions."
---

# Support matrix for Azure Blobs backup

This article summarizes the regional availability, supported scenarios, and limitations of operational and vaulted backups of blobs.

## Supported regions

**Choose a backup type**

# [Operational backup](#tab/operational-backup)

Operational backup for blobs is available in all public cloud regions, except France South and South Africa West. It's also available in sovereign cloud regions - all Azure Government regions and China regions (except China East).

# [Vaulted backup](#tab/vaulted-backup)

Vaulted backup for blobs is available in all public cloud regions.


---

## Supported and unsupported scenarios for Azure Blob backup

**Choose a backup type**

# [Operational backup](#tab/operational-backup)

Operational backup of blobs uses blob point-in-time restore, blob versioning, soft delete for blobs, change feed for blobs and delete lock to provide a local backup solution. Hence, the limitations that apply to these capabilities also apply to operational backup.

**Supported scenarios**:

- Operational backup supports block blobs in standard general-purpose v2 storage accounts only. Storage accounts with hierarchical namespace enabled (that is, ADLS Gen2 accounts) aren't supported.   <br><br>   Also, any page blobs, append blobs, and premium blobs in your storage account won't be restored and only block blobs will be restored.

- Blob backup is also supported when the storage account has private endpoints.

**Other limitations**:

- If you've deleted a container during the retention period, that container won't be restored with the point-in-time restore operation. If you attempt to restore a range of blobs that includes blobs in a deleted container, the point-in-time restore operation will fail. For more information about protecting containers from deletion, see [Soft delete for containers](../storage/blobs/soft-delete-container-overview.md).
- Containers with **legal hold** enabled aren't supported.
- If a blob has moved between the hot and cool tiers in the period between the present moment and the restore point, the blob is restored to its previous tier. Restoring block blobs in the archive tier isn't supported. For example, if a blob in the hot tier was moved to the archive tier two days ago, and a restore operation restores to a point three days ago, the blob isn't restored to the hot tier. To restore an archived blob, first move it out of the archive tier. For more information, see [Rehydrate blob data from the archive tier](../storage/blobs/archive-rehydrate-overview.md).
- A block that has been uploaded via [Put Block](/rest/api/storageservices/put-block) or [Put Block from URL](/rest/api/storageservices/put-block-from-url), but not committed via [`Put Block List`](/rest/api/storageservices/put-block-list), isn't part of a blob and so isn't restored as part of a restore operation.
- A blob with an active lease can't be restored. If a blob with an active lease is included in the range of blobs to restore, the restore operation will fail automatically. Break any active leases before starting the restore operation.
- Snapshots aren't created or deleted as part of a restore operation. Only the base blob is restored to its previous state.
- If there are [immutable blobs](../storage/blobs/immutable-storage-overview.md#about-immutable-storage-for-blobs) among those being restored, such immutable blobs won't be restored to their state as per the selected recovery point. However, other blobs that don't have immutability enabled will be restored to the selected recovery point as expected.


# [Vaulted backup](#tab/vaulted-backup)

- You can back up only block blobs in a *standard general-purpose v2 storage account* using the vaulted backup solution for blobs.
- Blob vaulted backup is also supported when the storage account has private endpoints.
- HNS-enabled storage accounts are currently not supported. This includes *ADLS Gen2 accounts*, *accounts using NFS 3.0*, and *SFTP protocols* for blobs.
- You can take up to five backups per storage account in a day.
- You can back up storage accounts with *up to 100 containers*, there is no limit on the number of blobs within those containers. You can also select a subset of containers to back up (up to 100 containers).
  - If your storage account contains more than 100 containers, you need to select *up to 100 containers* to back up.
  - To back up any new containers that get created after backup configuration for the storage account, modify the protection of the storage account. These containers aren't backed up automatically.
- The storage accounts to be backed up must contain *a minimum of one container*. If the storage account doesn't contain any containers or if no containers are selected, an error may appear when you configure backup.
- Only `$web` and `$root` system containers are supported for vaulted backup.
- If you stop protection (vaulted backup) on a storage account, it doesn't delete the object replication policy created on the storage account. In these scenarios, you need to manually delete the *OR policies*.
- Archive tier blob backup isn't supported. Cool and cold tier blobs are restored in hot tier. 
- The backup operation isn't supported for blobs that are uploaded by using [Data Lake Storage APIs](/rest/api/storageservices/data-lake-storage-gen2).
- When you delete and recreate a storage account with the same name, **Object Replication** doesn't recognize the change. As a result, future Recovery Points continue to include the older blobs and their versions.
- Similarly, if you delete and recreate a container with the same name, **Object Replication** doesn't track the change, and future Recovery Points still include the previous blobs and versions.
- If you suspend and resume protection or delete the **Object Replication policy** on the **source storage account**, the policy triggers a full backup.
- Backup vaults with User-Assigned Managed Identity (UAMI) aren't compatible with Azure Blob Vaulted backups. Only System-Assigned Managed Identity (SAMI) works, because the vault needs to access the storage account where the blobs are stored. The vault uses its system-assigned managed identity for this access.

- Enabling backups isn't supported for the blob container that are configured with native replication using data factory.
- The protection of  a container that is part of any object replication isn't supported, either as a source or destination. Attempting to back up such a container will result in backup failure.
- Containers with **legal hold** enabled aren't supported.
 

---

## Next steps

[Overview of Azure Blobs backup for Azure Blobs](blob-backup-overview.md)

## Related content

- [Create a backup policy for  Azure Blob using REST API](backup-azure-dataprotection-use-rest-api-create-update-blob-policy.md).
- [Back up Azure Blob using REST API](backup-azure-dataprotection-use-rest-api-backup-blobs.md).
- [Restore Azure Blob using REST API](backup-azure-dataprotection-use-rest-api-restore-blobs.md).

