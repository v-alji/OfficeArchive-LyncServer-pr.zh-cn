---
title: Lync Server 2013：MediaLine 表
description: Lync Server 2013： MediaLine 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine table
ms:assetid: 414b1d63-ae97-4c27-bac0-c9ad0f808ff0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425920(v=OCS.15)
ms:contentKeyID: 48183956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2acea8e14ba0608d9ebf72a48f888bfc4501fae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425617"
---
# <a name="medialine-table-in-lync-server-2013"></a><span data-ttu-id="1883b-103">Lync Server 2013 中的 MediaLine 表</span><span class="sxs-lookup"><span data-stu-id="1883b-103">MediaLine table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1883b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1883b-104">

<span> </span></span></span>

<span data-ttu-id="1883b-105">_**主题上次修改时间：** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="1883b-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="1883b-106">每条记录表示一个媒体行。</span><span class="sxs-lookup"><span data-stu-id="1883b-106">Each record represents one media line.</span></span> <span data-ttu-id="1883b-107"> (一个音频会话通常包含一个音频媒体行。</span><span class="sxs-lookup"><span data-stu-id="1883b-107">(One audio session usually contains one audio media line.</span></span> <span data-ttu-id="1883b-108">一个音频和视频 (A/V) 会话通常包含一个音频媒体线和一个视频媒体行，但如果使用了会议设备或使用了库视图，则该会话可能包含两个视频媒体线。</span><span class="sxs-lookup"><span data-stu-id="1883b-108">One audio and video (A/V) session usually contains one audio media line and one video media line, although the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1883b-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="1883b-110"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="1883b-111"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="1883b-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1883b-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-114">datetime</span><span class="sxs-lookup"><span data-stu-id="1883b-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="1883b-115">Primary</span><span class="sxs-lookup"><span data-stu-id="1883b-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="1883b-116">从 <a href="lync-server-2013-session-table.md">Lync Server 2013 中的会话表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-116">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-118">int</span><span class="sxs-lookup"><span data-stu-id="1883b-118">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-119">Primary</span><span class="sxs-lookup"><span data-stu-id="1883b-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="1883b-120">从 <a href="lync-server-2013-session-table.md">Lync Server 2013 中的会话表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-120">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-121"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-121"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-122">tinyint</span><span class="sxs-lookup"><span data-stu-id="1883b-122">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1883b-123">Primary</span><span class="sxs-lookup"><span data-stu-id="1883b-123">Primary</span></span></p></td>
<td><p><span data-ttu-id="1883b-124">0是主音频，1是主视频，2是全景视频，3是应用程序/桌面共享。</span><span class="sxs-lookup"><span data-stu-id="1883b-124">0 is main audio, 1 is main video, and 2 is panoramic video, 3 is Application/Desktop Sharing.</span></span> <span data-ttu-id="1883b-125">此标签在单个会话中必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="1883b-125">This label must be unique within a single session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-126"><strong>ConnectivityIce</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-126"><strong>ConnectivityIce</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-127">tinyint</span><span class="sxs-lookup"><span data-stu-id="1883b-127">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-128">此列存在，但未在 Microsoft Lync Server 2013 中使用。</span><span class="sxs-lookup"><span data-stu-id="1883b-128">This column is present but not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="1883b-129">在 "CallerConnectivityICE" 和 "CalleeConnectivityICE" 列中捕获有关用于媒体行的连接的信息。</span><span class="sxs-lookup"><span data-stu-id="1883b-129">Information about the connectivity used for a media line is captured in the CallerConnectivityICE and CalleeConnectivityICE columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-130"><strong>CallerIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-130"><strong>CallerIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-131">int</span><span class="sxs-lookup"><span data-stu-id="1883b-131">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-132">有关交互式连接建立 (ICE) 过程的信息在 bits 标志中描述。</span><span class="sxs-lookup"><span data-stu-id="1883b-132">Information about Interactive Connectivity Establishment (ICE) process described in bits flags.</span></span> <span data-ttu-id="1883b-133">有关详细信息，请参阅可供下载的 <em>体验质量监视服务器协议规范</em>。</span><span class="sxs-lookup"><span data-stu-id="1883b-133">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-134"><strong>CalleeIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-134"><strong>CalleeIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-135">int</span><span class="sxs-lookup"><span data-stu-id="1883b-135">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-136">与 CallerIceWarningFlags 相同，但在被调用方。</span><span class="sxs-lookup"><span data-stu-id="1883b-136">Same as CallerIceWarningFlags, but on the callee side.</span></span> <span data-ttu-id="1883b-137">有关详细信息，请参阅可供下载的 <em>体验质量监视服务器协议规范</em>。</span><span class="sxs-lookup"><span data-stu-id="1883b-137">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-138"><strong>安全性</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-138"><strong>Security</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-139">tinyint</span><span class="sxs-lookup"><span data-stu-id="1883b-139">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-140">正在使用的安全配置文件。</span><span class="sxs-lookup"><span data-stu-id="1883b-140">The security profile in use.</span></span> <span data-ttu-id="1883b-141">0为 NONE，1为 SRTP，2为 V1。</span><span class="sxs-lookup"><span data-stu-id="1883b-141">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-142"><strong>Transport</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-142"><strong>Transport</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-143">tinyint</span><span class="sxs-lookup"><span data-stu-id="1883b-143">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-144">0是 UDP，1是 TCP。</span><span class="sxs-lookup"><span data-stu-id="1883b-144">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-145"><strong>CallerIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-145"><strong>CallerIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-146">int</span><span class="sxs-lookup"><span data-stu-id="1883b-146">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-147">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-148">呼叫方的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-148">IP Address of the caller.</span></span> <span data-ttu-id="1883b-149">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="1883b-149">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-150"><strong>CallerPort</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-150"><strong>CallerPort</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-151">int</span><span class="sxs-lookup"><span data-stu-id="1883b-151">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-152">呼叫方使用的端口。</span><span class="sxs-lookup"><span data-stu-id="1883b-152">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-153"><strong>CallerSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-153"><strong>CallerSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-154">int</span><span class="sxs-lookup"><span data-stu-id="1883b-154">int</span></span></p></td>
<td><p> <span data-ttu-id="1883b-155">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-156">呼叫方的子网。</span><span class="sxs-lookup"><span data-stu-id="1883b-156">The subnet of the caller.</span></span> <span data-ttu-id="1883b-157">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="1883b-157">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-158"><strong>CallerInside</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-158"><strong>CallerInside</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-159">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-159">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-160">1表示呼叫方位于企业网络内，0表示呼叫方位于网络外部。</span><span class="sxs-lookup"><span data-stu-id="1883b-160">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-161"><strong>CallerMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-161"><strong>CallerMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-162">int</span><span class="sxs-lookup"><span data-stu-id="1883b-162">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-163">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-164">呼叫者的 mac 地址，从 <a href="lync-server-2013-macaddress-table.md">Lync Server 2013 中的 MacAddress 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-164">Caller’s mac address, referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-165"><strong>CallerRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-165"><strong>CallerRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-166">int</span><span class="sxs-lookup"><span data-stu-id="1883b-166">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-167">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-167">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-168">呼叫者使用的 Lync Server A/V 边缘服务的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-168">IP Address of the Lync Server A/V Edge service used by the caller.</span></span> <span data-ttu-id="1883b-169">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="1883b-169">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-170"><strong>CallerRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-170"><strong>CallerRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-171">int</span><span class="sxs-lookup"><span data-stu-id="1883b-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-172">由呼叫者在 A/V 边缘服务上使用的端口。</span><span class="sxs-lookup"><span data-stu-id="1883b-172">Port used on the A/V Edge service by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-173"><strong>CallerCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-173"><strong>CallerCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-174">int</span><span class="sxs-lookup"><span data-stu-id="1883b-174">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-175">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-176">由呼叫者使用的捕获设备。</span><span class="sxs-lookup"><span data-stu-id="1883b-176">Capture device used by the caller.</span></span> <span data-ttu-id="1883b-177">从 <a href="lync-server-2013-device-table.md">Lync Server 2013 中的设备表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-177">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-178"><strong>CallerRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-178"><strong>CallerRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-179">int</span><span class="sxs-lookup"><span data-stu-id="1883b-179">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-180">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-180">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-181">由呼叫者使用的渲染设备。</span><span class="sxs-lookup"><span data-stu-id="1883b-181">Render device used by caller.</span></span> <span data-ttu-id="1883b-182">从 <a href="lync-server-2013-device-table.md">Lync Server 2013 中的设备表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-182">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-183"><strong>CallerCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-183"><strong>CallerCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-184">int</span><span class="sxs-lookup"><span data-stu-id="1883b-184">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-185">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-186">呼叫者捕获设备的驱动程序，从 <a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 中的 DeviceDriver 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-186">Driver for the caller’s capture device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-187"><strong>CallerRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-187"><strong>CallerRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-188">int</span><span class="sxs-lookup"><span data-stu-id="1883b-188">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-189">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-189">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-190">呼叫者的呈现设备的驱动程序，从 <a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 中的 DeviceDriver 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-190">Driver for the caller’s render device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-191"><strong>CallerNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-191"><strong>CallerNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="1883b-192">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1883b-193">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-194">指示呼叫者如何连接到网络。</span><span class="sxs-lookup"><span data-stu-id="1883b-194">Indicates how the caller connected to the network.</span></span> <span data-ttu-id="1883b-195">从 <a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 中的 NetworkConnectionDetail 表中</a>获取值。</span><span class="sxs-lookup"><span data-stu-id="1883b-195">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="1883b-196">用于 WiFi 连接的有线连接 "1" 的典型值为 0;对于以太网连接，请使用3。</span><span class="sxs-lookup"><span data-stu-id="1883b-196">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-197"><strong>CallerBssid</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-197"><strong>CallerBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-198">int</span><span class="sxs-lookup"><span data-stu-id="1883b-198">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-199">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-200">呼叫者的 BSSID （如果使用无线）。</span><span class="sxs-lookup"><span data-stu-id="1883b-200">Caller’s BSSID if wireless is used.</span></span> <span data-ttu-id="1883b-201">从 <a href="lync-server-2013-macaddress-table.md">Lync Server 2013 中的 MacAddress 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-201">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-202"><strong>CallerVPN</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-202"><strong>CallerVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-203">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-203">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-204">呼叫者的链接。</span><span class="sxs-lookup"><span data-stu-id="1883b-204">The caller's link.</span></span> <span data-ttu-id="1883b-205">1是虚拟专用网 (VPN) ，0是非 VPN。</span><span class="sxs-lookup"><span data-stu-id="1883b-205">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-206"><strong>CallerLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-206"><strong>CallerLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-207">十进制 (18，0) </span><span class="sxs-lookup"><span data-stu-id="1883b-207">decimal(18,0)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-208">呼叫方终结点的网络链接速度（以 bps 为的）。</span><span class="sxs-lookup"><span data-stu-id="1883b-208">The network link speed, in bps, for the caller's endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-209"><strong>CalleeIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-209"><strong>CalleeIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-210">int</span><span class="sxs-lookup"><span data-stu-id="1883b-210">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-211">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-211">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-212">呼叫接收器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-212">IP Address of the call receiver.</span></span> <span data-ttu-id="1883b-213">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="1883b-213">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-214"><strong>CalleePort</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-214"><strong>CalleePort</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-215">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-216">呼叫接收器使用的端口。</span><span class="sxs-lookup"><span data-stu-id="1883b-216">Port used by the call receiver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-217"><strong>CalleeSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-217"><strong>CalleeSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-218">int</span><span class="sxs-lookup"><span data-stu-id="1883b-218">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-219">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-220">被调用的子网。</span><span class="sxs-lookup"><span data-stu-id="1883b-220">Subnet of callee.</span></span> <span data-ttu-id="1883b-221">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="1883b-221">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-222"><strong>CalleeInside</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-222"><strong>CalleeInside</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-223">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-224">1表示呼叫接收器位于企业网络内，0表示呼叫接收器位于网络外部。</span><span class="sxs-lookup"><span data-stu-id="1883b-224">1 means call receiver is inside the enterprise network, 0 means the call receiver is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-225"><strong>CalleeMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-225"><strong>CalleeMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-226">int</span><span class="sxs-lookup"><span data-stu-id="1883b-226">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-227">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-227">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-228">被呼叫方 Mac 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-228">Callee Mac address.</span></span> <span data-ttu-id="1883b-229">从 <a href="lync-server-2013-macaddress-table.md">Lync Server 2013 中的 MacAddress 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-229">Referenced from the <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-230"><strong>CalleeRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-230"><strong>CalleeRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-231">int</span><span class="sxs-lookup"><span data-stu-id="1883b-231">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-232">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-232">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-233">呼叫接收器使用的 A/V 边缘服务的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-233">IP Address of the A/V Edge service used by the call receiver.</span></span> <span data-ttu-id="1883b-234">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="1883b-234">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-235"><strong>CalleeRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-235"><strong>CalleeRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-236">int</span><span class="sxs-lookup"><span data-stu-id="1883b-236">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-237">由呼叫接收器在 A/V 边缘服务上使用的端口。</span><span class="sxs-lookup"><span data-stu-id="1883b-237">Port used on the A/V Edge Service by the call receiver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-238"><strong>CalleeCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-238"><strong>CalleeCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-239">int</span><span class="sxs-lookup"><span data-stu-id="1883b-239">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-240">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-240">foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-241">由呼叫接收器使用的捕获设备。</span><span class="sxs-lookup"><span data-stu-id="1883b-241">Capture device used by the call receiver.</span></span> <span data-ttu-id="1883b-242">从 <a href="lync-server-2013-device-table.md">Lync Server 2013 中的设备表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-242">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-243"><strong>CalleeRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-243"><strong>CalleeRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-244">int</span><span class="sxs-lookup"><span data-stu-id="1883b-244">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-245">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-245">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-246">由呼叫接收器使用的呈现设备。</span><span class="sxs-lookup"><span data-stu-id="1883b-246">Render device used by the call receiver.</span></span> <span data-ttu-id="1883b-247">从 <a href="lync-server-2013-device-table.md">Lync Server 2013 中的设备表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-247">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-248"><strong>CalleeCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-248"><strong>CalleeCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-249">int</span><span class="sxs-lookup"><span data-stu-id="1883b-249">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-250">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-250">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-251">呼叫接收器的捕获设备的驱动程序。</span><span class="sxs-lookup"><span data-stu-id="1883b-251">Driver for the call receiver’s capture device.</span></span> <span data-ttu-id="1883b-252">从 <a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 中的 DeviceDriver 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-252">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-253"><strong>CalleeRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-253"><strong>CalleeRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-254">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="1883b-254">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1883b-255">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-255">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-256">呼叫接收器的呈现设备的驱动程序。</span><span class="sxs-lookup"><span data-stu-id="1883b-256">Driver for the call receiver’s render device.</span></span> <span data-ttu-id="1883b-257">从 <a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 中的 DeviceDriver 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-257">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-258"><strong>CalleeNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-258"><strong>CalleeNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-259">tinyint</span><span class="sxs-lookup"><span data-stu-id="1883b-259">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1883b-260">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-260">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-261">指明被呼叫方如何连接到网络。</span><span class="sxs-lookup"><span data-stu-id="1883b-261">Indicates how the callee connected to the network.</span></span> <span data-ttu-id="1883b-262">从 <a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 中的 NetworkConnectionDetail 表中</a>获取值。</span><span class="sxs-lookup"><span data-stu-id="1883b-262">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="1883b-263">用于 WiFi 连接的有线连接 "1" 的典型值为 0;对于以太网连接，请使用3。</span><span class="sxs-lookup"><span data-stu-id="1883b-263">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-264"><strong>CalleeBssid</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-264"><strong>CalleeBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-265">int</span><span class="sxs-lookup"><span data-stu-id="1883b-265">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-266">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-266">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-267">如果使用无线，则被呼叫者的 BSSID。</span><span class="sxs-lookup"><span data-stu-id="1883b-267">Callee’s BSSID if wireless is used.</span></span> <span data-ttu-id="1883b-268">从 <a href="lync-server-2013-macaddress-table.md">Lync Server 2013 中的 MacAddress 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-268">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-269"><strong>CalleeVPN</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-269"><strong>CalleeVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-270">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-270">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-271">呼叫接收器的链接;1是虚拟专用网 (VPN) ，0是非 VPN。</span><span class="sxs-lookup"><span data-stu-id="1883b-271">The call receiver’s link; 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-272"><strong>CalleeLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-272"><strong>CalleeLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-273">十进制 (18，0) </span><span class="sxs-lookup"><span data-stu-id="1883b-273">decimal(18,0)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-274">呼叫接收器终结点的网络链接速度（以 bps 为 bps）。</span><span class="sxs-lookup"><span data-stu-id="1883b-274">The network link speed, in bps, for the call receiver’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-275"><strong>ConversationalMOS</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-275"><strong>ConversationalMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-276">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="1883b-276">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-277">Narrowband) 的音频 (会话的会话 MOS。</span><span class="sxs-lookup"><span data-stu-id="1883b-277">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-278"><strong>AppliedBandwidthLimit</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-278"><strong>AppliedBandwidthLimit</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-279">int</span><span class="sxs-lookup"><span data-stu-id="1883b-279">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-280">这是应用到给定发送端流的实际带宽，在给定各种策略设置 (转换、API、SDP、策略服务器等) 。</span><span class="sxs-lookup"><span data-stu-id="1883b-280">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="1883b-281">此操作不会与有效的带宽混淆，因为根据带宽估计，可能会有较低的有效带宽。</span><span class="sxs-lookup"><span data-stu-id="1883b-281">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="1883b-282">这基本上是发送流可以通过带宽估计限制限制的最大带宽。</span><span class="sxs-lookup"><span data-stu-id="1883b-282">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-283"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-283"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-284">smallint</span><span class="sxs-lookup"><span data-stu-id="1883b-284">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-285">这是所强加的带宽上限的来源。</span><span class="sxs-lookup"><span data-stu-id="1883b-285">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="1883b-286">它介绍带宽限制来自 ( "策略服务器"、"打开服务器"、"模态" 等) 。</span><span class="sxs-lookup"><span data-stu-id="1883b-286">It describes where the bandwidth limit is coming from (“Policy Server”, “TURN Server”, “Modality”, and so on).</span></span> <span data-ttu-id="1883b-287">从 <a href="lync-server-2013-appliedbandwidthsource-table.md">Lync Server 2013 中的 AppliedBandwidthSource 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="1883b-287">Referenced from the <a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-288"><strong>呼叫者</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-288"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-289">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-289">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-290">指示是否收到来自呼叫方的指标;1为 "是"，null 值为 "否"。</span><span class="sxs-lookup"><span data-stu-id="1883b-290">Indicates whether metrics from the caller were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-291"><strong>被叫方</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-291"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-292">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-292">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1883b-293">指示是否收到来自呼叫接收器的指标;1为 "是"，null 值为 "否"。</span><span class="sxs-lookup"><span data-stu-id="1883b-293">Indicates whether metrics from the call receiver were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-294"><strong>MidCallReport</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-294"><strong>MidCallReport</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-295">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-295">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-296">指示报表是用于会话的一部分还是整个会话。</span><span class="sxs-lookup"><span data-stu-id="1883b-296">Indicates whether the report is for a portion of the session or for the complete session.</span></span></p>
<p><span data-ttu-id="1883b-297">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-297">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-298"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-298"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-299">bit</span><span class="sxs-lookup"><span data-stu-id="1883b-299">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-300">指明呼叫是否分类为不太好的通话 (值为 1) 或 (0) 的良好通话。</span><span class="sxs-lookup"><span data-stu-id="1883b-300">Indicates whether a call was classified as a poor call (value of 1) or as a good call (0).</span></span></p>
<p><span data-ttu-id="1883b-301">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-302"><strong>CallerConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-302"><strong>CallerConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-303">tinyInt</span><span class="sxs-lookup"><span data-stu-id="1883b-303">tinyInt</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-304">指示呼叫者是否使用 ICE 协议连接到网络 (Internet 连接建立) 。</span><span class="sxs-lookup"><span data-stu-id="1883b-304">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="1883b-305">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-305">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-306"><strong>CalleeConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-306"><strong>CalleeConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-307">tinyint</span><span class="sxs-lookup"><span data-stu-id="1883b-307">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1883b-308">指示呼叫者是否使用 ICE 协议连接到网络 (Internet 连接建立) 。</span><span class="sxs-lookup"><span data-stu-id="1883b-308">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="1883b-309">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-309">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-310"><strong>CallerReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-310"><strong>CallerReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-311">int</span><span class="sxs-lookup"><span data-stu-id="1883b-311">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-312">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-312">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-313">发出呼叫的用户的自身 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-313">Reflexive IP address of the user who placed the call.</span></span> <span data-ttu-id="1883b-314">在使用 NAT (网络地址转换) 的组织中，自身 IP 地址是代理服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-314">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="1883b-315">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-315">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-316"><strong>CallerWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-316"><strong>CallerWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-317">int</span><span class="sxs-lookup"><span data-stu-id="1883b-317">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-318">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-318">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-319">发出呼叫的用户所使用的 WiFi 驱动程序的设备说明。</span><span class="sxs-lookup"><span data-stu-id="1883b-319">Device description for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="1883b-320">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-321"><strong>CallerWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-321"><strong>CallerWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-322">int</span><span class="sxs-lookup"><span data-stu-id="1883b-322">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-323">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-323">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-324">发出呼叫的用户所使用的 WiFi 驱动程序的版本号。</span><span class="sxs-lookup"><span data-stu-id="1883b-324">Version number for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="1883b-325">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-326"><strong>CalleReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-326"><strong>CalleReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-327">int</span><span class="sxs-lookup"><span data-stu-id="1883b-327">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-328">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-328">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-329">接收呼叫的用户的自身 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-329">Reflexive IP address of the user who received the call.</span></span> <span data-ttu-id="1883b-330">在使用 NAT (网络地址转换) 的组织中，自身 IP 地址是代理服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1883b-330">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="1883b-331">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1883b-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-333">int</span><span class="sxs-lookup"><span data-stu-id="1883b-333">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-334">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-334">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-335">接收呼叫的用户所使用的 WiFi 驱动程序的设备说明。</span><span class="sxs-lookup"><span data-stu-id="1883b-335">Device description for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="1883b-336">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-336">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1883b-337"><strong>CalleeWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="1883b-337"><strong>CalleeWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="1883b-338">int</span><span class="sxs-lookup"><span data-stu-id="1883b-338">int</span></span></p></td>
<td><p><span data-ttu-id="1883b-339">外表</span><span class="sxs-lookup"><span data-stu-id="1883b-339">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1883b-340">接收呼叫的用户所使用的 WiFi 驱动程序的版本号。</span><span class="sxs-lookup"><span data-stu-id="1883b-340">Version number for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="1883b-341">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="1883b-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1883b-342">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1883b-342">


</div>

<span> </span>

</div>

</div>

</span></span></div>

