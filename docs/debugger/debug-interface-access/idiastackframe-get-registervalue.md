---
description: "Retrieves the value of a specified register as stored in the stack frame."
title: "IDiaStackFrame::get_registerValue"
ms.date: "11/04/2016"
ms.topic: "reference"
dev_langs:
  - "C++"
helpviewer_keywords:
  - "IDiaStackFrame::get_registerValue method"
author: "mikejo5000"
ms.author: "mikejo"
manager: jmartens
ms.technology: vs-ide-debug
---
# IDiaStackFrame::get_registerValue

 [!INCLUDE [Visual Studio](~/includes/applies-to-version/vs-windows-only.md)]
Retrieves the value of a specified register as stored in the stack frame.

## Syntax

```C++
HRESULT get_registerValue(
   ULONG      registerIndex,
   ULONGLONG *pRetVal
);
```

#### Parameters
 `registerIndex`

[in] One of the [CV_HREG_e Enumeration](../../debugger/debug-interface-access/cv-hreg-e.md) enumeration values.

 `pRetVal`

[out] Value stored in the register.

## Return Value
 If successful, returns `S_OK`; otherwise, returns error code.

## See also
- [IDiaStackFrame](../../debugger/debug-interface-access/idiastackframe.md)
- [CV_HREG_e Enumeration](../../debugger/debug-interface-access/cv-hreg-e.md)
