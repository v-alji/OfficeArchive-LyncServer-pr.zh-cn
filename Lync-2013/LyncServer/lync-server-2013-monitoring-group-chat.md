---
title: Lync Server 2013：监视群组聊天
description: Lync Server 2013：监视群组聊天。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring group chat
ms:assetid: bddcf0be-ebf3-46bc-90c7-2576877734fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720924(v=OCS.15)
ms:contentKeyID: 63969648
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 625e45f455e8dba50a5fa64240b62cb010623d16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425421"
---
# <a name="monitoring-group-chat-in-lync-server-2013"></a><span data-ttu-id="6db56-103">在 Lync Server 2013 中监视群组聊天</span><span class="sxs-lookup"><span data-stu-id="6db56-103">Monitoring group chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6db56-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6db56-104">

<span> </span></span></span>

<span data-ttu-id="6db56-105">_**主题上次修改时间：** 2014-08-04_</span><span class="sxs-lookup"><span data-stu-id="6db56-105">_**Topic Last Modified:** 2014-08-04_</span></span>

<span data-ttu-id="6db56-106">强烈建议运行 Microsoft 下载中心提供的最新 [累积服务器更新安装程序](https://support.microsoft.com/kb/968802) ，以提高性能。</span><span class="sxs-lookup"><span data-stu-id="6db56-106">We highly recommend running the most recent [Cumulative Server Update Installer](https://support.microsoft.com/kb/968802) available on the Microsoft Download Center for performance improvements.</span></span>

<span data-ttu-id="6db56-107">假设你正在运行最新的累积更新，请使用以下压力测试表来了解你的群组聊天服务器是否在最佳运行状况下运行。</span><span class="sxs-lookup"><span data-stu-id="6db56-107">Assuming you are running latest cumulative update, use the following stress test table for metrics to understand if your Group Chat Servers are running at optimal health.</span></span>

### <a name="test-environment-and-user-model"></a><span data-ttu-id="6db56-108">测试环境和用户模型</span><span class="sxs-lookup"><span data-stu-id="6db56-108">Test environment and user model</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6db56-109">群组聊天池中的三个群组聊天服务器，每个服务器都有 8 GB 内存和8个处理器。</span><span class="sxs-lookup"><span data-stu-id="6db56-109">Three Group Chat Servers in a Group Chat pool, each with 8 GB memory and 8 processors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6db56-110">企业版中的两个 Lync Server 2013 前端。</span><span class="sxs-lookup"><span data-stu-id="6db56-110">Two Lync Server 2013 Front Ends in Enterprise Edition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6db56-111">60000多个群组聊天服务器上的并行用户。</span><span class="sxs-lookup"><span data-stu-id="6db56-111">60,000 concurrent users across three Group Chat Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6db56-112">25000通道由群组聊天池托管。</span><span class="sxs-lookup"><span data-stu-id="6db56-112">25,000 channels hosted by Group Chat Pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6db56-113">频道大小：</span><span class="sxs-lookup"><span data-stu-id="6db56-113">Channel Size:</span></span></p>
<ul>
<li><p><span data-ttu-id="6db56-114">小频道大小：30</span><span class="sxs-lookup"><span data-stu-id="6db56-114">Small Channel Size: 30</span></span></p></li>
<li><p><span data-ttu-id="6db56-115">中等频道大小：150</span><span class="sxs-lookup"><span data-stu-id="6db56-115">Medium Channel Size: 150</span></span></p></li>
<li><p><span data-ttu-id="6db56-116">大频道大小：2500</span><span class="sxs-lookup"><span data-stu-id="6db56-116">Large Channel Size: 2500</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6db56-117">频道计数：</span><span class="sxs-lookup"><span data-stu-id="6db56-117">Channel Count:</span></span></p>
<ul>
<li><p><span data-ttu-id="6db56-118">数字小型频道：24000</span><span class="sxs-lookup"><span data-stu-id="6db56-118">Number small channels: 24,000</span></span></p></li>
<li><p><span data-ttu-id="6db56-119">数字中等通道800</span><span class="sxs-lookup"><span data-stu-id="6db56-119">Number medium channels 800</span></span></p></li>
<li><p><span data-ttu-id="6db56-120">大量频道24</span><span class="sxs-lookup"><span data-stu-id="6db56-120">Number large channels 24</span></span></p></li>
<li><p><span data-ttu-id="6db56-121">通道24824总数</span><span class="sxs-lookup"><span data-stu-id="6db56-121">Total Channels 24,824</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6db56-122">邀请频道：</span><span class="sxs-lookup"><span data-stu-id="6db56-122">Invite channels:</span></span></p>
<ul>
<li><p><span data-ttu-id="6db56-123">频道的一半邀请频道</span><span class="sxs-lookup"><span data-stu-id="6db56-123">Half the channels were invite channels</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6db56-124">用户加入的频道数：</span><span class="sxs-lookup"><span data-stu-id="6db56-124">Number of channels a user joins:</span></span></p>
<ul>
<li><p><span data-ttu-id="6db56-125">小：12</span><span class="sxs-lookup"><span data-stu-id="6db56-125">Small: 12</span></span></p></li>
<li><p><span data-ttu-id="6db56-126">中等：2</span><span class="sxs-lookup"><span data-stu-id="6db56-126">Medium: 2</span></span></p></li>
<li><p><span data-ttu-id="6db56-127">大：1</span><span class="sxs-lookup"><span data-stu-id="6db56-127">Large: 1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6db56-128">联接费率：</span><span class="sxs-lookup"><span data-stu-id="6db56-128">Join rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="6db56-129">每台服务器10个总/秒、3.33/秒</span><span class="sxs-lookup"><span data-stu-id="6db56-129">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6db56-130">注销费率：</span><span class="sxs-lookup"><span data-stu-id="6db56-130">Logout rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="6db56-131">每台服务器10个总/秒、3.33/秒</span><span class="sxs-lookup"><span data-stu-id="6db56-131">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6db56-132">聊天费率：</span><span class="sxs-lookup"><span data-stu-id="6db56-132">Chat rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="6db56-133">每个服务器20总/秒、每个服务器 6.66/秒</span><span class="sxs-lookup"><span data-stu-id="6db56-133">20 total/second, 6.66/second per server</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="6db56-134">当使用不同的硬件规范或用户配置文件时，以下性能计数器数值可能会有所不同。</span><span class="sxs-lookup"><span data-stu-id="6db56-134">The following performance counter numbers will likely vary when different hardware specifications or user profiles are used.</span></span>



</div>

### <a name="performance-counter-to-be-monitored"></a><span data-ttu-id="6db56-135">要监视的性能计数器</span><span class="sxs-lookup"><span data-stu-id="6db56-135">Performance counter to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6db56-136">性能计数器</span><span class="sxs-lookup"><span data-stu-id="6db56-136">Performance Counter</span></span></th>
<th><span data-ttu-id="6db56-137">01b</span><span class="sxs-lookup"><span data-stu-id="6db56-137">Thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6db56-138">处理 (ChannelService) &gt; 处理器时间</span><span class="sxs-lookup"><span data-stu-id="6db56-138">Process(ChannelService)-&gt;%Processor Time</span></span></p></td>
<td><p><span data-ttu-id="6db56-139">分钟：0</span><span class="sxs-lookup"><span data-stu-id="6db56-139">Min: 0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6db56-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6db56-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

