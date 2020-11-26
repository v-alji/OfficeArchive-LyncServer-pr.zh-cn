---
title: Lync Server 2013： ProgressReport 视图
description: Lync Server 2013： ProgressReport 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport view
ms:assetid: b49f3fc7-0e2f-498f-8505-aaaf54e435f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721857(v=OCS.15)
ms:contentKeyID: 49733790
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b95086012f254499644e778e43cafdf70ffc8f9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436851"
---
# <a name="progressreport-view-in-lync-server-2013"></a><span data-ttu-id="bf40e-103">Lync Server 2013 中的 ProgressReport 视图</span><span class="sxs-lookup"><span data-stu-id="bf40e-103">ProgressReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf40e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf40e-104">

<span> </span></span></span>

<span data-ttu-id="bf40e-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="bf40e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="bf40e-106">ProgressReport 视图存储有关已完成会话的信息。</span><span class="sxs-lookup"><span data-stu-id="bf40e-106">The ProgressReport view stores information about completed sessions.</span></span> <span data-ttu-id="bf40e-107">将仅写入 Lync Server 2013 确定可能对诊断目的有用的通话和会话的进度报告。</span><span class="sxs-lookup"><span data-stu-id="bf40e-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span> <span data-ttu-id="bf40e-108">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="bf40e-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bf40e-109">"ErrorTime"、"ErrorReportSeq" 和 "ProgressReportSeq" 字段不一定是指错误，而是指示调用状态或消息的消息。</span><span class="sxs-lookup"><span data-stu-id="bf40e-109">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf40e-110">列</span><span class="sxs-lookup"><span data-stu-id="bf40e-110">Column</span></span></th>
<th><span data-ttu-id="bf40e-111">数据类型</span><span class="sxs-lookup"><span data-stu-id="bf40e-111">Data Type</span></span></th>
<th><span data-ttu-id="bf40e-112">详细信息</span><span class="sxs-lookup"><span data-stu-id="bf40e-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf40e-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-114">datetime</span><span class="sxs-lookup"><span data-stu-id="bf40e-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="bf40e-115">出现错误的时间。</span><span class="sxs-lookup"><span data-stu-id="bf40e-115">Time of error occurred.</span></span> <span data-ttu-id="bf40e-116">与 ErrorReportSeq 结合使用以唯一标识错误。</span><span class="sxs-lookup"><span data-stu-id="bf40e-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf40e-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-118">int</span><span class="sxs-lookup"><span data-stu-id="bf40e-118">int</span></span></p></td>
<td><p><span data-ttu-id="bf40e-119">标识错误的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="bf40e-119">ID number to identify the error.</span></span> <span data-ttu-id="bf40e-120">与 ErrorTime 结合使用以唯一标识错误。</span><span class="sxs-lookup"><span data-stu-id="bf40e-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf40e-121"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-121"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-122">int</span><span class="sxs-lookup"><span data-stu-id="bf40e-122">int</span></span></p></td>
<td><p><span data-ttu-id="bf40e-123">标识进度报表的 ID。</span><span class="sxs-lookup"><span data-stu-id="bf40e-123">ID to identify the progress report.</span></span> <span data-ttu-id="bf40e-124">用于区分同一错误报告的进度报告。</span><span class="sxs-lookup"><span data-stu-id="bf40e-124">Used to distinguish progress reports of the same error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf40e-125"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-125"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-126">int</span><span class="sxs-lookup"><span data-stu-id="bf40e-126">int</span></span></p></td>
<td><p><span data-ttu-id="bf40e-127">错误报告的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="bf40e-127">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf40e-128"><strong>来源</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-128"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-129">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bf40e-129">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bf40e-130">如果从服务器组件) 发送报表，则产生错误的服务器的名称 (。</span><span class="sxs-lookup"><span data-stu-id="bf40e-130">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf40e-131"><strong>Application</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-131"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bf40e-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bf40e-133">发出错误的应用程序的名称 (从服务器组件) 发送报表时。</span><span class="sxs-lookup"><span data-stu-id="bf40e-133">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf40e-134"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-134"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-135">标识符</span><span class="sxs-lookup"><span data-stu-id="bf40e-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="bf40e-136">关联会议中涉及的不同组件的加入时间信息的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="bf40e-136">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf40e-137"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-137"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-138">int</span><span class="sxs-lookup"><span data-stu-id="bf40e-138">int</span></span></p></td>
<td><p><span data-ttu-id="bf40e-139">特定组件加入会议所需的时间 (以毫秒为单位) 。</span><span class="sxs-lookup"><span data-stu-id="bf40e-139">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf40e-140"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="bf40e-140"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="bf40e-141">varchar (max) </span><span class="sxs-lookup"><span data-stu-id="bf40e-141">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="bf40e-142">其他错误信息。</span><span class="sxs-lookup"><span data-stu-id="bf40e-142">Additional error information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bf40e-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf40e-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

