---
title: Lync Server 2013：tblRoleType
description: Lync Server 2013： tblRoleType。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblRoleType
ms:assetid: 1eac3a54-656a-40ac-b771-edfc64d6e34b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558623(v=OCS.15)
ms:contentKeyID: 48183577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f458259acaee7821d5f6a7339b993c70fe65f595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391794"
---
# <a name="tblroletype-in-lync-server-2013"></a><span data-ttu-id="ed904-103">Lync Server 2013 中的 tblRoleType</span><span class="sxs-lookup"><span data-stu-id="ed904-103">tblRoleType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed904-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed904-104">

<span> </span></span></span>

<span data-ttu-id="ed904-105">_**主题上次修改时间：** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="ed904-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="ed904-106">tblRoleType 是一个具有角色类型及其关联权限集的静态查找表。</span><span class="sxs-lookup"><span data-stu-id="ed904-106">tblRoleType is a static lookup table with role types and their associated permission sets.</span></span>

### <a name="columns"></a><span data-ttu-id="ed904-107">多</span><span class="sxs-lookup"><span data-stu-id="ed904-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed904-108">列</span><span class="sxs-lookup"><span data-stu-id="ed904-108">Column</span></span></th>
<th><span data-ttu-id="ed904-109">类型</span><span class="sxs-lookup"><span data-stu-id="ed904-109">Type</span></span></th>
<th><span data-ttu-id="ed904-110">说明</span><span class="sxs-lookup"><span data-stu-id="ed904-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed904-111">rtypeID</span><span class="sxs-lookup"><span data-stu-id="ed904-111">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="ed904-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="ed904-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="ed904-113">角色类型 ID。</span><span class="sxs-lookup"><span data-stu-id="ed904-113">Role type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed904-114">rtypeDesc</span><span class="sxs-lookup"><span data-stu-id="ed904-114">rtypeDesc</span></span></p></td>
<td><p><span data-ttu-id="ed904-115">nvarchar (256) ，not null</span><span class="sxs-lookup"><span data-stu-id="ed904-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="ed904-116">角色类型说明。</span><span class="sxs-lookup"><span data-stu-id="ed904-116">Role type description.</span></span> <span data-ttu-id="ed904-117">有四个可用的角色：</span><span class="sxs-lookup"><span data-stu-id="ed904-117">There are four available roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="ed904-118">成员：聊天室成员</span><span class="sxs-lookup"><span data-stu-id="ed904-118">Member: Chat room member</span></span></p></li>
<li><p><span data-ttu-id="ed904-119">管理器：聊天室管理器</span><span class="sxs-lookup"><span data-stu-id="ed904-119">Manager: Chat room manager</span></span></p></li>
<li><p><span data-ttu-id="ed904-120">浊音：演示者使用 auditorium 聊天室</span><span class="sxs-lookup"><span data-stu-id="ed904-120">Voiced: Presenter for an auditorium chat room</span></span></p></li>
<li><p><span data-ttu-id="ed904-121">创建者：可以创建聊天室</span><span class="sxs-lookup"><span data-stu-id="ed904-121">Creator: Can create chat rooms</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed904-122">rtypeAllowedPermSet</span><span class="sxs-lookup"><span data-stu-id="ed904-122">rtypeAllowedPermSet</span></span></p></td>
<td><p><span data-ttu-id="ed904-123">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="ed904-123">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="ed904-124">角色的权限集。</span><span class="sxs-lookup"><span data-stu-id="ed904-124">Permission set for the role.</span></span> <span data-ttu-id="ed904-125">所用位为：</span><span class="sxs-lookup"><span data-stu-id="ed904-125">The used bits are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ed904-126">2：如果角色可以管理节点，则为 True。</span><span class="sxs-lookup"><span data-stu-id="ed904-126">2: True if the role can manage nodes.</span></span></p></li>
<li><p><span data-ttu-id="ed904-127">4：如果角色可以创建子节点，则为 True。</span><span class="sxs-lookup"><span data-stu-id="ed904-127">4: True if the role can create children nodes.</span></span></p></li>
<li><p><span data-ttu-id="ed904-128">7： True 如果角色可以加入聊天室 (或) 的儿童聊天室。</span><span class="sxs-lookup"><span data-stu-id="ed904-128">7: True if the role can join a chat room (or children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="ed904-129">8：如果角色可以在聊天室中聊天 (或在) 的儿童聊天室中聊天，则为 True。</span><span class="sxs-lookup"><span data-stu-id="ed904-129">8: True if the role can chat in a chat room (or in children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="ed904-130">10：如果角色可以读取聊天历史记录（即使未加入聊天室），则为 True。</span><span class="sxs-lookup"><span data-stu-id="ed904-130">10: True if the role can read chat history even when not joined to a chat room.</span></span></p></li>
<li><p><span data-ttu-id="ed904-131">11：如果角色可以查看聊天室，则为 True。</span><span class="sxs-lookup"><span data-stu-id="ed904-131">11: True if the role can see the chat room.</span></span> <span data-ttu-id="ed904-132"> (将通过范围和可见性等因素进一步改进。 ) </span><span class="sxs-lookup"><span data-stu-id="ed904-132">(This is further refined by factors such as scope and visibility.)</span></span></p></li>
<li><p><span data-ttu-id="ed904-133">12：如果角色可以在 auditorium 聊天室中聊天，则为 True。</span><span class="sxs-lookup"><span data-stu-id="ed904-133">12: True if the role can chat in an auditorium chat room.</span></span></p></li>
<li><p><span data-ttu-id="ed904-134">13：如果角色在查看节点时可以绕过可见性规则，则为 True。</span><span class="sxs-lookup"><span data-stu-id="ed904-134">13: True if the role can bypass visibility rules when viewing nodes.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="ed904-135">密钥</span><span class="sxs-lookup"><span data-stu-id="ed904-135">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed904-136">列</span><span class="sxs-lookup"><span data-stu-id="ed904-136">Column</span></span></th>
<th><span data-ttu-id="ed904-137">说明</span><span class="sxs-lookup"><span data-stu-id="ed904-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed904-138">rtypeID</span><span class="sxs-lookup"><span data-stu-id="ed904-138">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="ed904-139">主键。</span><span class="sxs-lookup"><span data-stu-id="ed904-139">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ed904-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed904-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

