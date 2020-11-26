---
title: Lync Server 2013：Lync 2013 中的客户端互操作性
description: Lync Server 2013： Lync 2013 中的客户端互操作性。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client interoperability in Lync 2013
ms:assetid: 0f126571-91a2-45d5-855c-1e4ddb45fc04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204672(v=OCS.15)
ms:contentKeyID: 48183417
ms.date: 03/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea6e90d9479f03dd6d946787e70a2b3cc078699
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434919"
---
# <a name="client-interoperability-in-lync-2013"></a><span data-ttu-id="4eb35-103">Lync 2013 中的客户端互操作性</span><span class="sxs-lookup"><span data-stu-id="4eb35-103">Client interoperability in Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4eb35-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4eb35-104">

<span> </span></span></span>

<span data-ttu-id="4eb35-105">_**主题上次修改时间：** 2016-03-04_</span><span class="sxs-lookup"><span data-stu-id="4eb35-105">_**Topic Last Modified:** 2016-03-04_</span></span>

<span data-ttu-id="4eb35-106">本主题讨论 Microsoft Lync Server 2013 客户端从早期版本的 Lync Server 和 Office 通信服务器中共存和与客户端交互的能力。</span><span class="sxs-lookup"><span data-stu-id="4eb35-106">This topic discusses the ability of Microsoft Lync Server 2013 clients to coexist and interact with clients from earlier versions of Lync Server and Office Communications Server.</span></span>

<div>

## <a name="server-and-client-compatibility"></a><span data-ttu-id="4eb35-107">服务器和客户端兼容性</span><span class="sxs-lookup"><span data-stu-id="4eb35-107">Server and Client Compatibility</span></span>

<span data-ttu-id="4eb35-108">下表显示了客户端版本和服务器版本受支持的组合。</span><span class="sxs-lookup"><span data-stu-id="4eb35-108">The following table shows the supported combinations of client versions and server versions.</span></span> <span data-ttu-id="4eb35-109">此表指示当客户端尝试连接到指示的服务器时，登录是否受支持。</span><span class="sxs-lookup"><span data-stu-id="4eb35-109">This table indicates whether sign-in is supported when the client attempts to connect to the server indicated.</span></span> <span data-ttu-id="4eb35-110">Lync Server 2013 支持以前的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="4eb35-110">Lync Server 2013 supports the previous client version.</span></span> <span data-ttu-id="4eb35-111">此外，与以前的版本不同，Lync Server 2010 支持新的 Lync 2013 客户端。</span><span class="sxs-lookup"><span data-stu-id="4eb35-111">Also, unlike previous releases, Lync Server 2010 supports the new Lync 2013 clients.</span></span> <span data-ttu-id="4eb35-112">这使得从 Lync Server 2010 升级的组织可以独立于 Lync Server 升级来部署新的客户端。</span><span class="sxs-lookup"><span data-stu-id="4eb35-112">This allows organizations who are upgrading from Lync Server 2010 to roll out new clients independent of Lync Server upgrades.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4eb35-113">客户端</span><span class="sxs-lookup"><span data-stu-id="4eb35-113">Client</span></span></th>
<th><span data-ttu-id="4eb35-114">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4eb35-114">Lync Server 2013</span></span></th>
<th><span data-ttu-id="4eb35-115">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="4eb35-115">Lync Server 2010</span></span></th>
<th><span data-ttu-id="4eb35-116">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4eb35-116">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-117">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4eb35-117">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="4eb35-118">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-118">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-119">Supported5</span><span class="sxs-lookup"><span data-stu-id="4eb35-119">Supported5</span></span></p></td>
<td><p><span data-ttu-id="4eb35-120">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-120">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-121">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="4eb35-121">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="4eb35-122">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-122">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-123">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-123">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-124">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-124">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-125">Lync Web App 2013</span><span class="sxs-lookup"><span data-stu-id="4eb35-125">Lync Web App 2013</span></span></p></td>
<td><p><span data-ttu-id="4eb35-126">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-126">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-127">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-127">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-128">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-128">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-129">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4eb35-129">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4eb35-130">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-130">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-131">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-131">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-132">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-132">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-133">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="4eb35-133">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="4eb35-134">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-134">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-135">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-135">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-136">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-136">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-137">Lync 2010 群聊</span><span class="sxs-lookup"><span data-stu-id="4eb35-137">Lync 2010 Group Chat</span></span></p></td>
<td><p><span data-ttu-id="4eb35-138">Supported1</span><span class="sxs-lookup"><span data-stu-id="4eb35-138">Supported1</span></span></p></td>
<td><p><span data-ttu-id="4eb35-139">Supported2</span><span class="sxs-lookup"><span data-stu-id="4eb35-139">Supported2</span></span></p></td>
<td><p><span data-ttu-id="4eb35-140">不适用</span><span class="sxs-lookup"><span data-stu-id="4eb35-140">Not Applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-141">Lync Web App 2010</span><span class="sxs-lookup"><span data-stu-id="4eb35-141">Lync Web App 2010</span></span></p></td>
<td><p><span data-ttu-id="4eb35-142">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-142">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-143">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-143">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-144">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-144">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-145">Lync 2010 Attendee</span><span class="sxs-lookup"><span data-stu-id="4eb35-145">Lync 2010 Attendee</span></span></p></td>
<td><p><span data-ttu-id="4eb35-146">不 Supported3</span><span class="sxs-lookup"><span data-stu-id="4eb35-146">Not Supported3</span></span></p></td>
<td><p><span data-ttu-id="4eb35-147">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-147">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-148">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-148">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-149">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4eb35-149">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="4eb35-150">Interoperable4</span><span class="sxs-lookup"><span data-stu-id="4eb35-150">Interoperable4</span></span></p></td>
<td><p><span data-ttu-id="4eb35-151">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-151">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-152">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-152">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-153">Microsoft Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="4eb35-153">Microsoft Office Communications Server 2007 R2 Attendant</span></span></p></td>
<td><p><span data-ttu-id="4eb35-154">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-154">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-155">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-155">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-156">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-156">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-157">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="4eb35-157">Office Communicator 2007</span></span></p></td>
<td><p><span data-ttu-id="4eb35-158">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-158">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-159">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-159">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-160">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-160">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-161">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="4eb35-161">Office Live Meeting 2007</span></span></p></td>
<td><p><span data-ttu-id="4eb35-162">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-162">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-163">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-163">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-164">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-164">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-165">Lync Windows 应用商店应用</span><span class="sxs-lookup"><span data-stu-id="4eb35-165">Lync Windows Store app</span></span></p></td>
<td><p><span data-ttu-id="4eb35-166">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-166">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-167">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-167">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-168">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-168">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4eb35-169">1For 详细信息，请参阅 [从 Lync server 2010 迁移、群组聊天或 Office 通信服务器 2007 R2 群组聊天到 Lync Server 2013、持久聊天服务器](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)。</span><span class="sxs-lookup"><span data-stu-id="4eb35-169">1For details, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="4eb35-170">2In Microsoft Lync Server 2010，群组聊天功能可通过群组聊天服务器使用，这是 Lync Server 2010 的第三方受信任的应用程序。</span><span class="sxs-lookup"><span data-stu-id="4eb35-170">2In Microsoft Lync Server 2010, group chat functionality was available with Group Chat Server, a third-party trusted application for Lync Server 2010.</span></span> <span data-ttu-id="4eb35-171">Lync 2013 客户端与 Lync Server 2010、群组聊天不兼容。</span><span class="sxs-lookup"><span data-stu-id="4eb35-171">Lync 2013 clients are not compatible with Lync Server 2010, Group Chat.</span></span>

<span data-ttu-id="4eb35-172">3Lync Web App 2013 现在提供了一个完整的会议体验，包括计算机音频和视频，并被视为 Lync 2010 与会者的替换。</span><span class="sxs-lookup"><span data-stu-id="4eb35-172">3Lync Web App 2013 now provides a full in-meeting experience, including computer audio and video, and is considered the replacement for Lync 2010 Attendee.</span></span> <span data-ttu-id="4eb35-173">仅当你使用不受支持的浏览器 (Internet Explorer 6 或 Internet Explorer 7) 和 Windows XP 时，lync 2010 与会者才会连接到 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="4eb35-173">Lync 2010 Attendee will connect to Lync Server 2013 only when you are using an unsupported browser (Internet Explorer 6 or Internet Explorer 7) and Windows XP.</span></span>

<span data-ttu-id="4eb35-174">Office Communicator 2007 R2 中的4The 状态和 IM 功能与 Lync Server 2013 兼容，但会议功能不兼容。</span><span class="sxs-lookup"><span data-stu-id="4eb35-174">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="4eb35-175">从 Office 通信服务器 2007 R2 迁移期间，Office Communicator 2007 R2 适用于状态和 IM 互操作性，但用户应使用 Lync Web App 2013 加入 Lync Server 2013 会议。</span><span class="sxs-lookup"><span data-stu-id="4eb35-175">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

<span data-ttu-id="4eb35-176">5有关限制，请参阅本主题后面部分的 "Lync Server 2010 会议中的 Lync 2013 客户端的会议功能支持"。</span><span class="sxs-lookup"><span data-stu-id="4eb35-176">5 For limitations, see "Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings" later in this topic.</span></span>

</div>

<div>

## <a name="interoperability-among-clients"></a><span data-ttu-id="4eb35-177">客户端之间的互操作性</span><span class="sxs-lookup"><span data-stu-id="4eb35-177">Interoperability among Clients</span></span>

<span data-ttu-id="4eb35-178">通过 Lync Server 2013 版本，各种客户端版本可以在对等和会议方案中无缝交互。</span><span class="sxs-lookup"><span data-stu-id="4eb35-178">With the Lync Server 2013 release, various client versions can interact seamlessly in both peer-to-peer and conferencing scenarios.</span></span> <span data-ttu-id="4eb35-179">本节讨论用户与其他使用不同版本的客户端和服务器的用户进行交互时的功能可用性。</span><span class="sxs-lookup"><span data-stu-id="4eb35-179">This section discusses feature availability when users interact with other users who are using different versions of clients and servers.</span></span>

<div>

## <a name="peer-to-peer-feature-support"></a><span data-ttu-id="4eb35-180">对等功能支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-180">Peer-to-Peer Feature Support</span></span>

<span data-ttu-id="4eb35-181">对于托管在不同版本的服务器上的用户以及使用不同客户端版本的用户，支持对等功能。</span><span class="sxs-lookup"><span data-stu-id="4eb35-181">Peer-to-peer features are supported for users who are homed on different versions of the server and who are using different client versions.</span></span> <span data-ttu-id="4eb35-182">最终用户体验和可用功能与用户的客户端的功能和用户登录到的服务器版本一致。</span><span class="sxs-lookup"><span data-stu-id="4eb35-182">The end-user experience and available features are consistent with the capabilities of the user’s client and the version of the server the user is signed in to.</span></span> <span data-ttu-id="4eb35-183">换言之：</span><span class="sxs-lookup"><span data-stu-id="4eb35-183">In other words:</span></span>

  - <span data-ttu-id="4eb35-184">如果用户使用较早的客户端登录到 Lync Server 2013，则用户将拥有自己所用的体验。</span><span class="sxs-lookup"><span data-stu-id="4eb35-184">If a user is signed in to Lync Server 2013 with an older client, the user will have the same experience he or she is used to.</span></span> <span data-ttu-id="4eb35-185">Lync Server 2013 中引入的任何新功能在用户的客户端升级之前都不可用。</span><span class="sxs-lookup"><span data-stu-id="4eb35-185">None of the new features introduced in Lync Server 2013 will be available until the user’s client is upgraded.</span></span> <span data-ttu-id="4eb35-186">示例包括视频库视图、HD 视频、更新的 PowerPoint 共享，以及用于在会议进入时将所有与会者音频和视频设为静音的选项。</span><span class="sxs-lookup"><span data-stu-id="4eb35-186">Examples include video gallery view, HD video, updated PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="4eb35-187">[Lync server 2013 中的新会议功能](lync-server-2013-new-conferencing-features.md)概述了新功能，以及[lync server 2013 中客户端的新增](lync-server-2013-what-s-new-for-clients.md)功能。</span><span class="sxs-lookup"><span data-stu-id="4eb35-187">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

  - <span data-ttu-id="4eb35-188">如果用户使用 Lync 2013 客户端登录到 Lync Server 2010，则 Lync Server 2010 不支持的任何新功能将在用户移到 Lync Server 2013 后才可用。</span><span class="sxs-lookup"><span data-stu-id="4eb35-188">If a user is signed in to Lync Server 2010 with a Lync 2013 client, any new features not supported by Lync Server 2010 will be unavailable until the user is moved to Lync Server 2013.</span></span>

<span data-ttu-id="4eb35-189">下表比较了客户登录到 Lync Server 2013 或 Lync Server 2010 的对等会话中的功能可用性。</span><span class="sxs-lookup"><span data-stu-id="4eb35-189">The following table compares feature availability in peer-to-peer sessions where the client is signed in to either Lync Server 2013 or Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4eb35-190">Lync Web App 和 Lync 2010 与会者是仅限会议客户端，不包括在此表中。</span><span class="sxs-lookup"><span data-stu-id="4eb35-190">Lync Web App and Lync 2010 Attendee are meeting-only clients and aren’t included in this table.</span></span>



</div>


<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4eb35-191">客户端</span><span class="sxs-lookup"><span data-stu-id="4eb35-191">Client</span></span></th>
<th><span data-ttu-id="4eb35-192">即时消息</span><span class="sxs-lookup"><span data-stu-id="4eb35-192">Instant Messaging</span></span></th>
<th><span data-ttu-id="4eb35-193">状态</span><span class="sxs-lookup"><span data-stu-id="4eb35-193">Presence</span></span></th>
<th><span data-ttu-id="4eb35-194">语音</span><span class="sxs-lookup"><span data-stu-id="4eb35-194">Voice</span></span></th>
<th><span data-ttu-id="4eb35-195">视频</span><span class="sxs-lookup"><span data-stu-id="4eb35-195">Video</span></span></th>
<th><span data-ttu-id="4eb35-196">应用程序共享</span><span class="sxs-lookup"><span data-stu-id="4eb35-196">Application Sharing</span></span></th>
<th><span data-ttu-id="4eb35-197">文件传输</span><span class="sxs-lookup"><span data-stu-id="4eb35-197">File Transfer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-198">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4eb35-198">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="4eb35-199">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-199">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-200">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-201">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-201">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-202">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-202">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-203">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-203">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-204">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-205">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="4eb35-205">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="4eb35-206">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-207">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-207">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-208">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-209">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-210">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-211">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-211">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-212">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4eb35-212">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4eb35-213">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-213">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-214">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-215">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-215">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-216">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-217">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-218">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-219">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="4eb35-219">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="4eb35-220">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-220">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-221">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-222">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-222">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-223">Lync 2010 Mobile</span><span class="sxs-lookup"><span data-stu-id="4eb35-223">Lync 2010 Mobile</span></span></p></td>
<td><p><span data-ttu-id="4eb35-224">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-225">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-225">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-226">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="4eb35-226">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="4eb35-227">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-228">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-229">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-229">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-230">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4eb35-230">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="4eb35-231">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-231">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-232">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-232">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-233">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-233">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-234">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-235">是1</span><span class="sxs-lookup"><span data-stu-id="4eb35-235">Yes1</span></span></p></td>
<td><p><span data-ttu-id="4eb35-236">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-236">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-237">公共 IM (AOL、Yahoo！ ) </span><span class="sxs-lookup"><span data-stu-id="4eb35-237">Public IM (AOL, Yahoo!)</span></span></p></td>
<td><p><span data-ttu-id="4eb35-238">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-239">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-239">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-240">公共 IM (MSN、Windows Live Messenger) </span><span class="sxs-lookup"><span data-stu-id="4eb35-240">Public IM (MSN, Windows Live Messenger)</span></span></p></td>
<td><p><span data-ttu-id="4eb35-241">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-241">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-242">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-243">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-243">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-244">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-244">Yes</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="4eb35-245">从2012年9月1日起，，Microsoft Lync 公共 IM 连接用户订阅许可证 (PIC USL) 不再可供购买新的或续订协议。</span><span class="sxs-lookup"><span data-stu-id="4eb35-245">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="4eb35-246">具有活动许可证的客户将能够继续与 Yahoo！进行联盟</span><span class="sxs-lookup"><span data-stu-id="4eb35-246">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="4eb35-247">Messenger，直到服务关闭日期。</span><span class="sxs-lookup"><span data-stu-id="4eb35-247">Messenger until the service shutdown date.</span></span> <span data-ttu-id="4eb35-248">AOL 和 Yahoo！的有效期结束日期为2014年6月</span><span class="sxs-lookup"><span data-stu-id="4eb35-248">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="4eb35-249">已宣布。</span><span class="sxs-lookup"><span data-stu-id="4eb35-249">has been announced.</span></span> <span data-ttu-id="4eb35-250">有关详细信息，请参阅 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 中的公共即时消息连接支持</A>。。</span><span class="sxs-lookup"><span data-stu-id="4eb35-250">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>..</span></span></P>
> <LI>
> <P><span data-ttu-id="4eb35-251">PIC USL 是 Lync Server 或 Office 通信服务器与 Yahoo！联合所需的每用户、每月订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="4eb35-251">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="4eb35-252">Messenger.</span><span class="sxs-lookup"><span data-stu-id="4eb35-252">Messenger.</span></span> <span data-ttu-id="4eb35-253">Microsoft 提供此服务的能力已由 Yahoo！的支持（将不会续订的底层协议）提供。</span><span class="sxs-lookup"><span data-stu-id="4eb35-253">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="4eb35-254">Lync 比以往更多，是一种强大的工具，用于跨组织和全球各地的人员进行连接。</span><span class="sxs-lookup"><span data-stu-id="4eb35-254">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="4eb35-255">与 Windows Live Messenger 的联盟不需要除 Lync 标准 CAL 之外的其他用户/设备许可证。</span><span class="sxs-lookup"><span data-stu-id="4eb35-255">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="4eb35-256">Skype 联盟将添加到此列表，使 Lync 用户可以通过 IM 和语音与成百上千人联系。</span><span class="sxs-lookup"><span data-stu-id="4eb35-256">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="4eb35-257">1在 Office Communicator 2007 R2 中，只有 "桌面共享" (，而不是 "程序共享") 可用。</span><span class="sxs-lookup"><span data-stu-id="4eb35-257">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4eb35-258">当已强制使用 Skype for Business 2015 客户端用户界面时，无法从较新的客户端启动 Office Communicator 2007 R2 和 Skype for business 2015 之间的桌面共享。</span><span class="sxs-lookup"><span data-stu-id="4eb35-258">Desktop sharing between Office Communicator 2007 R2 and Skype for Business 2015 cannot be initiated from the newer client when the Skype for Business 2015 client user interface is enforced.</span></span>



</div>

</div>

<div>

## <a name="conferencing-feature-support-for-lync-2013-clients-in-lync-server-2010-meetings"></a><span data-ttu-id="4eb35-259">Lync Server 2010 会议中 Lync 2013 客户端的会议功能支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-259">Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings</span></span>

<span data-ttu-id="4eb35-260">当用户使用 Lync 2013 客户端加入 Lync Server 2010 会议时，他们可以访问 Lync 2013 客户端功能，但有以下例外：</span><span class="sxs-lookup"><span data-stu-id="4eb35-260">When users join Lync Server 2010 meetings with a Lync 2013 client, they have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="4eb35-261">在 **参与者** 管理选项（可通过指向会议窗口中的 "人员" 图标访问）中，" **无会议即时消息** " 选项不起作用。</span><span class="sxs-lookup"><span data-stu-id="4eb35-261">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="4eb35-262">库视图在视频会议中不起作用。</span><span class="sxs-lookup"><span data-stu-id="4eb35-262">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="4eb35-263">用户仅看到活动的扬声器，而不是所有扬声器。</span><span class="sxs-lookup"><span data-stu-id="4eb35-263">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="4eb35-264">在 " **选择布局** " 选项列表中，" **库视图** " 不可用</span><span class="sxs-lookup"><span data-stu-id="4eb35-264">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="4eb35-265">参与者列表默认情况下显示在视频会议中。</span><span class="sxs-lookup"><span data-stu-id="4eb35-265">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="4eb35-266">右键单击参与者列表中的用户时， **锁定视频焦点** 和 **固定到库** 参与者管理选项不可用。</span><span class="sxs-lookup"><span data-stu-id="4eb35-266">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

<div>

## <a name="conferencing-feature-support-in-lync-server-2013-meetings"></a><span data-ttu-id="4eb35-267">Lync Server 2013 会议中的会议功能支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-267">Conferencing Feature Support in Lync Server 2013 Meetings</span></span>

<span data-ttu-id="4eb35-268">Lync Server 2013 提供新的会议功能，这些功能将在帐户移动到 Lync Server 2013 并使用 Lync 2013 客户端登录后向用户提供。</span><span class="sxs-lookup"><span data-stu-id="4eb35-268">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="4eb35-269">示例包括视频库视图、HD 视频、PowerPoint 共享，以及用于在会议进入时将所有与会者音频和视频设为静音的选项。</span><span class="sxs-lookup"><span data-stu-id="4eb35-269">Examples include video gallery view, HD video, PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="4eb35-270">[Lync server 2013 中的新会议功能](lync-server-2013-new-conferencing-features.md)概述了新功能，以及[lync server 2013 中客户端的新增](lync-server-2013-what-s-new-for-clients.md)功能。</span><span class="sxs-lookup"><span data-stu-id="4eb35-270">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="4eb35-271">在 Lync Server 2013 会议中，对于托管在不同版本的服务器以及使用不同客户端和客户端版本的用户，某些会议功能是受支持的。</span><span class="sxs-lookup"><span data-stu-id="4eb35-271">In Lync Server 2013 meetings, certain conferencing features are supported for users who are homed on different versions of the server and who are using different clients and client versions.</span></span> <span data-ttu-id="4eb35-272">当客户端加入 Lync Server 2013 会议时，用户有权访问此表中所示的功能和功能。</span><span class="sxs-lookup"><span data-stu-id="4eb35-272">When clients join a Lync Server 2013 meeting, users have access to the features and capabilities shown in this table.</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4eb35-273">客户端</span><span class="sxs-lookup"><span data-stu-id="4eb35-273">Client</span></span></th>
<th><span data-ttu-id="4eb35-274">对等 IM</span><span class="sxs-lookup"><span data-stu-id="4eb35-274">Peer-to-peer IM</span></span></th>
<th><span data-ttu-id="4eb35-275">语音</span><span class="sxs-lookup"><span data-stu-id="4eb35-275">Voice</span></span></th>
<th><span data-ttu-id="4eb35-276">视频</span><span class="sxs-lookup"><span data-stu-id="4eb35-276">Video</span></span></th>
<th><span data-ttu-id="4eb35-277">应用程序共享</span><span class="sxs-lookup"><span data-stu-id="4eb35-277">Application Sharing</span></span></th>
<th><span data-ttu-id="4eb35-278">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="4eb35-278">PowerPoint</span></span></th>
<th><span data-ttu-id="4eb35-279">文件传输</span><span class="sxs-lookup"><span data-stu-id="4eb35-279">File Transfer</span></span></th>
<th><span data-ttu-id="4eb35-280">Whiteboard</span><span class="sxs-lookup"><span data-stu-id="4eb35-280">Whiteboard</span></span></th>
<th><span data-ttu-id="4eb35-281">轮询</span><span class="sxs-lookup"><span data-stu-id="4eb35-281">Polling</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-282">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4eb35-282">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="4eb35-283">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-283">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-284">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-285">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-285">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-286">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-286">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-287">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-287">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-288">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-289">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-289">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-290">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-290">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-291">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="4eb35-291">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="4eb35-292">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-293">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-293">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-294">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-294">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-295">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-295">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-296">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-297">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-297">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-298">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-298">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-299">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-299">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-300">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="4eb35-300">Lync Web App</span></span></p></td>
<td><p><span data-ttu-id="4eb35-301">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-301">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-302">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-302">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-303">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-303">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-304">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-305">是2</span><span class="sxs-lookup"><span data-stu-id="4eb35-305">Yes2</span></span></p></td>
<td><p><span data-ttu-id="4eb35-306">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-306">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-307">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-307">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-308">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-308">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-309">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4eb35-309">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4eb35-310">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-311">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-311">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-312">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-312">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-313">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-314">是3</span><span class="sxs-lookup"><span data-stu-id="4eb35-314">Yes3</span></span></p></td>
<td><p><span data-ttu-id="4eb35-315">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-315">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-316">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-316">Yes</span></span></p></td>
<td><p><span data-ttu-id="4eb35-317">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-317">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-318">Office Communicator 2007 R2 4</span><span class="sxs-lookup"><span data-stu-id="4eb35-318">Office Communicator 2007 R2 4</span></span></p></td>
<td><p><span data-ttu-id="4eb35-319">是</span><span class="sxs-lookup"><span data-stu-id="4eb35-319">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4eb35-320">1在 Office Communicator 2007 R2 中，只有 "桌面共享" (，而不是 "程序共享") 可用。</span><span class="sxs-lookup"><span data-stu-id="4eb35-320">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<span data-ttu-id="4eb35-321">2 Lync Server 2013 使用更新的机制来上载 PowerPoint 文件。</span><span class="sxs-lookup"><span data-stu-id="4eb35-321">2 Lync Server 2013 uses an updated mechanism for uploading PowerPoint files.</span></span> <span data-ttu-id="4eb35-322">加入最初在 Lync Server 2010 上计划的会议的 Lync Web App 用户可以查看和导航 PowerPoint 演示文稿，但无法上载 PowerPoint 文件。</span><span class="sxs-lookup"><span data-stu-id="4eb35-322">Lync Web App users who join a meeting that was originally scheduled on Lync Server 2010 can view and navigate PowerPoint presentations, but cannot upload PowerPoint files.</span></span>

<span data-ttu-id="4eb35-323">3如果已在 Lync Server 2013 上安排了会议，并且已由 Lync 2013 客户端上载了 PowerPoint 幻灯片，则 Lync 2010 用户拥有对幻灯片的仅查看访问权限。</span><span class="sxs-lookup"><span data-stu-id="4eb35-323">3 If the meeting was scheduled on Lync Server 2013 and PowerPoint slides were uploaded by a Lync 2013 client, Lync 2010 users have view-only access to the slides.</span></span> <span data-ttu-id="4eb35-324">相反，如果 PowerPoint 2010 用户上传了 PowerPoint 幻灯片，则 Lync Server 2013 用户将能够查看和幻灯片，如果已配置 Office Web Apps 服务器，请访问新功能，例如更高分辨率的显示、动画、幻灯片切换和嵌入的视频。</span><span class="sxs-lookup"><span data-stu-id="4eb35-324">Conversely, if the PowerPoint slides were uploaded by a Lync 2010 user, Lync Server 2013 users will be able to view and slides and, if Office Web Apps Server is configured, access new capabilities such as higher resolution display, animations, slide transitions, and embedded video.</span></span> <span data-ttu-id="4eb35-325">有关详细信息，请参阅 [配置与 Office Web Apps server 和 Lync server 2013 的集成](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="4eb35-325">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="4eb35-326">Office Communicator 2007 R2 中的4The 状态和 IM 功能与 Lync Server 2013 兼容，但会议功能不兼容。</span><span class="sxs-lookup"><span data-stu-id="4eb35-326">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="4eb35-327">从 Office 通信服务器 2007 R2 迁移期间，Office Communicator 2007 R2 适用于状态和 IM 互操作性，但用户应使用 Lync Web App 2013 加入 Lync Server 2013 会议。</span><span class="sxs-lookup"><span data-stu-id="4eb35-327">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

</div>

</div>

<div>

## <a name="scheduling-add-in-support"></a><span data-ttu-id="4eb35-328">计划外接程序支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-328">Scheduling Add-in Support</span></span>

<span data-ttu-id="4eb35-329">针对各种计划外接程序的服务器支持与服务器和客户端版本兼容性一致。</span><span class="sxs-lookup"><span data-stu-id="4eb35-329">Server support for the various scheduling add-ins is consistent with server and client version compatibility.</span></span> <span data-ttu-id="4eb35-330">通常，在 Lync Server 2013 上支持以下计划外接程序。</span><span class="sxs-lookup"><span data-stu-id="4eb35-330">In general, the following scheduling add-ins are supported on Lync Server 2013.</span></span> <span data-ttu-id="4eb35-331">但是，以前版本的外接程序不提供新的 Lync 2013 加载项功能，例如将所有与会者音频和视频设置为 "会议进入时静音" 的选项。</span><span class="sxs-lookup"><span data-stu-id="4eb35-331">However, previous versions of add-ins do not provide new Lync 2013 add-in features, such as the option to mute all attendee audio and video upon meeting entry.</span></span>

  - <span data-ttu-id="4eb35-332">**Lync 2013 的联机会议加载项**   提供与 Lync 2010 的联机会议外接程序相同的功能，并且添加了 "与会者静音" 控件，使会议组织者可以安排与会者音频和视频在默认情况下静音的会议。</span><span class="sxs-lookup"><span data-stu-id="4eb35-332">**Online Meeting Add-in for Lync 2013**   Provides the same features as the Online Meeting Add-in for Lync 2010, with the addition of attendee mute controls, which allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span> <span data-ttu-id="4eb35-333">管理员还可以通过添加自定义徽标、支持 URL、合法免责声明 URL 或自定义页脚文本来自定义组织的会议邀请。</span><span class="sxs-lookup"><span data-stu-id="4eb35-333">Administrators can also customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span>

  - <span data-ttu-id="4eb35-334">**Lync 2010 的联机会议加载项**   提供 Lync 会议的日程安排，并删除安排 Office Live Meeting 会议的功能。</span><span class="sxs-lookup"><span data-stu-id="4eb35-334">**Online Meeting Add-in for Lync 2010**   Provides scheduling for Lync meetings and removes the capability to schedule Office Live Meeting conferences.</span></span>

  - <span data-ttu-id="4eb35-335">**Office Communicator 2007 R2 会议加载项**   提供 Office Live Meeting 会议和 Office Communicator 2007 R2 会议的计划。</span><span class="sxs-lookup"><span data-stu-id="4eb35-335">**Office Communicator 2007 R2 Conferencing Add-in**   Provides scheduling for both Office Live Meeting conferences and Office Communicator 2007 R2 conferences.</span></span> 

<div>


> [!NOTE]  
> <span data-ttu-id="4eb35-336">无法在 Lync Server 2013 上计划 Live Meeting 会议。</span><span class="sxs-lookup"><span data-stu-id="4eb35-336">Live Meeting conferences cannot be scheduled on Lync Server 2013.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4eb35-337">计划客户端</span><span class="sxs-lookup"><span data-stu-id="4eb35-337">Scheduling Client</span></span></th>
<th><span data-ttu-id="4eb35-338">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4eb35-338">Lync Server 2013</span></span></th>
<th><span data-ttu-id="4eb35-339">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="4eb35-339">Lync Server 2010</span></span></th>
<th><span data-ttu-id="4eb35-340">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4eb35-340">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-341">适用于 Lync 2013 的联机会议加载项 (可与 Office 2013、Outlook 2010 和 Outlook 2007) 配合使用</span><span class="sxs-lookup"><span data-stu-id="4eb35-341">Online Meeting Add-in for Lync 2013 (can be used with Office 2013, Outlook 2010, and Outlook 2007)</span></span></p></td>
<td><p><span data-ttu-id="4eb35-342">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-342">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-343">支持 (新外接程序功能不可用) </span><span class="sxs-lookup"><span data-stu-id="4eb35-343">Supported (new add-in features not available)</span></span></p></td>
<td><p><span data-ttu-id="4eb35-344">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-344">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-345">Lync 2013 Web 计划程序</span><span class="sxs-lookup"><span data-stu-id="4eb35-345">Lync 2013 Web Scheduler</span></span></p></td>
<td><p><span data-ttu-id="4eb35-346">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-346">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-347">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-347">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-348">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-348">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb35-349">Lync 2010 联机会议外接程序</span><span class="sxs-lookup"><span data-stu-id="4eb35-349">Online Meeting Add-in for Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4eb35-350">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-350">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-351">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-351">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-352">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-352">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb35-353">Office Communicator 2007 R2 会议加载项</span><span class="sxs-lookup"><span data-stu-id="4eb35-353">Office Communicator 2007 R2 Conferencing Add-in</span></span></p></td>
<td><p><span data-ttu-id="4eb35-354">否</span><span class="sxs-lookup"><span data-stu-id="4eb35-354">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-355">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-355">Supported</span></span></p></td>
<td><p><span data-ttu-id="4eb35-356">支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-356">Supported</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="support-for-joining-meetings"></a><span data-ttu-id="4eb35-357">对加入会议的支持</span><span class="sxs-lookup"><span data-stu-id="4eb35-357">Support for Joining Meetings</span></span>

<span data-ttu-id="4eb35-358">Lync Server 2013 支持的所有客户端都可以加入 Lync 2013 会议。</span><span class="sxs-lookup"><span data-stu-id="4eb35-358">All of the clients that Lync Server 2013 supports are allowed to join Lync 2013 meetings.</span></span> <span data-ttu-id="4eb35-359">由于 Lync web App 是服务器的 Web 组件，因此在使用 Lync Web App 加入 Lync Server 2013 会议的情况下，始终使用最新版本的 Lync Web App。</span><span class="sxs-lookup"><span data-stu-id="4eb35-359">Because Lync Web App is a web component of the server, in cases where Lync Web App is used to join a Lync Server 2013 meeting, the newer version of Lync Web App is always used.</span></span>

<span data-ttu-id="4eb35-360">Lync 2013 客户端可以加入在 Lync 2010 上托管的会议和具有缩小功能的 Office 通信服务器 2007 R2。</span><span class="sxs-lookup"><span data-stu-id="4eb35-360">Lync 2013 clients can join meetings hosted on Lync 2010 and Office Communications Server 2007 R2 with scaled-down functionality.</span></span> <span data-ttu-id="4eb35-361">会议中的功能受托管会议的服务器版本的限制。</span><span class="sxs-lookup"><span data-stu-id="4eb35-361">In-meeting features are limited by the version of the server on which the meeting is hosted.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4eb35-362">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4eb35-362">See Also</span></span>


[<span data-ttu-id="4eb35-363">Lync Server 2013 的 lync Windows 应用商店应用要求</span><span class="sxs-lookup"><span data-stu-id="4eb35-363">Lync Windows Store app requirements for Lync Server 2013</span></span>](lync-server-2013-lync-windows-store-app-requirements.md)  
[<span data-ttu-id="4eb35-364">Lync Server 2013 中新的会议功能</span><span class="sxs-lookup"><span data-stu-id="4eb35-364">New conferencing features in Lync Server 2013</span></span>](lync-server-2013-new-conferencing-features.md)  
[<span data-ttu-id="4eb35-365">Lync Server 2013 中面向客户端的新内容</span><span class="sxs-lookup"><span data-stu-id="4eb35-365">What's new for clients in Lync Server 2013</span></span>](lync-server-2013-what-s-new-for-clients.md)  
  

<span data-ttu-id="4eb35-366"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4eb35-366"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

