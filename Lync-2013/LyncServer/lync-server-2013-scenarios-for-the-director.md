---
title: Lync Server 2013：控制器方案
description: Lync Server 2013： Director 的方案。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scenarios for the Director
ms:assetid: d2cf384a-0860-4779-80ce-cba2543be322
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398908(v=OCS.15)
ms:contentKeyID: 48185419
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45c611fbe680ba55fb148c08fed26d96a848507e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444978"
---
# <a name="scenarios-for-the-director-in-lync-server-2013"></a><span data-ttu-id="442b8-103">Lync Server 2013 中的控制器方案</span><span class="sxs-lookup"><span data-stu-id="442b8-103">Scenarios for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="442b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="442b8-104">

<span> </span></span></span>

<span data-ttu-id="442b8-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="442b8-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="442b8-106">Director 是运行 Microsoft Lync Server 2013 通信软件的服务器，可对用户请求进行身份验证，但不会在家任何用户帐户。</span><span class="sxs-lookup"><span data-stu-id="442b8-106">A Director is a server running Microsoft Lync Server 2013 communications software that can authenticate user requests, but does not home any user accounts.</span></span> <span data-ttu-id="442b8-107">Director 还托管类似于前端服务器的 web 服务，并将验证 web 票证请求并提供其他服务。</span><span class="sxs-lookup"><span data-stu-id="442b8-107">The Director also hosts web services similar to the Front End Server and will authenticate web ticket requests and provide other services.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="442b8-108">如果你部署控制器，则必须通过反向代理以及前端服务器的 web 服务从外部发布 Director web 服务。</span><span class="sxs-lookup"><span data-stu-id="442b8-108">If you deploy Directors, you must publish the Director web services externally through the reverse proxy as well as the web services of the Front End Server.</span></span> <span data-ttu-id="442b8-109">下面的主题介绍了可能的控制器拓扑的规划流程。</span><span class="sxs-lookup"><span data-stu-id="442b8-109">The topics following describe the planning process for the possible Director topologies.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="442b8-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="442b8-110">In This Section</span></span>

  - [<span data-ttu-id="442b8-111">Lync Server 2013 中的控制器概述</span><span class="sxs-lookup"><span data-stu-id="442b8-111">Overview of the Director in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-director.md)

  - [<span data-ttu-id="442b8-112">Lync Server 2013 中控制器所需的组件</span><span class="sxs-lookup"><span data-stu-id="442b8-112">Components required for the Director in Lync Server 2013</span></span>](lync-server-2013-components-required-for-the-director.md)

  - [<span data-ttu-id="442b8-113">Lync Server 2013 中控制器的软硬件要求</span><span class="sxs-lookup"><span data-stu-id="442b8-113">Hardware and software requirements for the Director in Lync Server 2013</span></span>](lync-server-2013-hardware-and-software-requirements-for-the-director.md)

  - [<span data-ttu-id="442b8-114">Lync Server 2013 中的单一控制器</span><span class="sxs-lookup"><span data-stu-id="442b8-114">Single Director in Lync Server 2013</span></span>](lync-server-2013-single-director.md)

  - [<span data-ttu-id="442b8-115">Lync Server 2013 中扩展的控制器池</span><span class="sxs-lookup"><span data-stu-id="442b8-115">Scaled Director pool in Lync Server 2013</span></span>](lync-server-2013-scaled-director-pool.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="442b8-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="442b8-116">See Also</span></span>


[<span data-ttu-id="442b8-117">Lync Server 2013 中支持的拓扑</span><span class="sxs-lookup"><span data-stu-id="442b8-117">Supported topologies in Lync Server 2013</span></span>](lync-server-2013-supported-topologies.md)  
[<span data-ttu-id="442b8-118">Lync Server 2013 的服务器硬件平台</span><span class="sxs-lookup"><span data-stu-id="442b8-118">Server hardware platforms for Lync Server 2013</span></span>](lync-server-2013-server-hardware-platforms.md)  
  

<span data-ttu-id="442b8-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="442b8-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

