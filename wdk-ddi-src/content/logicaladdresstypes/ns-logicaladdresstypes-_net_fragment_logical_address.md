---
UID: NS:logicaladdresstypes._NET_FRAGMENT_LOGICAL_ADDRESS
title: NET_FRAGMENT_LOGICAL_ADDRESS (logicaladdresstypes.h)
description: The NET_FRAGMENT_LOGICAL_ADDRESS structure contains DMA logical address information for a NET_FRAGMENT.
tech.root: netvista
ms.date: 01/22/2024
keywords: ["NET_FRAGMENT_LOGICAL_ADDRESS structure"]
ms.keywords: NET_FRAGMENT_LOGICAL_ADDRESS, NET_FRAGMENT_LOGICAL_ADDRESS,
req.header: logicaladdresstypes.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: NET_FRAGMENT_LOGICAL_ADDRESS
targetos: Windows
ms.custom: Vb
f1_keywords:
 - _NET_FRAGMENT_LOGICAL_ADDRESS
 - logicaladdresstypes/_NET_FRAGMENT_LOGICAL_ADDRESS
 - NET_FRAGMENT_LOGICAL_ADDRESS
 - logicaladdresstypes/NET_FRAGMENT_LOGICAL_ADDRESS
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - logicaladdresstypes.h
api_name:
 - _NET_FRAGMENT_LOGICAL_ADDRESS
 - NET_FRAGMENT_LOGICAL_ADDRESS
product:
 - Windows
---

# NET_FRAGMENT_LOGICAL_ADDRESS structure


## -description

The **NET_FRAGMENT_LOGICAL_ADDRESS** structure contains DMA logical address information for a [**NET_FRAGMENT**](../fragment/ns-fragment-_net_fragment.md).

## -struct-fields

### -field LogicalAddress

On DMA capable adapters, contains a mapped DMA address that can be used to program NIC hardware.

Do not modify this value.

## -remarks

The **NET_FRAGMENT_LOGICAL_ADDRESS** extension is only valid if the driver sets the **DmaCapabilities** member in the [**NET_ADAPTER_TX_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_tx_capabilities.md) or [**NET_ADAPTER_RX_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_rx_capabilities.md) structure.

To obtain this structure, call [**NetExtensionGetFragmentLogicalAddress**](../logicaladdress/nf-logicaladdress-netextensiongetfragmentlogicaladdress.md).

## -see-also

[Packet descriptors and extensions](/windows-hardware/drivers/netcx/packet-descriptors-and-extensions)

[**NET_FRAGMENT**](../fragment/ns-fragment-_net_fragment.md)

[**NetExtensionGetFragmentLogicalAddress**](../logicaladdress/nf-logicaladdress-netextensiongetfragmentlogicaladdress.md)

[**NET_ADAPTER_TX_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_tx_capabilities.md)

[**NET_ADAPTER_RX_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_rx_capabilities.md)

