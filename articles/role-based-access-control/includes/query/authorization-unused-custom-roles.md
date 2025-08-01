---
author: jenniferf-skc
ms.service: resource-graph
ms.topic: include
ms.date: 05/30/2023
ms.author: jfields
ms.custom:
  - build-2025
---

```kusto
authorizationresources
| where type =~ "microsoft.authorization/roledefinitions"
| where tolower(properties.type) == "customrole"
| extend rdId = tolower(id)
| extend Scope = tolower(properties.assignableScopes)
| join kind = leftouter (
authorizationresources
  | where type =~ "microsoft.authorization/roleassignments"
  | extend RoleId = tolower(tostring(properties.roleDefinitionId))
  | summarize RoleAssignmentCount = count() by RoleId
) on $left.rdId == $right.RoleId
| where isempty(RoleAssignmentCount)
| project RoleDefinitionId = rdId, RoleDefinitionName = tostring(properties.roleName), Scope
```
