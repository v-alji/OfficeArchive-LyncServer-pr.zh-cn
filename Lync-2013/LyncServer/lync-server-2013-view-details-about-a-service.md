---
title: Lync Server 2013：查看有关服务的详细信息
description: Lync Server 2013：查看有关服务的详细信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View details about a service
ms:assetid: bc8e8202-cd68-47e4-95b2-bb36e51cc124
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182578(v=OCS.15)
ms:contentKeyID: 48185253
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09cc5a86748f18a9a032fbf7e90682f46b324902
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443354"
---
# <a name="view-details-about-a-service-in-lync-server-2013"></a><span data-ttu-id="aebb9-103">在 Lync Server 2013 中查看有关服务的详细信息</span><span class="sxs-lookup"><span data-stu-id="aebb9-103">View details about a service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aebb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aebb9-104">

<span> </span></span></span>

<span data-ttu-id="aebb9-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="aebb9-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="aebb9-106">可以使用 Lync Server "控制面板" 查看拓扑中特定计算机上运行的每个服务的详细信息。</span><span class="sxs-lookup"><span data-stu-id="aebb9-106">You can use Lync Server Control Panel to view details about each service that is running on a specific computer in your topology.</span></span> <span data-ttu-id="aebb9-107">你可以查看每个服务的状态以及相关联的数据库、端口和依赖服务等详细信息。</span><span class="sxs-lookup"><span data-stu-id="aebb9-107">You can view the status of each service and details such as the associated databases, ports, and dependent services.</span></span>

<div>

## <a name="to-view-details-for-a-service"></a><span data-ttu-id="aebb9-108">查看服务的详细信息</span><span class="sxs-lookup"><span data-stu-id="aebb9-108">To view details for a service</span></span>

1.  <span data-ttu-id="aebb9-109">从分配给 Lync Server 2013 的任何预定义管理角色的用户帐户登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="aebb9-109">From a user account that is assigned to any of the predefined administrative roles for Lync Server 2013, log on to any computer in your internal deployment.</span></span> <span data-ttu-id="aebb9-110">有关 Lync Server 2013 中可用的预定义管理角色的详细信息，请参阅 [在 Lync server 2013 中规划基于角色的访问控制](lync-server-2013-planning-for-role-based-access-control.md)。</span><span class="sxs-lookup"><span data-stu-id="aebb9-110">For details about the predefined administrative roles available in Lync Server 2013, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span></span>

2.  <span data-ttu-id="aebb9-111">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="aebb9-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="aebb9-112">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="aebb9-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="aebb9-113">在左侧导航栏中，单击 " **拓扑** "，然后单击 " **状态**"。</span><span class="sxs-lookup"><span data-stu-id="aebb9-113">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="aebb9-114">在 " **状态** " 页面中，对列表进行排序或搜索，然后单击要查看的计算机。</span><span class="sxs-lookup"><span data-stu-id="aebb9-114">In the **Status** page, sort or search through the list and then click the computer that you want to view.</span></span>

5.  <span data-ttu-id="aebb9-115">单击 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="aebb9-115">Click **Properties**.</span></span>

6.  <span data-ttu-id="aebb9-116">在 " **查看计算机详细信息** " 窗口中，对服务列表进行排序（如有必要），然后单击要查看的服务。</span><span class="sxs-lookup"><span data-stu-id="aebb9-116">In the **View Computer Detail** window, sort the list of services, if necessary, and click the service you want to view.</span></span>

7.  <span data-ttu-id="aebb9-117">根据需要执行下列任一操作：</span><span class="sxs-lookup"><span data-stu-id="aebb9-117">Do any of the following as needed:</span></span>
    
      - <span data-ttu-id="aebb9-118">若要查看该特定服务的最新状态，请单击 " **获取服务状态**"。</span><span class="sxs-lookup"><span data-stu-id="aebb9-118">To see the latest status of that specific service, click **Get service status**.</span></span>
    
      - <span data-ttu-id="aebb9-119">若要查看特定服务的详细信息，请单击 " **属性** "，然后单击 " **关闭**"。</span><span class="sxs-lookup"><span data-stu-id="aebb9-119">To see the details for that specific service, click **Properties** and then click **Close**.</span></span>
    
      - <span data-ttu-id="aebb9-120">若要返回到拓扑中的所有计算机的列表，请单击 " **关闭**"。</span><span class="sxs-lookup"><span data-stu-id="aebb9-120">To return to the list of all computers in your topology, click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="aebb9-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aebb9-121">See Also</span></span>


[<span data-ttu-id="aebb9-122">管理 Lync Server 2013 拓扑</span><span class="sxs-lookup"><span data-stu-id="aebb9-122">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="aebb9-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aebb9-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

