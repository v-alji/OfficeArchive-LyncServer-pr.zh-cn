---
title: Lync Server 2013：配置自动客户端登录以使用控制器
description: Lync Server 2013：配置自动客户端 Sign-In 以使用 Director。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Automatic Client Sign-In to use the Director
ms:assetid: 85369ffc-53ae-43be-8a23-84a094faecff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398678(v=OCS.15)
ms:contentKeyID: 48184703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9c45a1a677d3a30704d8dca1771ef865cef29ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392308"
---
# <a name="configure-automatic-client-sign-in-to-use-the-director-in-lync-server-2013"></a><span data-ttu-id="5b83f-103">在 Lync Server 2013 中配置自动客户端登录以使用控制器</span><span class="sxs-lookup"><span data-stu-id="5b83f-103">Configure Automatic Client Sign-In to use the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b83f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b83f-104">

<span> </span></span></span>

<span data-ttu-id="5b83f-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="5b83f-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="5b83f-106">当你部署 Lync Server 2013、Director 或 Director 池时，我们建议你使用自动客户端 Sign-In 作为最佳做法。</span><span class="sxs-lookup"><span data-stu-id="5b83f-106">When you deploy a Lync Server 2013, Director or a pool of Directors, we recommend that you use Automatic Client Sign-In as a best practice.</span></span> <span data-ttu-id="5b83f-107">有关如何为自动客户端登录配置 DNS 服务器的详细信息，请参阅规划文档中 [Lync Server 2013 中的自动客户端登录 DNS 要求](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) 。</span><span class="sxs-lookup"><span data-stu-id="5b83f-107">For details about how to configure DNS servers for automatic client sign-in, see [DNS requirements for automatic client sign-in in Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) in the Planning documentation.</span></span>

<span data-ttu-id="5b83f-108">如果已部署了自动客户端登录，请参阅以下部分，在控制器 (s 上配置它) 。</span><span class="sxs-lookup"><span data-stu-id="5b83f-108">If you have already deployed Automatic Client Sign-In, see the following sections to configure it on your Director(s).</span></span>

<div>

## <a name="single-director-instance"></a><span data-ttu-id="5b83f-109">单控制器实例</span><span class="sxs-lookup"><span data-stu-id="5b83f-109">Single Director Instance</span></span>

<span data-ttu-id="5b83f-110">如果已部署自动客户端 Sign-In 并且它指向前端服务器或前端池，则需要更改 DNS SRV 记录以指向 Director。</span><span class="sxs-lookup"><span data-stu-id="5b83f-110">If you already have Automatic Client Sign-In deployed and it is pointing to a Front End Server or a Front End pool, you need to change the DNS SRV record to point to the Director.</span></span>

</div>

<div>

## <a name="director-pool"></a><span data-ttu-id="5b83f-111">主管池</span><span class="sxs-lookup"><span data-stu-id="5b83f-111">Director Pool</span></span>

<span data-ttu-id="5b83f-112">如果已部署自动客户端 Sign-In 并且它指向前端服务器或前端池，则需要将 DNS SRV 记录更改为指向控制器池。</span><span class="sxs-lookup"><span data-stu-id="5b83f-112">If you already have Automatic Client Sign-In deployed and it is pointing to a Front End Server or a Front End pool, you need to change the DNS SRV record to point to the Director pool.</span></span>

<span data-ttu-id="5b83f-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b83f-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

