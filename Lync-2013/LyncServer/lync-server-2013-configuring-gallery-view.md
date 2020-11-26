---
title: Lync Server 2013：配置库视图
description: Lync Server 2013：配置库视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Gallery View
ms:assetid: 4a609178-47d8-4682-ac8d-29f882801924
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204871(v=OCS.15)
ms:contentKeyID: 48184069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2aec2f1e3c7bff9a3736f40584a29880978b9daa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433092"
---
# <a name="configuring-gallery-view-in-lync-server-2013"></a><span data-ttu-id="b7b80-103">在 Lync Server 2013 中配置库视图</span><span class="sxs-lookup"><span data-stu-id="b7b80-103">Configuring Gallery View in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7b80-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7b80-104">

<span> </span></span></span>

<span data-ttu-id="b7b80-105">_**主题上次修改时间：** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="b7b80-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="b7b80-106">在 Lync Server 2013 中，你可以在会议策略中配置库查看视频会议。</span><span class="sxs-lookup"><span data-stu-id="b7b80-106">In Lync Server 2013, you configure Gallery View video conferencing in conferencing policy.</span></span> <span data-ttu-id="b7b80-107">默认情况下，库视图处于打开状态。</span><span class="sxs-lookup"><span data-stu-id="b7b80-107">Gallery View is turned on by default.</span></span> <span data-ttu-id="b7b80-108">如果你不想允许库视图，或者希望仅对某些用户允许它，你需要关闭会议策略中的功能。</span><span class="sxs-lookup"><span data-stu-id="b7b80-108">If you do not want to allow Gallery View, or want to allow it for only some users, you need to turn off the feature in conferencing policy.</span></span>

<span data-ttu-id="b7b80-109">当会议参与者的视频不可用时，如果在 Lync Server 2013 中部署高分辨率的照片，则用户的库视图体验将会增强。</span><span class="sxs-lookup"><span data-stu-id="b7b80-109">When a conference participant's video is not available, the users' Gallery View experience can be enhanced if you deploy high-resolution photos, a new feature in Lync Server 2013.</span></span> <span data-ttu-id="b7b80-110">高分辨率照片为存储在 Active Directory 域服务中的较小的、有限的分辨率联系人照片提供备用方案。</span><span class="sxs-lookup"><span data-stu-id="b7b80-110">High-resolution photos provide an alternative to the smaller, limited resolution contact photos stored in Active Directory Domain Services.</span></span> <span data-ttu-id="b7b80-111">高分辨率的照片存储在用户的 Exchange 2013 邮箱中，因此需要您将 Lync Server 2013 与 Exchange 2013 集成。</span><span class="sxs-lookup"><span data-stu-id="b7b80-111">High-resolution photos are stored in a user's Exchange 2013 mailbox, and, therefore, require you to integrate Lync Server 2013 with Exchange 2013.</span></span> <span data-ttu-id="b7b80-112">有关详细信息，请参阅 NextHop 博客文章 "集成 Exchange 2013 和 Lync Server 2013" [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987) 。</span><span class="sxs-lookup"><span data-stu-id="b7b80-112">For details, see the NextHop blog article, "Integrating Exchange 2013 and Lync Server 2013," at [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b7b80-113">每个博客的内容及其 URL 如有更改，恕不另行通知。</span><span class="sxs-lookup"><span data-stu-id="b7b80-113">The content of each blog and its URL are subject to change without notice.</span></span>



</div>

<span data-ttu-id="b7b80-114">你可以使用 Lync Server 2013 控制面板或使用以下 cmdlet 之一查看或修改库视图参数：</span><span class="sxs-lookup"><span data-stu-id="b7b80-114">You can view or modify the Gallery View parameters by using Lync Server 2013 Control Panel or by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="b7b80-115">**Get-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="b7b80-115">**Get-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="b7b80-116">**Set-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="b7b80-116">**Set-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="b7b80-117">**New-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="b7b80-117">**New-CsConferencingPolicy**</span></span>

<span data-ttu-id="b7b80-118">通过下列会议策略设置配置库视图：</span><span class="sxs-lookup"><span data-stu-id="b7b80-118">Configure Gallery View with the following conferencing policy settings:</span></span>

  - <span data-ttu-id="b7b80-119">**AllowMultiview**   此参数控制是否允许用户组织库查看视频会议。</span><span class="sxs-lookup"><span data-stu-id="b7b80-119">**AllowMultiview**   This parameter controls whether a user is allowed to organize Gallery View video conferences.</span></span> <span data-ttu-id="b7b80-120">此参数适用于用户创建的计划和临时会议。</span><span class="sxs-lookup"><span data-stu-id="b7b80-120">This parameter applies to scheduled and ad-hoc meetings created by the user.</span></span>
    
    <span data-ttu-id="b7b80-121">说明</span><span class="sxs-lookup"><span data-stu-id="b7b80-121">Examples:</span></span>
    
      - <span data-ttu-id="b7b80-122">对于用户 A，此参数设置为 True，其托管在 Lync Server 2013 池中。</span><span class="sxs-lookup"><span data-stu-id="b7b80-122">This parameter is set to True for User A, who is homed on a Lync Server 2013 pool.</span></span> <span data-ttu-id="b7b80-123">通过用户 A 组织的会议允许用户加入和接收多个视频流。</span><span class="sxs-lookup"><span data-stu-id="b7b80-123">Meetings organized by User A enable users to join and receive multiple video streams.</span></span>
    
      - <span data-ttu-id="b7b80-124">对于在 Lync Server 2013 池中托管的用户 B，此参数设置为 "False"。</span><span class="sxs-lookup"><span data-stu-id="b7b80-124">This parameter is set to False for User B, who is homed on a Lync Server 2013 pool.</span></span> <span data-ttu-id="b7b80-125">按用户 B 组织的会议的单个视频流与 Lync Server 2010 提供的视频会议体验类似。</span><span class="sxs-lookup"><span data-stu-id="b7b80-125">Meetings organized by User B have a single video stream that is similar to the video conference experience provided by Lync Server 2010.</span></span>
    
    <span data-ttu-id="b7b80-126">此参数确定哪些人可以组织允许多个视频流的会议。</span><span class="sxs-lookup"><span data-stu-id="b7b80-126">This parameter determines who can organize meetings that allow multiple video streams.</span></span> <span data-ttu-id="b7b80-127">允许多个视频流的会议参与者可能或不允许多个视频流接收多个视频流，具体取决于各自的权限 (请参阅 EnableMultiviewJoin 参数的说明) 。</span><span class="sxs-lookup"><span data-stu-id="b7b80-127">Participants in meetings that allow multiple video streams may or may not be allowed to receive multiple video streams, based on their individual permissions (see the description for the EnableMultiviewJoin parameter).</span></span>

  - <span data-ttu-id="b7b80-128">**EnableMultiviewJoin**   此参数控制会议中的参与者是否在允许会议的会议中接收库查看视频体验。</span><span class="sxs-lookup"><span data-stu-id="b7b80-128">**EnableMultiviewJoin**   This parameter controls whether a participant in a meeting receives the Gallery View video experience in meetings that allow it.</span></span> <span data-ttu-id="b7b80-129">此参数控制用户在其参与的任何会议中的体验。</span><span class="sxs-lookup"><span data-stu-id="b7b80-129">This parameter controls the user's experience in any meeting in which he or she participates.</span></span>
    
    <span data-ttu-id="b7b80-130">说明</span><span class="sxs-lookup"><span data-stu-id="b7b80-130">Examples:</span></span>
    
      - <span data-ttu-id="b7b80-131">对于用户 C，此参数设置为 True。当参与由用户 A 组织或启动的会议时，用户 C 可以接收多个视频流。用户 C 收到单个视频流，该视频流与 Lync Server 2010 在用户 B 组织或启动的会议中提供的视频会议体验类似。</span><span class="sxs-lookup"><span data-stu-id="b7b80-131">This parameter is set to True for User C. User C can receive multiple video streams when participating in a meeting organized or started by User A. User C receives a single video stream that is similar to the video conference experience provided by Lync Server 2010 when participating in a meeting organized or started by User B.</span></span>
    
      - <span data-ttu-id="b7b80-132">对于用户 D，此参数设置为 False。用户 D 接收单个视频流，该视频流与 Lync Server 2010 在参与由用户 A 或用户 B 组织的任何会议时所提供的视频会议体验类似。</span><span class="sxs-lookup"><span data-stu-id="b7b80-132">This parameter is set to False for User D. User D receives single video stream that is similar to the video conference experience provided by Lync Server 2010 when participating in any meeting organized by User A or User B.</span></span>

<span data-ttu-id="b7b80-133">以下过程是使用 Lync Server 命令行管理程序启用库观看视频会议的示例。</span><span class="sxs-lookup"><span data-stu-id="b7b80-133">The following procedure is an example of using Lync Server Management Shell to enable Gallery View video conferencing.</span></span>

<div>

## <a name="to-modify-conferencing-policy-for-gallery-view-video-conferencing"></a><span data-ttu-id="b7b80-134">修改库的会议策略查看视频会议</span><span class="sxs-lookup"><span data-stu-id="b7b80-134">To modify conferencing policy for Gallery View video conferencing</span></span>

1.  <span data-ttu-id="b7b80-135">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="b7b80-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="b7b80-136">在命令行中，运行以下 cmdlet 以编辑会议策略：</span><span class="sxs-lookup"><span data-stu-id="b7b80-136">At the command line, run the following cmdlet to edit conferencing policy:</span></span>
    
        Set-CsConferencingPolicy -Identity Pool01ConferencingPolicy -AllowMultiview $true -EnableMultiviewJoin $true 

<span data-ttu-id="b7b80-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7b80-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

