---
UID: NF:dbgeng.IDebugDataSpaces.WriteVirtual
title: IDebugDataSpaces::WriteVirtual (dbgeng.h)
description: The WriteVirtual method writes data to the target's virtual address space. This method belongs to the IDebugDataSpaces interface.
old-location: debugger\writevirtual.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugDataSpaces::WriteVirtual"]
ms.keywords: IDebugDataSpaces interface [Windows Debugging],WriteVirtual method, IDebugDataSpaces.WriteVirtual, IDebugDataSpaces2 interface [Windows Debugging],WriteVirtual method, IDebugDataSpaces2::WriteVirtual, IDebugDataSpaces3 interface [Windows Debugging],WriteVirtual method, IDebugDataSpaces3::WriteVirtual, IDebugDataSpaces4 interface [Windows Debugging],WriteVirtual method, IDebugDataSpaces4::WriteVirtual, IDebugDataSpaces::WriteVirtual, IDebugDataSpaces_2f8783ea-c7e4-438f-ad5b-898d0072a2f4.xml, WriteVirtual, WriteVirtual method [Windows Debugging], WriteVirtual method [Windows Debugging],IDebugDataSpaces interface, WriteVirtual method [Windows Debugging],IDebugDataSpaces2 interface, WriteVirtual method [Windows Debugging],IDebugDataSpaces3 interface, WriteVirtual method [Windows Debugging],IDebugDataSpaces4 interface, dbgeng/IDebugDataSpaces2::WriteVirtual, dbgeng/IDebugDataSpaces3::WriteVirtual, dbgeng/IDebugDataSpaces4::WriteVirtual, dbgeng/IDebugDataSpaces::WriteVirtual, debugger.writevirtual
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
 - IDebugDataSpaces::WriteVirtual
 - dbgeng/IDebugDataSpaces::WriteVirtual
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugDataSpaces::WriteVirtual
---

# IDebugDataSpaces::WriteVirtual


## -description

The <b>WriteVirtual</b> method writes data to the target's virtual address space.

## -parameters

### -param Offset 

[in]
Specifies the location in the target's virtual address space to be written.

### -param Buffer 

[in]
Specifies the buffer to write the memory from.

### -param BufferSize 

[in]
Specifies the size in bytes of the buffer.  This is also the number of bytes requested to be written.

### -param BytesWritten 

[out, optional]
Receives the number of bytes that were written.  If it is set to <b>NULL</b>, this information is not returned.

## -returns

This method can also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

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
The method was at least partially successful.  <i>BytesWritten</i> indicates the number of bytes successfully written, which may be less than <i>BufferSize</i>.

</td>
</tr>
</table>

## -remarks

This method writes the buffer to the memory in the target's virtual address space.

This method may only write to a cache of memory data when storing data.  To avoid caching, use <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugdataspaces4-writevirtualuncached">WriteVirtualUncached</a> instead.

## -see-also

<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugdataspaces">IDebugDataSpaces</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugdataspaces2">IDebugDataSpaces2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugdataspaces3">IDebugDataSpaces3</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugdataspaces4">IDebugDataSpaces4</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugdataspaces4-readvirtual">ReadVirtual</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugdataspaces4-writevirtualuncached">WriteVirtualUncached</a>

