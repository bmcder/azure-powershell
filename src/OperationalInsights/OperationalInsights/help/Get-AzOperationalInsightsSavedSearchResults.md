---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresults
schema: 2.0.0
---

# Get-AzOperationalInsightsSavedSearchResults

## SYNOPSIS
This cmdlet is deprecated and no longer works.

## WORKAROUND

Use your query with the Invoke-AzOperationalInsightsQuery cmdlet instead

Alternatively if you wished to retrieve and then execute your saved search query you can do so with some code such as this
```
(Get-AzOperationalInsightsSavedSearch -ResourceGroupName <WorkspaceResourceGroupName> -WorkspaceName <WorkspaceName>).Value | 
Where-Object { $_.Properties.DisplayName -eq "<Your Saved Search Query>"}  |
foreach-object {Invoke-AzOperationalInsightsQuery -workspaceId <WorkspaceId> -Query $_.Properties.Query}

```

## RELATED LINKS
[Invoke-AzOperationalInsightsQuery](]https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery?view=azps-1.6.0)
