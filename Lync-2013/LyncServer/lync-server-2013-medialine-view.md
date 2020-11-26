---
title: Lync Server 2013： MediaLine 视图
description: Lync Server 2013： MediaLine 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine view
ms:assetid: 132eca13-8913-4218-9eff-4960ced8c3dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687972(v=OCS.15)
ms:contentKeyID: 49733560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c61fcc15b46958622e6cddd66427255a6def154
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445944"
---
# <a name="medialine-view-in-lync-server-2013"></a><span data-ttu-id="311ff-103">Lync Server 2013 中的 MediaLine 视图</span><span class="sxs-lookup"><span data-stu-id="311ff-103">MediaLine view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="311ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="311ff-104">

<span> </span></span></span>

<span data-ttu-id="311ff-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="311ff-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="311ff-106">MediaLine 视图存储有关数据库中每个媒体行的信息。</span><span class="sxs-lookup"><span data-stu-id="311ff-106">The MediaLine View stores information about each media line in the database.</span></span> <span data-ttu-id="311ff-107">一个音频会话通常包含一个音频媒体行。</span><span class="sxs-lookup"><span data-stu-id="311ff-107">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="311ff-108">一个音频和视频 (A/V) 会话通常包含一个音频媒体线和一个视频媒体线;但是，如果使用了会议设备或使用了库视图，则会话可能包含两个视频媒体线。</span><span class="sxs-lookup"><span data-stu-id="311ff-108">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span> <span data-ttu-id="311ff-109">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="311ff-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="311ff-110">列</span><span class="sxs-lookup"><span data-stu-id="311ff-110">Column</span></span></th>
<th><span data-ttu-id="311ff-111">数据类型</span><span class="sxs-lookup"><span data-stu-id="311ff-111">Data Type</span></span></th>
<th><span data-ttu-id="311ff-112">更多信息</span><span class="sxs-lookup"><span data-stu-id="311ff-112">details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="311ff-113">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="311ff-113">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="311ff-114">datetime</span><span class="sxs-lookup"><span data-stu-id="311ff-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="311ff-115">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="311ff-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-116">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="311ff-116">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="311ff-117">int</span><span class="sxs-lookup"><span data-stu-id="311ff-117">int</span></span></p></td>
<td><p><span data-ttu-id="311ff-118">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="311ff-118">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-119">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="311ff-119">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="311ff-120">tinyint</span><span class="sxs-lookup"><span data-stu-id="311ff-120">tinyint</span></span></p></td>
<td><p><span data-ttu-id="311ff-121">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="311ff-121">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-122">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="311ff-122">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="311ff-123">int</span><span class="sxs-lookup"><span data-stu-id="311ff-123">int</span></span></p></td>
<td><p><span data-ttu-id="311ff-124">有关交互式连接的信息 (冰) 过程（在调用方的位标志中描述）。</span><span class="sxs-lookup"><span data-stu-id="311ff-124">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="311ff-125">有关详细信息，请参阅体验质量监视服务器协议规范。</span><span class="sxs-lookup"><span data-stu-id="311ff-125">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-126">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="311ff-126">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="311ff-127">int</span><span class="sxs-lookup"><span data-stu-id="311ff-127">int</span></span></p></td>
<td><p><span data-ttu-id="311ff-128">有关交互式连接的信息 (冰) 进程（在被呼叫方的位标志中描述）。</span><span class="sxs-lookup"><span data-stu-id="311ff-128">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="311ff-129">有关详细信息，请参阅体验质量监视服务器协议规范。</span><span class="sxs-lookup"><span data-stu-id="311ff-129">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-130">安全性</span><span class="sxs-lookup"><span data-stu-id="311ff-130">Security</span></span></p></td>
<td><p><span data-ttu-id="311ff-131">tinyint</span><span class="sxs-lookup"><span data-stu-id="311ff-131">tinyint</span></span></p></td>
<td><p><span data-ttu-id="311ff-132">安全配置文件正在使用。</span><span class="sxs-lookup"><span data-stu-id="311ff-132">Security profile in use.</span></span> <span data-ttu-id="311ff-133">0为 NONE，1为 SRTP，2为 V1。</span><span class="sxs-lookup"><span data-stu-id="311ff-133">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-134">Transport</span><span class="sxs-lookup"><span data-stu-id="311ff-134">Transport</span></span></p></td>
<td><p><span data-ttu-id="311ff-135">tinyint</span><span class="sxs-lookup"><span data-stu-id="311ff-135">tinyint</span></span></p></td>
<td><p><span data-ttu-id="311ff-136">传输类型。</span><span class="sxs-lookup"><span data-stu-id="311ff-136">Transport type.</span></span> <span data-ttu-id="311ff-137">0是 UDP，1是 TCP。</span><span class="sxs-lookup"><span data-stu-id="311ff-137">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-138">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="311ff-138">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="311ff-139">var (50) </span><span class="sxs-lookup"><span data-stu-id="311ff-139">var(50)</span></span></p></td>
<td><p><span data-ttu-id="311ff-140">呼叫方的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-140">IP address of the caller.</span></span> <span data-ttu-id="311ff-141">这可以是 IPv4 地址或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-141">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-142">CallerPort</span><span class="sxs-lookup"><span data-stu-id="311ff-142">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="311ff-143">int</span><span class="sxs-lookup"><span data-stu-id="311ff-143">int</span></span></p></td>
<td><p><span data-ttu-id="311ff-144">呼叫方使用的端口。</span><span class="sxs-lookup"><span data-stu-id="311ff-144">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-145">CallerInside</span><span class="sxs-lookup"><span data-stu-id="311ff-145">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="311ff-146">bit</span><span class="sxs-lookup"><span data-stu-id="311ff-146">bit</span></span></p></td>
<td><p><span data-ttu-id="311ff-147">指示呼叫者是否在组织网络内。</span><span class="sxs-lookup"><span data-stu-id="311ff-147">Indicates whether or not the caller is inside the organization network.</span></span> <span data-ttu-id="311ff-148">1表示呼叫方位于企业网络内。</span><span class="sxs-lookup"><span data-stu-id="311ff-148">1 means that the caller is inside the enterprise network.</span></span> <span data-ttu-id="311ff-149">0表示呼叫方位于网络外部。</span><span class="sxs-lookup"><span data-stu-id="311ff-149">0 means that the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-150">CallerMacAddress</span><span class="sxs-lookup"><span data-stu-id="311ff-150">CallerMacAddress</span></span></p></td>
<td><p><span data-ttu-id="311ff-151">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-151">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-152">呼叫方使用的网络接口的 MAC 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-152">MAC address of network interface used by caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-153">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="311ff-153">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="311ff-154">var (50) </span><span class="sxs-lookup"><span data-stu-id="311ff-154">var(50)</span></span></p></td>
<td><p><span data-ttu-id="311ff-155">呼叫方使用的 A/V 边缘服务的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-155">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="311ff-156">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="311ff-156">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-157">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="311ff-157">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="311ff-158">int</span><span class="sxs-lookup"><span data-stu-id="311ff-158">int</span></span></p></td>
<td><p><span data-ttu-id="311ff-159">由呼叫方使用的 A/V 边缘服务使用的端口。</span><span class="sxs-lookup"><span data-stu-id="311ff-159">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-160">CallerReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="311ff-160">CallerReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="311ff-161">var (50) </span><span class="sxs-lookup"><span data-stu-id="311ff-161">var(50)</span></span></p></td>
<td><p><span data-ttu-id="311ff-162">由 A/V 边缘服务报告的呼叫者的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-162">Caller’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="311ff-163">如果客户端位于 NAT 后面，则该地址可能与 CallerIPAddr 不同，例如。</span><span class="sxs-lookup"><span data-stu-id="311ff-163">This address may be different that the CallerIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-164">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="311ff-164">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="311ff-165">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-165">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-166">呼叫方的捕获设备名称。</span><span class="sxs-lookup"><span data-stu-id="311ff-166">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-167">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="311ff-167">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="311ff-168">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-168">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-169">调用方的呈现设备名称。</span><span class="sxs-lookup"><span data-stu-id="311ff-169">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-170">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="311ff-170">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="311ff-171">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-171">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-172">呼叫方的捕获设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="311ff-172">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-173">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="311ff-173">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="311ff-174">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-174">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-175">呼叫方的呈现设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="311ff-175">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-176">CallerWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="311ff-176">CallerWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="311ff-177">varchar (256</span><span class="sxs-lookup"><span data-stu-id="311ff-177">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="311ff-178">呼叫方的 Wifi 驱动程序说明。</span><span class="sxs-lookup"><span data-stu-id="311ff-178">Caller’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-179">CallerWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="311ff-179">CallerWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="311ff-180">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-180">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-181">呼叫方的 Wifi 驱动程序版本。</span><span class="sxs-lookup"><span data-stu-id="311ff-181">Caller’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-182">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="311ff-182">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="311ff-183">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-183">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-184">呼叫方网络连接的详细信息。</span><span class="sxs-lookup"><span data-stu-id="311ff-184">Details of caller’s network connection.</span></span> <span data-ttu-id="311ff-185">有关详细信息，请参阅 <a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 中的 NetworkConnectionDetail 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="311ff-185">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-186">CallerBssid</span><span class="sxs-lookup"><span data-stu-id="311ff-186">CallerBssid</span></span></p></td>
<td><p><span data-ttu-id="311ff-187">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-187">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-188">呼叫方 WiFi 连接使用的基本服务设置标识符。</span><span class="sxs-lookup"><span data-stu-id="311ff-188">Basic Service Set Identifier used by callers WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-189">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="311ff-189">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="311ff-190">bit</span><span class="sxs-lookup"><span data-stu-id="311ff-190">bit</span></span></p></td>
<td><p><span data-ttu-id="311ff-191">指示呼叫者是否通过虚拟专用网络连接。</span><span class="sxs-lookup"><span data-stu-id="311ff-191">Indicates whether the caller connected over a virtual private network.</span></span> <span data-ttu-id="311ff-192">1是虚拟专用网 (VPN) ，0是非 VPN。</span><span class="sxs-lookup"><span data-stu-id="311ff-192">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-193">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="311ff-193">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="311ff-194">var (50) </span><span class="sxs-lookup"><span data-stu-id="311ff-194">var(50)</span></span></p></td>
<td><p><span data-ttu-id="311ff-195">被呼叫方的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-195">IP address of the callee.</span></span> <span data-ttu-id="311ff-196">这可以是 IPv4 地址或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-196">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-197">CalleePort</span><span class="sxs-lookup"><span data-stu-id="311ff-197">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="311ff-198">int</span><span class="sxs-lookup"><span data-stu-id="311ff-198">int</span></span></p></td>
<td><p><span data-ttu-id="311ff-199">被呼叫方使用的端口。</span><span class="sxs-lookup"><span data-stu-id="311ff-199">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-200">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="311ff-200">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="311ff-201">bit</span><span class="sxs-lookup"><span data-stu-id="311ff-201">bit</span></span></p></td>
<td><p><span data-ttu-id="311ff-202">指示被调用方是否位于企业网络内。</span><span class="sxs-lookup"><span data-stu-id="311ff-202">Indicates whether the callee is inside the enterprise network.</span></span> <span data-ttu-id="311ff-203">1表示被呼叫方位于企业网络内，0表示被呼叫方位于网络外部。</span><span class="sxs-lookup"><span data-stu-id="311ff-203">1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-204">CalleeMacAddress</span><span class="sxs-lookup"><span data-stu-id="311ff-204">CalleeMacAddress</span></span></p></td>
<td><p><span data-ttu-id="311ff-205">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-205">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-206">被呼叫方使用的网络接口的 MAC 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-206">MAC address of network interface used by callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-207">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="311ff-207">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="311ff-208">var (50) </span><span class="sxs-lookup"><span data-stu-id="311ff-208">var(50)</span></span></p></td>
<td><p><span data-ttu-id="311ff-209">被呼叫方使用的 A/V 边缘服务的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-209">IP Address of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="311ff-210">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="311ff-210">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-211">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="311ff-211">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="311ff-212">int</span><span class="sxs-lookup"><span data-stu-id="311ff-212">int</span></span></p></td>
<td><p><span data-ttu-id="311ff-213">用于由被呼叫方使用的 A/V 边缘服务的端口。</span><span class="sxs-lookup"><span data-stu-id="311ff-213">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-214">CalleeReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="311ff-214">CalleeReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="311ff-215">var (50) </span><span class="sxs-lookup"><span data-stu-id="311ff-215">var(50)</span></span></p></td>
<td><p><span data-ttu-id="311ff-216">由 A/V 边缘服务报告的被呼叫方的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="311ff-216">Callee’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="311ff-217">如果客户端位于 NAT 后面，则该地址可能与 CalleeIPAddr 不同，例如。</span><span class="sxs-lookup"><span data-stu-id="311ff-217">This address may be different that the CalleeIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-218">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="311ff-218">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="311ff-219">var (50) </span><span class="sxs-lookup"><span data-stu-id="311ff-219">var(50)</span></span></p></td>
<td><p><span data-ttu-id="311ff-220">被调用方的捕获设备名称。</span><span class="sxs-lookup"><span data-stu-id="311ff-220">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-221">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="311ff-221">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="311ff-222">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-222">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-223">被调用方的呈现设备名称。</span><span class="sxs-lookup"><span data-stu-id="311ff-223">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-224">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="311ff-224">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="311ff-225">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-225">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-226">被调用方的捕获设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="311ff-226">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-227">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="311ff-227">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="311ff-228">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-228">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-229">被调用方的呈现设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="311ff-229">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-230">CalleeWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="311ff-230">CalleeWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="311ff-231">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-231">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-232">被呼叫方的 Wifi 驱动程序说明。</span><span class="sxs-lookup"><span data-stu-id="311ff-232">Callee’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-233">CalleeWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="311ff-233">CalleeWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="311ff-234">varchar (256</span><span class="sxs-lookup"><span data-stu-id="311ff-234">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="311ff-235">被呼叫方的 Wifi 驱动程序版本。</span><span class="sxs-lookup"><span data-stu-id="311ff-235">Callee’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-236">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="311ff-236">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="311ff-237">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-237">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-238">被呼叫方的网络连接的详细信息。</span><span class="sxs-lookup"><span data-stu-id="311ff-238">Details of callee’s network connection.</span></span> <span data-ttu-id="311ff-239">有关详细信息，请参阅 <a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 中的 NetworkConnectionDetail 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="311ff-239">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-240">CalleeBssid</span><span class="sxs-lookup"><span data-stu-id="311ff-240">CalleeBssid</span></span></p></td>
<td><p><span data-ttu-id="311ff-241">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-241">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-242">被呼叫方的 WiFi 连接使用的基本服务设置标识符。</span><span class="sxs-lookup"><span data-stu-id="311ff-242">Basic Service Set Identifier used by callee’s WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-243">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="311ff-243">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="311ff-244">bit</span><span class="sxs-lookup"><span data-stu-id="311ff-244">bit</span></span></p></td>
<td><p><span data-ttu-id="311ff-245">指示被调用方是否通过虚拟专用网络进行连接。</span><span class="sxs-lookup"><span data-stu-id="311ff-245">Indicates whether the callee connected over a virtual private network.</span></span> <span data-ttu-id="311ff-246">1是虚拟专用网 (VPN) ，0是非 VPN。</span><span class="sxs-lookup"><span data-stu-id="311ff-246">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-247">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="311ff-247">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="311ff-248">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="311ff-248">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="311ff-249">Narrowband) 的音频 (会话的会话 MOS。</span><span class="sxs-lookup"><span data-stu-id="311ff-249">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-250">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="311ff-250">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="311ff-251">int</span><span class="sxs-lookup"><span data-stu-id="311ff-251">int</span></span></p></td>
<td><p><span data-ttu-id="311ff-252">这是应用到给定发送端流的实际带宽，这些带宽应用到 (转换、API、SDP、策略服务器等各种策略设置 ) 。</span><span class="sxs-lookup"><span data-stu-id="311ff-252">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, etc.).</span></span> <span data-ttu-id="311ff-253">不要将这一点与有效的带宽混淆，因为它可以根据带宽估计值降低较低的有效带宽。</span><span class="sxs-lookup"><span data-stu-id="311ff-253">This should not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="311ff-254">这基本上是发送流可以通过带宽估计限制限制的最大带宽。</span><span class="sxs-lookup"><span data-stu-id="311ff-254">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-255">AppliedBandwidthSource</span><span class="sxs-lookup"><span data-stu-id="311ff-255">AppliedBandwidthSource</span></span></p></td>
<td><p><span data-ttu-id="311ff-256">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="311ff-256">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="311ff-257">所强加带宽上限的来源。</span><span class="sxs-lookup"><span data-stu-id="311ff-257">Source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="311ff-258">它介绍了带宽 (限制的来源，例如 "策略服务器"、"打开服务器" 或 "模态" ) 。</span><span class="sxs-lookup"><span data-stu-id="311ff-258">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-259">呼叫者</span><span class="sxs-lookup"><span data-stu-id="311ff-259">Caller</span></span></p></td>
<td><p><span data-ttu-id="311ff-260">bit</span><span class="sxs-lookup"><span data-stu-id="311ff-260">bit</span></span></p></td>
<td><p><span data-ttu-id="311ff-261">指示是否收到来自呼叫方的指标;1为 "是"，0为 "否"。</span><span class="sxs-lookup"><span data-stu-id="311ff-261">Indicates whether metrics from the caller were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-262">被叫方</span><span class="sxs-lookup"><span data-stu-id="311ff-262">Callee</span></span></p></td>
<td><p><span data-ttu-id="311ff-263">bit</span><span class="sxs-lookup"><span data-stu-id="311ff-263">bit</span></span></p></td>
<td><p><span data-ttu-id="311ff-264">指示是否收到来自呼叫接收器的指标;1为 "是"，0为 "否"。</span><span class="sxs-lookup"><span data-stu-id="311ff-264">Indicates whether metrics from the call receiver were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-265">MidCallReport</span><span class="sxs-lookup"><span data-stu-id="311ff-265">MidCallReport</span></span></p></td>
<td><p><span data-ttu-id="311ff-266">bit</span><span class="sxs-lookup"><span data-stu-id="311ff-266">bit</span></span></p></td>
<td><p><span data-ttu-id="311ff-267">指示报表是用于部分通话还是完整通话。</span><span class="sxs-lookup"><span data-stu-id="311ff-267">Indicates whether the report is for a portion of the call or for the complete call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-268">ClassifiedPoorCall</span><span class="sxs-lookup"><span data-stu-id="311ff-268">ClassifiedPoorCall</span></span></p></td>
<td><p><span data-ttu-id="311ff-269">bit</span><span class="sxs-lookup"><span data-stu-id="311ff-269">bit</span></span></p></td>
<td><p><span data-ttu-id="311ff-270">指示呼叫是否归为差通话 (1) 或 (0) 的良好通话。</span><span class="sxs-lookup"><span data-stu-id="311ff-270">Indicates whether a call was classified as a poor call (1) or as a good call (0).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="311ff-271">CallerConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="311ff-271">CallerConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="311ff-272">tinyint</span><span class="sxs-lookup"><span data-stu-id="311ff-272">tinyint</span></span></p></td>
<td><p><span data-ttu-id="311ff-273">指示呼叫者是否使用 ICE 协议连接到网络 (Internet 连接建立) 。</span><span class="sxs-lookup"><span data-stu-id="311ff-273">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="311ff-274">CalleeConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="311ff-274">CalleeConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="311ff-275">tinyint</span><span class="sxs-lookup"><span data-stu-id="311ff-275">tinyint</span></span></p></td>
<td><p><span data-ttu-id="311ff-276">指示用户使用 ICE 协议连接到网络的用户是否 (Internet 连接建立) 。</span><span class="sxs-lookup"><span data-stu-id="311ff-276">Indicates whether the user called connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="311ff-277">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="311ff-277">


</div>

<span> </span>

</div>

</div>

</span></span></div>

