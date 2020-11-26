---
title: Lync Server 2013： UserAgentDef 表
description: Lync Server 2013： UserAgentDef 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgentDef table
ms:assetid: 96c49239-d999-4045-8b64-9d1940cce8ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205100(v=OCS.15)
ms:contentKeyID: 48184860
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a9b12239d0d6ba6e04a708708a1740dbf02c0e07
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439035"
---
# <a name="useragentdef-table-in-lync-server-2013"></a><span data-ttu-id="abbdf-103">Lync Server 2013 中的 UserAgentDef 表</span><span class="sxs-lookup"><span data-stu-id="abbdf-103">UserAgentDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abbdf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abbdf-104">

<span> </span></span></span>

<span data-ttu-id="abbdf-105">_**主题上次修改时间：** 2014-03-25_</span><span class="sxs-lookup"><span data-stu-id="abbdf-105">_**Topic Last Modified:** 2014-03-25_</span></span>

<span data-ttu-id="abbdf-106">UserAgentDef 表将用户代理标识符映射到代理的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="abbdf-106">The UserAgentDef table maps user agent identifiers to the agent’s descriptive names.</span></span> <span data-ttu-id="abbdf-107">用户代理是用于连接到 Microsoft Lync Server 2013 的软件客户端。</span><span class="sxs-lookup"><span data-stu-id="abbdf-107">User agents are software clients used to connect to Microsoft Lync Server 2013.</span></span> <span data-ttu-id="abbdf-108">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="abbdf-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="abbdf-109">UAType</span><span class="sxs-lookup"><span data-stu-id="abbdf-109">UAType</span></span></th>
<th><span data-ttu-id="abbdf-110">UAName</span><span class="sxs-lookup"><span data-stu-id="abbdf-110">UAName</span></span></th>
<th><span data-ttu-id="abbdf-111">UACategory</span><span class="sxs-lookup"><span data-stu-id="abbdf-111">UACategory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-112">1</span><span class="sxs-lookup"><span data-stu-id="abbdf-112">1</span></span></p></td>
<td><p><span data-ttu-id="abbdf-113">MediationServer</span><span class="sxs-lookup"><span data-stu-id="abbdf-113">MediationServer</span></span></p></td>
<td><p><span data-ttu-id="abbdf-114">MediationServer</span><span class="sxs-lookup"><span data-stu-id="abbdf-114">MediationServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-115">2</span><span class="sxs-lookup"><span data-stu-id="abbdf-115">2</span></span></p></td>
<td><p><span data-ttu-id="abbdf-116">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="abbdf-116">AV-MCU</span></span></p></td>
<td><p><span data-ttu-id="abbdf-117">AV-MCU</span><span class="sxs-lookup"><span data-stu-id="abbdf-117">AV-MCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-118">4</span><span class="sxs-lookup"><span data-stu-id="abbdf-118">4</span></span></p></td>
<td><p><span data-ttu-id="abbdf-119">OC</span><span class="sxs-lookup"><span data-stu-id="abbdf-119">OC</span></span></p></td>
<td><p><span data-ttu-id="abbdf-120">OC</span><span class="sxs-lookup"><span data-stu-id="abbdf-120">OC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-121">个</span><span class="sxs-lookup"><span data-stu-id="abbdf-121">8</span></span></p></td>
<td><p><span data-ttu-id="abbdf-122">OCPhone</span><span class="sxs-lookup"><span data-stu-id="abbdf-122">OCPhone</span></span></p></td>
<td><p><span data-ttu-id="abbdf-123">OCPhone</span><span class="sxs-lookup"><span data-stu-id="abbdf-123">OCPhone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-124">utf-16</span><span class="sxs-lookup"><span data-stu-id="abbdf-124">16</span></span></p></td>
<td><p><span data-ttu-id="abbdf-125">LMC</span><span class="sxs-lookup"><span data-stu-id="abbdf-125">LMC</span></span></p></td>
<td><p><span data-ttu-id="abbdf-126">LMC</span><span class="sxs-lookup"><span data-stu-id="abbdf-126">LMC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-127">32</span><span class="sxs-lookup"><span data-stu-id="abbdf-127">32</span></span></p></td>
<td><p><span data-ttu-id="abbdf-128">DVT</span><span class="sxs-lookup"><span data-stu-id="abbdf-128">DVT</span></span></p></td>
<td><p><span data-ttu-id="abbdf-129">DVT</span><span class="sxs-lookup"><span data-stu-id="abbdf-129">DVT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-130">64</span><span class="sxs-lookup"><span data-stu-id="abbdf-130">64</span></span></p></td>
<td><p><span data-ttu-id="abbdf-131">分钟</span><span class="sxs-lookup"><span data-stu-id="abbdf-131">MM</span></span></p></td>
<td><p><span data-ttu-id="abbdf-132">分钟</span><span class="sxs-lookup"><span data-stu-id="abbdf-132">MM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-133">64</span><span class="sxs-lookup"><span data-stu-id="abbdf-133">64</span></span></p></td>
<td><p><span data-ttu-id="abbdf-134">MC</span><span class="sxs-lookup"><span data-stu-id="abbdf-134">MC</span></span></p></td>
<td><p><span data-ttu-id="abbdf-135">分钟</span><span class="sxs-lookup"><span data-stu-id="abbdf-135">MM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-136">128</span><span class="sxs-lookup"><span data-stu-id="abbdf-136">128</span></span></p></td>
<td><p><span data-ttu-id="abbdf-137">助理</span><span class="sxs-lookup"><span data-stu-id="abbdf-137">Attendant</span></span></p></td>
<td><p><span data-ttu-id="abbdf-138">助理</span><span class="sxs-lookup"><span data-stu-id="abbdf-138">Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-139">256</span><span class="sxs-lookup"><span data-stu-id="abbdf-139">256</span></span></p></td>
<td><p><span data-ttu-id="abbdf-140">Conferencing_Announcement_Service_1 0</span><span class="sxs-lookup"><span data-stu-id="abbdf-140">Conferencing_Announcement_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="abbdf-141">而言</span><span class="sxs-lookup"><span data-stu-id="abbdf-141">CAS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-142">512</span><span class="sxs-lookup"><span data-stu-id="abbdf-142">512</span></span></p></td>
<td><p><span data-ttu-id="abbdf-143">Conferencing_Attendant_1 0</span><span class="sxs-lookup"><span data-stu-id="abbdf-143">Conferencing_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="abbdf-144">CAA</span><span class="sxs-lookup"><span data-stu-id="abbdf-144">CAA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-145">512</span><span class="sxs-lookup"><span data-stu-id="abbdf-145">512</span></span></p></td>
<td><p><span data-ttu-id="abbdf-146">Conference_Auto_Attendant_1 0</span><span class="sxs-lookup"><span data-stu-id="abbdf-146">Conference_Auto_Attendant_1.0</span></span></p></td>
<td><p><span data-ttu-id="abbdf-147">CAA</span><span class="sxs-lookup"><span data-stu-id="abbdf-147">CAA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-148">1024</span><span class="sxs-lookup"><span data-stu-id="abbdf-148">1024</span></span></p></td>
<td><p><span data-ttu-id="abbdf-149">Response_Group_Service</span><span class="sxs-lookup"><span data-stu-id="abbdf-149">Response_Group_Service</span></span></p></td>
<td><p><span data-ttu-id="abbdf-150">RG</span><span class="sxs-lookup"><span data-stu-id="abbdf-150">RGS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-151">1032</span><span class="sxs-lookup"><span data-stu-id="abbdf-151">1032</span></span></p></td>
<td><p><span data-ttu-id="abbdf-152">Call_Park_Service_1 0</span><span class="sxs-lookup"><span data-stu-id="abbdf-152">Call_Park_Service_1.0</span></span></p></td>
<td><p><span data-ttu-id="abbdf-153">方面</span><span class="sxs-lookup"><span data-stu-id="abbdf-153">CPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-154">1040</span><span class="sxs-lookup"><span data-stu-id="abbdf-154">1040</span></span></p></td>
<td><p><span data-ttu-id="abbdf-155">Response_Group_Service Announcement_Service</span><span class="sxs-lookup"><span data-stu-id="abbdf-155">Response_Group_Service Announcement_Service</span></span></p></td>
<td><p><span data-ttu-id="abbdf-156">方式</span><span class="sxs-lookup"><span data-stu-id="abbdf-156">AS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-157">2048</span><span class="sxs-lookup"><span data-stu-id="abbdf-157">2048</span></span></p></td>
<td><p><span data-ttu-id="abbdf-158">Microsoft Ccs</span><span class="sxs-lookup"><span data-stu-id="abbdf-158">Microsoft.Rtc.Applications.Ccs</span></span></p></td>
<td><p><span data-ttu-id="abbdf-159">CCS</span><span class="sxs-lookup"><span data-stu-id="abbdf-159">CCS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-160">16386</span><span class="sxs-lookup"><span data-stu-id="abbdf-160">16386</span></span></p></td>
<td><p><span data-ttu-id="abbdf-161">CoMo</span><span class="sxs-lookup"><span data-stu-id="abbdf-161">CoMo</span></span></p></td>
<td><p><span data-ttu-id="abbdf-162">CoMo</span><span class="sxs-lookup"><span data-stu-id="abbdf-162">CoMo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-163">16387</span><span class="sxs-lookup"><span data-stu-id="abbdf-163">16387</span></span></p></td>
<td><p><span data-ttu-id="abbdf-164">CWA</span><span class="sxs-lookup"><span data-stu-id="abbdf-164">CWA</span></span></p></td>
<td><p><span data-ttu-id="abbdf-165">CWA</span><span class="sxs-lookup"><span data-stu-id="abbdf-165">CWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-166">16388</span><span class="sxs-lookup"><span data-stu-id="abbdf-166">16388</span></span></p></td>
<td><p><span data-ttu-id="abbdf-167">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="abbdf-167">InboundRouting</span></span></p></td>
<td><p><span data-ttu-id="abbdf-168">InboundRouting</span><span class="sxs-lookup"><span data-stu-id="abbdf-168">InboundRouting</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-169">16389</span><span class="sxs-lookup"><span data-stu-id="abbdf-169">16389</span></span></p></td>
<td><p><span data-ttu-id="abbdf-170">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="abbdf-170">ComoSvc</span></span></p></td>
<td><p><span data-ttu-id="abbdf-171">ComoSvc</span><span class="sxs-lookup"><span data-stu-id="abbdf-171">ComoSvc</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-172">16393</span><span class="sxs-lookup"><span data-stu-id="abbdf-172">16393</span></span></p></td>
<td><p><span data-ttu-id="abbdf-173">MSExchangeUM</span><span class="sxs-lookup"><span data-stu-id="abbdf-173">MSExchangeUM</span></span></p></td>
<td><p><span data-ttu-id="abbdf-174">ExUM</span><span class="sxs-lookup"><span data-stu-id="abbdf-174">ExUM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-175">16395</span><span class="sxs-lookup"><span data-stu-id="abbdf-175">16395</span></span></p></td>
<td><p><span data-ttu-id="abbdf-176">ArchivingAgent</span><span class="sxs-lookup"><span data-stu-id="abbdf-176">ArchivingAgent</span></span></p></td>
<td><p><span data-ttu-id="abbdf-177">ARCHAGENT</span><span class="sxs-lookup"><span data-stu-id="abbdf-177">ARCHAGENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-178">16396</span><span class="sxs-lookup"><span data-stu-id="abbdf-178">16396</span></span></p></td>
<td><p><span data-ttu-id="abbdf-179">短期</span><span class="sxs-lookup"><span data-stu-id="abbdf-179">ST</span></span></p></td>
<td><p><span data-ttu-id="abbdf-180">短期</span><span class="sxs-lookup"><span data-stu-id="abbdf-180">ST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-181">16397</span><span class="sxs-lookup"><span data-stu-id="abbdf-181">16397</span></span></p></td>
<td><p><span data-ttu-id="abbdf-182">applicationsharing</span><span class="sxs-lookup"><span data-stu-id="abbdf-182">applicationsharing</span></span></p></td>
<td><p><span data-ttu-id="abbdf-183">ASMCU</span><span class="sxs-lookup"><span data-stu-id="abbdf-183">ASMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-184">16398</span><span class="sxs-lookup"><span data-stu-id="abbdf-184">16398</span></span></p></td>
<td><p><span data-ttu-id="abbdf-185">WPLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-185">WPLync</span></span></p></td>
<td><p><span data-ttu-id="abbdf-186">WPLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-186">WPLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-187">16399</span><span class="sxs-lookup"><span data-stu-id="abbdf-187">16399</span></span></p></td>
<td><p><span data-ttu-id="abbdf-188">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-188">iPhoneLync</span></span></p></td>
<td><p><span data-ttu-id="abbdf-189">iPhoneLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-189">iPhoneLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-190">16400</span><span class="sxs-lookup"><span data-stu-id="abbdf-190">16400</span></span></p></td>
<td><p><span data-ttu-id="abbdf-191">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-191">AndroidLync</span></span></p></td>
<td><p><span data-ttu-id="abbdf-192">AndroidLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-192">AndroidLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-193">16401</span><span class="sxs-lookup"><span data-stu-id="abbdf-193">16401</span></span></p></td>
<td><p><span data-ttu-id="abbdf-194">iPadLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-194">iPadLync</span></span></p></td>
<td><p><span data-ttu-id="abbdf-195">iPadLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-195">iPadLync</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-196">16402</span><span class="sxs-lookup"><span data-stu-id="abbdf-196">16402</span></span></p></td>
<td><p><span data-ttu-id="abbdf-197">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-197">NokiaLync</span></span></p></td>
<td><p><span data-ttu-id="abbdf-198">NokiaLync</span><span class="sxs-lookup"><span data-stu-id="abbdf-198">NokiaLync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-199">16403</span><span class="sxs-lookup"><span data-stu-id="abbdf-199">16403</span></span></p></td>
<td><p><span data-ttu-id="abbdf-200">LyncImm</span><span class="sxs-lookup"><span data-stu-id="abbdf-200">LyncImm</span></span></p></td>
<td><p><span data-ttu-id="abbdf-201">LyncImm</span><span class="sxs-lookup"><span data-stu-id="abbdf-201">LyncImm</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-202">16404</span><span class="sxs-lookup"><span data-stu-id="abbdf-202">16404</span></span></p></td>
<td><p><span data-ttu-id="abbdf-203">笔记本电脑</span><span class="sxs-lookup"><span data-stu-id="abbdf-203">PCS</span></span></p></td>
<td><p><span data-ttu-id="abbdf-204">笔记本电脑</span><span class="sxs-lookup"><span data-stu-id="abbdf-204">PCS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-205">16405</span><span class="sxs-lookup"><span data-stu-id="abbdf-205">16405</span></span></p></td>
<td><p><span data-ttu-id="abbdf-206">LWA</span><span class="sxs-lookup"><span data-stu-id="abbdf-206">LWA</span></span></p></td>
<td><p><span data-ttu-id="abbdf-207">LWA</span><span class="sxs-lookup"><span data-stu-id="abbdf-207">LWA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-208">16406</span><span class="sxs-lookup"><span data-stu-id="abbdf-208">16406</span></span></p></td>
<td><p><span data-ttu-id="abbdf-209">OWA</span><span class="sxs-lookup"><span data-stu-id="abbdf-209">OWA</span></span></p></td>
<td><p><span data-ttu-id="abbdf-210">OWA</span><span class="sxs-lookup"><span data-stu-id="abbdf-210">OWA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-211">16407</span><span class="sxs-lookup"><span data-stu-id="abbdf-211">16407</span></span></p></td>
<td><p><span data-ttu-id="abbdf-212">AOC</span><span class="sxs-lookup"><span data-stu-id="abbdf-212">AOC</span></span></p></td>
<td><p><span data-ttu-id="abbdf-213">AOC</span><span class="sxs-lookup"><span data-stu-id="abbdf-213">AOC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-214">16408</span><span class="sxs-lookup"><span data-stu-id="abbdf-214">16408</span></span></p></td>
<td><p><span data-ttu-id="abbdf-215">GCC</span><span class="sxs-lookup"><span data-stu-id="abbdf-215">GCC</span></span></p></td>
<td><p><span data-ttu-id="abbdf-216">GCC</span><span class="sxs-lookup"><span data-stu-id="abbdf-216">GCC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-217">16409</span><span class="sxs-lookup"><span data-stu-id="abbdf-217">16409</span></span></p></td>
<td><p><span data-ttu-id="abbdf-218">IMMCU</span><span class="sxs-lookup"><span data-stu-id="abbdf-218">IMMCU</span></span></p></td>
<td><p><span data-ttu-id="abbdf-219">IMMCU</span><span class="sxs-lookup"><span data-stu-id="abbdf-219">IMMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-220">16410</span><span class="sxs-lookup"><span data-stu-id="abbdf-220">16410</span></span></p></td>
<td><p><span data-ttu-id="abbdf-221">XmppTGW</span><span class="sxs-lookup"><span data-stu-id="abbdf-221">XmppTGW</span></span></p></td>
<td><p><span data-ttu-id="abbdf-222">XmppGateway</span><span class="sxs-lookup"><span data-stu-id="abbdf-222">XmppGateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbdf-223">32769</span><span class="sxs-lookup"><span data-stu-id="abbdf-223">32769</span></span></p></td>
<td><p><span data-ttu-id="abbdf-224">网关</span><span class="sxs-lookup"><span data-stu-id="abbdf-224">Gateway</span></span></p></td>
<td><p><span data-ttu-id="abbdf-225">网关</span><span class="sxs-lookup"><span data-stu-id="abbdf-225">Gateway</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbdf-226">32770</span><span class="sxs-lookup"><span data-stu-id="abbdf-226">32770</span></span></p></td>
<td><p><span data-ttu-id="abbdf-227">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="abbdf-227">GatewayMediationServerPair</span></span></p></td>
<td><p><span data-ttu-id="abbdf-228">GatewayMediationServerPair</span><span class="sxs-lookup"><span data-stu-id="abbdf-228">GatewayMediationServerPair</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="abbdf-229">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abbdf-229">


</div>

<span> </span>

</div>

</div>

</span></span></div>

