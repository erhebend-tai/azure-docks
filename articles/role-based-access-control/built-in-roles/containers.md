---
title: Azure built-in roles for Containers - Azure RBAC
description: This article lists the Azure built-in roles for Azure role-based access control (Azure RBAC) in the Containers category. It lists Actions, NotActions, DataActions, and NotDataActions.
ms.service: role-based-access-control
ms.topic: generated-reference
ms.workload: identity
author: jenniferf-skc    
manager: pmwongera
ms.author: jfields
ms.date: 06/30/2025
ms.custom: generated
---

# Azure built-in roles for Containers

This article lists the Azure built-in roles in the Containers category.


## AcrDelete

Delete repositories, tags, or manifests from a container registry.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/artifacts/delete | Delete artifact in a container registry. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "acr delete",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/c2f4ef07-c644-48eb-af81-4b1b4947fb11",
  "name": "c2f4ef07-c644-48eb-af81-4b1b4947fb11",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/artifacts/delete"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "AcrDelete",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## AcrImageSigner

Push trusted images to or pull trusted images from a container registry enabled for content trust.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/sign/write | Push/Pull content trust metadata for a container registry. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/trustedCollections/write | Allows push or publish of trusted collections of container registry content. This is similar to Microsoft.ContainerRegistry/registries/sign/write action except that this is a data action |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "acr image signer",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/6cef56e8-d556-48e5-a04f-b8e64114680f",
  "name": "6cef56e8-d556-48e5-a04f-b8e64114680f",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/sign/write"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerRegistry/registries/trustedCollections/write"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "AcrImageSigner",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## AcrPull

Pull artifacts from a container registry.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/pull/read | Pull or Get images from a container registry. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "acr pull",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/7f951dda-4ed3-4680-a7ca-43fe172d538d",
  "name": "7f951dda-4ed3-4680-a7ca-43fe172d538d",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/pull/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "AcrPull",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## AcrPush

Push artifacts to or pull artifacts from a container registry.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/pull/read | Pull or Get images from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/push/write | Push or Write images to a container registry. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "acr push",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/8311e382-0749-4cb8-b61a-304f252e45ec",
  "name": "8311e382-0749-4cb8-b61a-304f252e45ec",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/pull/read",
        "Microsoft.ContainerRegistry/registries/push/write"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "AcrPush",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## AcrQuarantineReader

Pull quarantined images from a container registry.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/quarantine/read | Pull or Get quarantined images from container registry |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/quarantinedArtifacts/read | Allows pull or get of the quarantined artifacts from container registry. This is similar to Microsoft.ContainerRegistry/registries/quarantine/read except that it is a data action |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "acr quarantine data reader",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/cdda3590-29a3-44f6-95f2-9f980659eb04",
  "name": "cdda3590-29a3-44f6-95f2-9f980659eb04",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/quarantine/read"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerRegistry/registries/quarantinedArtifacts/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "AcrQuarantineReader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## AcrQuarantineWriter

Push quarantined images to or pull quarantined images from a container registry.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/quarantine/read | Pull or Get quarantined images from container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/quarantine/write | Write/Modify quarantine state of quarantined images |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/quarantinedArtifacts/read | Allows pull or get of the quarantined artifacts from container registry. This is similar to Microsoft.ContainerRegistry/registries/quarantine/read except that it is a data action |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/quarantinedArtifacts/write | Allows write or update of the quarantine state of quarantined artifacts. This is similar to Microsoft.ContainerRegistry/registries/quarantine/write action except that it is a data action |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "acr quarantine data writer",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/c8d4ff99-41c3-41a8-9f60-21dfdad59608",
  "name": "c8d4ff99-41c3-41a8-9f60-21dfdad59608",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/quarantine/read",
        "Microsoft.ContainerRegistry/registries/quarantine/write"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerRegistry/registries/quarantinedArtifacts/read",
        "Microsoft.ContainerRegistry/registries/quarantinedArtifacts/write"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "AcrQuarantineWriter",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Arc Enabled Kubernetes Cluster User Role

List cluster user credentials action.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/write | Creates or updates an deployment. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/listClusterUserCredentials/action | List clusterUser credential(preview) |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Support](../permissions/general.md#microsoftsupport)/* | Create and update a support ticket |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/listClusterUserCredential/action | List clusterUser credential |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "List cluster user credentials action.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/00493d72-78f6-4148-b6c5-d3ce8e4799dd",
  "name": "00493d72-78f6-4148-b6c5-d3ce8e4799dd",
  "permissions": [
    {
      "actions": [
        "Microsoft.Resources/deployments/write",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Kubernetes/connectedClusters/listClusterUserCredentials/action",
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Support/*",
        "Microsoft.Kubernetes/connectedClusters/listClusterUserCredential/action"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Arc Enabled Kubernetes Cluster User Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Arc Kubernetes Admin

Lets you manage all resources under cluster/namespace, except update or delete resource quotas and namespaces.

[Learn more](/azure/azure-arc/kubernetes/azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/write | Creates or updates an deployment. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Support](../permissions/general.md#microsoftsupport)/* | Create and update a support ticket |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/controllerrevisions/read | Reads controllerrevisions |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/daemonsets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/deployments/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/replicasets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/statefulsets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/authorization.k8s.io/localsubjectaccessreviews/write | Writes localsubjectaccessreviews |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/autoscaling/horizontalpodautoscalers/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/batch/cronjobs/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/batch/jobs/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/configmaps/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/endpoints/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/events.k8s.io/events/read | Reads events |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/events/read | Reads events |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/daemonsets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/deployments/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/ingresses/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/networkpolicies/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/replicasets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/limitranges/read | Reads limitranges |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/namespaces/read | Reads namespaces |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/networking.k8s.io/ingresses/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/networking.k8s.io/networkpolicies/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/persistentvolumeclaims/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/pods/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/policy/poddisruptionbudgets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/rbac.authorization.k8s.io/rolebindings/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/rbac.authorization.k8s.io/roles/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/replicationcontrollers/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/replicationcontrollers/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/resourcequotas/read | Reads resourcequotas |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/secrets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/serviceaccounts/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/services/* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Lets you manage all resources under cluster/namespace, except update or delete resource quotas and namespaces.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/dffb1e0c-446f-4dde-a09f-99eb5cc68b96",
  "name": "dffb1e0c-446f-4dde-a09f-99eb5cc68b96",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/write",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Support/*"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.Kubernetes/connectedClusters/apps/controllerrevisions/read",
        "Microsoft.Kubernetes/connectedClusters/apps/daemonsets/*",
        "Microsoft.Kubernetes/connectedClusters/apps/deployments/*",
        "Microsoft.Kubernetes/connectedClusters/apps/replicasets/*",
        "Microsoft.Kubernetes/connectedClusters/apps/statefulsets/*",
        "Microsoft.Kubernetes/connectedClusters/authorization.k8s.io/localsubjectaccessreviews/write",
        "Microsoft.Kubernetes/connectedClusters/autoscaling/horizontalpodautoscalers/*",
        "Microsoft.Kubernetes/connectedClusters/batch/cronjobs/*",
        "Microsoft.Kubernetes/connectedClusters/batch/jobs/*",
        "Microsoft.Kubernetes/connectedClusters/configmaps/*",
        "Microsoft.Kubernetes/connectedClusters/endpoints/*",
        "Microsoft.Kubernetes/connectedClusters/events.k8s.io/events/read",
        "Microsoft.Kubernetes/connectedClusters/events/read",
        "Microsoft.Kubernetes/connectedClusters/extensions/daemonsets/*",
        "Microsoft.Kubernetes/connectedClusters/extensions/deployments/*",
        "Microsoft.Kubernetes/connectedClusters/extensions/ingresses/*",
        "Microsoft.Kubernetes/connectedClusters/extensions/networkpolicies/*",
        "Microsoft.Kubernetes/connectedClusters/extensions/replicasets/*",
        "Microsoft.Kubernetes/connectedClusters/limitranges/read",
        "Microsoft.Kubernetes/connectedClusters/namespaces/read",
        "Microsoft.Kubernetes/connectedClusters/networking.k8s.io/ingresses/*",
        "Microsoft.Kubernetes/connectedClusters/networking.k8s.io/networkpolicies/*",
        "Microsoft.Kubernetes/connectedClusters/persistentvolumeclaims/*",
        "Microsoft.Kubernetes/connectedClusters/pods/*",
        "Microsoft.Kubernetes/connectedClusters/policy/poddisruptionbudgets/*",
        "Microsoft.Kubernetes/connectedClusters/rbac.authorization.k8s.io/rolebindings/*",
        "Microsoft.Kubernetes/connectedClusters/rbac.authorization.k8s.io/roles/*",
        "Microsoft.Kubernetes/connectedClusters/replicationcontrollers/*",
        "Microsoft.Kubernetes/connectedClusters/replicationcontrollers/*",
        "Microsoft.Kubernetes/connectedClusters/resourcequotas/read",
        "Microsoft.Kubernetes/connectedClusters/secrets/*",
        "Microsoft.Kubernetes/connectedClusters/serviceaccounts/*",
        "Microsoft.Kubernetes/connectedClusters/services/*"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Arc Kubernetes Admin",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Arc Kubernetes Cluster Admin

Lets you manage all resources in the cluster.

[Learn more](/azure/azure-arc/kubernetes/azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/write | Creates or updates an deployment. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Support](../permissions/general.md#microsoftsupport)/* | Create and update a support ticket |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Lets you manage all resources in the cluster.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/8393591c-06b9-48a2-a542-1bd6b377f6a2",
  "name": "8393591c-06b9-48a2-a542-1bd6b377f6a2",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/write",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Support/*"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.Kubernetes/connectedClusters/*"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Arc Kubernetes Cluster Admin",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Arc Kubernetes Viewer

Lets you view all resources in cluster/namespace, except secrets.

[Learn more](/azure/azure-arc/kubernetes/azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/write | Creates or updates an deployment. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Support](../permissions/general.md#microsoftsupport)/* | Create and update a support ticket |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/controllerrevisions/read | Reads controllerrevisions |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/daemonsets/read | Reads daemonsets |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/deployments/read | Reads deployments |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/replicasets/read | Reads replicasets |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/statefulsets/read | Reads statefulsets |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/autoscaling/horizontalpodautoscalers/read | Reads horizontalpodautoscalers |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/batch/cronjobs/read | Reads cronjobs |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/batch/jobs/read | Reads jobs |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/configmaps/read | Reads configmaps |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/endpoints/read | Reads endpoints |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/events.k8s.io/events/read | Reads events |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/events/read | Reads events |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/daemonsets/read | Reads daemonsets |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/deployments/read | Reads deployments |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/ingresses/read | Reads ingresses |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/networkpolicies/read | Reads networkpolicies |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/replicasets/read | Reads replicasets |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/limitranges/read | Reads limitranges |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/namespaces/read | Reads namespaces |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/networking.k8s.io/ingresses/read | Reads ingresses |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/networking.k8s.io/networkpolicies/read | Reads networkpolicies |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/persistentvolumeclaims/read | Reads persistentvolumeclaims |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/pods/read | Reads pods |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/policy/poddisruptionbudgets/read | Reads poddisruptionbudgets |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/replicationcontrollers/read | Reads replicationcontrollers |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/replicationcontrollers/read | Reads replicationcontrollers |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/resourcequotas/read | Reads resourcequotas |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/serviceaccounts/read | Reads serviceaccounts |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/services/read | Reads services |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Lets you view all resources in cluster/namespace, except secrets.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/63f0a09d-1495-4db4-a681-037d84835eb4",
  "name": "63f0a09d-1495-4db4-a681-037d84835eb4",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/write",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Support/*"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.Kubernetes/connectedClusters/apps/controllerrevisions/read",
        "Microsoft.Kubernetes/connectedClusters/apps/daemonsets/read",
        "Microsoft.Kubernetes/connectedClusters/apps/deployments/read",
        "Microsoft.Kubernetes/connectedClusters/apps/replicasets/read",
        "Microsoft.Kubernetes/connectedClusters/apps/statefulsets/read",
        "Microsoft.Kubernetes/connectedClusters/autoscaling/horizontalpodautoscalers/read",
        "Microsoft.Kubernetes/connectedClusters/batch/cronjobs/read",
        "Microsoft.Kubernetes/connectedClusters/batch/jobs/read",
        "Microsoft.Kubernetes/connectedClusters/configmaps/read",
        "Microsoft.Kubernetes/connectedClusters/endpoints/read",
        "Microsoft.Kubernetes/connectedClusters/events.k8s.io/events/read",
        "Microsoft.Kubernetes/connectedClusters/events/read",
        "Microsoft.Kubernetes/connectedClusters/extensions/daemonsets/read",
        "Microsoft.Kubernetes/connectedClusters/extensions/deployments/read",
        "Microsoft.Kubernetes/connectedClusters/extensions/ingresses/read",
        "Microsoft.Kubernetes/connectedClusters/extensions/networkpolicies/read",
        "Microsoft.Kubernetes/connectedClusters/extensions/replicasets/read",
        "Microsoft.Kubernetes/connectedClusters/limitranges/read",
        "Microsoft.Kubernetes/connectedClusters/namespaces/read",
        "Microsoft.Kubernetes/connectedClusters/networking.k8s.io/ingresses/read",
        "Microsoft.Kubernetes/connectedClusters/networking.k8s.io/networkpolicies/read",
        "Microsoft.Kubernetes/connectedClusters/persistentvolumeclaims/read",
        "Microsoft.Kubernetes/connectedClusters/pods/read",
        "Microsoft.Kubernetes/connectedClusters/policy/poddisruptionbudgets/read",
        "Microsoft.Kubernetes/connectedClusters/replicationcontrollers/read",
        "Microsoft.Kubernetes/connectedClusters/replicationcontrollers/read",
        "Microsoft.Kubernetes/connectedClusters/resourcequotas/read",
        "Microsoft.Kubernetes/connectedClusters/serviceaccounts/read",
        "Microsoft.Kubernetes/connectedClusters/services/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Arc Kubernetes Viewer",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Arc Kubernetes Writer

Lets you update everything in cluster/namespace, except (cluster)roles and (cluster)role bindings.

[Learn more](/azure/azure-arc/kubernetes/azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/write | Creates or updates an deployment. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Support](../permissions/general.md#microsoftsupport)/* | Create and update a support ticket |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/controllerrevisions/read | Reads controllerrevisions |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/daemonsets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/deployments/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/replicasets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/apps/statefulsets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/autoscaling/horizontalpodautoscalers/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/batch/cronjobs/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/batch/jobs/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/configmaps/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/endpoints/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/events.k8s.io/events/read | Reads events |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/events/read | Reads events |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/daemonsets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/deployments/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/ingresses/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/networkpolicies/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/extensions/replicasets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/limitranges/read | Reads limitranges |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/namespaces/read | Reads namespaces |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/networking.k8s.io/ingresses/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/networking.k8s.io/networkpolicies/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/persistentvolumeclaims/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/pods/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/policy/poddisruptionbudgets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/replicationcontrollers/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/replicationcontrollers/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/resourcequotas/read | Reads resourcequotas |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/secrets/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/serviceaccounts/* |  |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/services/* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Lets you update everything in cluster/namespace, except (cluster)roles and (cluster)role bindings.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/5b999177-9696-4545-85c7-50de3797e5a1",
  "name": "5b999177-9696-4545-85c7-50de3797e5a1",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/write",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Support/*"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.Kubernetes/connectedClusters/apps/controllerrevisions/read",
        "Microsoft.Kubernetes/connectedClusters/apps/daemonsets/*",
        "Microsoft.Kubernetes/connectedClusters/apps/deployments/*",
        "Microsoft.Kubernetes/connectedClusters/apps/replicasets/*",
        "Microsoft.Kubernetes/connectedClusters/apps/statefulsets/*",
        "Microsoft.Kubernetes/connectedClusters/autoscaling/horizontalpodautoscalers/*",
        "Microsoft.Kubernetes/connectedClusters/batch/cronjobs/*",
        "Microsoft.Kubernetes/connectedClusters/batch/jobs/*",
        "Microsoft.Kubernetes/connectedClusters/configmaps/*",
        "Microsoft.Kubernetes/connectedClusters/endpoints/*",
        "Microsoft.Kubernetes/connectedClusters/events.k8s.io/events/read",
        "Microsoft.Kubernetes/connectedClusters/events/read",
        "Microsoft.Kubernetes/connectedClusters/extensions/daemonsets/*",
        "Microsoft.Kubernetes/connectedClusters/extensions/deployments/*",
        "Microsoft.Kubernetes/connectedClusters/extensions/ingresses/*",
        "Microsoft.Kubernetes/connectedClusters/extensions/networkpolicies/*",
        "Microsoft.Kubernetes/connectedClusters/extensions/replicasets/*",
        "Microsoft.Kubernetes/connectedClusters/limitranges/read",
        "Microsoft.Kubernetes/connectedClusters/namespaces/read",
        "Microsoft.Kubernetes/connectedClusters/networking.k8s.io/ingresses/*",
        "Microsoft.Kubernetes/connectedClusters/networking.k8s.io/networkpolicies/*",
        "Microsoft.Kubernetes/connectedClusters/persistentvolumeclaims/*",
        "Microsoft.Kubernetes/connectedClusters/pods/*",
        "Microsoft.Kubernetes/connectedClusters/policy/poddisruptionbudgets/*",
        "Microsoft.Kubernetes/connectedClusters/replicationcontrollers/*",
        "Microsoft.Kubernetes/connectedClusters/replicationcontrollers/*",
        "Microsoft.Kubernetes/connectedClusters/resourcequotas/read",
        "Microsoft.Kubernetes/connectedClusters/secrets/*",
        "Microsoft.Kubernetes/connectedClusters/serviceaccounts/*",
        "Microsoft.Kubernetes/connectedClusters/services/*"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Arc Kubernetes Writer",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Container Storage Contributor

Install Azure Container Storage and manage its storage resources. Includes an ABAC condition to constrain role assignments.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/write | Creates or updates extension resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/read | Gets extension instance resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/delete | Deletes extension instance resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/operations/read | Gets Async Operation status. |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Management](../permissions/management-and-governance.md#microsoftmanagement)/managementGroups/read | List management groups for the authenticated user. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.Support](../permissions/general.md#microsoftsupport)/* | Create and update a support ticket |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |
> | **Actions** |  |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/roleAssignments/write | Create a role assignment at the specified scope. |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/roleAssignments/delete | Delete a role assignment at the specified scope. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |
> | **Condition** |  |
> | ((!(ActionMatches{'Microsoft.Authorization/roleAssignments/write'})) OR (@Request[Microsoft.Authorization/roleAssignments:RoleDefinitionId] ForAnyOfAnyValues:GuidEquals{08d4c71acc634ce4a9c85dd251b4d619})) AND ((!(ActionMatches{'Microsoft.Authorization/roleAssignments/delete'})) OR (@Resource[Microsoft.Authorization/roleAssignments:RoleDefinitionId] ForAnyOfAnyValues:GuidEquals{08d4c71acc634ce4a9c85dd251b4d619})) | Add or remove role assignments for the following roles:<br/>Azure Container Storage Operator |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Lets you install Azure Container Storage and manage its storage resources",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/95dd08a6-00bd-4661-84bf-f6726f83a4d0",
  "name": "95dd08a6-00bd-4661-84bf-f6726f83a4d0",
  "permissions": [
    {
      "actions": [
        "Microsoft.KubernetesConfiguration/extensions/write",
        "Microsoft.KubernetesConfiguration/extensions/read",
        "Microsoft.KubernetesConfiguration/extensions/delete",
        "Microsoft.KubernetesConfiguration/extensions/operations/read",
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Management/managementGroups/read",
        "Microsoft.Resources/deployments/*",
        "Microsoft.Support/*"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    },
    {
      "actions": [
        "Microsoft.Authorization/roleAssignments/write",
        "Microsoft.Authorization/roleAssignments/delete"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": [],
      "conditionVersion": "2.0",
      "condition": "((!(ActionMatches{'Microsoft.Authorization/roleAssignments/write'})) OR (@Request[Microsoft.Authorization/roleAssignments:RoleDefinitionId] ForAnyOfAnyValues:GuidEquals{08d4c71acc634ce4a9c85dd251b4d619})) AND ((!(ActionMatches{'Microsoft.Authorization/roleAssignments/delete'})) OR (@Resource[Microsoft.Authorization/roleAssignments:RoleDefinitionId] ForAnyOfAnyValues:GuidEquals{08d4c71acc634ce4a9c85dd251b4d619}))"
    }
  ],
  "roleName": "Azure Container Storage Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Container Storage Operator

Enable a managed identity to perform Azure Container Storage operations, such as manage virtual machines and manage virtual networks.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ElasticSan](../permissions/storage.md#microsoftelasticsan)/elasticSans/* |  |
> | [Microsoft.ElasticSan](../permissions/storage.md#microsoftelasticsan)/locations/asyncoperations/read | Polls the status of an asynchronous operation. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/routeTables/join/action | Joins a route table. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/join/action | Joins a network security group. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/write | Creates a virtual network or updates an existing virtual network |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/delete | Deletes a virtual network |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/join/action | Joins a virtual network. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/read | Gets a virtual network subnet definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/write | Creates a virtual network subnet or updates an existing virtual network subnet |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/read | Get the properties of a virtual machine |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/write | Creates a new virtual machine or updates an existing virtual machine |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachineScaleSets/read | Get the properties of a Virtual Machine Scale Set |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachineScaleSets/write | Creates a new Virtual Machine Scale Set or updates an existing one |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachineScaleSets/virtualMachines/write | Updates the properties of a Virtual Machine in a VM Scale Set |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachineScaleSets/virtualMachines/read | Retrieves the properties of a Virtual Machine in a VM Scale Set |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/providers/read | Gets or lists resource providers. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/read | Get the virtual network definition |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Role required by a Managed Identity for Azure Container Storage operations",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/08d4c71a-cc63-4ce4-a9c8-5dd251b4d619",
  "name": "08d4c71a-cc63-4ce4-a9c8-5dd251b4d619",
  "permissions": [
    {
      "actions": [
        "Microsoft.ElasticSan/elasticSans/*",
        "Microsoft.ElasticSan/locations/asyncoperations/read",
        "Microsoft.Network/routeTables/join/action",
        "Microsoft.Network/networkSecurityGroups/join/action",
        "Microsoft.Network/virtualNetworks/write",
        "Microsoft.Network/virtualNetworks/delete",
        "Microsoft.Network/virtualNetworks/join/action",
        "Microsoft.Network/virtualNetworks/subnets/read",
        "Microsoft.Network/virtualNetworks/subnets/write",
        "Microsoft.Compute/virtualMachines/read",
        "Microsoft.Compute/virtualMachines/write",
        "Microsoft.Compute/virtualMachineScaleSets/read",
        "Microsoft.Compute/virtualMachineScaleSets/write",
        "Microsoft.Compute/virtualMachineScaleSets/virtualMachines/write",
        "Microsoft.Compute/virtualMachineScaleSets/virtualMachines/read",
        "Microsoft.Resources/subscriptions/providers/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Network/virtualNetworks/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Container Storage Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Container Storage Owner

Install Azure Container Storage, grant access to its storage resources, and configure Azure Elastic storage area network (SAN). Includes an ABAC condition to constrain role assignments.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ElasticSan](../permissions/storage.md#microsoftelasticsan)/elasticSans/* |  |
> | [Microsoft.ElasticSan](../permissions/storage.md#microsoftelasticsan)/locations/* |  |
> | [Microsoft.ElasticSan](../permissions/storage.md#microsoftelasticsan)/elasticSans/volumeGroups/* |  |
> | [Microsoft.ElasticSan](../permissions/storage.md#microsoftelasticsan)/elasticSans/volumeGroups/volumes/* |  |
> | [Microsoft.ElasticSan](../permissions/storage.md#microsoftelasticsan)/locations/asyncoperations/read | Polls the status of an asynchronous operation. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/write | Creates or updates extension resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/read | Gets extension instance resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/delete | Deletes extension instance resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/operations/read | Gets Async Operation status. |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Management](../permissions/management-and-governance.md#microsoftmanagement)/managementGroups/read | List management groups for the authenticated user. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.Support](../permissions/general.md#microsoftsupport)/* | Create and update a support ticket |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |
> | **Actions** |  |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/roleAssignments/write | Create a role assignment at the specified scope. |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/roleAssignments/delete | Delete a role assignment at the specified scope. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |
> | **Condition** |  |
> | ((!(ActionMatches{'Microsoft.Authorization/roleAssignments/write'})) OR (@Request[Microsoft.Authorization/roleAssignments:RoleDefinitionId] ForAnyOfAnyValues:GuidEquals{08d4c71acc634ce4a9c85dd251b4d619})) AND ((!(ActionMatches{'Microsoft.Authorization/roleAssignments/delete'})) OR (@Resource[Microsoft.Authorization/roleAssignments:RoleDefinitionId] ForAnyOfAnyValues:GuidEquals{08d4c71acc634ce4a9c85dd251b4d619})) | Add or remove role assignments for the following roles:<br/>Azure Container Storage Operator |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Lets you install Azure Container Storage and grants access to its storage resources",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/95de85bd-744d-4664-9dde-11430bc34793",
  "name": "95de85bd-744d-4664-9dde-11430bc34793",
  "permissions": [
    {
      "actions": [
        "Microsoft.ElasticSan/elasticSans/*",
        "Microsoft.ElasticSan/locations/*",
        "Microsoft.ElasticSan/elasticSans/volumeGroups/*",
        "Microsoft.ElasticSan/elasticSans/volumeGroups/volumes/*",
        "Microsoft.ElasticSan/locations/asyncoperations/read",
        "Microsoft.KubernetesConfiguration/extensions/write",
        "Microsoft.KubernetesConfiguration/extensions/read",
        "Microsoft.KubernetesConfiguration/extensions/delete",
        "Microsoft.KubernetesConfiguration/extensions/operations/read",
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Management/managementGroups/read",
        "Microsoft.Resources/deployments/*",
        "Microsoft.Support/*"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    },
    {
      "actions": [
        "Microsoft.Authorization/roleAssignments/write",
        "Microsoft.Authorization/roleAssignments/delete"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": [],
      "conditionVersion": "2.0",
      "condition": "((!(ActionMatches{'Microsoft.Authorization/roleAssignments/write'})) OR (@Request[Microsoft.Authorization/roleAssignments:RoleDefinitionId] ForAnyOfAnyValues:GuidEquals{08d4c71acc634ce4a9c85dd251b4d619})) AND ((!(ActionMatches{'Microsoft.Authorization/roleAssignments/delete'})) OR (@Resource[Microsoft.Authorization/roleAssignments:RoleDefinitionId] ForAnyOfAnyValues:GuidEquals{08d4c71acc634ce4a9c85dd251b4d619}))"
    }
  ],
  "roleName": "Azure Container Storage Owner",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Fleet Manager Contributor Role

Grants read/write access to Azure resources provided by Azure Kubernetes Fleet Manager, including fleets, fleet members, fleet update strategies, fleet update runs, etc.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/* |  |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants read/write access to Azure resources provided by Azure Kubernetes Fleet Manager, including fleets, fleet members, fleet update strategies, fleet update runs, etc.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/63bb64ad-9799-4770-b5c3-24ed299a07bf",
  "name": "63bb64ad-9799-4770-b5c3-24ed299a07bf",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerService/fleets/*",
        "Microsoft.Resources/deployments/*"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Fleet Manager Contributor Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```
## Azure Kubernetes Fleet Manager Hub Agent Role

Grants access to Azure resources needed by Azure Kubernetes Fleet Manager hub agents.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPAddresses/read | Gets a public IP address definition. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/trafficManagerProfiles/read | Get the Traffic Manager profile configuration. This includes DNS settings, traffic routing settings, endpoint monitoring settings, and the list of endpoints routed by this Traffic Manager profile. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/trafficManagerProfiles/write | Create a Traffic Manager profile, or modify the configuration of an existing Traffic Manager profile. This includes enabling or disabling a profile and modifying DNS settings, traffic routing settings, or endpoint monitoring settings. Endpoints routed by the Traffic Manager profile can be added, removed, enabled or disabled. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/trafficManagerProfiles/delete | Delete the Traffic Manager profile. All settings associated with the Traffic Manager profile will be lost, and the profile can no longer be used to route traffic. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/trafficManagerProfiles/azureEndpoints/read | Gets an Azure Endpoint which belongs to a Traffic Manager Profile, including all the properties of that Azure Endpoint. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/trafficManagerProfiles/azureEndpoints/write | Add a new Azure Endpoint in an existing Traffic Manager Profile or update the properties of an existing Azure Endpoint in that Traffic Manager Profile. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/trafficManagerProfiles/azureEndpoints/delete | Deletes an Azure Endpoint from an existing Traffic Manager Profile. Traffic Manager will stop routing traffic to the deleted Azure Endpoint. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants access to Azure resources needed by Azure Kubernetes Fleet Manager hub agents.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/de2b316d-7a2c-4143-b4cd-c148f6a355a1",
  "name": "de2b316d-7a2c-4143-b4cd-c148f6a355a1",
  "permissions": [
    {
      "actions": [
        "Microsoft.Network/publicIPAddresses/read",
        "Microsoft.Network/trafficManagerProfiles/read",
        "Microsoft.Network/trafficManagerProfiles/write",
        "Microsoft.Network/trafficManagerProfiles/delete",
        "Microsoft.Network/trafficManagerProfiles/azureEndpoints/read",
        "Microsoft.Network/trafficManagerProfiles/azureEndpoints/write",
        "Microsoft.Network/trafficManagerProfiles/azureEndpoints/delete"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Fleet Manager Hub Agent Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Fleet Manager RBAC Admin

Grants read/write access to Kubernetes resources within a namespace in the fleet-managed hub cluster - provides write permissions on most objects within a namespace, with the exception of ResourceQuota object and the namespace object itself. Applying this role at cluster scope will give access across all namespaces.

[Learn more](/azure/kubernetes-fleet/access-fleet-kubernetes-api)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/read | Get fleet |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/listCredentials/action | List fleet credentials |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/controllerrevisions/read | Reads controllerrevisions |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/daemonsets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/deployments/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/statefulsets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/authorization.k8s.io/localsubjectaccessreviews/write | Writes localsubjectaccessreviews |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/autoscaling/horizontalpodautoscalers/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/batch/cronjobs/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/batch/jobs/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/configmaps/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/endpoints/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/events.k8s.io/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/daemonsets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/deployments/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/ingresses/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/networkpolicies/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/limitranges/read | Reads limitranges |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/namespaces/read | Reads namespaces |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/networking.k8s.io/ingresses/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/networking.k8s.io/networkpolicies/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/persistentvolumeclaims/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/policy/poddisruptionbudgets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/rbac.authorization.k8s.io/rolebindings/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/rbac.authorization.k8s.io/roles/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/replicationcontrollers/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/replicationcontrollers/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/resourcequotas/read | Reads resourcequotas |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/secrets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/serviceaccounts/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/services/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/cluster.kubernetes-fleet.io/internalmemberclusters/read | Read fleet internalmembercluster resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/resourceoverrides/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/resourceoverridesnapshots/read | Read fleet resourceoverridesnapshot resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/works/read | Read fleet work resource |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants read/write access to Kubernetes resources within a namespace in the fleet-managed hub cluster - provides write permissions on most objects within a a namespace, with the exception of ResourceQuota object and the namespace object itself. Applying this role at cluster scope will give access across all namespaces.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/434fb43a-c01c-447e-9f67-c3ad923cfaba",
  "name": "434fb43a-c01c-447e-9f67-c3ad923cfaba",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.ContainerService/fleets/read",
        "Microsoft.ContainerService/fleets/listCredentials/action"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerService/fleets/apps/controllerrevisions/read",
        "Microsoft.ContainerService/fleets/apps/daemonsets/*",
        "Microsoft.ContainerService/fleets/apps/deployments/*",
        "Microsoft.ContainerService/fleets/apps/statefulsets/*",
        "Microsoft.ContainerService/fleets/authorization.k8s.io/localsubjectaccessreviews/write",
        "Microsoft.ContainerService/fleets/autoscaling/horizontalpodautoscalers/*",
        "Microsoft.ContainerService/fleets/batch/cronjobs/*",
        "Microsoft.ContainerService/fleets/batch/jobs/*",
        "Microsoft.ContainerService/fleets/configmaps/*",
        "Microsoft.ContainerService/fleets/endpoints/*",
        "Microsoft.ContainerService/fleets/events.k8s.io/events/read",
        "Microsoft.ContainerService/fleets/events/read",
        "Microsoft.ContainerService/fleets/extensions/daemonsets/*",
        "Microsoft.ContainerService/fleets/extensions/deployments/*",
        "Microsoft.ContainerService/fleets/extensions/ingresses/*",
        "Microsoft.ContainerService/fleets/extensions/networkpolicies/*",
        "Microsoft.ContainerService/fleets/limitranges/read",
        "Microsoft.ContainerService/fleets/namespaces/read",
        "Microsoft.ContainerService/fleets/networking.k8s.io/ingresses/*",
        "Microsoft.ContainerService/fleets/networking.k8s.io/networkpolicies/*",
        "Microsoft.ContainerService/fleets/persistentvolumeclaims/*",
        "Microsoft.ContainerService/fleets/policy/poddisruptionbudgets/*",
        "Microsoft.ContainerService/fleets/rbac.authorization.k8s.io/rolebindings/*",
        "Microsoft.ContainerService/fleets/rbac.authorization.k8s.io/roles/*",
        "Microsoft.ContainerService/fleets/replicationcontrollers/*",
        "Microsoft.ContainerService/fleets/replicationcontrollers/*",
        "Microsoft.ContainerService/fleets/resourcequotas/read",
        "Microsoft.ContainerService/fleets/secrets/*",
        "Microsoft.ContainerService/fleets/serviceaccounts/*",
        "Microsoft.ContainerService/fleets/services/*",
        "Microsoft.ContainerService/fleets/cluster.kubernetes-fleet.io/internalmemberclusters/read",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/resourceoverrides/*",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/resourceoverridesnapshots/read",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/works/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Fleet Manager RBAC Admin",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Fleet Manager RBAC Cluster Admin

Grants read/write access to all Kubernetes resources in the fleet-managed hub cluster.

[Learn more](/azure/kubernetes-fleet/access-fleet-kubernetes-api)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/read | Get fleet |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/listCredentials/action | List fleet credentials |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants read/write access to all Kubernetes resources in the fleet-managed hub cluster.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/18ab4d3d-a1bf-4477-8ad9-8359bc988f69",
  "name": "18ab4d3d-a1bf-4477-8ad9-8359bc988f69",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.ContainerService/fleets/read",
        "Microsoft.ContainerService/fleets/listCredentials/action"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerService/fleets/*"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Fleet Manager RBAC Cluster Admin",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Fleet Manager RBAC Reader

Grants read-only access to most Kubernetes resources within a namespace in the fleet-managed hub cluster. It does not allow viewing roles or role bindings. This role does not allow viewing Secrets, since reading the contents of Secrets enables access to ServiceAccount credentials in the namespace, which would allow API access as any ServiceAccount in the namespace (a form of privilege escalation).  Applying this role at cluster scope will give access across all namespaces.

[Learn more](/azure/kubernetes-fleet/access-fleet-kubernetes-api)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/read | Get fleet |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/listCredentials/action | List fleet credentials |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/controllerrevisions/read | Reads controllerrevisions |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/daemonsets/read | Reads daemonsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/deployments/read | Reads deployments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/statefulsets/read | Reads statefulsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/autoscaling/horizontalpodautoscalers/read | Reads horizontalpodautoscalers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/batch/cronjobs/read | Reads cronjobs |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/batch/jobs/read | Reads jobs |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/configmaps/read | Reads configmaps |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/endpoints/read | Reads endpoints |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/events.k8s.io/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/daemonsets/read | Reads daemonsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/deployments/read | Reads deployments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/ingresses/read | Reads ingresses |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/networkpolicies/read | Reads networkpolicies |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/limitranges/read | Reads limitranges |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/namespaces/read | Reads namespaces |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/networking.k8s.io/ingresses/read | Reads ingresses |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/networking.k8s.io/networkpolicies/read | Reads networkpolicies |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/persistentvolumeclaims/read | Reads persistentvolumeclaims |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/policy/poddisruptionbudgets/read | Reads poddisruptionbudgets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/replicationcontrollers/read | Reads replicationcontrollers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/replicationcontrollers/read | Reads replicationcontrollers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/resourcequotas/read | Reads resourcequotas |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/serviceaccounts/read | Reads serviceaccounts |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/services/read | Reads services |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/cluster.kubernetes-fleet.io/internalmemberclusters/read | Read fleet internalmembercluster resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/resourceoverrides/read | Read fleet resourceoverride resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/resourceoverridesnapshots/read | Read fleet resourceoverridesnapshot resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/works/read | Read fleet work resource |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants read-only access to most Kubernetes resources within a namespace in the fleet-managed hub cluster. It does not allow viewing roles or role bindings. This role does not allow viewing Secrets, since reading the contents of Secrets enables access to ServiceAccount credentials in the namespace, which would allow API access as any ServiceAccount in the namespace (a form of privilege escalation).  Applying this role at cluster scope will give access across all namespaces.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/30b27cfc-9c84-438e-b0ce-70e35255df80",
  "name": "30b27cfc-9c84-438e-b0ce-70e35255df80",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.ContainerService/fleets/read",
        "Microsoft.ContainerService/fleets/listCredentials/action"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerService/fleets/apps/controllerrevisions/read",
        "Microsoft.ContainerService/fleets/apps/daemonsets/read",
        "Microsoft.ContainerService/fleets/apps/deployments/read",
        "Microsoft.ContainerService/fleets/apps/statefulsets/read",
        "Microsoft.ContainerService/fleets/autoscaling/horizontalpodautoscalers/read",
        "Microsoft.ContainerService/fleets/batch/cronjobs/read",
        "Microsoft.ContainerService/fleets/batch/jobs/read",
        "Microsoft.ContainerService/fleets/configmaps/read",
        "Microsoft.ContainerService/fleets/endpoints/read",
        "Microsoft.ContainerService/fleets/events.k8s.io/events/read",
        "Microsoft.ContainerService/fleets/events/read",
        "Microsoft.ContainerService/fleets/extensions/daemonsets/read",
        "Microsoft.ContainerService/fleets/extensions/deployments/read",
        "Microsoft.ContainerService/fleets/extensions/ingresses/read",
        "Microsoft.ContainerService/fleets/extensions/networkpolicies/read",
        "Microsoft.ContainerService/fleets/limitranges/read",
        "Microsoft.ContainerService/fleets/namespaces/read",
        "Microsoft.ContainerService/fleets/networking.k8s.io/ingresses/read",
        "Microsoft.ContainerService/fleets/networking.k8s.io/networkpolicies/read",
        "Microsoft.ContainerService/fleets/persistentvolumeclaims/read",
        "Microsoft.ContainerService/fleets/policy/poddisruptionbudgets/read",
        "Microsoft.ContainerService/fleets/replicationcontrollers/read",
        "Microsoft.ContainerService/fleets/replicationcontrollers/read",
        "Microsoft.ContainerService/fleets/resourcequotas/read",
        "Microsoft.ContainerService/fleets/serviceaccounts/read",
        "Microsoft.ContainerService/fleets/services/read",
        "Microsoft.ContainerService/fleets/cluster.kubernetes-fleet.io/internalmemberclusters/read",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/resourceoverrides/read",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/resourceoverridesnapshots/read",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/works/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Fleet Manager RBAC Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Fleet Manager RBAC Writer

Grants read/write access to most Kubernetes resources within a namespace in the fleet-managed hub cluster. This role does not allow viewing or modifying roles or role bindings. However, this role allows accessing Secrets as any ServiceAccount in the namespace, so it can be used to gain the API access levels of any ServiceAccount in the namespace.  Applying this role at cluster scope will give access across all namespaces.

[Learn more](/azure/kubernetes-fleet/access-fleet-kubernetes-api)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/read | Get fleet |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/listCredentials/action | List fleet credentials |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/controllerrevisions/read | Reads controllerrevisions |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/daemonsets/read | Reads daemonsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/daemonsets/write | Writes daemonsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/deployments/read | Reads deployments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/deployments/write | Writes deployments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/statefulsets/read | Reads statefulsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/apps/statefulsets/write | Writes statefulsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/autoscaling/horizontalpodautoscalers/read | Reads horizontalpodautoscalers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/autoscaling/horizontalpodautoscalers/write | Writes horizontalpodautoscalers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/batch/cronjobs/read | Reads cronjobs |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/batch/cronjobs/write | Writes cronjobs |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/batch/jobs/read | Reads jobs |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/batch/jobs/write | Writes jobs |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/configmaps/read | Reads configmaps |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/configmaps/write | Writes configmaps |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/endpoints/read | Reads endpoints |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/endpoints/write | Writes endpoints |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/events.k8s.io/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/daemonsets/read | Reads daemonsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/daemonsets/write | Writes daemonsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/deployments/read | Reads deployments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/deployments/write | Writes deployments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/ingresses/read | Reads ingresses |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/ingresses/write | Writes ingresses |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/networkpolicies/read | Reads networkpolicies |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/extensions/networkpolicies/write | Writes networkpolicies |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/limitranges/read | Reads limitranges |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/namespaces/read | Reads namespaces |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/networking.k8s.io/ingresses/read | Reads ingresses |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/networking.k8s.io/ingresses/write | Writes ingresses |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/networking.k8s.io/networkpolicies/read | Reads networkpolicies |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/networking.k8s.io/networkpolicies/write | Writes networkpolicies |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/persistentvolumeclaims/read | Reads persistentvolumeclaims |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/persistentvolumeclaims/write | Writes persistentvolumeclaims |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/policy/poddisruptionbudgets/read | Reads poddisruptionbudgets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/policy/poddisruptionbudgets/write | Writes poddisruptionbudgets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/replicationcontrollers/read | Reads replicationcontrollers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/replicationcontrollers/write | Writes replicationcontrollers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/resourcequotas/read | Reads resourcequotas |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/secrets/read | Reads secrets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/secrets/write | Writes secrets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/serviceaccounts/read | Reads serviceaccounts |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/serviceaccounts/write | Writes serviceaccounts |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/services/read | Reads services |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/services/write | Writes services |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/cluster.kubernetes-fleet.io/internalmemberclusters/read | Read fleet internalmembercluster resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/resourceoverrides/read | Read fleet resourceoverride resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/resourceoverrides/write | Write fleet resourceoverride resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/resourceoverridesnapshots/read | Read fleet resourceoverridesnapshot resource |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/fleets/placement.kubernetes-fleet.io/works/read | Read fleet work resource |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants read/write access to most Kubernetes resources within a namespace in the fleet-managed hub cluster. This role does not allow viewing or modifying roles or role bindings. However, this role allows accessing Secrets as any ServiceAccount in the namespace, so it can be used to gain the API access levels of any ServiceAccount in the namespace.  Applying this role at cluster scope will give access across all namespaces.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/5af6afb3-c06c-4fa4-8848-71a8aee05683",
  "name": "5af6afb3-c06c-4fa4-8848-71a8aee05683",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.ContainerService/fleets/read",
        "Microsoft.ContainerService/fleets/listCredentials/action"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerService/fleets/apps/controllerrevisions/read",
        "Microsoft.ContainerService/fleets/apps/daemonsets/read",
        "Microsoft.ContainerService/fleets/apps/daemonsets/write",
        "Microsoft.ContainerService/fleets/apps/deployments/read",
        "Microsoft.ContainerService/fleets/apps/deployments/write",
        "Microsoft.ContainerService/fleets/apps/statefulsets/read",
        "Microsoft.ContainerService/fleets/apps/statefulsets/write",
        "Microsoft.ContainerService/fleets/autoscaling/horizontalpodautoscalers/read",
        "Microsoft.ContainerService/fleets/autoscaling/horizontalpodautoscalers/write",
        "Microsoft.ContainerService/fleets/batch/cronjobs/read",
        "Microsoft.ContainerService/fleets/batch/cronjobs/write",
        "Microsoft.ContainerService/fleets/batch/jobs/read",
        "Microsoft.ContainerService/fleets/batch/jobs/write",
        "Microsoft.ContainerService/fleets/configmaps/read",
        "Microsoft.ContainerService/fleets/configmaps/write",
        "Microsoft.ContainerService/fleets/endpoints/read",
        "Microsoft.ContainerService/fleets/endpoints/write",
        "Microsoft.ContainerService/fleets/events.k8s.io/events/read",
        "Microsoft.ContainerService/fleets/events/read",
        "Microsoft.ContainerService/fleets/extensions/daemonsets/read",
        "Microsoft.ContainerService/fleets/extensions/daemonsets/write",
        "Microsoft.ContainerService/fleets/extensions/deployments/read",
        "Microsoft.ContainerService/fleets/extensions/deployments/write",
        "Microsoft.ContainerService/fleets/extensions/ingresses/read",
        "Microsoft.ContainerService/fleets/extensions/ingresses/write",
        "Microsoft.ContainerService/fleets/extensions/networkpolicies/read",
        "Microsoft.ContainerService/fleets/extensions/networkpolicies/write",
        "Microsoft.ContainerService/fleets/limitranges/read",
        "Microsoft.ContainerService/fleets/namespaces/read",
        "Microsoft.ContainerService/fleets/networking.k8s.io/ingresses/read",
        "Microsoft.ContainerService/fleets/networking.k8s.io/ingresses/write",
        "Microsoft.ContainerService/fleets/networking.k8s.io/networkpolicies/read",
        "Microsoft.ContainerService/fleets/networking.k8s.io/networkpolicies/write",
        "Microsoft.ContainerService/fleets/persistentvolumeclaims/read",
        "Microsoft.ContainerService/fleets/persistentvolumeclaims/write",
        "Microsoft.ContainerService/fleets/policy/poddisruptionbudgets/read",
        "Microsoft.ContainerService/fleets/policy/poddisruptionbudgets/write",
        "Microsoft.ContainerService/fleets/replicationcontrollers/read",
        "Microsoft.ContainerService/fleets/replicationcontrollers/write",
        "Microsoft.ContainerService/fleets/resourcequotas/read",
        "Microsoft.ContainerService/fleets/secrets/read",
        "Microsoft.ContainerService/fleets/secrets/write",
        "Microsoft.ContainerService/fleets/serviceaccounts/read",
        "Microsoft.ContainerService/fleets/serviceaccounts/write",
        "Microsoft.ContainerService/fleets/services/read",
        "Microsoft.ContainerService/fleets/services/write",
        "Microsoft.ContainerService/fleets/cluster.kubernetes-fleet.io/internalmemberclusters/read",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/resourceoverrides/read",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/resourceoverrides/write",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/resourceoverridesnapshots/read",
        "Microsoft.ContainerService/fleets/placement.kubernetes-fleet.io/works/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Fleet Manager RBAC Writer",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service Arc Cluster Admin Role

List cluster admin credential action.

[Learn more](/azure/aks/hybrid/concepts-security-access-identity)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/read | Gets the Hybrid AKS provisioned cluster instances associated with the connected cluster |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/listAdminKubeconfig/action | Lists the admin credentials of a provisioned cluster instance used only in direct mode. |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/Read | Read connectedClusters |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "List cluster admin credential action.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/b29efa5f-7782-4dc3-9537-4d5bc70a5e9f",
  "name": "b29efa5f-7782-4dc3-9537-4d5bc70a5e9f",
  "permissions": [
    {
      "actions": [
        "Microsoft.HybridContainerService/provisionedClusterInstances/read",
        "Microsoft.HybridContainerService/provisionedClusterInstances/listAdminKubeconfig/action",
        "Microsoft.Kubernetes/connectedClusters/Read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service Arc Cluster Admin Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service Arc Cluster User Role

List cluster user credential action.

[Learn more](/azure/aks/hybrid/concepts-security-access-identity)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/read | Gets the Hybrid AKS provisioned cluster instances associated with the connected cluster |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/listUserKubeconfig/action | Lists the AAD user credentials of a provisioned cluster instance used only in direct mode. |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/Read | Read connectedClusters |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "List cluster user credential action.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/233ca253-b031-42ff-9fba-87ef12d6b55f",
  "name": "233ca253-b031-42ff-9fba-87ef12d6b55f",
  "permissions": [
    {
      "actions": [
        "Microsoft.HybridContainerService/provisionedClusterInstances/read",
        "Microsoft.HybridContainerService/provisionedClusterInstances/listUserKubeconfig/action",
        "Microsoft.Kubernetes/connectedClusters/Read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service Arc Cluster User Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service Arc Contributor Role

Grants access to read and write Azure Kubernetes Services hybrid clusters

[Learn more](/azure/aks/hybrid/concepts-security-access-identity)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/Locations/operationStatuses/read | read operationStatuses |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/Operations/read | read Operations |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/kubernetesVersions/read | Lists the supported kubernetes versions from the underlying custom location |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/kubernetesVersions/write | Puts the kubernetes version resource type |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/kubernetesVersions/delete | Delete the kubernetes versions resource type |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/read | Gets the Hybrid AKS provisioned cluster instances associated with the connected cluster |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/write | Creates the Hybrid AKS provisioned cluster instance |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/delete | Deletes the Hybrid AKS provisioned cluster instance |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/agentPools/read | Gets the agent pools in the Hybrid AKS provisioned cluster instance |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/agentPools/write | Updates the agent pool in the Hybrid AKS provisioned cluster instance |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/agentPools/delete | Deletes the agent pool in the Hybrid AKS provisioned cluster instance |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/provisionedClusterInstances/upgradeProfiles/read | read upgradeProfiles |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/skus/read | Lists the supported VM SKUs from the underlying custom location |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/skus/write | Puts the VM SKUs resource type |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/skus/delete | Deletes the Vm Sku resource type |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/virtualNetworks/read | Lists the Hybrid AKS virtual networks by subscription |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/virtualNetworks/write | Patches the Hybrid AKS virtual network |
> | [Microsoft.HybridContainerService](../permissions/hybrid-multicloud.md#microsofthybridcontainerservice)/virtualNetworks/delete | Deletes the Hybrid AKS virtual network |
> | [Microsoft.ExtendedLocation](../permissions/hybrid-multicloud.md#microsoftextendedlocation)/customLocations/deploy/action | Deploy permissions to a Custom Location resource |
> | [Microsoft.ExtendedLocation](../permissions/hybrid-multicloud.md#microsoftextendedlocation)/customLocations/read | Gets an Custom Location resource |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/Read | Read connectedClusters |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/Write | Writes connectedClusters |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/Delete | Deletes connectedClusters |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/listClusterUserCredential/action | List clusterUser credential |
> | [Microsoft.AzureStackHCI](../permissions/hybrid-multicloud.md#microsoftazurestackhci)/clusters/read | Gets clusters |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants access to read and write Azure Kubernetes Services hybrid clusters",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/5d3f1697-4507-4d08-bb4a-477695db5f82",
  "name": "5d3f1697-4507-4d08-bb4a-477695db5f82",
  "permissions": [
    {
      "actions": [
        "Microsoft.HybridContainerService/Locations/operationStatuses/read",
        "Microsoft.HybridContainerService/Operations/read",
        "Microsoft.HybridContainerService/kubernetesVersions/read",
        "Microsoft.HybridContainerService/kubernetesVersions/write",
        "Microsoft.HybridContainerService/kubernetesVersions/delete",
        "Microsoft.HybridContainerService/provisionedClusterInstances/read",
        "Microsoft.HybridContainerService/provisionedClusterInstances/write",
        "Microsoft.HybridContainerService/provisionedClusterInstances/delete",
        "Microsoft.HybridContainerService/provisionedClusterInstances/agentPools/read",
        "Microsoft.HybridContainerService/provisionedClusterInstances/agentPools/write",
        "Microsoft.HybridContainerService/provisionedClusterInstances/agentPools/delete",
        "Microsoft.HybridContainerService/provisionedClusterInstances/upgradeProfiles/read",
        "Microsoft.HybridContainerService/skus/read",
        "Microsoft.HybridContainerService/skus/write",
        "Microsoft.HybridContainerService/skus/delete",
        "Microsoft.HybridContainerService/virtualNetworks/read",
        "Microsoft.HybridContainerService/virtualNetworks/write",
        "Microsoft.HybridContainerService/virtualNetworks/delete",
        "Microsoft.ExtendedLocation/customLocations/deploy/action",
        "Microsoft.ExtendedLocation/customLocations/read",
        "Microsoft.Kubernetes/connectedClusters/Read",
        "Microsoft.Kubernetes/connectedClusters/Write",
        "Microsoft.Kubernetes/connectedClusters/Delete",
        "Microsoft.Kubernetes/connectedClusters/listClusterUserCredential/action",
        "Microsoft.AzureStackHCI/clusters/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service Arc Contributor Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service Cluster Admin Role

List cluster admin credential action.

[Learn more](/azure/aks/control-kubeconfig-access)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/listClusterAdminCredential/action | List the clusterAdmin credential of a managed cluster |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/accessProfiles/listCredential/action | Get a managed cluster access profile by role name using list credential |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/read | Get a managed cluster |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/runcommand/action | Run user issued command against managed kubernetes server. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "List cluster admin credential action.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/0ab0b1a8-8aac-4efd-b8c2-3ee1fb270be8",
  "name": "0ab0b1a8-8aac-4efd-b8c2-3ee1fb270be8",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerService/managedClusters/listClusterAdminCredential/action",
        "Microsoft.ContainerService/managedClusters/accessProfiles/listCredential/action",
        "Microsoft.ContainerService/managedClusters/read",
        "Microsoft.ContainerService/managedClusters/runcommand/action"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service Cluster Admin Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service Cluster Monitoring User

List cluster monitoring user credential action.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/listClusterMonitoringUserCredential/action | List the clusterMonitoringUser credential of a managed cluster |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/read | Get a managed cluster |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "List cluster monitoring user credential action.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/1afdec4b-e479-420e-99e7-f82237c7c5e6",
  "name": "1afdec4b-e479-420e-99e7-f82237c7c5e6",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerService/managedClusters/listClusterMonitoringUserCredential/action",
        "Microsoft.ContainerService/managedClusters/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service Cluster Monitoring User",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service Cluster User Role

List cluster user credential action.

[Learn more](/azure/aks/control-kubeconfig-access)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/listClusterUserCredential/action | List the clusterUser credential of a managed cluster |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/read | Get a managed cluster |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "List cluster user credential action.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/4abbcc35-e782-43d8-92c5-2d3f1bd2253f",
  "name": "4abbcc35-e782-43d8-92c5-2d3f1bd2253f",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerService/managedClusters/listClusterUserCredential/action",
        "Microsoft.ContainerService/managedClusters/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service Cluster User Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service Contributor Role

Grants access to read and write Azure Kubernetes Service clusters

[Learn more](/azure/aks/concepts-identity)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/locations/* | Read locations available to ContainerService resources |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/* | Create and manage a managed cluster |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedclustersnapshots/* | Create and manage a managed cluster snapshot |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/snapshots/* | Create and manage a snapshot |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants access to read and write Azure Kubernetes Service clusters",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/ed7f3fbd-7b88-4dd4-9017-9adb7ce333f8",
  "name": "ed7f3fbd-7b88-4dd4-9017-9adb7ce333f8",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.ContainerService/locations/*",
        "Microsoft.ContainerService/managedClusters/*",
        "Microsoft.ContainerService/managedclustersnapshots/*",
        "Microsoft.ContainerService/snapshots/*",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/*",
        "Microsoft.Resources/subscriptions/resourceGroups/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service Contributor Role",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service RBAC Admin

Lets you manage all resources under cluster/namespace, except update or delete resource quotas and namespaces.

[Learn more](/azure/aks/manage-azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/listClusterUserCredential/action | List the clusterUser credential of a managed cluster |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/* |  |
> | **NotDataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/resourcequotas/write | Writes resourcequotas |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/resourcequotas/delete | Deletes resourcequotas |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/namespaces/write | Writes namespaces |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/namespaces/delete | Deletes namespaces |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Lets you manage all resources under cluster/namespace, except update or delete resource quotas and namespaces.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/3498e952-d568-435e-9b2c-8d77e338d7f7",
  "name": "3498e952-d568-435e-9b2c-8d77e338d7f7",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.ContainerService/managedClusters/listClusterUserCredential/action"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerService/managedClusters/*"
      ],
      "notDataActions": [
        "Microsoft.ContainerService/managedClusters/resourcequotas/write",
        "Microsoft.ContainerService/managedClusters/resourcequotas/delete",
        "Microsoft.ContainerService/managedClusters/namespaces/write",
        "Microsoft.ContainerService/managedClusters/namespaces/delete"
      ]
    }
  ],
  "roleName": "Azure Kubernetes Service RBAC Admin",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service RBAC Cluster Admin

Lets you manage all resources in the cluster.

[Learn more](/azure/aks/manage-azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/listClusterUserCredential/action | List the clusterUser credential of a managed cluster |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Lets you manage all resources in the cluster.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/b1ff04bb-8a4e-4dc4-8eb5-8693973ce19b",
  "name": "b1ff04bb-8a4e-4dc4-8eb5-8693973ce19b",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.ContainerService/managedClusters/listClusterUserCredential/action"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerService/managedClusters/*"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service RBAC Cluster Admin",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service RBAC Reader

Allows read-only access to see most objects in a namespace. It does not allow viewing roles or role bindings. This role does not allow viewing Secrets, since reading the contents of Secrets enables access to ServiceAccount credentials in the namespace, which would allow API access as any ServiceAccount in the namespace (a form of privilege escalation). Applying this role at cluster scope will give access across all namespaces.

[Learn more](/azure/aks/manage-azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/controllerrevisions/read | Reads controllerrevisions |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/daemonsets/read | Reads daemonsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/deployments/read | Reads deployments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/replicasets/read | Reads replicasets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/statefulsets/read | Reads statefulsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/autoscaling/horizontalpodautoscalers/read | Reads horizontalpodautoscalers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/batch/cronjobs/read | Reads cronjobs |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/batch/jobs/read | Reads jobs |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/configmaps/read | Reads configmaps |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/discovery.k8s.io/endpointslices/read | Reads endpointslices |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/endpoints/read | Reads endpoints |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/events.k8s.io/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/daemonsets/read | Reads daemonsets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/deployments/read | Reads deployments |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/ingresses/read | Reads ingresses |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/networkpolicies/read | Reads networkpolicies |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/replicasets/read | Reads replicasets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/limitranges/read | Reads limitranges |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/metrics.k8s.io/pods/read | Reads pods |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/metrics.k8s.io/nodes/read | Reads nodes |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/namespaces/read | Reads namespaces |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/networking.k8s.io/ingresses/read | Reads ingresses |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/networking.k8s.io/networkpolicies/read | Reads networkpolicies |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/persistentvolumeclaims/read | Reads persistentvolumeclaims |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/pods/read | Reads pods |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/policy/poddisruptionbudgets/read | Reads poddisruptionbudgets |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/replicationcontrollers/read | Reads replicationcontrollers |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/resourcequotas/read | Reads resourcequotas |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/serviceaccounts/read | Reads serviceaccounts |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/services/read | Reads services |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Allows read-only access to see most objects in a namespace. It does not allow viewing roles or role bindings. This role does not allow viewing Secrets, since reading the contents of Secrets enables access to ServiceAccount credentials in the namespace, which would allow API access as any ServiceAccount in the namespace (a form of privilege escalation). Applying this role at cluster scope will give access across all namespaces.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/7f6c6a51-bcf8-42ba-9220-52d62157d7db",
  "name": "7f6c6a51-bcf8-42ba-9220-52d62157d7db",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerService/managedClusters/apps/controllerrevisions/read",
        "Microsoft.ContainerService/managedClusters/apps/daemonsets/read",
        "Microsoft.ContainerService/managedClusters/apps/deployments/read",
        "Microsoft.ContainerService/managedClusters/apps/replicasets/read",
        "Microsoft.ContainerService/managedClusters/apps/statefulsets/read",
        "Microsoft.ContainerService/managedClusters/autoscaling/horizontalpodautoscalers/read",
        "Microsoft.ContainerService/managedClusters/batch/cronjobs/read",
        "Microsoft.ContainerService/managedClusters/batch/jobs/read",
        "Microsoft.ContainerService/managedClusters/configmaps/read",
        "Microsoft.ContainerService/managedClusters/discovery.k8s.io/endpointslices/read",
        "Microsoft.ContainerService/managedClusters/endpoints/read",
        "Microsoft.ContainerService/managedClusters/events.k8s.io/events/read",
        "Microsoft.ContainerService/managedClusters/events/read",
        "Microsoft.ContainerService/managedClusters/extensions/daemonsets/read",
        "Microsoft.ContainerService/managedClusters/extensions/deployments/read",
        "Microsoft.ContainerService/managedClusters/extensions/ingresses/read",
        "Microsoft.ContainerService/managedClusters/extensions/networkpolicies/read",
        "Microsoft.ContainerService/managedClusters/extensions/replicasets/read",
        "Microsoft.ContainerService/managedClusters/limitranges/read",
        "Microsoft.ContainerService/managedClusters/metrics.k8s.io/pods/read",
        "Microsoft.ContainerService/managedClusters/metrics.k8s.io/nodes/read",
        "Microsoft.ContainerService/managedClusters/namespaces/read",
        "Microsoft.ContainerService/managedClusters/networking.k8s.io/ingresses/read",
        "Microsoft.ContainerService/managedClusters/networking.k8s.io/networkpolicies/read",
        "Microsoft.ContainerService/managedClusters/persistentvolumeclaims/read",
        "Microsoft.ContainerService/managedClusters/pods/read",
        "Microsoft.ContainerService/managedClusters/policy/poddisruptionbudgets/read",
        "Microsoft.ContainerService/managedClusters/replicationcontrollers/read",
        "Microsoft.ContainerService/managedClusters/resourcequotas/read",
        "Microsoft.ContainerService/managedClusters/serviceaccounts/read",
        "Microsoft.ContainerService/managedClusters/services/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service RBAC Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Kubernetes Service RBAC Writer

Allows read/write access to most objects in a namespace. This role does not allow viewing or modifying roles or role bindings. However, this role allows accessing Secrets and running Pods as any ServiceAccount in the namespace, so it can be used to gain the API access levels of any ServiceAccount in the namespace. Applying this role at cluster scope will give access across all namespaces.

[Learn more](/azure/aks/manage-azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/controllerrevisions/read | Reads controllerrevisions |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/daemonsets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/deployments/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/replicasets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/apps/statefulsets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/autoscaling/horizontalpodautoscalers/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/batch/cronjobs/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/coordination.k8s.io/leases/read | Reads leases |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/coordination.k8s.io/leases/write | Writes leases |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/coordination.k8s.io/leases/delete | Deletes leases |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/discovery.k8s.io/endpointslices/read | Reads endpointslices |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/batch/jobs/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/configmaps/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/endpoints/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/events.k8s.io/events/read | Reads events |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/events/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/daemonsets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/deployments/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/ingresses/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/networkpolicies/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/extensions/replicasets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/limitranges/read | Reads limitranges |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/metrics.k8s.io/pods/read | Reads pods |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/metrics.k8s.io/nodes/read | Reads nodes |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/namespaces/read | Reads namespaces |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/networking.k8s.io/ingresses/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/networking.k8s.io/networkpolicies/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/persistentvolumeclaims/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/pods/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/policy/poddisruptionbudgets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/replicationcontrollers/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/resourcequotas/read | Reads resourcequotas |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/secrets/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/serviceaccounts/* |  |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/services/* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Allows read/write access to most objects in a namespace.This role does not allow viewing or modifying roles or role bindings. However, this role allows accessing Secrets and running Pods as any ServiceAccount in the namespace, so it can be used to gain the API access levels of any ServiceAccount in the namespace. Applying this role at cluster scope will give access across all namespaces.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/a7ffa36f-339b-4b5c-8bdf-e2c188b2c0eb",
  "name": "a7ffa36f-339b-4b5c-8bdf-e2c188b2c0eb",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerService/managedClusters/apps/controllerrevisions/read",
        "Microsoft.ContainerService/managedClusters/apps/daemonsets/*",
        "Microsoft.ContainerService/managedClusters/apps/deployments/*",
        "Microsoft.ContainerService/managedClusters/apps/replicasets/*",
        "Microsoft.ContainerService/managedClusters/apps/statefulsets/*",
        "Microsoft.ContainerService/managedClusters/autoscaling/horizontalpodautoscalers/*",
        "Microsoft.ContainerService/managedClusters/batch/cronjobs/*",
        "Microsoft.ContainerService/managedClusters/coordination.k8s.io/leases/read",
        "Microsoft.ContainerService/managedClusters/coordination.k8s.io/leases/write",
        "Microsoft.ContainerService/managedClusters/coordination.k8s.io/leases/delete",
        "Microsoft.ContainerService/managedClusters/discovery.k8s.io/endpointslices/read",
        "Microsoft.ContainerService/managedClusters/batch/jobs/*",
        "Microsoft.ContainerService/managedClusters/configmaps/*",
        "Microsoft.ContainerService/managedClusters/endpoints/*",
        "Microsoft.ContainerService/managedClusters/events.k8s.io/events/read",
        "Microsoft.ContainerService/managedClusters/events/*",
        "Microsoft.ContainerService/managedClusters/extensions/daemonsets/*",
        "Microsoft.ContainerService/managedClusters/extensions/deployments/*",
        "Microsoft.ContainerService/managedClusters/extensions/ingresses/*",
        "Microsoft.ContainerService/managedClusters/extensions/networkpolicies/*",
        "Microsoft.ContainerService/managedClusters/extensions/replicasets/*",
        "Microsoft.ContainerService/managedClusters/limitranges/read",
        "Microsoft.ContainerService/managedClusters/metrics.k8s.io/pods/read",
        "Microsoft.ContainerService/managedClusters/metrics.k8s.io/nodes/read",
        "Microsoft.ContainerService/managedClusters/namespaces/read",
        "Microsoft.ContainerService/managedClusters/networking.k8s.io/ingresses/*",
        "Microsoft.ContainerService/managedClusters/networking.k8s.io/networkpolicies/*",
        "Microsoft.ContainerService/managedClusters/persistentvolumeclaims/*",
        "Microsoft.ContainerService/managedClusters/pods/*",
        "Microsoft.ContainerService/managedClusters/policy/poddisruptionbudgets/*",
        "Microsoft.ContainerService/managedClusters/replicationcontrollers/*",
        "Microsoft.ContainerService/managedClusters/resourcequotas/read",
        "Microsoft.ContainerService/managedClusters/secrets/*",
        "Microsoft.ContainerService/managedClusters/serviceaccounts/*",
        "Microsoft.ContainerService/managedClusters/services/*"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Kubernetes Service RBAC Writer",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift Cloud Controller Manager

Manage and update the cloud controller manager deployed on top of OpenShift.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/read | Get the properties of a virtual machine |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/backendAddressPools/join/action | Joins a load balancer backend address pool. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/read | Gets a load balancer definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/write | Creates a load balancer or updates an existing load balancer |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/read | Gets a network interface definition.  |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/write | Creates a network interface or updates an existing network interface.  |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/read | Gets a network security group definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/write | Creates a network security group or updates an existing network security group |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPAddresses/join/action | Joins a public IP address. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPAddresses/read | Gets a public IP address definition. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPAddresses/write | Creates a public IP address or updates an existing public IP address.  |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/join/action | Joins a virtual network. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/read | Gets a virtual network subnet definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/inboundNatRules/join/action | Joins a load balancer inbound nat rule. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/join/action | Joins a network security group. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPPrefixes/join/action | Joins a PublicIPPrefix. Not alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/applicationSecurityGroups/joinNetworkSecurityRule/action | Joins a Security Rule to Application Security Groups. Not alertable. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Manage and update the cloud controller manager deployed on top of OpenShift.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/a1f96423-95ce-4224-ab27-4e3dc72facd4",
  "name": "a1f96423-95ce-4224-ab27-4e3dc72facd4",
  "permissions": [
    {
      "actions": [
        "Microsoft.Compute/virtualMachines/read",
        "Microsoft.Network/loadBalancers/backendAddressPools/join/action",
        "Microsoft.Network/loadBalancers/read",
        "Microsoft.Network/loadBalancers/write",
        "Microsoft.Network/networkInterfaces/read",
        "Microsoft.Network/networkInterfaces/write",
        "Microsoft.Network/networkSecurityGroups/read",
        "Microsoft.Network/networkSecurityGroups/write",
        "Microsoft.Network/publicIPAddresses/join/action",
        "Microsoft.Network/publicIPAddresses/read",
        "Microsoft.Network/publicIPAddresses/write",
        "Microsoft.Network/virtualNetworks/subnets/join/action",
        "Microsoft.Network/virtualNetworks/subnets/read",
        "Microsoft.Network/loadBalancers/inboundNatRules/join/action",
        "Microsoft.Network/networkSecurityGroups/join/action",
        "Microsoft.Network/publicIPPrefixes/join/action",
        "Microsoft.Network/applicationSecurityGroups/joinNetworkSecurityRule/action"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift Cloud Controller Manager",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift Cluster Ingress Operator

Manage and configure the OpenShift router.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/dnsZones/A/delete | Remove the record set of a given name and type 'A' from a DNS zone. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/dnsZones/A/write | Create or update a record set of type 'A' within a DNS zone. The records specified will replace the current records in the record set. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/privateDnsZones/A/delete | Remove the record set of a given name and type 'A' from a Private DNS zone. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/privateDnsZones/A/write | Create or update a record set of type 'A' within a Private DNS zone. The records specified will replace the current records in the record set. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/read | Gets a virtual network subnet definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/join/action | Joins a virtual network. Not Alertable. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Manage and configure the OpenShift router.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/0336e1d3-7a87-462b-b6db-342b63f7802c",
  "name": "0336e1d3-7a87-462b-b6db-342b63f7802c",
  "permissions": [
    {
      "actions": [
        "Microsoft.Network/dnsZones/A/delete",
        "Microsoft.Network/dnsZones/A/write",
        "Microsoft.Network/privateDnsZones/A/delete",
        "Microsoft.Network/privateDnsZones/A/write",
        "Microsoft.Network/virtualNetworks/subnets/read",
        "Microsoft.Network/virtualNetworks/subnets/join/action"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift Cluster Ingress Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift Disk Storage Operator

Install Container Storage Interface (CSI) drivers that enable your cluster to use Azure Disks. Set OpenShift cluster-wide storage defaults to ensure a default storageclass exists for clusters.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/write | Creates a new virtual machine or updates an existing virtual machine |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/read | Get the properties of a virtual machine |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachineScaleSets/virtualMachines/write | Updates the properties of a Virtual Machine in a VM Scale Set |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachineScaleSets/virtualMachines/read | Retrieves the properties of a Virtual Machine in a VM Scale Set |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachineScaleSets/read | Get the properties of a Virtual Machine Scale Set |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/snapshots/write | Create a new Snapshot or update an existing one |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/snapshots/read | Get the properties of a Snapshot |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/snapshots/delete | Delete a Snapshot |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/locations/operations/read | Gets the status of an asynchronous operation |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/locations/DiskOperations/read | Gets the status of an asynchronous Disk operation |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/disks/write | Creates a new Disk or updates an existing one |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/disks/read | Get the properties of a Disk |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/disks/delete | Deletes the Disk |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/disks/beginGetAccess/action | Get the SAS URI of the Disk for blob access |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/diskEncryptionSets/read | Get the properties of a disk encryption set |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Install Container Storage Interface (CSI) drivers that enable your cluster to use Azure Disks. Set OpenShift cluster-wide storage defaults to ensure a default storageclass exists for clusters.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/5b7237c5-45e1-49d6-bc18-a1f62f400748",
  "name": "5b7237c5-45e1-49d6-bc18-a1f62f400748",
  "permissions": [
    {
      "actions": [
        "Microsoft.Compute/virtualMachines/write",
        "Microsoft.Compute/virtualMachines/read",
        "Microsoft.Compute/virtualMachineScaleSets/virtualMachines/write",
        "Microsoft.Compute/virtualMachineScaleSets/virtualMachines/read",
        "Microsoft.Compute/virtualMachineScaleSets/read",
        "Microsoft.Compute/snapshots/write",
        "Microsoft.Compute/snapshots/read",
        "Microsoft.Compute/snapshots/delete",
        "Microsoft.Compute/locations/operations/read",
        "Microsoft.Compute/locations/DiskOperations/read",
        "Microsoft.Compute/disks/write",
        "Microsoft.Compute/disks/read",
        "Microsoft.Compute/disks/delete",
        "Microsoft.Compute/disks/beginGetAccess/action",
        "Microsoft.Compute/diskEncryptionSets/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift Disk Storage Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift Federated Credential

Create, update and delete federated credentials on user assigned managed identities in order to build a trust relationship between the managed identity, OpenID Connect (OIDC), and the service account.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ManagedIdentity](../permissions/identity.md#microsoftmanagedidentity)/userAssignedIdentities/read | Gets an existing user assigned identity |
> | [Microsoft.ManagedIdentity](../permissions/identity.md#microsoftmanagedidentity)/userAssignedIdentities/federatedIdentityCredentials/write | Add or update a Federated Identity Credential |
> | [Microsoft.ManagedIdentity](../permissions/identity.md#microsoftmanagedidentity)/userAssignedIdentities/federatedIdentityCredentials/read | Get or list Federated Identity Credentials |
> | [Microsoft.ManagedIdentity](../permissions/identity.md#microsoftmanagedidentity)/userAssignedIdentities/federatedIdentityCredentials/delete | Delete a Federated Identity Credential |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Create, update and delete federated credentials on user assigned managed identities in order to build a trust relationship between the managed identity, OpenID Connect (OIDC), and the service account.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/ef318e2a-8334-4a05-9e4a-295a196c6a6e",
  "name": "ef318e2a-8334-4a05-9e4a-295a196c6a6e",
  "permissions": [
    {
      "actions": [
        "Microsoft.ManagedIdentity/userAssignedIdentities/read",
        "Microsoft.ManagedIdentity/userAssignedIdentities/federatedIdentityCredentials/write",
        "Microsoft.ManagedIdentity/userAssignedIdentities/federatedIdentityCredentials/read",
        "Microsoft.ManagedIdentity/userAssignedIdentities/federatedIdentityCredentials/delete"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift Federated Credential",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift File Storage Operator

Install Container Storage Interface (CSI) drivers that enable your cluster to use Azure Files. Set OpenShift cluster-wide storage defaults to ensure a default storageclass exists for clusters.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/delete | Deletes an existing storage account. |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/fileServices/read | Get file service properties |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/fileServices/shares/delete | Delete file share |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/fileServices/shares/read | List file shares |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/fileServices/shares/write | Create or update file share |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/listKeys/action | Returns the access keys for the specified storage account. |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/read | Returns the list of storage accounts or gets the properties for the specified storage account. |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/write | Creates a storage account with the specified parameters or update the properties or tags or adds custom domain for the specified storage account. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/join/action | Joins a network security group. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/read | Gets a virtual network subnet definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/write | Creates a virtual network subnet or updates an existing virtual network subnet |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/routeTables/join/action | Joins a route table. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/natGateways/join/action | Joins a NAT Gateway |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Install Container Storage Interface (CSI) drivers that enable your cluster to use Azure Files. Set OpenShift cluster-wide storage defaults to ensure a default storageclass exists for clusters.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/0d7aedc0-15fd-4a67-a412-efad370c947e",
  "name": "0d7aedc0-15fd-4a67-a412-efad370c947e",
  "permissions": [
    {
      "actions": [
        "Microsoft.Storage/storageAccounts/delete",
        "Microsoft.Storage/storageAccounts/fileServices/read",
        "Microsoft.Storage/storageAccounts/fileServices/shares/delete",
        "Microsoft.Storage/storageAccounts/fileServices/shares/read",
        "Microsoft.Storage/storageAccounts/fileServices/shares/write",
        "Microsoft.Storage/storageAccounts/listKeys/action",
        "Microsoft.Storage/storageAccounts/read",
        "Microsoft.Storage/storageAccounts/write",
        "Microsoft.Network/networkSecurityGroups/join/action",
        "Microsoft.Network/virtualNetworks/subnets/read",
        "Microsoft.Network/virtualNetworks/subnets/write",
        "Microsoft.Network/routeTables/join/action",
        "Microsoft.Network/natGateways/join/action"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift File Storage Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift Image Registry Operator

Enables permissions for the operator to manage a singleton instance of the OpenShift image registry. It manages all configuration of the registry, including creating storage.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/read | Returns blob service properties or statistics |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/containers/read | Returns list of containers |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/containers/write | Returns the result of put blob container |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/containers/delete | Returns the result of deleting a container |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/generateUserDelegationKey/action | Returns a user delegation key for the blob service |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/read | Returns the list of storage accounts or gets the properties for the specified storage account. |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/write | Creates a storage account with the specified parameters or update the properties or tags or adds custom domain for the specified storage account. |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/delete | Deletes an existing storage account. |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/listKeys/action | Returns the access keys for the specified storage account. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/tags/write | Updates the tags on a resource by replacing or merging existing tags with a new set of tags, or removing existing tags. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/containers/blobs/delete | Returns the result of deleting a blob |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/containers/blobs/write | Returns the result of writing a blob |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/containers/blobs/read | Returns a blob or a list of blobs |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/containers/blobs/add/action | Returns the result of adding blob content |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/blobServices/containers/blobs/move/action | Moves the blob from one path to another |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Enables permissions for the operator to manage a singleton instance of the OpenShift image registry. It manages all configuration of the registry, including creating storage.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/8b32b316-c2f5-4ddf-b05b-83dacd2d08b5",
  "name": "8b32b316-c2f5-4ddf-b05b-83dacd2d08b5",
  "permissions": [
    {
      "actions": [
        "Microsoft.Storage/storageAccounts/blobServices/read",
        "Microsoft.Storage/storageAccounts/blobServices/containers/read",
        "Microsoft.Storage/storageAccounts/blobServices/containers/write",
        "Microsoft.Storage/storageAccounts/blobServices/containers/delete",
        "Microsoft.Storage/storageAccounts/blobServices/generateUserDelegationKey/action",
        "Microsoft.Storage/storageAccounts/read",
        "Microsoft.Storage/storageAccounts/write",
        "Microsoft.Storage/storageAccounts/delete",
        "Microsoft.Storage/storageAccounts/listKeys/action",
        "Microsoft.Resources/tags/write"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/delete",
        "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write",
        "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read",
        "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/add/action",
        "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/move/action"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift Image Registry Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift Machine API Operator

Manage the lifecycle of specific-purpose custom resource definitions (CRD), controllers, and Azure RBAC objects that extend the Kubernetes API to declares the desired state of machines in a cluster.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/availabilitySets/delete | Deletes the availability set |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/availabilitySets/read | Get the properties of an availability set |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/availabilitySets/write | Creates a new availability set or updates an existing one |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/diskEncryptionSets/read | Get the properties of a disk encryption set |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/disks/delete | Deletes the Disk |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/galleries/images/versions/read | Gets the properties of Gallery Image Version |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/skus/read | Gets the list of Microsoft.Compute SKUs available for your Subscription |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/delete | Deletes the virtual machine |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/read | Get the properties of a virtual machine |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/write | Creates a new virtual machine or updates an existing virtual machine |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/capacityReservationGroups/deploy/action | Deploy a new VM/VMSS using Capacity Reservation Group |
> | [Microsoft.ManagedIdentity](../permissions/identity.md#microsoftmanagedidentity)/userAssignedIdentities/assign/action | RBAC action for assigning an existing user assigned identity to a resource |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/applicationSecurityGroups/read | Gets an Application Security Group ID. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/backendAddressPools/join/action | Joins a load balancer backend address pool. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/read | Gets a load balancer definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/write | Creates a load balancer or updates an existing load balancer |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/delete | Deletes a network interface |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/join/action | Joins a Virtual Machine to a network interface. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/loadBalancers/read | Gets all the load balancers that the network interface is part of |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/read | Gets a network interface definition.  |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/write | Creates a network interface or updates an existing network interface.  |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/read | Gets a network security group definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/write | Creates a network security group or updates an existing network security group |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPAddresses/delete | Deletes a public IP address. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPAddresses/join/action | Joins a public IP address. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPAddresses/read | Gets a public IP address definition. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/publicIPAddresses/write | Creates a public IP address or updates an existing public IP address.  |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/routeTables/read | Gets a route table definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/join/action | Joins a virtual network. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/read | Gets a virtual network subnet definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/applicationSecurityGroups/joinNetworkSecurityRule/action | Joins a Security Rule to Application Security Groups. Not alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/frontendIPConfigurations/join/action | Joins a Load Balancer Frontend IP Configuration. Not alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/inboundNATRules/join/action | Joins a load balancer inbound nat rule. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/join/action | Joins a network security group. Not Alertable. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Manage the lifecycle of specific-purpose custom resource definitions (CRD), controllers, and Azure RBAC objects that extend the Kubernetes API to declares the desired state of machines in a cluster.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/0358943c-7e01-48ba-8889-02cc51d78637",
  "name": "0358943c-7e01-48ba-8889-02cc51d78637",
  "permissions": [
    {
      "actions": [
        "Microsoft.Compute/availabilitySets/delete",
        "Microsoft.Compute/availabilitySets/read",
        "Microsoft.Compute/availabilitySets/write",
        "Microsoft.Compute/diskEncryptionSets/read",
        "Microsoft.Compute/disks/delete",
        "Microsoft.Compute/galleries/images/versions/read",
        "Microsoft.Compute/skus/read",
        "Microsoft.Compute/virtualMachines/delete",
        "Microsoft.Compute/virtualMachines/read",
        "Microsoft.Compute/virtualMachines/write",
        "Microsoft.Compute/capacityReservationGroups/deploy/action",
        "Microsoft.ManagedIdentity/userAssignedIdentities/assign/action",
        "Microsoft.Network/applicationSecurityGroups/read",
        "Microsoft.Network/loadBalancers/backendAddressPools/join/action",
        "Microsoft.Network/loadBalancers/read",
        "Microsoft.Network/loadBalancers/write",
        "Microsoft.Network/networkInterfaces/delete",
        "Microsoft.Network/networkInterfaces/join/action",
        "Microsoft.Network/networkInterfaces/loadBalancers/read",
        "Microsoft.Network/networkInterfaces/read",
        "Microsoft.Network/networkInterfaces/write",
        "Microsoft.Network/networkSecurityGroups/read",
        "Microsoft.Network/networkSecurityGroups/write",
        "Microsoft.Network/publicIPAddresses/delete",
        "Microsoft.Network/publicIPAddresses/join/action",
        "Microsoft.Network/publicIPAddresses/read",
        "Microsoft.Network/publicIPAddresses/write",
        "Microsoft.Network/routeTables/read",
        "Microsoft.Network/virtualNetworks/subnets/join/action",
        "Microsoft.Network/virtualNetworks/subnets/read",
        "Microsoft.Network/applicationSecurityGroups/joinNetworkSecurityRule/action",
        "Microsoft.Network/loadBalancers/frontendIPConfigurations/join/action",
        "Microsoft.Network/loadBalancers/inboundNATRules/join/action",
        "Microsoft.Network/networkSecurityGroups/join/action",
        "Microsoft.Resources/subscriptions/resourceGroups/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift Machine API Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift Network Operator

Install and upgrade the networking components on an OpenShift cluster.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/read | Gets a network interface definition.  |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkInterfaces/write | Creates a network interface or updates an existing network interface.  |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/read | Get the virtual network definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/join/action | Joins a virtual network. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/backendAddressPools/join/action | Joins a load balancer backend address pool. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/loadBalancers/backendAddressPools/read | Gets a load balancer backend address pool definition |
> | [Microsoft.Compute](../permissions/compute.md#microsoftcompute)/virtualMachines/read | Get the properties of a virtual machine |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Install and upgrade the networking components on an OpenShift cluster.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/be7a6435-15ae-4171-8f30-4a343eff9e8f",
  "name": "be7a6435-15ae-4171-8f30-4a343eff9e8f",
  "permissions": [
    {
      "actions": [
        "Microsoft.Network/networkInterfaces/read",
        "Microsoft.Network/networkInterfaces/write",
        "Microsoft.Network/virtualNetworks/read",
        "Microsoft.Network/virtualNetworks/subnets/join/action",
        "Microsoft.Network/loadBalancers/backendAddressPools/join/action",
        "Microsoft.Network/loadBalancers/backendAddressPools/read",
        "Microsoft.Compute/virtualMachines/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift Network Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Azure Red Hat OpenShift Service Operator

Maintain machine health, network configuration, monitoring, and other features that are specific to an OpenShift cluster's continued functionality as a managed service.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/read | Gets a virtual network subnet definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/write | Creates a virtual network subnet or updates an existing virtual network subnet |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/natGateways/join/action | Joins a NAT Gateway |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/routeTables/join/action | Joins a route table. Not Alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/networkSecurityGroups/join/action | Joins a network security group. Not Alertable. |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/listKeys/action | Returns the access keys for the specified storage account. |
> | [Microsoft.Storage](../permissions/storage.md#microsoftstorage)/storageAccounts/read | Returns the list of storage accounts or gets the properties for the specified storage account. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Maintain machine health, network configuration, monitoring, and other features that are specific to an OpenShift cluster's continued functionality as a managed service.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/4436bae4-7702-4c84-919b-c4069ff25ee2",
  "name": "4436bae4-7702-4c84-919b-c4069ff25ee2",
  "permissions": [
    {
      "actions": [
        "Microsoft.Network/virtualNetworks/subnets/read",
        "Microsoft.Network/virtualNetworks/subnets/write",
        "Microsoft.Network/natGateways/join/action",
        "Microsoft.Network/routeTables/join/action",
        "Microsoft.Network/networkSecurityGroups/join/action",
        "Microsoft.Storage/storageAccounts/listKeys/action",
        "Microsoft.Storage/storageAccounts/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Azure Red Hat OpenShift Service Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Connected Cluster Managed Identity CheckAccess Reader

Built-in role that allows a Connected Cluster managed identity to call the checkAccess API

[Learn more](/azure/azure-arc/kubernetes/azure-rbac)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Built-in role that allows a Connected Cluster managed identity to call the checkAccess API",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/65a14201-8f6c-4c28-bec4-12619c5a9aaa",
  "name": "65a14201-8f6c-4c28-bec4-12619c5a9aaa",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Connected Cluster Managed Identity CheckAccess Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps ConnectedEnvironments Contributor

Full management of Container Apps ConnectedEnvironments, including creation, deletion, and updates.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/* |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/write |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/delete |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/action |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/daprComponents/listSecrets/action | List Secrets of a Dapr Component |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Full management of Container Apps ConnectedEnvironments, including creation, deletion, and updates.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/6f4fe6fc-f04f-4d97-8528-8bc18c848dca",
  "name": "6f4fe6fc-f04f-4d97-8528-8bc18c848dca",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.App/connectedEnvironments/*",
        "Microsoft.App/connectedEnvironments/*/read",
        "Microsoft.App/connectedEnvironments/*/write",
        "Microsoft.App/connectedEnvironments/*/delete",
        "Microsoft.App/connectedEnvironments/*/action",
        "Microsoft.App/connectedEnvironments/daprComponents/listSecrets/action",
        "Microsoft.Resources/deployments/*"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps ConnectedEnvironments Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps ConnectedEnvironments Reader

Read access to Container Apps ConnectedEnvironments.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/read | Get a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/read |  |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Read access to Container Apps ConnectedEnvironments.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/d5adeb5b-107f-4aca-99ea-4e3f4fc008d5",
  "name": "d5adeb5b-107f-4aca-99ea-4e3f4fc008d5",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/*",
        "Microsoft.App/connectedEnvironments/read",
        "Microsoft.App/connectedEnvironments/*/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps ConnectedEnvironments Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps Contributor

Full management of Container Apps, including creation, deletion, and updates.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/*/write |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/*/delete |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/*/action |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/read | Get a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/join/action | Allows to create a Container App in a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/checknameavailability/action | Check reource name availability for a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/read | Get a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/join/action | Allows to create a Container App or Container Apps Job in a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/checknameavailability/action | Check reource name availability for a Connected Environment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Full management of Container Apps, including creation, deletion, and updates.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/358470bc-b998-42bd-ab17-a7e34c199c0f",
  "name": "358470bc-b998-42bd-ab17-a7e34c199c0f",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.App/containerApps/*/read",
        "Microsoft.App/containerApps/*/write",
        "Microsoft.App/containerApps/*/delete",
        "Microsoft.App/containerApps/*/action",
        "Microsoft.App/managedEnvironments/read",
        "Microsoft.App/managedEnvironments/*/read",
        "Microsoft.App/managedEnvironments/join/action",
        "Microsoft.App/managedEnvironments/checknameavailability/action",
        "Microsoft.App/connectedEnvironments/read",
        "Microsoft.App/connectedEnvironments/*/read",
        "Microsoft.App/connectedEnvironments/join/action",
        "Microsoft.App/connectedEnvironments/checknameavailability/action"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps Jobs Contributor

Full management of Container Apps jobs, including creation, deletion, and updates.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [microsoft.app](../permissions/compute.md#microsoftapp)/jobs/read | Get a Container Apps Job |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/*/action |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/write | Create or update a Container Apps Job |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/delete | Delete a Container Apps Job |
> | [Microsoft.app](../permissions/compute.md#microsoftapp)/managedenvironments/read | Get a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedenvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedenvironments/join/action | Allows to create a Container App in a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedenvironments/checknameavailability/action | Check reource name availability for a Managed Environment |
> | [Microsoft.app](../permissions/compute.md#microsoftapp)/connectedEnvironments/read | Get a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/join/action | Allows to create a Container App or Container Apps Job in a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/checknameavailability/action | Check reource name availability for a Connected Environment |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Full management of Container Apps jobs, including creation, deletion, and updates.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/4e3d2b60-56ae-4dc6-a233-09c8e5a82e68",
  "name": "4e3d2b60-56ae-4dc6-a233-09c8e5a82e68",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "microsoft.app/jobs/read",
        "Microsoft.App/jobs/*/read",
        "Microsoft.App/jobs/*/action",
        "Microsoft.App/jobs/write",
        "Microsoft.App/jobs/delete",
        "Microsoft.app/managedenvironments/read",
        "Microsoft.App/managedenvironments/*/read",
        "Microsoft.App/managedenvironments/join/action",
        "Microsoft.App/managedenvironments/checknameavailability/action",
        "Microsoft.app/connectedEnvironments/read",
        "Microsoft.App/connectedEnvironments/*/read",
        "Microsoft.App/connectedEnvironments/join/action",
        "Microsoft.App/connectedEnvironments/checknameavailability/action",
        "Microsoft.Resources/deployments/*"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps Jobs Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps Jobs Operator

Read, start, and stop Container Apps jobs.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [microsoft.app](../permissions/compute.md#microsoftapp)/jobs/read | Get a Container Apps Job |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/*/action |  |
> | [Microsoft.app](../permissions/compute.md#microsoftapp)/managedenvironments/read | Get a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedenvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedenvironments/join/action | Allows to create a Container App in a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedenvironments/checknameavailability/action | Check reource name availability for a Managed Environment |
> | [Microsoft.app](../permissions/compute.md#microsoftapp)/connectedEnvironments/read | Get a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/join/action | Allows to create a Container App or Container Apps Job in a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/checknameavailability/action | Check reource name availability for a Connected Environment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/logstream/action | View log stream of a container app job |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/exec/action | Connect to console of a container app job |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Read, start, and stop Container Apps jobs.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/b9a307c4-5aa3-4b52-ba60-2b17c136cd7b",
  "name": "b9a307c4-5aa3-4b52-ba60-2b17c136cd7b",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "microsoft.app/jobs/read",
        "Microsoft.App/jobs/*/read",
        "Microsoft.App/jobs/*/action",
        "Microsoft.app/managedenvironments/read",
        "Microsoft.App/managedenvironments/*/read",
        "Microsoft.App/managedenvironments/join/action",
        "Microsoft.App/managedenvironments/checknameavailability/action",
        "Microsoft.app/connectedEnvironments/read",
        "Microsoft.App/connectedEnvironments/*/read",
        "Microsoft.App/connectedEnvironments/join/action",
        "Microsoft.App/connectedEnvironments/checknameavailability/action"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.App/jobs/logstream/action",
        "Microsoft.App/jobs/exec/action"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps Jobs Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps Jobs Reader

Read access to ContainerApps jobs

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [microsoft.app](../permissions/compute.md#microsoftapp)/jobs/read | Get a Container Apps Job |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/jobs/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedenvironments/read | Get a Managed Environment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Read access to ContainerApps jobs",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/edd66693-d32a-450b-997d-0158c03976b0",
  "name": "edd66693-d32a-450b-997d-0158c03976b0",
  "permissions": [
    {
      "actions": [
        "microsoft.app/jobs/read",
        "Microsoft.App/jobs/*/read",
        "Microsoft.App/managedenvironments/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps Jobs Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps ManagedEnvironments Contributor

Full management of Container Apps ManagedEnvironments, including creation, deletion, and updates.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/*/write |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/*/delete |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/*/action |  |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Full management of Container Apps ManagedEnvironments, including creation, deletion, and updates.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/57cc5028-e6a7-4284-868d-0611c5923f8d",
  "name": "57cc5028-e6a7-4284-868d-0611c5923f8d",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.App/managedEnvironments/*/read",
        "Microsoft.App/managedEnvironments/*/write",
        "Microsoft.App/managedEnvironments/*/delete",
        "Microsoft.App/managedEnvironments/*/action",
        "Microsoft.Resources/deployments/*"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps ManagedEnvironments Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps ManagedEnvironments Reader

Read access to ContainerApps managedenvironments.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/*/read |  |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Read access to ContainerApps managedenvironments.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/1b32c00b-7eff-4c22-93e6-93d11d72d2d8",
  "name": "1b32c00b-7eff-4c22-93e6-93d11d72d2d8",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.App/managedEnvironments/*/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps ManagedEnvironments Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps Operator

Read, logstream and exec into Container Apps.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/*/action |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/read | Get a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/join/action | Allows to create a Container App in a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/checknameavailability/action | Check reource name availability for a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/read | Get a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/join/action | Allows to create a Container App or Container Apps Job in a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/checknameavailability/action | Check reource name availability for a Connected Environment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/logstream/action | View log stream of a container app |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/exec/action | Connect to console of a container app |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/containerApps/debug/action | Connect to debug console of a container app |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Read, logstream and exec into Container Apps.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/f3bd1b5c-91fa-40e7-afe7-0c11d331232c",
  "name": "f3bd1b5c-91fa-40e7-afe7-0c11d331232c",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.App/containerApps/*/read",
        "Microsoft.App/containerApps/*/action",
        "Microsoft.App/managedEnvironments/read",
        "Microsoft.App/managedEnvironments/*/read",
        "Microsoft.App/managedEnvironments/join/action",
        "Microsoft.App/managedEnvironments/checknameavailability/action",
        "Microsoft.App/connectedEnvironments/read",
        "Microsoft.App/connectedEnvironments/*/read",
        "Microsoft.App/connectedEnvironments/join/action",
        "Microsoft.App/connectedEnvironments/checknameavailability/action"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.App/containerApps/logstream/action",
        "Microsoft.App/containerApps/exec/action",
        "Microsoft.App/containerApps/debug/action"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps SessionPools Contributor

Full management of Container Apps SessionPools, including creation, deletion, and updates.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/sessionPools/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/sessionPools/*/write |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/sessionPools/*/delete |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/sessionPools/*/action |  |
> | [microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/read | Get a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/join/action | Allows to create a Container App in a Managed Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/managedEnvironments/checknameavailability/action | Check reource name availability for a Managed Environment |
> | [microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/read | Get a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/*/read |  |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/join/action | Allows to create a Container App or Container Apps Job in a Connected Environment |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/connectedEnvironments/checknameavailability/action | Check reource name availability for a Connected Environment |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Full management of Container Apps SessionPools, including creation, deletion, and updates.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/f7669afb-68b2-44b4-9c5f-6d2a47fddda0",
  "name": "f7669afb-68b2-44b4-9c5f-6d2a47fddda0",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.App/sessionPools/*/read",
        "Microsoft.App/sessionPools/*/write",
        "Microsoft.App/sessionPools/*/delete",
        "Microsoft.App/sessionPools/*/action",
        "microsoft.App/managedEnvironments/read",
        "Microsoft.App/managedEnvironments/*/read",
        "Microsoft.App/managedEnvironments/join/action",
        "Microsoft.App/managedEnvironments/checknameavailability/action",
        "microsoft.App/connectedEnvironments/read",
        "Microsoft.App/connectedEnvironments/*/read",
        "Microsoft.App/connectedEnvironments/join/action",
        "Microsoft.App/connectedEnvironments/checknameavailability/action",
        "Microsoft.Resources/deployments/*"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps SessionPools Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Apps SessionPools Reader

Read access to ContainerApps sessionpools.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.App](../permissions/compute.md#microsoftapp)/sessionPools/*/read |  |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Read access to ContainerApps sessionpools.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/af61e8fc-2633-4b95-bed3-421ad6826515",
  "name": "af61e8fc-2633-4b95-bed3-421ad6826515",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.App/sessionPools/*/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Apps SessionPools Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Cache Rule Administrator

Create, Read, Update, and Delete Cache Rules in Container Registry. This role doesn't grant permissions to manage Credential Sets.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/cacheRules/read | Gets the properties of the specified cache rule or lists all the cache rules for the specified container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/cacheRules/write | Creates or updates a cache rule for a container registry with the specified parameters |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/cacheRules/delete | Deletes a cache rule from a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/cacheRules/operationStatuses/read | Gets a cache rule async operation status |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Create, Read, Update, and Delete Cache Rules in Container Registry. This role doesn't grant permissions to manage Credential Sets.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/df87f177-bb12-4db1-9793-a413691eff94",
  "name": "df87f177-bb12-4db1-9793-a413691eff94",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/cacheRules/read",
        "Microsoft.ContainerRegistry/registries/cacheRules/write",
        "Microsoft.ContainerRegistry/registries/cacheRules/delete",
        "Microsoft.ContainerRegistry/registries/cacheRules/operationStatuses/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Cache Rule Administrator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Cache Rule Reader

Read the configuration of Cache Rules in Container Registry. This permission doesn't grant permission to read Credential Sets.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/cacheRules/read | Gets the properties of the specified cache rule or lists all the cache rules for the specified container registry |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Read the configuration of Cache Rules in Container Registry. This permission doesn't grant permission to read Credential Sets.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/c357b964-0002-4b64-a50d-7a28f02edc52",
  "name": "c357b964-0002-4b64-a50d-7a28f02edc52",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/cacheRules/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Cache Rule Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Configuration Reader and Data Access Configuration Reader

Provides permissions to list container registries and registry configuration properties. Provides permissions to list data access configuration such as admin user credentials, scope maps, and tokens, which can be used to read, write or delete repositories and images. Does not provide direct permissions to read, list, or write registry contents including repositories and images. Does not provide permissions to modify data plane content such as imports, Artifact Cache or Sync, and Transfer Pipelines. Does not provide permissions for managing Tasks.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/operationStatuses/read | Gets a registry async operation status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/read | Gets the properties of the specified container registry or lists all the container registries under the specified resource group or subscription. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/privateEndpointConnections/read | Gets the properties of private endpoint connection or list all the private endpoint connections for the specified container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/privateEndpointConnections/operationStatuses/read | Get Private Endpoint Connection Async Operation Status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/listCredentials/action | Lists the login credentials for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tokens/read | Gets the properties of the specified token or lists all the tokens for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tokens/operationStatuses/read | Gets a token async operation status. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/scopeMaps/read | Gets the properties of the specified scope map or lists all the scope maps for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/scopeMaps/operationStatuses/read | Gets a scope map async operation status. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/read | Gets the properties of the specified webhook or lists all the webhooks for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/getCallbackConfig/action | Gets the configuration of service URI and custom headers for the webhook. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/listEvents/action | Lists recent events for the specified webhook. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/operationStatuses/read | Gets a webhook async operation status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/replications/read | Gets the properties of the specified replication or lists all the replications for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/replications/operationStatuses/read | Gets a replication async operation status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/connectedRegistries/read | Gets the properties of the specified connected registry or lists all the connected registries for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Microsoft ContainerRegistry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Microsoft ContainerRegistry |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Write | Create or update a classic metric alert |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Delete | Delete a classic metric alert |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Read | Read a classic metric alert |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Activated/Action | Classic metric alert activated |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Resolved/Action | Classic metric alert resolved |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Throttled/Action | Classic metric alert rule throttled |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Incidents/Read | Read a classic metric alert incident |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Provides permissions to list container registries and registry configuration properties. Provides permissions to list data access configuration such as admin user credentials, scope maps, and tokens, which can be used to read, write or delete repositories and images. Does not provide direct permissions to read, list, or write registry contents including repositories and images. Does not provide permissions to modify data plane content such as imports, Artifact Cache or Sync, and Transfer Pipelines. Does not provide permissions for managing Tasks.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/69b07be0-09bf-439a-b9a6-e73de851bd59",
  "name": "69b07be0-09bf-439a-b9a6-e73de851bd59",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/read",
        "Microsoft.ContainerRegistry/registries/privateEndpointConnections/read",
        "Microsoft.ContainerRegistry/registries/privateEndpointConnections/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/listCredentials/action",
        "Microsoft.ContainerRegistry/registries/tokens/read",
        "Microsoft.ContainerRegistry/registries/tokens/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/scopeMaps/read",
        "Microsoft.ContainerRegistry/registries/scopeMaps/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/webhooks/read",
        "Microsoft.ContainerRegistry/registries/webhooks/getCallbackConfig/action",
        "Microsoft.ContainerRegistry/registries/webhooks/listEvents/action",
        "Microsoft.ContainerRegistry/registries/webhooks/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/replications/read",
        "Microsoft.ContainerRegistry/registries/replications/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/connectedRegistries/read",
        "Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/diagnosticSettings/read",
        "Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/diagnosticSettings/write",
        "Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/logDefinitions/read",
        "Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/metricDefinitions/read",
        "Microsoft.Insights/AlertRules/Write",
        "Microsoft.Insights/AlertRules/Delete",
        "Microsoft.Insights/AlertRules/Read",
        "Microsoft.Insights/AlertRules/Activated/Action",
        "Microsoft.Insights/AlertRules/Resolved/Action",
        "Microsoft.Insights/AlertRules/Throttled/Action",
        "Microsoft.Insights/AlertRules/Incidents/Read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Configuration Reader and Data Access Configuration Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Contributor and Data Access Configuration Administrator

Provides permissions to create, list, and update container registries and registry configuration properties. Provides permissions to configure data access such as admin user credentials, scope maps, and tokens, which can be used to read, write or delete repositories and images. Does not provide direct permissions to read, list, or write registry contents including repositories and images. Does not provide permissions to modify data plane content such as imports, Artifact Cache or Sync, and Transfer Pipelines. Does not provide permissions for managing Tasks.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/operationStatuses/read | Gets a registry async operation status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/read | Gets the properties of the specified container registry or lists all the container registries under the specified resource group or subscription. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/write | Creates or updates a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/delete | Deletes a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/listCredentials/action | Lists the login credentials for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/regenerateCredential/action | Regenerates one of the login credentials for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/generateCredentials/action | Generate keys for a token of a specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/replications/read | Gets the properties of the specified replication or lists all the replications for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/replications/write | Creates or updates a replication for a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/replications/delete | Deletes a replication from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/replications/operationStatuses/read | Gets a replication async operation status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/privateEndpointConnectionsApproval/action | Auto Approves a Private Endpoint Connection |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/privateEndpointConnections/read | Gets the properties of private endpoint connection or list all the private endpoint connections for the specified container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/privateEndpointConnections/write | Approves/Rejects the private endpoint connection |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/privateEndpointConnections/delete | Deletes the private endpoint connection |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/privateEndpointConnections/operationStatuses/read | Get Private Endpoint Connection Async Operation Status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tokens/read | Gets the properties of the specified token or lists all the tokens for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tokens/write | Creates or updates a token for a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tokens/delete | Deletes a token from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tokens/operationStatuses/read | Gets a token async operation status. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/scopeMaps/read | Gets the properties of the specified scope map or lists all the scope maps for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/scopeMaps/write | Creates or updates a scope map for a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/scopeMaps/delete | Deletes a scope map from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/scopeMaps/operationStatuses/read | Gets a scope map async operation status. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Microsoft ContainerRegistry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Microsoft ContainerRegistry |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/connectedRegistries/read | Gets the properties of the specified connected registry or lists all the connected registries for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/connectedRegistries/write | Creates or updates a connected registry for a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/connectedRegistries/delete | Deletes a connected registry from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/connectedRegistries/deactivate/action | Deactivates a connected registry for a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/read | Gets the properties of the specified webhook or lists all the webhooks for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/write | Creates or updates a webhook for a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/delete | Deletes a webhook from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/getCallbackConfig/action | Gets the configuration of service URI and custom headers for the webhook. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/ping/action | Triggers a ping event to be sent to the webhook. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/listEvents/action | Lists recent events for the specified webhook. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/webhooks/operationStatuses/read | Gets a webhook async operation status |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Write | Create or update a classic metric alert |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Delete | Delete a classic metric alert |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Read | Read a classic metric alert |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Activated/Action | Classic metric alert activated |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Resolved/Action | Classic metric alert resolved |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Throttled/Action | Classic metric alert rule throttled |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/AlertRules/Incidents/Read | Read a classic metric alert incident |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/locations/operationResults/read | Gets an async operation result |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/joinViaServiceEndpoint/action | Joins resource such as storage account or SQL database to a subnet. Not alertable. |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/read | Gets a virtual network subnet definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/subnets/write | Creates a virtual network subnet or updates an existing virtual network subnet |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/virtualNetworks/read | Get the virtual network definition |
> | [Microsoft.Network](../permissions/networking.md#microsoftnetwork)/privateEndpoints/privateLinkServiceProxies/write | Creates a new private link service proxy, or updates an existing private link service proxy. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Provides permissions to create, list, and update container registries and registry configuration properties. Provides permissions to configure data access such as admin user credentials, scope maps, and tokens, which can be used to read, write or delete repositories and images. Does not provide direct permissions to read, list, or write registry contents including repositories and images. Does not provide permissions to modify data plane content such as imports, Artifact Cache or Sync, and Transfer Pipelines. Does not provide permissions for managing Tasks.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/3bc748fc-213d-45c1-8d91-9da5725539b9",
  "name": "3bc748fc-213d-45c1-8d91-9da5725539b9",
  "permissions": [
    {
      "actions": [
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.ContainerRegistry/registries/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/read",
        "Microsoft.ContainerRegistry/registries/write",
        "Microsoft.ContainerRegistry/registries/delete",
        "Microsoft.ContainerRegistry/registries/listCredentials/action",
        "Microsoft.ContainerRegistry/registries/regenerateCredential/action",
        "Microsoft.ContainerRegistry/registries/generateCredentials/action",
        "Microsoft.ContainerRegistry/registries/replications/read",
        "Microsoft.ContainerRegistry/registries/replications/write",
        "Microsoft.ContainerRegistry/registries/replications/delete",
        "Microsoft.ContainerRegistry/registries/replications/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/privateEndpointConnectionsApproval/action",
        "Microsoft.ContainerRegistry/registries/privateEndpointConnections/read",
        "Microsoft.ContainerRegistry/registries/privateEndpointConnections/write",
        "Microsoft.ContainerRegistry/registries/privateEndpointConnections/delete",
        "Microsoft.ContainerRegistry/registries/privateEndpointConnections/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/tokens/read",
        "Microsoft.ContainerRegistry/registries/tokens/write",
        "Microsoft.ContainerRegistry/registries/tokens/delete",
        "Microsoft.ContainerRegistry/registries/tokens/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/scopeMaps/read",
        "Microsoft.ContainerRegistry/registries/scopeMaps/write",
        "Microsoft.ContainerRegistry/registries/scopeMaps/delete",
        "Microsoft.ContainerRegistry/registries/scopeMaps/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/diagnosticSettings/read",
        "Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/diagnosticSettings/write",
        "Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/logDefinitions/read",
        "Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/metricDefinitions/read",
        "Microsoft.Resources/deployments/*",
        "Microsoft.Authorization/*/read",
        "Microsoft.ContainerRegistry/registries/connectedRegistries/read",
        "Microsoft.ContainerRegistry/registries/connectedRegistries/write",
        "Microsoft.ContainerRegistry/registries/connectedRegistries/delete",
        "Microsoft.ContainerRegistry/registries/connectedRegistries/deactivate/action",
        "Microsoft.ContainerRegistry/registries/webhooks/read",
        "Microsoft.ContainerRegistry/registries/webhooks/write",
        "Microsoft.ContainerRegistry/registries/webhooks/delete",
        "Microsoft.ContainerRegistry/registries/webhooks/getCallbackConfig/action",
        "Microsoft.ContainerRegistry/registries/webhooks/ping/action",
        "Microsoft.ContainerRegistry/registries/webhooks/listEvents/action",
        "Microsoft.ContainerRegistry/registries/webhooks/operationStatuses/read",
        "Microsoft.Insights/AlertRules/Write",
        "Microsoft.Insights/AlertRules/Delete",
        "Microsoft.Insights/AlertRules/Read",
        "Microsoft.Insights/AlertRules/Activated/Action",
        "Microsoft.Insights/AlertRules/Resolved/Action",
        "Microsoft.Insights/AlertRules/Throttled/Action",
        "Microsoft.Insights/AlertRules/Incidents/Read",
        "Microsoft.ContainerRegistry/locations/operationResults/read",
        "Microsoft.Network/virtualNetworks/subnets/joinViaServiceEndpoint/action",
        "Microsoft.Network/virtualNetworks/subnets/read",
        "Microsoft.Network/virtualNetworks/subnets/write",
        "Microsoft.Network/virtualNetworks/read",
        "Microsoft.Network/privateEndpoints/privateLinkServiceProxies/write"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Contributor and Data Access Configuration Administrator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Credential Set Administrator

Create, Read, Update, and Delete Credential Sets in Container Registry. This role doesn't affect the needed permissions for storing content inside Azure Key Vault. This role also doesn't grant permissions to manage Cache Rules.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/credentialSets/read | Gets the properties of the specified credential set or lists all the credential sets for the specified container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/credentialSets/write | Creates or updates a credential set for a container registry with the specified parameters |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/credentialSets/delete | Deletes a credential set from a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/credentialSets/operationStatuses/read | Gets a credential set async operation status |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Create, Read, Update, and Delete Credential Sets in Container Registry. This role doesn't affect the needed permissions for storing content inside Azure Key Vault. This role also doesn't grant permissions to manage Cache Rules.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/f094fb07-0703-4400-ad6a-e16dd8000e14",
  "name": "f094fb07-0703-4400-ad6a-e16dd8000e14",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/credentialSets/read",
        "Microsoft.ContainerRegistry/registries/credentialSets/write",
        "Microsoft.ContainerRegistry/registries/credentialSets/delete",
        "Microsoft.ContainerRegistry/registries/credentialSets/operationStatuses/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Credential Set Administrator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Credential Set Reader

Read the configuration of Credential Sets in Container Registry. This permission doesn't allow permission to see content inside Azure Key vault only the content inside Container Registry. This permission doesn't grant permission to read Cache Rules.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/credentialSets/read | Gets the properties of the specified credential set or lists all the credential sets for the specified container registry |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Read the configuration of Credential Sets in Container Registry. This permission doesn't allow permission to see content inside Azure Key vault only the content inside Container Registry. This permission doesn't grant permission to read Cache Rules.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/29093635-9924-4f2c-913b-650a12949526",
  "name": "29093635-9924-4f2c-913b-650a12949526",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/credentialSets/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Credential Set Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Data Importer and Data Reader

Provides the ability to import images into a registry through the registry import operation. Provides the ability to list repositories, view images and tags, get manifests, and pull images. Does not provide permissions for importing images through configuring registry transfer pipelines such as import and export pipelines. Does not provide permissions for importing through configuring Artifact Cache or Sync rules.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/importImage/action | Import Image to container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/read | Gets the properties of the specified container registry or lists all the container registries under the specified resource group or subscription. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/pull/read | Pull or Get images from a container registry. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/content/read | Pull or Get images from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/metadata/read | Gets the metadata of a specific repository for a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/catalog/read | List repositories in a container registry. |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Provides the ability to import images into a registry through the registry import operation. Provides the ability to list repositories, view images and tags, get manifests, and pull images. Does not provide permissions for importing images through configuring registry transfer pipelines such as import and export pipelines. Does not provide permissions for importing through configuring Artifact Cache or Sync rules.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/577a9874-89fd-4f24-9dbd-b5034d0ad23a",
  "name": "577a9874-89fd-4f24-9dbd-b5034d0ad23a",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/importImage/action",
        "Microsoft.ContainerRegistry/registries/read",
        "Microsoft.ContainerRegistry/registries/pull/read"
      ],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerRegistry/registries/repositories/content/read",
        "Microsoft.ContainerRegistry/registries/repositories/metadata/read",
        "Microsoft.ContainerRegistry/registries/catalog/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Data Importer and Data Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Repository Catalog Lister

Allows for listing all repositories in an Azure Container Registry. This role is in preview and subject to change.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | *none* |  |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/catalog/read | List repositories in a container registry. |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Allows for listing all repositories in an Azure Container Registry. This role is in preview and subject to change.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/bfdb9389-c9a5-478a-bb2f-ba9ca092c3c7",
  "name": "bfdb9389-c9a5-478a-bb2f-ba9ca092c3c7",
  "permissions": [
    {
      "actions": [],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerRegistry/registries/catalog/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Repository Catalog Lister",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Repository Contributor

Allows for read, write, and delete access to Azure Container Registry repositories, but excluding catalog listing. This role is in preview and subject to change.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | *none* |  |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/metadata/read | Gets the metadata of a specific repository for a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/content/read | Pull or Get images from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/metadata/write | Updates the metadata of a repository for a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/content/write | Push or Write images to a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/metadata/delete | Delete the metadata of a repository for a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/content/delete | Delete artifact in a container registry. |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Allows for read, write, and delete access to Azure Container Registry repositories, but excluding catalog listing. This role is in preview and subject to change.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/2efddaa5-3f1f-4df3-97df-af3f13818f4c",
  "name": "2efddaa5-3f1f-4df3-97df-af3f13818f4c",
  "permissions": [
    {
      "actions": [],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerRegistry/registries/repositories/metadata/read",
        "Microsoft.ContainerRegistry/registries/repositories/content/read",
        "Microsoft.ContainerRegistry/registries/repositories/metadata/write",
        "Microsoft.ContainerRegistry/registries/repositories/content/write",
        "Microsoft.ContainerRegistry/registries/repositories/metadata/delete",
        "Microsoft.ContainerRegistry/registries/repositories/content/delete"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Repository Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Repository Reader

Allows for read access to Azure Container Registry repositories, but excluding catalog listing. This role is in preview and subject to change.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | *none* |  |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/metadata/read | Gets the metadata of a specific repository for a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/content/read | Pull or Get images from a container registry. |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Allows for read access to Azure Container Registry repositories, but excluding catalog listing. This role is in preview and subject to change.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/b93aa761-3e63-49ed-ac28-beffa264f7ac",
  "name": "b93aa761-3e63-49ed-ac28-beffa264f7ac",
  "permissions": [
    {
      "actions": [],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerRegistry/registries/repositories/metadata/read",
        "Microsoft.ContainerRegistry/registries/repositories/content/read"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Repository Reader",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Repository Writer

Allows for read and write access to Azure Container Registry repositories, but excluding catalog listing. This role is in preview and subject to change.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | *none* |  |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/metadata/read | Gets the metadata of a specific repository for a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/content/read | Pull or Get images from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/metadata/write | Updates the metadata of a repository for a container registry |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/repositories/content/write | Push or Write images to a container registry. |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Allows for read and write access to Azure Container Registry repositories, but excluding catalog listing. This role is in preview and subject to change.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/2a1e307c-b015-4ebd-883e-5b7698a07328",
  "name": "2a1e307c-b015-4ebd-883e-5b7698a07328",
  "permissions": [
    {
      "actions": [],
      "notActions": [],
      "dataActions": [
        "Microsoft.ContainerRegistry/registries/repositories/metadata/read",
        "Microsoft.ContainerRegistry/registries/repositories/content/read",
        "Microsoft.ContainerRegistry/registries/repositories/metadata/write",
        "Microsoft.ContainerRegistry/registries/repositories/content/write"
      ],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Repository Writer",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Tasks Contributor

Provides permissions to configure, read, list, trigger, or cancel Container Registry Tasks, Task Runs, Task Logs, Quick Runs, Quick Builds, and Task Agent Pools. Permissions granted for Tasks management can be used for full registry data plane permissions including reading/writing/deleting container images in registries. Permissions granted for Tasks management can also be used to run customer authored build directives and run scripts to build software artifacts.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/agentpools/read | Get a agentpool for a container registry or list all agentpools. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/agentpools/write | Create or Update an agentpool for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/agentpools/delete | Delete an agentpool for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/agentpools/listQueueStatus/action | List all queue status of an agentpool for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/agentpools/operationResults/status/read | Gets an agentpool async operation result status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/agentpools/operationStatuses/read | Gets an agentpool async operation status |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tasks/read | Gets a task for a container registry or list all tasks. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tasks/write | Creates or Updates a task for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tasks/delete | Deletes a task for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/tasks/listDetails/action | List all details of a task for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/scheduleRun/action | Schedule a run against a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/listBuildSourceUploadUrl/action | Get source upload url location for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/runs/read | Gets the properties of a run against a container registry or list runs. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/runs/write | Updates a run. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/runs/listLogSasUrl/action | Gets the log SAS URL for a run. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/runs/cancel/action | Cancel an existing run. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/taskruns/read | Get a taskrun for a container registry or list all taskruns. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/taskruns/write | Create or Update a taskrun for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/taskruns/delete | Delete a taskrun for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/taskruns/listDetails/action | List all details of a taskrun for a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/taskruns/operationStatuses/read | Gets a taskrun async operation status |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/read | Gets the properties of the specified container registry or lists all the container registries under the specified resource group or subscription. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Provides permissions to configure, read, list, trigger, or cancel Container Registry Tasks, Task Runs, Task Logs, Quick Runs, Quick Builds, and Task Agent Pools. Permissions granted for Tasks management can be used for full registry data plane permissions including reading/writing/deleting container images in registries. Permissions granted for Tasks management can also be used to run customer authored build directives and run scripts to build software artifacts.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/fb382eab-e894-4461-af04-94435c366c3f",
  "name": "fb382eab-e894-4461-af04-94435c366c3f",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/agentpools/read",
        "Microsoft.ContainerRegistry/registries/agentpools/write",
        "Microsoft.ContainerRegistry/registries/agentpools/delete",
        "Microsoft.ContainerRegistry/registries/agentpools/listQueueStatus/action",
        "Microsoft.ContainerRegistry/registries/agentpools/operationResults/status/read",
        "Microsoft.ContainerRegistry/registries/agentpools/operationStatuses/read",
        "Microsoft.ContainerRegistry/registries/tasks/read",
        "Microsoft.ContainerRegistry/registries/tasks/write",
        "Microsoft.ContainerRegistry/registries/tasks/delete",
        "Microsoft.ContainerRegistry/registries/tasks/listDetails/action",
        "Microsoft.ContainerRegistry/registries/scheduleRun/action",
        "Microsoft.ContainerRegistry/registries/listBuildSourceUploadUrl/action",
        "Microsoft.ContainerRegistry/registries/runs/read",
        "Microsoft.ContainerRegistry/registries/runs/write",
        "Microsoft.ContainerRegistry/registries/runs/listLogSasUrl/action",
        "Microsoft.ContainerRegistry/registries/runs/cancel/action",
        "Microsoft.ContainerRegistry/registries/taskruns/read",
        "Microsoft.ContainerRegistry/registries/taskruns/write",
        "Microsoft.ContainerRegistry/registries/taskruns/delete",
        "Microsoft.ContainerRegistry/registries/taskruns/listDetails/action",
        "Microsoft.ContainerRegistry/registries/taskruns/operationStatuses/read",
        "Microsoft.Resources/deployments/*",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.ContainerRegistry/registries/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Tasks Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Container Registry Transfer Pipeline Contributor

Provides the ability to transfer, import, and export artifacts through configuring registry transfer pipelines that involve intermediary storage accounts and key vaults. Does not provide permissions to push or pull images. Does not provide permissions to create, manage, or list storage accounts or key vaults. Does not provide permissions to perform role assignments.

[Learn more](/azure/container-registry/container-registry-rbac-built-in-roles-directory-reference)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/exportPipelines/read | Gets the properties of the specified export pipeline or lists all the export pipelines for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/exportPipelines/write | Creates or updates an export pipeline for a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/exportPipelines/delete | Deletes an export pipeline from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/importPipelines/read | Gets the properties of the specified import pipeline or lists all the import pipelines for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/importPipelines/write | Creates or updates an import pipeline for a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/importPipelines/delete | Deletes an import pipeline from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/pipelineRuns/read | Gets the properties of the specified pipeline run or lists all the pipeline runs for the specified container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/pipelineRuns/write | Creates or updates a pipeline run for a container registry with the specified parameters. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/pipelineRuns/delete | Deletes a pipeline run from a container registry. |
> | [Microsoft.ContainerRegistry](../permissions/containers.md#microsoftcontainerregistry)/registries/pipelineRuns/operationStatuses/read | Gets a pipeline run async operation status. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Provides the ability to transfer, import, and export artifacts through configuring registry transfer pipelines that involve intermediary storage accounts and key vaults. Does not provide permissions to push or pull images. Does not provide permissions to create, manage, or list storage accounts or key vaults. Does not provide permissions to perform role assignments.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/bf94e731-3a51-4a7c-8c54-a1ab9971dfc1",
  "name": "bf94e731-3a51-4a7c-8c54-a1ab9971dfc1",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerRegistry/registries/exportPipelines/read",
        "Microsoft.ContainerRegistry/registries/exportPipelines/write",
        "Microsoft.ContainerRegistry/registries/exportPipelines/delete",
        "Microsoft.ContainerRegistry/registries/importPipelines/read",
        "Microsoft.ContainerRegistry/registries/importPipelines/write",
        "Microsoft.ContainerRegistry/registries/importPipelines/delete",
        "Microsoft.ContainerRegistry/registries/pipelineRuns/read",
        "Microsoft.ContainerRegistry/registries/pipelineRuns/write",
        "Microsoft.ContainerRegistry/registries/pipelineRuns/delete",
        "Microsoft.ContainerRegistry/registries/pipelineRuns/operationStatuses/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Container Registry Transfer Pipeline Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Kubernetes Agentless Operator

Grants Microsoft Defender for Cloud access to Azure Kubernetes Services

[Learn more](/azure/defender-for-cloud/defender-for-containers-architecture)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/trustedAccessRoleBindings/write | Create or update trusted access role bindings for managed cluster |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/trustedAccessRoleBindings/read | Get trusted access role bindings for managed cluster |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/trustedAccessRoleBindings/delete | Delete trusted access role bindings for managed cluster |
> | [Microsoft.ContainerService](../permissions/containers.md#microsoftcontainerservice)/managedClusters/read | Get a managed cluster |
> | [Microsoft.Features](../permissions/management-and-governance.md#microsoftfeatures)/features/read | Gets the features of a subscription. |
> | [Microsoft.Features](../permissions/management-and-governance.md#microsoftfeatures)/providers/features/read | Gets the feature of a subscription in a given resource provider. |
> | [Microsoft.Features](../permissions/management-and-governance.md#microsoftfeatures)/providers/features/register/action | Registers the feature for a subscription in a given resource provider. |
> | [Microsoft.Security](../permissions/security.md#microsoftsecurity)/pricings/securityoperators/read | Gets the security operators for the scope |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Grants Microsoft Defender for Cloud access to Azure Kubernetes Services",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/d5a2ae44-610b-4500-93be-660a0c5f5ca6",
  "name": "d5a2ae44-610b-4500-93be-660a0c5f5ca6",
  "permissions": [
    {
      "actions": [
        "Microsoft.ContainerService/managedClusters/trustedAccessRoleBindings/write",
        "Microsoft.ContainerService/managedClusters/trustedAccessRoleBindings/read",
        "Microsoft.ContainerService/managedClusters/trustedAccessRoleBindings/delete",
        "Microsoft.ContainerService/managedClusters/read",
        "Microsoft.Features/features/read",
        "Microsoft.Features/providers/features/read",
        "Microsoft.Features/providers/features/register/action",
        "Microsoft.Security/pricings/securityoperators/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Kubernetes Agentless Operator",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Kubernetes Cluster - Azure Arc Onboarding

Role definition to authorize any user/service to create connectedClusters resource

[Learn more](/azure/azure-arc/kubernetes/connect-cluster)

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/write | Creates or updates an deployment. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/operationresults/read | Get the subscription operation results. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/read | Gets the list of subscriptions. |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/Write | Writes connectedClusters |
> | [Microsoft.Kubernetes](../permissions/hybrid-multicloud.md#microsoftkubernetes)/connectedClusters/read | Read connectedClusters |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/write | Creates or updates extension resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/read | Gets extension instance resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/delete | Deletes extension instance resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/operations/read | Gets Async Operation status. |
> | [Microsoft.Support](../permissions/general.md#microsoftsupport)/* | Create and update a support ticket |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Role definition to authorize any user/service to create connectedClusters resource",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/34e09817-6cbe-4d01-b1a2-e0eac5743d41",
  "name": "34e09817-6cbe-4d01-b1a2-e0eac5743d41",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/write",
        "Microsoft.Resources/subscriptions/operationresults/read",
        "Microsoft.Resources/subscriptions/read",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.Kubernetes/connectedClusters/Write",
        "Microsoft.Kubernetes/connectedClusters/read",
        "Microsoft.KubernetesConfiguration/extensions/write",
        "Microsoft.KubernetesConfiguration/extensions/read",
        "Microsoft.KubernetesConfiguration/extensions/delete",
        "Microsoft.KubernetesConfiguration/extensions/operations/read",
        "Microsoft.Support/*"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Kubernetes Cluster - Azure Arc Onboarding",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Kubernetes Extension Contributor

Can create, update, get, list and delete Kubernetes Extensions, and get extension async operations

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/write | Creates or updates extension resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/read | Gets extension instance resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/delete | Deletes extension instance resource. |
> | [Microsoft.KubernetesConfiguration](../permissions/hybrid-multicloud.md#microsoftkubernetesconfiguration)/extensions/operations/read | Gets Async Operation status. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Can create, update, get, list and delete Kubernetes Extensions, and get extension async operations",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/85cb6faf-e071-4c9b-8136-154b5a04f717",
  "name": "85cb6faf-e071-4c9b-8136-154b5a04f717",
  "permissions": [
    {
      "actions": [
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/*",
        "Microsoft.Resources/subscriptions/resourceGroups/read",
        "Microsoft.KubernetesConfiguration/extensions/write",
        "Microsoft.KubernetesConfiguration/extensions/read",
        "Microsoft.KubernetesConfiguration/extensions/delete",
        "Microsoft.KubernetesConfiguration/extensions/operations/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Kubernetes Extension Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Service Fabric Cluster Contributor

Manage your Service Fabric Cluster resources. Includes clusters, application types, application type versions, applications, and services. You will need additional permissions to deploy and manage the cluster's underlying resources such as virtual machine scale sets, storage accounts, networks, etc.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ServiceFabric](../permissions/compute.md#microsoftservicefabric)/clusters/* |  |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Manage your Service Fabric Cluster resources. Includes clusters, application types, application type versions, applications, and services. You will need additional permissions to deploy and manage the cluster's underlying resources such as virtual machine scale sets, storage accounts, networks, etc.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/b6efc156-f0da-4e90-a50a-8c000140b017",
  "name": "b6efc156-f0da-4e90-a50a-8c000140b017",
  "permissions": [
    {
      "actions": [
        "Microsoft.ServiceFabric/clusters/*",
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/*",
        "Microsoft.Resources/subscriptions/resourceGroups/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Service Fabric Cluster Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Service Fabric Managed Cluster Contributor

Deploy and manage your Service Fabric Managed Cluster resources. Includes managed clusters, node types, application types, application type versions, applications, and services.

> [!div class="mx-tableFixed"]
> | Actions | Description |
> | --- | --- |
> | [Microsoft.ServiceFabric](../permissions/compute.md#microsoftservicefabric)/managedclusters/* |  |
> | [Microsoft.Authorization](../permissions/management-and-governance.md#microsoftauthorization)/*/read | Read roles and role assignments |
> | [Microsoft.Insights](../permissions/monitor.md#microsoftinsights)/alertRules/* | Create and manage a classic metric alert |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/deployments/* | Create and manage a deployment |
> | [Microsoft.Resources](../permissions/management-and-governance.md#microsoftresources)/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | **NotActions** |  |
> | *none* |  |
> | **DataActions** |  |
> | *none* |  |
> | **NotDataActions** |  |
> | *none* |  |

```json
{
  "assignableScopes": [
    "/"
  ],
  "description": "Deploy and manage your Service Fabric Managed Cluster resources. Includes managed clusters, node types, application types, application type versions, applications, and services.",
  "id": "/providers/Microsoft.Authorization/roleDefinitions/83f80186-3729-438c-ad2d-39e94d718838",
  "name": "83f80186-3729-438c-ad2d-39e94d718838",
  "permissions": [
    {
      "actions": [
        "Microsoft.ServiceFabric/managedclusters/*",
        "Microsoft.Authorization/*/read",
        "Microsoft.Insights/alertRules/*",
        "Microsoft.Resources/deployments/*",
        "Microsoft.Resources/subscriptions/resourceGroups/read"
      ],
      "notActions": [],
      "dataActions": [],
      "notDataActions": []
    }
  ],
  "roleName": "Service Fabric Managed Cluster Contributor",
  "roleType": "BuiltInRole",
  "type": "Microsoft.Authorization/roleDefinitions"
}
```

## Next steps

- [Assign Azure roles using the Azure portal](/azure/role-based-access-control/role-assignments-portal)