---
title: Lync Server 2013：Registration 表
description: Lync Server 2013：注册表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration table
ms:assetid: 05ff9dd3-1aaa-4af0-bd69-8789fb8eaeb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398114(v=OCS.15)
ms:contentKeyID: 48183298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 806e1a4e944c9bc04ebdd167c41c80a57fde3f29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436564"
---
# <a name="registration-table-in-lync-server-2013"></a><span data-ttu-id="c95a3-103">Lync Server 2013 中的 Registration 表</span><span class="sxs-lookup"><span data-stu-id="c95a3-103">Registration table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c95a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c95a3-104">

<span> </span></span></span>

<span data-ttu-id="c95a3-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="c95a3-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="c95a3-106">每条记录表示一个用户注册事件。</span><span class="sxs-lookup"><span data-stu-id="c95a3-106">Each record represents one user registration event.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c95a3-107">列</span><span class="sxs-lookup"><span data-stu-id="c95a3-107">Column</span></span></th>
<th><span data-ttu-id="c95a3-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="c95a3-108">Data Type</span></span></th>
<th><span data-ttu-id="c95a3-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="c95a3-109">Key/Index</span></span></th>
<th><span data-ttu-id="c95a3-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="c95a3-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-112">datetime</span><span class="sxs-lookup"><span data-stu-id="c95a3-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="c95a3-113">主、外部</span><span class="sxs-lookup"><span data-stu-id="c95a3-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-114">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="c95a3-114">Time of session request.</span></span> <span data-ttu-id="c95a3-115">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="c95a3-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="c95a3-116">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c95a3-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-118">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-118">int</span></span></p></td>
<td><p><span data-ttu-id="c95a3-119">主、外部</span><span class="sxs-lookup"><span data-stu-id="c95a3-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-120">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="c95a3-120">ID number to identify the session.</span></span> <span data-ttu-id="c95a3-121">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="c95a3-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="c95a3-122">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c95a3-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-123"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-123"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-124">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-124">int</span></span></p></td>
<td><p><span data-ttu-id="c95a3-125">外表</span><span class="sxs-lookup"><span data-stu-id="c95a3-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-126">用户 ID。</span><span class="sxs-lookup"><span data-stu-id="c95a3-126">The user ID.</span></span> <span data-ttu-id="c95a3-127">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="c95a3-127">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-128"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-128"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-129">标识符</span><span class="sxs-lookup"><span data-stu-id="c95a3-129">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-130">用于标识注册终结点的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c95a3-130">A GUID to identify a registration endpoint.</span></span> <span data-ttu-id="c95a3-131">通常，来自同一用户的同一台计算机的注册事件将具有相同的终结点 ID。</span><span class="sxs-lookup"><span data-stu-id="c95a3-131">Usually the register event from the same computer of the same user will have the same endpoint ID.</span></span> <span data-ttu-id="c95a3-132">不同的计算机具有不同的终结点 ID。</span><span class="sxs-lookup"><span data-stu-id="c95a3-132">Different machines have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-133"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-133"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-134">标识符</span><span class="sxs-lookup"><span data-stu-id="c95a3-134">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-135">用于区分涉及同一用户和同一终结点的注册的 ID。</span><span class="sxs-lookup"><span data-stu-id="c95a3-135">ID used to differentiate registrations that involve the same user and the same endpoint.</span></span></p>
<p><span data-ttu-id="c95a3-136">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="c95a3-136">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-137"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-137"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-138">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-138">int</span></span></p></td>
<td><p><span data-ttu-id="c95a3-139">外表</span><span class="sxs-lookup"><span data-stu-id="c95a3-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-140">当前用户的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="c95a3-140">Client version of current user.</span></span> <span data-ttu-id="c95a3-141">有关详细信息，请参阅 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 中的 ClientVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c95a3-141">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-142"><strong>RegistrarId</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-142"><strong>RegistrarId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-143">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-143">int</span></span></p></td>
<td><p><span data-ttu-id="c95a3-144">外表</span><span class="sxs-lookup"><span data-stu-id="c95a3-144">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-145">用于注册的注册机构服务器的 ID。</span><span class="sxs-lookup"><span data-stu-id="c95a3-145">ID of the Registrar Server used for registration.</span></span> <span data-ttu-id="c95a3-146">有关详细信息，请参阅 <a href="lync-server-2013-servers-table.md">Lync Server 2013 中</a> 的 "服务器" 表。</span><span class="sxs-lookup"><span data-stu-id="c95a3-146">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-147"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-147"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-148">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-148">int</span></span></p></td>
<td><p><span data-ttu-id="c95a3-149">外表</span><span class="sxs-lookup"><span data-stu-id="c95a3-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-150">捕获会话的池的 ID。</span><span class="sxs-lookup"><span data-stu-id="c95a3-150">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="c95a3-151">有关详细信息，请参阅 <a href="lync-server-2013-pools-table.md">Lync Server 2013 中的 pool 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c95a3-151">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-152"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-152"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-153">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-153">int</span></span></p></td>
<td><p><span data-ttu-id="c95a3-154">外表</span><span class="sxs-lookup"><span data-stu-id="c95a3-154">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-155">注册要使用的边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="c95a3-155">Edge Server the registration is going through.</span></span> <span data-ttu-id="c95a3-156">有关详细信息，请参阅 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 中的 EdgeServers 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c95a3-156">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-157"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-157"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-158">位</span><span class="sxs-lookup"><span data-stu-id="c95a3-158">Bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-159">用户是否已从内部登录。</span><span class="sxs-lookup"><span data-stu-id="c95a3-159">Whether the user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-160"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-160"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-161">bit</span><span class="sxs-lookup"><span data-stu-id="c95a3-161">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-162">UserService 是否可用。</span><span class="sxs-lookup"><span data-stu-id="c95a3-162">Whether the UserService is available or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-163"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-163"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-164">bit</span><span class="sxs-lookup"><span data-stu-id="c95a3-164">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-165">是否注册到主注册机构。</span><span class="sxs-lookup"><span data-stu-id="c95a3-165">Whether register to the primary Registrar or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-166"><strong>IsPrimaryRegistrarCentral</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-166"><strong>IsPrimaryRegistrarCentral</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-167">bit</span><span class="sxs-lookup"><span data-stu-id="c95a3-167">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-168">指示用户是否已向 survivable 分支设备注册。</span><span class="sxs-lookup"><span data-stu-id="c95a3-168">Indicates whether or not the user is registered with a survivable branch appliance.</span></span></p>
<p><span data-ttu-id="c95a3-169">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="c95a3-169">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-170"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-170"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-171">datetime</span><span class="sxs-lookup"><span data-stu-id="c95a3-171">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-172">注册时间。</span><span class="sxs-lookup"><span data-stu-id="c95a3-172">Registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-173"><strong>DeRegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-173"><strong>DeRegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-174">datetime</span><span class="sxs-lookup"><span data-stu-id="c95a3-174">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-175">De-Registration 时间。</span><span class="sxs-lookup"><span data-stu-id="c95a3-175">De-Registration time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-176"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-176"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-177">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-177">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-178">注册请求的响应代码。</span><span class="sxs-lookup"><span data-stu-id="c95a3-178">Response code of the register request.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-179"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-179"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-180">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-180">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-181">注册请求的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="c95a3-181">Diagnostic ID of the register request.</span></span> <span data-ttu-id="c95a3-182">这表示诊断信息类型。</span><span class="sxs-lookup"><span data-stu-id="c95a3-182">This indicates that diagnostic information type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-183"><strong>Keyroutedeventargs.deviceid</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-183"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-184">int</span><span class="sxs-lookup"><span data-stu-id="c95a3-184">int</span></span></p></td>
<td><p><span data-ttu-id="c95a3-185">外表</span><span class="sxs-lookup"><span data-stu-id="c95a3-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-186">注册请求来自的设备。</span><span class="sxs-lookup"><span data-stu-id="c95a3-186">The device that the register request is coming from.</span></span> <span data-ttu-id="c95a3-187">有关详细信息，请参阅 <a href="lync-server-2013-devices-table.md">Lync Server 2013 中</a> 的 "设备" 表。</span><span class="sxs-lookup"><span data-stu-id="c95a3-187">See the <a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95a3-188"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-188"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="c95a3-189">tinyint</span></span></p></td>
<td><p><span data-ttu-id="c95a3-190">外表</span><span class="sxs-lookup"><span data-stu-id="c95a3-190">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95a3-191">取消注册的原因，如 "用户启动"、"注册到期"、"客户端失败" 等。</span><span class="sxs-lookup"><span data-stu-id="c95a3-191">The reason of de-register, such as ‘user initiated’, ‘registration expired’, ‘client fail’, and more.</span></span> <span data-ttu-id="c95a3-192">有关详细信息，请参阅 <a href="lync-server-2013-deregistertype-table.md">Lync Server 2013 中的 DeRegisterType 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c95a3-192">See the <a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95a3-193"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="c95a3-193"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="c95a3-194">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c95a3-194">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95a3-195">用户注册到的终结点的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="c95a3-195">IP address of the endpoint the user registered with.</span></span> <span data-ttu-id="c95a3-196">这可以是 IPv4 地址或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="c95a3-196">This can be an IPv4 address or an IPv6 address.</span></span></p>
<p><span data-ttu-id="c95a3-197">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="c95a3-197">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c95a3-198">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c95a3-198">


</div>

<span> </span>

</div>

</div>

</span></span></div>

