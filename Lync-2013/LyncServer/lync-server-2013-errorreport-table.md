---
title: Lync Server 2013：ErrorReport 表
description: Lync Server 2013： ErrorReport 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport table
ms:assetid: ae0287b4-e8ca-4f8c-84ef-502897dcaa2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412826(v=OCS.15)
ms:contentKeyID: 48185129
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c1cc65c396c16dc137255438f7ef7c32b2d0b78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428515"
---
# <a name="errorreport-table-in-lync-server-2013"></a><span data-ttu-id="18772-103">Lync Server 2013 中的 ErrorReport 表</span><span class="sxs-lookup"><span data-stu-id="18772-103">ErrorReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18772-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18772-104">

<span> </span></span></span>

<span data-ttu-id="18772-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="18772-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="18772-106">ErrorReport 表存储发生的错误的相关信息。</span><span class="sxs-lookup"><span data-stu-id="18772-106">The ErrorReport table stores information about errors that have occurred.</span></span> <span data-ttu-id="18772-107">每条记录是一个错误发生。</span><span class="sxs-lookup"><span data-stu-id="18772-107">Each record is one error occurrence.</span></span> <span data-ttu-id="18772-108">这些错误由前端服务器上运行的 CDR 代理或从客户端发送的 CDR 捕获。</span><span class="sxs-lookup"><span data-stu-id="18772-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18772-109">列</span><span class="sxs-lookup"><span data-stu-id="18772-109">Column</span></span></th>
<th><span data-ttu-id="18772-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="18772-110">Data Type</span></span></th>
<th><span data-ttu-id="18772-111">键/索引</span><span class="sxs-lookup"><span data-stu-id="18772-111">Key/Index</span></span></th>
<th><span data-ttu-id="18772-112">详细信息</span><span class="sxs-lookup"><span data-stu-id="18772-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18772-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="18772-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-114">datetime</span><span class="sxs-lookup"><span data-stu-id="18772-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="18772-115">Primary</span><span class="sxs-lookup"><span data-stu-id="18772-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="18772-116">出现错误的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="18772-116">Date and time the error occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="18772-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-118">int</span><span class="sxs-lookup"><span data-stu-id="18772-118">int</span></span></p></td>
<td><p><span data-ttu-id="18772-119">Primary</span><span class="sxs-lookup"><span data-stu-id="18772-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="18772-120">标识错误报告的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="18772-120">ID number to identify the error report.</span></span> <span data-ttu-id="18772-121">与 <strong>ErrorTime</strong> 结合使用以唯一标识错误报告。</span><span class="sxs-lookup"><span data-stu-id="18772-121">Used in conjunction with <strong>ErrorTime</strong> to uniquely identify an error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18772-122"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-122"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-123">int</span><span class="sxs-lookup"><span data-stu-id="18772-123">int</span></span></p></td>
<td><p><span data-ttu-id="18772-124">外表</span><span class="sxs-lookup"><span data-stu-id="18772-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-125">错误类型的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="18772-125">Unique ID of the error type.</span></span> <span data-ttu-id="18772-126">有关详细信息，请参阅 <a href="lync-server-2013-errordef-table.md">Lync Server 2013 中的 ErrorDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="18772-126">See the <a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-127"><strong>FromUserId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-127"><strong>FromUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-128">int</span><span class="sxs-lookup"><span data-stu-id="18772-128">int</span></span></p></td>
<td><p><span data-ttu-id="18772-129">外表</span><span class="sxs-lookup"><span data-stu-id="18772-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-130">发出导致错误的请求的用户。</span><span class="sxs-lookup"><span data-stu-id="18772-130">User who originated the request that caused the error.</span></span> <span data-ttu-id="18772-131">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="18772-131">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18772-132"><strong>ToUserId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-132"><strong>ToUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-133">int</span><span class="sxs-lookup"><span data-stu-id="18772-133">int</span></span></p></td>
<td><p><span data-ttu-id="18772-134">外表</span><span class="sxs-lookup"><span data-stu-id="18772-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-135">导致错误的请求的目标用户。</span><span class="sxs-lookup"><span data-stu-id="18772-135">Destination user for the request that caused the error.</span></span> <span data-ttu-id="18772-136">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="18772-136">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-137"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-137"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-138">int</span><span class="sxs-lookup"><span data-stu-id="18772-138">int</span></span></p></td>
<td><p><span data-ttu-id="18772-139">外表</span><span class="sxs-lookup"><span data-stu-id="18772-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-140">与该错误相关的会议 URI。</span><span class="sxs-lookup"><span data-stu-id="18772-140">Conference URI related to the error.</span></span> <span data-ttu-id="18772-141">有关详细信息，请参阅 <a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 中的 ConferenceUris 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="18772-141">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="18772-142">通常情况下，如果 ConferenceUriId 不为 null，则 FromUserId 或 ToUserId 将为 null。</span><span class="sxs-lookup"><span data-stu-id="18772-142">Typically, if ConferenceUriId is not null, then either FromUserId or ToUserId will be null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18772-143"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="18772-143"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-144">datetime</span><span class="sxs-lookup"><span data-stu-id="18772-144">datetime</span></span></p></td>
<td><p><span data-ttu-id="18772-145">外表</span><span class="sxs-lookup"><span data-stu-id="18772-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-146">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="18772-146">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="18772-147">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="18772-147">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-148"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="18772-148"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-149">int</span><span class="sxs-lookup"><span data-stu-id="18772-149">int</span></span></p></td>
<td><p><span data-ttu-id="18772-150">外表</span><span class="sxs-lookup"><span data-stu-id="18772-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-151">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="18772-151">ID number to identify the session.</span></span> <span data-ttu-id="18772-152">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="18772-152">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="18772-153">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="18772-153">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18772-154"><strong>SourceId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-154"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-155">int</span><span class="sxs-lookup"><span data-stu-id="18772-155">int</span></span></p></td>
<td><p><span data-ttu-id="18772-156">外表</span><span class="sxs-lookup"><span data-stu-id="18772-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-157">发送错误报告的服务器 (如果正在从服务器组件) 发送报表，则为该服务器。</span><span class="sxs-lookup"><span data-stu-id="18772-157">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="18772-158">有关详细信息，请参阅 <a href="lync-server-2013-servers-table.md">Lync Server 2013 中</a> 的 "服务器" 表。</span><span class="sxs-lookup"><span data-stu-id="18772-158">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="18772-159">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="18772-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-160"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-160"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-161">int</span><span class="sxs-lookup"><span data-stu-id="18772-161">int</span></span></p></td>
<td><p><span data-ttu-id="18772-162">外表</span><span class="sxs-lookup"><span data-stu-id="18772-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-163">发送错误报告的服务器 (如果正在从服务器组件) 发送报表，则为该服务器。</span><span class="sxs-lookup"><span data-stu-id="18772-163">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="18772-164">有关详细信息，请参阅 <a href="lync-server-2013-application-table.md">Lync Server 2013 中的应用程序表</a> 。</span><span class="sxs-lookup"><span data-stu-id="18772-164">See the <a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="18772-165">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="18772-165">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18772-166"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="18772-166"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-167">图像</span><span class="sxs-lookup"><span data-stu-id="18772-167">image</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="18772-168">有关错误的详细信息。</span><span class="sxs-lookup"><span data-stu-id="18772-168">More information about the error.</span></span></p>
<p><span data-ttu-id="18772-169">可以使用以下语法将此数据转换为文本格式：</span><span class="sxs-lookup"><span data-stu-id="18772-169">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(Detail as varbinary(max)) as varchar(max)) </code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-170"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-170"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-171">int</span><span class="sxs-lookup"><span data-stu-id="18772-171">int</span></span></p></td>
<td><p><span data-ttu-id="18772-172">外表</span><span class="sxs-lookup"><span data-stu-id="18772-172">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-173">发送错误报告的终结点的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="18772-173">The client version of endpoint that sends the error report.</span></span> <span data-ttu-id="18772-174">有关详细信息，请参阅 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 中的 ClientVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="18772-174">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18772-175"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="18772-175"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-176">bit</span><span class="sxs-lookup"><span data-stu-id="18772-176">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="18772-177">由前端服务器上运行的 CDR 代理捕获的错误报告，或由客户端发送的错误报告。</span><span class="sxs-lookup"><span data-stu-id="18772-177">Is the error report captured by the CDR agent running on the front-end server, or sent by the client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-178"><strong>旗</strong></span><span class="sxs-lookup"><span data-stu-id="18772-178"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-179">smallint</span><span class="sxs-lookup"><span data-stu-id="18772-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="18772-180">保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="18772-180">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18772-181"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-181"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-182">标识符</span><span class="sxs-lookup"><span data-stu-id="18772-182">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="18772-183">关联会议中涉及的不同组件的加入时间信息的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="18772-183">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="18772-184">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="18772-184">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-185"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="18772-185"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-186">int</span><span class="sxs-lookup"><span data-stu-id="18772-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="18772-187">特定组件加入会议所需的时间 (以毫秒为单位) 。</span><span class="sxs-lookup"><span data-stu-id="18772-187">Time (in milliseconds) required for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="18772-188">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="18772-188">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18772-189"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-189"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-190">int</span><span class="sxs-lookup"><span data-stu-id="18772-190">int</span></span></p></td>
<td><p><span data-ttu-id="18772-191">外表</span><span class="sxs-lookup"><span data-stu-id="18772-191">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-192">表示生成错误报告的服务器的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="18772-192">Represents the fully qualified domain name of the server that generated the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18772-193"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="18772-193"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="18772-194">int</span><span class="sxs-lookup"><span data-stu-id="18772-194">int</span></span></p></td>
<td><p><span data-ttu-id="18772-195">外表</span><span class="sxs-lookup"><span data-stu-id="18772-195">Foreign</span></span></p></td>
<td><p><span data-ttu-id="18772-196">表示生成错误报告的池的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="18772-196">Represents the fully qualified domain name of the pool where the error report was generated.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="18772-197">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18772-197">


</div>

<span> </span>

</div>

</div>

</span></span></div>

