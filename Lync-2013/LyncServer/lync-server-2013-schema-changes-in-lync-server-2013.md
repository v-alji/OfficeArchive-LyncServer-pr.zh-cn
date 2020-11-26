---
title: Lync Server 2013： Lync Server 2013 中的架构更改
description: Lync Server 2013： Lync Server 2013 中的架构更改。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema changes in Lync Server 2013
ms:assetid: d760cb93-77d4-4d64-adb7-416b808f36f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398944(v=OCS.15)
ms:contentKeyID: 48185575
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e914de48ace80fd2611f2d05b092894b11c534a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444922"
---
# <a name="schema-changes-in-lync-server-2013"></a><span data-ttu-id="531ce-103">Lync Server 2013 中的架构更改</span><span class="sxs-lookup"><span data-stu-id="531ce-103">Schema changes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="531ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="531ce-104">

<span> </span></span></span>

<span data-ttu-id="531ce-105">_**主题上次修改时间：** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="531ce-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="531ce-106">在部署和操作 Lync Server 2013 之前，必须通过扩展架构来准备 Active Directory 域服务。</span><span class="sxs-lookup"><span data-stu-id="531ce-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema.</span></span> <span data-ttu-id="531ce-107">架构扩展添加 Lync Server 2013 所需的类和属性。</span><span class="sxs-lookup"><span data-stu-id="531ce-107">The schema extensions add the classes and attributes that are required by Lync Server 2013.</span></span>

<span data-ttu-id="531ce-108">Lync Server 2013 需要多个新的类和属性，并修改一些现有的类和属性。</span><span class="sxs-lookup"><span data-stu-id="531ce-108">Lync Server 2013 requires several new classes and attributes and modifies some existing classes and attributes.</span></span> <span data-ttu-id="531ce-109">此外，Lync Server 2013 的许多配置信息存储在中央管理存储中，而不是在 AD DS 中，就像在以前的版本中一样。</span><span class="sxs-lookup"><span data-stu-id="531ce-109">In addition, much configuration information for Lync Server 2013 is stored in the Central Management store instead of in AD DS as in previous versions.</span></span> <span data-ttu-id="531ce-110">以下信息仍存储在 Lync Server 2013 中的 AD DS 中：</span><span class="sxs-lookup"><span data-stu-id="531ce-110">The following information is still stored in AD DS in Lync Server 2013:</span></span>

  - <span data-ttu-id="531ce-111">**架构扩展**：</span><span class="sxs-lookup"><span data-stu-id="531ce-111">**Schema extensions**:</span></span>
    
      - <span data-ttu-id="531ce-112">用户对象扩展</span><span class="sxs-lookup"><span data-stu-id="531ce-112">User object extensions</span></span>
    
      - <span data-ttu-id="531ce-113">Office 通信服务器2007和 Office 通信服务器 2007 R2 类的扩展，以保持受支持的早期版本的向后兼容性</span><span class="sxs-lookup"><span data-stu-id="531ce-113">Extensions for Office Communications Server 2007 and Office Communications Server 2007 R2 classes to maintain backward compatibility with supported previous versions</span></span>

<!-- end list -->

  - <span data-ttu-id="531ce-114">存储在 Lync Server 扩展架构和现有架构类) 中的 **数据** (：</span><span class="sxs-lookup"><span data-stu-id="531ce-114">**Data** (stored in Lync Server extended schema and in existing schema classes):</span></span>
    
      - <span data-ttu-id="531ce-115">用户 SIP 统一资源标识符 (URI) 和其他用户设置</span><span class="sxs-lookup"><span data-stu-id="531ce-115">User SIP Uniform Resource Identifier (URI) and other user settings</span></span>
    
      - <span data-ttu-id="531ce-116">响应组和会议助理等应用程序的联系人对象</span><span class="sxs-lookup"><span data-stu-id="531ce-116">Contact objects for applications such as Response Group and Conferencing Attendant</span></span>
    
      - <span data-ttu-id="531ce-117">指向中央管理存储的指针</span><span class="sxs-lookup"><span data-stu-id="531ce-117">A pointer to the Central Management store</span></span>
    
      - <span data-ttu-id="531ce-118">Kerberos 身份验证帐户（可选计算机对象）</span><span class="sxs-lookup"><span data-stu-id="531ce-118">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="531ce-119">本主题介绍 Lync Server 2013 所需的 Active Directory 架构更改。</span><span class="sxs-lookup"><span data-stu-id="531ce-119">This topic describes the Active Directory schema changes required by Lync Server 2013.</span></span> <span data-ttu-id="531ce-120">它不会描述以前版本的 Office 通信服务器引入的架构更改。</span><span class="sxs-lookup"><span data-stu-id="531ce-120">It does not describe schema changes that were introduced by previous versions of Office Communications Server.</span></span> <span data-ttu-id="531ce-121">有关类及其说明的列表，请参阅 [Lync Server 2013 中的架构类和说明](lync-server-2013-schema-classes-and-descriptions.md)。</span><span class="sxs-lookup"><span data-stu-id="531ce-121">For a list of classes and their descriptions, see [Schema classes and descriptions in Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span></span> <span data-ttu-id="531ce-122">有关属性及其说明的列表，请参阅 [Lync Server 2013 中的架构属性和说明](lync-server-2013-schema-attributes-and-descriptions.md)。</span><span class="sxs-lookup"><span data-stu-id="531ce-122">For a list of attributes and their descriptions, see [Schema attributes and descriptions in Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span></span> <span data-ttu-id="531ce-123">有关它们可能包含的属性的类的列表，请参阅 [Lync Server 2013 中按类列出的架构属性](lync-server-2013-schema-attributes-by-class.md)。</span><span class="sxs-lookup"><span data-stu-id="531ce-123">For a list of classes with the attributes they may contain, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span>

<span data-ttu-id="531ce-124">MsRTCSIP 前缀标识特定于 Lync Server 的类和属性。</span><span class="sxs-lookup"><span data-stu-id="531ce-124">The msRTCSIP prefix identifies classes and attributes that are specific to Lync Server.</span></span>

<div>

## <a name="new-active-directory-attributes"></a><span data-ttu-id="531ce-125">新的 Active Directory 属性</span><span class="sxs-lookup"><span data-stu-id="531ce-125">New Active Directory Attributes</span></span>

<span data-ttu-id="531ce-126">下表描述了 Lync Server 2013 添加的 Active Directory 属性。</span><span class="sxs-lookup"><span data-stu-id="531ce-126">The following table describes the Active Directory attributes that are added by Lync Server 2013.</span></span>

### <a name="attributes-added-by-lync-server-2013"></a><span data-ttu-id="531ce-127">Lync Server 2013 添加的属性</span><span class="sxs-lookup"><span data-stu-id="531ce-127">Attributes Added by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="531ce-128">属性</span><span class="sxs-lookup"><span data-stu-id="531ce-128">Attribute</span></span></th>
<th><span data-ttu-id="531ce-129">描述</span><span class="sxs-lookup"><span data-stu-id="531ce-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="531ce-130">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="531ce-130">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="531ce-131">此多值属性包含适用于用户的保留策略的标识符。</span><span class="sxs-lookup"><span data-stu-id="531ce-131">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="531ce-132">保留策略在保留期间保留用户的邮箱项目。</span><span class="sxs-lookup"><span data-stu-id="531ce-132">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="531ce-133">此属性是与 Exchange 2013 共享的。</span><span class="sxs-lookup"><span data-stu-id="531ce-133">This attribute is shared with Exchange 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="531ce-134">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="531ce-134">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="531ce-135">这是 SIP 路由组 ID。</span><span class="sxs-lookup"><span data-stu-id="531ce-135">This is the SIP routing group ID.</span></span> <span data-ttu-id="531ce-136">同一组中的用户将注册到同一前端服务器。</span><span class="sxs-lookup"><span data-stu-id="531ce-136">Users in the same group will register to the same Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="531ce-137">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="531ce-137">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="531ce-138">此属性用于存储前端池使用的镜像 SQL Server 后端。</span><span class="sxs-lookup"><span data-stu-id="531ce-138">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="modified-active-directory-classes"></a><span data-ttu-id="531ce-139">已修改的 Active Directory 类</span><span class="sxs-lookup"><span data-stu-id="531ce-139">Modified Active Directory Classes</span></span>

<span data-ttu-id="531ce-140">下表介绍了由 Lync Server 2013 修改的 Active Directory 类。</span><span class="sxs-lookup"><span data-stu-id="531ce-140">The following table describes the Active Directory classes that are modified by Lync Server 2013.</span></span>

### <a name="classes-modified-by-lync-server-2013"></a><span data-ttu-id="531ce-141">Lync Server 2013 修改的类</span><span class="sxs-lookup"><span data-stu-id="531ce-141">Classes Modified by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="531ce-142">种类</span><span class="sxs-lookup"><span data-stu-id="531ce-142">Class</span></span></th>
<th><span data-ttu-id="531ce-143">更改</span><span class="sxs-lookup"><span data-stu-id="531ce-143">Change</span></span></th>
<th><span data-ttu-id="531ce-144">类或属性</span><span class="sxs-lookup"><span data-stu-id="531ce-144">Class or Attribute</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="531ce-145">用户</span><span class="sxs-lookup"><span data-stu-id="531ce-145">User</span></span></p></td>
<td><p><span data-ttu-id="531ce-146">add： mayContain</span><span class="sxs-lookup"><span data-stu-id="531ce-146">add: mayContain</span></span></p>
<p><span data-ttu-id="531ce-147">add： mayContain</span><span class="sxs-lookup"><span data-stu-id="531ce-147">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="531ce-148">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="531ce-148">ProxyAddresses</span></span></p>
<p><span data-ttu-id="531ce-149">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="531ce-149">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="531ce-150">联系人</span><span class="sxs-lookup"><span data-stu-id="531ce-150">Contact</span></span></p></td>
<td><p><span data-ttu-id="531ce-151">add： mayContain</span><span class="sxs-lookup"><span data-stu-id="531ce-151">add: mayContain</span></span></p>
<p><span data-ttu-id="531ce-152">add： mayContain</span><span class="sxs-lookup"><span data-stu-id="531ce-152">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="531ce-153">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="531ce-153">ProxyAddresses</span></span></p>
<p><span data-ttu-id="531ce-154">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="531ce-154">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="531ce-155">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="531ce-155">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="531ce-156">add： mayContain</span><span class="sxs-lookup"><span data-stu-id="531ce-156">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="531ce-157">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="531ce-157">msExchUserHoldPolicies</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="531ce-158">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="531ce-158">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="531ce-159">add： mayContain</span><span class="sxs-lookup"><span data-stu-id="531ce-159">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="531ce-160">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="531ce-160">msRTCSIP-MirrorBackEndServer</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="531ce-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="531ce-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

