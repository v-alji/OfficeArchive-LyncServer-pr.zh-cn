---
title: Lync Server 2013： IMReportSummary 表
description: Lync Server 2013： IMReportSummary 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IMReportSummary table
ms:assetid: 27ff9453-53f2-4fae-b637-70a086c9df96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204753(v=OCS.15)
ms:contentKeyID: 48183673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dfafa81d1605845b29a3627321fcbc0f72ca7ac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427311"
---
# <a name="imreportsummary-table-in-lync-server-2013"></a><span data-ttu-id="1fe1e-103">Lync Server 2013 中的 IMReportSummary 表</span><span class="sxs-lookup"><span data-stu-id="1fe1e-103">IMReportSummary table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1fe1e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1fe1e-104">

<span> </span></span></span>

<span data-ttu-id="1fe1e-105">_**主题上次修改时间：** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="1fe1e-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="1fe1e-106">IMReportSummaryTable 提供组织中的即时消息会话的整体报告。</span><span class="sxs-lookup"><span data-stu-id="1fe1e-106">The IMReportSummaryTable provides an overall report on the instant messaging sessions held in an organization.</span></span> <span data-ttu-id="1fe1e-107">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="1fe1e-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fe1e-108">列</span><span class="sxs-lookup"><span data-stu-id="1fe1e-108">Column</span></span></th>
<th><span data-ttu-id="1fe1e-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="1fe1e-109">Data Type</span></span></th>
<th><span data-ttu-id="1fe1e-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="1fe1e-110">Key/Index</span></span></th>
<th><span data-ttu-id="1fe1e-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="1fe1e-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fe1e-112"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="1fe1e-112"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1fe1e-113">datetime</span><span class="sxs-lookup"><span data-stu-id="1fe1e-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="1fe1e-114">Primary</span><span class="sxs-lookup"><span data-stu-id="1fe1e-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="1fe1e-115">即时消息会话开始的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="1fe1e-115">Date and time that the instant messaging session began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fe1e-116"><strong>TimePeriod</strong></span><span class="sxs-lookup"><span data-stu-id="1fe1e-116"><strong>TimePeriod</strong></span></span></p></td>
<td><p><span data-ttu-id="1fe1e-117">char (1) </span><span class="sxs-lookup"><span data-stu-id="1fe1e-117">char(1)</span></span></p></td>
<td><p><span data-ttu-id="1fe1e-118">Primary</span><span class="sxs-lookup"><span data-stu-id="1fe1e-118">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fe1e-119"><strong>PoolFQDN</strong></span><span class="sxs-lookup"><span data-stu-id="1fe1e-119"><strong>PoolFQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="1fe1e-120">nvarchar (257) </span><span class="sxs-lookup"><span data-stu-id="1fe1e-120">nvarchar(257)</span></span></p></td>
<td><p><span data-ttu-id="1fe1e-121">Primary</span><span class="sxs-lookup"><span data-stu-id="1fe1e-121">Primary</span></span></p></td>
<td><p><span data-ttu-id="1fe1e-122">托管会话的池的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="1fe1e-122">Fully qualified domain name of the pool hosting the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fe1e-123"><strong>AuthType</strong></span><span class="sxs-lookup"><span data-stu-id="1fe1e-123"><strong>AuthType</strong></span></span></p></td>
<td><p><span data-ttu-id="1fe1e-124">int</span><span class="sxs-lookup"><span data-stu-id="1fe1e-124">int</span></span></p></td>
<td><p><span data-ttu-id="1fe1e-125">Primary</span><span class="sxs-lookup"><span data-stu-id="1fe1e-125">Primary</span></span></p></td>
<td><p><span data-ttu-id="1fe1e-126"> (例如紧急或非紧急) 通话的优先级。</span><span class="sxs-lookup"><span data-stu-id="1fe1e-126">Priority (for example, urgent or non-urgent) of the call.</span></span> <span data-ttu-id="1fe1e-127">优先级信息存储在 <a href="lync-server-2013-callpriorities-table.md">Lync Server 2013 的 CallPriorities 表中</a>。</span><span class="sxs-lookup"><span data-stu-id="1fe1e-127">Priority information is stored in the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fe1e-128"><strong>SessionCount</strong></span><span class="sxs-lookup"><span data-stu-id="1fe1e-128"><strong>SessionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="1fe1e-129">bigint</span><span class="sxs-lookup"><span data-stu-id="1fe1e-129">bigint</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fe1e-130"><strong>MsgCount</strong></span><span class="sxs-lookup"><span data-stu-id="1fe1e-130"><strong>MsgCount</strong></span></span></p></td>
<td><p><span data-ttu-id="1fe1e-131">bigint</span><span class="sxs-lookup"><span data-stu-id="1fe1e-131">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1fe1e-132">会话期间交换的即时消息总数。</span><span class="sxs-lookup"><span data-stu-id="1fe1e-132">Total number of instant messages exchanged during the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1fe1e-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1fe1e-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

