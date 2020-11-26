---
title: Lync Server 2013：还原 Lync Server 池
description: Lync Server 2013：还原 Lync Server 池。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Lync Server pool
ms:assetid: 6fe80fb3-38ad-4931-a07b-1763b61aa448
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202176(v=OCS.15)
ms:contentKeyID: 51541488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02e92b4e7af9cf782d49c265425006e0118b9161
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442598"
---
# <a name="restoring-a-lync-server-pool-in-lync-server-2013"></a><span data-ttu-id="53b07-103">在 Lync Server 2013 中还原 Lync 服务器池</span><span class="sxs-lookup"><span data-stu-id="53b07-103">Restoring a Lync Server pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="53b07-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="53b07-104">

<span> </span></span></span>

<span data-ttu-id="53b07-105">_**主题上次修改时间：** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="53b07-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="53b07-106">Lync Server 部署可能包含以下任何类型的池：</span><span class="sxs-lookup"><span data-stu-id="53b07-106">Your Lync Server deployment may include any of the following types of pools:</span></span>

  - <span data-ttu-id="53b07-107">前端服务器</span><span class="sxs-lookup"><span data-stu-id="53b07-107">Front End Server</span></span>

  - <span data-ttu-id="53b07-108">中介服务器</span><span class="sxs-lookup"><span data-stu-id="53b07-108">Mediation Server</span></span>

  - <span data-ttu-id="53b07-109">持久聊天服务器</span><span class="sxs-lookup"><span data-stu-id="53b07-109">Persistent Chat Server</span></span>

  - <span data-ttu-id="53b07-110">边缘服务器</span><span class="sxs-lookup"><span data-stu-id="53b07-110">Edge Server</span></span>

<span data-ttu-id="53b07-111">如果整个池遇到中断，请针对池中的每个成员服务器执行这些过程。</span><span class="sxs-lookup"><span data-stu-id="53b07-111">If an entire pool experiences an outage, follow these procedures for each member server in the pool.</span></span>

  - <span data-ttu-id="53b07-112">对于前端池，先还原后端服务器，然后还原每个前端服务器。</span><span class="sxs-lookup"><span data-stu-id="53b07-112">For a Front End pool, restore the Back End Server first, and then restore each Front End Server.</span></span> <span data-ttu-id="53b07-113">有关详细信息，请参阅 [在 Lync server 2013 中还原企业版后端服务器](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) 和 [在 lync Server 2013 中还原企业版成员服务器](lync-server-2013-restoring-an-enterprise-edition-member-server.md)。</span><span class="sxs-lookup"><span data-stu-id="53b07-113">For details, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) and [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

  - <span data-ttu-id="53b07-114">对于所有其他类型的池，请还原每个成员服务器。</span><span class="sxs-lookup"><span data-stu-id="53b07-114">For all other types of pools, restore each member server.</span></span> <span data-ttu-id="53b07-115">有关详细信息，请参阅 [在 Lync server 2013 中还原企业版成员服务器](lync-server-2013-restoring-an-enterprise-edition-member-server.md)。</span><span class="sxs-lookup"><span data-stu-id="53b07-115">For details, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="53b07-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="53b07-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

