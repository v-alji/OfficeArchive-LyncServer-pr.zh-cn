---
title: Lync Server 2013：会议的迁移注意事项
description: Lync Server 2013：会议的迁移注意事项。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration considerations for meetings
ms:assetid: a9807d58-99a3-4cff-b4c6-74950d106a2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412800(v=OCS.15)
ms:contentKeyID: 61097556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e238405acf7bc2a96fd2efd4cca761c1f1f258fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425582"
---
# <a name="migration-considerations-for-meetings-in-lync-server-2013"></a><span data-ttu-id="3210e-103">Lync Server 2013 中的会议的迁移注意事项</span><span class="sxs-lookup"><span data-stu-id="3210e-103">Migration considerations for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3210e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3210e-104">

<span> </span></span></span>

<span data-ttu-id="3210e-105">_**主题上次修改时间：** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="3210e-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="3210e-106">本节将讨论以下主题：</span><span class="sxs-lookup"><span data-stu-id="3210e-106">The following topics are discussed in this section:</span></span>

  - <span data-ttu-id="3210e-107">Microsoft Lync Server 2013 中的会议更改</span><span class="sxs-lookup"><span data-stu-id="3210e-107">Changes to meetings in Microsoft Lync Server 2013</span></span>

  - <span data-ttu-id="3210e-108">基于用户的会议需求迁移用户</span><span class="sxs-lookup"><span data-stu-id="3210e-108">Migrating users based on their conferencing needs</span></span>

  - <span data-ttu-id="3210e-109">迁移现有会议和会议内容</span><span class="sxs-lookup"><span data-stu-id="3210e-109">Migrating existing meetings and meeting content</span></span>

  - <span data-ttu-id="3210e-110">Lync Server 2010 迁移期间的用户体验</span><span class="sxs-lookup"><span data-stu-id="3210e-110">User experience during Lync Server 2010 migration</span></span>

  - <span data-ttu-id="3210e-111">Office 通信服务器 2007 R2 迁移期间的用户体验</span><span class="sxs-lookup"><span data-stu-id="3210e-111">User Experience during Office Communications Server 2007 R2 migration</span></span>

  - <span data-ttu-id="3210e-112">Microsoft Lync 2013 与早期服务器版本上的会议兼容</span><span class="sxs-lookup"><span data-stu-id="3210e-112">Microsoft Lync 2013 compatibility with meetings on earlier server versions</span></span>

<div>

## <a name="changes-to-meetings-in-lync-server-2013"></a><span data-ttu-id="3210e-113">Lync Server 2013 中的会议更改</span><span class="sxs-lookup"><span data-stu-id="3210e-113">Changes to Meetings in Lync Server 2013</span></span>

<span data-ttu-id="3210e-114">**Lync Server 2013 功能。**</span><span class="sxs-lookup"><span data-stu-id="3210e-114">**Lync Server 2013 features.**</span></span>   <span data-ttu-id="3210e-115">Lync Server 2013 提供新的会议功能，这些功能将在帐户移动到 Lync Server 2013 并使用 Lync 2013 客户端登录后向用户提供。</span><span class="sxs-lookup"><span data-stu-id="3210e-115">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="3210e-116">[Lync server 2013 中的新会议功能](lync-server-2013-new-conferencing-features.md)概述了新功能，以及[lync server 2013 中客户端的新增](lync-server-2013-what-s-new-for-clients.md)功能。</span><span class="sxs-lookup"><span data-stu-id="3210e-116">New features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="3210e-117">**会议 URL。**</span><span class="sxs-lookup"><span data-stu-id="3210e-117">**Meeting URL.**</span></span>   <span data-ttu-id="3210e-118">在 Lync Server 2010 中，Lync Server 2013 中的所有新计划会议都具有 https://的 URL 前缀，并且现有会议与用户帐户一起迁移。</span><span class="sxs-lookup"><span data-stu-id="3210e-118">As in Lync Server 2010, all newly scheduled meetings in Lync Server 2013 have a URL prefix of https:// and existing meetings migrate along with user accounts.</span></span> <span data-ttu-id="3210e-119">但是，Lync Server 2013 不支持 Office 通信服务器 2007 R2 会议呼叫 (conf://URL 前缀) 或 web 会议 (meet://URL 前缀) 。</span><span class="sxs-lookup"><span data-stu-id="3210e-119">However, Lync Server 2013 does not support the Office Communications Server 2007 R2 conference call (conf:// URL prefix) or web conference (meet:// URL prefix).</span></span> <span data-ttu-id="3210e-120">有关详细信息，请参阅本主题后面部分的 "从 Office 通信服务器迁移会议 2007 R2"。</span><span class="sxs-lookup"><span data-stu-id="3210e-120">See “Migrating Meetings from Office Communications Server 2007 R2” later in this topic for more information.</span></span>

<span data-ttu-id="3210e-121">**客户端支持。**</span><span class="sxs-lookup"><span data-stu-id="3210e-121">**Client support.**</span></span>   <span data-ttu-id="3210e-122">与 Lync Server 2010 不同，Lync Server 2013 不支持用于会议的 Office Communicator 客户端。</span><span class="sxs-lookup"><span data-stu-id="3210e-122">Unlike Lync Server 2010, Lync Server 2013 does not support Office Communicator clients for conferencing.</span></span> <span data-ttu-id="3210e-123">无法使用以下客户端加入通过 Lync 2013 的联机会议加载项安排的会议：</span><span class="sxs-lookup"><span data-stu-id="3210e-123">You cannot use the following clients to join meetings scheduled through the Online Meeting Add-in for Lync 2013:</span></span>

  - <span data-ttu-id="3210e-124">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="3210e-124">Office Communicator 2007 R2</span></span>

  - <span data-ttu-id="3210e-125">Microsoft Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="3210e-125">Microsoft Office Communications Server 2007 R2 Attendant</span></span>

  - <span data-ttu-id="3210e-126">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="3210e-126">Office Communicator 2007</span></span>

  - <span data-ttu-id="3210e-127">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="3210e-127">Office Live Meeting 2007</span></span>

<span data-ttu-id="3210e-128">在迁移期间，Office Communicator 2007 R2 用户应使用 Lync Web App 2013 加入 Lync Server 2013 会议，直到他们的客户升级。</span><span class="sxs-lookup"><span data-stu-id="3210e-128">During migration, Office Communicator 2007 R2 users should use Lync Web App 2013 to join Lync Server 2013 meetings until their clients are upgraded.</span></span> <span data-ttu-id="3210e-129">请注意，Office Communicator 2007 R2 用户可以继续使用其现有客户端与 Lync Server 2013 进行状态和 IM 功能，但不支持会议功能。</span><span class="sxs-lookup"><span data-stu-id="3210e-129">Note that Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

<div>


</div>

</div>

<div>

## <a name="migrating-users-based-on-their-conferencing-needs"></a><span data-ttu-id="3210e-130">基于用户的会议需求迁移用户</span><span class="sxs-lookup"><span data-stu-id="3210e-130">Migrating Users Based on Their Conferencing Needs</span></span>

<span data-ttu-id="3210e-131">**频繁的会议组织者。**</span><span class="sxs-lookup"><span data-stu-id="3210e-131">**Frequent meeting organizers.**</span></span>   <span data-ttu-id="3210e-132">请考虑在流程早期迁移频繁的会议组织者，以便他们可以利用 [Lync server 2013 的新会议功能](lync-server-2013-new-conferencing-features.md) 中概述的新 Lync server 2013 和 lync 2013 功能，以及 [lync server 2013 中客户端的新增](lync-server-2013-what-s-new-for-clients.md)功能。</span><span class="sxs-lookup"><span data-stu-id="3210e-132">Consider migrating frequent meeting organizers early in the process so that they can take advantage of the new Lync Server 2013 and Lync 2013 features outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="3210e-133">**Live Meeting 用户。**</span><span class="sxs-lookup"><span data-stu-id="3210e-133">**Live Meeting users.**</span></span>   <span data-ttu-id="3210e-134">如果您从 Office 通信服务器 2007 R2 迁移，并且您有需要特定于 Live Meeting 的 web 会议功能的用户（特别是对大型会议和休息会议室的支持），则可以使用以下选项：</span><span class="sxs-lookup"><span data-stu-id="3210e-134">If you are migrating from Office Communications Server 2007 R2 and you have users who need web conferencing features specific to Live Meeting—particularly support for large meetings and break-out rooms—you have the following options:</span></span>

  - <span data-ttu-id="3210e-135">建议组织者使用 Live Meeting 服务（如果在你的组织中可用）。</span><span class="sxs-lookup"><span data-stu-id="3210e-135">Advise organizers to use the Live Meeting service, if available in your organization.</span></span>

  - <span data-ttu-id="3210e-136">让组织者驻留在早期版本的 Office 通信服务器上，以便他们可以继续安排基于服务器的 Live Meeting web 会议。</span><span class="sxs-lookup"><span data-stu-id="3210e-136">Leave the organizers homed on the earlier version of Office Communications Server, so they can continue to schedule server-based Live Meeting web conferences.</span></span>

</div>

<div>

## <a name="migrating-existing-meetings-and-meeting-content"></a><span data-ttu-id="3210e-137">迁移现有会议和会议内容</span><span class="sxs-lookup"><span data-stu-id="3210e-137">Migrating Existing Meetings and Meeting Content</span></span>

<div>

## <a name="migrating-meetings-from-lync-server-2010"></a><span data-ttu-id="3210e-138">从 Lync Server 2010 迁移会议</span><span class="sxs-lookup"><span data-stu-id="3210e-138">Migrating Meetings from Lync Server 2010</span></span>

<span data-ttu-id="3210e-139">将用户从 Lync Server 2010 移动到 Lync Server 2013 时，以下信息将与用户帐户一起移动：</span><span class="sxs-lookup"><span data-stu-id="3210e-139">When you move a user from Lync Server 2010 to Lync Server 2013, the following information moves with the user’s account:</span></span>

  - <span data-ttu-id="3210e-140">已由用户安排的会议。</span><span class="sxs-lookup"><span data-stu-id="3210e-140">Meetings already scheduled by the user.</span></span> <span data-ttu-id="3210e-141">这包括会议目录和会议数据。</span><span class="sxs-lookup"><span data-stu-id="3210e-141">This includes conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="3210e-142">用户的个人识别码 (引脚) 。</span><span class="sxs-lookup"><span data-stu-id="3210e-142">The user’s personal identification number (PIN).</span></span> <span data-ttu-id="3210e-143">用户的当前 PIN 将继续工作，直到过期或用户请求新的 PIN。</span><span class="sxs-lookup"><span data-stu-id="3210e-143">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="3210e-144">但是，以下用户帐户信息不会移动到新服务器：</span><span class="sxs-lookup"><span data-stu-id="3210e-144">However, the following user account information does not move to the new server:</span></span>

  - <span data-ttu-id="3210e-145">会议内容，例如 PowerPoint 演示文稿、白板内容和投票数据</span><span class="sxs-lookup"><span data-stu-id="3210e-145">Meeting content, for example PowerPoint presentations, whiteboard content, and poll data</span></span>

<span data-ttu-id="3210e-146">若要移动已在会议中共享的内容，请使用 Move-CsUser cmdlet 的 MoveMeetingContent 参数。</span><span class="sxs-lookup"><span data-stu-id="3210e-146">To move the content that has been shared in meetings, use the MoveMeetingContent parameter of the Move-CsUser cmdlet.</span></span> <span data-ttu-id="3210e-147">有关使用此 cmdlet 的详细信息，请参阅 Lync Server 2013 cmdlet 文档中的 [move-csuser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) 。</span><span class="sxs-lookup"><span data-stu-id="3210e-147">For details about using this cmdlet, see [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) in the Lync Server 2013 cmdlets documentation.</span></span>

</div>

<div>

## <a name="migrating-meetings-from-office-communications-server-2007-r2"></a><span data-ttu-id="3210e-148">从 Office 通信服务器 2007 R2 迁移会议</span><span class="sxs-lookup"><span data-stu-id="3210e-148">Migrating Meetings from Office Communications Server 2007 R2</span></span>

<span data-ttu-id="3210e-149">Office 通信服务器 2007 R2 会议是电话会议 (conf://URL 前缀) 或 web 会议 (meet://URL 前缀) 。</span><span class="sxs-lookup"><span data-stu-id="3210e-149">Office Communications Server 2007 R2 meetings are either conference calls (conf:// URL prefix) or web conferences (meet:// URL prefix).</span></span> <span data-ttu-id="3210e-150">Lync Server 2013 不支持这些以前的 conf://和 meet://会议，它们不会与用户帐户一起迁移。</span><span class="sxs-lookup"><span data-stu-id="3210e-150">Lync Server 2013 does not support these earlier conf:// and meet:// conferences, and they are not migrated along with the user account.</span></span> <span data-ttu-id="3210e-151">迁移后，应指示用户更新已安排的任何联机会议的链接。</span><span class="sxs-lookup"><span data-stu-id="3210e-151">After migration, you should instruct users to update the links for any online meetings they have scheduled.</span></span> <span data-ttu-id="3210e-152">他们可以在安装 Lync 2013 客户端后执行此操作，方法是打开一个计划会议邀请（更新会议 URL），并向参与者重新发送邀请。</span><span class="sxs-lookup"><span data-stu-id="3210e-152">They can do this after installing the Lync 2013 client by opening a scheduled meeting invitation—which updates the meeting URL—and resending the invitation to participants.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-lync-server-2010-migration"></a><span data-ttu-id="3210e-153">Lync Server 2010 迁移期间的用户体验</span><span class="sxs-lookup"><span data-stu-id="3210e-153">User Experience during Lync Server 2010 Migration</span></span>

<span data-ttu-id="3210e-154">本部分提供从 Lync 2010 迁移时用户会议体验的摘要。</span><span class="sxs-lookup"><span data-stu-id="3210e-154">This section provides a summary of users’ conferencing experience when migrating from Lync 2010.</span></span> <span data-ttu-id="3210e-155">有关 Lync Server 2013 客户端可如何共存以及如何与以前的客户端和服务器版本交互的更多详细信息，请参阅 [Lync 2013 中的客户端互操作性](lync-server-2013-client-interoperability-in-lync-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="3210e-155">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="joining-lync-server-2010-meetings-with-a-lync-2013-client"></a><span data-ttu-id="3210e-156">使用 Lync 2013 客户端加入 Lync Server 2010 会议</span><span class="sxs-lookup"><span data-stu-id="3210e-156">Joining Lync Server 2010 Meetings with a Lync 2013 Client</span></span>

<span data-ttu-id="3210e-157">从 Lync Server 2010 迁移期间，在用户使用 Lync 2013 客户端加入 Lync Server 2010 会议时可能会有一段共存。</span><span class="sxs-lookup"><span data-stu-id="3210e-157">During migration from Lync Server 2010, there may be a period of coexistence when users join Lync Server 2010 meetings with a Lync 2013 client.</span></span> <span data-ttu-id="3210e-158">这些用户有权访问 Lync 2013 客户端功能，但出现以下异常：</span><span class="sxs-lookup"><span data-stu-id="3210e-158">These users have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="3210e-159">在 **参与者** 管理选项（可通过指向会议窗口中的 "人员" 图标访问）中，" **无会议即时消息** " 选项不起作用。</span><span class="sxs-lookup"><span data-stu-id="3210e-159">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="3210e-160">库视图在视频会议中不起作用。</span><span class="sxs-lookup"><span data-stu-id="3210e-160">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="3210e-161">用户仅看到活动的扬声器，而不是所有扬声器。</span><span class="sxs-lookup"><span data-stu-id="3210e-161">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="3210e-162">在 " **选择布局** " 选项列表中，" **库视图** " 不可用</span><span class="sxs-lookup"><span data-stu-id="3210e-162">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="3210e-163">参与者列表默认情况下显示在视频会议中。</span><span class="sxs-lookup"><span data-stu-id="3210e-163">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="3210e-164">右键单击参与者列表中的用户时， **锁定视频焦点** 和 **固定到库** 参与者管理选项不可用。</span><span class="sxs-lookup"><span data-stu-id="3210e-164">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-office-communications-server-2007-r2-migration"></a><span data-ttu-id="3210e-165">Office 通信服务器 2007 R2 迁移期间的用户体验</span><span class="sxs-lookup"><span data-stu-id="3210e-165">User Experience during Office Communications Server 2007 R2 Migration</span></span>

<span data-ttu-id="3210e-166">本部分提供了在安装 Lync 2013 之前和之后从 Office 通信服务器 2007 R2 迁移时的用户会议体验的摘要。</span><span class="sxs-lookup"><span data-stu-id="3210e-166">This section provides a summary of users’ conferencing experience when migrating from Office Communications Server 2007 R2, both before and after Lync 2013 is installed.</span></span> <span data-ttu-id="3210e-167">有关 Lync Server 2013 客户端可如何共存以及如何与以前的客户端和服务器版本交互的更多详细信息，请参阅 [Lync 2013 中的客户端互操作性](lync-server-2013-client-interoperability-in-lync-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="3210e-167">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="after-user-account-is-migrated-before-lync-2013-is-installed"></a><span data-ttu-id="3210e-168">在迁移用户帐户之后，安装 Lync 2013 之前</span><span class="sxs-lookup"><span data-stu-id="3210e-168">After User Account is Migrated, Before Lync 2013 Is Installed</span></span>

<span data-ttu-id="3210e-169">将用户迁移到 Lync Server 2013 服务器后，在安装新客户之前，Office Communicator 2007 R2 用户可以继续使用其现有客户端与 Lync Server 2013 的状态和 IM 功能，但不支持会议功能。</span><span class="sxs-lookup"><span data-stu-id="3210e-169">After a user is migrated to the Lync Server 2013 server, but before new clients are installed, Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

</div>

<div>

## <a name="after-user-account-is-migrated-after-lync-2013-is-installed"></a><span data-ttu-id="3210e-170">在迁移用户帐户后，安装 Lync 2013 后</span><span class="sxs-lookup"><span data-stu-id="3210e-170">After User Account is Migrated, After Lync 2013 Is Installed</span></span>

<span data-ttu-id="3210e-171">当已迁移用户安装 Lync 2013 时，也会安装 Lync 2013 的联机会议外接程序。</span><span class="sxs-lookup"><span data-stu-id="3210e-171">When a migrated user installs Lync 2013, the Online Meeting Add-in for Lync 2013 is installed too.</span></span> <span data-ttu-id="3210e-172">这具有以下效果：</span><span class="sxs-lookup"><span data-stu-id="3210e-172">This has the following effects:</span></span>

  - <span data-ttu-id="3210e-173">所有后续计划的会议都使用新的会议格式，该格式使用 https://地址，而不是旧版 meet://Live 会议地址。</span><span class="sxs-lookup"><span data-stu-id="3210e-173">All subsequently scheduled meetings use the new meeting format, which uses an https:// address instead of the legacy meet:// Live Meeting address.</span></span>

  - <span data-ttu-id="3210e-174">在 Lync 2013 的 IT 托管部署中，管理员可以选择卸载 Microsoft Office Outlook 的会议加载项，该加载项用于安排 Live Meeting 服务器和基于服务的会议。</span><span class="sxs-lookup"><span data-stu-id="3210e-174">In an IT-managed deployment of Lync 2013, the administrator has the option of uninstalling the Conferencing Add-in for Microsoft Office Outlook, which is used to schedule Live Meeting server and service-based meetings.</span></span> <span data-ttu-id="3210e-175">但是，你可能需要继续安排 Live Meeting 服务会议的用户。</span><span class="sxs-lookup"><span data-stu-id="3210e-175">However, you may have users who need to continue to schedule Live Meeting service meetings.</span></span> <span data-ttu-id="3210e-176">在这种情况下，你可以允许两个外接程序共存。</span><span class="sxs-lookup"><span data-stu-id="3210e-176">In this case, you can allow both add-ins to coexist.</span></span>

</div>

<div>

## <a name="meetings-with-federated-organizations-that-use-previous-clients"></a><span data-ttu-id="3210e-177">使用以前客户端的联盟组织的会议</span><span class="sxs-lookup"><span data-stu-id="3210e-177">Meetings with Federated Organizations that Use Previous Clients</span></span>

<span data-ttu-id="3210e-178">在组织中使用 Microsoft Office Communicator 2007 的联盟组织中的用户无法加入您组织中的 Lync Server 2013 会议（如果该会议由组织者锁定）。</span><span class="sxs-lookup"><span data-stu-id="3210e-178">Users in federated organizations who are using Microsoft Office Communicator 2007 cannot join Lync Server 2013 meetings in your organization if those meetings are locked by the organizer.</span></span> <span data-ttu-id="3210e-179">您必须在 Lync Server 2013 中重新安排这些会议，以便在联盟参与者使用新的 https://会议 URL 加入会议时，他们可以使用 Lync Web App。</span><span class="sxs-lookup"><span data-stu-id="3210e-179">You have to reschedule these meetings in Lync Server 2013 so when federated participants join the meeting by using the new https:// meeting URL, they can use Lync Web App.</span></span>

<span data-ttu-id="3210e-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3210e-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

