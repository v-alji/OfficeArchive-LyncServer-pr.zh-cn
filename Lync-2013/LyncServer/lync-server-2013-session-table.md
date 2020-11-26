---
title: Lync Server 2013：Session 表
description: Lync Server 2013： Session 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session table
ms:assetid: 7f05529c-794d-41ed-bca4-2e85b87b2dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398635(v=OCS.15)
ms:contentKeyID: 48184626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1a52813dfea808253cc934f71a9d4c846c2dbbd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441814"
---
# <a name="session-table-in-lync-server-2013"></a><span data-ttu-id="39175-103">Lync Server 2013 中的 Session 表</span><span class="sxs-lookup"><span data-stu-id="39175-103">Session table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39175-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39175-104">

<span> </span></span></span>

<span data-ttu-id="39175-105">_**主题上次修改时间：** 2013-09-09_</span><span class="sxs-lookup"><span data-stu-id="39175-105">_**Topic Last Modified:** 2013-09-09_</span></span>

<span data-ttu-id="39175-106">每条记录表示一个包含音频或音频和视频的会话。</span><span class="sxs-lookup"><span data-stu-id="39175-106">Each record represents one session which involves audio or audio and video.</span></span> <span data-ttu-id="39175-107">它包含有关会话的整体信息。</span><span class="sxs-lookup"><span data-stu-id="39175-107">It contains overall information about the session.</span></span> <span data-ttu-id="39175-108">会话在两个终结点之间定义为音频或视频会话初始协议 (SIP) 对话框。</span><span class="sxs-lookup"><span data-stu-id="39175-108">A session is defined as an audio or video Session Initiation Protocol (SIP) dialog between two endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39175-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="39175-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="39175-110"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="39175-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="39175-111"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="39175-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="39175-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="39175-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39175-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="39175-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-114">datetime</span><span class="sxs-lookup"><span data-stu-id="39175-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="39175-115">Primary</span><span class="sxs-lookup"><span data-stu-id="39175-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="39175-116">从 <a href="lync-server-2013-dialog-table.md">Lync Server 2013 的对话框表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-116">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="39175-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-118">int</span><span class="sxs-lookup"><span data-stu-id="39175-118">int</span></span></p></td>
<td><p><span data-ttu-id="39175-119">Primary</span><span class="sxs-lookup"><span data-stu-id="39175-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="39175-120">从 <a href="lync-server-2013-dialog-table.md">Lync Server 2013 的对话框表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-120">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-121"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="39175-121"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-122">int</span><span class="sxs-lookup"><span data-stu-id="39175-122">int</span></span></p></td>
<td><p><span data-ttu-id="39175-123">外表</span><span class="sxs-lookup"><span data-stu-id="39175-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-124">会议密钥。</span><span class="sxs-lookup"><span data-stu-id="39175-124">Conference key.</span></span> <span data-ttu-id="39175-125">从 <a href="lync-server-2013-conference-table.md">Lync Server 2013 中的 "会议" 表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-125">Referenced from the <a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-126"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="39175-126"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-127">int</span><span class="sxs-lookup"><span data-stu-id="39175-127">int</span></span></p></td>
<td><p><span data-ttu-id="39175-128">外表</span><span class="sxs-lookup"><span data-stu-id="39175-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-129">相关密钥。</span><span class="sxs-lookup"><span data-stu-id="39175-129">Correlation key.</span></span> <span data-ttu-id="39175-130">从 <a href="lync-server-2013-sessioncorrelation-table.md">Lync Server 2013 中的 SessionCorrelation 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-130">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-131"><strong>DialogCategory</strong></span><span class="sxs-lookup"><span data-stu-id="39175-131"><strong>DialogCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-132">bit</span><span class="sxs-lookup"><span data-stu-id="39175-132">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="39175-133">对话框类别;0是 Lync 服务器以中介服务器腿;1是中介服务器到 PSTN 网关腿。</span><span class="sxs-lookup"><span data-stu-id="39175-133">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-134"><strong>MediationServerBypassFlag</strong></span><span class="sxs-lookup"><span data-stu-id="39175-134"><strong>MediationServerBypassFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-135">bit</span><span class="sxs-lookup"><span data-stu-id="39175-135">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="39175-136">指示是否已绕过呼叫的标志。</span><span class="sxs-lookup"><span data-stu-id="39175-136">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-137"><strong>MediaBypassWarningFlag</strong></span><span class="sxs-lookup"><span data-stu-id="39175-137"><strong>MediaBypassWarningFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-138">int</span><span class="sxs-lookup"><span data-stu-id="39175-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="39175-139">此字段（如果存在）指示无法跳过呼叫的原因，即使旁路 Id 匹配也是如此。</span><span class="sxs-lookup"><span data-stu-id="39175-139">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="39175-140">对于 Lync Server，只定义一个值。</span><span class="sxs-lookup"><span data-stu-id="39175-140">For Lync Server, only one value is defined.</span></span></p>
<p><span data-ttu-id="39175-141">0x0001-默认网络适配器的旁路 ID 未知。</span><span class="sxs-lookup"><span data-stu-id="39175-141">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-142"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="39175-142"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-143">datetime</span><span class="sxs-lookup"><span data-stu-id="39175-143">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="39175-144">通话开始时间。</span><span class="sxs-lookup"><span data-stu-id="39175-144">Call start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-145"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="39175-145"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-146">datetime</span><span class="sxs-lookup"><span data-stu-id="39175-146">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="39175-147">通话结束时间。</span><span class="sxs-lookup"><span data-stu-id="39175-147">Call end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-148"><strong>CallerPool</strong></span><span class="sxs-lookup"><span data-stu-id="39175-148"><strong>CallerPool</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-149">int</span><span class="sxs-lookup"><span data-stu-id="39175-149">int</span></span></p></td>
<td><p><span data-ttu-id="39175-150">外表</span><span class="sxs-lookup"><span data-stu-id="39175-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-151">呼叫方的池。</span><span class="sxs-lookup"><span data-stu-id="39175-151">The pool of the caller.</span></span> <span data-ttu-id="39175-152">从 <a href="lync-server-2013-pool-table.md">Lync Server 2013 的 Pool 表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-152">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-153"><strong>CalleePool</strong></span><span class="sxs-lookup"><span data-stu-id="39175-153"><strong>CalleePool</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-154">int</span><span class="sxs-lookup"><span data-stu-id="39175-154">int</span></span></p></td>
<td><p><span data-ttu-id="39175-155">外表</span><span class="sxs-lookup"><span data-stu-id="39175-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-156">呼叫接收器的池。</span><span class="sxs-lookup"><span data-stu-id="39175-156">The pool of the call receiver.</span></span> <span data-ttu-id="39175-157">从 <a href="lync-server-2013-pool-table.md">Lync Server 2013 的 Pool 表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-157">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-158"><strong>CalleePAI</strong></span><span class="sxs-lookup"><span data-stu-id="39175-158"><strong>CalleePAI</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-159">int</span><span class="sxs-lookup"><span data-stu-id="39175-159">int</span></span></p></td>
<td><p><span data-ttu-id="39175-160">外表</span><span class="sxs-lookup"><span data-stu-id="39175-160">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-161">SIP p-声明标识 (PAI) 接收终结点的 SIP URI。</span><span class="sxs-lookup"><span data-stu-id="39175-161">SIP URI in the SIP p-asserted identity (PAI) of the receiving endpoint.</span></span> <span data-ttu-id="39175-162">从 <a href="lync-server-2013-user-table.md">Lync Server 2013 中的用户表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-162">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-163"><strong>CallerURI</strong></span><span class="sxs-lookup"><span data-stu-id="39175-163"><strong>CallerURI</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-164">int</span><span class="sxs-lookup"><span data-stu-id="39175-164">int</span></span></p></td>
<td><p><span data-ttu-id="39175-165">外表</span><span class="sxs-lookup"><span data-stu-id="39175-165">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-166">调用方的 URI。</span><span class="sxs-lookup"><span data-stu-id="39175-166">Caller’s URI.</span></span> <span data-ttu-id="39175-167">从 <a href="lync-server-2013-user-table.md">Lync Server 2013 中的用户表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-167">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-168"><strong>CallerEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="39175-168"><strong>CallerEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-169">int</span><span class="sxs-lookup"><span data-stu-id="39175-169">int</span></span></p></td>
<td><p><span data-ttu-id="39175-170">外表</span><span class="sxs-lookup"><span data-stu-id="39175-170">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-171">调用方的终结点。</span><span class="sxs-lookup"><span data-stu-id="39175-171">Caller’s endpoint.</span></span> <span data-ttu-id="39175-172">从 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 的终结点表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-172">Referenced from the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-173"><strong>CallerUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="39175-173"><strong>CallerUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-174">bit</span><span class="sxs-lookup"><span data-stu-id="39175-174">bit</span></span></p></td>
<td><p><span data-ttu-id="39175-175">外表</span><span class="sxs-lookup"><span data-stu-id="39175-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-176">呼叫方的用户代理。</span><span class="sxs-lookup"><span data-stu-id="39175-176">Caller’s user agent.</span></span> <span data-ttu-id="39175-177">从 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 中的 UserAgent 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="39175-177">Referenced from the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-178"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="39175-178"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-179">smallint</span><span class="sxs-lookup"><span data-stu-id="39175-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="39175-180">此通话的优先级。</span><span class="sxs-lookup"><span data-stu-id="39175-180">The priority of this call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-181"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="39175-181"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-182">bit</span><span class="sxs-lookup"><span data-stu-id="39175-182">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="39175-183">此列已弃用，并且未在 Microsoft Lync Server 2013 中使用。</span><span class="sxs-lookup"><span data-stu-id="39175-183">This column has been deprecated and is not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="39175-184">而是报告每个媒体行基础上的此信息。</span><span class="sxs-lookup"><span data-stu-id="39175-184">Instead, this information is reported on a per-media line bases.</span></span> <span data-ttu-id="39175-185">有关详细信息，请参阅 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="39175-185">Refer to the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-186"><strong>CallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="39175-186"><strong>CallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-187">int</span><span class="sxs-lookup"><span data-stu-id="39175-187">int</span></span></p></td>
<td><p><span data-ttu-id="39175-188">外表</span><span class="sxs-lookup"><span data-stu-id="39175-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-189">P-声明-发出呼叫的用户的标识。</span><span class="sxs-lookup"><span data-stu-id="39175-189">P-Asserted-Identity of the user who placed the call.</span></span> <span data-ttu-id="39175-190">P 声明的标识 (PAI) 用于传达发出呼叫的用户的真实标识。</span><span class="sxs-lookup"><span data-stu-id="39175-190">The P-Asserted-Identity (PAI) is used to convey the true identity of the user who placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-191"><strong>CalleeEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="39175-191"><strong>CalleeEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-192">int</span><span class="sxs-lookup"><span data-stu-id="39175-192">int</span></span></p></td>
<td><p><span data-ttu-id="39175-193">外表</span><span class="sxs-lookup"><span data-stu-id="39175-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-194">接收呼叫的终结点。</span><span class="sxs-lookup"><span data-stu-id="39175-194">Endpoint that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39175-195"><strong>CalleeUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="39175-195"><strong>CalleeUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-196">int</span><span class="sxs-lookup"><span data-stu-id="39175-196">int</span></span></p></td>
<td><p><span data-ttu-id="39175-197">外表</span><span class="sxs-lookup"><span data-stu-id="39175-197">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-198">接收呼叫的用户所使用的用户代理。</span><span class="sxs-lookup"><span data-stu-id="39175-198">User agent employed by the user who received the call.</span></span> <span data-ttu-id="39175-199">用户代理代表客户端终结点设备。</span><span class="sxs-lookup"><span data-stu-id="39175-199">User agents represent the client endpoint device.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39175-200"><strong>CalleeUri</strong></span><span class="sxs-lookup"><span data-stu-id="39175-200"><strong>CalleeUri</strong></span></span></p></td>
<td><p><span data-ttu-id="39175-201">int</span><span class="sxs-lookup"><span data-stu-id="39175-201">int</span></span></p></td>
<td><p><span data-ttu-id="39175-202">外表</span><span class="sxs-lookup"><span data-stu-id="39175-202">Foreign</span></span></p></td>
<td><p><span data-ttu-id="39175-203">接收呼叫的用户的 SIP URI。</span><span class="sxs-lookup"><span data-stu-id="39175-203">SIP URI of the user who received the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="39175-204">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39175-204">


</div>

<span> </span>

</div>

</div>

</span></span></div>

