---
title: Lync Server 2013：注册视图
description: Lync Server 2013： "注册" 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration view
ms:assetid: 8a42bc7d-3d4f-43c1-9e15-89b2ee419ade
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688120(v=OCS.15)
ms:contentKeyID: 49733718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be169cafc324f89cacedda154ca49a8ff1ff39aa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392012"
---
# <a name="registration-view-in-lync-server-2013"></a><span data-ttu-id="0d9d8-103">Lync Server 2013 中的注册视图</span><span class="sxs-lookup"><span data-stu-id="0d9d8-103">Registration view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0d9d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0d9d8-104">

<span> </span></span></span>

<span data-ttu-id="0d9d8-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="0d9d8-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="0d9d8-106">"注册" 视图存储有关用户注册的信息。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-106">The Registration view stores information about user registration.</span></span> <span data-ttu-id="0d9d8-107">此视图已引入 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-107">This view was introduced in Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0d9d8-108">列</span><span class="sxs-lookup"><span data-stu-id="0d9d8-108">Column</span></span></th>
<th><span data-ttu-id="0d9d8-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="0d9d8-109">Data Type</span></span></th>
<th><span data-ttu-id="0d9d8-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="0d9d8-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-112">datetime</span><span class="sxs-lookup"><span data-stu-id="0d9d8-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-113">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-113">Time of session request.</span></span> <span data-ttu-id="0d9d8-114">与 SessionIdSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="0d9d8-115">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-117">int</span><span class="sxs-lookup"><span data-stu-id="0d9d8-117">int</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-118">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-118">ID number to identify the session.</span></span> <span data-ttu-id="0d9d8-119">与 SessionIdTime 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="0d9d8-120">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-121"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-121"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-122">datetime</span><span class="sxs-lookup"><span data-stu-id="0d9d8-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-123">发生注册的时间。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-123">Time at which registration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-124"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-124"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-125">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="0d9d8-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-126">注册用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-126">URI of the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-127"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-127"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-129">注册用户的 URI 的类型。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-129">Type of URI of the user who registered.</span></span> <span data-ttu-id="0d9d8-130">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-131"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-131"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-133">注册用户的租户。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-133">Tenant of the user who registered.</span></span> <span data-ttu-id="0d9d8-134">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-135"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-135"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-136">标识符</span><span class="sxs-lookup"><span data-stu-id="0d9d8-136">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-137">注册的用户终结点的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-137">Unique identifier of the endpoint of the user registered with.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-138"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-138"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-139">标识符</span><span class="sxs-lookup"><span data-stu-id="0d9d8-139">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-140">唯一标识符，用于区分涉及同一用户和同一终结点的注册。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-140">Unique identifier used to differentiate registrations that involve the same user and the same endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-141"><strong>DeRegisterType</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-141"><strong>DeRegisterType</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-142">datetime</span><span class="sxs-lookup"><span data-stu-id="0d9d8-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-143">发生取消注册的时间。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-143">Time at which deregistration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-144"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-144"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-146">取消注册的原因。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-146">Reason for deregistration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-147"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-147"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-148">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-148">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-149">注册用户使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-149">Version of client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-150"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-150"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-151">int</span><span class="sxs-lookup"><span data-stu-id="0d9d8-151">int</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-152">注册用户使用的客户端。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-152">Client used by the user who registered.</span></span> <span data-ttu-id="0d9d8-153">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-153">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-154"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-154"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-155">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="0d9d8-155">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-156">注册用户使用的客户端的类别。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-156">Category of the client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-157"><strong>地址</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-157"><strong>IpAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-158">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-158">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-159">用户注册使用的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-159">IP Address the user registered with.</span></span> <span data-ttu-id="0d9d8-160">这可能是 IPv4 或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-160">This may be an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-161"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-161"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-162">varstring (775) </span><span class="sxs-lookup"><span data-stu-id="0d9d8-162">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-163">SIP 对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-163">SIP dialog ID.</span></span> <span data-ttu-id="0d9d8-164">的格式为：</span><span class="sxs-lookup"><span data-stu-id="0d9d8-164">The format of the is:</span></span></p>
<p><span data-ttu-id="0d9d8-165">对话框; 从-标签; 到-标记</span><span class="sxs-lookup"><span data-stu-id="0d9d8-165">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-166"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-166"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-167">int</span><span class="sxs-lookup"><span data-stu-id="0d9d8-167">int</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-168">会议邀请的 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-168">SIP response code to the session invitation.</span></span> <span data-ttu-id="0d9d8-169">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-169">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="0d9d8-170">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-170">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-171"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-171"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-172">int</span><span class="sxs-lookup"><span data-stu-id="0d9d8-172">int</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-173">从 SIP 标题捕获的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-173">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-174"><strong>注册器</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-174"><strong>Registrar</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-176">注册机构的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-176">FQDN of the Registrar.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-177"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-177"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-179">捕获会话的数据的池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-179">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-180"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-180"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-182">注册用户使用的边缘服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-182">FQDN of the Edge Server used by the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-183"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-183"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-184">bit</span><span class="sxs-lookup"><span data-stu-id="0d9d8-184">bit</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-185">指示用户是否从内部网络登录。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-185">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-186"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-186"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-187">bit</span><span class="sxs-lookup"><span data-stu-id="0d9d8-187">bit</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-188">指示 UserService 在注册时是否可用。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-188">Indicates whether the UserService was available at registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-189"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-189"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-190">bit</span><span class="sxs-lookup"><span data-stu-id="0d9d8-190">bit</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-191">指示注册是否与主注册机构一起注册。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-191">Indicates whether registration was with the primary Registrar.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-192"><strong>DeviceMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-192"><strong>DeviceMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-193">bigint</span><span class="sxs-lookup"><span data-stu-id="0d9d8-193">bigint</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-194">注册的设备的 MAC 地址。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-194">MAC Address of device registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9d8-195"><strong>DeviceManufacturer</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-195"><strong>DeviceManufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-197">注册设备的制造商。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-197">Manufacturer of the device registered.</span></span> <span data-ttu-id="0d9d8-198">有关详细信息，请参阅 <a href="lync-server-2013-manufacturers-table.md">Lync Server 2013 中的制造商表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-198">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9d8-199"><strong>DeviceHardwareVersion</strong></span><span class="sxs-lookup"><span data-stu-id="0d9d8-199"><strong>DeviceHardwareVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="0d9d8-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0d9d8-201">注册设备的硬件版本。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-201">Hardware version of the device registered.</span></span> <span data-ttu-id="0d9d8-202">有关详细信息，请参阅 <a href="lync-server-2013-hardwareversions-table.md">Lync Server 2013 中的 HardwareVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0d9d8-202">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0d9d8-203">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0d9d8-203">


</div>

<span> </span>

</div>

</div>

</span></span></div>

