---
title: array_sum() - Azure Data Explorer
description: This article describes array_sum() in Azure Data Explorer.
services: data-explorer
author: orspod
ms.author: orspodek
ms.reviewer: alexans
ms.service: data-explorer
ms.topic: reference
ms.date: 04/05/2021
---
# array_sum()

Calculates the sum of elements in a dynamic array.

## Syntax

`array_sum`(*`arr`*)

## Arguments

* *`arr`*: Input array.

## Returns

Double type value with the of elements of the array.

Note: if the array contains elements of non-numeric types, the result is `null`.

## Example

<!-- csl: https://help.kusto.windows.net:443/Samples -->
```kusto
print arr=dynamic([1,2,3,4]) 
| extend arr_sum=array_sum(arr)
```
|`arr`|`arr_sum`|
|---|---|
|[1,2,3,4]|10|