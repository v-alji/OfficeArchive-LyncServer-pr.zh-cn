---
title: Lync Server 2013：新的会议功能
description: Lync Server 2013：新的会议功能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New conferencing features
ms:assetid: feeb81e8-1424-408c-a440-886aa0fb133c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413085(v=OCS.15)
ms:contentKeyID: 48185966
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 832d1fdf916c3e97dc7eca7fc1378fe7cfa7c086
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425120"
---
# <a name="new-conferencing-features-in-lync-server-2013"></a><span data-ttu-id="3d3b5-103">Lync Server 2013 中新的会议功能</span><span class="sxs-lookup"><span data-stu-id="3d3b5-103">New conferencing features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d3b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d3b5-104">

<span> </span></span></span>

<span data-ttu-id="3d3b5-105">_**主题上次修改时间：** 2012-11-08_</span><span class="sxs-lookup"><span data-stu-id="3d3b5-105">_**Topic Last Modified:** 2012-11-08_</span></span>

<span data-ttu-id="3d3b5-106">Lync Server 2013 引入了一些新功能，可增强会议，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-106">Lync Server 2013 introduces several new features that enhance conferencing, as described in the following list.</span></span>

  - <span data-ttu-id="3d3b5-107">**加入启动器**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-107">**Join Launcher**</span></span>
    
    <span data-ttu-id="3d3b5-108">Lync Server 2013 更新联接启动器，以便在启动客户端之前验证每个会议，并为在以下客户端中打开会议提供支持：</span><span class="sxs-lookup"><span data-stu-id="3d3b5-108">Lync Server 2013 updates the Join launcher to validate each meeting before launching a client, and to provide support for opening a meeting in the following clients:</span></span>
    
      - <span data-ttu-id="3d3b5-109">Windows Phone 7</span><span class="sxs-lookup"><span data-stu-id="3d3b5-109">Windows Phone 7</span></span>
    
      - <span data-ttu-id="3d3b5-110">Android 设备</span><span class="sxs-lookup"><span data-stu-id="3d3b5-110">Android devices</span></span>
    
      - <span data-ttu-id="3d3b5-111">Apple iOS 设备</span><span class="sxs-lookup"><span data-stu-id="3d3b5-111">Apple iOS devices</span></span>
    
      - <span data-ttu-id="3d3b5-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3d3b5-112">Windows 8</span></span>
    
      - <span data-ttu-id="3d3b5-113">Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="3d3b5-113">Internet Explorer 10</span></span>

  - <span data-ttu-id="3d3b5-114">**更新的 PowerPoint 共享**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-114">**Updated PowerPoint Sharing**</span></span>
    
    <span data-ttu-id="3d3b5-115">Lync Server 2013 现在使用 Office Web Apps 和 Office Web Apps 服务器 (以前称为 WAC Server) 来处理 PowerPoint 演示文稿。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-115">Lync Server 2013 now uses Office Web Apps and the Office Web Apps Server (formerly known as WAC Server) to handle PowerPoint presentations.</span></span> <span data-ttu-id="3d3b5-116">Office Web Apps 服务器的使用允许更高分辨率显示和更好地支持 PowerPoint 功能、访问更多类型的移动设备 (Lync Server 2013 使用标准 DHTML 和 JavaScript 将 PowerPoint 演示文稿广播) ，以及具有相应权限的用户可在独立于演示文稿本身的情况下滚动浏览 PowerPoint 演示文稿的功能。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-116">The use of Office Web Apps Server allows for higher-resolution displays and better support for PowerPoint capabilities, access to more types of mobile devices (Lync Server 2013 uses standard DHTML and JavaScript to broadcast PowerPoint presentations), and the ability for users with the appropriate privileges to scroll through a PowerPoint presentation independent of the presentation itself.</span></span>

  - <span data-ttu-id="3d3b5-117">**库视图和 HD 视频会议**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-117">**Gallery View and HD Video Conferencing**</span></span>
    
    <span data-ttu-id="3d3b5-118">在视频会议中，用户可以同时查看多达五个会议参与者的视频。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-118">In video conferences, users can see videos of up to five conference participants at the same time.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3d3b5-119">与最多75个参与者的会议中，库视图很有经验。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-119">Gallery View is experienced in conferences with up to 75 participants.</span></span> <span data-ttu-id="3d3b5-120">当会议的参与者大于75时，体验将恢复为单视图。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-120">When the conference gets larger than 75 participants, the experience reverts to single view.</span></span>

    
    </div>

  - <span data-ttu-id="3d3b5-121">**HD 视频**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-121">**HD Video**</span></span>
    
    <span data-ttu-id="3d3b5-122">用户可以在两方呼叫和多方会议中体验高达 HD 1080P 的分辨率。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-122">Users can experience resolutions up to HD 1080P in two-party calls and multiparty conferences.</span></span>

  - <span data-ttu-id="3d3b5-123">**仅演示者视频模式**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-123">**Presenter Only Video Mode**</span></span>
    
    <span data-ttu-id="3d3b5-124">演示者可以配置会议，以便仅显示演示者的视频。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-124">Presenters can configure the conference so that only the video from the presenter is shown.</span></span> <span data-ttu-id="3d3b5-125">当多个视频流可用且锁定到不同的源时，此模式可防止大型会议中的干扰。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-125">This mode prevents distractions in large conferences when multiple video streams are available and locking to different sources.</span></span> <span data-ttu-id="3d3b5-126">此模式也适用于由会议设备捕获和提供的视频。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-126">This mode also applies to video captured and provided by conferencing devices.</span></span>

  - <span data-ttu-id="3d3b5-127">**视频聚焦**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-127">**Video Spotlight**</span></span>
    
    <span data-ttu-id="3d3b5-128">演示者可以配置会议，以便会议中的每个人只能看到来自所选参与者的视频。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-128">Presenters can configure the conference so that only the video from a selected participant who is a video source is seen by everyone in the conference.</span></span> <span data-ttu-id="3d3b5-129">此模式还适用于通过全景视频的会议设备捕获和提供的视频。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-129">This mode also applies to video captured and provided by conferencing devices for panoramic video.</span></span>

  - <span data-ttu-id="3d3b5-130">**非企业语音用户拨出式会议**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-130">**Dial-out Conferencing for non-Enterprise Voice users**</span></span>
    
    <span data-ttu-id="3d3b5-131">Lync Server 2013 现允许未启用企业语音的参与者从会议会议启动拨出呼叫。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-131">Lync Server 2013 now allows participants that are not Enterprise Voice enabled to initiate dial-out calls from a meeting conference.</span></span> <span data-ttu-id="3d3b5-132">管理员可对此功能进行配置。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-132">This feature is configurable by the administrator.</span></span>

  - <span data-ttu-id="3d3b5-133">**存档**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-133">**Archiving**</span></span>
    
    <span data-ttu-id="3d3b5-134">如果 Exchange Server 集成已启用存档，则在会议期间共享的任何文档将存档到 Exchange 2013 数据存储中。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-134">Any document that is shared during a conference is archived into Exchange 2013 data storage if Exchange Server integration is enabled with Archiving.</span></span> <span data-ttu-id="3d3b5-135">这包括 PowerPoint 演示文稿、附件、白板和投票。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-135">This includes PowerPoint presentations, attachments, whiteboards and polls.</span></span>

  - <span data-ttu-id="3d3b5-136">**会议邀请自定义**</span><span class="sxs-lookup"><span data-stu-id="3d3b5-136">**Meeting Invite Customization**</span></span>
    
    <span data-ttu-id="3d3b5-137">管理员可使用 Lync Server 控制面板或 Lync Server 命令行管理程序自定义联机会议的电子邮件邀请。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-137">Administrators can customize email invitations for online meetings using Lync Server Control Panel or Lync Server Management Shell.</span></span> <span data-ttu-id="3d3b5-138">自定义项可以包括徽标、帮助文本、法律文本和页脚文本的 Url。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-138">Customizations can include URLs for logos, help text, legal text, and footer text.</span></span> <span data-ttu-id="3d3b5-139">所有后续邀请将包含自定义设置。</span><span class="sxs-lookup"><span data-stu-id="3d3b5-139">All subsequent invitations will include the customizations.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="3d3b5-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d3b5-140">See Also</span></span>


[<span data-ttu-id="3d3b5-141">在 Lync Server 2013 中规划会议</span><span class="sxs-lookup"><span data-stu-id="3d3b5-141">Planning for conferencing in Lync Server 2013</span></span>](lync-server-2013-planning-for-conferencing.md)  
  

<span data-ttu-id="3d3b5-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d3b5-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

