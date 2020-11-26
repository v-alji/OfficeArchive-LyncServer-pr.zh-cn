---
title: Lync Server 2013：添加或删除前端服务器
description: Lync Server 2013：添加或删除前端服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add or remove a Front End Server
ms:assetid: ab748733-6bad-4c93-8dda-db8d5271653d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205153(v=OCS.15)
ms:contentKeyID: 48185050
ms.date: 01/21/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 297bbf42dbba3d4f9926fd5ab9e0d7ed79349dc4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439273"
---
# <a name="add-or-remove-a-front-end-server-in-lync-server-2013"></a><span data-ttu-id="8ac06-103">Add or remove a Front End Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ac06-103">Add or remove a Front End Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ac06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ac06-104">

<span> </span></span></span>

<span data-ttu-id="8ac06-105">_**主题上次修改时间：** 2016-01-21_</span><span class="sxs-lookup"><span data-stu-id="8ac06-105">_**Topic Last Modified:** 2016-01-21_</span></span>

<span data-ttu-id="8ac06-106">将前端服务器添加到池中或从池中删除前端服务器时，您需要重新启动池。</span><span class="sxs-lookup"><span data-stu-id="8ac06-106">When you add a Front End Server to a pool, or remove a Front End Server from a pool, you then need to restart the pool.</span></span> <span data-ttu-id="8ac06-107">若要防止向用户提供任何服务中断，请在添加或删除前端服务器时使用以下过程。</span><span class="sxs-lookup"><span data-stu-id="8ac06-107">To prevent any interruption of service to users, use the following procedure when adding or removing a Front End Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8ac06-108">如果将新服务器添加到池，请将您的新池服务器更新为与池中的现有服务器相同的累积更新级别。</span><span class="sxs-lookup"><span data-stu-id="8ac06-108">If you're adding new servers to the pool, update your new pool servers to be at the same Cumulative Update level as the existing servers in the Pool.</span></span>



</div>

<div>

## <a name="to-add-or-remove-front-end-servers"></a><span data-ttu-id="8ac06-109">添加或删除前端服务器</span><span class="sxs-lookup"><span data-stu-id="8ac06-109">To add or remove Front End servers</span></span>

1.  <span data-ttu-id="8ac06-110">如果您要删除任何前端服务器，请首先停止与这些服务器的新连接。</span><span class="sxs-lookup"><span data-stu-id="8ac06-110">If you are removing any Front End Servers, first stop new connections to those servers.</span></span> <span data-ttu-id="8ac06-111">为此，您可以使用以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8ac06-111">To do so, you can use the following cmdlet:</span></span>
    
        Stop-CsWindowsServices -Graceful

2.  <span data-ttu-id="8ac06-112">当要删除的服务器没有当前会话时，请在这些服务器上停止 Lync Server 服务。</span><span class="sxs-lookup"><span data-stu-id="8ac06-112">When the servers being removed have no current sessions, stop Lync Server services on them.</span></span>

3.  <span data-ttu-id="8ac06-113">打开拓扑生成器，然后添加或删除必要的服务器。</span><span class="sxs-lookup"><span data-stu-id="8ac06-113">Open Topology Builder, and add or remove the necessary servers.</span></span>

4.  <span data-ttu-id="8ac06-114">发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="8ac06-114">Publish the topology.</span></span>

5.  <span data-ttu-id="8ac06-115">如果池已有两个前端服务器的两个前端服务器，或者从两个以上的服务器到两个服务器，则需要键入以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8ac06-115">If the pool has gone from having two Front End Servers to more than two, or gone from more than two servers to exactly two, you need to type the following cmdlet:</span></span>
    
        Reset-CsPoolRegistrarState-ResetType FullReset -PoolFqdn <PoolFqdn>
    
    <span data-ttu-id="8ac06-116">如果池具有三个或更多个服务器，则在键入此 cmdlet 时，至少有三个服务器必须处于运行状态。</span><span class="sxs-lookup"><span data-stu-id="8ac06-116">If the pool has three or more servers, then at least three of those servers must be running when you type this cmdlet.</span></span>

6.  <span data-ttu-id="8ac06-117">重新启动池中的所有前端服务器，一次一个。</span><span class="sxs-lookup"><span data-stu-id="8ac06-117">Restart all Front End Servers in the pool, one at a time.</span></span>

<span data-ttu-id="8ac06-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ac06-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

