---
title: Lync Server 2013：新的存档功能
description: Lync Server 2013：新的存档功能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Archiving features
ms:assetid: c002e367-41ad-498d-9d23-8b117ac435b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205225(v=OCS.15)
ms:contentKeyID: 48185288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5b69c90e62914284f178ae328375c6e350f5b3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425157"
---
# <a name="new-archiving-features-in-lync-server-2013"></a><span data-ttu-id="09872-103">Lync Server 2013 中新的存档功能</span><span class="sxs-lookup"><span data-stu-id="09872-103">New Archiving features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09872-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09872-104">

<span> </span></span></span>

<span data-ttu-id="09872-105">_**主题上次修改时间：** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="09872-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="09872-106">Lync Server 2013 中的存档可存档以下类型的内容：</span><span class="sxs-lookup"><span data-stu-id="09872-106">Archiving in Lync Server 2013 can archive the following types of content:</span></span>

  - <span data-ttu-id="09872-107">对等即时消息</span><span class="sxs-lookup"><span data-stu-id="09872-107">Peer-to-peer instant messages</span></span>

  - <span data-ttu-id="09872-108">会议 (会议) 的多方即时消息</span><span class="sxs-lookup"><span data-stu-id="09872-108">Conferences (meetings) that are multi-party instant messages</span></span>

  - <span data-ttu-id="09872-109">会议内容，包括上载的内容（例如讲义）以及与事件相关的内容（例如，加入、离开、上载、共享以及可见性变化）</span><span class="sxs-lookup"><span data-stu-id="09872-109">Conference content, including uploaded content (for example, handouts) and event-related content (for example, joining, leaving, uploading sharing, and changes in visibility)</span></span>

<span data-ttu-id="09872-110">此外，Lync Server 2013 中的存档提供了可提高部署和操作效率的新功能。</span><span class="sxs-lookup"><span data-stu-id="09872-110">Additionally, Archiving in Lync Server 2013 provides new features that improve deployment and operations efficiency.</span></span> <span data-ttu-id="09872-111">这些新功能包括：</span><span class="sxs-lookup"><span data-stu-id="09872-111">These new features consist of:</span></span>

  - <span data-ttu-id="09872-112">**Collocation 前端服务器上的存档。**</span><span class="sxs-lookup"><span data-stu-id="09872-112">**Collocation of Archiving on Front End Servers.**</span></span>   <span data-ttu-id="09872-113">Lync Server 2013 没有单独的存档服务器角色。</span><span class="sxs-lookup"><span data-stu-id="09872-113">Lync Server 2013 does not have a separate Archiving Server role.</span></span> <span data-ttu-id="09872-114">存档是在企业版部署中的所有前端服务器上提供的可选功能，也可以在标准版服务器上实现，可以为池或网站进行配置。</span><span class="sxs-lookup"><span data-stu-id="09872-114">Archiving is an optional feature available on all Front End Servers in an Enterprise Edition deployment, and on Standard Edition servers, that can be implemented configured for a pool or a site.</span></span>

  - <span data-ttu-id="09872-115">**Microsoft Exchange 集成。**</span><span class="sxs-lookup"><span data-stu-id="09872-115">**Microsoft Exchange integration.**</span></span>   <span data-ttu-id="09872-116">部署存档时，你可以将数据存储与托管在 Exchange 2013 上的所有用户的现有 Exchange 2013 存储进行存档，并将其邮箱置于 In-Place 保留，因此无需部署单独的 SQL Server 数据库来存档 Lync 数据。</span><span class="sxs-lookup"><span data-stu-id="09872-116">When you deploy Archiving, you can integrate data storage for Archiving with your existing Exchange 2013 storage for all users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, so you don’t need to deploy separate SQL Server databases to archive Lync data.</span></span> <span data-ttu-id="09872-117">如果你没有 Exchange 2013 部署，或者你不希望将其与 Exchange 进行集成，或者如果你有任何 Lync 2013 用户未托管在 Exchange 2013 上，并且其邮箱置于 In-Place 保留状态，则可以通过使用 SQL Server 从 Lync 通信存储已存档的数据来部署单独的存档数据库。</span><span class="sxs-lookup"><span data-stu-id="09872-117">If you do not have an Exchange 2013 deployment, or if you prefer not to integrate with it, or if you have any Lync 2013 users who are not homed on Exchange 2013 with their mailboxes put on In-Place Hold, you can deploy separate Archiving databases by using SQL Server to store archived data from Lync communications.</span></span> <span data-ttu-id="09872-118">如果你想要对部署中的部分而非所有用户使用 Microsoft Exchange 集成，则可以使用 Microsoft Exchange 集成和 Lync Server 2013 存档数据库。</span><span class="sxs-lookup"><span data-stu-id="09872-118">You can use both Microsoft Exchange integration and Lync Server 2013 Archiving databases if you want to use Microsoft Exchange integration for some but not all users in your deployment.</span></span> <span data-ttu-id="09872-119">有关 In-Place 保留的详细信息，请参阅的 "就地保留" [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500) 。</span><span class="sxs-lookup"><span data-stu-id="09872-119">For details about In-Place Hold, see “In-Place Hold” at [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500).</span></span>

  - <span data-ttu-id="09872-120">**SQL 应用商店镜像。**</span><span class="sxs-lookup"><span data-stu-id="09872-120">**SQL Store Mirroring.**</span></span>   <span data-ttu-id="09872-121">部署存档时，可以为存档数据库启用 SQL Server 数据库镜像。</span><span class="sxs-lookup"><span data-stu-id="09872-121">When you deploy Archiving, you can enable SQL Server database mirroring for your Archiving database.</span></span>

  - <span data-ttu-id="09872-122">**白板和投票的存档。**</span><span class="sxs-lookup"><span data-stu-id="09872-122">**Archiving of Whiteboards and Polls.**</span></span>   <span data-ttu-id="09872-123">已存档的会议内容现在包括在会议期间共享的白板和投票。</span><span class="sxs-lookup"><span data-stu-id="09872-123">Archived conference content now includes whiteboards and polls that are shared during the meeting.</span></span>

<span data-ttu-id="09872-124">以下类型的内容未存档：</span><span class="sxs-lookup"><span data-stu-id="09872-124">The following types of content are not archived:</span></span>

  - <span data-ttu-id="09872-125">对等文件传输</span><span class="sxs-lookup"><span data-stu-id="09872-125">Peer-to-peer file transfers</span></span>

  - <span data-ttu-id="09872-126">对等即时消息和会议的音频/视频</span><span class="sxs-lookup"><span data-stu-id="09872-126">Audio/video for peer-to-peer instant messages and conferences</span></span>

  - <span data-ttu-id="09872-127">对等即时消息和会议的应用程序共享</span><span class="sxs-lookup"><span data-stu-id="09872-127">Application sharing for peer-to-peer instant messages and conferences</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="09872-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09872-128">See Also</span></span>


[<span data-ttu-id="09872-129">在 Lync Server 2013 中规划存档</span><span class="sxs-lookup"><span data-stu-id="09872-129">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)  
  

<span data-ttu-id="09872-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09872-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

