---
UID: NF:wdm.MmGetMdlByteCount
title: MmGetMdlByteCount macro (wdm.h)
description: The MmGetMdlByteCount macro returns the length, in bytes, of the buffer described by the specified MDL.
tech.root: kernel
ms.date: 08/16/2023
keywords: ["MmGetMdlByteCount macro"]
ms.keywords: MmGetMdlByteCount, MmGetMdlByteCount macro [Tools], k106_f750d750-c5ca-44cf-b8f1-f52d2eb8bc27.xml, kernel.mmgetmdlbytecount, wdm/MmGetMdlByteCount
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Desktop
req.target-min-winverclnt:
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: MdlAfterReqCompletedIntIoctlA, MdlAfterReqCompletedIoctlA, MdlAfterReqCompletedReadA, MdlAfterReqCompletedWriteA
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: Any level (see Remarks section)
targetos: Windows
req.typenames: 
f1_keywords:
 - MmGetMdlByteCount
 - wdm/MmGetMdlByteCount
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdm.h
api_name:
 - MmGetMdlByteCount
returns-override: true
---

## -description

The **MmGetMdlByteCount** macro returns the length, in bytes, of the buffer described by the specified MDL.

## -parameters

### -param Mdl

A pointer to an [MDL](./ns-wdm-_mdl.md) structure that describes the layout of a virtual memory buffer in physical memory. For more information, see [Using MDLs](/windows-hardware/drivers/kernel/using-mdls).

## -returns

**MmGetMdlByteCount** returns the length, in bytes, of the buffer described by Mdl.

## -remarks

Macro definition:

```cpp
#define MmGetMdlByteCount(Mdl)  ((Mdl)->ByteCount)
```

Callers of **MmGetMdlByteCount** can be running at any IRQL. Usually, callers are running at IRQL <= DISPATCH_LEVEL.

## -see-also

[MDL](./ns-wdm-_mdl.md)

[MmGetMdlByteOffset](./nf-wdm-mmgetmdlbyteoffset.md)

## -syntax

```cpp
ULONG MmGetMdlByteCount(
  [in] PMDL Mdl
);
```
