---
title: Lync Server 2013： ConferenceMessageCount 视图
description: Lync Server 2013： ConferenceMessageCount 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount view
ms:assetid: 8ee3ee95-fb78-4d4e-bcdd-6ce5a0a23b44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688129(v=OCS.15)
ms:contentKeyID: 49733727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 212d6e1a346253809fb70806424350cc7fc0dfe2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434429"
---
# <a name="conferencemessagecount-view-in-lync-server-2013"></a><span data-ttu-id="f6d14-103">Lync Server 2013 中的 ConferenceMessageCount 视图</span><span class="sxs-lookup"><span data-stu-id="f6d14-103">ConferenceMessageCount view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6d14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6d14-104">

<span> </span></span></span>

<span data-ttu-id="f6d14-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="f6d14-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="f6d14-106">ConferenceMessageCount 视图存储有关用户向会议发送的邮件数的信息。</span><span class="sxs-lookup"><span data-stu-id="f6d14-106">The ConferenceMessageCount view stores information about how many messages were sent by a user to a conference.</span></span> <span data-ttu-id="f6d14-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="f6d14-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f6d14-108">ConferenceMessageCount 视图包含 <A href="lync-server-2013-conferencesessiondetails-view.md">Lync Server 2013 的 ConferenceSessionDetails 视图</A> 中的所有列以及下面列出的列。</span><span class="sxs-lookup"><span data-stu-id="f6d14-108">The ConferenceMessageCount view contains all of the columns in the <A href="lync-server-2013-conferencesessiondetails-view.md">ConferenceSessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6d14-109">列</span><span class="sxs-lookup"><span data-stu-id="f6d14-109">Column</span></span></th>
<th><span data-ttu-id="f6d14-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="f6d14-110">Data Type</span></span></th>
<th><span data-ttu-id="f6d14-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="f6d14-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6d14-112"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="f6d14-112"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="f6d14-113">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="f6d14-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="f6d14-114">发送邮件的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="f6d14-114">URI of the user who sent the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6d14-115"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="f6d14-115"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="f6d14-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f6d14-116">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f6d14-117">发送邮件的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="f6d14-117">Type of URI of the user who sent the messages.</span></span> <span data-ttu-id="f6d14-118">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="f6d14-118">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6d14-119"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="f6d14-119"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="f6d14-120">标识符</span><span class="sxs-lookup"><span data-stu-id="f6d14-120">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="f6d14-121">发送消息的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="f6d14-121">Tenant of user who sent the messages.</span></span> <span data-ttu-id="f6d14-122">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="f6d14-122">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6d14-123"><strong>UserMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="f6d14-123"><strong>UserMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="f6d14-124">smallint</span><span class="sxs-lookup"><span data-stu-id="f6d14-124">smallint</span></span></p></td>
<td><p><span data-ttu-id="f6d14-125">在会议会话期间用户发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="f6d14-125">Number of messages sent by the user during the conference session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f6d14-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6d14-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

