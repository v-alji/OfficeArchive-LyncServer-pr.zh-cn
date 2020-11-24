---
title: Lync Server 2013：使用 Lync Room System 管理 Web 门户
description: Lync Server 2013：使用 Lync 会议室系统管理 Web 门户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Lync Room System Administrative Web Portal
ms:assetid: c387b2a3-3e42-4642-af72-88126ed2820f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743660(v=OCS.15)
ms:contentKeyID: 62268951
ms.date: 11/13/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28c29677080bf081eae0fa4227e4cb56ccac697b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392483"
---
# <a name="using-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="b1eda-103">在 Lync Server 2013 中使用 Lync Room System 管理 Web 门户</span><span class="sxs-lookup"><span data-stu-id="b1eda-103">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1eda-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1eda-104">

<span> </span></span></span>

<span data-ttu-id="b1eda-105">_**主题上次修改时间：** 2014-11-10_</span><span class="sxs-lookup"><span data-stu-id="b1eda-105">_**Topic Last Modified:** 2014-11-10_</span></span>

<span data-ttu-id="b1eda-106">在服务器上部署 LRS 后，你可以通过从浏览器登录到 LRS 管理 Web 门户来检查所有 LRS 聊天室的状态。</span><span class="sxs-lookup"><span data-stu-id="b1eda-106">After you deploy LRS on the server, you can check the status of all LRS rooms by signing into the LRS Administrative Web Portal from a browser.</span></span>

<div>

## <a name="sign-in"></a><span data-ttu-id="b1eda-107">登录</span><span class="sxs-lookup"><span data-stu-id="b1eda-107">Sign in</span></span>

1.  <span data-ttu-id="b1eda-108">浏览到以下 URL：</span><span class="sxs-lookup"><span data-stu-id="b1eda-108">Browse to the following URL:</span></span>
    
    <span data-ttu-id="b1eda-109"> https:// \<fe-server\> /lrs</span><span class="sxs-lookup"><span data-stu-id="b1eda-109">https://\<fe-server\>/lrs</span></span>

2.  <span data-ttu-id="b1eda-110">输入 LRSSupport 帐户或已添加到 LRSSupportAdminGroup 安全组的帐户的凭据。</span><span class="sxs-lookup"><span data-stu-id="b1eda-110">Enter the credentials for the LRSSupport account or an account that has been added to the LRSSupportAdminGroup security group.</span></span>

<span data-ttu-id="b1eda-111">![Lync 聊天室系统管理门户登录屏幕](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync 聊天室系统管理门户登录屏幕")</span><span class="sxs-lookup"><span data-stu-id="b1eda-111">![Lync Room System Admin Portal Sign In screen](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System Admin Portal Sign In screen")</span></span>

</div>

<div>

## <a name="lrs-administrative-web-portal-summary-page"></a><span data-ttu-id="b1eda-112">LRS 管理 Web 门户摘要页面</span><span class="sxs-lookup"><span data-stu-id="b1eda-112">LRS Administrative Web Portal Summary Page</span></span>

<span data-ttu-id="b1eda-113">"摘要" 页面为服务器上部署的所有 LRS 聊天室提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="b1eda-113">The summary page provides the following information for all of the LRS rooms deployed on the server:</span></span>

  - <span data-ttu-id="b1eda-114">**标记**   管理员提供给聊天室的自定义名称。</span><span class="sxs-lookup"><span data-stu-id="b1eda-114">**Tag**   The custom name that the administrator gives to the room.</span></span> <span data-ttu-id="b1eda-115">可以通过在门户中单击会议室名称来设置标记。</span><span class="sxs-lookup"><span data-stu-id="b1eda-115">The Tag can be set in the portal by clicking on the room name.</span></span>

  - <span data-ttu-id="b1eda-116">**运行状况**   会议室的运行状况状态，这是源自会议室的“聚合运行状况”状态，它显示在“会议室设置”页面的“运行状况”部分下方。</span><span class="sxs-lookup"><span data-stu-id="b1eda-116">**Health**   The health status of the room, which is derived from the Aggregate Health status of the room, which is shown under the Health section of the Room Settings page.</span></span>

  - <span data-ttu-id="b1eda-117">**下次会议**   计划召开下次会议的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b1eda-117">**Next Meeting**   The date and time the next meeting is scheduled.</span></span>

  - <span data-ttu-id="b1eda-118">**LRS 版本、制造商、型号**   这些值在 LRS 中预设。</span><span class="sxs-lookup"><span data-stu-id="b1eda-118">**LRS Version, Manufacturer, Model**   These values are preset in LRS.</span></span> <span data-ttu-id="b1eda-119">根据制造商，这些字段可能留空。</span><span class="sxs-lookup"><span data-stu-id="b1eda-119">Depending on the manufacturer, these fields might be left blank.</span></span>

  - <span data-ttu-id="b1eda-120">**上次刷新**   显示上次刷新网页的时间。</span><span class="sxs-lookup"><span data-stu-id="b1eda-120">**Last Refresh**   Displays the last time the webpage was refreshed.</span></span>

<span data-ttu-id="b1eda-121">![Lync 聊天室系统管理门户摘要视图](images/Dn743660.f829ce90-dd95-4725-bd94-6870c5dcf046(OCS.15).png "Lync 聊天室系统管理门户摘要视图")</span><span class="sxs-lookup"><span data-stu-id="b1eda-121">![Lync Room System Admin Portal Summary View](images/Dn743660.f829ce90-dd95-4725-bd94-6870c5dcf046(OCS.15).png "Lync Room System Admin Portal Summary View")</span></span>

</div>

<div>

## <a name="lrs-room-information"></a><span data-ttu-id="b1eda-122">LRS 会议室信息</span><span class="sxs-lookup"><span data-stu-id="b1eda-122">LRS Room Information</span></span>

<span data-ttu-id="b1eda-123">门户的 "房间信息" 部分允许你查看和配置单个 LRS 会议室。</span><span class="sxs-lookup"><span data-stu-id="b1eda-123">The Room Info section of the portal allows you to view and configure individual LRS rooms.</span></span> <span data-ttu-id="b1eda-124">其中包含四个部分：设置、详细信息、疑难解答和运行状况。</span><span class="sxs-lookup"><span data-stu-id="b1eda-124">It contains four sections: Settings, Details, Troubleshooting, and Health.</span></span>

<div>

## <a name="settings"></a><span data-ttu-id="b1eda-125">设置</span><span class="sxs-lookup"><span data-stu-id="b1eda-125">Settings</span></span>

<span data-ttu-id="b1eda-126">在“设置”部分中，你可以设置会议室的密码、会议室标记和默认音量大小。</span><span class="sxs-lookup"><span data-stu-id="b1eda-126">In the Settings section, you can set the password, room tag, and default volume levels for the room.</span></span> <span data-ttu-id="b1eda-127">如果配置这些设置，则仅在重新启动 LRS 控制台后才会复制更改。</span><span class="sxs-lookup"><span data-stu-id="b1eda-127">If you configure these settings, the changes are replicated only after you restart the LRS console.</span></span> <span data-ttu-id="b1eda-128">你将仅看到版本15.12 和更高版本的 Lync 会议室系统的系统更新设置。</span><span class="sxs-lookup"><span data-stu-id="b1eda-128">You will only see System Updates settings for Lync Room Systems that are version 15.12 and later.</span></span>

<span data-ttu-id="b1eda-129">![Lync 聊天室系统管理门户聊天室设置](images/Dn743660.ab162e19-41ac-4991-9b2a-92575aa53eda(OCS.15).png "Lync 聊天室系统管理门户聊天室设置")</span><span class="sxs-lookup"><span data-stu-id="b1eda-129">![Lync Room System Admin Portal Room Settings](images/Dn743660.ab162e19-41ac-4991-9b2a-92575aa53eda(OCS.15).png "Lync Room System Admin Portal Room Settings")</span></span>

</div>

<div>

## <a name="details"></a><span data-ttu-id="b1eda-130">详细信息</span><span class="sxs-lookup"><span data-stu-id="b1eda-130">Details</span></span>

<span data-ttu-id="b1eda-131">详细信息部分提供 LRS 聊天室设置的只读摘要，包括：上次刷新的时间;下一次会议;上次更新、维护和校准;默认扬声器、麦克风和铃声设置;版本SIP URI;屏幕数和每个屏幕的详细信息;状态和活动。</span><span class="sxs-lookup"><span data-stu-id="b1eda-131">The Details section provides a read-only summary of the LRS room’s settings, including: the time of last refresh; next meeting; last updates, maintenance and calibration; default speaker, mic, and ringer settings; version; SIP URI; number of screens and details about each screen; status, and activity.</span></span>

<span data-ttu-id="b1eda-132">![Lync 聊天室系统管理门户详细信息视图](images/Dn743660.2958bbba-db74-4670-a920-87fdfb2fc22d(OCS.15).png "Lync 聊天室系统管理门户详细信息视图")</span><span class="sxs-lookup"><span data-stu-id="b1eda-132">![Lync Room System Admin Portal Detail View](images/Dn743660.2958bbba-db74-4670-a920-87fdfb2fc22d(OCS.15).png "Lync Room System Admin Portal Detail View")</span></span>

</div>

<div>

## <a name="troubleshooting"></a><span data-ttu-id="b1eda-133">疑难解答</span><span class="sxs-lookup"><span data-stu-id="b1eda-133">Troubleshooting</span></span>

<span data-ttu-id="b1eda-134">“疑难解答”部分可用于远程收集日志并将它们保存到指定位置。</span><span class="sxs-lookup"><span data-stu-id="b1eda-134">The Troubleshooting section can be used to remotely collect logs and save them to a specified location.</span></span> <span data-ttu-id="b1eda-135">您也可以重新启动 LRS console (LRS 用户界面) 或重启整个系统。</span><span class="sxs-lookup"><span data-stu-id="b1eda-135">You can also restart the LRS console (LRS user interface) or restart the entire system.</span></span> <span data-ttu-id="b1eda-136">若要收集日志，请以指定格式提供文件夹路径，并确保文件夹具有授予 LRS 计算机帐户的写入权限。</span><span class="sxs-lookup"><span data-stu-id="b1eda-136">To collect logs, provide a folder path in the specified format and make sure that the folder has write permissions given to the LRS machine account.</span></span> <span data-ttu-id="b1eda-137">如果日志太大，可能需要长达 5 分钟才能完成日志的收集。</span><span class="sxs-lookup"><span data-stu-id="b1eda-137">If the log size is too big, it can take up to 5 minutes to finish collecting logs.</span></span> <span data-ttu-id="b1eda-138">刷新页面将显示最新状态。</span><span class="sxs-lookup"><span data-stu-id="b1eda-138">Refreshing the page will give you the latest status.</span></span>

<span data-ttu-id="b1eda-139">![Lync 聊天室系统管理门户聊天室日志记录](images/Dn743660.749aee71-deaa-4ace-a146-fe2b349f0f42(OCS.15).png "Lync 聊天室系统管理门户聊天室日志记录")</span><span class="sxs-lookup"><span data-stu-id="b1eda-139">![Lync Room System Admin Portal Room Logging](images/Dn743660.749aee71-deaa-4ace-a146-fe2b349f0f42(OCS.15).png "Lync Room System Admin Portal Room Logging")</span></span>

</div>

<div>

## <a name="health"></a><span data-ttu-id="b1eda-140">运行状况</span><span class="sxs-lookup"><span data-stu-id="b1eda-140">Health</span></span>

<span data-ttu-id="b1eda-141">"运行状况" 部分提供了 Lync 服务器连接、音频设备、视频设备、复原状态和屏幕设备的运行状况的可视指示。</span><span class="sxs-lookup"><span data-stu-id="b1eda-141">The Health section gives a visual indication of the health of the Lync Server connection, audio device, video device, resiliency state, and screen device.</span></span>

<span data-ttu-id="b1eda-142">![Lync 聊天室系统管理门户聊天室运行状况](images/Dn743660.8cc644f8-8e3e-42d5-9079-045d8fe9daa7(OCS.15).png "Lync 聊天室系统管理门户聊天室运行状况")</span><span class="sxs-lookup"><span data-stu-id="b1eda-142">![Lync Room System Admin Portal Room Health](images/Dn743660.8cc644f8-8e3e-42d5-9079-045d8fe9daa7(OCS.15).png "Lync Room System Admin Portal Room Health")</span></span>

</div>

</div>

<div>

## <a name="additional-notes-about-the-administrative-web-portal"></a><span data-ttu-id="b1eda-143">有关管理 Web 门户的其他说明</span><span class="sxs-lookup"><span data-stu-id="b1eda-143">Additional Notes about the Administrative Web Portal</span></span>

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="b1eda-144">仅在重新启动 LRS 系统后应用设置更改。</span><span class="sxs-lookup"><span data-stu-id="b1eda-144">Setting changes are applied only after the LRS system is restarted.</span></span></P>
> <LI>
> <P><span data-ttu-id="b1eda-145">如果 LRSApp 帐户密码过期，你不能查看会议室的状态。</span><span class="sxs-lookup"><span data-stu-id="b1eda-145">If the LRSApp account password expires, you will not be able to see the status of the rooms.</span></span> <span data-ttu-id="b1eda-146">配置 LRSAppuser 帐户密码，使其永不过期，或者确保在密码即将过期时更新密码。</span><span class="sxs-lookup"><span data-stu-id="b1eda-146">Configure the LRSAppuser account password so that it never expires, or be sure to update the password when it’s near expiration.</span></span></P>
> <LI>
> <P><span data-ttu-id="b1eda-147">只有本地部署才支持 LRS 管理 web 门户。</span><span class="sxs-lookup"><span data-stu-id="b1eda-147">The LRS administrative web portal is supported for on-premises deployments only.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="frequently-asked-questions"></a><span data-ttu-id="b1eda-148">常见问题</span><span class="sxs-lookup"><span data-stu-id="b1eda-148">Frequently Asked Questions</span></span>

<div>

## <a name="why-cant-i-sign-in-to-the-administrative-web-portal"></a><span data-ttu-id="b1eda-149">为什么我无法登录管理 Web 门户？</span><span class="sxs-lookup"><span data-stu-id="b1eda-149">Why can’t I sign in to the administrative web portal?</span></span>

  - <span data-ttu-id="b1eda-150">打开时 https://localhost/lrs ，你将能够看到 "登录" 页面，但当你键入凭据时，无法登录。</span><span class="sxs-lookup"><span data-stu-id="b1eda-150">When you open https://localhost/lrs, you will be able to see the sign in page, but when you type in your credentials, you cannot sign in.</span></span> <span data-ttu-id="b1eda-151">在这种情况下，必须打开 https://FQDNofFEserver/lrs 才能登录到管理 web 门户。</span><span class="sxs-lookup"><span data-stu-id="b1eda-151">In this case, you must open https://FQDNofFEserver/lrs to sign in to the administrative web portal.</span></span>

  - <span data-ttu-id="b1eda-152">如果您要从中访问管理 web 门户的计算机在工作组中，"http://" 将不起作用。</span><span class="sxs-lookup"><span data-stu-id="b1eda-152">If the machine from which you are accessing the administrative web portal is in a workgroup, "http://" will not work.</span></span> <span data-ttu-id="b1eda-153">请改用 "https"。</span><span class="sxs-lookup"><span data-stu-id="b1eda-153">Use "https" instead.</span></span>

</div>

<div>

## <a name="why-cant-i-see-lrs-in-the-administrative-web-portal"></a><span data-ttu-id="b1eda-154">为什么我在管理 web 门户中看不到 LRS？</span><span class="sxs-lookup"><span data-stu-id="b1eda-154">Why can’t I see LRS in the administrative web portal?</span></span>

  - <span data-ttu-id="b1eda-155">请确保你在部署中拥有 LRS 帐户，并且根据 LRS 管理 Web 门户部署建议创建这些帐户。</span><span class="sxs-lookup"><span data-stu-id="b1eda-155">Make sure you have LRS accounts in your deployment and that they are created according to the LRS Administrative Web Portal deployment recommendations.</span></span> <span data-ttu-id="b1eda-156">请确保在 Lync server 上使用 Enable-CsMeetingRoom，而不是 Enable-Move-csuser 来设置 LRS 帐户。</span><span class="sxs-lookup"><span data-stu-id="b1eda-156">Make sure the LRS accounts are provisioned using Enable-CsMeetingRoom, not Enable-CsUser, on the Lync server.</span></span>

  - <span data-ttu-id="b1eda-157">如果已创建 LRS 帐户，并且在管理 web 门户中看不到帐户，请使用选定 **MeetingPortal** 组件的 Lync Server 日志记录工具收集服务器日志，然后将其发送到 LRS 支持联系人。</span><span class="sxs-lookup"><span data-stu-id="b1eda-157">If you have created LRS accounts and cannot see the accounts in administrative web portal, collect the server logs by using the Lync Server Logging tool with the **MeetingPortal** component selected, and then send them to your LRS support contact.</span></span>

</div>

<div>

## <a name="why-cant-i-see-the-status-of-lrs-in-the-administrative-web-portal"></a><span data-ttu-id="b1eda-158">为什么我在管理 web 门户中看不到 LRS 的状态？</span><span class="sxs-lookup"><span data-stu-id="b1eda-158">Why can’t I see the status of LRS in the administrative web portal?</span></span>

  - <span data-ttu-id="b1eda-159">请确保 LRSApp 用户帐户已启用 SIP。</span><span class="sxs-lookup"><span data-stu-id="b1eda-159">Make sure that the LRSApp user account is SIP-enabled.</span></span>

  - <span data-ttu-id="b1eda-160">如果仍有问题，请从 D： LRS 系统中收集跟踪 LRSAdminLogs 的 **日志** 文件 \\ \\ \\ ，然后将其发送到 LRS 支持联系人。</span><span class="sxs-lookup"><span data-stu-id="b1eda-160">If you are still having issues, collect the **Trace.log** file in the LRS system from D:\\Tracing\\LRSAdminLogs\\, and then send it to your LRS support contact.</span></span>

<span data-ttu-id="b1eda-161"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1eda-161"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

