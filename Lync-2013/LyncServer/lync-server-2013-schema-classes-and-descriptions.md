---
title: Lync Server 2013：架构类和说明
description: Lync Server 2013：架构类和说明。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema classes and descriptions
ms:assetid: 7d43b920-ac37-40cc-adfe-be289bda6e9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398625(v=OCS.15)
ms:contentKeyID: 48184612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec27c2e00a7f969dbc13c91b06313c8045894a9e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441968"
---
# <a name="schema-classes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="b5b07-103">Lync Server 2013 中的架构类和说明</span><span class="sxs-lookup"><span data-stu-id="b5b07-103">Schema classes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b5b07-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b5b07-104">

<span> </span></span></span>

<span data-ttu-id="b5b07-105">_**主题上次修改时间：** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="b5b07-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="b5b07-106">本部分介绍 Lync Server 2013 使用的所有架构类。</span><span class="sxs-lookup"><span data-stu-id="b5b07-106">This section describes all the schema classes used by Lync Server 2013.</span></span>

<div>

## <a name="schema-classes-and-descriptions"></a><span data-ttu-id="b5b07-107">架构类和说明</span><span class="sxs-lookup"><span data-stu-id="b5b07-107">Schema Classes and Descriptions</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5b07-108">种类</span><span class="sxs-lookup"><span data-stu-id="b5b07-108">Class</span></span></th>
<th><span data-ttu-id="b5b07-109">说明</span><span class="sxs-lookup"><span data-stu-id="b5b07-109">Description</span></span></th>
<th><span data-ttu-id="b5b07-110">备注</span><span class="sxs-lookup"><span data-stu-id="b5b07-110">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-111">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="b5b07-111">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="b5b07-112">Exchange 统一消息 (UM) 电子邮件收件人。</span><span class="sxs-lookup"><span data-stu-id="b5b07-112">Exchange Unified Messaging (UM) email recipient.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-113">此辅助类与 Exchange UM 共享。</span><span class="sxs-lookup"><span data-stu-id="b5b07-113">This auxiliary class is shared with Exchange UM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-114">msRTCSIP-ApplicationContacts</span><span class="sxs-lookup"><span data-stu-id="b5b07-114">msRTCSIP-ApplicationContacts</span></span></p></td>
<td><p><span data-ttu-id="b5b07-115">此类是多个应用程序联系人的容器，并且不包含任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-115">This class is a container for multiple application contacts and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-116">Microsoft Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-116">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-117">msRTCSIP-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="b5b07-117">msRTCSIP-ApplicationServer</span></span></p></td>
<td><p><span data-ttu-id="b5b07-118">此类包含统一通信应用程序服务实例的服务控制点的条目 (UCAS) 。</span><span class="sxs-lookup"><span data-stu-id="b5b07-118">This class holds the entry for the service control point for an instance of Unified Communications Application Services (UCAS).</span></span></p></td>
<td><p><span data-ttu-id="b5b07-119">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-119">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-120">msRTCSIP-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="b5b07-120">msRTCSIP-ApplicationServerService</span></span></p></td>
<td><p><span data-ttu-id="b5b07-121">此类提供从特定池到其应用程序服务的关联。</span><span class="sxs-lookup"><span data-stu-id="b5b07-121">This class provides an association from a specific pool to its Application service.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-122">通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-122">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-123">msRTCSIP-ApplicationServerSettings</span><span class="sxs-lookup"><span data-stu-id="b5b07-123">msRTCSIP-ApplicationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="b5b07-124">此辅助类到 msRTCSIP-ApplicationServer 保留表示应用程序服务实例的设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-124">This auxiliary class to msRTCSIP-ApplicationServer holds attributes representing settings for instances of the Application service.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-125">通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-125">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-126">msRTCSIP-存档 (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-126">msRTCSIP-Archive (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-127">此辅助类到 msRTCSIP-GlobalContainer 保存与存档相关的所有设置。</span><span class="sxs-lookup"><span data-stu-id="b5b07-127">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to archiving.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-128">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-128">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-129">msRTCSIP-ArchivingServer (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-129">msRTCSIP-ArchivingServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-130">此类表示单个即时消息存档服务器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-130">This class represents a single instant messaging Archiving Server.</span></span> <span data-ttu-id="b5b07-131">在将计算机激活为即时消息存档服务器（如安装了即时消息存档服务的计算机）时，将创建此类的实例。</span><span class="sxs-lookup"><span data-stu-id="b5b07-131">An instance of this class is created when a computer is activated as an instant messaging Archiving Server, such as a computer with the Instant Messaging Archiving service installed.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-132">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-132">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-133">msRTCSIP-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="b5b07-133">msRTCSIP-ConferenceDirectories</span></span></p></td>
<td><p><span data-ttu-id="b5b07-134">此类是多个会议目录实例的容器，并且不包含任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-134">This class is a container for multiple instances of conference directories and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-135">通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-135">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-136">msRTCSIP-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="b5b07-136">msRTCSIP-ConferenceDirectory</span></span></p></td>
<td><p><span data-ttu-id="b5b07-137">此类包含表示特定会议目录的设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-137">This class holds attributes representing settings for a specific conference directory.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-138">通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-138">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-139">msRTCSIP-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="b5b07-139">msRTCSIP-ConnectionPoint</span></span></p></td>
<td><p><span data-ttu-id="b5b07-140"> (SCP) 的一般服务控制点将计算机指定为运行 Lync Server 的服务器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-140">Generic service control point (SCP) to specify the computer as a server running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-141">Lync 2010 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-141">New in Lync 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-142">msRTCSIP-DefaultCWABank</span><span class="sxs-lookup"><span data-stu-id="b5b07-142">msRTCSIP-DefaultCWABank</span></span></p></td>
<td><p><span data-ttu-id="b5b07-143">此辅助类保留 Microsoft Lync Web App bank 的设置。</span><span class="sxs-lookup"><span data-stu-id="b5b07-143">This auxiliary class holds the settings for a Microsoft Lync Web App bank.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-144">通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-144">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-145">msRTCSIP-域</span><span class="sxs-lookup"><span data-stu-id="b5b07-145">msRTCSIP-Domain</span></span></p></td>
<td><p><span data-ttu-id="b5b07-146">此类包含用于定义 SIP 注册机构配置的域的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-146">This class holds attributes that define the configured domains of the SIP Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-147">msRTCSIP-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="b5b07-147">msRTCSIP-EdgeProxy</span></span></p></td>
<td><p><span data-ttu-id="b5b07-148">此类容器表示单个访问边缘服务。</span><span class="sxs-lookup"><span data-stu-id="b5b07-148">This class container represents a single Access Edge service.</span></span> <span data-ttu-id="b5b07-149">由于在外围网络中部署了 Access Edge 服务，并且客户通常不允许从外围网络访问 Active Directory 域服务，因此 Access Edge 服务的实例未联接到 intranet 的 Active Directory 网络。</span><span class="sxs-lookup"><span data-stu-id="b5b07-149">Because an Access Edge service is deployed in the perimeter network and customers usually do not allow Active Directory Domain Services access from the perimeter network, instances of Access Edge service are not joined to the intranet’s Active Directory network.</span></span> <span data-ttu-id="b5b07-150">因此，访问代理服务器不会自动在 AD DS 中注册。</span><span class="sxs-lookup"><span data-stu-id="b5b07-150">Therefore, Access Proxies are not automatically registered in AD DS.</span></span> <span data-ttu-id="b5b07-151">管理员必须手动配置 AD DS 中的每个 Access Edge 服务实例的存在。</span><span class="sxs-lookup"><span data-stu-id="b5b07-151">The administrator must manually configure the existence of each instance of Access Edge service in AD DS.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-152">msRTCSIP-EnterpriseMCUSettings</span><span class="sxs-lookup"><span data-stu-id="b5b07-152">msRTCSIP-EnterpriseMCUSettings</span></span></p></td>
<td><p><span data-ttu-id="b5b07-153">MsRTCSIP 的此辅助类保留表示会议服务器设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-153">This auxiliary class to msRTCSIP-MCU holds attributes representing settings for Conferencing servers.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-154">Microsoft Office 通信服务器2007中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="b5b07-154">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-155">msRTCSIP-EnterpriseMediationServerSettings</span><span class="sxs-lookup"><span data-stu-id="b5b07-155">msRTCSIP-EnterpriseMediationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="b5b07-156">此辅助类到 msRTCSIP-MediationServer 包含表示中介服务器设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-156">This auxiliary class to msRTCSIP-MediationServer holds attributes representing settings for Mediation Servers.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-157">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-157">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-158">msRTCSIP-EnterpriseServerSettings</span><span class="sxs-lookup"><span data-stu-id="b5b07-158">msRTCSIP-EnterpriseServerSettings</span></span></p></td>
<td><p><span data-ttu-id="b5b07-159">此辅助类到 msRTCSIP-服务器保留表示 SIP 服务器设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-159">This auxiliary class to msRTCSIP-Server holds attributes representing settings for SIP servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-160">msRTCSIP-联合</span><span class="sxs-lookup"><span data-stu-id="b5b07-160">msRTCSIP-Federation</span></span></p></td>
<td><p><span data-ttu-id="b5b07-161">此辅助类到 msRTCSIP-GlobalContainer 保存与联盟相关的所有设置。</span><span class="sxs-lookup"><span data-stu-id="b5b07-161">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to federation.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-162">msRTCSIP-GlobalContainer</span><span class="sxs-lookup"><span data-stu-id="b5b07-162">msRTCSIP-GlobalContainer</span></span></p></td>
<td><p><span data-ttu-id="b5b07-163">此类包含适用于整个 Lync Server 部署的所有设置。</span><span class="sxs-lookup"><span data-stu-id="b5b07-163">This class holds all settings that apply throughout a Lync Server deployment.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-164">msRTCSIP-GlobalUserPolicy (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-164">msRTCSIP-GlobalUserPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-165">此类表示单个 Office 通信服务器会议策略。</span><span class="sxs-lookup"><span data-stu-id="b5b07-165">This class represents a single Office Communications Server meeting policy.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-166">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-166">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-167">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="b5b07-167">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="b5b07-168">本地全局拓扑设置对象。</span><span class="sxs-lookup"><span data-stu-id="b5b07-168">The local global topology setting object.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-169">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="b5b07-169">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-170">msRTCSIP-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="b5b07-170">msRTCSIP-GlobalTopologySettings</span></span></p></td>
<td><p><span data-ttu-id="b5b07-171">用于保存全局拓扑设置对象的容器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-171">Container to hold global topology setting objects.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-172">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="b5b07-172">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-173">msRTCSIP-LocalNormalization</span><span class="sxs-lookup"><span data-stu-id="b5b07-173">msRTCSIP-LocalNormalization</span></span></p></td>
<td><p><span data-ttu-id="b5b07-174">此类是表示位置规范化规则的实例的容器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-174">This class is a container that represents an instance of a location normalization rule.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-175">msRTCSIP-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="b5b07-175">msRTCSIP-LocationContactMapping</span></span></p></td>
<td><p><span data-ttu-id="b5b07-176">此类由会议助理应用程序创建，并保留用于按地区对会议电话号码进行分类的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-176">This class is created by the Conferencing Attendant application and holds attributes used to categorize conference telephone numbers by region.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-177">通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-177">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-178">msRTCSIP-LocationContactMappings</span><span class="sxs-lookup"><span data-stu-id="b5b07-178">msRTCSIP-LocationContactMappings</span></span></p></td>
<td><p><span data-ttu-id="b5b07-179">此类是位置联系人映射的多个实例的容器，并且不包含任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-179">This class is a container for multiple instances of location contact mappings and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-180">通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-180">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-181">msRTCSIP-LocationProfile</span><span class="sxs-lookup"><span data-stu-id="b5b07-181">msRTCSIP-LocationProfile</span></span></p></td>
<td><p><span data-ttu-id="b5b07-182">此类是一个表示特定位置配置文件的容器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-182">This class is a container that represents a specific location profile.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-183">msRTCSIP-LocationProfiles (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-183">msRTCSIP-LocationProfiles (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-184">此类是多个位置配置文件的容器，并且不包含任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-184">This class is a container for multiple location profiles and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-185">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-185">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-186">msRTCSIP-LocalNormalizations (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-186">msRTCSIP-LocalNormalizations (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-187">此类是多个本地规范化规则的容器，并且不包含任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-187">This class is a container for multiple local normalization rules and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-188">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-188">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-189">msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="b5b07-189">msRTCSIP-MCU</span></span></p></td>
<td><p><span data-ttu-id="b5b07-190">此类表示单个会议服务器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-190">This class represents a single Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-191">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-191">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-192">msRTCSIP-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="b5b07-192">msRTCSIP-MCUFactories</span></span></p></td>
<td><p><span data-ttu-id="b5b07-193">此类保存多个 msRTCSIP MCUFactory 类，并且没有属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-193">This class holds multiple msRTCSIP-MCUFactory classes and does not have attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-194">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-194">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-195">msRTCSIP-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="b5b07-195">msRTCSIP-MCUFactory</span></span></p></td>
<td><p><span data-ttu-id="b5b07-196">此类是一个容器，表示适用于单个媒体类型的会议服务器工厂。</span><span class="sxs-lookup"><span data-stu-id="b5b07-196">This class is a container representing a Conferencing Server Factory for a single medium type.</span></span> <span data-ttu-id="b5b07-197">当激活此特定类型和供应商的第一个会议服务器时，将创建此类的实例。</span><span class="sxs-lookup"><span data-stu-id="b5b07-197">An instance of this class is created when the first Conferencing server for this particular type and vendor is activated.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-198">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-198">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-199">msRTCSIP-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="b5b07-199">msRTCSIP-MCUFactoryService</span></span></p></td>
<td><p><span data-ttu-id="b5b07-200">此类提供从特定池到其会议服务器工厂的关联。</span><span class="sxs-lookup"><span data-stu-id="b5b07-200">This class provides an association from a specific pool to its Conferencing Server Factory.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-201">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-201">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-202">msRTCSIP-MediationServer</span><span class="sxs-lookup"><span data-stu-id="b5b07-202">msRTCSIP-MediationServer</span></span></p></td>
<td><p><span data-ttu-id="b5b07-203">此类包含用于中介服务器的服务控制点的条目。</span><span class="sxs-lookup"><span data-stu-id="b5b07-203">This class holds the entry for the service control point for a Mediation Server.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-204">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-204">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-205">msRTCSIP-会议 (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-205">msRTCSIP-Meeting (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-206">此辅助类到 msRTCSIP-GlobalContainer 包含表示可配置的会议设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-206">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing configurable meeting settings.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-207">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-207">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-208">msRTCSIP-移动性</span><span class="sxs-lookup"><span data-stu-id="b5b07-208">msRTCSIP-Mobility</span></span></p></td>
<td><p><span data-ttu-id="b5b07-209">存储全局移动设置的容器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-209">Container that stores the global mobility settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-210">msRTCSIP-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="b5b07-210">msRTCSIP-MonitoringServer</span></span></p></td>
<td><p><span data-ttu-id="b5b07-211">此类包含表示单个监视服务器的设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-211">This class holds attributes that represent settings for a single Monitoring Server.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-212">通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-212">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-213">msRTCSIP-PhoneRoute (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-213">msRTCSIP-PhoneRoute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-214">此类是一个容器，表示指向网关或网关集的最低成本路线的实例。</span><span class="sxs-lookup"><span data-stu-id="b5b07-214">This class is a container representing an instance of a least cost route to a gateway or set of gateways.</span></span> <span data-ttu-id="b5b07-215">此信息由运行标准版的所有企业池或服务器使用，以最经济高效的方式将传出呼叫路由到公共交换电话网络 (PSTN) 。</span><span class="sxs-lookup"><span data-stu-id="b5b07-215">This information is used by all Enterprise pools or servers running Standard Edition to route outgoing calls to the public switched telephone network (PSTN) in the most cost effective way.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-216">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-216">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-217">msRTCSIP-PhoneRoutes (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-217">msRTCSIP-PhoneRoutes (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-218">此类是多个最少的成本路由的容器，并且不包含任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-218">This class is a container for multiple, least cost routes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-219">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-219">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-220">msRTCSIP-策略 (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-220">msRTCSIP-Policies (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-221">此类包含多个 Lync 服务器策略类，并且没有任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-221">This class holds multiple Lync Server policy classes and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-222">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-222">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-223">msRTCSIP-Pool</span><span class="sxs-lookup"><span data-stu-id="b5b07-223">msRTCSIP-Pool</span></span></p></td>
<td><p><span data-ttu-id="b5b07-224">此类表示单个 Lync 服务器池。</span><span class="sxs-lookup"><span data-stu-id="b5b07-224">This class represents a single Lync Server pool.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-225">msRTCSIP-池</span><span class="sxs-lookup"><span data-stu-id="b5b07-225">msRTCSIP-Pools</span></span></p></td>
<td><p><span data-ttu-id="b5b07-226">此类包含多个 Lync 服务器池，并且没有任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-226">This class holds multiple Lync Server pools and does not have any attributes itself.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-227">msRTCSIP-PoolService</span><span class="sxs-lookup"><span data-stu-id="b5b07-227">msRTCSIP-PoolService</span></span></p></td>
<td><p><span data-ttu-id="b5b07-228">此类表示池的服务控制 pointservice 控制点。</span><span class="sxs-lookup"><span data-stu-id="b5b07-228">This class represents the service control pointservice control point of a pool.</span></span> <span data-ttu-id="b5b07-229">托管在池中的用户将其 msRTCSIP-PrimaryHomeServer 属性指向此类的实例。</span><span class="sxs-lookup"><span data-stu-id="b5b07-229">Users hosted on a pool have their msRTCSIP-PrimaryHomeServer attribute point to an instance of this class.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-230">msRTCSIP-状态</span><span class="sxs-lookup"><span data-stu-id="b5b07-230">msRTCSIP-Presence</span></span></p></td>
<td><p><span data-ttu-id="b5b07-231">存储全局状态设置的容器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-231">Container that stores the global presence settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-232">msRTCSIP-注册机构</span><span class="sxs-lookup"><span data-stu-id="b5b07-232">msRTCSIP-Registrar</span></span></p></td>
<td><p><span data-ttu-id="b5b07-233">此辅助类到 msRTCSIP-GlobalContainer 包含表示 SIP 注册机构维护的用户设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-233">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing user settings maintained by the SIP Registrar servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-234">msRTCSIP-RouteUsage (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-234">msRTCSIP-RouteUsage (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-235">此类是一个容器，表示手机路线使用情况的实例。</span><span class="sxs-lookup"><span data-stu-id="b5b07-235">This class is a container representing an instance of a phone route usage.</span></span> <span data-ttu-id="b5b07-236">电话路由使用类包含一个属性字段和一个说明字段。</span><span class="sxs-lookup"><span data-stu-id="b5b07-236">A phone route usage class consists of an attribute field and a description field.</span></span> <span data-ttu-id="b5b07-237">属性字段定义使用类型。</span><span class="sxs-lookup"><span data-stu-id="b5b07-237">The attribute field defines a usage type.</span></span> <span data-ttu-id="b5b07-238">"说明" 域允许管理员在手机路线中描述此属性的用法。</span><span class="sxs-lookup"><span data-stu-id="b5b07-238">The description field allows administrators to describe the usage for this attribute in the phone route.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-239">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-239">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-240">msRTCSIP-RouteUsages (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-240">msRTCSIP-RouteUsages (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-241">此类保留 msRTCSIP 类的多个实例，并且没有任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-241">This class holds multiple instances of the msRTCSIP-RouteUsage class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-242">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-243">msRTCSIP-搜索</span><span class="sxs-lookup"><span data-stu-id="b5b07-243">msRTCSIP-Search</span></span></p></td>
<td><p><span data-ttu-id="b5b07-244">此辅助类到 msRTCSIP-GlobalContainer 包含限制和控制搜索结果范围的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-244">This auxiliary class to msRTCSIP-GlobalContainer holds attributes that limit and control the scope of search results.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-245">msRTCSIP-服务器</span><span class="sxs-lookup"><span data-stu-id="b5b07-245">msRTCSIP-Server</span></span></p></td>
<td><p><span data-ttu-id="b5b07-246">此类表示运行 Lync Server 的单个服务器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-246">This class represents a single server running Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-247">msRTCSIP-服务</span><span class="sxs-lookup"><span data-stu-id="b5b07-247">msRTCSIP-Service</span></span></p></td>
<td><p><span data-ttu-id="b5b07-248">此类包含全局设置容器和 msRTCSIP 域对象。</span><span class="sxs-lookup"><span data-stu-id="b5b07-248">This class holds the global settings container and msRTCSIP-Domain objects.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-249">msRTCSIP-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="b5b07-249">msRTCSIP-TrustedMCU</span></span></p></td>
<td><p><span data-ttu-id="b5b07-250">此类包含表示受信任的会议服务器的设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-250">This class holds attributes that represent settings for a trusted Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-251">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-251">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-252">msRTCSIP-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="b5b07-252">msRTCSIP-TrustedMCUs</span></span></p></td>
<td><p><span data-ttu-id="b5b07-253">此类保留 msRTCSIP 类的多个实例，并且没有任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-253">This class holds multiple instances of the msRTCSIP-TrustedMCU class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-254">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-254">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-255">msRTCSIP-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="b5b07-255">msRTCSIP-TrustedProxies</span></span></p></td>
<td><p><span data-ttu-id="b5b07-256">此类包含多个 msRTCSIP TrustedProxy 类，并且不包含任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-256">This class holds multiple msRTCSIP-TrustedProxy classes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-257">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-257">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-258">msRTCSIP-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="b5b07-258">msRTCSIP-TrustedProxy</span></span></p></td>
<td><p><span data-ttu-id="b5b07-259">此类是一个容器，表示运行代理服务器的服务器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-259">This class is a container representing a server running Proxy Server.</span></span> <span data-ttu-id="b5b07-260">在加入到 AD DS 的计算机上激活新的代理服务器时，将创建此类的实例。</span><span class="sxs-lookup"><span data-stu-id="b5b07-260">An instance of this class is created when activating a new Proxy Server on a computer joined to AD DS.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-261">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-261">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-262">msRTCSIP-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="b5b07-262">msRTCSIP-TrustedServer</span></span></p></td>
<td><p><span data-ttu-id="b5b07-263">此类包含表示受信任服务器的设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-263">This class holds attributes that represent settings for a trusted server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-264">msRTCSIP-TrustedService</span><span class="sxs-lookup"><span data-stu-id="b5b07-264">msRTCSIP-TrustedService</span></span></p></td>
<td><p><span data-ttu-id="b5b07-265">此类是一个容器，表示受信任的服务，可使用全局可路由的用户代理 URI (GRUU) 地址进行路由。</span><span class="sxs-lookup"><span data-stu-id="b5b07-265">This class is a container representing a trusted service that is routable using a Globally Routable User Agent URI (GRUU) address.</span></span> <span data-ttu-id="b5b07-266">当激活由 Lync Server 信任的新服务器时，将创建此类的实例。</span><span class="sxs-lookup"><span data-stu-id="b5b07-266">An instance of this class is created when a new server that is trusted by Lync Server is activated.</span></span> <span data-ttu-id="b5b07-267">此受信任服务器必须加入 Active Directory 域。</span><span class="sxs-lookup"><span data-stu-id="b5b07-267">This trusted server must be joined to an Active Directory domain.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-268">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-268">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-269">msRTCSIP-TrustedServices</span><span class="sxs-lookup"><span data-stu-id="b5b07-269">msRTCSIP-TrustedServices</span></span></p></td>
<td><p><span data-ttu-id="b5b07-270">此类是多个 GRUU 服务器的容器，并且不包含任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-270">This class is a container for multiple GRUU servers and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-271">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-271">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-272">msRTCSIP-TrustedWebComponentsServer</span><span class="sxs-lookup"><span data-stu-id="b5b07-272">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
<td><p><span data-ttu-id="b5b07-273">此类包含表示受信任 web 组件的设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-273">This class holds attributes that represent the settings for a trusted web component.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-274">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-274">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-275">msRTCSIP-TrustedWebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="b5b07-275">msRTCSIP-TrustedWebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="b5b07-276">此类保留 msRTCSIP 类的多个实例，并且没有任何属性本身。</span><span class="sxs-lookup"><span data-stu-id="b5b07-276">This class holds multiple instances of the msRTCSIP-TrustedWebComponentServer class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-277">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-277">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-278">msRTCSIP-UnifiedCommunications (过时) </span><span class="sxs-lookup"><span data-stu-id="b5b07-278">msRTCSIP-UnifiedCommunications (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="b5b07-279">此辅助类到 msRTCSIP-GlobalContainer 保存与统一通信相关的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-279">This auxiliary class to msRTCSIP-GlobalContainer holds attributes related to unified communications.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-280">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b5b07-280">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-281">msRTCSIP-WebComponents</span><span class="sxs-lookup"><span data-stu-id="b5b07-281">msRTCSIP-WebComponents</span></span></p></td>
<td><p><span data-ttu-id="b5b07-282">此类包含 (IIS) 的 Internet 信息服务器的服务控制 pointservice 控制点。</span><span class="sxs-lookup"><span data-stu-id="b5b07-282">This class holds the service control pointservice control point for Internet Information Server (IIS).</span></span> <span data-ttu-id="b5b07-283">它将服务器标识为 web 组件服务器。</span><span class="sxs-lookup"><span data-stu-id="b5b07-283">It identifies a server as a web components server.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-284">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-284">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5b07-285">msRTCSIP-WebComponentsService</span><span class="sxs-lookup"><span data-stu-id="b5b07-285">msRTCSIP-WebComponentsService</span></span></p></td>
<td><p><span data-ttu-id="b5b07-286">此类提供从特定池到该池将使用的 web 组件的关联。</span><span class="sxs-lookup"><span data-stu-id="b5b07-286">This class provides an association from a specific pool to the web components that the pool will use.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-287">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-287">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5b07-288">msRTCSIP-WebComponentSettings</span><span class="sxs-lookup"><span data-stu-id="b5b07-288">msRTCSIP-WebComponentSettings</span></span></p></td>
<td><p><span data-ttu-id="b5b07-289">此辅助类到 msRTCSIP-WebComponents 包含表示 web 组件的设置的属性。</span><span class="sxs-lookup"><span data-stu-id="b5b07-289">This auxiliary class to msRTCSIP-WebComponents holds attributes representing settings for web components.</span></span></p></td>
<td><p><span data-ttu-id="b5b07-290">通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="b5b07-290">New in Communications Server 2007.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b5b07-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b5b07-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

