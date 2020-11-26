---
title: Lync Server 2013： Grant-CsOUPermission 所做的更改
description: Lync Server 2013：通过授予-CsOUPermission 进行的更改。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsOUPermission
ms:assetid: d744d352-1ad9-4447-8e2b-28e768d2ed1b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205310(v=OCS.15)
ms:contentKeyID: 48185564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10d3db0e9dde380628690bc016e2b4bd2ec85b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435052"
---
# <a name="changes-made-by-grant-csoupermission-in-lync-server-2013"></a><span data-ttu-id="96d3a-103">Lync Server 2013 中 Grant-CsOUPermission 所做的更改</span><span class="sxs-lookup"><span data-stu-id="96d3a-103">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96d3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96d3a-104">

<span> </span></span></span>

<span data-ttu-id="96d3a-105">_**主题上次修改时间：** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="96d3a-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="96d3a-106">若要委派 Lync Server 2013 管理，可以向指定组织单位 (Ou) 添加权限，以便林准备创建的 RTC 通用组的成员无需成为域管理员组的成员即可访问 Ou。</span><span class="sxs-lookup"><span data-stu-id="96d3a-106">To delegate Lync Server 2013 administration, you can add permissions to specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access the OUs without being members of the Domain Admins group.</span></span>

<span data-ttu-id="96d3a-107">**CsOuPermission** cmdlet 按下表中指定的方式向指定 OU 中的对象授予权限。</span><span class="sxs-lookup"><span data-stu-id="96d3a-107">The **Grant-CsOuPermission** cmdlet grants permissions to objects in the specified OU as specified in the following tables.</span></span>

<div>

## <a name="granting-permission-for-user-objects"></a><span data-ttu-id="96d3a-108">为用户对象授予权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-108">Granting Permission for User Objects</span></span>

<span data-ttu-id="96d3a-109">在 OU 上运行用户对象的 **CsOuPermission** cmdlet 时，将向组授予下表中所示的权限。</span><span class="sxs-lookup"><span data-stu-id="96d3a-109">When you run the **Grant-CsOuPermission** cmdlet for User objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-user-objects"></a><span data-ttu-id="96d3a-110">为用户对象授予的权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-110">Permissions Granted for User Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96d3a-111">团队</span><span class="sxs-lookup"><span data-stu-id="96d3a-111">Group</span></span></th>
<th><span data-ttu-id="96d3a-112">权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-112">Permission</span></span></th>
<th><span data-ttu-id="96d3a-113">适用于</span><span class="sxs-lookup"><span data-stu-id="96d3a-113">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-114">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="96d3a-114">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="96d3a-115">复制目录更改</span><span class="sxs-lookup"><span data-stu-id="96d3a-115">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="96d3a-116">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-116">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-117">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-117">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-118">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-118">List contents</span></span></p>
<p><span data-ttu-id="96d3a-119">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-119">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-120">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-120">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-121">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-121">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-122">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-122">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-123">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-123">List contents</span></span></p>
<p><span data-ttu-id="96d3a-124">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-124">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-125">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-125">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-126">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-126">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-127">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-127">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-128">阅读 RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-128">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-129">阅读 RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-129">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-130">阅读 RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-130">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-131">阅读 Public-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-131">Read Public-Information</span></span></p>
<p><span data-ttu-id="96d3a-132">阅读 General-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-132">Read General-Information</span></span></p>
<p><span data-ttu-id="96d3a-133">阅读用户-帐户限制</span><span class="sxs-lookup"><span data-stu-id="96d3a-133">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-134">子代用户对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-134">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-135">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="96d3a-135">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="96d3a-136">写 RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-136">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-137">写 msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="96d3a-137">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="96d3a-138">写 RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-138">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-139">写 RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-139">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-140">写 proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="96d3a-140">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="96d3a-141">子代用户对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-141">Descendant User objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-computer-objects"></a><span data-ttu-id="96d3a-142">为计算机对象授予权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-142">Granting Permission for Computer Objects</span></span>

<span data-ttu-id="96d3a-143">在 OU 上运行计算机对象的 **CsOuPermission** cmdlet 时，将向组授予下表中所示的权限。</span><span class="sxs-lookup"><span data-stu-id="96d3a-143">When you run the **Grant-CsOuPermission** cmdlet for Computer objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-computer-objects"></a><span data-ttu-id="96d3a-144">为计算机对象授予的权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-144">Permissions Granted for Computer Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96d3a-145">团队</span><span class="sxs-lookup"><span data-stu-id="96d3a-145">Group</span></span></th>
<th><span data-ttu-id="96d3a-146">权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-146">Permission</span></span></th>
<th><span data-ttu-id="96d3a-147">适用于</span><span class="sxs-lookup"><span data-stu-id="96d3a-147">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-148">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="96d3a-148">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="96d3a-149">复制目录更改</span><span class="sxs-lookup"><span data-stu-id="96d3a-149">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="96d3a-150">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-150">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-151">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-151">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-152">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-152">List contents</span></span></p>
<p><span data-ttu-id="96d3a-153">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-153">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-154">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-154">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-155">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-155">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-156">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-156">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-157">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-157">List contents</span></span></p>
<p><span data-ttu-id="96d3a-158">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-158">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-159">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-159">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-160">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-160">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-161">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-161">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-162">阅读 Public-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-162">Read Public-Information</span></span></p>
<p><span data-ttu-id="96d3a-163">读取已验证的 DNS 主机名</span><span class="sxs-lookup"><span data-stu-id="96d3a-163">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="96d3a-164">子体计算机对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-164">Descendant Computer objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-165">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="96d3a-165">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="96d3a-166">阅读 Public-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-166">Read Public-Information</span></span></p>
<p><span data-ttu-id="96d3a-167">读取已验证的 DNS 主机名</span><span class="sxs-lookup"><span data-stu-id="96d3a-167">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="96d3a-168">子体计算机对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-168">Descendant Computer objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-contact-or-appcontact-objects"></a><span data-ttu-id="96d3a-169">授予联系人或 AppContact 对象的权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-169">Granting Permission for Contact or AppContact Objects</span></span>

<span data-ttu-id="96d3a-170">当你为某个 OU 上的 Contact 对象或 AppContact 对象运行 **CsOuPermission** cmdlet 时，将向组授予下表中所示的权限。</span><span class="sxs-lookup"><span data-stu-id="96d3a-170">When you run the **Grant-CsOuPermission** cmdlet for Contact objects or AppContact objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-contact-or-appcontact-objects"></a><span data-ttu-id="96d3a-171">为联系人或 AppContact 对象授予的权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-171">Permissions Granted for Contact or AppContact Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96d3a-172">团队</span><span class="sxs-lookup"><span data-stu-id="96d3a-172">Group</span></span></th>
<th><span data-ttu-id="96d3a-173">权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-173">Permission</span></span></th>
<th><span data-ttu-id="96d3a-174">适用于</span><span class="sxs-lookup"><span data-stu-id="96d3a-174">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-175">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="96d3a-175">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="96d3a-176">复制目录更改</span><span class="sxs-lookup"><span data-stu-id="96d3a-176">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="96d3a-177">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-177">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-178">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-178">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-179">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-179">List contents</span></span></p>
<p><span data-ttu-id="96d3a-180">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-180">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-181">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-181">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-182">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-182">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-183">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-183">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-184">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-184">List contents</span></span></p>
<p><span data-ttu-id="96d3a-185">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-185">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-186">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-186">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-187">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-187">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-188">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-188">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-189">阅读 RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-189">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-190">阅读 RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-190">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-191">阅读 RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-191">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-192">阅读 Public-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-192">Read Public-Information</span></span></p>
<p><span data-ttu-id="96d3a-193">阅读 General-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-193">Read General-Information</span></span></p>
<p><span data-ttu-id="96d3a-194">阅读 Personal-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-194">Read Personal-Information</span></span></p>
<p><span data-ttu-id="96d3a-195">阅读用户-帐户限制</span><span class="sxs-lookup"><span data-stu-id="96d3a-195">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-196">子代联系人对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-196">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-197">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="96d3a-197">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="96d3a-198">写 RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-198">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-199">写 otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="96d3a-199">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="96d3a-200">写入 displayName</span><span class="sxs-lookup"><span data-stu-id="96d3a-200">Write displayName</span></span></p>
<p><span data-ttu-id="96d3a-201">写入说明</span><span class="sxs-lookup"><span data-stu-id="96d3a-201">Write description</span></span></p>
<p><span data-ttu-id="96d3a-202">写 telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="96d3a-202">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="96d3a-203">写 msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="96d3a-203">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="96d3a-204">写 RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-204">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-205">写 RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-205">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-206">写 proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="96d3a-206">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="96d3a-207">子代联系人对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-207">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-device-objects"></a><span data-ttu-id="96d3a-208">为设备对象授予权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-208">Granting Permission for Device Objects</span></span>

<span data-ttu-id="96d3a-209">在 OU 上运行设备对象的 **CsOuPermission** cmdlet 时，将向组授予下表中所示的权限。</span><span class="sxs-lookup"><span data-stu-id="96d3a-209">When you run the **Grant-CsOuPermission** cmdlet for Device objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-device-objects"></a><span data-ttu-id="96d3a-210">为设备对象授予的权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-210">Permissions Granted for Device Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96d3a-211">团队</span><span class="sxs-lookup"><span data-stu-id="96d3a-211">Group</span></span></th>
<th><span data-ttu-id="96d3a-212">权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-212">Permission</span></span></th>
<th><span data-ttu-id="96d3a-213">适用于</span><span class="sxs-lookup"><span data-stu-id="96d3a-213">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-214">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="96d3a-214">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="96d3a-215">复制目录更改</span><span class="sxs-lookup"><span data-stu-id="96d3a-215">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="96d3a-216">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-216">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-217">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-217">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-218">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-218">List contents</span></span></p>
<p><span data-ttu-id="96d3a-219">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-219">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-220">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-220">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-221">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-221">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-222">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-222">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-223">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-223">List contents</span></span></p>
<p><span data-ttu-id="96d3a-224">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-224">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-225">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-225">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-226">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-226">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-227">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-227">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-228">阅读 RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-228">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-229">阅读 RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-229">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-230">阅读 RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-230">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-231">阅读 Public-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-231">Read Public-Information</span></span></p>
<p><span data-ttu-id="96d3a-232">阅读 Personal-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-232">Read Personal-Information</span></span></p>
<p><span data-ttu-id="96d3a-233">阅读 General-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-233">Read General-Information</span></span></p>
<p><span data-ttu-id="96d3a-234">阅读用户-帐户限制</span><span class="sxs-lookup"><span data-stu-id="96d3a-234">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-235">子代联系人对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-235">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-236">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="96d3a-236">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="96d3a-237">创建子元素</span><span class="sxs-lookup"><span data-stu-id="96d3a-237">Create child</span></span></p>
<p><span data-ttu-id="96d3a-238">删除子元素</span><span class="sxs-lookup"><span data-stu-id="96d3a-238">Delete child</span></span></p>
<p><span data-ttu-id="96d3a-239">删除树</span><span class="sxs-lookup"><span data-stu-id="96d3a-239">Delete tree</span></span></p></td>
<td><p><span data-ttu-id="96d3a-240">联系人</span><span class="sxs-lookup"><span data-stu-id="96d3a-240">Contact</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-241">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="96d3a-241">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="96d3a-242">写入 displayName</span><span class="sxs-lookup"><span data-stu-id="96d3a-242">Write displayName</span></span></p>
<p><span data-ttu-id="96d3a-243">写入说明</span><span class="sxs-lookup"><span data-stu-id="96d3a-243">Write description</span></span></p>
<p><span data-ttu-id="96d3a-244">写 telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="96d3a-244">Write telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="96d3a-245">子代用户对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-245">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-246">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="96d3a-246">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="96d3a-247">写 RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-247">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-248">写 otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="96d3a-248">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="96d3a-249">写入 displayName</span><span class="sxs-lookup"><span data-stu-id="96d3a-249">Write displayName</span></span></p>
<p><span data-ttu-id="96d3a-250">写入说明</span><span class="sxs-lookup"><span data-stu-id="96d3a-250">Write description</span></span></p>
<p><span data-ttu-id="96d3a-251">写 telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="96d3a-251">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="96d3a-252">写 msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="96d3a-252">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="96d3a-253">写 RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-253">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-254">写 RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-254">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-255">写 proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="96d3a-255">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="96d3a-256">子代联系人对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-256">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-inetorgperson-objects"></a><span data-ttu-id="96d3a-257">为 InetOrgPerson 对象授予权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-257">Granting Permission for InetOrgPerson Objects</span></span>

<span data-ttu-id="96d3a-258">当你针对 OU 上的 InetOrgPerson 对象运行 **CsOuPermission** cmdlet 时，将向组授予下表中所示的权限。</span><span class="sxs-lookup"><span data-stu-id="96d3a-258">When you run the **Grant-CsOuPermission** cmdlet for InetOrgPerson objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-inetorgperson-objects"></a><span data-ttu-id="96d3a-259">为 InetOrgPerson 对象授予的权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-259">Permissions Granted for InetOrgPerson Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96d3a-260">团队</span><span class="sxs-lookup"><span data-stu-id="96d3a-260">Group</span></span></th>
<th><span data-ttu-id="96d3a-261">权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-261">Permission</span></span></th>
<th><span data-ttu-id="96d3a-262">适用于</span><span class="sxs-lookup"><span data-stu-id="96d3a-262">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-263">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="96d3a-263">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="96d3a-264">复制目录更改</span><span class="sxs-lookup"><span data-stu-id="96d3a-264">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="96d3a-265">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-265">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-266">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-266">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-267">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-267">List contents</span></span></p>
<p><span data-ttu-id="96d3a-268">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-268">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-269">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-269">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-270">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-270">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-271">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-271">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-272">列表内容</span><span class="sxs-lookup"><span data-stu-id="96d3a-272">List contents</span></span></p>
<p><span data-ttu-id="96d3a-273">读取所有属性</span><span class="sxs-lookup"><span data-stu-id="96d3a-273">Read all properties</span></span></p>
<p><span data-ttu-id="96d3a-274">读取权限</span><span class="sxs-lookup"><span data-stu-id="96d3a-274">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-275">仅此对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-275">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96d3a-276">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="96d3a-276">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="96d3a-277">阅读 RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-277">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-278">阅读 RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-278">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-279">阅读 RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-279">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-280">阅读 Personal-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-280">Read Personal-Information</span></span></p>
<p><span data-ttu-id="96d3a-281">阅读 Public-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-281">Read Public-Information</span></span></p>
<p><span data-ttu-id="96d3a-282">阅读 General-Information</span><span class="sxs-lookup"><span data-stu-id="96d3a-282">Read General-Information</span></span></p>
<p><span data-ttu-id="96d3a-283">阅读用户-帐户限制</span><span class="sxs-lookup"><span data-stu-id="96d3a-283">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="96d3a-284">子代 inetOrgPerson 对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-284">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96d3a-285">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="96d3a-285">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="96d3a-286">写 RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-286">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-287">写 RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-287">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-288">写 RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="96d3a-288">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="96d3a-289">写 proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="96d3a-289">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="96d3a-290">子代 inetOrgPerson 对象</span><span class="sxs-lookup"><span data-stu-id="96d3a-290">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="96d3a-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96d3a-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

