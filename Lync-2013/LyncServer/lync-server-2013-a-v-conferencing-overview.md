---
title: Lync Server 2013 A/V 会议概述
description: Lync Server 2013 A/V 会议概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: A/V conferencing overview
ms:assetid: 9583de87-4618-4a99-a47a-45e8cc4cc221
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619186(v=OCS.15)
ms:contentKeyID: 49733747
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76ef4f76a4df0187a7c36394b2c95e99876df9be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439546"
---
# <a name="overview-of-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="bc83d-103">Lync Server 2013 中的 A/V 会议概述</span><span class="sxs-lookup"><span data-stu-id="bc83d-103">Overview of A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc83d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc83d-104">

<span> </span></span></span>

<span data-ttu-id="bc83d-105">_**主题上次修改时间：** 2012-10-13_</span><span class="sxs-lookup"><span data-stu-id="bc83d-105">_**Topic Last Modified:** 2012-10-13_</span></span>

<span data-ttu-id="bc83d-106">A/V 会议支持用户之间的实时音频和视频通信。</span><span class="sxs-lookup"><span data-stu-id="bc83d-106">A/V conferencing enables real-time audio and video communications between your users.</span></span> <span data-ttu-id="bc83d-107">部署会议时，可以选择启用和使用 web 会议和 A/V 会议，或者仅启用网络会议。</span><span class="sxs-lookup"><span data-stu-id="bc83d-107">When you deploy conferencing, you can choose to enable and use both web conferencing and A/V conferencing, or just web conferencing.</span></span>

<span data-ttu-id="bc83d-108">要规划 A/V 会议，需了解组织所需会议媒体类型要求的网络带宽。</span><span class="sxs-lookup"><span data-stu-id="bc83d-108">To plan for A/V conferencing, you need to understand the network bandwidth required by the type of conferencing media that your organization requires.</span></span> <span data-ttu-id="bc83d-109">这包含音频、视频和全景视频。</span><span class="sxs-lookup"><span data-stu-id="bc83d-109">This could include audio, video, and panoramic video.</span></span>

<span data-ttu-id="bc83d-110">在为用户启用 A/V 会议之前，请确保你的网络可以处理所产生的负载。</span><span class="sxs-lookup"><span data-stu-id="bc83d-110">Before you enable users for A/V conferencing, ensure that your network can handle the resulting load.</span></span> <span data-ttu-id="bc83d-111">如果网络带宽不足，用户体验可能大打折扣。</span><span class="sxs-lookup"><span data-stu-id="bc83d-111">Without sufficient network bandwidth, the user experience may be severely degraded.</span></span> <span data-ttu-id="bc83d-112">可以使用 "呼叫许可控制" (CAC) 管理由 A/V 会议使用的网络带宽。</span><span class="sxs-lookup"><span data-stu-id="bc83d-112">You can use call admission control (CAC) to manage the network bandwidth used by A/V Conferencing.</span></span> <span data-ttu-id="bc83d-113">这对受限网络（例如中央站点和分支站点之间的受限带宽链接）很重要。</span><span class="sxs-lookup"><span data-stu-id="bc83d-113">This is important for restricted networks, such as limited bandwidth links between central and branch sites.</span></span> <span data-ttu-id="bc83d-114">有关详细信息，请参阅 [Lync Server 2013 中的呼叫许可控制概述](lync-server-2013-overview-of-call-admission-control.md)。</span><span class="sxs-lookup"><span data-stu-id="bc83d-114">For details, see [Overview of call admission control in Lync Server 2013](lync-server-2013-overview-of-call-admission-control.md).</span></span> <span data-ttu-id="bc83d-115">有关媒体带宽要求的详细信息，请参阅 [Lync Server 2013 中媒体流量的网络带宽要求](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="bc83d-115">For details about media bandwidth requirements, see [Network bandwidth requirements for media traffic in Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md).</span></span>

<span data-ttu-id="bc83d-116">如果在网络中部署音频会议，用户需要耳机等音频设备来参加音频会议。</span><span class="sxs-lookup"><span data-stu-id="bc83d-116">If you deploy audio conferencing in your network, your users will need audio devices such as headsets to participate in an audio conference.</span></span> <span data-ttu-id="bc83d-117">如果部署视频会议，需要为用户部署视频设备，如网络摄像头。</span><span class="sxs-lookup"><span data-stu-id="bc83d-117">If you deploy video conferencing, you need to deploy video devices, such as webcams for users.</span></span> <span data-ttu-id="bc83d-118">我们建议你使用由 Microsoft 为所有设备类型认证的统一通信 (UC) 设备，以确保获得最佳的用户体验。</span><span class="sxs-lookup"><span data-stu-id="bc83d-118">We recommend that you use unified communications (UC) devices that are certified by Microsoft for all device types, to ensure an optimal user experience.</span></span> <span data-ttu-id="bc83d-119">有关 UC 认证的设备的详细信息，请参阅 "Lync 的电话和设备" [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861) 。</span><span class="sxs-lookup"><span data-stu-id="bc83d-119">For details about UC-certified devices, see "Phones and Devices for Lync" at [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861).</span></span> <span data-ttu-id="bc83d-120">对于音频或视频设备、设备部署和用户培训是考虑和规划的重要步骤。</span><span class="sxs-lookup"><span data-stu-id="bc83d-120">For either audio or video devices, device deployment, and user training are important steps for you to consider and plan for.</span></span>

<span data-ttu-id="bc83d-121">以下部分介绍音频和视频会议的功能，包括有关管理带宽和选择相应客户端的信息。</span><span class="sxs-lookup"><span data-stu-id="bc83d-121">The following sections describe the features for audio and video conferencing, including information about managing bandwidth and selecting the appropriate clients.</span></span>

<div>

## <a name="audio-conferencing-features"></a><span data-ttu-id="bc83d-122">音频会议功能</span><span class="sxs-lookup"><span data-stu-id="bc83d-122">Audio Conferencing Features</span></span>

<span data-ttu-id="bc83d-123">Lync Server 2013 提供了多个可用于为用户配置音频会议体验的功能，包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="bc83d-123">Lync Server 2013 provides several features that you can use to configure the audio conferencing experience for the user, including the following:</span></span>

  - <span data-ttu-id="bc83d-124">**观众静音**   演示者可以使用此设置将会议中的所有音频参与者设为静音，并将会议置于非演示者无法取消静音的状态中。</span><span class="sxs-lookup"><span data-stu-id="bc83d-124">**Audience mute**   The presenter can use this setting to mute all the audio participants in the conference and put the conference in a state where non-presenters cannot unmute themselves.</span></span>

  - <span data-ttu-id="bc83d-125">**会议进入/退出公告**   如果已启用电话拨入式会议，演示者可以使用此设置打开或关闭通知，以在会议正在进行时最大限度地减少干扰。</span><span class="sxs-lookup"><span data-stu-id="bc83d-125">**Conferencing Entry/Exit Announcements**   If you have enabled dial-in conferencing, presenters can use this setting to turn entry and exit announcements on or off to minimize distractions while a conference is in progress.</span></span>

  - <span data-ttu-id="bc83d-126">**通过拨出添加用户**   已授予权限的演示者和与会者可以向会议添加 PSTN 号码，并让会议拨出到这些号码。</span><span class="sxs-lookup"><span data-stu-id="bc83d-126">**Adding a user by dialing out**   Presenters and attendees that have been given permission, can add PSTN numbers to the conferences and have the conference dial-out to those numbers.</span></span>

</div>

<div>

## <a name="video-conferencing-features"></a><span data-ttu-id="bc83d-127">视频会议功能</span><span class="sxs-lookup"><span data-stu-id="bc83d-127">Video Conferencing Features</span></span>

<span data-ttu-id="bc83d-128">Lync Server 2013 提供了多个可用于为用户配置视频会议体验的功能，包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="bc83d-128">Lync Server 2013 provides several features that you can use to configure the video conferencing experience for the user, including the following:</span></span>

  - <span data-ttu-id="bc83d-129">**库视图**   在包含两人以上的视频会议中，用户可自动查看会议中的每个人。</span><span class="sxs-lookup"><span data-stu-id="bc83d-129">**Gallery View**   In video conferences that have more than two people, users automatically see everyone in the conference.</span></span> <span data-ttu-id="bc83d-130">如果与会者超过五名，那么最活跃与会者的视频将显示在最上面一行，并仅对其他与会者显示照片。</span><span class="sxs-lookup"><span data-stu-id="bc83d-130">If the conference has more than five participants, the video of the most active participants appear in the top row and only the photo appears for the other participants.</span></span> <span data-ttu-id="bc83d-131">默认情况下，已启用多方视频。</span><span class="sxs-lookup"><span data-stu-id="bc83d-131">Multiparty video is turned on by default.</span></span> <span data-ttu-id="bc83d-132">有关配置或关闭多方视频的详细信息，请参阅 [在 Lync Server 2013 中配置视频带宽](lync-server-2013-configuring-video-bandwidth.md)。</span><span class="sxs-lookup"><span data-stu-id="bc83d-132">For details about configuring or turning off multiparty video, see [Configuring video bandwidth in Lync Server 2013](lync-server-2013-configuring-video-bandwidth.md).</span></span>

  - <span data-ttu-id="bc83d-133">**全景视频**   如果在会议室中安装了圆桌视频会议设备，此功能将提供会议室的完整360度视图。</span><span class="sxs-lookup"><span data-stu-id="bc83d-133">**Panoramic Video**   If a RoundTable video conferencing device is installed in the conferencing room, this feature provides a full 360 degree view of the conference room.</span></span> <span data-ttu-id="bc83d-134">全景视频带只能用于 RoundTable 设备。</span><span class="sxs-lookup"><span data-stu-id="bc83d-134">The panoramic video strip is only available with RoundTable devices.</span></span>

  - <span data-ttu-id="bc83d-135">**仅演示者视频模式**   演示者可以配置会议，以便仅显示演示者的视频。</span><span class="sxs-lookup"><span data-stu-id="bc83d-135">**Presenter only video mode**   Presenters can configure the meeting so that only the video from the presenter is shown.</span></span> <span data-ttu-id="bc83d-136">如果提供了多个视频流并锁定到不同的源，这可阻止大型会议受到干扰。</span><span class="sxs-lookup"><span data-stu-id="bc83d-136">This prevents distractions in large meetings when multiple video streams are available and locking to different sources.</span></span> <span data-ttu-id="bc83d-137">此模式还适用于由 RoundTable 设备捕获和提供的视频。</span><span class="sxs-lookup"><span data-stu-id="bc83d-137">This mode also applies to video captured and provided by RoundTable devices.</span></span>

  - <span data-ttu-id="bc83d-138">**HD 视频**   用户可以在两方呼叫和多方会议中体验高达 HD 1080P 的分辨率。</span><span class="sxs-lookup"><span data-stu-id="bc83d-138">**HD video**   Users can experience resolutions up to HD 1080P in two-party calls and multiparty conferences.</span></span>

  - <span data-ttu-id="bc83d-139">**视频聚焦**   演示者可以配置会议，以便会议中的其他参与者只能看到来自所选参与者的视频。</span><span class="sxs-lookup"><span data-stu-id="bc83d-139">**Video Spotlight**   Presenters can configure the meeting so that only the video from a selected participant who is a video source is seen by the other participants in the conference.</span></span> <span data-ttu-id="bc83d-140">此模式还适用于由 RoundTable 设备针对全景视频捕获和提供的视频。</span><span class="sxs-lookup"><span data-stu-id="bc83d-140">This mode also applies to video captured and provided by RoundTable devices for panoramic video.</span></span>

<span data-ttu-id="bc83d-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc83d-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

