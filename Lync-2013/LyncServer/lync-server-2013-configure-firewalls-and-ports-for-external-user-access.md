---
title: Lync Server 2013：为外部用户访问配置防火墙和端口
description: Lync Server 2013：为外部用户访问配置防火墙和端口。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure firewalls and ports for external user access
ms:assetid: cacb3832-f8db-4009-bfcf-6f5c15c236ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398848(v=OCS.15)
ms:contentKeyID: 48185430
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 68ccb382c3b3632b113b2b0a36846500700c1b9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433967"
---
# <a name="configure-firewalls-and-ports-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="bdbd4-103">在 Lync Server 2013 中为外部用户访问配置防火墙和端口</span><span class="sxs-lookup"><span data-stu-id="bdbd4-103">Configure firewalls and ports for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bdbd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bdbd4-104">

<span> </span></span></span>

<span data-ttu-id="bdbd4-105">_**主题上次修改时间：** 2012-05-21_</span><span class="sxs-lookup"><span data-stu-id="bdbd4-105">_**Topic Last Modified:** 2012-05-21_</span></span>

<span data-ttu-id="bdbd4-106">若要配置防火墙和端口，你需要针对边缘服务器、反向代理服务器和可能的硬件负载平衡器配置它们，以用于不使用 DNS 负载平衡) 的缩放部署 (。</span><span class="sxs-lookup"><span data-stu-id="bdbd4-106">To configure firewalls and ports, you need to configure them for Edge Servers, reverse proxy servers, and possibly hardware load balancers (for a scaled deployment that does not use DNS load balancing).</span></span> <span data-ttu-id="bdbd4-107">本部分提供有关所有 Edge 服务器组件的防火墙和端口要求以及边缘服务器的防火墙端口的配置的信息。</span><span class="sxs-lookup"><span data-stu-id="bdbd4-107">This section provides information about firewall and port requirements for all Edge Server components and the configuration of firewall ports for Edge Servers.</span></span> <span data-ttu-id="bdbd4-108">有关为反向代理服务器配置端口的详细信息，请参阅 [为 Lync Server 2013 设置反向代理服务器](lync-server-2013-setting-up-reverse-proxy-servers.md)。</span><span class="sxs-lookup"><span data-stu-id="bdbd4-108">For details about configuring ports for reverse proxy servers, see [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md).</span></span> <span data-ttu-id="bdbd4-109">如果你正在部署缩放的边缘拓扑，并且使用的是硬件负载平衡，而不是 DNS 负载平衡，请参阅计划文档中的在 [Lync Server 2013 中使用硬件负载平衡器缩放的合并边界](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md) ，了解有关配置硬件负载平衡器端口的详细信息。</span><span class="sxs-lookup"><span data-stu-id="bdbd4-109">If you are deploying a scaled edge topology and are using hardware load balancing instead of DNS load balancing, see [Scaled consolidated edge with hardware load balancers in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md) in the Planning documentation for details about configuring ports for hardware load balancers.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="bdbd4-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bdbd4-110">See Also</span></span>


[<span data-ttu-id="bdbd4-111">确定 Lync Server 2013 的外部 A/V 防火墙和端口要求</span><span class="sxs-lookup"><span data-stu-id="bdbd4-111">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="bdbd4-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bdbd4-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

