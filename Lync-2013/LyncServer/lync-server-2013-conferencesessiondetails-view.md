---
title: Lync Server 2013： ConferenceSessionDetails 视图
description: Lync Server 2013： ConferenceSessionDetails 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails view
ms:assetid: 5858c84d-baed-421d-ad1d-3726e150e256
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688066(v=OCS.15)
ms:contentKeyID: 49733660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1c62f020413efecdbc0f909618256ccc7308d4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434394"
---
# <a name="conferencesessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="9c5b5-103">Lync Server 2013 中的 ConferenceSessionDetails 视图</span><span class="sxs-lookup"><span data-stu-id="9c5b5-103">ConferenceSessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c5b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c5b5-104">

<span> </span></span></span>

<span data-ttu-id="9c5b5-105">_**主题上次修改时间：** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="9c5b5-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="9c5b5-106">ConferenceSessionDetails 视图存储有关多方会话的信息。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-106">The ConferenceSessionDetails view stores information about multiparty sessions.</span></span> <span data-ttu-id="9c5b5-107">每个记录表示一个会议会话，该会话可以是与焦点的会话，也可以是与特定的会议服务器的会话。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-107">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span> <span data-ttu-id="9c5b5-108">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c5b5-109">列</span><span class="sxs-lookup"><span data-stu-id="9c5b5-109">Column</span></span></th>
<th><span data-ttu-id="9c5b5-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="9c5b5-110">Data Type</span></span></th>
<th><span data-ttu-id="9c5b5-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="9c5b5-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-113">datetime</span><span class="sxs-lookup"><span data-stu-id="9c5b5-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-114">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-114">Time of session request.</span></span> <span data-ttu-id="9c5b5-115">与 SessionIdSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-115">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="9c5b5-116">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-118">int</span><span class="sxs-lookup"><span data-stu-id="9c5b5-118">int</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-119">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-119">ID number to identify the session.</span></span> <span data-ttu-id="9c5b5-120">与 SessionIdTime 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-120">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="9c5b5-121">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-122"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-122"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-123">datetime</span><span class="sxs-lookup"><span data-stu-id="9c5b5-123">datetime</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-124">第一次邀请请求的时间。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-124">Time of the first INVITE request.</span></span> <span data-ttu-id="9c5b5-125">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-125">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9c5b5-126">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-126">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-127"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-127"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-128">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-128">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-129">会议的 URI。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-129">URI of the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-130"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-130"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-131">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-131">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-132">会议 URI 的类型。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-132">Type of conference URI.</span></span> <span data-ttu-id="9c5b5-133">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-133">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-134"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-134"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-135">标识符</span><span class="sxs-lookup"><span data-stu-id="9c5b5-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-136">区分定期会议的实例的标识符。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-136">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="9c5b5-137">每个定期会议实例具有相同的 ConferenceURI，但具有不同的 ConfInstance 值。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-137">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-138"><strong>McuConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-138"><strong>McuConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-139">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-140">会议服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-140">URI of the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-141"><strong>McuConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-141"><strong>McuConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-143">会议服务器 URI 的类型。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-143">Type of conferencing server URI.</span></span> <span data-ttu-id="9c5b5-144">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-145"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-145"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-146">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-146">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-147">会话中涉及的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-147">URI of the user involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-148"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-148"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-149">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-149">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-150">属于会话的用户的 URI 的类型。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-150">Type of URI of the user whose was part of the session.</span></span> <span data-ttu-id="9c5b5-151">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-151">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-152"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-152"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-154">属于会话一部分的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-154">Tenant of the user whose was part of the session.</span></span> <span data-ttu-id="9c5b5-155">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-155">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-156"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-156"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-157">标识符</span><span class="sxs-lookup"><span data-stu-id="9c5b5-157">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-158">属于会话的用户的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-158">Unique identifier of the user whose was part of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-159"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-159"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-160">datetime</span><span class="sxs-lookup"><span data-stu-id="9c5b5-160">datetime</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-161">会话的结束时间。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-161">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-162"><strong>ConferenceClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-162"><strong>ConferenceClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-163">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-163">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-164">会议服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-164">Version of conference server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-165"><strong>ConferenceClientType</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-165"><strong>ConferenceClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-166">int</span><span class="sxs-lookup"><span data-stu-id="9c5b5-166">int</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-167">会议服务器的类型。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-167">Type of conference server.</span></span> <span data-ttu-id="9c5b5-168">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-168">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-169"><strong>ConferenceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-169"><strong>ConferenceCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-170">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-170">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-171">"会议服务器" 类别。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-171">Conference server category.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-172"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-172"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-173">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-173">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-174">参与会话的用户使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-174">Version of client used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-175"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-175"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-176">int</span><span class="sxs-lookup"><span data-stu-id="9c5b5-176">int</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-177">参与会话的用户所使用的客户端。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-177">Client used by the user who participated in the session.</span></span> <span data-ttu-id="9c5b5-178">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-178">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-179"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-179"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-180">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-180">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-181">参与会话的用户所使用的客户端类别的名称。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-181">Name of the category of the client used by the user who was part of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-182"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-182"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-183">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-183">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-184">已代表其启动会话的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-184">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-185"><strong>OnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-185"><strong>OnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-186">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-186">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-187">已代表其启动会话的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-187">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="9c5b5-188">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-188">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-189"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-189"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-190">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-190">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-191">其代表启动会话的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-191">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="9c5b5-192">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-192">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-193"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-193"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-194">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-194">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-195">引用会话的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-195">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-196"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-196"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-197">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-197">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-198">引用会话的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-198">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="9c5b5-199">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-199">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-200"><strong>ReferredByUriTenant</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-200"><strong>ReferredByUriTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-201">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-201">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-202">引用会话的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-202">Tenant of the user who referred the session.</span></span> <span data-ttu-id="9c5b5-203">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-203">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-204"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-204"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-205">varstring (775) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-205">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-206">SIP 对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-206">SIP dialog ID.</span></span> <span data-ttu-id="9c5b5-207">格式为</span><span class="sxs-lookup"><span data-stu-id="9c5b5-207">The format is</span></span></p>
<p><span data-ttu-id="9c5b5-208">:d ialog; from-标记; to-标记</span><span class="sxs-lookup"><span data-stu-id="9c5b5-208">:dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-209"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-209"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-210">datetime</span><span class="sxs-lookup"><span data-stu-id="9c5b5-210">datetime</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-211">标识由当前会话替换的对话框的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-211">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="9c5b5-212">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-212">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-213"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-213"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-214">int</span><span class="sxs-lookup"><span data-stu-id="9c5b5-214">int</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-215">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-215">ID number to identify the session.</span></span> <span data-ttu-id="9c5b5-216">与 ReplaceDialogIdTime 结合使用以唯一标识此会话替换的会话。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-216">Used in conjunction with ReplaceDialogIdTime to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="9c5b5-217">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-217">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-218"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-218"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-219">varchar (775) </span><span class="sxs-lookup"><span data-stu-id="9c5b5-219">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-220">会话将替换的 SIP 对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-220">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="9c5b5-221">的格式为：</span><span class="sxs-lookup"><span data-stu-id="9c5b5-221">The format of the is:</span></span></p>
<p><span data-ttu-id="9c5b5-222">对话框; 从-标签; 到-标记</span><span class="sxs-lookup"><span data-stu-id="9c5b5-222">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-223"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-223"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-224">bit</span><span class="sxs-lookup"><span data-stu-id="9c5b5-224">bit</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-225">指示会话是否由会议服务器启动。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-225">Indicates whether the session was started by the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-226"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-226"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-227">bit</span><span class="sxs-lookup"><span data-stu-id="9c5b5-227">bit</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-228">指示会话是否已由会议服务器结束。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-228">Indicates whether the session was ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-229"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-229"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-230">bit</span><span class="sxs-lookup"><span data-stu-id="9c5b5-230">bit</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-231">指示用户是否从内部网络登录。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-231">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-233">datetime</span><span class="sxs-lookup"><span data-stu-id="9c5b5-233">datetime</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-234">对第一个邀请消息的答复时间。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-234">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="9c5b5-235">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9c5b5-236">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-237"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-237"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-238">int</span><span class="sxs-lookup"><span data-stu-id="9c5b5-238">int</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-239">会议邀请的 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-239">SIP response code to the session invitation.</span></span> <span data-ttu-id="9c5b5-240">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9c5b5-241">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-242"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-242"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-243">int</span><span class="sxs-lookup"><span data-stu-id="9c5b5-243">int</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-244">从会话 SIP 标题捕获的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-244">Diagnostic ID captured from session SIP headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-245"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-245"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-246">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-246">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-247">会话的内容类型。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-247">Content type for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-248"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-248"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-249">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-249">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-250">捕获会话的数据的前端服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-250">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-251"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-251"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-252">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-252">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-253">捕获会话的数据的池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-253">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-254"><strong>MediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-254"><strong>MediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-255">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-255">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-256">参与会话的用户使用的中介服务器。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-256">Mediation Server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-257"><strong>网关</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-257"><strong>Gateway</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-258">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-258">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-259">参与会话的用户使用的网关。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-259">Gateway used by the user who participated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-260"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-260"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-261">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9c5b5-261">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-262">参与会话的用户所使用的边缘服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-262">FQDN of the Edge server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c5b5-263"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-263"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-264">smallint</span><span class="sxs-lookup"><span data-stu-id="9c5b5-264">smallint</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-265">指示参与会话的用户的属性。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-265">Indicates the attributes of the user who participated in the session.</span></span> <span data-ttu-id="9c5b5-266">允许以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="9c5b5-266">The following attribute definitions allowed:</span></span></p>
<p><span data-ttu-id="9c5b5-267">0x01-与桌面电话集成</span><span class="sxs-lookup"><span data-stu-id="9c5b5-267">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c5b5-268"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="9c5b5-268"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="9c5b5-269">smallint</span><span class="sxs-lookup"><span data-stu-id="9c5b5-269">smallint</span></span></p></td>
<td><p><span data-ttu-id="9c5b5-270">指示通话属性。</span><span class="sxs-lookup"><span data-stu-id="9c5b5-270">Indicates the call attributes.</span></span> <span data-ttu-id="9c5b5-271">允许以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="9c5b5-271">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="9c5b5-272">0x01-重试 Session0</span><span class="sxs-lookup"><span data-stu-id="9c5b5-272">0x01 - Retried Session0</span></span></p>
<p><span data-ttu-id="9c5b5-273">x02-代表响应组的代理发出的呼叫</span><span class="sxs-lookup"><span data-stu-id="9c5b5-273">x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9c5b5-274">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c5b5-274">


</div>

<span> </span>

</div>

</div>

</span></span></div>

