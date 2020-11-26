---
title: Lync Server 2013：CDR 表的列表
description: Lync Server 2013： CDR 表的列表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of CDR tables
ms:assetid: 031843fd-c7ff-4534-9b02-8847aad70807
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398084(v=OCS.15)
ms:contentKeyID: 48183254
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 21d0f683ffeb0f5f1cbba5db4c45d248aa14e8e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426611"
---
# <a name="list-of-cdr-tables-in-lync-server-2013"></a><span data-ttu-id="c3cad-103">Lync Server 2013 中 CDR 表的列表</span><span class="sxs-lookup"><span data-stu-id="c3cad-103">List of CDR tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3cad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3cad-104">

<span> </span></span></span>

<span data-ttu-id="c3cad-105">_**主题上次修改时间：** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="c3cad-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="c3cad-106"> (CDR) 数据库架构的 "呼叫详细信息" 录制包括下表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-106">The call detail recording (CDR) database schema consists of the following tables.</span></span>

<div>

## <a name="static-tables"></a><span data-ttu-id="c3cad-107">静态表</span><span class="sxs-lookup"><span data-stu-id="c3cad-107">Static Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-108">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-108">Table</span></span></th>
<th><span data-ttu-id="c3cad-109">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-110"><a href="lync-server-2013-callpriorities-table.md">Lync Server 2013 中的 CallPriorities 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-110"><a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-111">存储可能的通话优先级列表，例如紧急情况、紧急、普通、非紧急等。</span><span class="sxs-lookup"><span data-stu-id="c3cad-111">Stores the list of possible call priorities, such as emergency, urgent, normal, non-urgent, and more.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-112"><a href="lync-server-2013-conferencejointimethresholds-table.md">Lync Server 2013 中的 ConferenceJoinTimeThresholds 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-112"><a href="lync-server-2013-conferencejointimethresholds-table.md">ConferenceJoinTimeThresholds table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-113">存储 "会议加入时间摘要" 报表使用的分类边界。</span><span class="sxs-lookup"><span data-stu-id="c3cad-113">Stores the classification boundaries used by the Conference Join Time Summary Report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-114"><a href="lync-server-2013-deregistertype-table.md">Lync Server 2013 中的 DeRegisterType 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-114"><a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-115">存储可能的用户取消注册原因的列表，例如 &quot; 客户端启动、 &quot; &quot; 注册过期、 &quot; &quot; 客户端崩溃等 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c3cad-115">Stores the list of possible user de-register reasons, such as &quot;client initiated,&quot; &quot;registration expired,&quot; &quot;client crash,&quot; and more.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-116"><a href="lync-server-2013-medialist-table.md">Lync Server 2013 中的 MediaList 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-116"><a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-117">存储可在数据库中生成条目的媒体类型的列表 (例如，IM、音频、视频和文件传输) 。</span><span class="sxs-lookup"><span data-stu-id="c3cad-117">Stores the list of media types that can generate entries in the database (for example, IM, audio, video, and file transfer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-118"><a href="lync-server-2013-purgesettings-table.md">Lync Server 2013 中的 PurgeSettings 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-118"><a href="lync-server-2013-purgesettings-table.md">PurgeSettings table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-119">存储用于指定) 过期的呼叫详细记录 (是否会自动从 CDR 数据库中删除的信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-119">Stores information that specifies if (and when) outdated call detail records will automatically be deleted from the CDR database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-120"><a href="lync-server-2013-roles-table.md">Lync Server 2013 中的 Roles 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-120"><a href="lync-server-2013-roles-table.md">Roles table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-121">存储可能的会议角色列表 (例如，与会者和演示者) 。</span><span class="sxs-lookup"><span data-stu-id="c3cad-121">Stores the list of possible conference roles (for example, attendee and presenter).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-122"><a href="lync-server-2013-sipresponsemetadata-table.md">Lync Server 2013 中的 SIPResponseMetaData 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-122"><a href="lync-server-2013-sipresponsemetadata-table.md">SIPResponseMetaData table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-123">存储 SIP 响应代码的列表以及每个代码的分类和定义。</span><span class="sxs-lookup"><span data-stu-id="c3cad-123">Stores a list of SIP response codes and the classification and definition of each of those codes.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supporting-tables"></a><span data-ttu-id="c3cad-124">支持表</span><span class="sxs-lookup"><span data-stu-id="c3cad-124">Supporting Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-125">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-125">Table</span></span></th>
<th><span data-ttu-id="c3cad-126">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-127"><a href="lync-server-2013-clientversions-table.md">Lync Server 2013 中的 ClientVersions 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-127"><a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-128">将客户端存储在使用此数据库中捕获的信息的通话中涉及的每个客户端的客户端类型和版本号)  (。</span><span class="sxs-lookup"><span data-stu-id="c3cad-128">Stores the clients (both client type and version number) of each client involved in a call with information captured in this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-129"><a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 中的 ConferenceUris 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-129"><a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-130">存储与会议相关的通话中使用的 ConferenceURIs 列表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-130">Stores a list of ConferenceURIs that are used in conference related calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-131"><a href="lync-server-2013-contenttypes-table.md">Lync Server 2013 中的 ContentTypes 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-131"><a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-132">存储在对等呼叫和电话会议中使用的会话初始协议 (SIP) 内容类型的列表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-132">Stores a list of Session Initiation Protocol (SIP) content types that are used in both peer-to-peer calls and conference calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-133"><a href="lync-server-2013-devices-table.md">Lync Server 2013 中的 Devices 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-133"><a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-134">存储设备列表，包括制造商、硬件版本和 MAC 地址。</span><span class="sxs-lookup"><span data-stu-id="c3cad-134">Stores a list of devices, including their manufacturer, hardware version, and MAC address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-135"><a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的 Dialogs 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-135"><a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-136">存储有关数据库中每个会话的对话框 ID 的信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-136">Stores information about the Dialog ID for each session in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-137"><a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 中的 EdgeServers 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-137"><a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-138">存储用于外部呼叫的边缘服务器的列表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-138">Stores a list of Edge Servers that are used for external calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-139"><a href="lync-server-2013-gateways-table.md">Lync Server 2013 中的 Gateways 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-139"><a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-140">存储用于通过 Internet 协议 (VoIP) 呼叫的网关的列表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-140">Stores a list of Gateways that are used for Voice over Internet Protocol (VoIP) calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-141"><a href="lync-server-2013-hardwareversions-table.md">Lync Server 2013 中的 HardwareVersions 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-141"><a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-142">存储 (桌面电话) 的设备的硬件版本列表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-142">Stores a list of hardware versions of devices (desk phone).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-143"><a href="lync-server-2013-manufacturers-table.md">Lync Server 2013 中的 Manufacturers 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-143"><a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-144">存储 (桌面电话) 的设备制造商列表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-144">Stores a list of manufacturers of devices (desk phone).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-145"><a href="lync-server-2013-mcus-table.md">Lync Server 2013 中的 Mcus 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-145"><a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-146">存储有关各种 A/V 会议服务器及其 Uri 的信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-146">Stores information about the various A/V Conferencing Servers and their URIs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-147"><a href="lync-server-2013-mediationservers-table.md">Lync Server 2013 中的 MediationServers 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-147"><a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-148">存储用于 VoIP 呼叫的中介服务器的列表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-148">Stores a list of Mediation Servers that are used for VoIP calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-149"><a href="lync-server-2013-phones-table.md">Lync Server 2013 中的 Phones 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-149"><a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-150">存储在已存档或已记录其通话详细信息的 VoIP 呼叫中使用的所有电话号码。</span><span class="sxs-lookup"><span data-stu-id="c3cad-150">Stores all the phone numbers used in VoIP calls that were archived or whose call details were recorded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-151"><a href="lync-server-2013-pools-table.md">Lync Server 2013 中的 Pools 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-151"><a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-152">存储在其上捕获即时消息的池的名称。</span><span class="sxs-lookup"><span data-stu-id="c3cad-152">Stores the names of the pool on which IM messages are captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-153"><a href="lync-server-2013-servers-table.md">Lync Server 2013 中的 Servers 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-153"><a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-154">存储通话中涉及的服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="c3cad-154">Stores the name of servers involved in calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-155"><a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的 Tenants 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-155"><a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-156">存储当前部署支持的租户。</span><span class="sxs-lookup"><span data-stu-id="c3cad-156">Stores the tenants supported by current deployment.</span></span> <span data-ttu-id="c3cad-157">企业用户、联合用户、公共 IM 连接用户和匿名用户有一些内置租户。</span><span class="sxs-lookup"><span data-stu-id="c3cad-157">There some build-in tenants for Enterprise user, Federated User, public IM connectivity user, and Anonymous users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-158"><a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-158"><a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-159">将用户代理标识符映射到代理的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="c3cad-159">Maps user agent identifiers to the agent’s descriptive names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-160"><a href="lync-server-2013-users-table.md">Lync Server 2013 中的 Users 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-160"><a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-161">存储参与此数据库中记录或存档的会话的用户的用户 Uri。</span><span class="sxs-lookup"><span data-stu-id="c3cad-161">Stores the user URIs of users who have participated in sessions recorded or archived in this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-162"><a href="lync-server-2013-userstatistics-table.md">Lync Server 2013 中的 UserStatistics 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-162"><a href="lync-server-2013-userstatistics-table.md">UserStatistics table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-163">存储有关个人用户对系统的使用情况的信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-163">Stores information about an individual user’s usage of the system.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-specific-to-conference-cdr-records"></a><span data-ttu-id="c3cad-164">特定于会议 CDR 记录的表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-164">Tables Specific to Conference CDR Records</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-165">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-165">Table</span></span></th>
<th><span data-ttu-id="c3cad-166">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-167"><a href="lync-server-2013-conferences-table.md">Lync Server 2013 中的 Conferences 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-167"><a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-168">存储有关已存档或记录其详细信息的所有会议的信息，包括 ConferenceURI 和开始时间和结束时间。</span><span class="sxs-lookup"><span data-stu-id="c3cad-168">Stores information about all conferences that were archived or whose details were recorded, including ConferenceURI, and start and end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-169"><a href="lync-server-2013-conferencesessiondetails-table.md">Lync Server 2013 中的 ConferenceSessionDetails 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-169"><a href="lync-server-2013-conferencesessiondetails-table.md">ConferenceSessionDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-170">存储有关每个基于 SIP 的会议会话的信息，包括开始和结束时间、用户 ID、响应代码和每个会话的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="c3cad-170">Stores information about every SIP-based conference session, including start and end time, user ID, response code, and diagnostic ID for each session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-171"><a href="lync-server-2013-focusjoinsandleaves-table.md">Lync Server 2013 中的 FocusJoinsAndLeaves 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-171"><a href="lync-server-2013-focusjoinsandleaves-table.md">FocusJoinsAndLeaves table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-172">存储有关会议加入和保留的信息，包括用户的角色和客户端版本。</span><span class="sxs-lookup"><span data-stu-id="c3cad-172">Stores information about conference joins and leaves, including users’ role and client version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-173"><a href="lync-server-2013-mcujoinsandleaves-table.md">Lync Server 2013 中的 McuJoinsAndLeaves 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-173"><a href="lync-server-2013-mcujoinsandleaves-table.md">McuJoinsAndLeaves table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-174">存储有关会议和用户加入以及休假时间的 A/V 会议服务器的相关信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-174">Stores information about the A/V Conferencing Servers that are involved in a conference and the user join and leave times.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-messages-in-im-conferences"></a><span data-ttu-id="c3cad-175">IM 会议中的消息表</span><span class="sxs-lookup"><span data-stu-id="c3cad-175">Tables for Messages in IM Conferences</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-176">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-176">Table</span></span></th>
<th><span data-ttu-id="c3cad-177">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-178"><a href="lync-server-2013-conferencemessagecount-table.md">Lync Server 2013 中的 ConferenceMessageCount 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-178"><a href="lync-server-2013-conferencemessagecount-table.md">ConferenceMessageCount table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-179">对于每个 IM 会议，存储每个用户发送的邮件数。</span><span class="sxs-lookup"><span data-stu-id="c3cad-179">For each IM conference, stores the number of messages that were sent by each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-180"><a href="lync-server-2013-imreportsummary-table.md">Lync Server 2013 中的 IMReportSummary 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-180"><a href="lync-server-2013-imreportsummary-table.md">IMReportSummary table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-181">提供组织中保留的即时消息会话的整体报告。</span><span class="sxs-lookup"><span data-stu-id="c3cad-181">Provides an overall report on the instant messaging sessions held in an organization.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-peer-to-peer-sessions"></a><span data-ttu-id="c3cad-182">对等会话的表</span><span class="sxs-lookup"><span data-stu-id="c3cad-182">Tables for Peer-to-Peer Sessions</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-183">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-183">Table</span></span></th>
<th><span data-ttu-id="c3cad-184">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-185"><a href="lync-server-2013-sessiondetails-table.md">Lync Server 2013 中的 SessionDetails 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-185"><a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-186">存储每个对等会话的相关信息，包括开始和结束时间、用户 ID、响应代码和每个用户的邮件计数。</span><span class="sxs-lookup"><span data-stu-id="c3cad-186">Stores information about every peer-to-peer session, including start and end time, user ID, response code, and message count for each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-187"><a href="lync-server-2013-filetransfers-table.md">Lync Server 2013 中的 FileTransfers 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-187"><a href="lync-server-2013-filetransfers-table.md">FileTransfers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-188">存储有关文件传输会话的信息，包括文件名和结果 (接受、拒绝或取消) 。</span><span class="sxs-lookup"><span data-stu-id="c3cad-188">Stores information about file transfer sessions, including file name and result (accepted, rejected, or canceled).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-189"><a href="lync-server-2013-media-table.md">Lync Server 2013 中的 Media 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-189"><a href="lync-server-2013-media-table.md">Media table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-190">存储对等会话中涉及的不同媒体类型的相关信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-190">Stores information about the different media types involved in peer-to-peer sessions.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="table-for-voip-call-details"></a><span data-ttu-id="c3cad-191">VoIP 呼叫详细信息表</span><span class="sxs-lookup"><span data-stu-id="c3cad-191">Table for VoIP Call Details</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-192">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-192">Table</span></span></th>
<th><span data-ttu-id="c3cad-193">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-194"><a href="lync-server-2013-voipdetails-table.md">Lync Server 2013 中的 VoipDetails 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-194"><a href="lync-server-2013-voipdetails-table.md">VoipDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-195">对于每个两方 VoIP/PSTN 呼叫，存储有关呼叫的信息，例如 VoIP 电话的电话 ID、使用的网关以及哪一方断开连接。</span><span class="sxs-lookup"><span data-stu-id="c3cad-195">For each two-party VoIP/PSTN call, stores information about the call, such as the phone ID of VoIP phone, gateway used, and which party disconnected.</span></span> <span data-ttu-id="c3cad-196">指 <a href="lync-server-2013-sessiondetails-table.md">Lync Server 2013 中的 SessionDetails 表</a> ，用于呼叫开始/结束时间和响应代码。</span><span class="sxs-lookup"><span data-stu-id="c3cad-196">Refers to the <a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a> for call start/end times and response code.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="c3cad-197">如果呼叫中的一方是 VoIP 用户，或者在呼叫中涉及中介服务器，则会在此表中创建记录。</span><span class="sxs-lookup"><span data-stu-id="c3cad-197">If one party on a call is a VoIP user or if a Mediation Server was involved in the call, a record will be created in this table.</span></span> <span data-ttu-id="c3cad-198">在 <A href="lync-server-2013-sessiondetails-table.md">Lync Server 2013 的 SessionDetails 表</A>中捕获了不涉及公共交换电话网络的 VoIP/voip 呼叫的信息 (PSTN) phone。</span><span class="sxs-lookup"><span data-stu-id="c3cad-198">Information about VoIP/VoIP calls not involving a public switched telephone network (PSTN) phone is captured in the <A href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</A>.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="table-for-e9-1-1-call-auditing"></a><span data-ttu-id="c3cad-199">E9 的表-1-1-通话审核</span><span class="sxs-lookup"><span data-stu-id="c3cad-199">Table for E9-1-1 Call Auditing</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-200">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-200">Table</span></span></th>
<th><span data-ttu-id="c3cad-201">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-201">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-202"><a href="lync-server-2013-locations-table.md">Lync Server 2013 中的 Locations 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-202"><a href="lync-server-2013-locations-table.md">Locations table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-203">对于每个紧急电话（例如，增强的 9-1-1 (E9-1) 呼叫）存储有关通话的位置信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-203">For each emergency call, such as an Enhanced 9-1-1 (E9-1-1) call, stores location information about the call.</span></span> <span data-ttu-id="c3cad-204">指 <a href="lync-server-2013-sessiondetails-table.md">Lync Server 2013 中的 SessionDetails 表</a> ，用于呼叫开始/结束时间和响应代码。</span><span class="sxs-lookup"><span data-stu-id="c3cad-204">Refers to the <a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a> for call start/end times and response code.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="c3cad-205">此表仅包含 E9-1-1 调用的位置 blob。</span><span class="sxs-lookup"><span data-stu-id="c3cad-205">This table only contains the location blob for the E9-1-1 call.</span></span> <span data-ttu-id="c3cad-206">有关通话的其他详细信息，请参阅 SessionDetails 表。</span><span class="sxs-lookup"><span data-stu-id="c3cad-206">Refers to the SessionDetails table for other detailed information about the call.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-troubleshooting"></a><span data-ttu-id="c3cad-207">用于疑难解答的表</span><span class="sxs-lookup"><span data-stu-id="c3cad-207">Tables for Troubleshooting</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-208">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-208">Table</span></span></th>
<th><span data-ttu-id="c3cad-209">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-210"><a href="lync-server-2013-application-table.md">Lync Server 2013 中的 Application 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-210"><a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-211">存储有关在路由和连接中涉及的 Lync Server 2013 中的各种进程的信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-211">Stores information about various processes within Lync Server 2013 that are involved in routing and connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-212"><a href="lync-server-2013-calltype-table.md">Lync Server 2013 中的 CallType 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-212"><a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-213">存储有关呼叫类型的信息，例如 "音频"、"即时消息"、"音频和视频" 和 "应用程序共享"。</span><span class="sxs-lookup"><span data-stu-id="c3cad-213">Stores information about types of the call, such as, “audio”, “Instant Messaging”, “audio and video” and “application sharing”.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-214"><a href="lync-server-2013-errorcategory-table.md">Lync Server 2013 中的 ErrorCategory 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-214"><a href="lync-server-2013-errorcategory-table.md">ErrorCategory table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-215">存储每个 Microsoft Lync Server 2013 诊断分类的友好名称。</span><span class="sxs-lookup"><span data-stu-id="c3cad-215">Stores the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-216"><a href="lync-server-2013-errordef-table.md">Lync Server 2013 中的 ErrorDef 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-216"><a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-217">存储有关错误类型及其定义的信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-217">Stores information about types of errors and their definitions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-218"><a href="lync-server-2013-errorreport-table.md">Lync Server 2013 中的 ErrorReport 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-218"><a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-219">存储已发生的错误的相关信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-219">Stores information about errors that have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-220"><a href="lync-server-2013-progressreport-table.md">Lync Server 2013 中的 ProgressReport 表</a></span><span class="sxs-lookup"><span data-stu-id="c3cad-220"><a href="lync-server-2013-progressreport-table.md">ProgressReport table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c3cad-221">存储有关 Lync Server 2013 进程中涉及的各种步骤的进度报告的信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-221">Stores information about the progress reports of various steps involved in Lync Server 2013 processes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c3cad-222">以下列表中的表由 Lync Server 内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-222">The tables in the following list are used internally by Lync Server.</span></span> <span data-ttu-id="c3cad-223">本文档中未介绍其详细信息。</span><span class="sxs-lookup"><span data-stu-id="c3cad-223">Their details are not described in this document.</span></span>

</div>

<div>

## <a name="tables-for-internal-use-by-lync-server"></a><span data-ttu-id="c3cad-224">Lync Server 供内部使用的表</span><span class="sxs-lookup"><span data-stu-id="c3cad-224">Tables for Internal Use by Lync Server</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3cad-225">表格</span><span class="sxs-lookup"><span data-stu-id="c3cad-225">Table</span></span></th>
<th><span data-ttu-id="c3cad-226">说明</span><span class="sxs-lookup"><span data-stu-id="c3cad-226">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-227"><strong>DbConfigDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-227"><strong>DbConfigDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-228">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-228">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-229"><strong>DbConfigInt</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-229"><strong>DbConfigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-230">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-230">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-231"><strong>DbErrorMessage</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-231"><strong>DbErrorMessage</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-232">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-232">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-233"><strong>前端表</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-233"><strong>FrontEnd Table</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-234">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-234">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-235"><strong>MSMQProcessing 表</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-235"><strong>MSMQProcessing Table</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-236">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-236">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-237"><strong>SummaryTableConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-237"><strong>SummaryTableConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-238">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-238">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-239"><strong>Syndicators 表</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-239"><strong>Syndicators Table</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-240">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-240">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-241"><strong>SyndicatorsTenantMap 表</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-241"><strong>SyndicatorsTenantMap Table</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-242">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-242">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-243"><strong>任务表</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-243"><strong>Task Table</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-244">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-244">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-245"><strong>UserStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-245"><strong>UserStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-246">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-246">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-247"><strong>UsageSummary_UQ</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-247"><strong>UsageSummary_UQ</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-248">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-248">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-249"><strong>UsageSummary</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-249"><strong>UsageSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-250">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-250">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-251"><strong>DaylightSavingYears</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-251"><strong>DaylightSavingYears</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-252">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-252">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-253"><strong>TimeZoneConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-253"><strong>TimeZoneConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-254">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-254">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-255"><strong>时区</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-255"><strong>TimeZones</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-256">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-256">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-257"><strong>FailureSummary_UQ</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-257"><strong>FailureSummary_UQ</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-258">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-258">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-259"><strong>FailureSummary</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-259"><strong>FailureSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-260">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-260">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cad-261"><strong>ServerSummary</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-261"><strong>ServerSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-262">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-262">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cad-263"><strong>MsDiagMetaData</strong></span><span class="sxs-lookup"><span data-stu-id="c3cad-263"><strong>MsDiagMetaData</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cad-264">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c3cad-264">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c3cad-265">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3cad-265">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

