---
title: Lync Server 2013：ProgressReport 表
description: Lync Server 2013： ProgressReport 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport table
ms:assetid: 38e5f060-5e9b-4185-87b2-7ef61c4bb75f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425864(v=OCS.15)
ms:contentKeyID: 48183847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d36ee2ab75410ea2462da4b647ef5b45afefb1bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436865"
---
# <a name="progressreport-table-in-lync-server-2013"></a><span data-ttu-id="e047b-103">Lync Server 2013 中的 ProgressReport 表</span><span class="sxs-lookup"><span data-stu-id="e047b-103">ProgressReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e047b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e047b-104">

<span> </span></span></span>

<span data-ttu-id="e047b-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="e047b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="e047b-106">进度报告基于客户端在通话或会话完成后上载到数据库的数据。</span><span class="sxs-lookup"><span data-stu-id="e047b-106">Progress reports are based on data uploaded by the client to the database after a call or session is completed.</span></span> <span data-ttu-id="e047b-107">将仅写入 Lync Server 2013 确定可能对诊断目的有用的通话和会话的进度报告。</span><span class="sxs-lookup"><span data-stu-id="e047b-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span>

<span data-ttu-id="e047b-108">"ErrorTime"、"ErrorReportSeq" 和 "ProgressReportSeq" 字段不一定是指错误，而是指示调用状态或消息的消息。</span><span class="sxs-lookup"><span data-stu-id="e047b-108">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e047b-109">列</span><span class="sxs-lookup"><span data-stu-id="e047b-109">Column</span></span></th>
<th><span data-ttu-id="e047b-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="e047b-110">Data Type</span></span></th>
<th><span data-ttu-id="e047b-111">键/索引</span><span class="sxs-lookup"><span data-stu-id="e047b-111">Key/Index</span></span></th>
<th><span data-ttu-id="e047b-112">详细信息</span><span class="sxs-lookup"><span data-stu-id="e047b-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e047b-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-114">datetime</span><span class="sxs-lookup"><span data-stu-id="e047b-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="e047b-115">主、外部</span><span class="sxs-lookup"><span data-stu-id="e047b-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e047b-116">包含此进度报表的 "进度错误" 报表的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e047b-116">Date and time of the progress error report that contains this progress report.</span></span> <span data-ttu-id="e047b-117">有关详细信息，请参阅 <a href="lync-server-2013-errorreport-table.md">Lync Server 2013 中的 ErrorReport 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="e047b-117">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e047b-118"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-118"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-119">int</span><span class="sxs-lookup"><span data-stu-id="e047b-119">int</span></span></p></td>
<td><p><span data-ttu-id="e047b-120">主、外部</span><span class="sxs-lookup"><span data-stu-id="e047b-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e047b-121">与 ErrorTime 和 ProgressReportSeq 结合使用的 ID 号，用于唯一标识进度报告。</span><span class="sxs-lookup"><span data-stu-id="e047b-121">ID number used in conjunction with ErrorTime, ProgressReportSeq to uniquely identify a progress report.</span></span> <span data-ttu-id="e047b-122">有关详细信息，请参阅 <a href="lync-server-2013-errorreport-table.md">Lync Server 2013 中的 ErrorReport 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="e047b-122">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e047b-123"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-123"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-124">int</span><span class="sxs-lookup"><span data-stu-id="e047b-124">int</span></span></p></td>
<td><p><span data-ttu-id="e047b-125">主、外部</span><span class="sxs-lookup"><span data-stu-id="e047b-125">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e047b-126">标识错误报告的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="e047b-126">ID number that identifies the error report.</span></span> <span data-ttu-id="e047b-127">ErrorReporSeq 与 ErrorTime 结合使用，以唯一标识错误报告。</span><span class="sxs-lookup"><span data-stu-id="e047b-127">ErrorReporSeq is used in conjunction with ErrorTime to uniquely identify an error report.</span></span> <span data-ttu-id="e047b-128">有关详细信息，请参阅 <a href="lync-server-2013-errorreport-table.md">Lync Server 2013 中的 ErrorReport 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="e047b-128">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information</span></span></p>
<p><span data-ttu-id="e047b-129">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="e047b-129">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e047b-130"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-130"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-131">int</span><span class="sxs-lookup"><span data-stu-id="e047b-131">int</span></span></p></td>
<td><p><span data-ttu-id="e047b-132">Primary</span><span class="sxs-lookup"><span data-stu-id="e047b-132">Primary</span></span></p></td>
<td><p><span data-ttu-id="e047b-133">标识进度报表的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="e047b-133">ID number to identify the progress report.</span></span> <span data-ttu-id="e047b-134">与 ErrorTime 和 ErrorReportSeq 结合使用，以唯一标识进度报表。</span><span class="sxs-lookup"><span data-stu-id="e047b-134">Used in conjunction with ErrorTime and ErrorReportSeq to uniquely identify a progress report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e047b-135"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-135"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-136">int</span><span class="sxs-lookup"><span data-stu-id="e047b-136">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e047b-137">进度报表的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="e047b-137">Diagnostic ID of the progress report.</span></span></p>
<p><span data-ttu-id="e047b-138">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="e047b-138">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e047b-139"><strong>SourceId</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-139"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-140">int</span><span class="sxs-lookup"><span data-stu-id="e047b-140">int</span></span></p></td>
<td><p><span data-ttu-id="e047b-141">外表</span><span class="sxs-lookup"><span data-stu-id="e047b-141">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e047b-142">如果报表是从服务器组件) 发送的，则发送错误报告 (的服务器。</span><span class="sxs-lookup"><span data-stu-id="e047b-142">Server that sent the error report (if the report was sent from a server component).</span></span> <span data-ttu-id="e047b-143">有关详细信息，请参阅 <a href="lync-server-2013-servers-table.md">Lync Server 2013 中</a> 的 "服务器" 表。此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="e047b-143">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e047b-144"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-144"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-145">int</span><span class="sxs-lookup"><span data-stu-id="e047b-145">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e047b-146">报表所针对的 Lync Server 进程。</span><span class="sxs-lookup"><span data-stu-id="e047b-146">The Lync Server process that the report is about.</span></span> <span data-ttu-id="e047b-147">有关详细信息，请参阅应用程序表。</span><span class="sxs-lookup"><span data-stu-id="e047b-147">See the Application Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e047b-148"><strong>详情</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-148"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-149">图像</span><span class="sxs-lookup"><span data-stu-id="e047b-149">image</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e047b-150">进度报告详细信息，以二进制格式存储以节省空间。此数据可以使用以下语法转换为文本格式：</span><span class="sxs-lookup"><span data-stu-id="e047b-150">Progress report details, stored in binary format to save space.This data can be converted to text format using this syntax:</span></span></p>
<p><span data-ttu-id="e047b-151">转换 (将 (详细信息转换为 varbinary (最大) # A4 作为 varchar (最大) # A7</span><span class="sxs-lookup"><span data-stu-id="e047b-151">cast(cast(Detail as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e047b-152"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-152"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-153">标识符</span><span class="sxs-lookup"><span data-stu-id="e047b-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e047b-154">关联会议中涉及的不同组件的联接时间信息的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e047b-154">Unique identifier that correlates join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="e047b-155">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="e047b-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e047b-156"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="e047b-156"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e047b-157">int</span><span class="sxs-lookup"><span data-stu-id="e047b-157">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e047b-158">特定组件加入会议的时间 (（以毫秒为单位）) 。</span><span class="sxs-lookup"><span data-stu-id="e047b-158">Time (in milliseconds) for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="e047b-159">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="e047b-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e047b-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e047b-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

