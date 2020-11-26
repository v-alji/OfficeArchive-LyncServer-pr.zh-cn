---
title: Lync Server 2013：IP 地址类型概述
description: Lync Server 2013： IP 地址类型概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of IP address types for Lync Server
ms:assetid: ee9a695f-5cf5-441e-94fb-6adeca50e8d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205363(v=OCS.15)
ms:contentKeyID: 48185759
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81492b2e006a6f44f6deb78e6a0560f6e319992f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445132"
---
# <a name="overview-of-ip-address-types-for-lync-server-2013"></a><span data-ttu-id="f1c72-103">Lync Server 2013 的 IP 地址类型概述</span><span class="sxs-lookup"><span data-stu-id="f1c72-103">Overview of IP address types for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1c72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1c72-104">

<span> </span></span></span>

<span data-ttu-id="f1c72-105">_**主题上次修改时间：** 2013-01-29_</span><span class="sxs-lookup"><span data-stu-id="f1c72-105">_**Topic Last Modified:** 2013-01-29_</span></span>

<span data-ttu-id="f1c72-106">在 Lync Server 2013 中配置 IP 地址时，有三个选项。</span><span class="sxs-lookup"><span data-stu-id="f1c72-106">You have three options when configuring IP addresses in Lync Server 2013.</span></span> <span data-ttu-id="f1c72-107">你可以将 Lync Server 2013 配置为仅支持 (IPv4) 的 IP 版本4、仅支持 IP 版本 6 (IPv6) ，或者仅支持 (两个) *堆栈* 的 ip 版本6。</span><span class="sxs-lookup"><span data-stu-id="f1c72-107">You can configure Lync Server 2013 to support only IP version 4 (IPv4), only IP version 6 (IPv6), or a combination of both (known as a *dual stack*).</span></span> <span data-ttu-id="f1c72-108">对于每种类型的配置，都需要考虑一些问题：</span><span class="sxs-lookup"><span data-stu-id="f1c72-108">There are several issues to consider with each type of configuration:</span></span>

  - <span data-ttu-id="f1c72-109">**仅限 IPv4**   由于全球 IPv4 地址不足，因此已创建 IPv6。</span><span class="sxs-lookup"><span data-stu-id="f1c72-109">**IPv4 only**   IPv6 was created because the world is running out of IPv4 addresses.</span></span> <span data-ttu-id="f1c72-110">最终，IPv6 将在全球范围内获得全面支持，但就目前而言，您的企业需要与之通信的很多公司和设备可能尚不支持 IPv6，并且在一段时间内可能也不会提供相应支持。</span><span class="sxs-lookup"><span data-stu-id="f1c72-110">Ultimately, IPv6 will be fully supported worldwide, but at this time, many companies and devices that your enterprise might need to communicate with do not yet support IPv6, and may not for some time.</span></span> <span data-ttu-id="f1c72-111">仅 IPv4 配置将有助于确保 Lync 服务器实现可以与大多数现有设备进行通信。</span><span class="sxs-lookup"><span data-stu-id="f1c72-111">An IPv4-only configuration will help to ensure that your Lync Server implementation can communicate with most existing devices.</span></span>

  - <span data-ttu-id="f1c72-112">**仅限 IPv6**   相反，完全 IPv6 实现此时将排除与许多现有设备的通信。</span><span class="sxs-lookup"><span data-stu-id="f1c72-112">**IPv6 only**   Conversely, a full IPv6 implementation, at this time, will exclude communication with many existing devices.</span></span>

  - <span data-ttu-id="f1c72-113">**双栈**   双堆栈是启用 IPv4 和 IPv6 地址的网络。</span><span class="sxs-lookup"><span data-stu-id="f1c72-113">**Dual Stack**   Dual stack is a network where both IPv4 and IPv6 addresses are enabled.</span></span> <span data-ttu-id="f1c72-114">Lync Server 2013 支持此配置，因为在大多数情况下，从完整 IPv4 到完整 IPv6 的转换将需要几年。</span><span class="sxs-lookup"><span data-stu-id="f1c72-114">This configuration is supported in Lync Server 2013 because in most cases the transition from full-IPv4 to full-IPv6 will take several years.</span></span>

<span data-ttu-id="f1c72-115">以下部分概述了各种 Lync Server 功能的这三种配置之间的兼容性。</span><span class="sxs-lookup"><span data-stu-id="f1c72-115">The following sections outline the compatibility among these three configurations for various Lync Server features.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f1c72-p104">仅 IPv6 的客户端或服务器配置只受选项卡或验证的支持。仅 IPv6 配置在生产部署中不受支持。</span><span class="sxs-lookup"><span data-stu-id="f1c72-p104">Client or server configuration with IPv6 only is supported only for lab or validation purposes. IPv6 only configuration is not supported in the production deployment.</span></span>



</div>

<div>

## <a name="client-registration"></a><span data-ttu-id="f1c72-118">客户端注册</span><span class="sxs-lookup"><span data-stu-id="f1c72-118">Client Registration</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1c72-119">客户端终结点网络</span><span class="sxs-lookup"><span data-stu-id="f1c72-119">Client endpoint network</span></span></th>
<th><span data-ttu-id="f1c72-120">服务器网络</span><span class="sxs-lookup"><span data-stu-id="f1c72-120">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-121">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-121">IPv4</span></span></p></td>
<td><p><span data-ttu-id="f1c72-122">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-122">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-123">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-123">IPv4</span></span></p></td>
<td><p><span data-ttu-id="f1c72-124">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-124">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-125">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-125">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-126">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-126">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-127">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-127">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-128">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-128">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-129">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-129">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-130">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-130">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-131">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-131">IPv6</span></span></p></td>
<td><p><span data-ttu-id="f1c72-132">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-132">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-133">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-133">IPv6</span></span></p></td>
<td><p><span data-ttu-id="f1c72-134">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-134">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="peer-to-peer-client"></a><span data-ttu-id="f1c72-135">对等客户端</span><span class="sxs-lookup"><span data-stu-id="f1c72-135">Peer-to-Peer Client</span></span>

<span data-ttu-id="f1c72-p105">对等通信包括音频、音频/视频、应用程序共享和文件传输。两个客户端均注册成功后，将支持以下组合。</span><span class="sxs-lookup"><span data-stu-id="f1c72-p105">Peer-to-peer communications include audio, audio/video, application sharing, and file transfer. After both clients have successfully registered, the following combinations are supported.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1c72-138">客户端终结点 1</span><span class="sxs-lookup"><span data-stu-id="f1c72-138">Client endpoint 1</span></span></th>
<th><span data-ttu-id="f1c72-139">客户端终结点 2</span><span class="sxs-lookup"><span data-stu-id="f1c72-139">Client endpoint 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-140">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-140">IPv4</span></span></p></td>
<td><p><span data-ttu-id="f1c72-141">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-141">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-142">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-142">IPv4</span></span></p></td>
<td><p><span data-ttu-id="f1c72-143">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-143">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-144">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-144">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-145">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-145">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-146">IPv6</span></span></p></td>
<td><p><span data-ttu-id="f1c72-147">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-147">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-148">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-148">IPv6</span></span></p></td>
<td><p><span data-ttu-id="f1c72-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-149">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="conferencing"></a><span data-ttu-id="f1c72-150">会议</span><span class="sxs-lookup"><span data-stu-id="f1c72-150">Conferencing</span></span>

<span data-ttu-id="f1c72-151">会议包括音频/视频、应用程序共享和数据协作 (whiteboarding 和文件共享) 。</span><span class="sxs-lookup"><span data-stu-id="f1c72-151">Conferencing includes audio/video, application sharing, and data collaboration (whiteboarding and file sharing).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1c72-152">客户端终结点网络</span><span class="sxs-lookup"><span data-stu-id="f1c72-152">Client endpoint network</span></span></th>
<th><span data-ttu-id="f1c72-153">服务器网络</span><span class="sxs-lookup"><span data-stu-id="f1c72-153">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-154">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-154">IPv4</span></span></p></td>
<td><p><span data-ttu-id="f1c72-155">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-155">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-156">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-156">IPv4</span></span></p></td>
<td><p><span data-ttu-id="f1c72-157">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-157">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-158">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-158">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-159">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-159">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-160">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-160">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-161">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-161">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-162">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-162">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-163">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-163">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-164">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-164">IPv6</span></span></p></td>
<td><p><span data-ttu-id="f1c72-165">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-165">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-166">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-166">IPv6</span></span></p></td>
<td><p><span data-ttu-id="f1c72-167">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-167">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="mediation-serverpstn"></a><span data-ttu-id="f1c72-168">中介服务器/PSTN</span><span class="sxs-lookup"><span data-stu-id="f1c72-168">Mediation Server/PSTN</span></span>

<span data-ttu-id="f1c72-169">如果通信通过 IPv6 接口，则 Lync Server 2013 不支持公共交换电话网络 (PSTN) 呼叫的媒体旁路。</span><span class="sxs-lookup"><span data-stu-id="f1c72-169">Lync Server 2013 does not support media bypass for public switched telephone network (PSTN) calls if the traffic is through an IPv6 interface.</span></span> <span data-ttu-id="f1c72-170">如果需要媒体旁路，则我们建议将 PSTN 网关配置为 IPv4。</span><span class="sxs-lookup"><span data-stu-id="f1c72-170">If media bypass is required, we recommend that the PSTN gateway is configured to IPv4.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1c72-171">主要接口\*</span><span class="sxs-lookup"><span data-stu-id="f1c72-171">Primary interface\*</span></span></th>
<th><span data-ttu-id="f1c72-172">PSTN 接口（位于中介服务器上）</span><span class="sxs-lookup"><span data-stu-id="f1c72-172">PSTN interface (on Mediation Server)</span></span></th>
<th><span data-ttu-id="f1c72-173">PSTN 网关设置</span><span class="sxs-lookup"><span data-stu-id="f1c72-173">PSTN gateway setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-174">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-174">IPv4</span></span></p></td>
<td><p><span data-ttu-id="f1c72-175">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-175">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-176">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-176">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-177">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-177">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-178">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-178">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-179">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-179">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-180">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-180">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-181">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-181">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-182">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-182">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1c72-183">\* 主界面是与 Lync Server 组件进行通信的接口。</span><span class="sxs-lookup"><span data-stu-id="f1c72-183">\* The primary interface is the interface that communicates with the Lync Server components.</span></span>

</div>

<div>

## <a name="remote-user-peer-to-peer-communications"></a><span data-ttu-id="f1c72-184">远程用户对等通信</span><span class="sxs-lookup"><span data-stu-id="f1c72-184">Remote User Peer-to-Peer Communications</span></span>

<span data-ttu-id="f1c72-185">与远程用户的对等通信包括即时消息、音频/视频、应用程序共享和文件传输。</span><span class="sxs-lookup"><span data-stu-id="f1c72-185">Peer-to-peer communications with remote users include instant messaging, audio/video, application sharing, and file transfer.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1c72-186">远程用户网络</span><span class="sxs-lookup"><span data-stu-id="f1c72-186">Remote user network</span></span></th>
<th><span data-ttu-id="f1c72-187">边缘服务器（外部边缘）</span><span class="sxs-lookup"><span data-stu-id="f1c72-187">Edge server (External edge)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-188">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-188">IPv4</span></span></p></td>
<td><p><span data-ttu-id="f1c72-189">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-189">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-190">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-190">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-191">IPv4</span><span class="sxs-lookup"><span data-stu-id="f1c72-191">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-192">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-192">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="f1c72-193">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-193">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-194">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-194">IPv6</span></span></p></td>
<td><p><span data-ttu-id="f1c72-195">双协议栈</span><span class="sxs-lookup"><span data-stu-id="f1c72-195">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-196">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-196">IPv6</span></span></p></td>
<td><p><span data-ttu-id="f1c72-197">IPv6</span><span class="sxs-lookup"><span data-stu-id="f1c72-197">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="front-end-pool-and-edge-pool-configuration"></a><span data-ttu-id="f1c72-198">前端池和边缘池配置</span><span class="sxs-lookup"><span data-stu-id="f1c72-198">Front End Pool and Edge Pool Configuration</span></span>

<span data-ttu-id="f1c72-199">下表显示了前端服务器池和内部边缘服务器池之间的支持列表。</span><span class="sxs-lookup"><span data-stu-id="f1c72-199">The following table shows the support matrix between the Front End Server pool and the internal Edge Server pool.</span></span>

### <a name="front-end-pool-and-edge-pool-internal-edge-matrix"></a><span data-ttu-id="f1c72-200">前端池和边缘池（内部边缘）矩阵</span><span class="sxs-lookup"><span data-stu-id="f1c72-200">Front End Pool and Edge Pool (Internal Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="f1c72-201"><strong>边缘池：IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-201"><strong>Edge Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-202"><strong>边缘池：双协议栈</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-202"><strong>Edge Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-203"><strong>边缘池：IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-203"><strong>Edge Pool: IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-204"><strong>前端池：IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-204"><strong>Front End Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-205">是</span><span class="sxs-lookup"><span data-stu-id="f1c72-205">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1c72-206">是</span><span class="sxs-lookup"><span data-stu-id="f1c72-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1c72-207">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-208"><strong>前端池：双协议栈</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-208"><strong>Front End Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-209">是</span><span class="sxs-lookup"><span data-stu-id="f1c72-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1c72-210">是</span><span class="sxs-lookup"><span data-stu-id="f1c72-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1c72-211">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-212"><strong>前端池：IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-212"><strong>Front End Pool: IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-213">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-213">No</span></span></p></td>
<td><p><span data-ttu-id="f1c72-214">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-214">No</span></span></p></td>
<td><p><span data-ttu-id="f1c72-215">是\*</span><span class="sxs-lookup"><span data-stu-id="f1c72-215">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1c72-216">\* 仅在实验室环境中使用此组合。</span><span class="sxs-lookup"><span data-stu-id="f1c72-216">\* Use this combination only in a lab environment.</span></span>

<span data-ttu-id="f1c72-217">下表是内部和外部边缘接口支持的组合矩阵。</span><span class="sxs-lookup"><span data-stu-id="f1c72-217">The following table is a matrix of the supported combinations of internal and external edge interfaces.</span></span>

### <a name="edge-pool-internal-edge-and-edge-pool-external-edge-matrix"></a><span data-ttu-id="f1c72-218">边缘池（内部边缘）和边缘池（外部边缘）矩阵</span><span class="sxs-lookup"><span data-stu-id="f1c72-218">Edge Pool (Internal Edge) and Edge pool (External Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="f1c72-219"><strong>边缘池（外部边缘）：IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-219"><strong>Edge Pool (External Edge) : IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-220"><strong>边缘池（外部边缘）：双协议栈</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-220"><strong>Edge Pool (External Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-221"><strong>边缘池（外部边缘）：IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-221"><strong>Edge Pool (External Edge): IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-222"><strong>边缘池（内部边缘）：IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-222"><strong>Edge Pool (Internal Edge): IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-223">是</span><span class="sxs-lookup"><span data-stu-id="f1c72-223">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1c72-224">是</span><span class="sxs-lookup"><span data-stu-id="f1c72-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1c72-225">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-225">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1c72-226"><strong>边缘池（内部边缘）：双协议栈</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-226"><strong>Edge Pool (Internal Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-227">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-227">No</span></span></p></td>
<td><p><span data-ttu-id="f1c72-228">是</span><span class="sxs-lookup"><span data-stu-id="f1c72-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1c72-229">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-229">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c72-230"><strong>边缘池（内部边缘）：IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="f1c72-230"><strong>Edge Pool (Internal Edge): IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c72-231">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-231">No</span></span></p></td>
<td><p><span data-ttu-id="f1c72-232">否</span><span class="sxs-lookup"><span data-stu-id="f1c72-232">No</span></span></p></td>
<td><p><span data-ttu-id="f1c72-233">是\*</span><span class="sxs-lookup"><span data-stu-id="f1c72-233">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1c72-234">\* 仅在实验室环境中使用此组合。</span><span class="sxs-lookup"><span data-stu-id="f1c72-234">\* Use this combination only in a lab environment.</span></span>

</div>

<div>

## <a name="advanced-enterprise-voice-support-for-ipv6"></a><span data-ttu-id="f1c72-235">IPv6 的高级企业语音支持</span><span class="sxs-lookup"><span data-stu-id="f1c72-235">Advanced Enterprise Voice Support for IPv6</span></span>

<span data-ttu-id="f1c72-236">包括呼叫许可控制 (CAC)、增强型 9-1-1 (E9-1-1) 或媒体旁路的部署必须配置为仅 IPv4 或双协议栈实施。</span><span class="sxs-lookup"><span data-stu-id="f1c72-236">Deployments that include call admission control (CAC), Enhanced 9-1-1 (E9-1-1), or media bypass must be configured as IPv4 only or as a dual-stacked implementation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f1c72-237">在双堆栈部署中，即使 Lync 客户端通过使用 IPv6 连接到 Lync 服务器，Lync 也将尽力映射合适的 IPv4 地址以支持 E9-1。</span><span class="sxs-lookup"><span data-stu-id="f1c72-237">In a dual-stacked deployment, even if a Lync client connects to a Lync Server by using IPv6, Lync will make a best effort to map an appropriate IPv4 address to support E9-1-1.</span></span>



</div>

<span data-ttu-id="f1c72-238">不支持具有 IPv6 地址的位置信息服务。</span><span class="sxs-lookup"><span data-stu-id="f1c72-238">Location Information service with IPv6 addresses is not supported.</span></span>

<span data-ttu-id="f1c72-p107">Exchange 统一消息 (UM) 不支持 IPv6。对于 Exchange UM，请确保 DNS 解析不会返回 IPv6 地址。使用 IPv6 可能会在将呼叫发送至语音信箱时导致失败。</span><span class="sxs-lookup"><span data-stu-id="f1c72-p107">Exchange Unified Messaging (UM) does not support IPv6. For Exchange UM, be sure that DNS resolution does not return an IPv6 address. Using IPv6 may cause failure when calls are sent to voice mail.</span></span>

</div>

<div>

## <a name="other-lync-server-2013-feature-support-for-ipv6"></a><span data-ttu-id="f1c72-242">适用于 IPv6 的其他 Lync Server 2013 功能支持</span><span class="sxs-lookup"><span data-stu-id="f1c72-242">Other Lync Server 2013 Feature Support for IPv6</span></span>

<span data-ttu-id="f1c72-243">除了之前提到的功能和组件，Lync Server 2013 支持针对以下功能的 IPv6：</span><span class="sxs-lookup"><span data-stu-id="f1c72-243">In addition to the features and components mentioned previously, Lync Server 2013 supports IPv6 for the following features:</span></span>

  - <span data-ttu-id="f1c72-244">**持久聊天**</span><span class="sxs-lookup"><span data-stu-id="f1c72-244">**Persistent Chat**</span></span>
    
    <span data-ttu-id="f1c72-245">可使用拓扑生成器为持久聊天配置 IPv6。</span><span class="sxs-lookup"><span data-stu-id="f1c72-245">You configure IPv6 for Persistent Chat by using Topology Builder.</span></span> <span data-ttu-id="f1c72-246">有关配置持久聊天的详细信息，请参阅部署持久聊天服务器文档。</span><span class="sxs-lookup"><span data-stu-id="f1c72-246">For details about configuring Persistent Chat, see the Deploying Persistent Chat Server documentation.</span></span>

  - <span data-ttu-id="f1c72-247">**用户体验质量 (QoE) 和呼叫详细信息记录 (CDR) 报告**</span><span class="sxs-lookup"><span data-stu-id="f1c72-247">**Quality of Experience (QoE) and call detail recording (CDR) reports**</span></span>
    
    <span data-ttu-id="f1c72-248">监视报告将会包括 IP 地址，因为该地址存储在监视服务器数据库中（无论类型为 IPv4 还是 IPv6）。</span><span class="sxs-lookup"><span data-stu-id="f1c72-248">Monitoring reports include the IP address as it is stored in the Monitoring Server database, whether of type IPv4 or IPv6.</span></span>

<span data-ttu-id="f1c72-249"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1c72-249"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

