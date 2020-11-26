---
title: Lync Server 2013：移动性能计数器
description: Lync Server 2013：移动性能计数器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility performance counters
ms:assetid: d18ed85a-673d-4695-aa3f-ac83a38ab90a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690046(v=OCS.15)
ms:contentKeyID: 48185441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 922288f6c026f088d651dc61afdcb6ba04fed30a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425554"
---
# <a name="mobility-performance-counters-in-lync-server-2013"></a><span data-ttu-id="fb32a-103">Lync Server 2013 中的移动性能计数器</span><span class="sxs-lookup"><span data-stu-id="fb32a-103">Mobility performance counters in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb32a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb32a-104">

<span> </span></span></span>

<span data-ttu-id="fb32a-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="fb32a-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="fb32a-106">下表列出了可用于监视运行统一通信 Web API (UCWA) 和 Lync Server 2013 Mcx 移动服务的服务器的性能计数器的名称和说明。</span><span class="sxs-lookup"><span data-stu-id="fb32a-106">The following tables list the names and descriptions of performance counters that you can use to monitor servers running the Unified Communications Web API (UCWA) and the Lync Server 2013 Mcx Mobility Service.</span></span>

<span data-ttu-id="fb32a-107">UCWA 表中计数器的类别名称为 **LS:WEB – UCWA**。</span><span class="sxs-lookup"><span data-stu-id="fb32a-107">The category name for the counters in the UCWA table is **LS:WEB – UCWA**.</span></span>

<span data-ttu-id="fb32a-108">Mcx Mobility Service 表中计数器的类别名称为 **LS:WEB - Mobile Communication Service**。</span><span class="sxs-lookup"><span data-stu-id="fb32a-108">The category name for the counters in the Mcx Mobility Service table is **LS:WEB - Mobile Communication Service**.</span></span>

<div>

## <a name="performance-counters-for-ucwa"></a><span data-ttu-id="fb32a-109">UCWA 性能计数器</span><span class="sxs-lookup"><span data-stu-id="fb32a-109">Performance Counters for UCWA</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb32a-110">计数器</span><span class="sxs-lookup"><span data-stu-id="fb32a-110">Counter</span></span></th>
<th><span data-ttu-id="fb32a-111">描述</span><span class="sxs-lookup"><span data-stu-id="fb32a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-112">Active Application Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-112">Active Application Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-113">当前应用程序数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-113">The current number of applications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-114">Active Application Sharing Modality Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-114">Active Application Sharing Modality Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-115">当前应用程序共享形式数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-115">The current number of Application Sharing modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-116">Active Audio Modality Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-116">Active Audio Modality Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-117">当前音频形式数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-117">The current number of Audio modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-118">Active Data Collaboration Modality Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-118">Active Data Collaboration Modality Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-119">当前数据协作形式数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-119">The current number of Data Collaboration modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-120">Active Directory Photo Get Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="fb32a-120">Active Directory Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="fb32a-121">此计数器显示从 Active Directory 检索照片所花的平均时间（以毫秒为单位）</span><span class="sxs-lookup"><span data-stu-id="fb32a-121">This counter shows the average time (in milliseconds) to retrieve a photo from active directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-122">Active Messaging Modality Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-122">Active Messaging Modality Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-123">当前消息传递形式数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-123">The current number of Messaging modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-124">Active Panoramic Video Modality Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-124">Active Panoramic Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-125">当前全景视频形式数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-125">The current number of Panoramic Video modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-126">Active Pending Get Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-126">Active Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-127">当前活动待处理项数；与服务器长期保持连接</span><span class="sxs-lookup"><span data-stu-id="fb32a-127">The number of currently active pending gets; long-held connections to the server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-128">Active Session Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-128">Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-129">当前在 UCWA 中按应用程序注册的终结点数和总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-129">The current number of endpoints registered in UCWA per application and total</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-130">Active User Instance Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-130">Active User Instance Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-131">当前用户实例数</span><span class="sxs-lookup"><span data-stu-id="fb32a-131">The current number of user instances</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-132">Active User Instances without Application</span><span class="sxs-lookup"><span data-stu-id="fb32a-132">Active User Instances without Application</span></span></p></td>
<td><p><span data-ttu-id="fb32a-133">当前用户实例数（无应用程序）</span><span class="sxs-lookup"><span data-stu-id="fb32a-133">The current number of user instances without application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-134">Active Video Modality Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-134">Active Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-135">当前视频形式数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-135">The current number of Video modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-136">Application Creation Requests Received/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-136">Application Creation Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-137">应用程序创建请求的每秒接收速率</span><span class="sxs-lookup"><span data-stu-id="fb32a-137">The per second rate of received application creation requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-138">AS MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-138">AS MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-139">AS MCU 联接失败数</span><span class="sxs-lookup"><span data-stu-id="fb32a-139">The number of AS MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-140">AV MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-140">AV MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-141">AV MCU 联接失败数</span><span class="sxs-lookup"><span data-stu-id="fb32a-141">The number of AV MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-142">Average Application Startup Time (ms)</span><span class="sxs-lookup"><span data-stu-id="fb32a-142">Average Application Startup Time (ms)</span></span></p></td>
<td><p><span data-ttu-id="fb32a-143">应用程序平均启动时间（以毫秒为单位）</span><span class="sxs-lookup"><span data-stu-id="fb32a-143">The average application startup time in Milliseconds</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-144">Average Lifetime for Session (ms)</span><span class="sxs-lookup"><span data-stu-id="fb32a-144">Average Lifetime for Session (ms)</span></span></p></td>
<td><p><span data-ttu-id="fb32a-145">会话的平均生存时间（以毫秒为单位）</span><span class="sxs-lookup"><span data-stu-id="fb32a-145">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-146">Data MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-146">Data MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-147">Data MCU 联接失败数</span><span class="sxs-lookup"><span data-stu-id="fb32a-147">The number of Data MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-148">Exchange Contact Search Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="fb32a-148">Exchange Contact Search Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="fb32a-149">此计数器显示在 Exchange 中搜索联系人所花的平均时间（以毫秒为单位）</span><span class="sxs-lookup"><span data-stu-id="fb32a-149">This counter shows the average time (in milliseconds) to search contact in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-150">Exchange HD Photo Get Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="fb32a-150">Exchange HD Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="fb32a-151">此计数器显示从 Exchange 中检索照片所花的平均时间（以毫秒为单位）</span><span class="sxs-lookup"><span data-stu-id="fb32a-151">This counter shows the average time (in milliseconds) to retrieve a photo from Exchange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-152">HTTP 4xx Responses/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-152">HTTP 4xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-153">HTTP 4xx 代码的每秒响应速率</span><span class="sxs-lookup"><span data-stu-id="fb32a-153">The per second rate of responses with HTTP 4xx code</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-154">HTTP 5xx Responses/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-154">HTTP 5xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-155">HTTP 5xx 代码的每秒响应速率</span><span class="sxs-lookup"><span data-stu-id="fb32a-155">The per second rate of responses with HTTP 5xx code</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-156">IM MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-156">IM MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-157">IM MCU 联接失败数</span><span class="sxs-lookup"><span data-stu-id="fb32a-157">The number of IM MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-158">Number of Active Directory Photo Get Failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-158">Number of Active Directory Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-159">从 Active Directory 中检索照片的总失败次数</span><span class="sxs-lookup"><span data-stu-id="fb32a-159">The total number of failures to retrieve photos from Active Directory</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-160">Number of Contact Search failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-160">Number of Contact Search failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-161">在 Exchange 中搜索联系人的总失败次数</span><span class="sxs-lookup"><span data-stu-id="fb32a-161">The total number of failures to search contacts in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-162">Number of Deserialization Failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-162">Number of Deserialization Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-163">反序列化的总失败次数</span><span class="sxs-lookup"><span data-stu-id="fb32a-163">The total number of deserialization failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-164">HD 照片获取失败的次数</span><span class="sxs-lookup"><span data-stu-id="fb32a-164">Number of HD Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-165">从 Exchange 中检索 HD 照片的总失败次数</span><span class="sxs-lookup"><span data-stu-id="fb32a-165">The total number of failures to retrieve HD photos from Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-166">Over The Maximum Subscriptions Per Application</span><span class="sxs-lookup"><span data-stu-id="fb32a-166">Over The Maximum Subscriptions Per Application</span></span></p></td>
<td><p><span data-ttu-id="fb32a-167">允许的每应用程序最大订阅请求数</span><span class="sxs-lookup"><span data-stu-id="fb32a-167">The number of Subscription requests over the maximum allowed per application</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-168">Over The Maximum Subscriptions Per Batch</span><span class="sxs-lookup"><span data-stu-id="fb32a-168">Over The Maximum Subscriptions Per Batch</span></span></p></td>
<td><p><span data-ttu-id="fb32a-169">允许的每批次最大订阅请求数</span><span class="sxs-lookup"><span data-stu-id="fb32a-169">The number of Subscription requests over the maximum allowed per batch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-170">Presence Subscription Failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-170">Presence Subscription Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-171">订阅状态失败次数</span><span class="sxs-lookup"><span data-stu-id="fb32a-171">The number of failures to subscribe presence</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-172">Registering Endpoint Failures</span><span class="sxs-lookup"><span data-stu-id="fb32a-172">Registering Endpoint Failures</span></span></p></td>
<td><p><span data-ttu-id="fb32a-173">注册终结点的失败次数</span><span class="sxs-lookup"><span data-stu-id="fb32a-173">The number of failures to register endpoints</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-174">Requests Received/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-174">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-175">每秒收到的请求数</span><span class="sxs-lookup"><span data-stu-id="fb32a-175">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-176">Requests Succeeded/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-176">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-177">每秒的成功请求数（HTTP 2xx/3xx 响应代码）</span><span class="sxs-lookup"><span data-stu-id="fb32a-177">The per second rate of successful requests (HTTP 2xx/3xx response codes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-178">Succeeded Create Application Requests/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-178">Succeeded Create Application Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-179">成功应用程序创建请求的每秒接收速率</span><span class="sxs-lookup"><span data-stu-id="fb32a-179">The per second rate of successful application creation requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-180">Timed Out Pending Get Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-180">Timed Out Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-181">超时的待处理项数</span><span class="sxs-lookup"><span data-stu-id="fb32a-181">The number of pending gets that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-182">Total Application Creation Requests Received</span><span class="sxs-lookup"><span data-stu-id="fb32a-182">Total Application Creation Requests Received</span></span></p></td>
<td><p><span data-ttu-id="fb32a-183">自启动服务以来收到的应用程序创建请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-183">The total number of application creation requests received since the service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-184">Total HTTP 4xx Responses</span><span class="sxs-lookup"><span data-stu-id="fb32a-184">Total HTTP 4xx Responses</span></span></p></td>
<td><p><span data-ttu-id="fb32a-185">HTTP 4xx 响应总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-185">The total number of HTTP 4xx responses</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-186">Total HTTP 5xx Responses</span><span class="sxs-lookup"><span data-stu-id="fb32a-186">Total HTTP 5xx Responses</span></span></p></td>
<td><p><span data-ttu-id="fb32a-187">HTTP 5xx 响应总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-187">The total number of HTTP 5xx responses</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-188">Total Requests Received on the Command Channel</span><span class="sxs-lookup"><span data-stu-id="fb32a-188">Total Requests Received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="fb32a-189">命令通道上收到的请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-189">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-190">Total Requests Succeeded</span><span class="sxs-lookup"><span data-stu-id="fb32a-190">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="fb32a-191">成功的请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-191">The total number of requests that succeeded</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-192">Total Sessions Initiated</span><span class="sxs-lookup"><span data-stu-id="fb32a-192">Total Sessions Initiated</span></span></p></td>
<td><p><span data-ttu-id="fb32a-193">自启动服务以来启动的会话总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-193">The total number of sessions that were initiated since the service was started</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-194">Total Sessions Terminated Because of Idle Timeout</span><span class="sxs-lookup"><span data-stu-id="fb32a-194">Total Sessions Terminated Because of Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="fb32a-195">因用户空闲超时终止的会话总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-195">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-196">Total Throttled Applications</span><span class="sxs-lookup"><span data-stu-id="fb32a-196">Total Throttled Applications</span></span></p></td>
<td><p><span data-ttu-id="fb32a-197">阻止的应用程序数</span><span class="sxs-lookup"><span data-stu-id="fb32a-197">The number of throttled applications</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div id="sectionSection1" class="section">

### <a name="performance-counters-for-mcx-mobility-service"></a><span data-ttu-id="fb32a-198">Mcx Mobility Service 性能计数器</span><span class="sxs-lookup"><span data-stu-id="fb32a-198">Performance Counters for Mcx Mobility Service</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb32a-199">计数器</span><span class="sxs-lookup"><span data-stu-id="fb32a-199">Counter</span></span></th>
<th><span data-ttu-id="fb32a-200">描述</span><span class="sxs-lookup"><span data-stu-id="fb32a-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-201">Average Lifetime for a Session in Milliseconds</span><span class="sxs-lookup"><span data-stu-id="fb32a-201">Average Lifetime for a Session in Milliseconds</span></span></p></td>
<td><p><span data-ttu-id="fb32a-202">会话的平均生存时间（以毫秒为单位）</span><span class="sxs-lookup"><span data-stu-id="fb32a-202">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-203">Current Push Notification Subscriptions</span><span class="sxs-lookup"><span data-stu-id="fb32a-203">Current Push Notification Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="fb32a-p101">当前推送通知订阅数。此数目与 Currently Active Session Count 结合在一起表示为 Windows Mobile 或 iPhone 设备注册的当前活动会话的子集。</span><span class="sxs-lookup"><span data-stu-id="fb32a-p101">The current number of push notification subscriptions. This number, in conjunction with Currently Active Session Count, represents the subset of currently active sessions that are registered for Windows Mobile or iPhone devices.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-206">Currently Active Network Timeout Poll Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-206">Currently Active Network Timeout Poll Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-207">超时的网络投票数</span><span class="sxs-lookup"><span data-stu-id="fb32a-207">The number of network polls that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-208">Currently Active Poll Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-208">Currently Active Poll Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-209">当前活动投票数（与服务器的长期连接）</span><span class="sxs-lookup"><span data-stu-id="fb32a-209">The number of currently active polls (long-held connections to the server)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-210">Currently Active Session Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-210">Currently Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-211">当前注册到 Mobility Service 中的终结点的数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-211">Current number of endpoints registered in the Mobility Service</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-212">Currently Active Session Count with Active Presence Subscriptions</span><span class="sxs-lookup"><span data-stu-id="fb32a-212">Currently Active Session Count with Active Presence Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="fb32a-213">包含活动状态订阅的当前活动会话的数目</span><span class="sxs-lookup"><span data-stu-id="fb32a-213">The number of currently active sessions with active presence subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-214">Push Notification Requests Failed/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-214">Push Notification Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-215">每秒失败的推送通知数</span><span class="sxs-lookup"><span data-stu-id="fb32a-215">The per second rate of failed push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-216">Push Notification Requests Succeeded/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-216">Push Notification Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-217">每秒成功的推送通知数</span><span class="sxs-lookup"><span data-stu-id="fb32a-217">The per second rate of successful push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-218">Push Notification Requests Throttled/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-218">Push Notification Requests Throttled/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-219">每秒阻止的推送通知数</span><span class="sxs-lookup"><span data-stu-id="fb32a-219">The per second rate of throttled push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-220">Push Notification Requests/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-220">Push Notification Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-221">每秒发送的推送通知数</span><span class="sxs-lookup"><span data-stu-id="fb32a-221">The per second rate of sent push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-222">Requests Failed/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-222">Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-223">每秒失败的请求数</span><span class="sxs-lookup"><span data-stu-id="fb32a-223">The per second rate of failed requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-224">Requests Received/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-224">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-225">每秒收到的请求数</span><span class="sxs-lookup"><span data-stu-id="fb32a-225">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-226">Requests Rejected/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-226">Requests Rejected/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-227">每秒拒绝的请求数</span><span class="sxs-lookup"><span data-stu-id="fb32a-227">The per second rate of rejected requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-228">Requests Succeeded/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-228">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-229">每秒成功的请求数</span><span class="sxs-lookup"><span data-stu-id="fb32a-229">The per second rate of successful requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-230">Succeeded Initiate Session Requests/Second</span><span class="sxs-lookup"><span data-stu-id="fb32a-230">Succeeded Initiate Session Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="fb32a-p102">每秒成功的 Get Location 请求数。启动会话的请求占用了服务器上大部分 CPU。支持的峰值负载为 12/秒。可持续性依赖于服务器上的其他负载。启动会话通常意味着用户登录已注销很长一段时间。</span><span class="sxs-lookup"><span data-stu-id="fb32a-p102">The per second rate of successful Get Location requests. Requests to initiate a session consume the most CPU on the server. Peak supported load is 12/second. Sustainability depends on other loads on the server. Initiate a session typically means a sign-in for a user that has been signed out for an extended period of time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-236">Total Declined Inbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="fb32a-236">Total Declined Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="fb32a-237">拒绝的入站语音呼叫总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-237">The total number of inbound voice calls that were declined</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-238">Total Failed Inbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="fb32a-238">Total Failed Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="fb32a-239">失败的入站语音呼叫总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-239">The total number of inbound voice calls that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-240">Total Failed Outbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="fb32a-240">Total Failed Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="fb32a-241">失败的出站语音呼叫总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-241">The total number of outbound voice calls that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-242">Total number of sessions terminated by user</span><span class="sxs-lookup"><span data-stu-id="fb32a-242">Total number of sessions terminated by user</span></span></p></td>
<td><p><span data-ttu-id="fb32a-243">用户终止的会话总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-243">The total number of sessions terminated by users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-244">Total Push Notification Requests</span><span class="sxs-lookup"><span data-stu-id="fb32a-244">Total Push Notification Requests</span></span></p></td>
<td><p><span data-ttu-id="fb32a-245">推送通知请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-245">The total number of push notification requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-246">Total Push Notification Requests Failed</span><span class="sxs-lookup"><span data-stu-id="fb32a-246">Total Push Notification Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="fb32a-247">失败的推送通知请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-247">The total number of push notification requests that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-248">Total Push Notification Requests Succeeded</span><span class="sxs-lookup"><span data-stu-id="fb32a-248">Total Push Notification Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="fb32a-249">成功的推送通知请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-249">The total number of push notification requests that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-250">Total Push Notification Requests Throttled</span><span class="sxs-lookup"><span data-stu-id="fb32a-250">Total Push Notification Requests Throttled</span></span></p></td>
<td><p><span data-ttu-id="fb32a-251">阻止的推送通知请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-251">The total number of push notification requests that were throttled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-252">Total Requests Failed</span><span class="sxs-lookup"><span data-stu-id="fb32a-252">Total Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="fb32a-253">失败的请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-253">The total number of requests that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-254">Total Requests received on the Command Channel</span><span class="sxs-lookup"><span data-stu-id="fb32a-254">Total Requests received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="fb32a-255">命令通道上收到的请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-255">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-256">Total Requests Rejected</span><span class="sxs-lookup"><span data-stu-id="fb32a-256">Total Requests Rejected</span></span></p></td>
<td><p><span data-ttu-id="fb32a-257">拒绝的请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-257">The total number of requests that were rejected</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-258">Total Requests Succeeded</span><span class="sxs-lookup"><span data-stu-id="fb32a-258">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="fb32a-259">成功发送给 Mobility Service 的请求总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-259">The total number of requests made to the Mobility Service that succeeded</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-260">Total Session Initiated Count</span><span class="sxs-lookup"><span data-stu-id="fb32a-260">Total Session Initiated Count</span></span></p></td>
<td><p><span data-ttu-id="fb32a-261">自启动 Mobility Service 后启动的会话总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-261">The total number of sessions that were initiated since the Mobility Service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-262">Total Sessions Terminated Because of User Idle Timeout</span><span class="sxs-lookup"><span data-stu-id="fb32a-262">Total Sessions Terminated Because of User Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="fb32a-263">因用户空闲超时终止的会话总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-263">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb32a-264">Total Successful Inbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="fb32a-264">Total Successful Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="fb32a-265">成功的入站语音呼叫总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-265">The total number of inbound voice calls that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb32a-266">Total Successful Outbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="fb32a-266">Total Successful Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="fb32a-267">成功的出站语音呼叫总数</span><span class="sxs-lookup"><span data-stu-id="fb32a-267">The total number of outbound voice calls that were successful</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fb32a-268">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb32a-268">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

