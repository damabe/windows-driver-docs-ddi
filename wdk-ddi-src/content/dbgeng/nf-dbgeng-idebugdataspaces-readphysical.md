---
UID: NF:dbgeng.IDebugDataSpaces.ReadPhysical
title: IDebugDataSpaces::ReadPhysical (dbgeng.h)
description: The ReadPhysical method reads the target's memory from the specified physical address. This method belongs to the IDebugDataSpaces interface.
old-location: debugger\readphysical3.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugDataSpaces::ReadPhysical"]
ms.keywords: IDebugDataSpaces interface [Windows Debugging],ReadPhysical method, IDebugDataSpaces.ReadPhysical, IDebugDataSpaces2 interface [Windows Debugging],ReadPhysical method, IDebugDataSpaces2::ReadPhysical, IDebugDataSpaces3 interface [Windows Debugging],ReadPhysical method, IDebugDataSpaces3::ReadPhysical, IDebugDataSpaces4 interface [Windows Debugging],ReadPhysical method, IDebugDataSpaces4::ReadPhysical, IDebugDataSpaces::ReadPhysical, IDebugDataSpaces_5be1f680-1177-4cdf-a4d8-5868644a51af.xml, ReadPhysical, ReadPhysical method [Windows Debugging], ReadPhysical method [Windows Debugging],IDebugDataSpaces interface, ReadPhysical method [Windows Debugging],IDebugDataSpaces2 interface, ReadPhysical method [Windows Debugging],IDebugDataSpaces3 interface, ReadPhysical method [Windows Debugging],IDebugDataSpaces4 interface, dbgeng/IDebugDataSpaces2::ReadPhysical, dbgeng/IDebugDataSpaces3::ReadPhysical, dbgeng/IDebugDataSpaces4::ReadPhysical, dbgeng/IDebugDataSpaces::ReadPhysical, debugger.readphysical3
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IDebugDataSpaces::ReadPhysical
 - dbgeng/IDebugDataSpaces::ReadPhysical
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugDataSpaces::ReadPhysical
---

# IDebugDataSpaces::ReadPhysical


## -description

The <b>ReadPhysical</b> method reads the target's memory from the specified physical address.

## -parameters

### -param Offset 

[in]
Specifies the physical address of the memory to read.

### -param Buffer 

[out]
Receives the memory that is read.

### -param BufferSize 

[in]
Specifies the size in bytes of the buffer <i>Buffer</i>.  This is the maximum number of bytes that will be read.

### -param BytesRead 

[out, optional]
Receives the number of bytes read from the target's memory.  If <i>BytesRead</i> is <b>NULL</b>, this information is not returned.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 

This method can also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

## -remarks

This method is only available in kernel-mode debugging.

