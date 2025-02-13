---
description: "Retrieves the symbol that represents the type for this symbol."
title: "IDiaSymbol::get_type"
ms.date: "11/04/2016"
ms.topic: "reference"
dev_langs:
  - "C++"
helpviewer_keywords:
  - "IDiaSymbol::get_type method"
author: "mikejo5000"
ms.author: "mikejo"
manager: jmartens
ms.technology: vs-ide-debug
---
# IDiaSymbol::get_type

 [!INCLUDE [Visual Studio](~/includes/applies-to-version/vs-windows-only.md)]
Retrieves the symbol that represents the type for this symbol.

## Syntax

```C++
HRESULT get_type (
    IDiaSymbol** pRetVal
);
```

#### Parameters
`pRetVal`

[out] Returns an [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md) object that represents the type of this symbol.

## Return Value
If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.

> [!NOTE]
> A return value of `S_FALSE` means the property is not available for the symbol.

## Remarks
To determine the type a symbol has, you must call this method and examine the resulting [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md) object. Note that it is possible for a symbol to not have a type. For example, the name of a structure has no type but it might have children symbols (use the [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md) method to examine those children).

## Example

```C++
IDiaSymbol*         pType;
CComPtr<IDiaSymbol> pBaseType;
if (SUCCEEDED(pType->get_type( &pBaseType ))) {
    BasicType btBaseType;
    if (SUCCEEDED(pBaseType->get_baseType((DWORD *)&btBaseType))) {
        // Do something with basic type.
    }
}
```

## See also
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [IDiaSymbol::get_baseType](../../debugger/debug-interface-access/idiasymbol-get-basetype.md)
- [IDiaSymbol::findChildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md)
