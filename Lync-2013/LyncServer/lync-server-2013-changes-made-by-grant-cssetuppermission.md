---
title: Lync Server 2013： Grant-CsSetupPermission 所做的更改
description: Lync Server 2013：通过授予-CsSetupPermission 进行的更改。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsSetupPermission
ms:assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205250(v=OCS.15)
ms:contentKeyID: 48185360
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2a9156c977c993dd32e38fc6816bd08d3f65c1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435066"
---
# <a name="changes-made-by-grant-cssetuppermission-in-lync-server-2013"></a><span data-ttu-id="0fa8f-103">Lync Server 2013 中 Grant-CsSetupPermission 所做的更改</span><span class="sxs-lookup"><span data-stu-id="0fa8f-103">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0fa8f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0fa8f-104">

<span> </span></span></span>

<span data-ttu-id="0fa8f-105">_**主题上次修改时间：** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="0fa8f-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="0fa8f-106">若要委派设置，您可以为特定 Active Directory 组织 (单位的 RTCUniversalServerAdmins 通用组授予权限) ，允许该 OU 中的 RTCUniversalServerAdmins 组成员在指定域中安装 Lync Server 2013，而不是域管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="0fa8f-106">To delegate setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="0fa8f-107">**CsSetupPermission** cmdlet 授予对 OU 的 RTCUniversalServerAdmins 组权限，如下表所示：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-107">The **Grant-CsSetupPermission** cmdlet grants the RTCUniversalServerAdmins group permissions on an OU, as specified in the following table:</span></span>

### <a name="permissions-granted-to-objects-in-the-ou"></a><span data-ttu-id="0fa8f-108">在 OU 中授予对象的权限</span><span class="sxs-lookup"><span data-stu-id="0fa8f-108">Permissions granted to Objects in the OU</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fa8f-109">权限适用于：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-109">Permissions apply to:</span></span></th>
<th><span data-ttu-id="0fa8f-110">授予的权限为：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-110">Permissions granted are:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fa8f-111">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0fa8f-111">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-112">特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-112">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-113">阅读 servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0fa8f-113">Read servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-114">写入 servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0fa8f-114">Write servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-115">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-115">Delete tree</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-116">复制目录更改</span><span class="sxs-lookup"><span data-stu-id="0fa8f-116">Replicating directory changes</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa8f-117">后代 serviceConnectionPoint 对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-117">Descendant serviceConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-118">特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-118">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-119">读取权限</span><span class="sxs-lookup"><span data-stu-id="0fa8f-119">Read permissions</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-120">写入权限</span><span class="sxs-lookup"><span data-stu-id="0fa8f-120">Write permissions</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-121">创建子元素</span><span class="sxs-lookup"><span data-stu-id="0fa8f-121">Create child</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-122">删除子元素</span><span class="sxs-lookup"><span data-stu-id="0fa8f-122">Delete child</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-123">列表内容</span><span class="sxs-lookup"><span data-stu-id="0fa8f-123">List contents</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-124">Write 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-124">Write property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-125">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-125">Read property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-126">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-126">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa8f-127">子代 msRTCSIP-服务器对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-127">Descendant msRTCSIP-Server objects</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-128">特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-128">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-129">Write 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-129">Write property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-130">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-130">Read property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-131">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-131">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa8f-132">子代 msRTCSIP-WebComponents 对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-132">Descendant msRTCSIP-WebComponents objects</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-133">特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-133">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-134">Write 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-134">Write property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-135">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-135">Read property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-136">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-136">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa8f-137">子体 msRTCSIP-MCU 对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-137">Descendant msRTCSIP-MCU objects</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-138">特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-138">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-139">Write 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-139">Write property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-140">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-140">Read property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-141">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-141">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa8f-142">子代 msRTCSIP-MediationServer 对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-142">Descendant msRTCSIP-MediationServer objects</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-143">特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-143">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-144">Write 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-144">Write property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-145">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-145">Read property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-146">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-146">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa8f-147">子代 msRTCSIP-ApplicationServer 对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-147">Descendant msRTCSIP-ApplicationServer objects</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-148">特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-148">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-149">Write 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-149">Write property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-150">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-150">Read property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-151">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-151">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa8f-152">子代 msRTCSIP-ConnectionPoint 对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-152">Descendant msRTCSIP-ConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-153">特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-153">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-154">Write 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-154">Write property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-155">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-155">Read property</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-156">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-156">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa8f-157">子体计算机对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-157">Descendant Computer objects</span></span></p></td>
<td><p><span data-ttu-id="0fa8f-158">用于 serviceConnectionPoint 的特殊访问：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-158">Special access for serviceConnectionPoint:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-159">创建子对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-159">Create child objects</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-160">删除子对象</span><span class="sxs-lookup"><span data-stu-id="0fa8f-160">Delete child objects</span></span></p></li>
<li><p><span data-ttu-id="0fa8f-161">删除树</span><span class="sxs-lookup"><span data-stu-id="0fa8f-161">Delete tree</span></span></p></li>
</ul>
<p><span data-ttu-id="0fa8f-162">公共信息的特殊访问权限：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-162">Special access for public information:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-163">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-163">Read property</span></span></p></li>
</ul>
<p><span data-ttu-id="0fa8f-164">DNS 主机名的特殊访问权限：</span><span class="sxs-lookup"><span data-stu-id="0fa8f-164">Special access for DNS host name:</span></span></p>
<ul>
<li><p><span data-ttu-id="0fa8f-165">Read 属性</span><span class="sxs-lookup"><span data-stu-id="0fa8f-165">Read property</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="0fa8f-166">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0fa8f-166">


</div>

<span> </span>

</div>

</div>

</span></span></div>

