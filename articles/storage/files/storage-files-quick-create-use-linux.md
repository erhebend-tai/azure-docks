---
title: Create an NFS Azure File Share
description: This article covers how to use the Azure portal to deploy a Linux virtual machine (VM), create an Azure file share using the NFS protocol, and mount the file share.
author: khdownie
ms.service: azure-file-storage
ms.custom: linux-related-content
ms.topic: tutorial
ms.date: 07/01/2025
ms.author: kendownie
# Customer intent: "As an IT admin evaluating Azure Files, I want to create an NFS file share and mount it on a Linux VM, so that I can assess its performance and integration with my existing workflows."
---

# Create an NFS Azure file share using the Azure portal

Azure Files offers fully managed file shares in the cloud that are accessible via the industry standard [Server Message Block (SMB) protocol](/windows/win32/fileio/microsoft-smb-protocol-and-cifs-protocol-overview) or [Network File System (NFS) protocol](https://en.wikipedia.org/wiki/Network_File_System). Both NFS and SMB protocols are supported on Azure virtual machines (VMs) running Linux. This article shows you how to create an Azure file share using the NFS protocol and connect it to a Linux VM.

## Applies to
| Management model | Billing model | Media tier | Redundancy | SMB | NFS |
|-|-|-|-|:-:|:-:|
| Microsoft.Storage | Provisioned v2 | HDD (standard) | Local (LRS) | ![No](../media/icons/no-icon.png) | ![No](../media/icons/no-icon.png) |
| Microsoft.Storage | Provisioned v2 | HDD (standard) | Zone (ZRS) | ![No](../media/icons/no-icon.png) | ![No](../media/icons/no-icon.png) |
| Microsoft.Storage | Provisioned v2 | HDD (standard) | Geo (GRS) | ![No](../media/icons/no-icon.png) | ![No](../media/icons/no-icon.png) |
| Microsoft.Storage | Provisioned v2 | HDD (standard) | GeoZone (GZRS) | ![No](../media/icons/no-icon.png) | ![No](../media/icons/no-icon.png) |
| Microsoft.Storage | Provisioned v1 | SSD (premium) | Local (LRS) | ![No](../media/icons/no-icon.png) | ![Yes](../media/icons/yes-icon.png) |
| Microsoft.Storage | Provisioned v1 | SSD (premium) | Zone (ZRS) | ![No](../media/icons/no-icon.png) | ![Yes](../media/icons/yes-icon.png) |
| Microsoft.Storage | Pay-as-you-go | HDD (standard) | Local (LRS) | ![No](../media/icons/no-icon.png) | ![No](../media/icons/no-icon.png) |
| Microsoft.Storage | Pay-as-you-go | HDD (standard) | Zone (ZRS) | ![No](../media/icons/no-icon.png) | ![No](../media/icons/no-icon.png) |
| Microsoft.Storage | Pay-as-you-go | HDD (standard) | Geo (GRS) | ![No](../media/icons/no-icon.png) | ![No](../media/icons/no-icon.png) |
| Microsoft.Storage | Pay-as-you-go | HDD (standard) | GeoZone (GZRS) | ![No](../media/icons/no-icon.png) | ![No](../media/icons/no-icon.png) |

## Getting started

If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.

Sign in to the [Azure portal](https://portal.azure.com).

### Create a storage account

Before you can work with an NFS file share, you have to create a storage account for SSD file shares.

1. On the Azure portal menu, select **All services**. In the list of resources, type **Storage Accounts**. As you begin typing, the list filters based on your input. Select **Storage Accounts**.
1. On the **Storage Accounts** window that appears, choose **+ Create**.
1. Under **Project details**, select the subscription in which to create the storage account.
1. Under the **Resource group** field, select **Create new** to create a new resource group. Or you can choose an existing resource group.
1. Under **Instance details**, enter a name for your storage account. The name must be unique across Azure. The name also must be between 3 and 24 characters in length, and may include only numbers and lowercase letters.
1. Select a region for your storage account, or use the default region. Azure supports NFS file shares in all the same [regions that support SSD file shares](redundancy-premium-file-shares.md).
1. Under **Primary service**, select **Azure Files**.
1. Select the *Premium* performance tier to store your data on solid-state drives (SSD). This is required for NFS file shares.
1. Under **File share billing**, leave the default of *Provisioned v1* selected. This is currently the only option available for NFS file shares.
1. Under **Redundancy**, select *Locally redundant storage (LRS)*.
1. Select **Review + Create** to review your storage account settings and create the account.
1. When you see the **Validation passed** notification appear, select **Create**. You should see a notification that deployment is in progress.

The following image shows the settings on the **Basics** tab for a new storage account:

:::image type="content" source="media/storage-files-quick-create-use-linux/create-storage-account.png" alt-text="Screenshot showing how to create a storage account using the Azure portal." lightbox="media/storage-files-quick-create-use-linux/create-storage-account.png":::

## Deploy an Azure VM running Linux

Next, create an Azure VM running Linux to represent the on-premises server. When you create the VM, a virtual network will be created for you. The NFS protocol can only be used from a machine inside of a virtual network.

1. Select **Home**, and then select **Virtual machines** under **Azure services**.

1. Select **+ Create** and then **Azure virtual machine**.

1. In the **Basics** tab, under **Project details**, make sure the correct subscription and resource group are selected. Under **Instance details**, type *myVM* for the **Virtual machine name**, and select the same region as your storage account.

1. Under **Availability options**, select *No infrastructure redundancy required*. Under **Security type**, select *Standard*.

1. Choose your Linux distribution for your **Image**. Leave the other defaults. The default size and pricing is only shown as an example. Size availability and pricing are dependent on your region and subscription.

    :::image type="content" source="media/storage-files-quick-create-use-linux/vm-project-instance-details.png" alt-text="Screenshot showing how to enter the project and instance details to create a new V M." lightbox="media/storage-files-quick-create-use-linux/vm-project-instance-details.png" border="true":::

1. Under **Administrator account**, select **SSH public key**. Leave the rest of the defaults.

    :::image type="content" source="media/storage-files-quick-create-use-linux/vm-admin-account.png" alt-text="Screenshot showing how to configure the administrator account and create an S S H key pair for a new V M." lightbox="media/storage-files-quick-create-use-linux/vm-admin-account.png" border="true":::

1. Under **Inbound port rules > Public inbound ports**, choose **Allow selected ports** and then select **SSH (22)** and **HTTP (80)** from the drop-down.

    :::image type="content" source="media/storage-files-quick-create-use-linux/create-vm-inbound-port-rules.png" alt-text="Screenshot showing how to configure the inbound port rules for a new V M." lightbox="media/storage-files-quick-create-use-linux/create-vm-inbound-port-rules.png" border="true":::

   > [!IMPORTANT]
   > Setting SSH port(s) open to the internet is only recommended for testing. If you want to change this setting later, go back to the **Basics** tab.

1. Select the **Review + create** button at the bottom of the page.

1. On the **Create a virtual machine** page, you can see the details about the VM you're about to create. Under **Networking**, note the name of the virtual network. When you're ready, select **Create**.

1. When the **Generate new key pair** window opens, select **Download private key and create resource**. Your key file will be downloaded as **myVM_key.pem**. Make sure you know where the .pem file was downloaded, because you'll need the path to it to connect to your VM.

You'll see a message that deployment is in progress. Wait a few minutes for deployment to complete.

## Create an NFS Azure file share

Now you're ready to create an NFS file share and provide network-level security for your NFS traffic.

### Add a file share to your storage account

1. Select **Home** and then **Storage accounts**.

1. Select the storage account you created.

1. In the service menu, under **Data storage**, select **File shares**.

1. Select **+ File Share**.

1. Name the new file share *qsfileshare* and enter "100" for the minimum **Provisioned capacity**, or provision more capacity (up to 102,400 GiB) to get more performance. Select **NFS** protocol and choose a **Root Squash** setting. To learn more about root squash and its security benefits for NFS file shares, see [Configure root squash for Azure Files](nfs-root-squash.md).

1. Select **Review + create**. When you see the **Validation passed** notification appear, select **Create**.

    :::image type="content" source="media/storage-files-quick-create-use-linux/create-nfs-file-share.png" alt-text="Screenshot showing how to name the file share and provision capacity to create a new N F S file share." lightbox="media/storage-files-quick-create-use-linux/create-nfs-file-share.png" border="true":::

### Set up a private endpoint or service endpoint

Next, set up a private endpoint for your storage account. This gives your storage account a private IP address from within the address space of your virtual network. Standard [data processing rates](https://azure.microsoft.com/pricing/details/private-link/) for private endpoints apply. If you don't require a static IP address, you can use a service endpoint instead. There's no extra charge for using service endpoints.

1. Select the file share *qsfileshare*. You should see a dialog that says *Connect to this NFS share from Linux*. Under **Network configuration**, select **Review options**

    :::image type="content" source="media/storage-files-quick-create-use-linux/connect-from-linux.png" alt-text="Screenshot showing how to configure network settings to connect to the N F S share from Linux." lightbox="media/storage-files-quick-create-use-linux/connect-from-linux.png" border="true":::

1. Next, select **Setup a private endpoint**.

    :::image type="content" source="media/storage-files-quick-create-use-linux/configure-network-security.png" alt-text="Screenshot showing network-level security configurations." lightbox="media/storage-files-quick-create-use-linux/configure-network-security.png" border="true":::

1. Select **+ Private endpoint**.

    :::image type="content" source="media/storage-files-quick-create-use-linux/create-private-endpoint.png" alt-text="Screenshot showing how to select + private endpoint to create a new private endpoint.":::

1. Leave **Subscription** and **Resource group** the same. Under **Instance**, provide a name and select a region for the new private endpoint. Your private endpoint must be in the same region as your virtual network, so use the same region as you specified when creating the VM. When all the fields are complete, select **Next: Resource**.

    :::image type="content" source="media/storage-files-quick-create-use-linux/private-endpoint-basics.png" alt-text="Screenshot showing how to provide the project and instance details for a new private endpoint." lightbox="media/storage-files-quick-create-use-linux/private-endpoint-basics.png" border="true":::

1. Confirm that the **Subscription**, **Resource type** and **Resource** are correct, and select **File** from the **Target sub-resource** drop-down. Then select **Next: Virtual Network**.

    :::image type="content" source="media/storage-files-quick-create-use-linux/private-endpoint-resource.png" alt-text="Screenshot showing how to select the resources that a new private endpoint should connect to." lightbox="media/storage-files-quick-create-use-linux/private-endpoint-resource.png" border="true":::

1. Under **Networking**, select the virtual network associated with your VM and leave the default subnet. Under **Private IP configuration**, leave **Dynamically allocate IP address** selected. Select **Next: DNS**.

    :::image type="content" source="media/storage-files-quick-create-use-linux/private-endpoint-virtual-network.png" alt-text="Screenshot showing how to add virtual networking and private IP configuration to a new private endpoint." lightbox="media/storage-files-quick-create-use-linux/private-endpoint-virtual-network.png" border="true":::

1. Select **Yes** for **Integrate with private DNS zone**. Make sure the correct subscription and resource group are selected, and then select **Next: Tags**.

    :::image type="content" source="media/storage-files-quick-create-use-linux/private-endpoint-dns.png" alt-text="Screenshot showing how to integrate your private endpoint with a private DNS zone." lightbox="media/storage-files-quick-create-use-linux/private-endpoint-dns.png" border="true":::

1. You can optionally apply tags to categorize your resources, such as applying the name **Environment** and the value **Test** to all testing resources. Enter name/value pairs if desired, and then select **Next: Review + create**.

    :::image type="content" source="media/storage-files-quick-create-use-linux/private-endpoint-tags.png" alt-text="Screenshot showing how to add tags to resources in order to categorize them." lightbox="media/storage-files-quick-create-use-linux/private-endpoint-tags.png" border="true":::

1. Azure will attempt to validate the private endpoint. When validation is complete, select **Create**. You'll see a notification that deployment is in progress. After a few minutes, you should see a notification that deployment is complete.

## Connect to your VM

Create an SSH connection with the VM.

1. Select **Home** and then **Virtual machines**.

1. Select the Linux VM you created and ensure that its status is **Running**. Take note of the VM's public IP address and copy it to your clipboard.

    :::image type="content" source="media/storage-files-quick-create-use-linux/connect-to-vm.png" alt-text="Screenshot showing how to confirm that the V M is running and find its public I P address." lightbox="media/storage-files-quick-create-use-linux/connect-to-vm.png" border="true":::

1. If you are on a Mac or Linux machine, open a Bash prompt. If you are on a Windows machine, open a PowerShell prompt.

1. At your prompt, open an SSH connection to your VM. Replace `xx.xx.xx.xx` with the IP address of your VM, and replace the path to the `.pem` with the path to where the key file was downloaded.

```console
ssh -i .\Downloads\myVM_key.pem azureuser@xx.xx.xx.xx
```

If you encounter a warning that the authenticity of the host can't be established, type **yes** to continue connecting to the VM. Leave the ssh connection open for the next step.

> [!TIP]
> You can use the SSH key you created the next time you create a VM in Azure. Just select the **Use a key stored in Azure** for **SSH public key source** the next time you create a VM. You already have the private key on your computer, so you won't need to download anything.

## Mount the NFS share

Now that you've created an NFS share, you have to mount it on your Linux client. Using Azure Storage Explorer isn't supported for NFS Azure file shares, either standalone or from within the Azure portal. To view the files in the share, you must mount the share.

1. Select **Home** and then **Storage accounts**.

1. Select the storage account you created.

1. In the service menu, under **Data storage**, select **File shares**, and then select the NFS file share you created.

1. You should see **Connect to this NFS share from Linux** along with sample commands to use NFS on your Linux distribution and a mounting script that contains the required mount options. For other recommended mount options, see [Mount NFS Azure file share on Linux](storage-files-how-to-mount-nfs-shares.md#mount-options). Azure portal offers a step-by-step, ready-to-use installation script tailored to your selected Linux distribution for installing the AZNFS mount helper package. Once installed, you can use the provided AZNFS mount script to securely mount the share using [Encyption in Transit](encryption-in-transit-for-nfs-shares.md).

   > [!IMPORTANT]
   > The provided mounting script will mount the NFS share only until the Linux machine is rebooted. To automatically mount the share every time the machine reboots, see [Mount an NFS share using /etc/fstab](storage-files-how-to-mount-nfs-shares.md#mount-an-nfs-share-using-etcfstab).

    :::image type="content" source="media/storage-files-quick-create-use-linux/mount-nfs-share.png" alt-text="Screenshot showing how to connect to an N F S file share from Linux using a provided mounting script." lightbox="media/storage-files-quick-create-use-linux/mount-nfs-share.png" border="true":::

1. Select your Linux distribution.

1. Using the ssh connection you created to your VM, enter the sample commands to use NFS and mount the file share.

You have now mounted your NFS share, and it's ready to store files.

> [!NOTE]
> Alternatively, you can also mount the NFS share using [NFS client mount in command line](storage-files-how-to-mount-nfs-shares.md#mount-an-nfs-share-using-the-nfs-client-mount-in-command-line).


## Clean up resources

When you're done, delete the resource group. Deleting the resource group deletes the storage account, the Azure file share, and any other resources that you deployed inside the resource group.

1. Select **Home** and then **Resource groups**.
1. Select the resource group you created.
1. Select **Delete resource group**. A window opens and displays a warning about the resources that will be deleted with the resource group.
1. Enter the name of the resource group, and then select **Delete**.

## Next steps

> [!div class="nextstepaction"]
> [Learn about using NFS Azure file shares](files-nfs-protocol.md)
