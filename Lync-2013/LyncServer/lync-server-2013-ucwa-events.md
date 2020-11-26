---
title: Lync Server 2013： UCWA 事件
description: Lync Server 2013： UCWA 事件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UCWA events
ms:assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945621(v=OCS.15)
ms:contentKeyID: 51541461
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8104ce9c7533350f40ce194e1cde205bc3692792
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440463"
---
# <a name="ucwa-events-in-lync-server-2013"></a><span data-ttu-id="01850-103">Lync Server 2013 中的 UCWA 事件</span><span class="sxs-lookup"><span data-stu-id="01850-103">UCWA events in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01850-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01850-104">

<span> </span></span></span>

<span data-ttu-id="01850-105">_**主题上次修改时间：** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="01850-105">_**Topic Last Modified:** 2013-02-15_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="01850-106">Lync Server 2013 使用统一通信 Web API (UCWA) 来实现许多用途，从访问 Microsoft Exchange 到联系人搜索以更新移动客户端的状态。</span><span class="sxs-lookup"><span data-stu-id="01850-106">Lync Server 2013 uses the Unified Communications Web API (UCWA) for a number of purposes, from accessing Microsoft Exchange for contact searches to updating presence for mobile clients.</span></span>

<span data-ttu-id="01850-p101">UCWA 将运行行为的记录编写成“信息”、“警告”和“错误”事件类型。下表介绍了可由 UCWA 组件编写的事件。</span><span class="sxs-lookup"><span data-stu-id="01850-p101">UCWA will write records of operational behavior as event types Informational, Warning, and Error. The following table describes the events that can be written by the UCWA components.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01850-109">事件 ID</span><span class="sxs-lookup"><span data-stu-id="01850-109">Event ID</span></span></th>
<th><span data-ttu-id="01850-110">事件类型</span><span class="sxs-lookup"><span data-stu-id="01850-110">Event Type</span></span></th>
<th><span data-ttu-id="01850-111">摘要</span><span class="sxs-lookup"><span data-stu-id="01850-111">Summary</span></span></th>
<th><span data-ttu-id="01850-112">原因和解决方法</span><span class="sxs-lookup"><span data-stu-id="01850-112">Cause and Resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01850-113">20001</span><span class="sxs-lookup"><span data-stu-id="01850-113">20001</span></span></p></td>
<td><p><span data-ttu-id="01850-114">信息</span><span class="sxs-lookup"><span data-stu-id="01850-114">Informational</span></span></p></td>
<td><p><span data-ttu-id="01850-115">UCWA 已初始化</span><span class="sxs-lookup"><span data-stu-id="01850-115">UCWA initialized</span></span></p></td>
<td><p><span data-ttu-id="01850-116">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-116">N/A</span></span></p>
<p><span data-ttu-id="01850-117">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-117">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-118">20002</span><span class="sxs-lookup"><span data-stu-id="01850-118">20002</span></span></p></td>
<td><p><span data-ttu-id="01850-119">错误</span><span class="sxs-lookup"><span data-stu-id="01850-119">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-120">UCWA 在初始化期间遇到意外异常</span><span class="sxs-lookup"><span data-stu-id="01850-120">UCWA encountered an unexpected exception during initialization</span></span></p></td>
<td><p><span data-ttu-id="01850-121">初始化期间出现意外错误</span><span class="sxs-lookup"><span data-stu-id="01850-121">An unexpected error has occurred during initialization</span></span></p>
<p><span data-ttu-id="01850-122">检查相关事件日志条目中的异常详细信息以确定可能的原因</span><span class="sxs-lookup"><span data-stu-id="01850-122">Examine the exception details in the associated event log entry to determine the possible cause</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-123">20003</span><span class="sxs-lookup"><span data-stu-id="01850-123">20003</span></span></p></td>
<td><p><span data-ttu-id="01850-124">错误</span><span class="sxs-lookup"><span data-stu-id="01850-124">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-125">UCWA 遇到未经处理的异常</span><span class="sxs-lookup"><span data-stu-id="01850-125">UCWA encountered an unhandled exception</span></span></p></td>
<td><p><span data-ttu-id="01850-126">出现未经处理的异常</span><span class="sxs-lookup"><span data-stu-id="01850-126">An unhandled exception happened</span></span></p>
<p><span data-ttu-id="01850-p102">重新启动服务器。如果问题仍然存在，请联系产品支持人员</span><span class="sxs-lookup"><span data-stu-id="01850-p102">Restart the server. If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-129">20004</span><span class="sxs-lookup"><span data-stu-id="01850-129">20004</span></span></p></td>
<td><p><span data-ttu-id="01850-130">错误</span><span class="sxs-lookup"><span data-stu-id="01850-130">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-131">无法访问 Exchange 获取高清照片</span><span class="sxs-lookup"><span data-stu-id="01850-131">Cannot access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="01850-132">与 Exchange 的连接不可用</span><span class="sxs-lookup"><span data-stu-id="01850-132">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="01850-133">确保与 Exchange 的连接可用</span><span class="sxs-lookup"><span data-stu-id="01850-133">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-134">20005</span><span class="sxs-lookup"><span data-stu-id="01850-134">20005</span></span></p></td>
<td><p><span data-ttu-id="01850-135">信息</span><span class="sxs-lookup"><span data-stu-id="01850-135">Informational</span></span></p></td>
<td><p><span data-ttu-id="01850-136">从无法访问 Exchange 获取高清照片的故障中恢复</span><span class="sxs-lookup"><span data-stu-id="01850-136">Recovered from failing to access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="01850-137">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-137">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-138">20006</span><span class="sxs-lookup"><span data-stu-id="01850-138">20006</span></span></p></td>
<td><p><span data-ttu-id="01850-139">错误</span><span class="sxs-lookup"><span data-stu-id="01850-139">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-140">无法访问 Exchange 进行联系人搜索</span><span class="sxs-lookup"><span data-stu-id="01850-140">Cannot access Exchange for contact search</span></span></p></td>
<td><p><span data-ttu-id="01850-141">与 Exchange 的连接不可用</span><span class="sxs-lookup"><span data-stu-id="01850-141">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="01850-142">确保与 Exchange 的连接可用</span><span class="sxs-lookup"><span data-stu-id="01850-142">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-143">20007</span><span class="sxs-lookup"><span data-stu-id="01850-143">20007</span></span></p></td>
<td><p><span data-ttu-id="01850-144">信息</span><span class="sxs-lookup"><span data-stu-id="01850-144">Informational</span></span></p></td>
<td><p><span data-ttu-id="01850-145">从无法在 Exchange 中搜索联系人的故障中恢复</span><span class="sxs-lookup"><span data-stu-id="01850-145">Recovered from failing to search contact in Exchange</span></span></p></td>
<td><p><span data-ttu-id="01850-146">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-147">20008</span><span class="sxs-lookup"><span data-stu-id="01850-147">20008</span></span></p></td>
<td><p><span data-ttu-id="01850-148">警告</span><span class="sxs-lookup"><span data-stu-id="01850-148">Warning</span></span></p></td>
<td><p><span data-ttu-id="01850-149">尝试订阅超过每应用程序允许的状态订阅数量</span><span class="sxs-lookup"><span data-stu-id="01850-149">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p></td>
<td><p><span data-ttu-id="01850-150">尝试订阅超过每应用程序允许的状态订阅数量</span><span class="sxs-lookup"><span data-stu-id="01850-150">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p>
<p><span data-ttu-id="01850-151">检查客户端中不必要的订阅</span><span class="sxs-lookup"><span data-stu-id="01850-151">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-152">20009</span><span class="sxs-lookup"><span data-stu-id="01850-152">20009</span></span></p></td>
<td><p><span data-ttu-id="01850-153">警告</span><span class="sxs-lookup"><span data-stu-id="01850-153">Warning</span></span></p></td>
<td><p><span data-ttu-id="01850-154">尝试订阅超过每批允许的状态订阅数量</span><span class="sxs-lookup"><span data-stu-id="01850-154">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p></td>
<td><p><span data-ttu-id="01850-155">尝试订阅超过每批允许的状态订阅数量</span><span class="sxs-lookup"><span data-stu-id="01850-155">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p>
<p><span data-ttu-id="01850-156">检查客户端中不必要的订阅</span><span class="sxs-lookup"><span data-stu-id="01850-156">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-157">20010</span><span class="sxs-lookup"><span data-stu-id="01850-157">20010</span></span></p></td>
<td><p><span data-ttu-id="01850-158">错误</span><span class="sxs-lookup"><span data-stu-id="01850-158">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-159">无法检索带内数据</span><span class="sxs-lookup"><span data-stu-id="01850-159">Cannot retrieve inband data</span></span></p></td>
<td><p><span data-ttu-id="01850-160">无法检索带内数据</span><span class="sxs-lookup"><span data-stu-id="01850-160">Cannot retrieve inband data</span></span></p>
<p><span data-ttu-id="01850-161">如果问题仍然存在，请联系产品支持人员</span><span class="sxs-lookup"><span data-stu-id="01850-161">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-162">20011</span><span class="sxs-lookup"><span data-stu-id="01850-162">20011</span></span></p></td>
<td><p><span data-ttu-id="01850-163">错误</span><span class="sxs-lookup"><span data-stu-id="01850-163">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-164">无法订阅状态</span><span class="sxs-lookup"><span data-stu-id="01850-164">Cannot subscribe presence</span></span></p></td>
<td><p><span data-ttu-id="01850-165">无法订阅状态</span><span class="sxs-lookup"><span data-stu-id="01850-165">Cannot subscribe presence</span></span></p>
<p><span data-ttu-id="01850-166">如果问题仍然存在，请联系产品支持人员</span><span class="sxs-lookup"><span data-stu-id="01850-166">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-167">20012</span><span class="sxs-lookup"><span data-stu-id="01850-167">20012</span></span></p></td>
<td><p><span data-ttu-id="01850-168">错误</span><span class="sxs-lookup"><span data-stu-id="01850-168">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-169">未能注册终结点</span><span class="sxs-lookup"><span data-stu-id="01850-169">Failed to register endpoint</span></span></p></td>
<td><p><span data-ttu-id="01850-170">未能注册终结点</span><span class="sxs-lookup"><span data-stu-id="01850-170">Failed to register endpoint</span></span></p>
<p><span data-ttu-id="01850-171">如果问题仍然存在，请联系产品支持人员</span><span class="sxs-lookup"><span data-stu-id="01850-171">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-172">20013</span><span class="sxs-lookup"><span data-stu-id="01850-172">20013</span></span></p></td>
<td><p><span data-ttu-id="01850-173">错误</span><span class="sxs-lookup"><span data-stu-id="01850-173">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-174">IM MCU 不可用</span><span class="sxs-lookup"><span data-stu-id="01850-174">IM MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="01850-175">IM MCU 不可用</span><span class="sxs-lookup"><span data-stu-id="01850-175">IM MCU is unavailable</span></span></p>
<p><span data-ttu-id="01850-176">查看 IM MCU 是否在运行</span><span class="sxs-lookup"><span data-stu-id="01850-176">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-177">20014</span><span class="sxs-lookup"><span data-stu-id="01850-177">20014</span></span></p></td>
<td><p><span data-ttu-id="01850-178">信息</span><span class="sxs-lookup"><span data-stu-id="01850-178">Informational</span></span></p></td>
<td><p><span data-ttu-id="01850-179">从无法连接 IM MCU 的故障中恢复</span><span class="sxs-lookup"><span data-stu-id="01850-179">Recovered from failing to connect to IM MCU</span></span></p></td>
<td><p><span data-ttu-id="01850-180">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-180">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-181">20015</span><span class="sxs-lookup"><span data-stu-id="01850-181">20015</span></span></p></td>
<td><p><span data-ttu-id="01850-182">错误</span><span class="sxs-lookup"><span data-stu-id="01850-182">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-183">AV MCU 不可用</span><span class="sxs-lookup"><span data-stu-id="01850-183">AV MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="01850-184">AV MCU 不可用</span><span class="sxs-lookup"><span data-stu-id="01850-184">AV MCU is unavailable</span></span></p>
<p><span data-ttu-id="01850-185">查看 AV MCU 是否在运行</span><span class="sxs-lookup"><span data-stu-id="01850-185">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-186">20016</span><span class="sxs-lookup"><span data-stu-id="01850-186">20016</span></span></p></td>
<td><p><span data-ttu-id="01850-187">信息</span><span class="sxs-lookup"><span data-stu-id="01850-187">Informational</span></span></p></td>
<td><p><span data-ttu-id="01850-188">从无法连接 AV MCU 的故障中恢复</span><span class="sxs-lookup"><span data-stu-id="01850-188">Recovered from failing to connect to AV MCU</span></span></p></td>
<td><p><span data-ttu-id="01850-189">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-189">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-190">20017</span><span class="sxs-lookup"><span data-stu-id="01850-190">20017</span></span></p></td>
<td><p><span data-ttu-id="01850-191">错误</span><span class="sxs-lookup"><span data-stu-id="01850-191">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-192">AS MCU 不可用</span><span class="sxs-lookup"><span data-stu-id="01850-192">AS MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="01850-193">AS MCU 不可用</span><span class="sxs-lookup"><span data-stu-id="01850-193">AS MCU is unavailable</span></span></p>
<p><span data-ttu-id="01850-194">查看 AS MCU 是否在运行</span><span class="sxs-lookup"><span data-stu-id="01850-194">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-195">20018</span><span class="sxs-lookup"><span data-stu-id="01850-195">20018</span></span></p></td>
<td><p><span data-ttu-id="01850-196">信息</span><span class="sxs-lookup"><span data-stu-id="01850-196">Informational</span></span></p></td>
<td><p><span data-ttu-id="01850-197">从无法连接 AS MCU 的故障中恢复</span><span class="sxs-lookup"><span data-stu-id="01850-197">Recovered from failing to connect to AS MCU</span></span></p></td>
<td><p><span data-ttu-id="01850-198">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-198">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-199">20019</span><span class="sxs-lookup"><span data-stu-id="01850-199">20019</span></span></p></td>
<td><p><span data-ttu-id="01850-200">错误</span><span class="sxs-lookup"><span data-stu-id="01850-200">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-201">Data MCU 不可用</span><span class="sxs-lookup"><span data-stu-id="01850-201">Data MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="01850-202">Data MCU 不可用</span><span class="sxs-lookup"><span data-stu-id="01850-202">Data MCU is unavailable</span></span></p>
<p><span data-ttu-id="01850-203">查看 Data MCU 是否在运行</span><span class="sxs-lookup"><span data-stu-id="01850-203">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-204">20020</span><span class="sxs-lookup"><span data-stu-id="01850-204">20020</span></span></p></td>
<td><p><span data-ttu-id="01850-205">信息</span><span class="sxs-lookup"><span data-stu-id="01850-205">Informational</span></span></p></td>
<td><p><span data-ttu-id="01850-206">从无法连接 Data MCU 的故障中恢复</span><span class="sxs-lookup"><span data-stu-id="01850-206">Recovered from failing to connect to Data MCU</span></span></p></td>
<td><p><span data-ttu-id="01850-207">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-207">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-208">20021</span><span class="sxs-lookup"><span data-stu-id="01850-208">20021</span></span></p></td>
<td><p><span data-ttu-id="01850-209">错误</span><span class="sxs-lookup"><span data-stu-id="01850-209">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-210">无法加入 IM MCU</span><span class="sxs-lookup"><span data-stu-id="01850-210">Cannot join IM MCU</span></span></p></td>
<td><p><span data-ttu-id="01850-211">无法加入 IM MCU</span><span class="sxs-lookup"><span data-stu-id="01850-211">Cannot join IM MCU</span></span></p>
<p><span data-ttu-id="01850-212">查看 IM MCU 是否在运行</span><span class="sxs-lookup"><span data-stu-id="01850-212">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-213">20022</span><span class="sxs-lookup"><span data-stu-id="01850-213">20022</span></span></p></td>
<td><p><span data-ttu-id="01850-214">错误</span><span class="sxs-lookup"><span data-stu-id="01850-214">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-215">无法加入 AV MCU</span><span class="sxs-lookup"><span data-stu-id="01850-215">Cannot join AV MCU</span></span></p></td>
<td><p><span data-ttu-id="01850-216">无法加入 AV MCU</span><span class="sxs-lookup"><span data-stu-id="01850-216">Cannot join AV MCU</span></span></p>
<p><span data-ttu-id="01850-217">查看 AV MCU 是否在运行</span><span class="sxs-lookup"><span data-stu-id="01850-217">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-218">20023</span><span class="sxs-lookup"><span data-stu-id="01850-218">20023</span></span></p></td>
<td><p><span data-ttu-id="01850-219">错误</span><span class="sxs-lookup"><span data-stu-id="01850-219">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-220">无法加入 AS MCU</span><span class="sxs-lookup"><span data-stu-id="01850-220">Cannot join AS MCU</span></span></p></td>
<td><p><span data-ttu-id="01850-221">无法加入 AS MCU</span><span class="sxs-lookup"><span data-stu-id="01850-221">Cannot join AS MCU</span></span></p>
<p><span data-ttu-id="01850-222">查看 AS MCU 是否在运行</span><span class="sxs-lookup"><span data-stu-id="01850-222">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-223">20024</span><span class="sxs-lookup"><span data-stu-id="01850-223">20024</span></span></p></td>
<td><p><span data-ttu-id="01850-224">错误</span><span class="sxs-lookup"><span data-stu-id="01850-224">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-225">无法加入 Data MCU</span><span class="sxs-lookup"><span data-stu-id="01850-225">Cannot join Data MCU</span></span></p></td>
<td><p><span data-ttu-id="01850-226">无法加入 Data MCU</span><span class="sxs-lookup"><span data-stu-id="01850-226">Cannot join Data MCU</span></span></p>
<p><span data-ttu-id="01850-227">查看 Data MCU 是否在运行</span><span class="sxs-lookup"><span data-stu-id="01850-227">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-228">20025</span><span class="sxs-lookup"><span data-stu-id="01850-228">20025</span></span></p></td>
<td><p><span data-ttu-id="01850-229">错误</span><span class="sxs-lookup"><span data-stu-id="01850-229">Error</span></span></p></td>
<td><p><span data-ttu-id="01850-230">无法访问 Active Directory 获取照片</span><span class="sxs-lookup"><span data-stu-id="01850-230">Cannot access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="01850-231">与 Active Directory 的连接不可用</span><span class="sxs-lookup"><span data-stu-id="01850-231">Connection to active directory is not available</span></span></p>
<p><span data-ttu-id="01850-232">确保与 Active Directory 的连接可用</span><span class="sxs-lookup"><span data-stu-id="01850-232">Make sure the connection to active directory is available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01850-233">20026</span><span class="sxs-lookup"><span data-stu-id="01850-233">20026</span></span></p></td>
<td><p><span data-ttu-id="01850-234">信息</span><span class="sxs-lookup"><span data-stu-id="01850-234">Informational</span></span></p></td>
<td><p><span data-ttu-id="01850-235">从无法访问 Active Directory 获取照片的故障中恢复</span><span class="sxs-lookup"><span data-stu-id="01850-235">Recovered from failing to access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="01850-236">不适用</span><span class="sxs-lookup"><span data-stu-id="01850-236">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01850-237">20027</span><span class="sxs-lookup"><span data-stu-id="01850-237">20027</span></span></p></td>
<td><p><span data-ttu-id="01850-238">警告</span><span class="sxs-lookup"><span data-stu-id="01850-238">Warning</span></span></p></td>
<td><p><span data-ttu-id="01850-239">无法反序列化</span><span class="sxs-lookup"><span data-stu-id="01850-239">Cannot deserialize</span></span></p></td>
<td><p><span data-ttu-id="01850-240">无法反序列化</span><span class="sxs-lookup"><span data-stu-id="01850-240">Cannot deserialize</span></span></p>
<p><span data-ttu-id="01850-241">如果问题仍然存在，请联系产品支持人员</span><span class="sxs-lookup"><span data-stu-id="01850-241">If the problem persists contact product support</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="01850-242">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01850-242">


</div>

<span> </span>

</div>

</div>

</span></span></div>

