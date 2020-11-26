---
title: Lync Server 2013：由域准备进行的更改
description: Lync Server 2013：由域准备进行的更改。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435115"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a><span data-ttu-id="3c06e-103">Lync Server 2013 中的域准备进行的更改</span><span class="sxs-lookup"><span data-stu-id="3c06e-103">Changes made by domain preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c06e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c06e-104">

<span> </span></span></span>

<span data-ttu-id="3c06e-105">_**主题上次修改时间：** 2010-10-18_</span><span class="sxs-lookup"><span data-stu-id="3c06e-105">_**Topic Last Modified:** 2010-10-18_</span></span>

<span data-ttu-id="3c06e-106">下表列出了 (Ace) "域准备" 在域根上创建的访问控制条目。</span><span class="sxs-lookup"><span data-stu-id="3c06e-106">The following table lists the access control entries (ACEs) that domain preparation creates on the domain root.</span></span> <span data-ttu-id="3c06e-107">除非另有说明，否则将继承所有 Ace。</span><span class="sxs-lookup"><span data-stu-id="3c06e-107">All ACEs are inherited unless otherwise noted.</span></span>

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a><span data-ttu-id="3c06e-108">添加到域根的 Ace</span><span class="sxs-lookup"><span data-stu-id="3c06e-108">ACEs Added to Domain Root</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c06e-109">棒</span><span class="sxs-lookup"><span data-stu-id="3c06e-109">ACE</span></span></th>
<th><span data-ttu-id="3c06e-110">RTCUniversal-UserReadOnly</span><span class="sxs-lookup"><span data-stu-id="3c06e-110">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="3c06e-111">RTCUniversal-ServerReadOnly</span><span class="sxs-lookup"><span data-stu-id="3c06e-111">RTCUniversal-ServerReadOnly-Group</span></span></th>
<th><span data-ttu-id="3c06e-112">RTCUniversal-UserAdmins</span><span class="sxs-lookup"><span data-stu-id="3c06e-112">RTCUniversal-UserAdmins</span></span></th>
<th><span data-ttu-id="3c06e-113">RTCHSUniversal-Services</span><span class="sxs-lookup"><span data-stu-id="3c06e-113">RTCHSUniversal-Services</span></span></th>
<th><span data-ttu-id="3c06e-114">Authenticated-Users</span><span class="sxs-lookup"><span data-stu-id="3c06e-114">Authenticated-Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c06e-115">未继承 (读取容器) </span><span class="sxs-lookup"><span data-stu-id="3c06e-115">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="3c06e-116"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-116"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-117"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-117"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-118">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-118">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-119">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-119">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-120">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c06e-121">阅读用户 PropertySet 用户帐户-限制</span><span class="sxs-lookup"><span data-stu-id="3c06e-121">Read User PropertySet User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="3c06e-122"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-122"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-123">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-123">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-124">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-124">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-125">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-125">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-126">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c06e-127">阅读用户 PropertySet Personal-Information</span><span class="sxs-lookup"><span data-stu-id="3c06e-127">Read User PropertySet Personal-Information</span></span></p></td>
<td><p><span data-ttu-id="3c06e-128"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-128"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-129">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-129">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-130">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-130">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-131">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-131">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-132">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c06e-133">阅读用户 PropertySet General-Information</span><span class="sxs-lookup"><span data-stu-id="3c06e-133">Read User PropertySet General-Information</span></span></p></td>
<td><p><span data-ttu-id="3c06e-134"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-134"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-135">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-135">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-136">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-136">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-137">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-137">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-138">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-138">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c06e-139">阅读用户 PropertySet Public-Information</span><span class="sxs-lookup"><span data-stu-id="3c06e-139">Read User PropertySet Public-Information</span></span></p></td>
<td><p><span data-ttu-id="3c06e-140"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-140"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-141">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-141">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-142">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-142">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-143">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-143">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-144">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-144">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c06e-145">阅读用户 PropertySet RTCUserSearchProperty-Set</span><span class="sxs-lookup"><span data-stu-id="3c06e-145">Read User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="3c06e-146"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-146"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-147">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-147">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-148">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-148">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-149">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-149">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-150"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-150"><strong>Yes</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c06e-151">阅读用户 PropertySet RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="3c06e-151">Read User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="3c06e-152"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-152"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-153">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-153">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-154">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-154">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-155">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-155">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-156">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c06e-157">编写用户属性 Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="3c06e-157">Write User Property Proxy-Addresses</span></span></p></td>
<td><p><span data-ttu-id="3c06e-158">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-158">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-159">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-159">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-160"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-160"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-161">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-161">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-162">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-162">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c06e-163">编写用户 PropertySet RTCUserSearchProperty-Set</span><span class="sxs-lookup"><span data-stu-id="3c06e-163">Write User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="3c06e-164">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-164">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-165">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-165">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-166"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-166"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-167">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-167">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-168">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-168">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c06e-169">编写用户 PropertySet RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="3c06e-169">Write User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="3c06e-170">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-170">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-171">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-171">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-172"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-172"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-173">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-173">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-174">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-174">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c06e-175">读取 PropertySet DS-复制-对所有 Active Directory 对象的获取更改</span><span class="sxs-lookup"><span data-stu-id="3c06e-175">Read PropertySet DS-Replication-Get-Changes of all Active Directory objects</span></span></p></td>
<td><p><span data-ttu-id="3c06e-176">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-176">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-177">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-177">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-178">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-178">No</span></span></p></td>
<td><p><span data-ttu-id="3c06e-179"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-179"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-180">否</span><span class="sxs-lookup"><span data-stu-id="3c06e-180">No</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3c06e-181">下表列出了域准备在三个内置容器中创建的 Ace：用户、计算机和域控制器。</span><span class="sxs-lookup"><span data-stu-id="3c06e-181">The following table lists the ACEs that domain preparation creates in the three built-in containers: Users, Computers, and Domain Controllers.</span></span> <span data-ttu-id="3c06e-182">除非另有说明，否则将继承所有 Ace。</span><span class="sxs-lookup"><span data-stu-id="3c06e-182">All ACEs are inherited unless otherwise noted.</span></span>

### <a name="aces-added-to-built-in-containers"></a><span data-ttu-id="3c06e-183">添加到内置容器的 Ace</span><span class="sxs-lookup"><span data-stu-id="3c06e-183">ACEs Added to Built-in Containers</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c06e-184">棒</span><span class="sxs-lookup"><span data-stu-id="3c06e-184">ACE</span></span></th>
<th><span data-ttu-id="3c06e-185">RTCUniversal-UserReadOnly</span><span class="sxs-lookup"><span data-stu-id="3c06e-185">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="3c06e-186">RTCUniversal-ServerReadOnly</span><span class="sxs-lookup"><span data-stu-id="3c06e-186">RTCUniversal-ServerReadOnly-Group</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c06e-187">未继承 (读取容器) </span><span class="sxs-lookup"><span data-stu-id="3c06e-187">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="3c06e-188"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-188"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3c06e-189"><strong>是</strong></span><span class="sxs-lookup"><span data-stu-id="3c06e-189"><strong>Yes</strong></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3c06e-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c06e-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

