---
title: Lync Server 2013：阻止服务会话
description: Lync Server 2013：阻止服务会话。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 977dcc5c-2aac-48ef-86a1-a8d47b4d9e74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182553(v=OCS.15)
ms:contentKeyID: 48184866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 846a9da5330c3e64f61c27dfadd883f0c43a0ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436895"
---
# <a name="prevent-sessions-for-services-in-lync-server-2013"></a><span data-ttu-id="c3baa-103">在 Lync Server 2013 中阻止服务的会话</span><span class="sxs-lookup"><span data-stu-id="c3baa-103">Prevent sessions for services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3baa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3baa-104">

<span> </span></span></span>

<span data-ttu-id="c3baa-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="c3baa-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="c3baa-106">可以使用 Lync Server 控制面板阻止在特定计算机上运行的所有 Lync Server 2013 服务的新会话或阻止特定 Lync Server 2013 服务的新会话。</span><span class="sxs-lookup"><span data-stu-id="c3baa-106">You can use Lync Server Control Panel to prevent new sessions for all the Lync Server 2013 services running on a specific computer or to prevent new sessions for a specific Lync Server 2013 service.</span></span>

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a><span data-ttu-id="c3baa-107">阻止计算机上所有 Lync Server 服务的新会话</span><span class="sxs-lookup"><span data-stu-id="c3baa-107">To prevent new sessions for all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="c3baa-108">从属于 RTCUniversalServerAdmins 组成员的用户帐户 (或具有等效的用户权限) 或分配给 CsServerAdministrator 或 CsAdministrator 角色，请登录到你部署 Lync Server 2013 的网络中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="c3baa-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="c3baa-109">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c3baa-110">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="c3baa-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c3baa-111">在左侧导航栏中，单击 " **拓扑** "，然后单击 " **状态**"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-111">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="c3baa-112">在 " **状态** " 页面上，根据需要对列表进行排序或搜索以查找运行要阻止新会话的服务的计算机，然后单击该计算机。</span><span class="sxs-lookup"><span data-stu-id="c3baa-112">On the **Status** page, sort or search through the list as needed to find the computer that is running the services for which you want to prevent new sessions, and then click it.</span></span>

5.  <span data-ttu-id="c3baa-113">单击 " **操作**"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-113">Click **Action**.</span></span>

6.  <span data-ttu-id="c3baa-114">单击 " **阻止所有服务的新会话**"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-114">Click **Prevent new sessions for all services**.</span></span>

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a><span data-ttu-id="c3baa-115">阻止特定服务的新会话</span><span class="sxs-lookup"><span data-stu-id="c3baa-115">To prevent new sessions for a specific service</span></span>

1.  <span data-ttu-id="c3baa-116">从属于 RTCUniversalServerAdmins 组成员的用户帐户 (或具有等效的用户权限) 或分配给 CsServerAdministrator 或 CsAdministrator 角色，请登录到你部署 Lync Server 2013 的网络中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="c3baa-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="c3baa-117">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c3baa-118">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="c3baa-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c3baa-119">在左侧导航栏中，单击 " **拓扑** "，然后单击 " **状态**"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-119">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="c3baa-120">在 " **状态** " 页面上，根据需要对列表进行排序或搜索以查找运行要启动或停止的服务的计算机，然后单击它。</span><span class="sxs-lookup"><span data-stu-id="c3baa-120">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="c3baa-121">单击 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-121">Click **Properties**.</span></span>

6.  <span data-ttu-id="c3baa-122">对服务列表进行排序（如有必要），然后单击要阻止新会话的服务。</span><span class="sxs-lookup"><span data-stu-id="c3baa-122">Sort the list of services, if necessary, and click the service for which you want to prevent new sessions.</span></span>

7.  <span data-ttu-id="c3baa-123">单击 " **操作**"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-123">Click **Action**.</span></span>

8.  <span data-ttu-id="c3baa-124">单击 " **阻止新的服务会话**"。</span><span class="sxs-lookup"><span data-stu-id="c3baa-124">Click **Prevent new sessions for service**.</span></span>

9.  <span data-ttu-id="c3baa-125">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="c3baa-125">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c3baa-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c3baa-126">See Also</span></span>


[<span data-ttu-id="c3baa-127">管理 Lync Server 2013 拓扑</span><span class="sxs-lookup"><span data-stu-id="c3baa-127">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="c3baa-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3baa-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

