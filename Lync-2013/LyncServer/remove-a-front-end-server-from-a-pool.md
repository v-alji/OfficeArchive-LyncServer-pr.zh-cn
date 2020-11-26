---
title: 从池中删除前端服务器
description: 从池中删除前端服务器。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove a Front End Server from a pool
ms:assetid: 767225c9-7c0b-4d54-a407-d77134ba2abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688095(v=OCS.15)
ms:contentKeyID: 49733694
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45560a6f43288b47c0f85f880a190e31f2c8c04d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440323"
---
# <a name="remove-a-front-end-server-from-a-pool"></a><span data-ttu-id="6c069-103">从池中删除前端服务器</span><span class="sxs-lookup"><span data-stu-id="6c069-103">Remove a Front End Server from a pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c069-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c069-104">

<span> </span></span></span>

<span data-ttu-id="6c069-105">_**主题上次修改时间：** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="6c069-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="6c069-106">Microsoft Lync Server 2010 Enterprise Edition 前端服务器不能作为独立计算机存在。</span><span class="sxs-lookup"><span data-stu-id="6c069-106">The Microsoft Lync Server 2010 Enterprise Edition Front End Server cannot exist as a stand-alone computer.</span></span> <span data-ttu-id="6c069-107">它必须定义为前端池，即使池中只有一台计算机。</span><span class="sxs-lookup"><span data-stu-id="6c069-107">It must be defined as a Front End pool, even if there is only a single computer in the pool.</span></span>

<span data-ttu-id="6c069-108">本主题将指导你完成从现有前端池删除单个前端服务器的过程。</span><span class="sxs-lookup"><span data-stu-id="6c069-108">This topic guides you through the process of removing an individual Front End Server from an existing Front End pool.</span></span> <span data-ttu-id="6c069-109">如果前端服务器是池中的最后一个服务器，或者如果你完全删除该池，请参阅 [删除前端池或标准版服务器](remove-front-end-pool-or-standard-edition-server.md)。</span><span class="sxs-lookup"><span data-stu-id="6c069-109">If the Front End Server is the last server in the pool or if you are removing the pool completely, see [Remove Front End pool or Standard Edition server](remove-front-end-pool-or-standard-edition-server.md).</span></span> <span data-ttu-id="6c069-110">删除前端池之前无需删除单个前端服务器。</span><span class="sxs-lookup"><span data-stu-id="6c069-110">There is no need to remove the individual Front End Servers before you remove the Front End pool.</span></span> <span data-ttu-id="6c069-111">删除池时，删除每个前端服务器。</span><span class="sxs-lookup"><span data-stu-id="6c069-111">When you remove the pool, you remove each Front End Server.</span></span>

<div>

## <a name="to-remove-a-front-end-server-from-a-pool"></a><span data-ttu-id="6c069-112">从池中删除前端服务器</span><span class="sxs-lookup"><span data-stu-id="6c069-112">To remove a Front End Server from a pool</span></span>

1.  <span data-ttu-id="6c069-113">打开 Lync Server 2013 前端服务器，打开拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="6c069-113">Open the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="6c069-114">导航到 Lync Server 2010 节点。</span><span class="sxs-lookup"><span data-stu-id="6c069-114">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="6c069-115">展开 " **企业版前端池**"，展开要删除的前端服务器的前端池，右键单击要删除的前端服务器，然后单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="6c069-115">Expand **Enterprise Edition Front End pools**, expand the Front End pool with the Front End Server that you want to remove, right-click the Front End Server that you want to remove, and then click **Delete**.</span></span>

<span data-ttu-id="6c069-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c069-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

