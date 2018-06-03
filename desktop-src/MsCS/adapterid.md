---
title: AdapterId
description: Provides the GUID that is used to uniquely identify the network interface in the cluster.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 252197fb-f91b-42f6-b64a-f09d336704d1
ms.prod: windows-server-dev
ms.technology: failover-clustering
ms.tgt_platform: multiple
keywords:
- AdapterId Failover Cluster , for Network Interface common properties
- AdapterId Failover Cluster
topic_type:
- apiref
api_name:
- AdapterId
api_type:
- NA
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# AdapterId

Provides the **GUID** that is used to uniquely identify the network interface in the cluster. The following table summarizes the attributes of the **AdapterId** property.



| Attribute | Value                                                            |
|-----------|------------------------------------------------------------------|
| Data type | Null-terminated Unicode string                                   |
| Access    | [Read-only](read-only-properties.md)                            |
| Structure | [**CLUSPROP\_SZ**](/previous-versions/windows/desktop/api/ClusAPI/)                              |
| Maximum   | None (but see [Maximum Property Size](maximum-string-size.md).) |
| Default   | **NULL**                                                         |



 

## Examples

The property value portion of a property list entry for **AdapterId** can be set with the following example code.


```C++
WCHAR szAdapterIdData[] = L"f605d1fd-e5de-4495-a680-44254c38d2d4";
CLUSPROP_SZ_DECLARE( AdapterIdValue, sizeof(szAdapterIdData) / sizeof(WCHAR) );

AdapterIdValue.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
AdapterIdValue.cbLength  = sizeof( szAdapterIdData );
StringCbCopy( AdapterIdValue.sz, AdapterIdValue.cbLength, szAdapterIdData );
```



## Requirements



|                                     |                                                                           |
|-------------------------------------|---------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                 |
| Minimum supported server<br/> | Windows Server 2008 Datacenter, Windows Server 2008 Enterprise<br/> |



## See also

<dl> <dt>

[Network Interface Common Properties](network-interface-common-properties.md)
</dt> <dt>

[**CLUSPROP\_SZ**](/previous-versions/windows/desktop/api/ClusAPI/)
</dt> <dt>

[**CLUSPROP\_SZ\_DECLARE**](/previous-versions/windows/desktop/api/ClusAPI/nf-clusapi-clusprop_sz_declare)
</dt> </dl>

 

 




