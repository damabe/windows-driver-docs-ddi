---
UID: NF:dbgeng.IDebugBreakpoint2.SetMatchThreadId
title: IDebugBreakpoint2::SetMatchThreadId (dbgeng.h)
description: The SetMatchThreadId method sets the engine thread ID of the thread that can trigger a breakpoint. This method belongs to the IDebugBreakpoint2 interface.
old-location: debugger\setmatchthreadid.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugBreakpoint2::SetMatchThreadId"]
ms.keywords: ComOther_5100cd0c-7d69-4210-9d32-ca1e9bd321aa.xml, IDebugBreakpoint interface [Windows Debugging],SetMatchThreadId method, IDebugBreakpoint2 interface [Windows Debugging],SetMatchThreadId method, IDebugBreakpoint2.SetMatchThreadId, IDebugBreakpoint2::SetMatchThreadId, IDebugBreakpoint::SetMatchThreadId, SetMatchThreadId, SetMatchThreadId method [Windows Debugging], SetMatchThreadId method [Windows Debugging],IDebugBreakpoint interface, SetMatchThreadId method [Windows Debugging],IDebugBreakpoint2 interface, dbgeng/IDebugBreakpoint2::SetMatchThreadId, dbgeng/IDebugBreakpoint::SetMatchThreadId, debugger.setmatchthreadid
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
 - IDebugBreakpoint2::SetMatchThreadId
 - dbgeng/IDebugBreakpoint2::SetMatchThreadId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugBreakpoint2::SetMatchThreadId
---

# IDebugBreakpoint2::SetMatchThreadId


## -description

The <b>SetMatchThreadId</b> method sets the engine thread ID of the thread that can trigger a breakpoint.

## -parameters

### -param Thread 

[in]
The engine thread ID of the thread that can trigger this breakpoint.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The thread that <i>Thread</i> specifies could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The target is in a kernel and the breakpoint is a processor breakpoint.  Processor breakpoints cannot be limited to threads in kernel mode.

</td>
</tr>
</table>
 

This method can also return other error values.  For more information, see <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a>.

## -remarks

If you have set a thread for the breakpoint, the breakpoint can be triggered only if that thread hits the breakpoint.  If you have not set a thread, any thread can trigger the breakpoint.

If you have set a thread, you can remove the setting by setting <i>Id</i> to DEBUG_ANY_ID.

For more information about breakpoint properties, see <a href="/windows-hardware/drivers/debugger/controlling-breakpoint-flags-and-parameters">Controlling Breakpoint Flags and Parameters</a>.

