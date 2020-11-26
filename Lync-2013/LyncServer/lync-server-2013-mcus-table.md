---
title: Lync Server 2013：Mcus 表
description: Lync Server 2013： Mcus 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mcus table
ms:assetid: 271b7963-8fd8-4d92-a701-1a62aaf895ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425742(v=OCS.15)
ms:contentKeyID: 48183674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0b5d0bcbebb5efc1d767776b4581b18d9f2ed18
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425743"
---
# <a name="mcus-table-in-lync-server-2013"></a><span data-ttu-id="d664b-103">Lync Server 2013 中的 Mcus 表</span><span class="sxs-lookup"><span data-stu-id="d664b-103">Mcus table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d664b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d664b-104">

<span> </span></span></span>

<span data-ttu-id="d664b-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="d664b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="d664b-106">Mcus 表是支持表。</span><span class="sxs-lookup"><span data-stu-id="d664b-106">The Mcus table is a supporting table.</span></span> <span data-ttu-id="d664b-107">每条记录存储有关一个会议服务的信息。</span><span class="sxs-lookup"><span data-stu-id="d664b-107">Each record stores information about one conferencing service.</span></span> <span data-ttu-id="d664b-108">其中包括 IM 会议服务和电话会议服务 (，该服务作为前端服务器上的进程运行) 、Web 会议服务和 A/V 会议服务。</span><span class="sxs-lookup"><span data-stu-id="d664b-108">These can include the IM Conferencing service and the Telephony Conferencing service (which run as processes on front-end servers), and the Web Conferencing service and A/V Conferencing service.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d664b-109">列</span><span class="sxs-lookup"><span data-stu-id="d664b-109">Column</span></span></th>
<th><span data-ttu-id="d664b-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="d664b-110">Data Type</span></span></th>
<th><span data-ttu-id="d664b-111">键/索引</span><span class="sxs-lookup"><span data-stu-id="d664b-111">Key/Index</span></span></th>
<th><span data-ttu-id="d664b-112">详细信息</span><span class="sxs-lookup"><span data-stu-id="d664b-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d664b-113"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="d664b-113"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="d664b-114">int</span><span class="sxs-lookup"><span data-stu-id="d664b-114">int</span></span></p></td>
<td><p><span data-ttu-id="d664b-115">Primary</span><span class="sxs-lookup"><span data-stu-id="d664b-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="d664b-116">标识此会议服务器的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="d664b-116">Unique number identifying this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d664b-117"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="d664b-117"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d664b-118">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="d664b-118">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d664b-119"><strong>McuTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="d664b-119"><strong>McuTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="d664b-120">inyint</span><span class="sxs-lookup"><span data-stu-id="d664b-120">inyint</span></span></p></td>
<td><p> <span data-ttu-id="d664b-121">外表</span><span class="sxs-lookup"><span data-stu-id="d664b-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="d664b-122">会议服务器类型，例如会议：即时消息的聊天 () 或会议：音频视频。</span><span class="sxs-lookup"><span data-stu-id="d664b-122">Conferencing server type, such as conf:chat (for IMs) or conf:audio-video.</span></span> <span data-ttu-id="d664b-123">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="d664b-123">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d664b-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d664b-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

