---
title: Lync Server 2013： ErrorReport 视图
description: Lync Server 2013： ErrorReport 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport view
ms:assetid: ca873f7e-b18b-4eaf-8db0-5f9d5a9b60a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721887(v=OCS.15)
ms:contentKeyID: 49733821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50fb0a362c71d8dfb5873157e7b1ed3d3eb680ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428522"
---
# <a name="errorreport-view-in-lync-server-2013"></a><span data-ttu-id="13e4f-103">Lync Server 2013 中的 ErrorReport 视图</span><span class="sxs-lookup"><span data-stu-id="13e4f-103">ErrorReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13e4f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13e4f-104">

<span> </span></span></span>

<span data-ttu-id="13e4f-105">_**主题上次修改时间：** 2013-01-22_</span><span class="sxs-lookup"><span data-stu-id="13e4f-105">_**Topic Last Modified:** 2013-01-22_</span></span>

<span data-ttu-id="13e4f-106">ErrorReport 视图存储有关报告的错误的信息。</span><span class="sxs-lookup"><span data-stu-id="13e4f-106">The ErrorReport view stores information about errors reported.</span></span> <span data-ttu-id="13e4f-107">每条记录是一个错误发生。</span><span class="sxs-lookup"><span data-stu-id="13e4f-107">Each record is one error occurrence.</span></span> <span data-ttu-id="13e4f-108">这些错误由前端服务器上运行的 CDR 代理或从客户端发送的 CDR 捕获。</span><span class="sxs-lookup"><span data-stu-id="13e4f-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span> <span data-ttu-id="13e4f-109">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="13e4f-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13e4f-110">列</span><span class="sxs-lookup"><span data-stu-id="13e4f-110">Column</span></span></th>
<th><span data-ttu-id="13e4f-111">数据类型</span><span class="sxs-lookup"><span data-stu-id="13e4f-111">Data Type</span></span></th>
<th><span data-ttu-id="13e4f-112">详细信息</span><span class="sxs-lookup"><span data-stu-id="13e4f-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-114">datetime</span><span class="sxs-lookup"><span data-stu-id="13e4f-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="13e4f-115">出现错误的时间。</span><span class="sxs-lookup"><span data-stu-id="13e4f-115">Time of error occurred.</span></span> <span data-ttu-id="13e4f-116">与 ErrorReportSeq 结合使用以唯一标识错误。</span><span class="sxs-lookup"><span data-stu-id="13e4f-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-118">int</span><span class="sxs-lookup"><span data-stu-id="13e4f-118">int</span></span></p></td>
<td><p><span data-ttu-id="13e4f-119">标识错误的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="13e4f-119">ID number to identify the error.</span></span> <span data-ttu-id="13e4f-120">与 ErrorTime 结合使用以唯一标识错误。</span><span class="sxs-lookup"><span data-stu-id="13e4f-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-121"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-121"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-122">int</span><span class="sxs-lookup"><span data-stu-id="13e4f-122">int</span></span></p></td>
<td><p><span data-ttu-id="13e4f-123">错误报告的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="13e4f-123">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-124"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-124"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-125">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="13e4f-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-126">发出错误的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="13e4f-126">URI of the user who originated the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-127"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-127"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-129">发出错误的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="13e4f-129">Type of URI of the user who originated the error.</span></span> <span data-ttu-id="13e4f-130">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-131"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-131"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-133">发出错误的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="13e4f-133">Tenant of the user who originated the error.</span></span> <span data-ttu-id="13e4f-134">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-135"><strong>ToUri</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-135"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-136">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="13e4f-136">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-137">错误报告目标用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="13e4f-137">URI of the user who was the target of the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-140">错误报告目标用户的 URI 的类型。</span><span class="sxs-lookup"><span data-stu-id="13e4f-140">Type of URI of the user who target of the error report.</span></span> <span data-ttu-id="13e4f-141">有关详细信息，请参阅 UriTypes 表。</span><span class="sxs-lookup"><span data-stu-id="13e4f-141">See the UriTypes Table for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-142"><strong>ToTenant</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-142"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-143">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-143">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-144">错误报告面向的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="13e4f-144">Tenant of the user who target of the error report.</span></span> <span data-ttu-id="13e4f-145">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-146"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-146"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-147">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="13e4f-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-148">错误报告目标的会议的 URI。</span><span class="sxs-lookup"><span data-stu-id="13e4f-148">URI of the conference that was the target of the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-149"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-149"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-151">错误报告目标的会议的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="13e4f-151">URI type of the conference that was the target of the error report.</span></span> <span data-ttu-id="13e4f-152">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-152">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-153"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-153"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-154">datetime</span><span class="sxs-lookup"><span data-stu-id="13e4f-154">datetime</span></span></p></td>
<td><p><span data-ttu-id="13e4f-155">发出错误报告的会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="13e4f-155">Time of session request that originated the error report.</span></span> <span data-ttu-id="13e4f-156">与 SessionIdSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="13e4f-156">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="13e4f-157">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-157">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-158"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-158"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-159">int</span><span class="sxs-lookup"><span data-stu-id="13e4f-159">int</span></span></p></td>
<td><p><span data-ttu-id="13e4f-160">标识发出错误报告的会话请求的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="13e4f-160">ID number to identify the session request that originated the error report.</span></span> <span data-ttu-id="13e4f-161">与 SessionIdTime 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="13e4f-161">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="13e4f-162">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-162">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-163"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-163"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-164">varstring (775) </span><span class="sxs-lookup"><span data-stu-id="13e4f-164">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-165">发出错误的会话的 SIP 对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="13e4f-165">SIP dialog ID of session that originated the error.</span></span> <span data-ttu-id="13e4f-166">格式为：</span><span class="sxs-lookup"><span data-stu-id="13e4f-166">The format is:</span></span></p>
<p><span data-ttu-id="13e4f-167">对话框; 从-标签; 到-标记</span><span class="sxs-lookup"><span data-stu-id="13e4f-167">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="13e4f-168">可以使用以下语法将此数据转换为文本格式：</span><span class="sxs-lookup"><span data-stu-id="13e4f-168">This data can be converted to text format by using this syntax:</span></span></p>
<p><span data-ttu-id="13e4f-169">转换 (转换 (ExternalId 为 varbinary (最大) # A4 作为 varchar (最大) # A7</span><span class="sxs-lookup"><span data-stu-id="13e4f-169">cast(cast(ExternalId as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-170"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-170"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-171">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-171">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-172">发出错误的用户使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="13e4f-172">Version of client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-173"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-173"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-174">int</span><span class="sxs-lookup"><span data-stu-id="13e4f-174">int</span></span></p></td>
<td><p><span data-ttu-id="13e4f-175">发出错误的用户所使用的客户端。</span><span class="sxs-lookup"><span data-stu-id="13e4f-175">Client used by the user who originated the error.</span></span> <span data-ttu-id="13e4f-176">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-176">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-177"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-177"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-178">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="13e4f-178">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-179">发出错误的用户所使用的客户端类别的名称。</span><span class="sxs-lookup"><span data-stu-id="13e4f-179">Name of the category of the client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-180"><strong>来源</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-180"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-182">如果从服务器组件) 发送报表，则产生错误的服务器的名称 (。</span><span class="sxs-lookup"><span data-stu-id="13e4f-182">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-183"><strong>Application</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-183"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-184">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-184">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-185">发出错误的应用程序的名称 (从服务器组件) 发送报表时。</span><span class="sxs-lookup"><span data-stu-id="13e4f-185">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-186"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-186"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-187">int</span><span class="sxs-lookup"><span data-stu-id="13e4f-187">int</span></span></p></td>
<td><p><span data-ttu-id="13e4f-188">SIP 回复代码发送到包含错误报告的 SIP 邮件的会话。</span><span class="sxs-lookup"><span data-stu-id="13e4f-188">SIP response code to the session of the SIP message containing the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-189"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-189"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-190">varchar (max) </span><span class="sxs-lookup"><span data-stu-id="13e4f-190">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-191">失败的请求类型。</span><span class="sxs-lookup"><span data-stu-id="13e4f-191">Type of request that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-192"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-192"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-193">varchar (max) </span><span class="sxs-lookup"><span data-stu-id="13e4f-193">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-194">失败的请求的内容类型。</span><span class="sxs-lookup"><span data-stu-id="13e4f-194">Content type of the request that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-195"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-195"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="13e4f-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-197">会话类型。</span><span class="sxs-lookup"><span data-stu-id="13e4f-197">Type of session.</span></span> <span data-ttu-id="13e4f-198">有关详细信息，请参阅 <a href="lync-server-2013-calltype-table.md">Lync Server 2013 中的 CallType 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-198">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-199"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-199"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-200">标识符</span><span class="sxs-lookup"><span data-stu-id="13e4f-200">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="13e4f-201">关联会议中涉及的不同组件的加入时间信息的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="13e4f-201">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-202"><strong>SetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-202"><strong>SetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-203">int</span><span class="sxs-lookup"><span data-stu-id="13e4f-203">int</span></span></p></td>
<td><p><span data-ttu-id="13e4f-204">特定组件加入会议所需的时间 (以毫秒为单位) 。</span><span class="sxs-lookup"><span data-stu-id="13e4f-204">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-205"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-205"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-206">bit</span><span class="sxs-lookup"><span data-stu-id="13e4f-206">bit</span></span></p></td>
<td><p><span data-ttu-id="13e4f-207">指示错误报告是由前端服务器上运行的 CDR 代理捕获的还是由客户端发送的。</span><span class="sxs-lookup"><span data-stu-id="13e4f-207">Indicates whether the error report was captured by the CDR agent running on the Front End server, or sent by the client.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-208"><strong>旗</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-208"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-209">smallint</span><span class="sxs-lookup"><span data-stu-id="13e4f-209">smallint</span></span></p></td>
<td><p><span data-ttu-id="13e4f-210">保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="13e4f-210">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-211"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-211"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-212">varchar (max) </span><span class="sxs-lookup"><span data-stu-id="13e4f-212">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="13e4f-213">有关错误的其他信息。</span><span class="sxs-lookup"><span data-stu-id="13e4f-213">Additional information about the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13e4f-214"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-214"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-215">nvarchar</span><span class="sxs-lookup"><span data-stu-id="13e4f-215">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="13e4f-216">提交报表的前端服务器的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="13e4f-216">Fully qualified domain name of the Front End server that submitted the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13e4f-217"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="13e4f-217"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="13e4f-218">nvarchar</span><span class="sxs-lookup"><span data-stu-id="13e4f-218">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="13e4f-219">包含提交报表的前端服务器的池的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="13e4f-219">Fully qualified domain name of the pool containing the Front End server that submitted the report.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="13e4f-220">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13e4f-220">


</div>

<span> </span>

</div>

</div>

</span></span></div>

