---
title: Lync Server 2013：增强型 9-1-1 (E9-1-1) 和中介服务器
description: Lync Server 2013：增强的 9-1-1 (E9-1) 和中介服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enhanced 9-1-1 (E9-1-1) and Mediation Server
ms:assetid: d231221f-5596-4a87-a463-269f5bcce65f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398903(v=OCS.15)
ms:contentKeyID: 48185448
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7fb6da8e69883e321f23a53e8dc5067817d5aa66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428627"
---
# <a name="enhanced-9-1-1-e9-1-1-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="cb7a6-103">Lync Server 2013 中的增强型 9-1-1 (E9-1-1) 和中介服务器</span><span class="sxs-lookup"><span data-stu-id="cb7a6-103">Enhanced 9-1-1 (E9-1-1) and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb7a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb7a6-104">

<span> </span></span></span>

<span data-ttu-id="cb7a6-105">_**主题上次修改时间：** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="cb7a6-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="cb7a6-106">中介服务器具有扩展的功能，使其能够与增强的 9-1-1 (E9) 服务提供商正确交互。</span><span class="sxs-lookup"><span data-stu-id="cb7a6-106">The Mediation Server has extended capabilities so that it can correctly interact with Enhanced 9-1-1 (E9-1-1) service providers.</span></span> <span data-ttu-id="cb7a6-107">中介服务器上不需要特殊配置;默认情况下，E9-1-1 交互所需的 SIP 扩展包括在中介服务器的 SIP 协议中，用于与网关对等 (PSTN 网关、IP PBX 或 Internet 电话服务提供商的 SBC，包括 E9-1 服务提供商) </span><span class="sxs-lookup"><span data-stu-id="cb7a6-107">No special configuration is needed on the Mediation Server; the SIP extensions required for E9-1-1 interaction are, by default, included in the Mediation Server’s SIP protocol for its interactions with a gateway peer (PSTN gateway, IP-PBX, or the SBC of an Internet Telephony Service Provider, including E9-1-1 Service Providers)</span></span>

<span data-ttu-id="cb7a6-108">是否可以在现有中介服务器池上终止 E9 服务提供商的 SIP 主干，或者是否需要独立中介服务器将取决于 E9 SBC 是否可以与中介服务器池进行交互。</span><span class="sxs-lookup"><span data-stu-id="cb7a6-108">Whether the SIP trunk to an E9-1-1 Service Provider can be terminated on an existing Mediation Server pool or will require stand-alone Mediation Servers will depend on whether the E9-1-1 SBC can interact with a pool of Mediation Servers.</span></span> <span data-ttu-id="cb7a6-109">有关详细信息，请参阅 [Lync Server 2013 中的 M:N 主干](lync-server-2013-m-n-trunk.md)。</span><span class="sxs-lookup"><span data-stu-id="cb7a6-109">For details, see [M:N trunk in Lync Server 2013](lync-server-2013-m-n-trunk.md).</span></span>

<span data-ttu-id="cb7a6-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb7a6-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

