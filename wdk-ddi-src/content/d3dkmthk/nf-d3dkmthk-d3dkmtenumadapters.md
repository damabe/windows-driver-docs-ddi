---
UID: NF:d3dkmthk.D3DKMTEnumAdapters
title: D3DKMTEnumAdapters function (d3dkmthk.h)
description: The D3DKMTEnumAdapters function enumerates all graphics adapters on the system. The function returns STATUS_SUCCESS if the enumeration was successful.
old-location: display\d3dkmtenumadapters.htm
ms.date: 05/10/2018
keywords: ["D3DKMTEnumAdapters function"]
ms.keywords: D3DKMTEnumAdapters, D3DKMTEnumAdapters callback function [Display Devices], PFND3DKMT_ENUMADAPTERS, PFND3DKMT_ENUMADAPTERS callback, d3dkmthk/D3DKMTEnumAdapters, display.d3dkmtenumadapters
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Universal
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
tech.root: display
req.typenames: 
f1_keywords:
 - D3DKMTEnumAdapters
 - d3dkmthk/D3DKMTEnumAdapters
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
api_name:
 - D3DKMTEnumAdapters
---

# D3DKMTEnumAdapters function


## -description

Enumerates all graphics adapters on the system.

## -parameters

### -param D3DKMT_ENUMADAPTERS

[in, out] A pointer to a <a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_enumadapters">D3DKMT_ENUMADAPTERS</a> structure that lists all graphics adapters and their characteristics.

## -returns

Returns one of the following values:

|Return code|Description|
|--- |--- |
|STATUS_SUCCESS|The enumeration was successful.|
|STATUS_INVALID_PARAMETER|The  pEnumAdapters parameter was validated and determined to be incorrect.|

This function might also return other NTSTATUS values.

## -remarks

The operating system enumerates graphics adapters in the same sequence as their corresponding physical devices.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_enumadapters">D3DKMT_ENUMADAPTERS</a>
