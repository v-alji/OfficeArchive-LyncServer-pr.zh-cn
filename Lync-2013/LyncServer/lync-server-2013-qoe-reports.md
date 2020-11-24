---
title: Lync Server 2013： QoE 报表
description: Lync Server 2013： QoE 报表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392101"
---
# <a name="qoe-reports-in-lync-server-2013"></a><span data-ttu-id="a8560-103">Lync Server 2013 中的 QoE 报表</span><span class="sxs-lookup"><span data-stu-id="a8560-103">QoE reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8560-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8560-104">

<span> </span></span></span>

<span data-ttu-id="a8560-105">_**主题上次修改时间：** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="a8560-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<div>

## <a name="qoe-summarytrend-reports"></a><span data-ttu-id="a8560-106">QoE 摘要/趋势报告</span><span class="sxs-lookup"><span data-stu-id="a8560-106">QoE summary/trend reports</span></span>

<span data-ttu-id="a8560-107">QoE 摘要/趋势报表可用于查找每天的高峰使用时间和在这些时间内检查媒体质量，以帮助确保你的组织的网络资源足够有效。</span><span class="sxs-lookup"><span data-stu-id="a8560-107">The QoE summary/trends reports are useful for finding the peak usage times of day and examining the media quality during those times to help assure that your organization's network resources are sufficient.</span></span> <span data-ttu-id="a8560-108">你的组织还可以使用报表中提供的许多筛选器来隔离特定位置、客户端和设备类型以及服务器的性能数字。</span><span class="sxs-lookup"><span data-stu-id="a8560-108">Your organization can also use the many filters available in the report to isolate performance numbers for certain locations, client and device types, and servers.</span></span>

<span data-ttu-id="a8560-109">QoE 摘要/趋势报告包括：</span><span class="sxs-lookup"><span data-stu-id="a8560-109">QoE summary/trend reports consist of:</span></span>

  - <span data-ttu-id="a8560-110">UC 到 UC 摘要/趋势报告</span><span class="sxs-lookup"><span data-stu-id="a8560-110">UC-to-UC Summary/Trend Report</span></span>

  - <span data-ttu-id="a8560-111">PSTN 摘要/趋势报告</span><span class="sxs-lookup"><span data-stu-id="a8560-111">PSTN Summary/Trend Report</span></span>

  - <span data-ttu-id="a8560-112">会议摘要/趋势报告</span><span class="sxs-lookup"><span data-stu-id="a8560-112">Conference Summary/Trend Report</span></span>

</div>

<div>

## <a name="qoe-performance-reports"></a><span data-ttu-id="a8560-113">QoE 性能报告</span><span class="sxs-lookup"><span data-stu-id="a8560-113">QoE performance reports</span></span>

<span data-ttu-id="a8560-114">QoE 性能报告提供了有关三个报表的详细信息，这些报表专注于中介服务器、A/V 会议服务器和终结点位置的 QoE 性能。</span><span class="sxs-lookup"><span data-stu-id="a8560-114">QoE performance reports provide details about the three reports that concentrate on the QoE performance of Mediation Servers, A/V Conferencing Servers, and endpoint locations.</span></span>

</div>

<div>

## <a name="mediation-server-performance-report"></a><span data-ttu-id="a8560-115">中介服务器性能报告</span><span class="sxs-lookup"><span data-stu-id="a8560-115">Mediation server performance report</span></span>

<span data-ttu-id="a8560-116">中介服务器性能报告列出了在指定时间段内由一个或多个中介实现的指标。</span><span class="sxs-lookup"><span data-stu-id="a8560-116">The Mediation Server Performance report lists the metrics achieved by one or more Mediation during the specified time period.</span></span> <span data-ttu-id="a8560-117">统一通信的指标 (UC) -中介服务器腿和每个通话的中介服务器到网关腿分别报告。</span><span class="sxs-lookup"><span data-stu-id="a8560-117">The metrics for the unified communications (UC)-to-Mediation Server leg and the Mediation Server-to-Gateway leg of each call are reported separately.</span></span> <span data-ttu-id="a8560-118">使用此报告比较组织的各种中介服务器的数量和性能。</span><span class="sxs-lookup"><span data-stu-id="a8560-118">Use this report to compare the volume and performance of your organization's various Mediation Servers.</span></span>

<span data-ttu-id="a8560-119">对于每个中介服务器 (和每个呼叫腿) ，报表将显示以下内容：</span><span class="sxs-lookup"><span data-stu-id="a8560-119">For each Mediation Server (and for each call leg), the report displays the following:</span></span>

  - <span data-ttu-id="a8560-120">通话的数量</span><span class="sxs-lookup"><span data-stu-id="a8560-120">Number of calls</span></span>

  - <span data-ttu-id="a8560-121">丢包</span><span class="sxs-lookup"><span data-stu-id="a8560-121">Packet Loss</span></span>

  - <span data-ttu-id="a8560-122">往返行程时间</span><span class="sxs-lookup"><span data-stu-id="a8560-122">Round Trip Time</span></span>

  - <span data-ttu-id="a8560-123">抖动</span><span class="sxs-lookup"><span data-stu-id="a8560-123">Jitter</span></span>

  - <span data-ttu-id="a8560-124">按 MOS) 的观点分数 (</span><span class="sxs-lookup"><span data-stu-id="a8560-124">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="a8560-125">发送 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-125">Sending MOS</span></span>

  - <span data-ttu-id="a8560-126">侦听 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-126">Listening MOS</span></span>

  - <span data-ttu-id="a8560-127">网络 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-127">Network MOS</span></span>

  - <span data-ttu-id="a8560-128">网络 MOS 性能下降</span><span class="sxs-lookup"><span data-stu-id="a8560-128">Network MOS Degradation</span></span>

  - <span data-ttu-id="a8560-129">回音返回</span><span class="sxs-lookup"><span data-stu-id="a8560-129">Echo Return</span></span>

  - <span data-ttu-id="a8560-130">信号级别</span><span class="sxs-lookup"><span data-stu-id="a8560-130">Signal Level</span></span>

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a><span data-ttu-id="a8560-131">A/V 会议服务器性能报告</span><span class="sxs-lookup"><span data-stu-id="a8560-131">A/V conferencing server performance report</span></span>

<span data-ttu-id="a8560-132">A/V 会议服务器性能报告提供指定时间段内由一个或多个 A/V 会议服务器实现的指标的列表。</span><span class="sxs-lookup"><span data-stu-id="a8560-132">The A/V Conferencing Server Performance report provides lists of metrics achieved by one or more A/V Conferencing Servers during the specified time period.</span></span> <span data-ttu-id="a8560-133">此报告可用于比较组织的各种 A/V 会议服务器的数量和性能。</span><span class="sxs-lookup"><span data-stu-id="a8560-133">This report can be used to compare the volume and performance of your organization’s various A/V Conferencing Servers.</span></span> <span data-ttu-id="a8560-134">你的组织还可以隔离报表以仅显示特定客户端类型（如 Lync 客户端或 PSTN 客户端）的体验。</span><span class="sxs-lookup"><span data-stu-id="a8560-134">Your organization can also isolate the report to show only the experience for specific client types, such as Lync clients or PSTN clients.</span></span>

<span data-ttu-id="a8560-135">对于每个 A/V 会议服务器，报表显示以下内容：</span><span class="sxs-lookup"><span data-stu-id="a8560-135">For each A/V Conferencing Server, the report displays the following:</span></span>

  - <span data-ttu-id="a8560-136">会议数</span><span class="sxs-lookup"><span data-stu-id="a8560-136">Number of conferences</span></span>

  - <span data-ttu-id="a8560-137">丢包</span><span class="sxs-lookup"><span data-stu-id="a8560-137">Packet Loss</span></span>

  - <span data-ttu-id="a8560-138">往返行程时间</span><span class="sxs-lookup"><span data-stu-id="a8560-138">Round Trip Time</span></span>

  - <span data-ttu-id="a8560-139">抖动</span><span class="sxs-lookup"><span data-stu-id="a8560-139">Jitter</span></span>

  - <span data-ttu-id="a8560-140">按 MOS) 的观点分数 (</span><span class="sxs-lookup"><span data-stu-id="a8560-140">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="a8560-141">发送 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-141">Sending MOS</span></span>

  - <span data-ttu-id="a8560-142">侦听 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-142">Listening MOS</span></span>

  - <span data-ttu-id="a8560-143">网络 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-143">Network MOS</span></span>

  - <span data-ttu-id="a8560-144">网络 MOS 性能下降</span><span class="sxs-lookup"><span data-stu-id="a8560-144">Network MOS Degradation</span></span>

  - <span data-ttu-id="a8560-145">回音返回</span><span class="sxs-lookup"><span data-stu-id="a8560-145">Echo Return</span></span>

  - <span data-ttu-id="a8560-146">信号级别</span><span class="sxs-lookup"><span data-stu-id="a8560-146">Signal Level</span></span>

</div>

<div>

## <a name="location-based-performance-report"></a><span data-ttu-id="a8560-147">基于位置的性能报告</span><span class="sxs-lookup"><span data-stu-id="a8560-147">Location-based performance report</span></span>

<span data-ttu-id="a8560-148">Location-Based 性能报告提供网络位置列表和每个位置的列表，显示每个预确定的质量范围内的呼叫数。</span><span class="sxs-lookup"><span data-stu-id="a8560-148">The Location-Based Performance report provides a list of network locations and for each location shows the number of calls in each pre-determined range of quality.</span></span> <span data-ttu-id="a8560-149">此报告的目标是提供对各种位置的组织电话通话的媒体质量的深入了解，以便您能够识别出较差的位置，并在组织的不同位置查看不同等级的媒体质量。</span><span class="sxs-lookup"><span data-stu-id="a8560-149">The goal of this report is to provide insight into the media quality of the bulk of your organization’s telephone calls for various locations so that you can identify poorly performing locations, and see the different grades of media quality in your organization’s different locations.</span></span>

<span data-ttu-id="a8560-150">显示报表时，将显示不同的度量表，即组织决定报告的每个指标的一个表。</span><span class="sxs-lookup"><span data-stu-id="a8560-150">When displaying the report, different tables of metrics appear—one table for each metric your organization decides to report on.</span></span> <span data-ttu-id="a8560-151">你可以从此报表的以下指标中进行选择：</span><span class="sxs-lookup"><span data-stu-id="a8560-151">You can choose from the following metrics for this report:</span></span>

  - <span data-ttu-id="a8560-152">按 MOS) 的观点分数 (</span><span class="sxs-lookup"><span data-stu-id="a8560-152">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="a8560-153">网络 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-153">Network MOS</span></span>

  - <span data-ttu-id="a8560-154">网络 MOS 性能下降</span><span class="sxs-lookup"><span data-stu-id="a8560-154">Network MOS Degradation</span></span>

  - <span data-ttu-id="a8560-155">发送 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-155">Sending MOS</span></span>

  - <span data-ttu-id="a8560-156">侦听 MOS</span><span class="sxs-lookup"><span data-stu-id="a8560-156">Listening MOS</span></span>

  - <span data-ttu-id="a8560-157">丢包</span><span class="sxs-lookup"><span data-stu-id="a8560-157">Packet Loss</span></span>

  - <span data-ttu-id="a8560-158">抖动</span><span class="sxs-lookup"><span data-stu-id="a8560-158">Jitter</span></span>

  - <span data-ttu-id="a8560-159">滞后</span><span class="sxs-lookup"><span data-stu-id="a8560-159">Latency</span></span>

<span data-ttu-id="a8560-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8560-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

