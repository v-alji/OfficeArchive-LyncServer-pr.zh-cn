---
title: 'Lync Server 2013： UserAgentDef table (QoE) '
description: Lync Server 2013： UserAgentDef table (QoE) 。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgentDef table (QoE)
ms:assetid: cfd8e3e0-4076-4162-9381-5276da8316d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205259(v=OCS.15)
ms:contentKeyID: 48185394
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8546a33e607524b23755e9abf3edb2d5e2e417d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439042"
---
# <a name="useragentdef-table-qoe-in-lync-server-2013"></a><span data-ttu-id="2d9c4-103">UserAgentDef 表 (Lync Server 2013 中的 QoE) </span><span class="sxs-lookup"><span data-stu-id="2d9c4-103">UserAgentDef table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d9c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d9c4-104">

<span> </span></span></span>

<span data-ttu-id="2d9c4-105">_**主题上次修改时间：** 2014-03-25_</span><span class="sxs-lookup"><span data-stu-id="2d9c4-105">_**Topic Last Modified:** 2014-03-25_</span></span>

<span data-ttu-id="2d9c4-106">UserAgentDef 表将用户代理标识符映射到代理的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="2d9c4-106">The UserAgentDef table maps user agent identifiers to the agent’s descriptive names.</span></span> <span data-ttu-id="2d9c4-107">用户代理是用于连接到 Microsoft Lync Server 2013 的软件客户端。</span><span class="sxs-lookup"><span data-stu-id="2d9c4-107">User agents are software clients used to connect to Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2d9c4-108">UAType</span><span class="sxs-lookup"><span data-stu-id="2d9c4-108">UAType</span></span></th>
<th><span data-ttu-id="2d9c4-109">UAName</span><span class="sxs-lookup"><span data-stu-id="2d9c4-109">UAName</span></span></th>
<th><span data-ttu-id="2d9c4-110">UACategory</span><span class="sxs-lookup"><span data-stu-id="2d9c4-110">UACategory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-111">1</span><span class="sxs-lookup"><span data-stu-id="2d9c4-111">1</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-112">MediationServer</span><span class="sxs-lookup"><span data-stu-id="2d9c4-112">MediationServer</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-113">MediationServer</span><span class="sxs-lookup"><span data-stu-id="2d9c4-113">MediationServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-114">2</span><span class="sxs-lookup"><span data-stu-id="2d9c4-114">2</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-115">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="2d9c4-115">AV-MCU</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-116">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="2d9c4-116">AV-MCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-117">4</span><span class="sxs-lookup"><span data-stu-id="2d9c4-117">4</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-118">OC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-118">OC</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-119">OC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-119">OC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-120">个</span><span class="sxs-lookup"><span data-stu-id="2d9c4-120">8</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-121">OCPhone</span><span class="sxs-lookup"><span data-stu-id="2d9c4-121">OCPhone</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-122">OCPhone</span><span class="sxs-lookup"><span data-stu-id="2d9c4-122">OCPhone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-123">utf-16</span><span class="sxs-lookup"><span data-stu-id="2d9c4-123">16</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-124">LMC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-124">LMC</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-125">LMC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-125">LMC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-126">32</span><span class="sxs-lookup"><span data-stu-id="2d9c4-126">32</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-127">DVT</span><span class="sxs-lookup"><span data-stu-id="2d9c4-127">DVT</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-128">DVT</span><span class="sxs-lookup"><span data-stu-id="2d9c4-128">DVT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-129">64</span><span class="sxs-lookup"><span data-stu-id="2d9c4-129">64</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-130">分钟</span><span class="sxs-lookup"><span data-stu-id="2d9c4-130">MM</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-131">分钟</span><span class="sxs-lookup"><span data-stu-id="2d9c4-131">MM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-132">64</span><span class="sxs-lookup"><span data-stu-id="2d9c4-132">64</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-133">MC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-133">MC</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-134">分钟</span><span class="sxs-lookup"><span data-stu-id="2d9c4-134">MM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-135">128</span><span class="sxs-lookup"><span data-stu-id="2d9c4-135">128</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-136">助理</span><span class="sxs-lookup"><span data-stu-id="2d9c4-136">Attendant</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-137">助理</span><span class="sxs-lookup"><span data-stu-id="2d9c4-137">Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-138">256</span><span class="sxs-lookup"><span data-stu-id="2d9c4-138">256</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-139">Conferencing_Announcement_Service_1 0</span><span class="sxs-lookup"><span data-stu-id="2d9c4-139">Conferencing_Announcement_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-140">而言</span><span class="sxs-lookup"><span data-stu-id="2d9c4-140">CAS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-141">512</span><span class="sxs-lookup"><span data-stu-id="2d9c4-141">512</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-142">Conferencing_Attendant_1 0</span><span class="sxs-lookup"><span data-stu-id="2d9c4-142">Conferencing_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-143">CAA</span><span class="sxs-lookup"><span data-stu-id="2d9c4-143">CAA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-144">512</span><span class="sxs-lookup"><span data-stu-id="2d9c4-144">512</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-145">Conference_Auto_Attendant_1 0</span><span class="sxs-lookup"><span data-stu-id="2d9c4-145">Conference_Auto_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-146">CAA</span><span class="sxs-lookup"><span data-stu-id="2d9c4-146">CAA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-147">1024</span><span class="sxs-lookup"><span data-stu-id="2d9c4-147">1024</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-148">Response_Group_Service</span><span class="sxs-lookup"><span data-stu-id="2d9c4-148">Response_Group_Service</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-149">RG</span><span class="sxs-lookup"><span data-stu-id="2d9c4-149">RGS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-150">1032</span><span class="sxs-lookup"><span data-stu-id="2d9c4-150">1032</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-151">Call_Park_Service_1 0</span><span class="sxs-lookup"><span data-stu-id="2d9c4-151">Call_Park_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-152">方面</span><span class="sxs-lookup"><span data-stu-id="2d9c4-152">CPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-153">1040</span><span class="sxs-lookup"><span data-stu-id="2d9c4-153">1040</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-154">Response_Group_Service Announcement_Service</span><span class="sxs-lookup"><span data-stu-id="2d9c4-154">Response_Group_Service Announcement_Service</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-155">方式</span><span class="sxs-lookup"><span data-stu-id="2d9c4-155">AS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-156">2048</span><span class="sxs-lookup"><span data-stu-id="2d9c4-156">2048</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-157">Microsoft Ccs</span><span class="sxs-lookup"><span data-stu-id="2d9c4-157">Microsoft.Rtc.Applications.Ccs</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-158">CCS</span><span class="sxs-lookup"><span data-stu-id="2d9c4-158">CCS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-159">16386</span><span class="sxs-lookup"><span data-stu-id="2d9c4-159">16386</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-160">CoMo</span><span class="sxs-lookup"><span data-stu-id="2d9c4-160">CoMo</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-161">CoMo</span><span class="sxs-lookup"><span data-stu-id="2d9c4-161">CoMo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-162">16387</span><span class="sxs-lookup"><span data-stu-id="2d9c4-162">16387</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-163">CWA</span><span class="sxs-lookup"><span data-stu-id="2d9c4-163">CWA</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-164">CWA</span><span class="sxs-lookup"><span data-stu-id="2d9c4-164">CWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-165">16388</span><span class="sxs-lookup"><span data-stu-id="2d9c4-165">16388</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-166">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="2d9c4-166">InboundRouting</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-167">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="2d9c4-167">InboundRouting</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-168">16389</span><span class="sxs-lookup"><span data-stu-id="2d9c4-168">16389</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-169">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="2d9c4-169">ComoSvc</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-170">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="2d9c4-170">ComoSvc</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-171">16393</span><span class="sxs-lookup"><span data-stu-id="2d9c4-171">16393</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-172">MSExchangeUM</span><span class="sxs-lookup"><span data-stu-id="2d9c4-172">MSExchangeUM</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-173">ExUM</span><span class="sxs-lookup"><span data-stu-id="2d9c4-173">ExUM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-174">16395</span><span class="sxs-lookup"><span data-stu-id="2d9c4-174">16395</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-175">ArchivingAgent</span><span class="sxs-lookup"><span data-stu-id="2d9c4-175">ArchivingAgent</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-176">ARCHAGENT</span><span class="sxs-lookup"><span data-stu-id="2d9c4-176">ARCHAGENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-177">16396</span><span class="sxs-lookup"><span data-stu-id="2d9c4-177">16396</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-178">短期</span><span class="sxs-lookup"><span data-stu-id="2d9c4-178">ST</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-179">短期</span><span class="sxs-lookup"><span data-stu-id="2d9c4-179">ST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-180">16397</span><span class="sxs-lookup"><span data-stu-id="2d9c4-180">16397</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-181">applicationsharing</span><span class="sxs-lookup"><span data-stu-id="2d9c4-181">applicationsharing</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-182">ASMCU</span><span class="sxs-lookup"><span data-stu-id="2d9c4-182">ASMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-183">16398</span><span class="sxs-lookup"><span data-stu-id="2d9c4-183">16398</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-184">WPLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-184">WPLync</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-185">WPLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-185">WPLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-186">16399</span><span class="sxs-lookup"><span data-stu-id="2d9c4-186">16399</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-187">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-187">iPhoneLync</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-188">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-188">iPhoneLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-189">16400</span><span class="sxs-lookup"><span data-stu-id="2d9c4-189">16400</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-190">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-190">AndroidLync</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-191">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-191">AndroidLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-192">16401</span><span class="sxs-lookup"><span data-stu-id="2d9c4-192">16401</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-193">iPadLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-193">iPadLync</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-194">iPadLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-194">iPadLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-195">16402</span><span class="sxs-lookup"><span data-stu-id="2d9c4-195">16402</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-196">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-196">NokiaLync</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-197">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="2d9c4-197">NokiaLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-198">16403</span><span class="sxs-lookup"><span data-stu-id="2d9c4-198">16403</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-199">LyncImm</span><span class="sxs-lookup"><span data-stu-id="2d9c4-199">LyncImm</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-200">LyncImm</span><span class="sxs-lookup"><span data-stu-id="2d9c4-200">LyncImm</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-201">16404</span><span class="sxs-lookup"><span data-stu-id="2d9c4-201">16404</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-202">笔记本电脑</span><span class="sxs-lookup"><span data-stu-id="2d9c4-202">PCS</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-203">笔记本电脑</span><span class="sxs-lookup"><span data-stu-id="2d9c4-203">PCS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-204">16405</span><span class="sxs-lookup"><span data-stu-id="2d9c4-204">16405</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-205">LWA</span><span class="sxs-lookup"><span data-stu-id="2d9c4-205">LWA</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-206">LWA</span><span class="sxs-lookup"><span data-stu-id="2d9c4-206">LWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-207">16406</span><span class="sxs-lookup"><span data-stu-id="2d9c4-207">16406</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-208">OWA</span><span class="sxs-lookup"><span data-stu-id="2d9c4-208">OWA</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-209">OWA</span><span class="sxs-lookup"><span data-stu-id="2d9c4-209">OWA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-210">16407</span><span class="sxs-lookup"><span data-stu-id="2d9c4-210">16407</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-211">AOC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-211">AOC</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-212">AOC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-212">AOC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-213">16408</span><span class="sxs-lookup"><span data-stu-id="2d9c4-213">16408</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-214">GCC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-214">GCC</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-215">GCC</span><span class="sxs-lookup"><span data-stu-id="2d9c4-215">GCC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-216">16409</span><span class="sxs-lookup"><span data-stu-id="2d9c4-216">16409</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-217">IMMCU</span><span class="sxs-lookup"><span data-stu-id="2d9c4-217">IMMCU</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-218">IMMCU</span><span class="sxs-lookup"><span data-stu-id="2d9c4-218">IMMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-219">16410</span><span class="sxs-lookup"><span data-stu-id="2d9c4-219">16410</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-220">XmppTGW</span><span class="sxs-lookup"><span data-stu-id="2d9c4-220">XmppTGW</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-221">XmppGateway</span><span class="sxs-lookup"><span data-stu-id="2d9c4-221">XmppGateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9c4-222">32769</span><span class="sxs-lookup"><span data-stu-id="2d9c4-222">32769</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-223">网关</span><span class="sxs-lookup"><span data-stu-id="2d9c4-223">Gateway</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-224">网关</span><span class="sxs-lookup"><span data-stu-id="2d9c4-224">Gateway</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9c4-225">32770</span><span class="sxs-lookup"><span data-stu-id="2d9c4-225">32770</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-226">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="2d9c4-226">GatewayMediationServerPair</span></span></p></td>
<td><p><span data-ttu-id="2d9c4-227">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="2d9c4-227">GatewayMediationServerPair</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2d9c4-228">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d9c4-228">


</div>

<span> </span>

</div>

</div>

</span></span></div>

