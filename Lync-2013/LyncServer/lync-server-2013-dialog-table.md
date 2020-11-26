---
title: Lync Server 2013：Dialog 表
description: Lync Server 2013：对话框表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialog table
ms:assetid: 4d93424f-9072-43f5-83c2-3d539e3e9ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398313(v=OCS.15)
ms:contentKeyID: 48184068
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ae93b8ca9f1146b7dc164803f27cbeeadc66777
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429201"
---
# <a name="dialog-table-in-lync-server-2013"></a><span data-ttu-id="0ac56-103">Lync Server 2013 中的 Dialog 表</span><span class="sxs-lookup"><span data-stu-id="0ac56-103">Dialog table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ac56-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ac56-104">

<span> </span></span></span>

<span data-ttu-id="0ac56-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="0ac56-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="0ac56-106">对话框表是支持表;每条记录表示一个会话初始协议 (SIP) 对话框。</span><span class="sxs-lookup"><span data-stu-id="0ac56-106">The Dialog table is a supporting table; each record represents one Session Initiation Protocol (SIP) dialog.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ac56-107"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="0ac56-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="0ac56-108"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="0ac56-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="0ac56-109"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="0ac56-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="0ac56-110"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="0ac56-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ac56-111"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="0ac56-111"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0ac56-112">datetime</span><span class="sxs-lookup"><span data-stu-id="0ac56-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="0ac56-113">Primary</span><span class="sxs-lookup"><span data-stu-id="0ac56-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ac56-114">优秀 (QoE) 代理接收来自呼叫方或被叫方的第一个报告的时间。</span><span class="sxs-lookup"><span data-stu-id="0ac56-114">Time when the Quality of Excellence (QoE) agent receives the first report from either caller or callee.</span></span> <span data-ttu-id="0ac56-115">与 SessionSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="0ac56-115">Used in conjunction with SessionSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac56-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0ac56-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0ac56-117">int</span><span class="sxs-lookup"><span data-stu-id="0ac56-117">int</span></span></p></td>
<td><p><span data-ttu-id="0ac56-118">Primary</span><span class="sxs-lookup"><span data-stu-id="0ac56-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ac56-119">序列号，以便在具有相同的 ConferenceDateTime 时区分会话。</span><span class="sxs-lookup"><span data-stu-id="0ac56-119">Sequence number to differentiate sessions when they have the same ConferenceDateTime.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ac56-120"><strong>DialogID</strong></span><span class="sxs-lookup"><span data-stu-id="0ac56-120"><strong>DialogID</strong></span></span></p></td>
<td><p><span data-ttu-id="0ac56-121">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="0ac56-121">varchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ac56-122">全局唯一的对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="0ac56-122">Dialog ID which is globally unique.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac56-123"><strong>DialogIDChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="0ac56-123"><strong>DialogIDChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="0ac56-124">int</span><span class="sxs-lookup"><span data-stu-id="0ac56-124">int</span></span></p></td>
<td><p><span data-ttu-id="0ac56-125">食指</span><span class="sxs-lookup"><span data-stu-id="0ac56-125">index</span></span></p></td>
<td><p><span data-ttu-id="0ac56-126">对话框 ID 的校验和。</span><span class="sxs-lookup"><span data-stu-id="0ac56-126">Checksum of the Dialog ID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0ac56-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ac56-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

