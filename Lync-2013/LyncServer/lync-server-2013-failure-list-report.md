---
title: Lync Server 2013： "失败列表" 报表
description: Lync Server 2013：失败列表报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure List Report
ms:assetid: b6f3a605-e0c6-461e-b17a-41d8039ace9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615446(v=OCS.15)
ms:contentKeyID: 48185194
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7467144fe207ab61fd086cd35aac74779fd4f771
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391828"
---
# <a name="failure-list-report-in-lync-server-2013"></a><span data-ttu-id="2bd2e-103">Lync Server 2013 中的 "故障列表" 报表</span><span class="sxs-lookup"><span data-stu-id="2bd2e-103">Failure List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2bd2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2bd2e-104">

<span> </span></span></span>

<span data-ttu-id="2bd2e-105">_**主题上次修改时间：** 2012-07-02_</span><span class="sxs-lookup"><span data-stu-id="2bd2e-105">_**Topic Last Modified:** 2012-07-02_</span></span>

<span data-ttu-id="2bd2e-p101">故障列表报告提供有关参加失败的对等会话或会议会话的各个参与者的信息。此信息包括遇到问题的用户的 URI，以及与故障相关联的 SIP 响应代码和诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-p101">The Failure List report provides information about the individual participants who took part in a failed peer-to-peer or conferencing session. This information includes the URI of the user who experienced the problem, as well as the SIP Response code and Diagnostic ID associated with the failure.</span></span>

<div>

## <a name="accessing-the-failure-list-report"></a><span data-ttu-id="2bd2e-108">访问故障列表报告</span><span class="sxs-lookup"><span data-stu-id="2bd2e-108">Accessing the Failure List Report</span></span>

<span data-ttu-id="2bd2e-109">通过 [在 Lync Server 2013 中的 "失败分发报告](lync-server-2013-failure-distribution-report.md)" 上单击以下任一指标可访问 "故障列表" 报告：</span><span class="sxs-lookup"><span data-stu-id="2bd2e-109">The Failure List Report is accessed by clicking any of the following metrics on the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md):</span></span>

  - <span data-ttu-id="2bd2e-110">主要诊断原因（会话）</span><span class="sxs-lookup"><span data-stu-id="2bd2e-110">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="2bd2e-111">主要形式（会话）</span><span class="sxs-lookup"><span data-stu-id="2bd2e-111">Top modalities (sessions)</span></span>

  - <span data-ttu-id="2bd2e-112">主要池（会话）</span><span class="sxs-lookup"><span data-stu-id="2bd2e-112">Top pools (sessions)</span></span>

  - <span data-ttu-id="2bd2e-113">主要来源（会话）</span><span class="sxs-lookup"><span data-stu-id="2bd2e-113">Top sources (sessions)</span></span>

  - <span data-ttu-id="2bd2e-114">主要组件（会话）</span><span class="sxs-lookup"><span data-stu-id="2bd2e-114">Top components (sessions)</span></span>

  - <span data-ttu-id="2bd2e-115">主要来源用户（会话）</span><span class="sxs-lookup"><span data-stu-id="2bd2e-115">Top from users (sessions)</span></span>

  - <span data-ttu-id="2bd2e-116">主要目标用户（会话）</span><span class="sxs-lookup"><span data-stu-id="2bd2e-116">Top to users (sessions)</span></span>

  - <span data-ttu-id="2bd2e-117">主要来源用户代理（会话）</span><span class="sxs-lookup"><span data-stu-id="2bd2e-117">Top from user agents (sessions)</span></span>

<span data-ttu-id="2bd2e-118">在 "故障列表" 报表中，通过单击对等会话的会话详细信息指标，可以 [在 Lync Server 2013 中访问对等会话详细信息报告](lync-server-2013-peer-to-peer-session-detail-report.md) 。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-118">From the Failure List Report you can access the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) by clicking the Session detail metric for a peer-to-peer session.</span></span> <span data-ttu-id="2bd2e-119">也可以单击会议的”会议“指标，以访问会议详细信息报告。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-119">You can also access the Conference Detail Report by clicking the Conference metric for a conference.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-failure-list-report"></a><span data-ttu-id="2bd2e-120">充分利用故障列表报告</span><span class="sxs-lookup"><span data-stu-id="2bd2e-120">Making the Best Use of the Failure List Report</span></span>

<span data-ttu-id="2bd2e-p103">在故障列表报告中，您只需将鼠标置于每个响应代码或每个诊断 ID 上，即可查看它们的说明。例如，如果您将鼠标置于诊断 ID 7025 上，则将会看到在工具提示中显示以下内容：</span><span class="sxs-lookup"><span data-stu-id="2bd2e-p103">In the Failure List Report, you can view a description for each Response code or each Diagnostic ID simply by holding your mouse over that value. For example, if you hold your mouse over Diagnostic ID 7025 you'll see the following displayed in a tooltip:</span></span>

<span data-ttu-id="2bd2e-123">为用户创建媒体时发生内部服务器错误。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-123">Internal server error creating media for user.</span></span>

<span data-ttu-id="2bd2e-124">务必注意，故障列表报告并未提供一种简单直观的方式来直接检索至少参加一次失败会话的所有用户列表，也未提供一种用来确定失败会话中最常涉及哪些用户的方法。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-124">It's important to note that the Failure List Report does not provide a straightforward way to directly retrieve a list of all the users who participated in at least one failed session, nor does it provide a way to determine which users were most-often involved in a failed session.</span></span> <span data-ttu-id="2bd2e-125"> (一件事，"故障列表" 报表没有筛选功能。 ) 但是，如果导出数据，然后将其转换为逗号分隔值文件，则可以使用 Windows PowerShell 查找类似问题的答案。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-125">(For one thing, the Failure List Report has no filtering capabilities.) However, if you export the data and then convert it to a comma-separated values file, you can use Windows PowerShell to find the answers to questions like those.</span></span> <span data-ttu-id="2bd2e-126">例如，假设您将数据保存到。名为 C： \\ 数据 \\ 失败的 CSV 文件 \_List.csv。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-126">For example, suppose you save the data to a .CSV file named C:\\Data\\Failure\_List.csv.</span></span> <span data-ttu-id="2bd2e-127">根据该文件中所保存的数据，以下命令会列出至少一次失败会话中所涉及的所有用户：</span><span class="sxs-lookup"><span data-stu-id="2bd2e-127">Based on the data saved in that file, this command lists all the users who were involved in at least one failed session:</span></span>

    $failures = Import-Csv -Path " C:\Data\Failure_List.csv"
    $failure |Sort-Object "From user" | Select-Object "From user" -Unique

<span data-ttu-id="2bd2e-128">该命令将返回与以下类似的列表：</span><span class="sxs-lookup"><span data-stu-id="2bd2e-128">That command will return a list similar to this:</span></span>

    From user
    ----
    Pilar.Ackerman@litwareinc.com
    Henrik.Jensen@litwareinc.com
    Gilead.Amosnino@litwareinc.com
    David.Ahs@litwareinc.com
    Ken.Myer@litwareinc.com

<span data-ttu-id="2bd2e-129">以下两个命令将返回涉及每个用户的失败会话总数：</span><span class="sxs-lookup"><span data-stu-id="2bd2e-129">These two commands report back the total number of failed sessions that each user was involved in:</span></span>

    $failures = Import-Csv -Path "C:\Data\Failure_List.csv"
    $failures | Group-Object "From user" | Select-Object Count, Name | Sort-Object -Property Count -Descending

<span data-ttu-id="2bd2e-130">这将返回与以下类似的数据：</span><span class="sxs-lookup"><span data-stu-id="2bd2e-130">That will return data similar to this:</span></span>

    Count    Name
     -----    ----
        20    Pilar.Ackerman@litwareinc.com
        20    David.Ahs@litwareinc.com
        16    Gilead.Amosnino@litwareinc.com
        16    Ken.Myero@litwareinc.com
        14    Henrik.Jensen@litwareinc.com

</div>

<div>

## <a name="filters"></a><span data-ttu-id="2bd2e-131">筛选器</span><span class="sxs-lookup"><span data-stu-id="2bd2e-131">Filters</span></span>

<span data-ttu-id="2bd2e-p105">无。您无法筛选故障列表报告。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-p105">None. You cannot filter the Failure List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="2bd2e-134">指标</span><span class="sxs-lookup"><span data-stu-id="2bd2e-134">Metrics</span></span>

<span data-ttu-id="2bd2e-135">下表列出了各失败呼叫的故障列表报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-135">The following table lists the information provided in the Failure List Report for each failed call.</span></span>

### <a name="failure-list-report-metrics"></a><span data-ttu-id="2bd2e-136">故障列表报告指标</span><span class="sxs-lookup"><span data-stu-id="2bd2e-136">Failure List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd2e-137">名称</span><span class="sxs-lookup"><span data-stu-id="2bd2e-137">Name</span></span></th>
<th><span data-ttu-id="2bd2e-138">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="2bd2e-138">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="2bd2e-139">描述</span><span class="sxs-lookup"><span data-stu-id="2bd2e-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bd2e-140"><strong>报告时间</strong></span><span class="sxs-lookup"><span data-stu-id="2bd2e-140"><strong>Reported time</strong></span></span></p></td>
<td><p><span data-ttu-id="2bd2e-141">否</span><span class="sxs-lookup"><span data-stu-id="2bd2e-141">No</span></span></p></td>
<td><p><span data-ttu-id="2bd2e-142">记录报告的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-142">Date and time the report was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bd2e-143"><strong>请求</strong></span><span class="sxs-lookup"><span data-stu-id="2bd2e-143"><strong>Request</strong></span></span></p></td>
<td><p><span data-ttu-id="2bd2e-144">否</span><span class="sxs-lookup"><span data-stu-id="2bd2e-144">No</span></span></p></td>
<td><p><span data-ttu-id="2bd2e-p106">失败的 SIP 请求类型。例如 INVITE 或 BYE。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-p106">SIP request type that failed. For example, INVITE or BYE.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bd2e-147"><strong>响应代码</strong></span><span class="sxs-lookup"><span data-stu-id="2bd2e-147"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="2bd2e-148">否</span><span class="sxs-lookup"><span data-stu-id="2bd2e-148">No</span></span></p></td>
<td><p><span data-ttu-id="2bd2e-149">会议失败时发送的 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-149">SIP response code sent when the conference failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bd2e-150"><strong>诊断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="2bd2e-150"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="2bd2e-151">否</span><span class="sxs-lookup"><span data-stu-id="2bd2e-151">No</span></span></p></td>
<td><p><span data-ttu-id="2bd2e-152">附加到 SIP 消息的唯一标识符（采用 ms-diagnostics 标头的形式），提供的信息在排查错误时通常很有帮助。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-152">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bd2e-153"><strong>加入成本时间（毫秒）</strong></span><span class="sxs-lookup"><span data-stu-id="2bd2e-153"><strong>Join cost time (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="2bd2e-154">否</span><span class="sxs-lookup"><span data-stu-id="2bd2e-154">No</span></span></p></td>
<td><p><span data-ttu-id="2bd2e-155">用户加入会议所需的时间量（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-155">Amount of time (in milliseconds) required for the user to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bd2e-156"><strong>来源用户</strong></span><span class="sxs-lookup"><span data-stu-id="2bd2e-156"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="2bd2e-157">否</span><span class="sxs-lookup"><span data-stu-id="2bd2e-157">No</span></span></p></td>
<td><p><span data-ttu-id="2bd2e-158">发起呼叫的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-158">SIP address of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bd2e-159"><strong>源用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="2bd2e-159"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="2bd2e-160">否</span><span class="sxs-lookup"><span data-stu-id="2bd2e-160">No</span></span></p></td>
<td><p><span data-ttu-id="2bd2e-161">呼叫发起用户的终结点使用的软件。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-161">Software used by the endpoint of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bd2e-162"><strong>目标用户</strong></span><span class="sxs-lookup"><span data-stu-id="2bd2e-162"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="2bd2e-163">否</span><span class="sxs-lookup"><span data-stu-id="2bd2e-163">No</span></span></p></td>
<td><p><span data-ttu-id="2bd2e-164">被呼叫用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="2bd2e-164">SIP address of the user who was being called.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2bd2e-165">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2bd2e-165">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

