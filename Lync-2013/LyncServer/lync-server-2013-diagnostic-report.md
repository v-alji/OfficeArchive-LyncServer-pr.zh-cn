---
title: Lync Server 2013：诊断报告
description: Lync Server 2013：诊断报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Diagnostic Report
ms:assetid: b389dbd9-f2e8-4184-93d0-2e504796ac16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615445(v=OCS.15)
ms:contentKeyID: 48185159
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 198b836437285b464ba9172e59c9a60ed0a53b65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429302"
---
# <a name="diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="09fb8-103">Lync Server 2013 中的诊断报告</span><span class="sxs-lookup"><span data-stu-id="09fb8-103">Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09fb8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09fb8-104">

<span> </span></span></span>

<span data-ttu-id="09fb8-105">_**主题上次修改时间：** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="09fb8-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="09fb8-106">诊断报告提供失败的会话的诊断和故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="09fb8-106">The Diagnostic Report provides diagnostic and troubleshooting information for a failed session.</span></span> <span data-ttu-id="09fb8-107">此信息包括在会话失败时所报告的诊断 ID 和诊断标头。</span><span class="sxs-lookup"><span data-stu-id="09fb8-107">This information includes both the Diagnostic ID and the Diagnostic header that were reported when the session failed.</span></span> <span data-ttu-id="09fb8-108">诊断 ID 是附加到 SIP 消息的唯一标识符（采用 ms-diagnostics 标头的形式），而诊断标头提供诊断 ID 的附带说明。</span><span class="sxs-lookup"><span data-stu-id="09fb8-108">The Diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) that gets attached to a SIP message, while the Diagnostic header provides an accompanying description for the Diagnostic ID.</span></span> <span data-ttu-id="09fb8-109">该报告可能还包含报告组件所了解的有价值的故障排除详细信息。</span><span class="sxs-lookup"><span data-stu-id="09fb8-109">The report might also contain valuable troubleshooting details that are known by the reporting component.</span></span> <span data-ttu-id="09fb8-110">例如：</span><span class="sxs-lookup"><span data-stu-id="09fb8-110">For example:</span></span>

  - <span data-ttu-id="09fb8-p102">由生成故障的 PSTN 网关提供的原因代码。在 PSTN 网络上，传出呼叫失败时，会自动生成 ISDN 用户部分 (ISUP) 原因代码。例如，PSTN 网关可能会发送原因代码 34，指示不存在可用于完成呼叫的任何电路或信道。</span><span class="sxs-lookup"><span data-stu-id="09fb8-p102">The cause code provided by the PSTN gateway that generated the failure. When an outgoing call fails on the PSTN network, an ISDN User Part (ISUP) cause code is automatically generated. For example, a PSTN gateway might send cause code 34 to indicate that no circuit or channel was available for completing the call.</span></span>

  - <span data-ttu-id="09fb8-114">针对连接失败的对等方 FQDN、端口和 Winsock 错误。</span><span class="sxs-lookup"><span data-stu-id="09fb8-114">Peer FQDN, port, and Winsock errors for connectivity failures.</span></span>

  - <span data-ttu-id="09fb8-p103">针对 DNS 解析失败所查找的名称。每次客户端联系名称服务器并请求与指定的设备名称相对应的 IP 地址时，都会进行 DNS 解析。</span><span class="sxs-lookup"><span data-stu-id="09fb8-p103">Names being looked up for DNS resolution failures. DNS resolution takes place any time a client contacts a name server and requests the IP address that corresponds to specified device name.</span></span>

<div>

## <a name="accessing-the-diagnostic-report"></a><span data-ttu-id="09fb8-117">访问诊断报告</span><span class="sxs-lookup"><span data-stu-id="09fb8-117">Accessing the Diagnostic Report</span></span>

<span data-ttu-id="09fb8-118">通过在 Lync Server 2013 或会议详细信息报告中单击 " [对等会话详细信息" 报表](lync-server-2013-peer-to-peer-session-detail-report.md) 上的 "诊断报告" (详细信息) 指标，即可访问诊断报告。</span><span class="sxs-lookup"><span data-stu-id="09fb8-118">The Diagnostic Report can be accessed by clicking the Diagnostic Report (Detail) metric on either the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) or the Conference Detail Report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="09fb8-119">筛选器</span><span class="sxs-lookup"><span data-stu-id="09fb8-119">Filters</span></span>

<span data-ttu-id="09fb8-p104">无。您不能对诊断报告进行筛选。</span><span class="sxs-lookup"><span data-stu-id="09fb8-p104">None. You cannot filter the Diagnostic Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="09fb8-122">指标</span><span class="sxs-lookup"><span data-stu-id="09fb8-122">Metrics</span></span>

<span data-ttu-id="09fb8-123">下表列出了各会话的诊断报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="09fb8-123">The following table lists the information provided in the Diagnostic Report for each session.</span></span>

### <a name="diagnostic-report-metrics"></a><span data-ttu-id="09fb8-124">诊断报告指标</span><span class="sxs-lookup"><span data-stu-id="09fb8-124">Diagnostic Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09fb8-125">名称</span><span class="sxs-lookup"><span data-stu-id="09fb8-125">Name</span></span></th>
<th><span data-ttu-id="09fb8-126">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="09fb8-126">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="09fb8-127">描述</span><span class="sxs-lookup"><span data-stu-id="09fb8-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09fb8-128"><strong>报告时间</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-128"><strong>Report time</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-129">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-129">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-130">记录报告的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="09fb8-130">Date and time that the report was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fb8-131"><strong>响应代码</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-131"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-132">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-132">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-133">会话失败时发送的 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="09fb8-133">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fb8-134"><strong>请求类型</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-134"><strong>Request type</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-135">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-135">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-p105">失败的 SIP 请求类型。例如，INVITE、BYE 或 SERVICE。</span><span class="sxs-lookup"><span data-stu-id="09fb8-p105">SIP request type that failed. For example, INVITE, BYE, or SERVICE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fb8-138"><strong>来源</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-138"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-139">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-139">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-140">错误的来源。</span><span class="sxs-lookup"><span data-stu-id="09fb8-140">Source of the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fb8-141"><strong>源用户 URI</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-141"><strong>From user URI</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-142">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-142">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-143">发起会话的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="09fb8-143">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fb8-144"><strong>源用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-144"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-145">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-145">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-146">发起会话的用户的终结点使用的软件。</span><span class="sxs-lookup"><span data-stu-id="09fb8-146">Software used by the endpoint of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fb8-147"><strong>诊断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-147"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-148">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-148">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-149">附加到 SIP 消息的唯一标识符（采用 ms-diagnostics 标头的形式），提供的信息在排查错误时通常很有帮助。</span><span class="sxs-lookup"><span data-stu-id="09fb8-149">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fb8-150"><strong>内容类型</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-150"><strong>Content type</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-151">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-151">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-p106">失败的媒体内容类型。例如，常见内容类型为 Application/sdp。会话描述协议 (SDP) 是用于会话公告、会话邀请及其他形式的多媒体会话启动的标准 Internet 协议。</span><span class="sxs-lookup"><span data-stu-id="09fb8-p106">Type of media content that failed. For example, a common content type is Application/sdp. Session Description Protocol (SDP) is a standard Internet protocol used for session announcements, session invitations, and other forms of multimedia session initiation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fb8-155"><strong>应用程序</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-155"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-156">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-156">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-157">错误涉及的应用程序。</span><span class="sxs-lookup"><span data-stu-id="09fb8-157">Application involved in the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fb8-158"><strong>目标用户 URI</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-158"><strong>To user URI</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-159">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-159">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-160">受邀加入会话的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="09fb8-160">SIP address of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fb8-161">会议加入时间（毫秒）</span><span class="sxs-lookup"><span data-stu-id="09fb8-161">Conference join times (ms)</span></span></p></td>
<td><p><span data-ttu-id="09fb8-162">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-162">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-163">用户加入会议所需的时间量（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="09fb8-163">Amount of time (in milliseconds) it took for the user to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fb8-164"><strong>诊断标头</strong></span><span class="sxs-lookup"><span data-stu-id="09fb8-164"><strong>Diagnostic header</strong></span></span></p></td>
<td><p><span data-ttu-id="09fb8-165">否</span><span class="sxs-lookup"><span data-stu-id="09fb8-165">No</span></span></p></td>
<td><p><span data-ttu-id="09fb8-166">诊断 ID 描述</span><span class="sxs-lookup"><span data-stu-id="09fb8-166">Diagnostic ID description.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09fb8-167">可以在 [Ms Diagnostics 标题页面](https://msdn.microsoft.com/library/gg132446\(v=office.12\).aspx)上找到诊断错误列表。</span><span class="sxs-lookup"><span data-stu-id="09fb8-167">A list of diagnostic errors can be found on the [Ms-Diagnostics Header page](https://msdn.microsoft.com/library/gg132446\(v=office.12\).aspx).</span></span>

<span data-ttu-id="09fb8-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09fb8-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

