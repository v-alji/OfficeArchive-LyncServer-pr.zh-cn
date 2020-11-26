---
title: Lync Server 2013：新的虚拟化功能
description: Lync Server 2013：新的虚拟化功能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New virtualization features
ms:assetid: edeb2c41-765e-47b8-8a2b-7a7ce09de2ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721926(v=OCS.15)
ms:contentKeyID: 49733861
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac15b8592d158d84807ff9e665dd6da50b699059
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424980"
---
# <a name="new-virtualization-features-in-lync-server-2013"></a><span data-ttu-id="30181-103">Lync Server 2013 中新的虚拟化功能</span><span class="sxs-lookup"><span data-stu-id="30181-103">New virtualization features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30181-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30181-104">

<span> </span></span></span>

<span data-ttu-id="30181-105">_**主题上次修改时间：** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="30181-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="30181-106">Lync Server 2013 支持 Windows Server 2012、Windows Server 2012 R2 和 Windows Server 2008 R2 上的虚拟化。</span><span class="sxs-lookup"><span data-stu-id="30181-106">Lync Server 2013 supports virtualization on both Windows Server 2012, Windows Server 2012 R2, and Windows Server 2008 R2.</span></span> <span data-ttu-id="30181-107">Windows Server 2012 和 Windows Server 2012 R2 上的支持包括对单个根 i/o 虚拟化的支持 (SR-IOV) 功能。</span><span class="sxs-lookup"><span data-stu-id="30181-107">Support on Windows Server 2012 and Windows Server 2012 R2 includes support for the Single Root I/O Virtualization (SR-IOV) capabilities.</span></span> <span data-ttu-id="30181-108">使用 SR-IOV，物理网络适配器的虚函数直接分配给虚拟机。</span><span class="sxs-lookup"><span data-stu-id="30181-108">With SR-IOV, the virtual function of a physical network adapter is assigned directly to a virtual machine.</span></span> <span data-ttu-id="30181-109">这会增加网络吞吐量并减少网络延迟，同时减少处理网络流量所需的主机 CPU 开销。</span><span class="sxs-lookup"><span data-stu-id="30181-109">This increases network throughput and reduces network latency while also reducing the host CPU overhead that is required for processing network traffic.</span></span> <span data-ttu-id="30181-110">若要充分利用 SR-IOV，你必须使用具有支持 SR-IOV 的 BIOS 的主机服务器，以及使用支持 SR-IOV 的网络适配器。</span><span class="sxs-lookup"><span data-stu-id="30181-110">To take advantage of SR-IOV, you must use a host server which has BIOS which supports SR-IOV, as well as use network adapters that support SR-IOV.</span></span>

<span data-ttu-id="30181-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30181-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

