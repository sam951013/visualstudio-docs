---
description: "Retrieves the name of the server."
title: IDebugCoreServer3::GetServerName
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCoreServer3::GetServerName
helpviewer_keywords:
- IDebugCoreServer3::GetServerName
author: maiak
ms.author: maiak
manager: jmartens
ms.technology: vs-ide-debug
dev_langs:
- CPP
- CSharp
---
# IDebugCoreServer3::GetServerName

 [!INCLUDE [Visual Studio](~/includes/applies-to-version/vs-windows-only.md)]
Retrieves the name of the server.

## Syntax

### [C#](#tab/csharp)
```csharp
int GetServerName(
   out string pbstrName
);
```
### [C++](#tab/cpp)
```cpp
HRESULT GetServerName(
   BSTR* pbstrName
);
```
---

## Parameters
`pbstrName`\
[out] Returns the name of the server.

> [!NOTE]
> The caller is responsible for freeing the string.

## Return Value
 If successful, returns `S_OK`; otherwise, returns error code.

## Remarks
 For a friendly server name, call the [GetServerFriendlyName](../../../extensibility/debugger/reference/idebugcoreserver3-getserverfriendlyname.md) method.

## See also
- [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)
- [GetServerFriendlyName](../../../extensibility/debugger/reference/idebugcoreserver3-getserverfriendlyname.md)
