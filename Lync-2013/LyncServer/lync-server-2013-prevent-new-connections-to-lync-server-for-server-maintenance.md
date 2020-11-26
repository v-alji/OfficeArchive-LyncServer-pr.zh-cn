---
title: 阻止与 Lync Server 的新连接进行服务器维护
description: 阻止与 Lync Server 的新连接进行服务器维护。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent new connections to Lync Server for server maintenance
ms:assetid: 22b27adf-a590-43bd-9306-a5789ae108d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520964(v=OCS.15)
ms:contentKeyID: 48183625
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd676467cdd6b5bb430f972e48c2f3a53f3f6f14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436893"
---
# <a name="prevent-new-connections-to-lync-server-2013-for-server-maintenance"></a><span data-ttu-id="be9ae-103">阻止与 Lync Server 2013 的新连接进行服务器维护</span><span class="sxs-lookup"><span data-stu-id="be9ae-103">Prevent new connections to Lync Server 2013 for server maintenance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be9ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be9ae-104">

<span> </span></span></span>

<span data-ttu-id="be9ae-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="be9ae-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="be9ae-106">Lync Server 使你能够使服务器脱机 (例如，将软件或硬件升级) 应用，而不会损失任何服务。</span><span class="sxs-lookup"><span data-stu-id="be9ae-106">Lync Server enables you to take a server offline (for example, to apply software or hardware upgrades) without any loss of service to users.</span></span>

<span data-ttu-id="be9ae-107">当你指定用于阻止新连接或呼叫池中的服务器的选项时，一旦你执行此选项，它将停止进行任何新的连接和调用。</span><span class="sxs-lookup"><span data-stu-id="be9ae-107">When you specify the option to prevent new connections or calls to a server in a pool, it stops taking any new connections and calls as soon as you implement this option.</span></span> <span data-ttu-id="be9ae-108">这些新连接和呼叫通过池中的其他服务器路由。</span><span class="sxs-lookup"><span data-stu-id="be9ae-108">These new connections and calls are routed through other servers in the pool.</span></span> <span data-ttu-id="be9ae-109">阻止新连接的服务器允许现有连接上的会话继续运行，直到它们自然结束。</span><span class="sxs-lookup"><span data-stu-id="be9ae-109">A server that is preventing new connections allows its sessions on existing connections to continue until they naturally end.</span></span> <span data-ttu-id="be9ae-110">当所有现有会话都已结束时，服务器可以脱机使用。</span><span class="sxs-lookup"><span data-stu-id="be9ae-110">When all existing sessions have ended, the server is ready to be taken offline.</span></span>

<span data-ttu-id="be9ae-111">当你阻止与前端服务器的新连接时，某些 Lync Server 功能和服务依赖于 DNS 负载平衡来确保它正常工作。</span><span class="sxs-lookup"><span data-stu-id="be9ae-111">When you prevent new connections to a Front End Server, some Lync Server features and services rely on DNS load balancing to ensure that it functions properly.</span></span> <span data-ttu-id="be9ae-112">如果未在池上使用 DNS 负载平衡，则通过这些服务的连接可能无法在服务器阻止新连接期间重新路由到其他服务器，因此当服务器脱机时，可能会中断某些会话和呼叫。</span><span class="sxs-lookup"><span data-stu-id="be9ae-112">If you are not using DNS load balancing on the pool, connections through these services may not be re-routed to other servers during the period that the server is preventing new connections, and thus when the server is taken offline some sessions and calls may be interrupted.</span></span> <span data-ttu-id="be9ae-113">依赖于 DNS 负载平衡以确保此选项正常运行的功能如下所示：</span><span class="sxs-lookup"><span data-stu-id="be9ae-113">The features that rely on DNS load balancing to ensure that this option operates properly are as follows:</span></span>

  - <span data-ttu-id="be9ae-114">助理</span><span class="sxs-lookup"><span data-stu-id="be9ae-114">Attendant</span></span>

  - <span data-ttu-id="be9ae-115">会议通知应用程序</span><span class="sxs-lookup"><span data-stu-id="be9ae-115">Conferencing Announcement application</span></span>

  - <span data-ttu-id="be9ae-116">响应组应用程序</span><span class="sxs-lookup"><span data-stu-id="be9ae-116">Response Group application</span></span>

  - <span data-ttu-id="be9ae-117">通知应用程序</span><span class="sxs-lookup"><span data-stu-id="be9ae-117">Announcement application</span></span>

  - <span data-ttu-id="be9ae-118">呼叫寄存应用程序</span><span class="sxs-lookup"><span data-stu-id="be9ae-118">Call Park application</span></span>

<span data-ttu-id="be9ae-119">有关 DNS 负载平衡的详细信息，请参阅规划文档中 [Lync Server 2013 中的 "DNS 负载平衡](lync-server-2013-dns-load-balancing.md) "。</span><span class="sxs-lookup"><span data-stu-id="be9ae-119">For details about DNS load balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

<span data-ttu-id="be9ae-120">除了阻止运行 Lync Server 的服务器上的所有服务的新连接之外，还可以阻止单个 Lync Server 服务的新连接。</span><span class="sxs-lookup"><span data-stu-id="be9ae-120">In addition to preventing new connections for all services on a server running Lync Server, you can also prevent new connections for individual Lync Server services.</span></span> <span data-ttu-id="be9ae-121">例如，此方法在你需要应用 Lync Server 更新（不需要整个服务器关闭）的情况下很有用。</span><span class="sxs-lookup"><span data-stu-id="be9ae-121">For example, this method is useful in a situation where you need to apply a Lync Server update that does not require the whole server to be shut down.</span></span> <span data-ttu-id="be9ae-122">请注意，当你阻止一个服务的连接时，你必须选择在服务的 Windows 列表中对其进行分组和显示的服务。</span><span class="sxs-lookup"><span data-stu-id="be9ae-122">Note that when you prevent connections for one service, you must select a service as it is grouped and displayed in the Windows list of services.</span></span> <span data-ttu-id="be9ae-123">例如，Lync Server Front-End 服务和用于监视的数据收集代理是单独的 Lync Server 服务，但在 Windows 服务列表中，它们将被合并并显示为 Lync Server 前端服务。</span><span class="sxs-lookup"><span data-stu-id="be9ae-123">For example, the Lync Server Front-End service and the data collection agent for Monitoring are separate Lync Server services, but in the Windows services list they are consolidated and shown as the Lync Server Front End service.</span></span> <span data-ttu-id="be9ae-124">你可以阻止 Lync Server 前端服务的新连接，但不能单独阻止这两个单独的基础 Lync 服务器服务的新连接。</span><span class="sxs-lookup"><span data-stu-id="be9ae-124">You can prevent new connections for the Lync Server Front End service, but you cannot prevent new connections for these two individual underlying Lync Server services separately.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="be9ae-125">如果将服务器设置为阻止新连接，然后重新启动服务器，则默认情况下，服务器将在启动后立即开始接受新连接。</span><span class="sxs-lookup"><span data-stu-id="be9ae-125">When you set a server to prevent new connections, and then restart the server, by default the server will immediately begin accepting new connections after it starts.</span></span> <span data-ttu-id="be9ae-126">若要防止这种情况，请将服务器设置为仅在重新启动服务器之前暂停和手动恢复。</span><span class="sxs-lookup"><span data-stu-id="be9ae-126">To prevent this, set the server to only pause and resume manually, before you restart the server.</span></span>



</div>

<div>

## <a name="to-prevent-new-connections-to-lync-server"></a><span data-ttu-id="be9ae-127">若要阻止与 Lync Server 的新连接，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="be9ae-127">To prevent new connections to Lync Server:</span></span>

1.  <span data-ttu-id="be9ae-128">以 Administrators 组成员的身份登录本地计算机。</span><span class="sxs-lookup"><span data-stu-id="be9ae-128">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="be9ae-129">打开 "服务" 管理单元控制台：单击 " **开始**"，指向 " **所有程序**"，指向 " **管理工具**"，然后单击 " **服务**"。</span><span class="sxs-lookup"><span data-stu-id="be9ae-129">Open the Services snap-in console: Click **Start**, point to **All Programs**, point to **Administrative Tools**, and then click **Services**.</span></span>

3.  <span data-ttu-id="be9ae-130">在列表中，双击要阻止新连接的 Lync Server Windows 服务。</span><span class="sxs-lookup"><span data-stu-id="be9ae-130">In the list, double-click the Lync Server Windows service to which you want to prevent new connections.</span></span>

4.  <span data-ttu-id="be9ae-131">在 "属性" 对话框中的 " **服务状态：已开始**" 下，单击 " **暂停**"。</span><span class="sxs-lookup"><span data-stu-id="be9ae-131">In the Properties dialog box, under **Service status: Started**, click **Pause**.</span></span>

5.  <span data-ttu-id="be9ae-132">（可选，但建议在 " **启动类型**" 旁边，单击 " **手动**"。</span><span class="sxs-lookup"><span data-stu-id="be9ae-132">Optionally, but recommended, next to **Startup type**, click **Manual**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="be9ae-133">如果将服务器设置为阻止新连接，然后重新启动服务器，则默认情况下，服务器将在启动后立即开始接受新连接。</span><span class="sxs-lookup"><span data-stu-id="be9ae-133">When you set a server to prevent new connections, and then restart the server, by default the server will immediately begin accepting new connections after it starts.</span></span> <span data-ttu-id="be9ae-134">若要防止这种情况，请将服务器设置为仅在重新启动服务器之前暂停和手动恢复。</span><span class="sxs-lookup"><span data-stu-id="be9ae-134">To prevent this, set the server to only pause and resume manually, before you restart the server.</span></span>

    
    </div>

6.  <span data-ttu-id="be9ae-135">完成后，单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="be9ae-135">When you are finished, click **OK**.</span></span>

<span data-ttu-id="be9ae-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be9ae-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

