---
title: 解释结果
description: 解释结果。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Interpreting the Results
ms:assetid: dd7f199f-7075-4d88-bb84-49a7e05eb593
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945608(v=OCS.15)
ms:contentKeyID: 51541433
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8342a1ec1e15e42852fc5293f87342e98587a60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443172"
---
# <a name="interpreting-the-results"></a><span data-ttu-id="636d7-103">解释结果</span><span class="sxs-lookup"><span data-stu-id="636d7-103">Interpreting the Results</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="636d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="636d7-104">

<span> </span></span></span>

<span data-ttu-id="636d7-105">_**主题上次修改时间：** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="636d7-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="636d7-106">Lync Server 2013 应力和性能工具 ( # A0) 具有许多计数器，您可以使用这些计数器来了解客户端正在执行的操作以及它是否会遇到问题。</span><span class="sxs-lookup"><span data-stu-id="636d7-106">The Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) has many counters that you can use to understand what the client is doing and whether it is encountering issues.</span></span>

<div>

## <a name="client-counters"></a><span data-ttu-id="636d7-107">客户端计数器</span><span class="sxs-lookup"><span data-stu-id="636d7-107">Client Counters</span></span>

<span data-ttu-id="636d7-108">正在运行的 LyncPerfTool.exe 的每个实例都具有计数器的单独实例。</span><span class="sxs-lookup"><span data-stu-id="636d7-108">Each instance of LyncPerfTool.exe that is running has a separate instance of the counters.</span></span> <span data-ttu-id="636d7-109">每个实例均按其进程 ID 命名。</span><span class="sxs-lookup"><span data-stu-id="636d7-109">Each instance is named by its process ID.</span></span>

<span data-ttu-id="636d7-110">如果客户端超载，可能会出现问题。</span><span class="sxs-lookup"><span data-stu-id="636d7-110">If the clients are overloaded, issues can occur.</span></span> <span data-ttu-id="636d7-111">若要防止这些问题，请执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="636d7-111">To prevent these issues, do the following:</span></span>

1.  <span data-ttu-id="636d7-112">监视客户端计算机上的 CPU 和内存使用情况。</span><span class="sxs-lookup"><span data-stu-id="636d7-112">Monitor the CPU and the memory usage on the client computers.</span></span> <span data-ttu-id="636d7-113">如果 CPU 持续超过90%，请减少用户数。</span><span class="sxs-lookup"><span data-stu-id="636d7-113">If the CPU is consistently above 90 percent, reduce the number of users.</span></span>

2.  <span data-ttu-id="636d7-114">如果内存占用量较高，则当页面文件不够大时，可能会遇到问题。</span><span class="sxs-lookup"><span data-stu-id="636d7-114">If the memory footprint is high, you could run into issues if the page file is not big enough.</span></span> <span data-ttu-id="636d7-115">验证确认费用未达到计算机的限制。</span><span class="sxs-lookup"><span data-stu-id="636d7-115">Verify that the Commit Charge is not hitting the limit on the computer.</span></span> <span data-ttu-id="636d7-116">如果您运行的是内存限制，请考虑增加页面文件大小或减少用户数</span><span class="sxs-lookup"><span data-stu-id="636d7-116">If you are running into memory limits, consider increasing the page file size or reducing the number of users</span></span>

<span data-ttu-id="636d7-117">下表列出了关键 LyncPerfTool 性能计数器。</span><span class="sxs-lookup"><span data-stu-id="636d7-117">The following tables list the key LyncPerfTool performance counters.</span></span>

<span data-ttu-id="636d7-118">**常规信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-118">**General Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-119"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-119"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-120"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-120"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-121">分钟花费的时间</span><span class="sxs-lookup"><span data-stu-id="636d7-121">Time Spent in Minutes</span></span></p></td>
<td><p><span data-ttu-id="636d7-122">启动流程后所花费的时间。</span><span class="sxs-lookup"><span data-stu-id="636d7-122">Time spent since the process was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-123">活动终结点</span><span class="sxs-lookup"><span data-stu-id="636d7-123">Active Endpoints</span></span></p></td>
<td><p><span data-ttu-id="636d7-124">当前连接到服务器的终结点的数量。</span><span class="sxs-lookup"><span data-stu-id="636d7-124">Number of endpoints currently connected to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-125">失败的登录</span><span class="sxs-lookup"><span data-stu-id="636d7-125">Failed Logons</span></span></p></td>
<td><p><span data-ttu-id="636d7-126">终结点登录失败总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-126">Total number of endpoint sign-in failures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-127">登录尝试</span><span class="sxs-lookup"><span data-stu-id="636d7-127">Logon Attempts</span></span></p></td>
<td><p><span data-ttu-id="636d7-128">终结点登录尝试的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-128">Total number of endpoint sign-in attempts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-129">终结点断开连接</span><span class="sxs-lookup"><span data-stu-id="636d7-129">Endpoints Disconnected</span></span></p></td>
<td><p><span data-ttu-id="636d7-130">已断开连接的终结点的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-130">Total number of endpoints that have been disconnected.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-131">**状态信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-131">**Presence Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-132"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-132"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-133"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-133"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-134">SetPresence 通话</span><span class="sxs-lookup"><span data-stu-id="636d7-134">SetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="636d7-135">联机状态更改尝试总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-135">Total number of presence change attempts.</span></span> <span data-ttu-id="636d7-136">对于不同类型的状态更改，请参阅 SetPresence (状态类型) 调用性能计数器。</span><span class="sxs-lookup"><span data-stu-id="636d7-136">For different types of presence changes, see the SetPresence (Presence Type) Calls Performance Counter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-137">SetPresence 的 NNN 响应</span><span class="sxs-lookup"><span data-stu-id="636d7-137">NNN Responses for SetPresence</span></span></p></td>
<td><p><span data-ttu-id="636d7-138">从服务器接收的 nnn 响应代码的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-138">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-139">GetPresence 通话</span><span class="sxs-lookup"><span data-stu-id="636d7-139">GetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="636d7-140">获取状态请求尝试的总次数。</span><span class="sxs-lookup"><span data-stu-id="636d7-140">Total number of get presence request attempts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-141">GetPresence 的 NNN 响应</span><span class="sxs-lookup"><span data-stu-id="636d7-141">NNN Responses for GetPresence</span></span></p></td>
<td><p><span data-ttu-id="636d7-142">从服务器接收的 nnn 响应代码的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-142">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-143">**通讯簿服务信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-143">**Address Book service Information**</span></span>

<span data-ttu-id="636d7-144">此类别包含用于监视通讯簿服务 (ABS) 文件下载和通讯簿 Web 查询服务请求的计数器。</span><span class="sxs-lookup"><span data-stu-id="636d7-144">This category includes counters used to monitor Address Book service (ABS) file downloads and Address Book Web Query service requests.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-145"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-145"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-146"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-146"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-147">已尝试绝对值完整/增量文件下载</span><span class="sxs-lookup"><span data-stu-id="636d7-147">ABS Full/Delta File Downloads Attempted</span></span></p></td>
<td><p><span data-ttu-id="636d7-148">已尝试的完整或增量文件下载请求的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-148">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-149">ABS 完整/增量文件下载成功</span><span class="sxs-lookup"><span data-stu-id="636d7-149">ABS Full/Delta File Downloads Succeeded</span></span></p></td>
<td><p><span data-ttu-id="636d7-150">已尝试的完整或增量文件下载请求的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-150">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-151">通讯簿 Web 查询服务相关计数器</span><span class="sxs-lookup"><span data-stu-id="636d7-151">Address Book Web Query service related counters</span></span></p></td>
<td><p><span data-ttu-id="636d7-152">通讯簿文件下载相关计数器。</span><span class="sxs-lookup"><span data-stu-id="636d7-152">Address book file download related counters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-153">尝试进行 ABS WS 呼叫</span><span class="sxs-lookup"><span data-stu-id="636d7-153">ABS WS Calls attempted</span></span></p></td>
<td><p><span data-ttu-id="636d7-154">尝试的通讯簿 Web 查询服务请求总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-154">Total number of Address Book Web Query service requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-155">ABS WS 呼叫成功</span><span class="sxs-lookup"><span data-stu-id="636d7-155">ABS WS Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="636d7-156">返回成功响应代码的通讯簿 Web 查询服务请求的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-156">Total number of Address Book Web Query service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-157">ABS WS 呼叫失败</span><span class="sxs-lookup"><span data-stu-id="636d7-157">ABS WS Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="636d7-158">返回错误响应代码的通讯簿 Web 查询服务请求的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-158">Total number of Address Book Web Query service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-159">**通讯组列表 (DL) 信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-159">**Distribution List (DL) Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-160"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-160"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-161"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-161"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-162">已尝试呼叫</span><span class="sxs-lookup"><span data-stu-id="636d7-162">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="636d7-163">尝试的通讯组列表扩展 (DLX) web 服务请求的总数量。</span><span class="sxs-lookup"><span data-stu-id="636d7-163">Total number of distribution list expansion (DLX) web service requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-164">通话成功</span><span class="sxs-lookup"><span data-stu-id="636d7-164">Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="636d7-165">返回成功响应代码的 DLX web 服务请求的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-165">Total number of DLX web service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-166">呼叫失败</span><span class="sxs-lookup"><span data-stu-id="636d7-166">Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="636d7-167">返回了错误响应代码的 DLX web 服务请求的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-167">Total number of DLX web service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-168">**VoIP 基本信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-168">**VoIP Basic Information**</span></span>

<span data-ttu-id="636d7-169">在启用这些方案时，以下列出的性能计数器将列出所有基于语音的 IP (VoIP) 呼叫（包括中介服务器、A/V 会议服务器、边缘服务器、响应组应用程序和会议自动助理）的报告编号。</span><span class="sxs-lookup"><span data-stu-id="636d7-169">The performance counters listed below report numbers for all Voice over IP (VoIP) calls, including calls to Mediation Server, A/V Conferencing Server, Edge Server, Response Group application, and Conference Auto Attendant, when these scenarios are enabled.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-170"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-170"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-171"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-171"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-172">通话处于活动状态</span><span class="sxs-lookup"><span data-stu-id="636d7-172">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="636d7-173">当前正在进行的传入/传出语音呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-173">Total number of incoming/outgoing voice calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-174">通话终止</span><span class="sxs-lookup"><span data-stu-id="636d7-174">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="636d7-175">已终止的传入/传出语音通话总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-175">Total number of incoming/outgoing voice calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-176">通话被拒绝</span><span class="sxs-lookup"><span data-stu-id="636d7-176">Calls Declined</span></span></p></td>
<td><p><span data-ttu-id="636d7-177">已拒绝的传入语音呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-177">Total number of incoming voice calls declined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-178">已尝试拨入/拨出电话</span><span class="sxs-lookup"><span data-stu-id="636d7-178">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="636d7-179">已尝试传入/传出语音通话的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-179">Total number of incoming/outgoing voice calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-180">已建立传入/传出呼叫</span><span class="sxs-lookup"><span data-stu-id="636d7-180">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="636d7-181">已建立的传入/传出语音通话的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-181">Total number of incoming/outgoing voice calls established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-182">呼叫接收的 NNN</span><span class="sxs-lookup"><span data-stu-id="636d7-182">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="636d7-183">从服务器接收的 nnn 响应代码的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-183">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-184">VoIP 传递率 (% ) </span><span class="sxs-lookup"><span data-stu-id="636d7-184">VoIP Pass Rate (%)</span></span></p></td>
<td><p><span data-ttu-id="636d7-185">已建立通话总次数/尝试的通话总次数。</span><span class="sxs-lookup"><span data-stu-id="636d7-185">Total calls established/Total calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-186">**响应组服务呼叫信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-186">**Response Group service Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-187"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-187"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-188"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-188"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-189">通话处于活动状态</span><span class="sxs-lookup"><span data-stu-id="636d7-189">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="636d7-190">对响应组应用程序的活动呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-190">Total number of active calls to the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-191">已尝试呼叫</span><span class="sxs-lookup"><span data-stu-id="636d7-191">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="636d7-192">尝试的通话总次数。</span><span class="sxs-lookup"><span data-stu-id="636d7-192">Total number of calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-193">**即时消息 (IM) 呼叫信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-193">**Instant Messaging (IM) Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-194"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-194"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-195"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-195"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-196">通话处于活动状态</span><span class="sxs-lookup"><span data-stu-id="636d7-196">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="636d7-197">正在进行的传入/传出即时消息呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-197">Total number of ongoing incoming/outgoing instant messaging calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-198">通话终止</span><span class="sxs-lookup"><span data-stu-id="636d7-198">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="636d7-199">已终止的传入/传出即时消息呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-199">Total number of incoming/outgoing instant messaging calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-200">呼叫接收的 NNN</span><span class="sxs-lookup"><span data-stu-id="636d7-200">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="636d7-201">从服务器接收的 nnn 响应代码的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-201">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-202">接收/发送的 IM 消息</span><span class="sxs-lookup"><span data-stu-id="636d7-202">IM Messages Received/Sent</span></span></p></td>
<td><p><span data-ttu-id="636d7-203">所有会话的已接收或已发送邮件的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-203">Total number of messages received or sent for all sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-204">已尝试拨入/拨出电话</span><span class="sxs-lookup"><span data-stu-id="636d7-204">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="636d7-205">尝试的传入/传出即时消息呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-205">Total number of incoming/outgoing instant messaging calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-206">已建立传入/传出呼叫</span><span class="sxs-lookup"><span data-stu-id="636d7-206">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="636d7-207">已建立的传入/传出即时消息呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-207">Total number of incoming/outgoing instant message calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-208">**应用共享呼叫信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-208">**App Sharing Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-209"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-209"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-210"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-210"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-211">通话处于活动状态</span><span class="sxs-lookup"><span data-stu-id="636d7-211">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="636d7-212">正在进行的传入/传出应用程序共享呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-212">Total number of ongoing incoming/outgoing application sharing calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-213">通话终止</span><span class="sxs-lookup"><span data-stu-id="636d7-213">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="636d7-214">已终止的传入/传出应用程序共享呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-214">Total number of incoming/outgoing application sharing calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-215">呼叫接收的 NNN</span><span class="sxs-lookup"><span data-stu-id="636d7-215">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="636d7-216">从服务器接收的 nnn 响应代码的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-216">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-217">已尝试拨入/拨出电话</span><span class="sxs-lookup"><span data-stu-id="636d7-217">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="636d7-218">尝试的传入/传出应用程序共享呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-218">Total number of incoming/outgoing application sharing calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-219">已建立传入/传出呼叫</span><span class="sxs-lookup"><span data-stu-id="636d7-219">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="636d7-220">已建立的传入/传出应用程序共享呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-220">Total number of incoming/outgoing application sharing calls established.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-221">**CAA 通话信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-221">**CAA Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-222"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-222"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-223"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-223"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-224">通话处于活动状态</span><span class="sxs-lookup"><span data-stu-id="636d7-224">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="636d7-225">当前正在进行的 (PSTN) 呼叫的传入/传出公共交换式电话网络总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-225">Total number of incoming/outgoing public switched telephone network (PSTN) calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-226">通话终止</span><span class="sxs-lookup"><span data-stu-id="636d7-226">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="636d7-227">已终止的传入/传出 PSTN 呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-227">Total number of incoming/outgoing PSTN calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-228">已尝试拨入/拨出电话</span><span class="sxs-lookup"><span data-stu-id="636d7-228">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="636d7-229">尝试的传入/传出 PSTN 呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-229">Total number of incoming/outgoing PSTN calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-230">已建立传入/传出呼叫</span><span class="sxs-lookup"><span data-stu-id="636d7-230">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="636d7-231">已建立的传入/传出 PSTN 呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-231">Total number of incoming/outgoing PSTN calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-232">**会议信息**</span><span class="sxs-lookup"><span data-stu-id="636d7-232">**Conference Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-233"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-233"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-234"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-234"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-235">活动即时消息会议</span><span class="sxs-lookup"><span data-stu-id="636d7-235">Active Instant Messaging Conferences</span></span></p></td>
<td><p><span data-ttu-id="636d7-236">正在进行的即时消息会议总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-236">Total number of ongoing instant messaging conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-237">活动音频/视频会议</span><span class="sxs-lookup"><span data-stu-id="636d7-237">Active Audio/Video Conferences</span></span></p></td>
<td><p><span data-ttu-id="636d7-238"> (A/V) 会议的正在进行的音频/视频的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-238">Total number of ongoing audio/video (A/V) conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-239">活动应用程序共享会议</span><span class="sxs-lookup"><span data-stu-id="636d7-239">Active Application Sharing Conferences</span></span></p></td>
<td><p><span data-ttu-id="636d7-240">正在进行的应用程序共享会议总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-240">Total number of ongoing application sharing conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-241">参与者的人数</span><span class="sxs-lookup"><span data-stu-id="636d7-241">Number of Participants</span></span></p></td>
<td><p><span data-ttu-id="636d7-242">当前连接到会议的参与者总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-242">Total number of participants currently connected to conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636d7-243">会议计划失败</span><span class="sxs-lookup"><span data-stu-id="636d7-243">Conference Schedule Failure</span></span></p></td>
<td><p><span data-ttu-id="636d7-244">尝试安排会议时失败的总次数。</span><span class="sxs-lookup"><span data-stu-id="636d7-244">Total number of failures while trying to schedule a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-245">加入会议失败</span><span class="sxs-lookup"><span data-stu-id="636d7-245">Join Conference Failure</span></span></p></td>
<td><p><span data-ttu-id="636d7-246">尝试连接到会议时失败的总次数。</span><span class="sxs-lookup"><span data-stu-id="636d7-246">Total number of failures while trying to connect to a conference.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="636d7-247">**UCWA 客户端计数器**</span><span class="sxs-lookup"><span data-stu-id="636d7-247">**UCWA Client Counters**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636d7-248"><strong>性能计数器</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-248"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="636d7-249"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="636d7-249"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636d7-250">已成功联接的 IMMCU 总数</span><span class="sxs-lookup"><span data-stu-id="636d7-250">Total Number of IMMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="636d7-251">已加入的即时消息会议的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-251">Total number of instant messaging conferences joined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636d7-252">已成功联接的 DMCU 总数</span><span class="sxs-lookup"><span data-stu-id="636d7-252">Total Number of DMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="636d7-253">已加入/V 会议的总数。</span><span class="sxs-lookup"><span data-stu-id="636d7-253">Total number of A/V conferences joined.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="636d7-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="636d7-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

