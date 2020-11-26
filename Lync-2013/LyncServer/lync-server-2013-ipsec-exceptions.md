---
title: Lync Server 2013 IPsec 例外
description: Lync Server 2013 IPsec 例外。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPsec exceptions
ms:assetid: 241f1eca-6f2f-44de-90b1-2cb659cbe27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425719(v=OCS.15)
ms:contentKeyID: 48183627
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b01264171592ec352b778e1aa7eee5861801991
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426723"
---
# <a name="ipsec-exceptions-in-lync-server-2013"></a><span data-ttu-id="13102-103">Lync Server 2013 中的 IPsec 例外</span><span class="sxs-lookup"><span data-stu-id="13102-103">IPsec exceptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13102-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13102-104">

<span> </span></span></span>

<span data-ttu-id="13102-105">_**主题上次修改时间：** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="13102-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="13102-106">对于 Internet 协议安全 (IPsec) 的企业网络 (请参阅 IETF RFC 4301-4309) 已部署，必须在用于传送音频、视频和全景视频的端口范围内禁用 IPsec。</span><span class="sxs-lookup"><span data-stu-id="13102-106">For enterprise networks where Internet Protocol security (IPsec) (see IETF RFC 4301-4309) has been deployed, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span> <span data-ttu-id="13102-107">提出此建议的动机是需要避免由于 IPsec 协商而在分配媒体端口时产生任何延迟。</span><span class="sxs-lookup"><span data-stu-id="13102-107">The recommendation is motivated by the need to avoid any delay in the allocation of media ports due to IPsec negotiation.</span></span>

<span data-ttu-id="13102-108">下表介绍了建议采用的 IPsec 例外设置。</span><span class="sxs-lookup"><span data-stu-id="13102-108">The following table explains the recommended IPsec exception settings.</span></span>

### <a name="recommended-ipsec-exceptions"></a><span data-ttu-id="13102-109">建议采用的 IPsec 例外</span><span class="sxs-lookup"><span data-stu-id="13102-109">Recommended IPsec Exceptions</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13102-110">规则名称</span><span class="sxs-lookup"><span data-stu-id="13102-110">Rule name</span></span></th>
<th><span data-ttu-id="13102-111">源 IP</span><span class="sxs-lookup"><span data-stu-id="13102-111">Source IP</span></span></th>
<th><span data-ttu-id="13102-112">目标 IP</span><span class="sxs-lookup"><span data-stu-id="13102-112">Destination IP</span></span></th>
<th><span data-ttu-id="13102-113">协议</span><span class="sxs-lookup"><span data-stu-id="13102-113">Protocol</span></span></th>
<th><span data-ttu-id="13102-114">源端口</span><span class="sxs-lookup"><span data-stu-id="13102-114">Source port</span></span></th>
<th><span data-ttu-id="13102-115">目标端口</span><span class="sxs-lookup"><span data-stu-id="13102-115">Destination port</span></span></th>
<th><span data-ttu-id="13102-116">身份验证要求</span><span class="sxs-lookup"><span data-stu-id="13102-116">Authentication Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13102-117">A/V 边缘服务器内部入站</span><span class="sxs-lookup"><span data-stu-id="13102-117">A/V Edge Server Internal Inbound</span></span></p></td>
<td><p><span data-ttu-id="13102-118">任意</span><span class="sxs-lookup"><span data-stu-id="13102-118">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-119">A/V 边缘服务器内部</span><span class="sxs-lookup"><span data-stu-id="13102-119">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="13102-120">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-120">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-121">任意</span><span class="sxs-lookup"><span data-stu-id="13102-121">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-122">任意</span><span class="sxs-lookup"><span data-stu-id="13102-122">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-123">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-123">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13102-124">A/V 边缘服务器外部入站</span><span class="sxs-lookup"><span data-stu-id="13102-124">A/V Edge Server External Inbound</span></span></p></td>
<td><p><span data-ttu-id="13102-125">任意</span><span class="sxs-lookup"><span data-stu-id="13102-125">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-126">A/V 边缘服务器外部</span><span class="sxs-lookup"><span data-stu-id="13102-126">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="13102-127">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-127">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-128">任意</span><span class="sxs-lookup"><span data-stu-id="13102-128">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-129">任意</span><span class="sxs-lookup"><span data-stu-id="13102-129">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-130">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-130">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13102-131">A/V 边缘服务器内部出站</span><span class="sxs-lookup"><span data-stu-id="13102-131">A/V Edge Server Internal Outbound</span></span></p></td>
<td><p><span data-ttu-id="13102-132">A/V 边缘服务器内部</span><span class="sxs-lookup"><span data-stu-id="13102-132">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="13102-133">任意</span><span class="sxs-lookup"><span data-stu-id="13102-133">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-134">UDP &amp; TCP</span><span class="sxs-lookup"><span data-stu-id="13102-134">UDP &amp; TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-135">任意</span><span class="sxs-lookup"><span data-stu-id="13102-135">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-136">任意</span><span class="sxs-lookup"><span data-stu-id="13102-136">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-137">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-137">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13102-138">A/V 边缘服务器外部出站</span><span class="sxs-lookup"><span data-stu-id="13102-138">A/V Edge Server External Outbound</span></span></p></td>
<td><p><span data-ttu-id="13102-139">A/V 边缘服务器外部</span><span class="sxs-lookup"><span data-stu-id="13102-139">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="13102-140">任意</span><span class="sxs-lookup"><span data-stu-id="13102-140">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-141">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-141">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-142">任意</span><span class="sxs-lookup"><span data-stu-id="13102-142">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-143">任意</span><span class="sxs-lookup"><span data-stu-id="13102-143">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-144">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-144">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13102-145">中介服务器入站</span><span class="sxs-lookup"><span data-stu-id="13102-145">Mediation Server Inbound</span></span></p></td>
<td><p><span data-ttu-id="13102-146">任意</span><span class="sxs-lookup"><span data-stu-id="13102-146">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-147">中介</span><span class="sxs-lookup"><span data-stu-id="13102-147">Mediation</span></span></p>
<p><span data-ttu-id="13102-148">服务器</span><span class="sxs-lookup"><span data-stu-id="13102-148">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="13102-149">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-149">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-150">任意</span><span class="sxs-lookup"><span data-stu-id="13102-150">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-151">任意</span><span class="sxs-lookup"><span data-stu-id="13102-151">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-152">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-152">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13102-153">中介服务器出站</span><span class="sxs-lookup"><span data-stu-id="13102-153">Mediation Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="13102-154">中介</span><span class="sxs-lookup"><span data-stu-id="13102-154">Mediation</span></span></p>
<p><span data-ttu-id="13102-155">服务器</span><span class="sxs-lookup"><span data-stu-id="13102-155">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="13102-156">任意</span><span class="sxs-lookup"><span data-stu-id="13102-156">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-157">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-157">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-158">任意</span><span class="sxs-lookup"><span data-stu-id="13102-158">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-159">任意</span><span class="sxs-lookup"><span data-stu-id="13102-159">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-160">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-160">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13102-161">会议助理入站</span><span class="sxs-lookup"><span data-stu-id="13102-161">Conferencing Attendant Inbound</span></span></p></td>
<td><p><span data-ttu-id="13102-162">任意</span><span class="sxs-lookup"><span data-stu-id="13102-162">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-163">运行会议助理的前端服务器</span><span class="sxs-lookup"><span data-stu-id="13102-163">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="13102-164">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-164">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-165">任意</span><span class="sxs-lookup"><span data-stu-id="13102-165">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-166">任意</span><span class="sxs-lookup"><span data-stu-id="13102-166">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-167">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-167">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13102-168">会议助理出站</span><span class="sxs-lookup"><span data-stu-id="13102-168">Conferencing Attendant Outbound</span></span></p></td>
<td><p><span data-ttu-id="13102-169">运行会议助理的前端服务器</span><span class="sxs-lookup"><span data-stu-id="13102-169">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="13102-170">任意</span><span class="sxs-lookup"><span data-stu-id="13102-170">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-171">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-171">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-172">任意</span><span class="sxs-lookup"><span data-stu-id="13102-172">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-173">任意</span><span class="sxs-lookup"><span data-stu-id="13102-173">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-174">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-174">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13102-175">A/V 会议入站</span><span class="sxs-lookup"><span data-stu-id="13102-175">A/V Conferencing Inbound</span></span></p></td>
<td><p><span data-ttu-id="13102-176">任意</span><span class="sxs-lookup"><span data-stu-id="13102-176">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-177">前端服务器</span><span class="sxs-lookup"><span data-stu-id="13102-177">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="13102-178">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-178">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-179">任意</span><span class="sxs-lookup"><span data-stu-id="13102-179">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-180">任意</span><span class="sxs-lookup"><span data-stu-id="13102-180">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-181">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-181">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13102-182">A/V 会议出站</span><span class="sxs-lookup"><span data-stu-id="13102-182">A/V Conferencing Outbound</span></span></p></td>
<td><p><span data-ttu-id="13102-183">前端服务器</span><span class="sxs-lookup"><span data-stu-id="13102-183">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="13102-184">任意</span><span class="sxs-lookup"><span data-stu-id="13102-184">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-185">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-185">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-186">任意</span><span class="sxs-lookup"><span data-stu-id="13102-186">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-187">任意</span><span class="sxs-lookup"><span data-stu-id="13102-187">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-188">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-188">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13102-189">Exchange 入站</span><span class="sxs-lookup"><span data-stu-id="13102-189">Exchange Inbound</span></span></p></td>
<td><p><span data-ttu-id="13102-190">任意</span><span class="sxs-lookup"><span data-stu-id="13102-190">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-191">Exchange 统一消息</span><span class="sxs-lookup"><span data-stu-id="13102-191">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="13102-192">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-192">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-193">任意</span><span class="sxs-lookup"><span data-stu-id="13102-193">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-194">任意</span><span class="sxs-lookup"><span data-stu-id="13102-194">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-195">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-195">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13102-196">应用程序共享服务器入站</span><span class="sxs-lookup"><span data-stu-id="13102-196">Application Sharing Servers Inbound</span></span></p></td>
<td><p><span data-ttu-id="13102-197">任意</span><span class="sxs-lookup"><span data-stu-id="13102-197">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-198">应用程序共享服务器</span><span class="sxs-lookup"><span data-stu-id="13102-198">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="13102-199">TCP</span><span class="sxs-lookup"><span data-stu-id="13102-199">TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-200">任意</span><span class="sxs-lookup"><span data-stu-id="13102-200">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-201">任意</span><span class="sxs-lookup"><span data-stu-id="13102-201">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-202">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-202">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13102-203">应用程序共享服务器出站</span><span class="sxs-lookup"><span data-stu-id="13102-203">Application Sharing Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="13102-204">应用程序共享服务器</span><span class="sxs-lookup"><span data-stu-id="13102-204">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="13102-205">任意</span><span class="sxs-lookup"><span data-stu-id="13102-205">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-206">TCP</span><span class="sxs-lookup"><span data-stu-id="13102-206">TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-207">任意</span><span class="sxs-lookup"><span data-stu-id="13102-207">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-208">任意</span><span class="sxs-lookup"><span data-stu-id="13102-208">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-209">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-209">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13102-210">Exchange 出站</span><span class="sxs-lookup"><span data-stu-id="13102-210">Exchange Outbound</span></span></p></td>
<td><p><span data-ttu-id="13102-211">Exchange 统一消息</span><span class="sxs-lookup"><span data-stu-id="13102-211">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="13102-212">任意</span><span class="sxs-lookup"><span data-stu-id="13102-212">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-213">UDP 和 TCP</span><span class="sxs-lookup"><span data-stu-id="13102-213">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="13102-214">任意</span><span class="sxs-lookup"><span data-stu-id="13102-214">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-215">任意</span><span class="sxs-lookup"><span data-stu-id="13102-215">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-216">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-216">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13102-217">客户端</span><span class="sxs-lookup"><span data-stu-id="13102-217">Clients</span></span></p></td>
<td><p><span data-ttu-id="13102-218">任意</span><span class="sxs-lookup"><span data-stu-id="13102-218">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-219">任意</span><span class="sxs-lookup"><span data-stu-id="13102-219">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-220">UDP</span><span class="sxs-lookup"><span data-stu-id="13102-220">UDP</span></span></p></td>
<td><p><span data-ttu-id="13102-221">指定的媒体端口范围</span><span class="sxs-lookup"><span data-stu-id="13102-221">Specified media port range</span></span></p></td>
<td><p><span data-ttu-id="13102-222">任意</span><span class="sxs-lookup"><span data-stu-id="13102-222">Any</span></span></p></td>
<td><p><span data-ttu-id="13102-223">不进行身份验证</span><span class="sxs-lookup"><span data-stu-id="13102-223">Do not authenticate</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="13102-224">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13102-224">


</div>

<span> </span>

</div>

</div>

</span></span></div>

