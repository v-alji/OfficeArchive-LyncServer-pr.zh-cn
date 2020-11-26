---
title: Lync Server 2013：架构属性和说明
description: Lync Server 2013：架构属性和说明。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes and descriptions
ms:assetid: b009df76-9c22-471d-b57a-bda009a98261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412841(v=OCS.15)
ms:contentKeyID: 48185083
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18888d20a772b3e84970e7d874bd6b6964affc75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444957"
---
# <a name="schema-attributes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="83990-103">Lync Server 2013 中的架构属性和说明</span><span class="sxs-lookup"><span data-stu-id="83990-103">Schema attributes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83990-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83990-104">

<span> </span></span></span>

<span data-ttu-id="83990-105">_**主题上次修改时间：** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="83990-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="83990-106">本部分介绍 Lync Server 2013 使用的所有架构属性。</span><span class="sxs-lookup"><span data-stu-id="83990-106">This section describes all the schema attributes used by Lync Server 2013.</span></span> <span data-ttu-id="83990-107">对于与属性相关联的类，请参阅 [Lync Server 2013 中的 "按类架构属性](lync-server-2013-schema-attributes-by-class.md)"。</span><span class="sxs-lookup"><span data-stu-id="83990-107">For the classes associated with attributes, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span> <span data-ttu-id="83990-108">有关 Lync Server 2013 中新增的类和属性的列表，请参阅 [Lync server 2013 中的架构更改](lync-server-2013-schema-changes-in-lync-server-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="83990-108">For a list of classes and attributes that are new in Lync Server 2013, see [Schema changes in Lync Server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span></span>

<span data-ttu-id="83990-109">链接对的属性指定为 "前进链接" 或 "反向链接"。</span><span class="sxs-lookup"><span data-stu-id="83990-109">Attributes that are linked pairs are specified as forward links or back links.</span></span> <span data-ttu-id="83990-110">引用另一个对象的属性是前向链接;引用第一个对象的其他对象的属性是 "后退" 链接。</span><span class="sxs-lookup"><span data-stu-id="83990-110">An attribute that refers to another object is a forward link; the attribute of the other object that refers back to the first object is a back link.</span></span> <span data-ttu-id="83990-111">正向链接是可更新的，而反向链接是只读的。</span><span class="sxs-lookup"><span data-stu-id="83990-111">Forward links are updatable, while back links are read-only.</span></span>

<span data-ttu-id="83990-112">某些属性具有位掩码值。</span><span class="sxs-lookup"><span data-stu-id="83990-112">Some attributes have a bit-mask value.</span></span> <span data-ttu-id="83990-113">对于这些属性，每个设置都由一个位表示，显示的十进制值表示位位置。</span><span class="sxs-lookup"><span data-stu-id="83990-113">For these attributes, each setting is represented by a bit, and the displayed decimal value represents the bit position.</span></span> <span data-ttu-id="83990-114">位位置从位0开始。</span><span class="sxs-lookup"><span data-stu-id="83990-114">Bit positions start with bit 0.</span></span> <span data-ttu-id="83990-115">例如，1 (binary) 位0设置，10000 (二进制) 是位4设置。</span><span class="sxs-lookup"><span data-stu-id="83990-115">For example, 1 (binary) is bit 0 set and 10000 (binary) is bit 4 set.</span></span> <span data-ttu-id="83990-116">每个位表示一个属性。</span><span class="sxs-lookup"><span data-stu-id="83990-116">Each bit represents a property.</span></span> <span data-ttu-id="83990-117">下面是一些示例：</span><span class="sxs-lookup"><span data-stu-id="83990-117">The following are some examples:</span></span>

  - <span data-ttu-id="83990-118">10000 (二进制) 的十进制值为 16 (也就是说，第4位设置) 。</span><span class="sxs-lookup"><span data-stu-id="83990-118">10000 (binary) has a decimal value of 16 (that is, bit 4 is set).</span></span>

  - <span data-ttu-id="83990-119">100000000 (二进制) 的十进制值为 256 (也就是说，第8位设置) 。</span><span class="sxs-lookup"><span data-stu-id="83990-119">100000000 (binary) has a decimal value of 256 (that is, bit 8 is set).</span></span>

  - <span data-ttu-id="83990-120">1100 (二进制) 的十进制值为 12 (，即位2和3的设置;将启用) 两位均表示的属性。</span><span class="sxs-lookup"><span data-stu-id="83990-120">1100 (binary) has a decimal value of 12 (that is, bits 2 and 3 are set; properties represented by both bits are enabled).</span></span>

  - <span data-ttu-id="83990-121">1111000001 (二进制) 的十进制值为 961 (，即位0、6、7、8和9的设置;) 的每个位的属性均已启用。</span><span class="sxs-lookup"><span data-stu-id="83990-121">1111000001 (binary) has a decimal value of 961 (that is, bits 0, 6, 7, 8, and 9 are set; properties for each of these bits are enabled).</span></span>

<div id="sectionSection0" class="section">

### <a name="schema-attributes-for-lync-server-2013"></a><span data-ttu-id="83990-122">Lync Server 2013 的架构属性</span><span class="sxs-lookup"><span data-stu-id="83990-122">Schema Attributes for Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="83990-123">属性</span><span class="sxs-lookup"><span data-stu-id="83990-123">Attribute</span></span></th>
<th><span data-ttu-id="83990-124">描述</span><span class="sxs-lookup"><span data-stu-id="83990-124">Description</span></span></th>
<th><span data-ttu-id="83990-125">备注</span><span class="sxs-lookup"><span data-stu-id="83990-125">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83990-126">dnsHostName</span><span class="sxs-lookup"><span data-stu-id="83990-126">dnsHostName</span></span></p></td>
<td><p><span data-ttu-id="83990-127">Active Directory 域服务中现与 <strong>msRTCSIP</strong> 和 <strong>msRTCSIP</strong> 类相关联的现有属性。</span><span class="sxs-lookup"><span data-stu-id="83990-127">An existing attribute in Active Directory Domain Services that is now associated with the <strong>msRTCSIP-Pool</strong> and <strong>msRTCSIP-MonitoringServer</strong> classes.</span></span> <span data-ttu-id="83990-128">此属性指定池或监视服务器 (FQDN) 的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="83990-128">This attribute specifies the fully qualified domain name (FQDN) of a pool or Monitoring Server.</span></span></p>
<p><span data-ttu-id="83990-129">每个段的有效值为63个字符;整个 FQDN 的有效值为255个字符。</span><span class="sxs-lookup"><span data-stu-id="83990-129">A valid value for each segment is 63 characters; a valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="83990-130">Microsoft Office Live 通信服务器2005中的新增新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-130">New in Microsoft Office Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-131">SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="83990-131">msDS-SourceObjectDN</span></span></p></td>
<td><p><span data-ttu-id="83990-132">此属性包含与该对象对应的其他林中的对象的可分辨名称 (DN) 的字符串表示形式。</span><span class="sxs-lookup"><span data-stu-id="83990-132">This attribute contains the string representation of the distinguished name (DN) of the object in another forest that corresponds to this object.</span></span> <span data-ttu-id="83990-133">此属性用于通讯组扩展和自动出席。</span><span class="sxs-lookup"><span data-stu-id="83990-133">This attribute is used for distribution group expansion and auto attendance.</span></span> <span data-ttu-id="83990-134">此属性在 Windows Server 2003 R2 的默认 Active Directory 架构中定义。</span><span class="sxs-lookup"><span data-stu-id="83990-134">This attribute is defined in the default Active Directory schema for Windows Server 2003 R2.</span></span></p>
<p><span data-ttu-id="83990-135">为避免需要将 AD DS 升级到 Windows Server 2003 R2，Active Directory 架构准备使用此属性定义扩展了 Windows Server 2003 架构。</span><span class="sxs-lookup"><span data-stu-id="83990-135">To avoid requiring an upgrade of AD DS to Windows Server 2003 R2, Active Directory schema preparation extends the Windows Server 2003 schema with this attribute definition.</span></span></p></td>
<td><p><span data-ttu-id="83990-136">Microsoft Office 通信服务器2007中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-136">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-137">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="83990-137">msExchUCVoiceMailSettings</span></span></p></td>
<td><p><span data-ttu-id="83990-138">此多值属性包含语音邮件设置。</span><span class="sxs-lookup"><span data-stu-id="83990-138">This multi-valued attribute holds voice mail settings.</span></span> <span data-ttu-id="83990-139">此属性是通过 Exchange 统一消息 (UM) 共享的。</span><span class="sxs-lookup"><span data-stu-id="83990-139">This attribute is shared with Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="83990-140">Microsoft Lync Server 2010 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-140">New in Microsoft Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-141">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="83990-141">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="83990-142">此多值属性包含适用于用户的保留策略的标识符。</span><span class="sxs-lookup"><span data-stu-id="83990-142">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="83990-143">保留策略在保留期间保留用户的邮箱项目。</span><span class="sxs-lookup"><span data-stu-id="83990-143">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="83990-144">此属性是与 Exchange 2013 共享的。</span><span class="sxs-lookup"><span data-stu-id="83990-144">This attribute is shared with Exchange 2013.</span></span></p></td>
<td><p><span data-ttu-id="83990-145">Lync Server 2013 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-145">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-146">msRTCSIP-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="83990-146">msRTCSIP-AcpInfo</span></span></p></td>
<td><p><span data-ttu-id="83990-147">此属性存储用户的音频会议提供商信息。</span><span class="sxs-lookup"><span data-stu-id="83990-147">This attribute stores audio conferencing provider information for a user.</span></span></p></td>
<td><p><span data-ttu-id="83990-148">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-148">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-149">msRTCSIP-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="83990-149">msRTCSIP-ApplicationDestination</span></span></p></td>
<td><p><span data-ttu-id="83990-150">此属性指向应用程序联系人的受信任服务条目。</span><span class="sxs-lookup"><span data-stu-id="83990-150">This attribute points to the trusted service entry for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="83990-151">Microsoft Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-151">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-152">msRTCSIP-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="83990-152">msRTCSIP-ApplicationList</span></span></p></td>
<td><p><span data-ttu-id="83990-153">此属性包含应用服务器上托管应用程序的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-153">This attribute contains a list of hosted applications on the application server.</span></span></p></td>
<td><p><span data-ttu-id="83990-154">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-154">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-155">msRTCSIP-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="83990-155">msRTCSIP-ApplicationOptions</span></span></p></td>
<td><p><span data-ttu-id="83990-156">此属性指定应用程序联系人的选项。</span><span class="sxs-lookup"><span data-stu-id="83990-156">This attribute specifies the options for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="83990-157">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-157">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-158">msRTCSIP-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="83990-158">msRTCSIP-ApplicationPrimaryLanguage</span></span></p></td>
<td><p><span data-ttu-id="83990-159">此属性包含应用程序联系人的主要语言。</span><span class="sxs-lookup"><span data-stu-id="83990-159">This attribute contains the primary language for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="83990-160">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-160">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-161">msRTCSIP-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="83990-161">msRTCSIP-ApplicationSecondaryLanguages</span></span></p></td>
<td><p><span data-ttu-id="83990-162">此多值属性包含应用程序联系人的辅助语言。</span><span class="sxs-lookup"><span data-stu-id="83990-162">This multiple value attribute contains the secondary languages for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="83990-163">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-163">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-164">msRTCSIP-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="83990-164">msRTCSIP-ApplicationServerBL</span></span></p></td>
<td><p><span data-ttu-id="83990-165">此属性包含属于此池的应用程序服务器的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-165">This attribute contains a list of application servers that belong to this pool.</span></span> <span data-ttu-id="83990-166">指向此 back link 属性的相应正向链接是 <strong>msRTCSIP-ApplicationServerPoolLink</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-166">The corresponding forward link to this back link attribute is <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-167">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-167">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-168">msRTCSIP-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="83990-168">msRTCSIP-ApplicationServerPoolLink</span></span></p></td>
<td><p><span data-ttu-id="83990-169">此属性指向应用服务器所属的池。</span><span class="sxs-lookup"><span data-stu-id="83990-169">This attribute points to the pool to which this application server belongs.</span></span> <span data-ttu-id="83990-170">这是 "转发" 链接。</span><span class="sxs-lookup"><span data-stu-id="83990-170">This is the forward link.</span></span> <span data-ttu-id="83990-171">相应的反向链接为 <strong>msRTCSIP-ApplicationServerBL</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-171">The corresponding backward link is <strong>msRTCSIP-ApplicationServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-172">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-172">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-173">msRTCSIP-ArchiveDefault (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-173">msRTCSIP-ArchiveDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-174">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-174">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-175">Office 通信服务器2007中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-175">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-176">msRTCSIP-ArchiveDefaultFlags (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-176">msRTCSIP-ArchiveDefaultFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-177">此属性指定林边界内用于存档所有用户通信的全局默认值。</span><span class="sxs-lookup"><span data-stu-id="83990-177">This attribute specifies the global default within the forest boundary for archiving all user communications.</span></span> <span data-ttu-id="83990-178">这由存档代理层强制执行。</span><span class="sxs-lookup"><span data-stu-id="83990-178">This is enforced by the archiving agent layer.</span></span> <span data-ttu-id="83990-179">此属性的值范围如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-179">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-180"><strong>TRUE</strong>：对所有用户进行存档</span><span class="sxs-lookup"><span data-stu-id="83990-180"><strong>TRUE</strong>: Archive all users</span></span></p></li>
<li><p><span data-ttu-id="83990-181"><strong>FALSE</strong>：不存档所有用户</span><span class="sxs-lookup"><span data-stu-id="83990-181"><strong>FALSE</strong>: Do not archive all users</span></span></p></li>
</ul>
<p><span data-ttu-id="83990-182">此属性在林边界内对内部网络内的用户通信的存档方式进行全局控制。</span><span class="sxs-lookup"><span data-stu-id="83990-182">This attribute globally controls, within the forest boundary, how user communications within an internal network are archived.</span></span></p>
<p><span data-ttu-id="83990-183"><strong>实时通信服务器2005行为 (现已停用) </strong></span><span class="sxs-lookup"><span data-stu-id="83990-183"><strong>Live Communications Server 2005 behavior (now retired)</strong></span></span></p>
<p><span data-ttu-id="83990-184">此属性的值范围如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-184">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-185">0：将邮件正文存档 [位 0]</span><span class="sxs-lookup"><span data-stu-id="83990-185">0: Archive the message body [bit 0]</span></span></p></li>
<li><p><span data-ttu-id="83990-186">1：不存档邮件正文 [位 0]</span><span class="sxs-lookup"><span data-stu-id="83990-186">1: Do not archive the message body [bit 0]</span></span></p></li>
</ul>
<p><span data-ttu-id="83990-187"><strong>Office 通信服务器2007行为</strong></span><span class="sxs-lookup"><span data-stu-id="83990-187"><strong>Office Communications Server 2007 behavior</strong></span></span></p>
<p><span data-ttu-id="83990-188">此属性的值范围如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-188">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-189">0： ArchiveFederationDefaultWithoutBody (已停用) </span><span class="sxs-lookup"><span data-stu-id="83990-189">0: ArchiveFederationDefaultWithoutBody (retired)</span></span></p></li>
<li><p><span data-ttu-id="83990-190">1-2： ArchiveInternalCommunications</span><span class="sxs-lookup"><span data-stu-id="83990-190">1-2: ArchiveInternalCommunications</span></span></p></li>
<li><p><span data-ttu-id="83990-191">3-4： ArchiveFederatedCommunications</span><span class="sxs-lookup"><span data-stu-id="83990-191">3-4: ArchiveFederatedCommunications</span></span></p></li>
<li><p><span data-ttu-id="83990-192">5： RecordPresenceRegistrations</span><span class="sxs-lookup"><span data-stu-id="83990-192">5: RecordPresenceRegistrations</span></span></p></li>
<li><p><span data-ttu-id="83990-193">6： RecordIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="83990-193">6: RecordIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="83990-194">7： RecordGroupIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="83990-194">7: RecordGroupIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="83990-195">8： RecordFileTransferInstances</span><span class="sxs-lookup"><span data-stu-id="83990-195">8: RecordFileTransferInstances</span></span></p></li>
<li><p><span data-ttu-id="83990-196">9： RecordAudioCallDetails</span><span class="sxs-lookup"><span data-stu-id="83990-196">9: RecordAudioCallDetails</span></span></p></li>
<li><p><span data-ttu-id="83990-197">10： RecordVideoCallDetails</span><span class="sxs-lookup"><span data-stu-id="83990-197">10: RecordVideoCallDetails</span></span></p></li>
<li><p><span data-ttu-id="83990-198">11： RecordRemoteAssistanceCallDetails</span><span class="sxs-lookup"><span data-stu-id="83990-198">11: RecordRemoteAssistanceCallDetails</span></span></p></li>
<li><p><span data-ttu-id="83990-199">12： RecordApplicationSharingDetails</span><span class="sxs-lookup"><span data-stu-id="83990-199">12: RecordApplicationSharingDetails</span></span></p></li>
<li><p><span data-ttu-id="83990-200">13： RecordMeetingInstantiations</span><span class="sxs-lookup"><span data-stu-id="83990-200">13: RecordMeetingInstantiations</span></span></p></li>
<li><p><span data-ttu-id="83990-201">14： RecordMeetingJoins</span><span class="sxs-lookup"><span data-stu-id="83990-201">14: RecordMeetingJoins</span></span></p></li>
<li><p><span data-ttu-id="83990-202">15： RecordDataJoins</span><span class="sxs-lookup"><span data-stu-id="83990-202">15: RecordDataJoins</span></span></p></li>
<li><p><span data-ttu-id="83990-203">16： RecordAVJoins</span><span class="sxs-lookup"><span data-stu-id="83990-203">16: RecordAVJoins</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-204">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-204">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-205">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-205">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-206">msRTCSIP-ArchiveFederationDefault (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-206">msRTCSIP-ArchiveFederationDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-207">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-207">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-208">Office 通信服务器2007中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-208">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-209">msRTCSIP-ArchiveFederationDefaultFlags (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-209">msRTCSIP-ArchiveFederationDefaultFlags (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-210">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-210">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-211">Office 通信服务器2007中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-211">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-212">msRTCSIP-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="83990-212">msRTCSIP-ArchivingEnabled</span></span></p></td>
<td><p><span data-ttu-id="83990-213">此属性是一个整数，用作位域，用于控制是否要存档单个用户的通信。</span><span class="sxs-lookup"><span data-stu-id="83990-213">This attribute is an integer used as a bit field to control whether a single user’s communications are to be archived.</span></span> <span data-ttu-id="83990-214">此控件由存档代理层强制执行。</span><span class="sxs-lookup"><span data-stu-id="83990-214">This control is enforced by the archiving agent layer.</span></span> <span data-ttu-id="83990-215">它标记为用于全局编录复制。</span><span class="sxs-lookup"><span data-stu-id="83990-215">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="83990-216">此属性的范围特定于单个用户或联系人。</span><span class="sxs-lookup"><span data-stu-id="83990-216">The scope of this attribute is specific to a single user or contact.</span></span> <span data-ttu-id="83990-217">Lync Server 中)  (和关联位位置的有效值如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-217">The valid values (and associated bit positions) in Lync Server are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-218">0：不存档 (未设置任何位) </span><span class="sxs-lookup"><span data-stu-id="83990-218">0: Do not archive (no bit set)</span></span></p></li>
<li><p><span data-ttu-id="83990-219">1：已停用 (位位置 0) </span><span class="sxs-lookup"><span data-stu-id="83990-219">1: Retired (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="83990-220">2：已停用 (位位置 1) </span><span class="sxs-lookup"><span data-stu-id="83990-220">2: Retired (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="83990-221">4：将内部通信存档 (位位置 2) </span><span class="sxs-lookup"><span data-stu-id="83990-221">4: Archive internal communications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="83990-222">8：将联合通信存档 (位位置 3) </span><span class="sxs-lookup"><span data-stu-id="83990-222">8: Archive federated communications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="83990-223">实时通信服务器2005中以前的有效值如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-223">Previously valid values in Live Communications Server 2005 are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-224">0：使用 <strong>msRTCSIP-ArchiveDefault</strong> 和 <strong>msRTCSIP-ArchiveFederation</strong> 定义的默认值，按优先级顺序排列：</span><span class="sxs-lookup"><span data-stu-id="83990-224">0:Use the default value defined by <strong>msRTCSIP-ArchiveDefault</strong> and <strong>msRTCSIP-ArchiveFederation</strong> in this order of precedence:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-225">1：存档</span><span class="sxs-lookup"><span data-stu-id="83990-225">1: Archive</span></span></p></li>
<li><p><span data-ttu-id="83990-226">2：不存档</span><span class="sxs-lookup"><span data-stu-id="83990-226">2: Do not archive</span></span></p></li>
<li><p><span data-ttu-id="83990-227">3：存档但不包含邮件正文</span><span class="sxs-lookup"><span data-stu-id="83990-227">3: Archive without the message body</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="83990-228">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-228">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-229">msRTCSIP-ArchivingServerData (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-229">msRTCSIP-ArchivingServerData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-230">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-230">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-231">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-231">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-232">msRTCSIP-ArchivingServerVersion (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-232">msRTCSIP-ArchivingServerVersion (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-233">此属性定义存档服务的版本。</span><span class="sxs-lookup"><span data-stu-id="83990-233">This attribute defines the version of the Archiving service.</span></span> <span data-ttu-id="83990-234">此属性是与每个正式产品版本递增的 monotonously 增加的整数类型。</span><span class="sxs-lookup"><span data-stu-id="83990-234">This attribute is a monotonously increasing integer type that increments with each official product release.</span></span> <span data-ttu-id="83990-235">可能的有效值如下：</span><span class="sxs-lookup"><span data-stu-id="83990-235">The possible valid values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-236">未定义：实时通信服务器2003</span><span class="sxs-lookup"><span data-stu-id="83990-236">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="83990-237">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="83990-237">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="83990-238">Live Communications Server 2005 SP1</span><span class="sxs-lookup"><span data-stu-id="83990-238">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="83990-239">3： Office 通信服务器2007</span><span class="sxs-lookup"><span data-stu-id="83990-239">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="83990-240">4： Office 通信服务器 2007 R2</span><span class="sxs-lookup"><span data-stu-id="83990-240">4: Office Communications Server 2007 R2</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-241">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-241">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-242">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-243">msRTCSIP-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="83990-243">msRTCSIP-BackEndServer</span></span></p></td>
<td><p><span data-ttu-id="83990-244">此属性指定池后端服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83990-244">This attribute specifies the FQDN of the Back End Server of the pool.</span></span> <span data-ttu-id="83990-245">由于每个池中只能有一个后端服务器，这是单值属性。</span><span class="sxs-lookup"><span data-stu-id="83990-245">Because there can only be a single Back End Server per pool, this is a single-valued attribute.</span></span></p>
<p><span data-ttu-id="83990-246">每个段的有效值为63个字符;整个 FQDN 的有效值为255个字符。</span><span class="sxs-lookup"><span data-stu-id="83990-246">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="83990-247">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-247">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-248">msRTCSIP-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="83990-248">msRTCSIP-ConferenceDirectoryHomePool</span></span></p></td>
<td><p><span data-ttu-id="83990-249">此属性包含托管会议目录的池的标识符。</span><span class="sxs-lookup"><span data-stu-id="83990-249">This attribute contains the identifier of the pool that hosts the conference directory.</span></span></p></td>
<td><p><span data-ttu-id="83990-250">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-250">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-251">msRTCSIP-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="83990-251">msRTCSIP-ConferenceDirectoryId</span></span></p></td>
<td><p><span data-ttu-id="83990-252">此属性包含会议目录的标识符。</span><span class="sxs-lookup"><span data-stu-id="83990-252">This attribute contains the identifier of a conference directory.</span></span></p></td>
<td><p><span data-ttu-id="83990-253">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-253">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-254">msRTCSIP-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="83990-254">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p></td>
<td><p><span data-ttu-id="83990-255">此属性包含要将会议目录移动到的池的标识符。</span><span class="sxs-lookup"><span data-stu-id="83990-255">This attribute contains the identifier of the pool to which the conference directory is being moved.</span></span></p></td>
<td><p><span data-ttu-id="83990-256">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-256">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-257">msRTCSIP-默认值</span><span class="sxs-lookup"><span data-stu-id="83990-257">msRTCSIP-Default</span></span></p></td>
<td><p><span data-ttu-id="83990-258">此布尔属性定义电话使用情况是否为默认用法。</span><span class="sxs-lookup"><span data-stu-id="83990-258">This Boolean attribute defines whether the phone usage is a default usage.</span></span> <span data-ttu-id="83990-259">如果此属性设置为 <strong>TRUE</strong>，则电话使用是默认用法，并且不能由管理员删除。</span><span class="sxs-lookup"><span data-stu-id="83990-259">If this attribute is set to <strong>TRUE</strong>, the phone usage is a default usage and cannot be deleted by the administrator.</span></span> <span data-ttu-id="83990-260">如果此属性设置为 <strong>FALSE</strong>，则可以删除用法。</span><span class="sxs-lookup"><span data-stu-id="83990-260">If this attribute is set to <strong>FALSE</strong>, the usage can be deleted.</span></span></p></td>
<td><p><span data-ttu-id="83990-261">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-261">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-262">msRTCSIP-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="83990-262">msRTCSIP-DefaultCWAExternalURL</span></span></p></td>
<td><p><span data-ttu-id="83990-263">此属性标识组织外部用户的 Communicator Web 访问 URL。</span><span class="sxs-lookup"><span data-stu-id="83990-263">This attribute identifies the Communicator Web Access URL for users who are outside the organization.</span></span></p></td>
<td><p><span data-ttu-id="83990-264">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-264">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-265">msRTCSIP-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="83990-265">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
<td><p><span data-ttu-id="83990-266">此属性标识组织内部用户的 Communicator Web 访问 URL。</span><span class="sxs-lookup"><span data-stu-id="83990-266">This attribute identifies the Communicator Web Access URL for users who are inside the organization.</span></span></p></td>
<td><p><span data-ttu-id="83990-267">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-267">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-268">msRTCSIP-DefaultLocationProfileLink (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-268">msRTCSIP-DefaultLocationProfileLink (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-269">此单值属性包含为其分配了位置配置文件类对象 (DN) 的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="83990-269">This single-valued attribute contains the distinguished name (DN) of a location profile class object assigned to it.</span></span></p>
<p><span data-ttu-id="83990-270">转发链接： <strong>链接 ID 11036</strong></span><span class="sxs-lookup"><span data-stu-id="83990-270">Forward link: <strong>Link ID 11036</strong></span></span></p>
<p><span data-ttu-id="83990-271">相应的反向链接为 <strong>msRTCSIP-ServerReferenceBL</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-271">The corresponding backward link is <strong>msRTCSIP-ServerReferenceBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-272">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-272">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-273">msRTCSIP-DefaultPolicy (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-273">msRTCSIP-DefaultPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-274">此布尔属性指定策略是否为默认策略。</span><span class="sxs-lookup"><span data-stu-id="83990-274">This Boolean attribute specifies whether the policy is a default policy.</span></span> <span data-ttu-id="83990-275">策略是设置为 <strong>TRUE</strong>时的默认策略。</span><span class="sxs-lookup"><span data-stu-id="83990-275">The policy is a default policy when set to <strong>TRUE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-276">Office 通信服务器2007中的新增</span><span class="sxs-lookup"><span data-stu-id="83990-276">New in Office Communications Server 2007</span></span></p>
<p><span data-ttu-id="83990-277">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-277">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-278">msRTCSIP-DefaultRouteToEdgeProxy (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-278">msRTCSIP-DefaultRouteToEdgeProxy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-279">此属性指定运行访问边缘服务的边缘服务器的 FQDN （如果可直接访问），或者指定运行 Access Edge 服务的服务器池的硬件负载平衡器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83990-279">This attribute specifies the FQDN of either the Edge Server running the Access Edge service, if it can be accessed directly, or of the hardware load balancer for a pool of servers running Access Edge service.</span></span> <span data-ttu-id="83990-280">如果运行 Access Edge 服务的服务器只能通过一个或多个控制器访问，则此属性指定 FQDN 和（可选）为控制器池提供服务的控制器或硬件负载平衡器的端口号。</span><span class="sxs-lookup"><span data-stu-id="83990-280">If the servers running Access Edge service can be accessed only through one or more Directors, this attribute specifies the FQDN and, optionally, the port number of the Director or of the hardware load balancer serving a Director pool.</span></span></p>
<p><span data-ttu-id="83990-281">每个段的有效值为63个字符;整个 FQDN 的有效值为255个字符。</span><span class="sxs-lookup"><span data-stu-id="83990-281">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="83990-282">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-282">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-283">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-283">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-284">msRTCSIP-DefaultRouteToEdgeProxyPort (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-285">此属性表示应用于连接到运行 Access Edge 服务的服务器的端口号。</span><span class="sxs-lookup"><span data-stu-id="83990-285">This attribute represents the port number that should be used to connect to the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="83990-286">有效值是指定要使用的端口的整数值。</span><span class="sxs-lookup"><span data-stu-id="83990-286">The valid value is an integer value specifying the port to be used.</span></span> <span data-ttu-id="83990-287">默认值为5061。</span><span class="sxs-lookup"><span data-stu-id="83990-287">The default value is 5061.</span></span></p></td>
<td><p><span data-ttu-id="83990-288">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-288">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-289">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-289">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-290">msRTCSIP-DefPresenceSubscriptionTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-291">此属性表示默认状态订阅的超时期限。</span><span class="sxs-lookup"><span data-stu-id="83990-291">This attribute represents the default presence subscription time-out period.</span></span></p></td>
<td><p><span data-ttu-id="83990-292">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-292">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-293">msRTCSIP-DefRegistrationTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-293">msRTCSIP-DefRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-294">此属性表示默认的注册超时窗口。</span><span class="sxs-lookup"><span data-stu-id="83990-294">This attribute represents the default registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="83990-295">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-295">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-297">此属性表示默认的漫游数据订阅超时窗口。</span><span class="sxs-lookup"><span data-stu-id="83990-297">This attribute represents the default roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="83990-298">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-298">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-299">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="83990-299">msRTCSIP-DeploymentLocator</span></span></p></td>
<td><p><span data-ttu-id="83990-300">此属性在拆分的域拓扑中使用，并且包含 (FQDN) 的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="83990-300">This attribute is used in a split domain topology and contains a fully qualified domain name (FQDN).</span></span></p></td>
<td><p><span data-ttu-id="83990-301">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-301">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-302">msRTCSIP-说明 (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-302">msRTCSIP-Description (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-303">此单值 UNICODE 字符串属性包含此电话路由或规范化规则的友好描述。</span><span class="sxs-lookup"><span data-stu-id="83990-303">This single-valued UNICODE string attribute contains a friendly description of this phone route or normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="83990-304">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-304">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-305">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-305">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-306">msRTCSIP-DomainData</span><span class="sxs-lookup"><span data-stu-id="83990-306">msRTCSIP-DomainData</span></span></p></td>
<td><p><span data-ttu-id="83990-307">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-307">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-308">msRTCSIP-域名</span><span class="sxs-lookup"><span data-stu-id="83990-308">msRTCSIP-DomainName</span></span></p></td>
<td><p><span data-ttu-id="83990-309">此属性表示为注册机构配置的域。</span><span class="sxs-lookup"><span data-stu-id="83990-309">This attribute represents a domain configured for the Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-310">msRTCSIP-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="83990-310">msRTCSIP-EdgeProxyData</span></span></p></td>
<td><p><span data-ttu-id="83990-311">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-311">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-312">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-312">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-313">msRTCSIP-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="83990-313">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="83990-314">此属性指定运行访问边缘服务的服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83990-314">This attribute specifies the FQDN of the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="83990-315">每个段的有效值为63个字符;整个 FQDN 的有效值为255个字符。</span><span class="sxs-lookup"><span data-stu-id="83990-315">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="83990-316">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-316">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-317">msRTCSIP-EnableBestEffortNotify (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-317">msRTCSIP-EnableBestEffortNotify (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-318">此属性控制服务器是否生成最佳操作通知 (BENOTIFY) 请求（而不是通知请求）以响应来自客户的订阅请求。</span><span class="sxs-lookup"><span data-stu-id="83990-318">This attribute controls whether a server generates a Best Effort NOTIFY (BENOTIFY) request, instead of a NOTIFY request, in response to a SUBSCRIBE request from a client.</span></span> <span data-ttu-id="83990-319">BENOTIFY 是对订阅通知握手的性能增强扩展，服务器将生成 BENOTIFY 请求，而不是常规通知请求。</span><span class="sxs-lookup"><span data-stu-id="83990-319">BENOTIFY is a performance-enhancing extension to the subscribe notification handshake where the server generates BENOTIFY requests, instead of regular NOTIFY requests.</span></span> <span data-ttu-id="83990-320">性能好处是 BENOTIFY 请求不需要来自客户端的 200 OK 响应，因为通知请求。</span><span class="sxs-lookup"><span data-stu-id="83990-320">The performance benefit is that a BENOTIFY request does not require a 200 OK response from the client as the NOTIFY request does.</span></span></p>
<p><span data-ttu-id="83990-321">有效值为 <strong>TRUE</strong> 或 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-321">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="83990-322">实时通信服务器2003不支持 BENOTIFY 请求。</span><span class="sxs-lookup"><span data-stu-id="83990-322">Live Communications Server 2003 does not support BENOTIFY requests.</span></span> <span data-ttu-id="83990-323">若要与在实时通信服务器2005和第三方服务器上运行的实时通信2003服务器 API 编写的服务器应用程序互操作，可通过将 BENOTIFY 请求的值设置为 <STRONG>FALSE</STRONG>来禁用这些请求。</span><span class="sxs-lookup"><span data-stu-id="83990-323">To interoperate with server applications written with the Live Communications Server 2003 server API running on Live Communications Server 2005 and third-party servers, BENOTIFY requests can be disabled by setting its value to <STRONG>FALSE</STRONG>.</span></span> <span data-ttu-id="83990-324">BENOTIFY 目前不属于 IETF (Internet 工程任务组) SIP 标准化过程。</span><span class="sxs-lookup"><span data-stu-id="83990-324">BENOTIFY is not currently part of the IETF (Internet Engineering Task Force) SIP standardization process.</span></span>


</div></td>
<td><p><span data-ttu-id="83990-325">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-325">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-326">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-326">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-327">msRTCSIP-EnableFederation (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-327">msRTCSIP-EnableFederation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-328">此属性是一个全局开关，IT 管理员使用它配置用户是否可以与其他组织中的用户进行通信。</span><span class="sxs-lookup"><span data-stu-id="83990-328">This attribute is a global switch that IT administrators use to configure whether users are allowed to communicate with users from other organizations.</span></span> <span data-ttu-id="83990-329">它使管理员能够覆盖单个用户的 <strong>FederationEnabled</strong> 属性。</span><span class="sxs-lookup"><span data-stu-id="83990-329">It enables an administrator to overwrite an individual user’s <strong>FederationEnabled</strong> attribute.</span></span> <span data-ttu-id="83990-330">此属性可用于帮助保护内部网络免受受蠕虫、病毒或公司的目标攻击导致的网络攻击。</span><span class="sxs-lookup"><span data-stu-id="83990-330">This attribute can be useful to help protect the internal network from Internet attacks that may be caused by worms, viruses, or targeted attacks on the company.</span></span></p>
<p><span data-ttu-id="83990-331">有效值 (和关联位位置) 如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-331">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-332">1：已启用公共 IM 连接 (位位置 0) </span><span class="sxs-lookup"><span data-stu-id="83990-332">1: Enabled for public IM connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="83990-333">2：保留 (位位置 1) </span><span class="sxs-lookup"><span data-stu-id="83990-333">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="83990-334">4：保留 (位位置 2) </span><span class="sxs-lookup"><span data-stu-id="83990-334">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="83990-335">8：保留 (位位置 3) </span><span class="sxs-lookup"><span data-stu-id="83990-335">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="83990-336">16：启用远程呼叫控制 [电话服务] (位位置 4) </span><span class="sxs-lookup"><span data-stu-id="83990-336">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="83990-337">64： AllowOrganizeMeetingWithAnonymousParticipants (允许用户向 (位位置6的会议邀请匿名用户) </span><span class="sxs-lookup"><span data-stu-id="83990-337">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="83990-338">128： UCEnabled (为统一通信启用用户)  (位位置 7) </span><span class="sxs-lookup"><span data-stu-id="83990-338">128: UCEnabled (enable users for unified communications) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="83990-339">256： EnabledForEnhancedPresence (启用公共 IM 连接的用户)  (位位置 8) </span><span class="sxs-lookup"><span data-stu-id="83990-339">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="83990-340">512： RemoteCallControlDualMode (位位置 9) </span><span class="sxs-lookup"><span data-stu-id="83990-340">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-341">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-341">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-342">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-342">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-343">msRTCSIP-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="83990-343">msRTCSIP-EnterpriseServices</span></span></p></td>
<td><p><span data-ttu-id="83990-344">此属性指示是否已在给定服务器上加载企业服务。</span><span class="sxs-lookup"><span data-stu-id="83990-344">This attribute indicates whether the Enterprise Services are loaded on the given server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-345">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="83990-345">msRTCSIP-ExtensionData</span></span></p></td>
<td><p><span data-ttu-id="83990-346">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-346">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-347">msRTCSIP-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="83990-347">msRTCSIP-ExternalAccessCode</span></span></p></td>
<td><p><span data-ttu-id="83990-348">此属性包含用于外部访问的拨号代码。</span><span class="sxs-lookup"><span data-stu-id="83990-348">This attribute contains the dial code for external access.</span></span></p></td>
<td><p><span data-ttu-id="83990-349">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-349">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-350">msRTCSIP-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="83990-350">msRTCSIP-FederationEnabled</span></span></p></td>
<td><p><span data-ttu-id="83990-351">此属性控制是否为单个用户启用联盟。</span><span class="sxs-lookup"><span data-stu-id="83990-351">This attribute controls whether a single user is enabled for federation.</span></span> <span data-ttu-id="83990-352">它由企业服务层强制执行。</span><span class="sxs-lookup"><span data-stu-id="83990-352">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="83990-353">它标记为用于全局编录复制。</span><span class="sxs-lookup"><span data-stu-id="83990-353">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="83990-354">有效值为 <strong>TRUE</strong> 或 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-354">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-355">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-355">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-356">msRTCSIP-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="83990-356">msRTCSIP-FrontEndServers</span></span></p></td>
<td><p><span data-ttu-id="83990-357">此属性是与池关联的所有企业版服务器的域名的多值列表。</span><span class="sxs-lookup"><span data-stu-id="83990-357">This attribute is a multi-valued list of the domain names of all Enterprise Edition servers associated with a pool.</span></span></p>
<p><span data-ttu-id="83990-358">反向链接： <strong>链接 ID 11023</strong></span><span class="sxs-lookup"><span data-stu-id="83990-358">Back link: <strong>Link ID 11023</strong></span></span></p>
<p><span data-ttu-id="83990-359">指向此 back 链接的相应正向链接是 <strong>msRTCSIP-PoolAddress</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-359">The corresponding forward link to this back link is <strong>msRTCSIP-PoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-360">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-360">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-361">msRTCSIP-网关 (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-361">msRTCSIP-Gateways (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-362">此多值字符串属性包含网关) 和每个网关的端口 (列表。</span><span class="sxs-lookup"><span data-stu-id="83990-362">This multi-valued string attribute contains a list of gateways and ports (per gateway).</span></span></p></td>
<td><p><span data-ttu-id="83990-363">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-363">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-364">msRTCSIP-GlobalSettingsData (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-364">msRTCSIP-GlobalSettingsData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-365">此属性存储 "名称：值" 对。</span><span class="sxs-lookup"><span data-stu-id="83990-365">This attribute stores name:value pairs.</span></span> <span data-ttu-id="83990-366">已定义的名称：值对用于 " <strong>允许轮询状态</strong> " 设置。</span><span class="sxs-lookup"><span data-stu-id="83990-366">The already-defined name:value pair is for the <strong>allow polling for presence</strong> setting.</span></span></p></td>
<td><p><span data-ttu-id="83990-367">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-367">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-368">msRTCSIP-GroupingID</span><span class="sxs-lookup"><span data-stu-id="83990-368">msRTCSIP-GroupingID</span></span></p></td>
<td><p><span data-ttu-id="83990-369">此属性是用于分组通讯簿条目的组的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="83990-369">This attribute is a unique identifier of a group that is used to group address book entries.</span></span></p></td>
<td><p><span data-ttu-id="83990-370">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-370">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-371">msRTCSIP-HomeServer (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-371">msRTCSIP-HomeServer (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-372">实时通信服务器2003中的新增 (未使用) 。</span><span class="sxs-lookup"><span data-stu-id="83990-372">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="83990-373">在实时通信服务器2005中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-373">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-374">msRTCSIP-HomeServerString (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-374">msRTCSIP-HomeServerString (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-375">实时通信服务器2003中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-375">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="83990-376">在实时通信服务器2005中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-376">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-377">msRTCSIP-HomeUsers (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-377">msRTCSIP-HomeUsers (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-378">实时通信服务器2003中的新增 (未使用) 。</span><span class="sxs-lookup"><span data-stu-id="83990-378">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="83990-379">在实时通信服务器2005中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-379">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-380">msRTCSIP-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="83990-380">msRTCSIP-InternetAccessEnabled</span></span></p></td>
<td><p><span data-ttu-id="83990-381">此属性控制是否为单个用户启用外部用户访问权限。</span><span class="sxs-lookup"><span data-stu-id="83990-381">This attribute controls whether a single user is enabled for outside user access.</span></span> <span data-ttu-id="83990-382">它由企业服务层强制执行。</span><span class="sxs-lookup"><span data-stu-id="83990-382">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="83990-383">它标记为用于全局编录复制。</span><span class="sxs-lookup"><span data-stu-id="83990-383">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="83990-384">有效值为 <strong>TRUE</strong> 或 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-384">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-385">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-385">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-386">msRTCSIP-IsMaster (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-386">msRTCSIP-IsMaster (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-387">实时通信服务器2003中的新增</span><span class="sxs-lookup"><span data-stu-id="83990-387">New in Live Communications Server 2003</span></span></p>
<p><span data-ttu-id="83990-388">在实时通信服务器2005中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-388">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-389">msRTCSIP-行</span><span class="sxs-lookup"><span data-stu-id="83990-389">msRTCSIP-Line</span></span></p></td>
<td><p><span data-ttu-id="83990-390">此单值属性包含设备 ID (由 Lync 用于电话服务) 用户控制的电话的 SIP URI 或电话 URI。</span><span class="sxs-lookup"><span data-stu-id="83990-390">This single-valued attribute contains the device ID (either the SIP URI or the TEL URI of the phone the user controls) used by Lync for telephony.</span></span> <span data-ttu-id="83990-391">此属性标记为 "全局编录复制"，并且已编制索引。</span><span class="sxs-lookup"><span data-stu-id="83990-391">This attribute is marked for Global Catalog replication and is indexed.</span></span> <span data-ttu-id="83990-392">如果用户已启用企业语音，此属性将存储标准化的用户电话号码版本。</span><span class="sxs-lookup"><span data-stu-id="83990-392">If a user is enabled for Enterprise Voice, this attribute stores the E.164 normalized version of the user’s phone number.</span></span></p></td>
<td><p><span data-ttu-id="83990-393">Microsoft Office Live 通信服务器2005中的新增 SP1</span><span class="sxs-lookup"><span data-stu-id="83990-393">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-394">msRTCSIP-LineServer</span><span class="sxs-lookup"><span data-stu-id="83990-394">msRTCSIP-LineServer</span></span></p></td>
<td><p><span data-ttu-id="83990-395">此单值属性包含 CSTA 的 sip 网关服务器的 SIP URI。</span><span class="sxs-lookup"><span data-stu-id="83990-395">This single-valued attribute contains the SIP URI of the CSTA-SIP gateway server.</span></span> <span data-ttu-id="83990-396">此属性标记为全局编录复制，但未编入索引。</span><span class="sxs-lookup"><span data-stu-id="83990-396">This attribute is marked for Global Catalog replication but is not indexed.</span></span></p></td>
<td><p><span data-ttu-id="83990-397">Microsoft Office Live 通信服务器2005中的新增 SP1</span><span class="sxs-lookup"><span data-stu-id="83990-397">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-398">msRTCSIP-LocalNormalizationData (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-398">msRTCSIP-LocalNormalizationData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-399">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-399">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-400">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-400">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-401">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-401">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-402">msRTCSIP-LocalNormalizationLinks (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-402">msRTCSIP-LocalNormalizationLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-403">此多值属性包含与此位置配置文件关联 (DN) 的本地规范化可分辨名称的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-403">This multi-valued attribute contains a list of local normalization distinguished names (DN) associated with this location profile.</span></span> <span data-ttu-id="83990-404">此属性的类型是 DN 二进制。</span><span class="sxs-lookup"><span data-stu-id="83990-404">The type of this attribute is a DN binary.</span></span> <span data-ttu-id="83990-405">位置配置文件与本地规范化规则之间存在一对多关系。</span><span class="sxs-lookup"><span data-stu-id="83990-405">There is a one-to-many relationship between location profile and local normalization rules.</span></span> <span data-ttu-id="83990-406">本地规范化 DNs 列表的顺序必须按管理员指定的顺序进行维护。</span><span class="sxs-lookup"><span data-stu-id="83990-406">The ordering of the list of local normalization DNs must be maintained in the order specified by the administrator.</span></span> <span data-ttu-id="83990-407">顺序保留由 DN 二进制部分的二进制部分进行维护，该二进制部分指定订单索引。</span><span class="sxs-lookup"><span data-stu-id="83990-407">The preservation of order is maintained by the binary portion of the DN binary, which specifies the order index.</span></span></p>
<p><span data-ttu-id="83990-408">转发链接： <strong>链接 ID 11034</strong></span><span class="sxs-lookup"><span data-stu-id="83990-408">Forward link: <strong>Link ID 11034</strong></span></span></p>
<p><span data-ttu-id="83990-409">此前向链接属性的对应反向链接是 <strong>msRTCSIP-LocationProfileBL</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-409">The corresponding back link to this forward link attribute is <strong>msRTCSIP-LocationProfileBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-410">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-410">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-411">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-411">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-412">msRTCSIP-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="83990-412">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
<td><p><span data-ttu-id="83990-413">此属性包含规范化规则的选项列表。</span><span class="sxs-lookup"><span data-stu-id="83990-413">This attribute contains a list of options for the normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="83990-414">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-414">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-415">msRTCSIP-LocationName (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-415">msRTCSIP-LocationName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-416">此单值属性包含位置配置文件的友好名称，用于指示此配置文件所代表的位置。</span><span class="sxs-lookup"><span data-stu-id="83990-416">This single-valued attribute contains a friendly name for the location profile that indicates which location this profile represents.</span></span> <span data-ttu-id="83990-417">由于可以有多个位置配置文件，因此管理员需要一种方式来区分不同的配置文件。</span><span class="sxs-lookup"><span data-stu-id="83990-417">Because there can be multiple location profiles, the administrator needs a way to distinguish between different profiles.</span></span></p></td>
<td><p><span data-ttu-id="83990-418">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-418">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-419">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-419">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-420">msRTCSIP-locationProfileBL (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-420">msRTCSIP-locationProfileBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-421">此多值属性包含位置配置文件的可分辨名称的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-421">This multi-valued attribute contains a list of location profile distinguished names.</span></span> <span data-ttu-id="83990-422">此属性指定指向一个或多个位置配置文件的反向链接。</span><span class="sxs-lookup"><span data-stu-id="83990-422">This attribute specifies the back link to one or more location profiles.</span></span></p>
<p><span data-ttu-id="83990-423">反向链接： <strong>链接 ID 11035</strong></span><span class="sxs-lookup"><span data-stu-id="83990-423">Back link: <strong>Link ID 11035</strong></span></span></p>
<p><span data-ttu-id="83990-424">此属性对应于 <strong>msRTCSIP-LocalNormalizationLinks</strong>的前进链接。</span><span class="sxs-lookup"><span data-stu-id="83990-424">This attribute corresponds to the forward link <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-425">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-425">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-426">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-426">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-427">msRTCSIP-LocationProfileData (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-427">msRTCSIP-LocationProfileData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-428">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-428">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-429">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-429">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-430">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-430">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-431">msRTCSIP-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="83990-431">msRTCSIP-LocationProfileOptions</span></span></p></td>
<td><p><span data-ttu-id="83990-432">此属性包含位置配置文件的选项。</span><span class="sxs-lookup"><span data-stu-id="83990-432">This attribute contains the options for the location profile.</span></span></p></td>
<td><p><span data-ttu-id="83990-433">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-433">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-434">msRTCSIP-MappingContact</span><span class="sxs-lookup"><span data-stu-id="83990-434">msRTCSIP-MappingContact</span></span></p></td>
<td><p><span data-ttu-id="83990-435">此多值属性包含应用程序联系人列表。</span><span class="sxs-lookup"><span data-stu-id="83990-435">This multiple-value attribute holds a list of application contacts.</span></span></p></td>
<td><p><span data-ttu-id="83990-436">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-436">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-437">msRTCSIP-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="83990-437">msRTCSIP-MappingLocation</span></span></p></td>
<td><p><span data-ttu-id="83990-438">此多值属性包含位置配置文件的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-438">This multiple-value attribute holds a list of location profiles.</span></span></p></td>
<td><p><span data-ttu-id="83990-439">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-439">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-440">msRTCSIP-MaxNumOutstandingSearchPerServer (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-441">此属性表示每台服务器的未完成搜索请求的最大数量。</span><span class="sxs-lookup"><span data-stu-id="83990-441">This attribute represents the maximum number of outstanding search requests per server.</span></span></p></td>
<td><p><span data-ttu-id="83990-442">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-442">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-443">msRTCSIP-MaxNumSubscriptionsPerUser (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-444">该属性表示每个用户的最大订阅数。</span><span class="sxs-lookup"><span data-stu-id="83990-444">The attribute represents the maximum number of subscriptions per user.</span></span></p></td>
<td><p><span data-ttu-id="83990-445">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-445">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-446">msRTCSIP-MaxPresenceSubscriptionTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-447">此属性表示最长订阅超时时间窗口。</span><span class="sxs-lookup"><span data-stu-id="83990-447">This attribute represents the maximum subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="83990-448">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-448">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-449">msRTCSIP-MaxRegistrationsTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-449">msRTCSIP-MaxRegistrationsTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-450">此属性表示最大注册超时时段。</span><span class="sxs-lookup"><span data-stu-id="83990-450">This attribute represents the maximum registrations time-out window.</span></span></p></td>
<td><p><span data-ttu-id="83990-451">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-451">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-453">此属性表示 "漫游数据订阅最大超时" 窗口。</span><span class="sxs-lookup"><span data-stu-id="83990-453">This attribute represents the maximum roaming data subscriptions time-out window.</span></span></p></td>
<td><p><span data-ttu-id="83990-454">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-454">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-455">msRTCSIP-MCUData</span><span class="sxs-lookup"><span data-stu-id="83990-455">msRTCSIP-MCUData</span></span></p></td>
<td><p><span data-ttu-id="83990-456">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-456">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-457">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-457">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-458">msRTCSIP-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="83990-458">msRTCSIP-MCUFactoryAddress</span></span></p></td>
<td><p><span data-ttu-id="83990-459">此属性是计算机类下的服务控制点属性，用于指定链接返回到其所属的 multipoint 控件单元 (MCU) 工厂。</span><span class="sxs-lookup"><span data-stu-id="83990-459">This attribute is a service control point attribute under the computer class that specifies a link back to the multipoint control unit (MCU) Factory to which it belongs.</span></span> <span data-ttu-id="83990-460">将为每个 Microsoft MCU 创建此服务控制点和属性。</span><span class="sxs-lookup"><span data-stu-id="83990-460">This service control point and attribute is created for every Microsoft MCU.</span></span> <span data-ttu-id="83990-461">每个 Microsoft MCU 都必须找到其所属池的后端服务器，才能从中检索池级别的设置。</span><span class="sxs-lookup"><span data-stu-id="83990-461">Each Microsoft MCU must find the Back End Server of the pool to which it belongs, in order to retrieve pool-level settings from it.</span></span></p>
<p><span data-ttu-id="83990-462">此属性的值是 MCU 工厂 (DN) 的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="83990-462">The value of this attribute is the distinguished name (DN) of the MCU Factory.</span></span> <span data-ttu-id="83990-463">这是单值属性，并标记为用于全局编录复制。</span><span class="sxs-lookup"><span data-stu-id="83990-463">This is a single-valued attribute and marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="83990-464">转发链接： <strong>链接 ID 11026</strong></span><span class="sxs-lookup"><span data-stu-id="83990-464">Forward link: <strong>Link ID 11026</strong></span></span></p>
<p><span data-ttu-id="83990-465">此前向链接属性的对应反向链接是 <strong>msRTCSIP-MCUServers</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-465">The corresponding back link to this forward link attribute is <strong>msRTCSIP-MCUServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-466">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-466">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-467">msRTCSIP-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="83990-467">msRTCSIP-MCUFactoryData</span></span></p></td>
<td><p><span data-ttu-id="83990-468">这是一个多字符串保留属性。</span><span class="sxs-lookup"><span data-stu-id="83990-468">This is a multi-string reserved attribute.</span></span> <span data-ttu-id="83990-469">存储在此属性中的设置表示为 name = value 对。</span><span class="sxs-lookup"><span data-stu-id="83990-469">Settings stored in this attribute are represented as name=value pairs.</span></span> <span data-ttu-id="83990-470">当前定义的 name = value 对：</span><span class="sxs-lookup"><span data-stu-id="83990-470">Currently defined name=value pairs are:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-471">FactoryURL = &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="83990-471">FactoryURL = &lt;URL&gt;</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-472">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-472">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-473">msRTCSIP-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="83990-473">msRTCSIP-MCUFactoryPath</span></span></p></td>
<td><p><span data-ttu-id="83990-474">这是一个单值属性，包含与池关联的单个 MCU 工厂 (DN) 的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="83990-474">This is a single-valued attribute that contains the distinguished name (DN) of a single MCU factory associated with a pool.</span></span></p>
<p><span data-ttu-id="83990-475">转发链接： <strong>链接 ID 11024</strong></span><span class="sxs-lookup"><span data-stu-id="83990-475">Forward link: <strong>Link ID 11024</strong></span></span></p>
<p><span data-ttu-id="83990-476">此前向链接属性的对应反向链接是 <strong>msRTCSIP-PoolAddresses</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-476">The corresponding back link to this forward link attribute is <strong>msRTCSIP-PoolAddresses</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-477">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-477">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-478">msRTCSIP-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="83990-478">msRTCSIP-MCUFactoryProviderID</span></span></p></td>
<td><p><span data-ttu-id="83990-479">此属性是一个单值字符串，用于指定 MCU 工厂提供程序的 GUID。</span><span class="sxs-lookup"><span data-stu-id="83990-479">This attribute is a single-valued string that specifies the GUID of the MCU factory provider.</span></span> <span data-ttu-id="83990-480">根据 GUID 值，MCU 工厂进程确定是否为此 MCU 类型服务。</span><span class="sxs-lookup"><span data-stu-id="83990-480">Based on the GUID value, the MCU factory process determines whether to service this MCU type.</span></span> <span data-ttu-id="83990-481">如果 GUID 值为 <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>，则默认情况下， (在 Lync Server 中使用 MCU 工厂进程) 将处理它。</span><span class="sxs-lookup"><span data-stu-id="83990-481">If the GUID value is <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, then the MCU factory process (available by default in Lync Server) will process it.</span></span> <span data-ttu-id="83990-482">对于任何其他 GUID 值，MCU 工厂进程将不会为 MCU 类型提供服务。</span><span class="sxs-lookup"><span data-stu-id="83990-482">For any other GUID value, the MCU factory process will not service the MCU type.</span></span></p></td>
<td><p><span data-ttu-id="83990-483">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-483">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-484">msRTCSIP-MCUServers</span><span class="sxs-lookup"><span data-stu-id="83990-484">msRTCSIP-MCUServers</span></span></p></td>
<td><p><span data-ttu-id="83990-485">此属性是 (DN) 的多值可分辨名称列表。</span><span class="sxs-lookup"><span data-stu-id="83990-485">This attribute is a multi-valued list of distinguished names (DN).</span></span> <span data-ttu-id="83990-486">此属性包含与此 MCU 工厂关联的同一类型和供应商的所有 MCU 服务器的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-486">This attribute contains a list of all MCU servers of the same type and vendor associated with this MCU factory.</span></span> <span data-ttu-id="83990-487">每个段的有效值为63个字符;整个 FQDN 的有效值为255个字符。</span><span class="sxs-lookup"><span data-stu-id="83990-487">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p>
<p><span data-ttu-id="83990-488">反向链接：链接 ID 11027</span><span class="sxs-lookup"><span data-stu-id="83990-488">Back link: Link ID 11027</span></span></p>
<p><span data-ttu-id="83990-489">指向此 back 链接的相应正向链接是 <strong>msRTCSIP-MCUFactoryAddress</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-489">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-490">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-490">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-491">msRTCSIP-MCUType</span><span class="sxs-lookup"><span data-stu-id="83990-491">msRTCSIP-MCUType</span></span></p></td>
<td><p><span data-ttu-id="83990-492">此属性是一个单值字符串，用于指定 MCU 可以处理的媒介。</span><span class="sxs-lookup"><span data-stu-id="83990-492">This attribute is a single-valued string that specifies the medium the MCU can handle.</span></span></p>
<p><span data-ttu-id="83990-493">受支持的有效类型包括：</span><span class="sxs-lookup"><span data-stu-id="83990-493">Supported valid types are:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-494">符合</span><span class="sxs-lookup"><span data-stu-id="83990-494">meeting</span></span></p></li>
<li><p><span data-ttu-id="83990-495">音频视频</span><span class="sxs-lookup"><span data-stu-id="83990-495">audio-video</span></span></p></li>
<li><p><span data-ttu-id="83990-496">聊天</span><span class="sxs-lookup"><span data-stu-id="83990-496">chat</span></span></p></li>
<li><p><span data-ttu-id="83990-497">电话会议</span><span class="sxs-lookup"><span data-stu-id="83990-497">phone-conf</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-498">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-498">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-499">msRTCSIP-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="83990-499">msRTCSIP-MCUVendor</span></span></p></td>
<td><p><span data-ttu-id="83990-500">此属性是一个单值字符串，用于指定 MCU 供应商的名称。</span><span class="sxs-lookup"><span data-stu-id="83990-500">This attribute is a single-valued string that specifies an MCU vendor’s name.</span></span> <span data-ttu-id="83990-501">所有 Microsoft MCUs 都将此属性指定为 <strong>Microsoft Corporation</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-501">All Microsoft MCUs will specify this attribute to be <strong>Microsoft Corporation</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-502">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-502">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-503">msRTCSIP-MeetingFlags (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-503">msRTCSIP-MeetingFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-504">此属性定义为所有用户或联系人对象全局启用的不同会议选项。</span><span class="sxs-lookup"><span data-stu-id="83990-504">This attribute defines different meeting options that are enabled globally for all users or contact objects.</span></span> <span data-ttu-id="83990-505">此属性是整数类型的位掩码值。</span><span class="sxs-lookup"><span data-stu-id="83990-505">This attribute is a bit-mask value of integer type.</span></span></p>
<p><span data-ttu-id="83990-506">有效值 (和关联位位置) 如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-506">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-507">0： AllowOrganizeMeetingWithAnonymousParticipants 为 None (不允许用户邀请匿名用户加入会议)  (未设置任何 bits) </span><span class="sxs-lookup"><span data-stu-id="83990-507">0: AllowOrganizeMeetingWithAnonymousParticipants is None (do not allow users to invite anonymous users to meetings) (no bits set)</span></span></p></li>
<li><p><span data-ttu-id="83990-508">4： AllowOrganizeMeetingWithAnonymousParticipants 是 "每个人" (允许所有用户邀请匿名用户加入会议)  (位位置 2) </span><span class="sxs-lookup"><span data-stu-id="83990-508">4: AllowOrganizeMeetingWithAnonymousParticipants is Everyone (allow all users to invite anonymous users to meetings) (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="83990-509">8： AllowOrganizeMeetingWithAnonymousParticipants 为 UsePerUserSetting (允许用户基于每个用户设置邀请匿名用户加入会议)  (位位置 3) </span><span class="sxs-lookup"><span data-stu-id="83990-509">8: AllowOrganizeMeetingWithAnonymousParticipants is UsePerUserSetting (allow users to invite anonymous users to meetings based on per user setting) (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="83990-510">16： UserPerUserMeetingPolicy (会议策略按用户定义)  (位位置 4) </span><span class="sxs-lookup"><span data-stu-id="83990-510">16: UserPerUserMeetingPolicy (meeting policy is defined per user) (bit position 4)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-511">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-511">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-512">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-512">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-513">msRTCSIP-MeetingPolicy (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-513">msRTCSIP-MeetingPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-514">此属性指定管理员为此用户分配的策略 (DN) 的可分辨名称作为单值属性。</span><span class="sxs-lookup"><span data-stu-id="83990-514">This attribute specifies the distinguished name (DN) of the policy the administrator has assigned for this user as a single-valued attribute.</span></span></p></td>
<td><p><span data-ttu-id="83990-515">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-515">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-516">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-516">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-517">msRTCSIP-MinPresenceSubscriptionTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-518">此属性表示最小联机状态订阅超时窗口。</span><span class="sxs-lookup"><span data-stu-id="83990-518">This attribute represents the minimum presence subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="83990-519">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-519">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-520">msRTCSIP-MinRegistrationTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-520">msRTCSIP-MinRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-521">此属性表示最小的注册超时窗口。</span><span class="sxs-lookup"><span data-stu-id="83990-521">This attribute represents the minimum registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="83990-522">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-522">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-523">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-523">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-525">此属性表示最少的漫游数据订阅超时窗口。</span><span class="sxs-lookup"><span data-stu-id="83990-525">This attribute represents the minimum roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="83990-526">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-526">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-527">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-527">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-528">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="83990-528">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="83990-529">此属性用于存储前端池使用的镜像 SQL Server 后端。</span><span class="sxs-lookup"><span data-stu-id="83990-529">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
<td><p><span data-ttu-id="83990-530">Lync Server 2013 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-530">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-531">msRTCSIP-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="83990-531">msRTCSIP-MobilityFlags</span></span></p></td>
<td><p><span data-ttu-id="83990-532">此属性包含用于定义移动设置的选项和标志。</span><span class="sxs-lookup"><span data-stu-id="83990-532">This attribute contains options and flags that define mobility settings.</span></span></p></td>
<td><p><span data-ttu-id="83990-533">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-533">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-534">msRTCSIP-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="83990-534">msRTCSIP-MobilityPolicy</span></span></p></td>
<td><p><span data-ttu-id="83990-535">此属性包含移动策略对象的 DN。</span><span class="sxs-lookup"><span data-stu-id="83990-535">This attribute contains the DN for a mobility policy object.</span></span></p></td>
<td><p><span data-ttu-id="83990-536">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-536">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-537">msRTCSIP-NumDevicesPerUser (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-537">msRTCSIP-NumDevicesPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-538">此属性表示用户可以注册 SIP 通信和订阅状态的允许的设备数。</span><span class="sxs-lookup"><span data-stu-id="83990-538">This attribute represents the allowed number of devices on which a user can register for SIP communications and subscribe to presence.</span></span></p></td>
<td><p><span data-ttu-id="83990-539">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-539">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-540">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-540">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-541">msRTCSIP-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="83990-541">msRTCSIP-OptionFlags</span></span></p></td>
<td><p><span data-ttu-id="83990-542">此属性指定为用户或联系人对象启用的选项。</span><span class="sxs-lookup"><span data-stu-id="83990-542">This attribute specifies the options that are enabled for the user or contact object.</span></span> <span data-ttu-id="83990-543">此属性是整数类型的位掩码值。</span><span class="sxs-lookup"><span data-stu-id="83990-543">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="83990-544">每个选项表示一个位。</span><span class="sxs-lookup"><span data-stu-id="83990-544">Each option is represented by a bit.</span></span> <span data-ttu-id="83990-545">此属性标记为 "全局编录复制"。</span><span class="sxs-lookup"><span data-stu-id="83990-545">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="83990-546">有效值 (和关联位位置) 如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-546">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-547">1：已启用公共即时消息 (IM) 连接 (位位置 0) </span><span class="sxs-lookup"><span data-stu-id="83990-547">1: Enabled for public instant messaging (IM) connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="83990-548">2：保留 (位位置 1) </span><span class="sxs-lookup"><span data-stu-id="83990-548">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="83990-549">4：保留 (位位置 2) </span><span class="sxs-lookup"><span data-stu-id="83990-549">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="83990-550">8：保留 (位位置 3) </span><span class="sxs-lookup"><span data-stu-id="83990-550">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="83990-551">16：启用远程呼叫控制 [电话服务] (位位置 4) </span><span class="sxs-lookup"><span data-stu-id="83990-551">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="83990-552">64： AllowOrganizeMeetingWithAnonymousParticipants (允许用户向 (位位置6的会议邀请匿名用户) </span><span class="sxs-lookup"><span data-stu-id="83990-552">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="83990-553">128： UCEnabled (启用 UC) 的用户 (位位置 7) </span><span class="sxs-lookup"><span data-stu-id="83990-553">128: UCEnabled (enable users for UC) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="83990-554">256： EnabledForEnhancedPresence (启用公共 IM 连接的用户)  (位位置 8) </span><span class="sxs-lookup"><span data-stu-id="83990-554">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="83990-555">512： RemoteCallControlDualMode (位位置 9) </span><span class="sxs-lookup"><span data-stu-id="83990-555">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-556">SP1 的实时通信服务器2005中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-556">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-557">msRTCSIP-OriginatorSID</span><span class="sxs-lookup"><span data-stu-id="83990-557">msRTCSIP-OriginatorSID</span></span></p></td>
<td><p><span data-ttu-id="83990-558">当从 Windows NT 服务器主体帐户中的用户的 ObjectSID 复制到资源或中央林中的相应用户或联系人对象的此属性时，在资源和中央林拓扑中使用此属性可启用单一登录。</span><span class="sxs-lookup"><span data-stu-id="83990-558">This attribute is used in resource and central forest topologies to enable single sign-on when a user’s ObjectSID from the Windows NT Server principal account is copied into this attribute of the corresponding user or contact object in the resource or central forest.</span></span> <span data-ttu-id="83990-559">Communicator Web Access 使用此属性或用户的 ObjectSID 在 AD DS 中搜索用户。</span><span class="sxs-lookup"><span data-stu-id="83990-559">Communicator Web Access searches for a user in AD DS using this attribute or the user’s ObjectSID.</span></span> <span data-ttu-id="83990-560">此属性标记为 "全局编录复制"。</span><span class="sxs-lookup"><span data-stu-id="83990-560">This attribute is marked for global catalog replication.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-561">msRTCSIP-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="83990-561">msRTCSIP-OwnerUrn</span></span></p></td>
<td><p><span data-ttu-id="83990-562">此属性是应用程序联系人所有者 (URN) 的统一资源名称。</span><span class="sxs-lookup"><span data-stu-id="83990-562">This attribute is the Uniform Resource Name (URN) of the owner for an application contact.</span></span></p></td>
<td><p><span data-ttu-id="83990-563">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-563">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-564">msRTCSIP 模式 (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-564">msRTCSIP-Pattern (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-565">此单值字符串属性包含用于将拨号号码匹配到164格式的模式。</span><span class="sxs-lookup"><span data-stu-id="83990-565">This single-valued string attribute contains a pattern used for matching dial numbers into E.164 format.</span></span> <span data-ttu-id="83990-566">如果拨号号码与此模式匹配，则转换将应用于已拨号码。</span><span class="sxs-lookup"><span data-stu-id="83990-566">If the dial number matches this pattern, the translation is applied to the dialed number.</span></span></p></td>
<td><p><span data-ttu-id="83990-567">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-567">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-568">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-568">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-569">msRTCSIP-PhoneRouteBL (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-569">msRTCSIP-PhoneRouteBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-570">此多值属性包含 (DN) 的电话路由可分辨名称的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-570">This multi-valued attribute contains a list of phone route distinguished names (DN).</span></span> <span data-ttu-id="83990-571">此属性指定指向一个或多个电话路由的反向链接。</span><span class="sxs-lookup"><span data-stu-id="83990-571">This attribute specifies the back link to one or more phone routes.</span></span></p>
<p><span data-ttu-id="83990-572">反向链接： <strong>链接 ID 11033</strong></span><span class="sxs-lookup"><span data-stu-id="83990-572">Back link: <strong>Link ID 11033</strong></span></span></p>
<p><span data-ttu-id="83990-573">此属性对应于 <strong>msRTCSIP-RouteUsageLinks</strong>的前进链接。</span><span class="sxs-lookup"><span data-stu-id="83990-573">This attribute corresponds to the forward link <strong>msRTCSIP-RouteUsageLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-574">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-574">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-575">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-575">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-576">msRTCSIP-PhoneRouteData (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-576">msRTCSIP-PhoneRouteData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-577">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-577">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-578">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-578">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-579">msRTCSIP-PhoneRouteName (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-579">msRTCSIP-PhoneRouteName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-580">此单值 UNICODE 字符串属性指定手机路由的友好名称，以便管理员可以轻松地引用它。</span><span class="sxs-lookup"><span data-stu-id="83990-580">This single valued UNICODE string attribute specifies the friendly name of the phone route, so it can easily be referenced by the administrator.</span></span></p></td>
<td><p><span data-ttu-id="83990-581">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-581">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-582">msRTCSIP-PhoneUsageData (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-582">msRTCSIP-PhoneUsageData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-583">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-583">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-584">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-584">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-585">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-585">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-586">msRTCSIP-PolicyContent (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-586">msRTCSIP-PolicyContent (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-587">此属性是一个单值的 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="83990-587">This attribute is a single-valued Unicode string.</span></span> <span data-ttu-id="83990-588">此字符串属性包含 XML 格式的策略定义。</span><span class="sxs-lookup"><span data-stu-id="83990-588">This string attribute contains the policy definition in XML format.</span></span> <span data-ttu-id="83990-589">XML 架构定义在不同的策略类型中是通用的，对于每个策略类型，仅这些设置是不同的。</span><span class="sxs-lookup"><span data-stu-id="83990-589">The XML schema definition is common across different policy types, only the settings are different for each policy type.</span></span></p>
<p><span data-ttu-id="83990-590"> (XSD) 的 XML 架构定义定义如下：</span><span class="sxs-lookup"><span data-stu-id="83990-590">The XML schema definition (XSD) is defined as follows:</span></span></p>
<pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;xs:schema id=&quot;instance&quot; xmlns=&quot;&quot; xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:msdata=&quot;urn:schemas-microsoft-com:xml-msdata&quot;&gt;
  &lt;xs:element name=&quot;instance&quot; msdata:IsDataSet=&quot;true&quot;&gt;
    &lt;xs:complexType&gt;
      &lt;xs:choice maxOccurs=&quot;unbounded&quot;&gt;
        &lt;xs:element name=&quot;property&quot; nillable=&quot;true&quot;&gt;
          &lt;xs:complexType&gt;
            &lt;xs:simpleContent msdata:ColumnName=&quot;property_Text&quot; msdata:Ordinal=&quot;1&quot;&gt;
              &lt;xs:extension base=&quot;xs:string&quot;&gt;
                &lt;xs:attribute name=&quot;name&quot; type=&quot;xs:string&quot; /&gt;
              &lt;/xs:extension&gt;
            &lt;/xs:simpleContent&gt;
          &lt;/xs:complexType&gt;
        &lt;/xs:element&gt;
      &lt;/xs:choice&gt;
    &lt;/xs:complexType&gt;
  &lt;/xs:element&gt;
&lt;/xs:schema&gt;</code></pre></td>
<td><p><span data-ttu-id="83990-591">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-591">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-592">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-592">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-593">msRTCSIP-PolicyData (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-593">msRTCSIP-PolicyData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-594">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-594">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-595">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-595">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-596">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-596">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-597">msRTCSIP-PolicyType (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-597">msRTCSIP-PolicyType (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-598">此单值 Unicode 字符串属性包含策略类型。</span><span class="sxs-lookup"><span data-stu-id="83990-598">This single-valued Unicode string attribute contains the policy type.</span></span> <span data-ttu-id="83990-599">有效的策略类型如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-599">Valid policy types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-600">符合</span><span class="sxs-lookup"><span data-stu-id="83990-600">meeting</span></span></p></li>
<li><p><span data-ttu-id="83990-601">电话</span><span class="sxs-lookup"><span data-stu-id="83990-601">telephony</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-602">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-602">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-603">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-603">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-604">msRTCSIP-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="83990-604">msRTCSIP-PoolAddress</span></span></p></td>
<td><p><span data-ttu-id="83990-605">此属性指定一个链接，该链接返回到计算机所属的池。</span><span class="sxs-lookup"><span data-stu-id="83990-605">This attribute specifies a link back to the pool to which a computer belongs.</span></span> <span data-ttu-id="83990-606">无论计算机运行的是标准版 Lync Server 还是企业版 Lync Server，均会设置此属性。</span><span class="sxs-lookup"><span data-stu-id="83990-606">This attribute is set regardless of whether the computer is running the Standard Edition or the Enterprise Edition of Lync Server.</span></span> <span data-ttu-id="83990-607">此属性标记为 "全局编录复制"。</span><span class="sxs-lookup"><span data-stu-id="83990-607">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="83990-608">有效的值是池的域名。</span><span class="sxs-lookup"><span data-stu-id="83990-608">The valid value is the domain name of the pool.</span></span></p>
<p><span data-ttu-id="83990-609">转发链接： <strong>链接 ID 11022</strong></span><span class="sxs-lookup"><span data-stu-id="83990-609">Forward link: <strong>Link ID 11022</strong></span></span></p>
<p><span data-ttu-id="83990-610">此前向链接属性的对应反向链接是 <strong>msRTCSIP-FrontEndServers</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-610">The corresponding back link to this forward link attribute is <strong>msRTCSIP-FrontEndServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-611">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-611">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-612">msRTCSIP-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="83990-612">msRTCSIP-PoolAddresses</span></span></p></td>
<td><p><span data-ttu-id="83990-613">这是一个多值属性，其中包含与 MCU 工厂关联的池 (DN) 的名称列表。</span><span class="sxs-lookup"><span data-stu-id="83990-613">This is a multi-valued attribute that contains a list of the distinguished names (DN) of pools with which the MCU factory is associated.</span></span></p>
<p><span data-ttu-id="83990-614">反向链接： <strong>链接 ID 11025</strong></span><span class="sxs-lookup"><span data-stu-id="83990-614">Back link: <strong>Link ID 11025</strong></span></span></p>
<p><span data-ttu-id="83990-615">指向此 back 链接的相应正向链接是 <strong>msRTCSIP-MCUFactoryPath</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-615">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryPath</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-616">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-616">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-617">msRTCSIP-PoolData</span><span class="sxs-lookup"><span data-stu-id="83990-617">msRTCSIP-PoolData</span></span></p></td>
<td><p><span data-ttu-id="83990-618">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-618">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-619">SP1 的实时通信服务器2005中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-619">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-620">msRTCSIP-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="83990-620">msRTCSIP-PoolDisplayName</span></span></p></td>
<td><p><span data-ttu-id="83990-621">此属性为管理控制台显示的池指定任意名称。</span><span class="sxs-lookup"><span data-stu-id="83990-621">This attribute specifies an arbitrary name for a pool that is displayed by the management console.</span></span> <span data-ttu-id="83990-622">管理员可以更改此名称。</span><span class="sxs-lookup"><span data-stu-id="83990-622">This name can be changed by the administrator.</span></span></p>
<p><span data-ttu-id="83990-623">有效值是表示池名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="83990-623">The valid value is a string representing the name of a pool.</span></span></p></td>
<td><p><span data-ttu-id="83990-624">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-624">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-625">msRTCSIP-PoolDomainFQDN</span><span class="sxs-lookup"><span data-stu-id="83990-625">msRTCSIP-PoolDomainFQDN</span></span></p></td>
<td><p><span data-ttu-id="83990-626">此属性是单值字符串值。</span><span class="sxs-lookup"><span data-stu-id="83990-626">This attribute is a single-valued string value.</span></span> <span data-ttu-id="83990-627">此属性的值（当存在时）表示池的域 FQDN （如果管理员希望使用不符合在其中创建前端池的 Active Directory 域结构的 FQDN 创建前端池） (例如，SIP 命名空间从域名系统中脱离 (DNS) namespace) 。</span><span class="sxs-lookup"><span data-stu-id="83990-627">The value of this attribute, when present, represents the pool’s domain FQDN if the administrator wants to create a Front End pool with an FQDN that does not conform to the Active Directory domain structure in which the Front End pool is created (for example, a SIP namespace disjoined from Domain Name System (DNS) namespace).</span></span></p>
<p><span data-ttu-id="83990-628">我们建议你将前端池域 FQDN 映射到域名部分，作为池所在的 Active Directory 域。</span><span class="sxs-lookup"><span data-stu-id="83990-628">We recommend that you map the Front End pool domain FQDN to the domain name portion as the Active Directory domain in which the pool resides.</span></span> <span data-ttu-id="83990-629">因此，当此属性中不存在值时，前端池 FQDN 将默认为 Active Directory 域名结构，由 <strong>dnsHostName</strong> 属性表示。</span><span class="sxs-lookup"><span data-stu-id="83990-629">Therefore, when no value is present in this attribute, the Front End pool FQDN will default to the Active Directory domain name structure, as denoted by the <strong>dnsHostName</strong> attribute.</span></span></p></td>
<td><p><span data-ttu-id="83990-630">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-630">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-631">msRTCSIP-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="83990-631">msRTCSIP-PoolFunctionality</span></span></p></td>
<td><p><span data-ttu-id="83990-632">与池关联的所有 Lync Server、企业版服务器的域名的多值列表。</span><span class="sxs-lookup"><span data-stu-id="83990-632">A multi-valued list of the domain names of all Lync Server, Enterprise Edition servers associated with a pool.</span></span> <span data-ttu-id="83990-633">Type integer 的此属性定义池是否支持即时消息 (IM) 和状态以及会议。</span><span class="sxs-lookup"><span data-stu-id="83990-633">This attribute of type integer defines whether the pool is capable of instant messaging (IM) and presence, and meetings.</span></span></p>
<p><span data-ttu-id="83990-634">可能有效的值类型如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-634">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-635">未定义：即时消息和状态服务 (Live 通信服务器2005和 2003) </span><span class="sxs-lookup"><span data-stu-id="83990-635">Undefined: IM and Presence Service (Live Communications Server 2005 and 2003)</span></span></p></li>
<li><p><span data-ttu-id="83990-636">1： IM 和联机状态服务 (Lync Server) </span><span class="sxs-lookup"><span data-stu-id="83990-636">1: IM and Presence Service (Lync Server)</span></span></p></li>
<li><p><span data-ttu-id="83990-637">2： (Lync Server) 的 IM 和状态和会议服务</span><span class="sxs-lookup"><span data-stu-id="83990-637">2: IM and Presence and Meeting Service (Lync Server)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-638">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-638">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-639">msRTCSIP-PoolType</span><span class="sxs-lookup"><span data-stu-id="83990-639">msRTCSIP-PoolType</span></span></p></td>
<td><p><span data-ttu-id="83990-640">此属性指定服务器池是否正在运行标准版服务器或企业版服务器。</span><span class="sxs-lookup"><span data-stu-id="83990-640">This attribute specifies whether a server pool is running Standard Edition server or Enterprise Edition server.</span></span> <span data-ttu-id="83990-641">此属性是整数类型的位掩码值。</span><span class="sxs-lookup"><span data-stu-id="83990-641">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="83990-642">每个选项表示一个位。</span><span class="sxs-lookup"><span data-stu-id="83990-642">Each option is represented by a bit.</span></span></p>
<p><span data-ttu-id="83990-643">有效值 (和关联位位置) 如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-643">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-644">1：标准版服务器，托管用户 (位位置 0) </span><span class="sxs-lookup"><span data-stu-id="83990-644">1: Standard Edition server, hosts users (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="83990-645">2：企业版服务器，托管用户 (位位置 1) </span><span class="sxs-lookup"><span data-stu-id="83990-645">2: Enterprise Edition server, hosts users (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="83990-646">4：标准版服务器，托管应用程序 (位位置 2) </span><span class="sxs-lookup"><span data-stu-id="83990-646">4: Standard Edition server, hosts applications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="83990-647">8：企业版服务器，托管应用程序 (位位置 3) </span><span class="sxs-lookup"><span data-stu-id="83990-647">8: Enterprise Edition server, hosts applications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="83990-648">由于 Lync Server 不支持仅托管应用程序的池，因此唯一有效的值如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-648">Because Lync Server does not support pools that host only applications, the only valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-649">5：标准版服务器、托管用户和应用程序 (位位置0和 2) </span><span class="sxs-lookup"><span data-stu-id="83990-649">5: Standard Edition server, hosts users and applications (bit positions 0 and 2)</span></span></p></li>
<li><p><span data-ttu-id="83990-650">10：企业版服务器、托管用户和应用程序 (位位置1和 3) </span><span class="sxs-lookup"><span data-stu-id="83990-650">10: Enterprise Edition server, hosts users and applications (bit positions 1 and 3)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-651">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-651">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-652">msRTCSIP-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="83990-652">msRTCSIP-PoolVersion</span></span></p></td>
<td><p><span data-ttu-id="83990-653">此属性定义池版本。</span><span class="sxs-lookup"><span data-stu-id="83990-653">This attribute defines the pool version.</span></span> <span data-ttu-id="83990-654">它是一种与每个主要产品发布递增的整数类型。</span><span class="sxs-lookup"><span data-stu-id="83990-654">It is an integer type that is incremented with each major product release.</span></span></p>
<p><span data-ttu-id="83990-655">可能有效的值类型如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-655">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-656">0：实时通信服务器2003</span><span class="sxs-lookup"><span data-stu-id="83990-656">0: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="83990-657">1：实时通信服务器2005</span><span class="sxs-lookup"><span data-stu-id="83990-657">1: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="83990-658">2：实时通信服务器2005与 SP1</span><span class="sxs-lookup"><span data-stu-id="83990-658">2: Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="83990-659">3： Office 通信服务器2007</span><span class="sxs-lookup"><span data-stu-id="83990-659">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="83990-660">4： Office 通信服务器 2007 R2</span><span class="sxs-lookup"><span data-stu-id="83990-660">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="83990-661">5： Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="83990-661">5: Lync Server 2010</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-662">带有 SP1 的实时通信服务器2005。</span><span class="sxs-lookup"><span data-stu-id="83990-662">Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-663">msRTCSIP-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="83990-663">msRTCSIP-PresenceFlags</span></span></p></td>
<td><p><span data-ttu-id="83990-664">此属性包含用于定义联机状态设置的选项和标志。</span><span class="sxs-lookup"><span data-stu-id="83990-664">This attribute contains options and flags that define presence settings.</span></span></p></td>
<td><p><span data-ttu-id="83990-665">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-665">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-666">msRTCSIP-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="83990-666">msRTCSIP-PresencePolicy</span></span></p></td>
<td><p><span data-ttu-id="83990-667">此属性包含状态策略对象的 DN。</span><span class="sxs-lookup"><span data-stu-id="83990-667">This attribute contains the DN for a presence policy object.</span></span></p></td>
<td><p><span data-ttu-id="83990-668">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-668">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-669">msRTCSIP-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="83990-669">msRTCSIP-PrimaryHomeServer</span></span></p></td>
<td><p><span data-ttu-id="83990-670">此属性启用 SIP 消息的用户或联系人。</span><span class="sxs-lookup"><span data-stu-id="83990-670">This attribute enables a user or contact for SIP messaging.</span></span> <span data-ttu-id="83990-671">它将添加到 contact 类，因为在中央林拓扑中，联系人对象（而不是用户对象）已启用 SIP。</span><span class="sxs-lookup"><span data-stu-id="83990-671">It is added to the contact class because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="83990-672">有效值是用户托管的标准版服务器或企业版前端池的 DN。</span><span class="sxs-lookup"><span data-stu-id="83990-672">The valid value is the DN of the Standard Edition server or Enterprise Edition Front End pool where a user is homed.</span></span></p></td>
<td><p><span data-ttu-id="83990-673">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-673">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-674">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="83990-674">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="83990-675">此属性包含给定用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="83990-675">This attribute contains the SIP address of a given user.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-676">msRTCSIP-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="83990-676">msRTCSIP-PrivateLine</span></span></p></td>
<td><p><span data-ttu-id="83990-677">此属性包含专用线路设备的设备 ID。</span><span class="sxs-lookup"><span data-stu-id="83990-677">This attribute contains the device ID of the private line device.</span></span></p></td>
<td><p><span data-ttu-id="83990-678">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-678">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-679">msRTCSIP-可路由</span><span class="sxs-lookup"><span data-stu-id="83990-679">msRTCSIP-Routable</span></span></p></td>
<td><p><span data-ttu-id="83990-680">此属性是一个布尔属性，用于确定是否授权 Lync 服务器使用其 GRUU 地址路由到此服务。</span><span class="sxs-lookup"><span data-stu-id="83990-680">This attribute is a Boolean attribute used to determine whether Lync Server is authorized to route to this service using its GRUU address.</span></span> <span data-ttu-id="83990-681">如果此值设置为 <strong>TRUE</strong>，则 Lync Server 有权路由到此服务。</span><span class="sxs-lookup"><span data-stu-id="83990-681">If this value is set to <strong>TRUE</strong>, Lync Server is authorized to route to this service.</span></span> <span data-ttu-id="83990-682">如果此值设置为 <strong>FALSE</strong>，则 Lync Server 无权路由到此服务。</span><span class="sxs-lookup"><span data-stu-id="83990-682">If this value is set to <strong>FALSE</strong>, Lync Server is not authorized to route to this service.</span></span></p></td>
<td><p><span data-ttu-id="83990-683">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-683">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-684">msRTCSIP-RouteUsageAttribute (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-684">msRTCSIP-RouteUsageAttribute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-685">此单值 UNICODE 字符串属性定义了限定手机路由使用的属性。</span><span class="sxs-lookup"><span data-stu-id="83990-685">This single-valued UNICODE string attribute defines an attribute that qualifies the usage for a phone route.</span></span> <span data-ttu-id="83990-686">根据两个元素确定手机路线的选择：分配给电话路线的使用属性和呼叫者允许的策略使用情况属性。</span><span class="sxs-lookup"><span data-stu-id="83990-686">Selection of a phone route is determined based on two elements: the usage attribute assigned to the phone route and the caller’s allowed policy usage attributes.</span></span> <span data-ttu-id="83990-687">已选中与呼叫者允许的使用相匹配的第一条电话路由和使用情况属性。</span><span class="sxs-lookup"><span data-stu-id="83990-687">The first phone route with a usage attribute that matches the caller’s allowed usage is selected.</span></span></p></td>
<td><p><span data-ttu-id="83990-688">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-688">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-689">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-689">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-690">msRTCSIP-RouteUsageLinks (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-690">msRTCSIP-RouteUsageLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-691"> (DN) 属性的多值可分辨名称包含路由使用可分辨名称的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-691">This multi-valued distinguished name (DN) attribute contains a list of route usage distinguished names.</span></span></p>
<p><span data-ttu-id="83990-692">转发链接： <strong>链接 ID 11032</strong></span><span class="sxs-lookup"><span data-stu-id="83990-692">Forward link: <strong>Link ID 11032</strong></span></span></p>
<p><span data-ttu-id="83990-693">此属性是指向对应的 back link <strong>msRTCSIP-PhoneRouteBL</strong>的前向链接。</span><span class="sxs-lookup"><span data-stu-id="83990-693">This attribute is a forward link to the corresponding back link <strong>msRTCSIP-PhoneRouteBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-694">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-694">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-695">msRTCSIP-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="83990-695">msRTCSIP-RoutingPoolDN</span></span></p></td>
<td><p><span data-ttu-id="83990-696">此属性包含指向所有寻址到此 MCU 或受信任服务的 SIP 流量必须经过的池的 DN。</span><span class="sxs-lookup"><span data-stu-id="83990-696">This attribute contains the DN that points to the pool that all SIP traffic addressed to this MCU or Trusted Service must go through.</span></span></p></td>
<td><p><span data-ttu-id="83990-697">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-697">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-698">msRTCSIP-RuleName (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-698">msRTCSIP-RuleName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-699">此单值 UNICODE 字符串属性指定规范化规则的友好名称，因此它可以由管理员轻松引用。</span><span class="sxs-lookup"><span data-stu-id="83990-699">This single-valued UNICODE string attribute specifies the friendly name of the normalization rule, so it can easily be referenced by an administrator.</span></span></p></td>
<td><p><span data-ttu-id="83990-700">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-700">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-701">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-701">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-702">msRTCSIP-SchemaVersion</span><span class="sxs-lookup"><span data-stu-id="83990-702">msRTCSIP-SchemaVersion</span></span></p></td>
<td><p><span data-ttu-id="83990-703">此属性表示组织中当前部署的架构版本。</span><span class="sxs-lookup"><span data-stu-id="83990-703">This attribute represents the schema version currently deployed in the organization.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-704">msRTCSIP-SearchMaxRequests (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-704">msRTCSIP-SearchMaxRequests (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-705">此属性限制当用户使用 Communicator 搜索联系人时，将从目录搜索返回的搜索结果的数量。</span><span class="sxs-lookup"><span data-stu-id="83990-705">This attribute limits the number of search results to be returned from a directory search when a user searches for a contact using Communicator.</span></span> <span data-ttu-id="83990-706">此属性将替代客户端提供的值。</span><span class="sxs-lookup"><span data-stu-id="83990-706">This attribute will override the value provided by the client.</span></span></p></td>
<td><p><span data-ttu-id="83990-707">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-707">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-708">msRTCSIP-SearchMaxResults (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-708">msRTCSIP-SearchMaxResults (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-709">此属性限制返回的搜索请求数。</span><span class="sxs-lookup"><span data-stu-id="83990-709">This attribute limits the number of search requests returned.</span></span></p></td>
<td><p><span data-ttu-id="83990-710">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-710">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-711">msRTCSIP-ServerBL</span><span class="sxs-lookup"><span data-stu-id="83990-711">msRTCSIP-ServerBL</span></span></p></td>
<td><p><span data-ttu-id="83990-712">此多值属性是一个 back 链接，其中包含 (DN) 的可分辨名称的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-712">This multi-valued attribute is a back link that contains a list of distinguished names (DN).</span></span> <span data-ttu-id="83990-713">这些 DNs 指向一个 pool 或 <strong>TrustedService</strong> 对象。</span><span class="sxs-lookup"><span data-stu-id="83990-713">These DNs point to a pool or <strong>TrustedService</strong> object.</span></span></p>
<p><span data-ttu-id="83990-714">此属性对应于 <strong>msRTCSIP-TrustedServiceLinks</strong>的前进链接。</span><span class="sxs-lookup"><span data-stu-id="83990-714">This attribute corresponds to the forward link <strong>msRTCSIP-TrustedServiceLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-715">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-715">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-716">msRTCSIP-ServerData</span><span class="sxs-lookup"><span data-stu-id="83990-716">msRTCSIP-ServerData</span></span></p></td>
<td><p><span data-ttu-id="83990-717">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-717">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-718">msRTCSIP-ServerReferenceBL (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-718">msRTCSIP-ServerReferenceBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-719">此多值属性包含一个可分辨名称的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-719">This multi-valued attribute contains a list of distinguished names.</span></span> <span data-ttu-id="83990-720">这些可分辨名称是反向链接，这些链接引用可以为其分配默认位置配置文件的其他服务器对象。</span><span class="sxs-lookup"><span data-stu-id="83990-720">These distinguished names are back links that reference other server objects that can be assigned a default location profile.</span></span></p>
<p><span data-ttu-id="83990-721">反向链接： <strong>链接 ID 11037</strong></span><span class="sxs-lookup"><span data-stu-id="83990-721">Back link: <strong>Link ID 11037</strong></span></span></p>
<p><span data-ttu-id="83990-722">指向此 back 链接的相应正向链接是 <strong>msRTCSIP-DefaultLocationProfileLink</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-722">The corresponding forward link to this back link is <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span></span></p>
<p><span data-ttu-id="83990-723">此 back link 属性仅引用池和中介服务器。</span><span class="sxs-lookup"><span data-stu-id="83990-723">This back link attribute references pools and Mediation Servers only.</span></span></p></td>
<td><p><span data-ttu-id="83990-724">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-724">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-725">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-725">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-726">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="83990-726">msRTCSIP-ServerVersion</span></span></p></td>
<td><p><span data-ttu-id="83990-727">此属性定义服务器的版本信息。</span><span class="sxs-lookup"><span data-stu-id="83990-727">This attribute defines the version information of the server.</span></span> <span data-ttu-id="83990-728">此版本号适用于所有服务器角色。</span><span class="sxs-lookup"><span data-stu-id="83990-728">This version number applies to all server roles.</span></span> <span data-ttu-id="83990-729">这是一个 monotonously 增加的整数，每个官方产品版本增加。</span><span class="sxs-lookup"><span data-stu-id="83990-729">It is a monotonously increasing integer that increments with each official product release.</span></span></p>
<p><span data-ttu-id="83990-730">可能的有效值如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-730">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-731">未定义：实时通信服务器2003</span><span class="sxs-lookup"><span data-stu-id="83990-731">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="83990-732">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="83990-732">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="83990-733">Live Communications Server 2005 SP1</span><span class="sxs-lookup"><span data-stu-id="83990-733">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="83990-734">3： Office 通信服务器2007</span><span class="sxs-lookup"><span data-stu-id="83990-734">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="83990-735">4： Office 通信服务器 2007 R2</span><span class="sxs-lookup"><span data-stu-id="83990-735">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="83990-736">5： Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="83990-736">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="83990-737">6： Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83990-737">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-738">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-738">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-739">msRTCSIP-SourceObjectType</span><span class="sxs-lookup"><span data-stu-id="83990-739">msRTCSIP-SourceObjectType</span></span></p></td>
<td><p><span data-ttu-id="83990-740">Integer 类型的此单值属性指定 <strong>SourceObjectDN</strong> 指向的对象的类型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-740">This single-valued attribute of integer type specifies the type of object the <strong>msDS-SourceObjectDN</strong> points to, as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-741">null |0x00000001：表示来自不同林中的 Windows NT 服务器主体用户对象</span><span class="sxs-lookup"><span data-stu-id="83990-741">null | 0x00000001: Represents a Windows NT Server principal user object from a different forest</span></span></p></li>
<li><p><span data-ttu-id="83990-742">以下属性表示通讯组扩展来自不同林中的组类型：</span><span class="sxs-lookup"><span data-stu-id="83990-742">The following attributes represent a group type from a different forest for distribution group expansion:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-743">0x00000002： ADS_GROUP_TYPE_GLOBAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="83990-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="83990-744">0x00000004： ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="83990-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="83990-745">0x00000004： ADS_GROUP_TYPE_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="83990-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="83990-746">0x00000008： ADS_GROUP_TYPE_UNIVERSAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="83990-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="83990-747">0x80000000： ADS_GROUP_TYPE_SECURITY_ENABLED</span><span class="sxs-lookup"><span data-stu-id="83990-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span></span></p></li>
<li><p><span data-ttu-id="83990-748">0x90000000：表示来自同一林或不同林中的自动助理或订阅者访问对象</span><span class="sxs-lookup"><span data-stu-id="83990-748">0x90000000: Represents an Auto-Attendant or subscriber access object from the same forest or a different forest</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="83990-749">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-749">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-750">msRTCSIP-SubscriptionAuthRequired (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-750">msRTCSIP-SubscriptionAuthRequired (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-751">实时通信服务器2003中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-751">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="83990-752">在实时通信服务器2005中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-752">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-753">msRTCSIP-TargetHomeServer</span><span class="sxs-lookup"><span data-stu-id="83990-753">msRTCSIP-TargetHomeServer</span></span></p></td>
<td><p><span data-ttu-id="83990-754">此属性使你能够将用户或联系人对象从一个 Lync 服务器池移动到另一个。</span><span class="sxs-lookup"><span data-stu-id="83990-754">This attribute enables you to move a user or contact object from one Lync Server pool to another.</span></span> <span data-ttu-id="83990-755">此属性将添加到 contact 类，因为在中央林拓扑中，联系人对象（而不是用户对象）已启用 SIP。</span><span class="sxs-lookup"><span data-stu-id="83990-755">This attribute is added to the contact class, because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="83990-756">有效值是要将用户移动到的目标标准版服务器或前端池的 DN。</span><span class="sxs-lookup"><span data-stu-id="83990-756">The valid value is the DN of the destination Standard Edition server or Front End pool to which a user is to be moved.</span></span></p></td>
<td><p><span data-ttu-id="83990-757">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-757">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-758">msRTCSIP-TargetPhoneNumber (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-758">msRTCSIP-TargetPhoneNumber (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-759">此单值字符串属性包含用于路由到在 <strong>msRTCSIP-网关</strong>定义的指定网关的电话号码模式或范围。</span><span class="sxs-lookup"><span data-stu-id="83990-759">This single-valued string attribute contains a phone number pattern or range to route to the specified gateways defined in <strong>msRTCSIP-Gateways</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-760">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-760">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-761">msRTCSIP-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="83990-761">msRTCSIP-TargetUserPolicies</span></span></p></td>
<td><p><span data-ttu-id="83990-762">此属性存储 Lync Server 用户的目标策略的名称/值对。</span><span class="sxs-lookup"><span data-stu-id="83990-762">This attribute stores name-value pairs for target policies for Lync Server users.</span></span></p></td>
<td><p><span data-ttu-id="83990-763">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-763">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-764">msRTCSIP-TenantId</span><span class="sxs-lookup"><span data-stu-id="83990-764">msRTCSIP-TenantId</span></span></p></td>
<td><p><span data-ttu-id="83990-765">此属性存储租户的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="83990-765">This attribute stores the unique identifier for a tenant.</span></span></p></td>
<td><p><span data-ttu-id="83990-766">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-766">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-767">msRTCSIP-翻译 (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-767">msRTCSIP-Translation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-768">此属性由 Lync Server 的语音功能使用，并且包含要在已拨号码上应用的翻译字符串（如果找到匹配项）。</span><span class="sxs-lookup"><span data-stu-id="83990-768">This attribute is used by the voice feature of Lync Server and contains the translation string to apply on the dialed number, if a match is found.</span></span></p></td>
<td><p><span data-ttu-id="83990-769">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-769">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="83990-770">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-770">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-771">msRTCSIP-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="83990-771">msRTCSIP-TrustedMCUData</span></span></p></td>
<td><p><span data-ttu-id="83990-772">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-772">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-773">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-773">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-774">msRTCSIP-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="83990-774">msRTCSIP-TrustedMCUFQDN</span></span></p></td>
<td><p><span data-ttu-id="83990-775">此属性是一个字符串值，其中包含 MCU 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83990-775">This attribute is a string value that contains the FQDN of the MCU.</span></span> <span data-ttu-id="83990-776">这是单值属性。</span><span class="sxs-lookup"><span data-stu-id="83990-776">This is a single-valued attribute.</span></span> <span data-ttu-id="83990-777">每个段的有效值为63个字符;整个 FQDN 的有效值为255个字符。</span><span class="sxs-lookup"><span data-stu-id="83990-777">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="83990-778">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-778">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-779">msRTCSIP-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="83990-779">msRTCSIP-TrustedProxyData</span></span></p></td>
<td><p><span data-ttu-id="83990-780">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-780">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-781">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-781">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-782">msRTCSIP-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="83990-782">msRTCSIP-TrustedProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="83990-783">此属性是一个字符串值，其中包含运行代理服务器的服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83990-783">This attribute is a string value that contains the FQDN of the server running Proxy Server.</span></span> <span data-ttu-id="83990-784">此属性是单值的。</span><span class="sxs-lookup"><span data-stu-id="83990-784">This attribute is single-valued.</span></span> <span data-ttu-id="83990-785">每个段的有效值为63个字符;整个 FQDN 的有效值为255个字符。</span><span class="sxs-lookup"><span data-stu-id="83990-785">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="83990-786">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-786">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-787">msRTCSIP-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="83990-787">msRTCSIP-TrustedServerData</span></span></p></td>
<td><p><span data-ttu-id="83990-788">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-788">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-789">msRTCSIP-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="83990-789">msRTCSIP-TrustedServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="83990-790">此属性是一个单值属性，表示受信任服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83990-790">This attribute is a single-valued attribute that represents the FQDN of a trusted server.</span></span></p></td>
<td><p><span data-ttu-id="83990-791">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-791">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-792">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="83990-792">msRTCSIP-TrustedServerVersion</span></span></p></td>
<td><p><span data-ttu-id="83990-793">此属性指定受信任服务器列表中服务器的版本号。</span><span class="sxs-lookup"><span data-stu-id="83990-793">This attribute specifies the version number of a server in the trusted server list.</span></span></p>
<p><span data-ttu-id="83990-794">可能的有效值如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-794">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-795">NULL：实时通信服务器2003</span><span class="sxs-lookup"><span data-stu-id="83990-795">NULL: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="83990-796">2：实时通信服务器2005</span><span class="sxs-lookup"><span data-stu-id="83990-796">2: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="83990-797">3： Office 通信服务器2007</span><span class="sxs-lookup"><span data-stu-id="83990-797">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="83990-798">4： Office 通信服务器 2007 R2</span><span class="sxs-lookup"><span data-stu-id="83990-798">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="83990-799">5： Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="83990-799">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="83990-800">6： Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83990-800">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-801">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-801">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-802">msRTCSIP-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="83990-802">msRTCSIP-TrustedServiceFlags</span></span></p></td>
<td><p><span data-ttu-id="83990-803">此属性定义为受信任的服务启用的选项。</span><span class="sxs-lookup"><span data-stu-id="83990-803">This attribute defines the options that are enabled for the trusted service.</span></span></p></td>
<td><p><span data-ttu-id="83990-804">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-804">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-805">msRTCSIP-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="83990-805">msRTCSIP-TrustedServiceLinks</span></span></p></td>
<td><p><span data-ttu-id="83990-806">此多值属性包含引用受信任服务对象（如媒体中继身份验证服务） (DN) 的可分辨名称列表。</span><span class="sxs-lookup"><span data-stu-id="83990-806">This multi-valued attribute contains a list of distinguished names (DN) that reference a trusted service object, such as a Media Relay Authentication Service.</span></span> <span data-ttu-id="83990-807">媒体中继身份验证服务 (在运行 A/V 会议服务的边缘服务器上物理 collocated，) 必须与池相关联才能支持远程用户的音频方案。</span><span class="sxs-lookup"><span data-stu-id="83990-807">A Media Relay Authentication Service (physically collocated on the Edge Server running the A/V Conferencing service) must be associated with a pool to support audio scenarios for remote users.</span></span></p>
<p><span data-ttu-id="83990-808">此前向链接属性的对应反向链接是 <strong>msRTCSIP-ServerBL</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-808">The corresponding back link to this forward link attribute is <strong>msRTCSIP-ServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-809">跨度</span><span class="sxs-lookup"><span data-stu-id="83990-809">UC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-810">msRTCSIP-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="83990-810">msRTCSIP-TrustedServicePort</span></span></p></td>
<td><p><span data-ttu-id="83990-811">此属性是一个整数，用于定义用于连接到此 GRUU 服务的端口号。</span><span class="sxs-lookup"><span data-stu-id="83990-811">This attribute is an integer that defines the port number used to connect to this GRUU service.</span></span></p></td>
<td><p><span data-ttu-id="83990-812">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-812">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-813">msRTCSIP-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="83990-813">msRTCSIP-TrustedServiceType</span></span></p></td>
<td><p><span data-ttu-id="83990-814">此属性是一个字符串值，用于定义它所表示的 GRUU 服务的类型。</span><span class="sxs-lookup"><span data-stu-id="83990-814">This attribute is a string value that defines the type of GRUU service it represents.</span></span></p>
<p><span data-ttu-id="83990-815">有效的 GRUU 服务类型如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-815">The valid GRUU service types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-816">MediationServer</span><span class="sxs-lookup"><span data-stu-id="83990-816">MediationServer</span></span></p></li>
<li><p><span data-ttu-id="83990-817">网关</span><span class="sxs-lookup"><span data-stu-id="83990-817">Gateway</span></span></p></li>
<li><p><span data-ttu-id="83990-818">媒体中继身份验证服务 (MRAS) </span><span class="sxs-lookup"><span data-stu-id="83990-818">Media Relay Authentication Service (MRAS)</span></span></p></li>
<li><p><span data-ttu-id="83990-819">QoSM</span><span class="sxs-lookup"><span data-stu-id="83990-819">QoSM</span></span></p></li>
<li><p><span data-ttu-id="83990-820">msRTCSIP-UserExtension CWA</span><span class="sxs-lookup"><span data-stu-id="83990-820">msRTCSIP-UserExtension CWA</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-821">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-821">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-822">msRTCSIP-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="83990-822">msRTCSIP-TrustedWebComponentsServerData</span></span></p></td>
<td><p><span data-ttu-id="83990-823">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-823">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-824">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-824">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-825">msRTCSIP-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="83990-825">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="83990-826">此属性是一个字符串值，其中包含运行 Lync Server Web 服务的 IIS 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83990-826">This attribute is a string value that contains the FQDN of the IIS running Lync Server Web Services.</span></span> <span data-ttu-id="83990-827">这是单值属性。</span><span class="sxs-lookup"><span data-stu-id="83990-827">This is a single-valued attribute.</span></span> <span data-ttu-id="83990-828">每个段的有效值为63个字符;整个 FQDN 的有效值为255个字符。</span><span class="sxs-lookup"><span data-stu-id="83990-828">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="83990-829">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-829">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-830">msRTCSIP-UCFlags (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-830">msRTCSIP-UCFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-831">此属性定义对所有用户或联系人对象全局启用的不同 UC 选项。</span><span class="sxs-lookup"><span data-stu-id="83990-831">This attribute defines different UC options that are enabled globally to all user or contact objects.</span></span> <span data-ttu-id="83990-832">此属性是整数类型的位掩码值。</span><span class="sxs-lookup"><span data-stu-id="83990-832">This attribute is a bit-mask value of integer type.</span></span> <span data-ttu-id="83990-833">每个选项都由存在一个位表示。</span><span class="sxs-lookup"><span data-stu-id="83990-833">Each option is represented by the presence of a bit.</span></span></p>
<p><span data-ttu-id="83990-834">可能有效的值 (和关联的位位置) 如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-834">The possible valid value (and associated bit position) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-835">4： UsePerUserUCPolicy (位位置 2) </span><span class="sxs-lookup"><span data-stu-id="83990-835">4: UsePerUserUCPolicy (bit position 2)</span></span></p></li>
</ul>
<p><span data-ttu-id="83990-836">设置此位时，UC 策略按用户定义。</span><span class="sxs-lookup"><span data-stu-id="83990-836">When this bit is set, the UC policy is defined per user.</span></span></p></td>
<td><p><span data-ttu-id="83990-837">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-837">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-838">msRTCSIP-UCPolicy (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-838">msRTCSIP-UCPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-839">此单值属性包含管理员为该用户分配的 UC 策略 (DN) 的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="83990-839">This single-valued attribute contains the distinguished name (DN) of the UC policy that the administrator has assigned for this user.</span></span></p></td>
<td><p><span data-ttu-id="83990-840">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-840">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-841">msRTCSIP-UserDomainList (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-841">msRTCSIP-UserDomainList (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="83990-842">此属性提供林中托管启用了 SIP 的用户的所有域的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-842">This attribute provides a list of all the domains in a forest that host SIP-enabled users.</span></span> <span data-ttu-id="83990-843">默认值为空列表，表示林中的所有域均为 SIP 启用。</span><span class="sxs-lookup"><span data-stu-id="83990-843">The default is an empty list, indicating that all domains in the forest are SIP-enabled.</span></span></p>
<p><span data-ttu-id="83990-844">有效值是表示单个域的域名的多个字符串。</span><span class="sxs-lookup"><span data-stu-id="83990-844">Valid values are multiple strings representing the domain names of individual domains.</span></span></p></td>
<td><p><span data-ttu-id="83990-845">实时通信服务器2005中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-845">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="83990-846">在 Lync Server 2010 中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-846">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-847">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="83990-847">msRTCSIP-UserEnabled</span></span></p></td>
<td><p><span data-ttu-id="83990-848">此属性确定用户当前是否已启用 Lync Server。</span><span class="sxs-lookup"><span data-stu-id="83990-848">This attribute determines whether the user is currently enabled for Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-849">msRTCSIP-UserExtension</span><span class="sxs-lookup"><span data-stu-id="83990-849">msRTCSIP-UserExtension</span></span></p></td>
<td><p><span data-ttu-id="83990-850">此多值属性包含名称 = 值格式的名称值对列表 &quot; 。 &quot; 此属性标记为 "全局编录复制"。</span><span class="sxs-lookup"><span data-stu-id="83990-850">This multi-valued attribute contains a list of name-value pairs in the format of &quot;name=value.&quot; This attribute is marked for global catalog replication.</span></span></p></td>
<td><p><span data-ttu-id="83990-851">SP1 的实时通信服务器2005中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-851">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-852">msRTCSIP-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="83990-852">msRTCSIP-UserLocationProfile</span></span></p></td>
<td><p><span data-ttu-id="83990-853">此属性包含指向位置配置文件对象 (DN) 的识别名。</span><span class="sxs-lookup"><span data-stu-id="83990-853">This attribute contains the distinguished name (DN) that points to a location profile object.</span></span></p></td>
<td><p><span data-ttu-id="83990-854">Office 通信服务器 2007 R2 中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-854">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-855">msRTCSIP-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="83990-855">msRTCSIP-UserPolicies</span></span></p></td>
<td><p><span data-ttu-id="83990-856">此属性存储用户策略的名称/值对。</span><span class="sxs-lookup"><span data-stu-id="83990-856">This attribute stores name-value pairs for user policies.</span></span></p></td>
<td><p><span data-ttu-id="83990-857">Lync Server 2010 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-857">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-858">msRTCSIP-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="83990-858">msRTCSIP-UserPolicy</span></span></p></td>
<td><p><span data-ttu-id="83990-859">这是一个多值属性，其中包含具有二进制 (DN_WITH_BINARY) 指向不同类型的全局用户策略的可分辨名称的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-859">This is a multi-valued attribute containing a list of distinguished names with binary (DN_WITH_BINARY) pointing to global user policies of different types.</span></span> <span data-ttu-id="83990-860">二进制部分指示 DN 部分指向的策略类型。</span><span class="sxs-lookup"><span data-stu-id="83990-860">The binary part indicates the type of policy to which the DN portion points.</span></span></p>
<p><span data-ttu-id="83990-861">有效的二进制值如下所示：</span><span class="sxs-lookup"><span data-stu-id="83990-861">The valid binary values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-862">0x00000001：会议策略</span><span class="sxs-lookup"><span data-stu-id="83990-862">0x00000001: Meeting policy</span></span></p></li>
<li><p><span data-ttu-id="83990-863">0x00000002： UC 策略</span><span class="sxs-lookup"><span data-stu-id="83990-863">0x00000002: UC policy</span></span></p></li>
<li><p><span data-ttu-id="83990-864">0x00000005：状态策略</span><span class="sxs-lookup"><span data-stu-id="83990-864">0x00000005: Presence policy</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-865">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-865">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-866">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="83990-866">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="83990-867">这是 SIP 路由组 ID。</span><span class="sxs-lookup"><span data-stu-id="83990-867">This is the SIP routing group ID.</span></span> <span data-ttu-id="83990-868">同一组中的用户将注册到同一前端服务器。</span><span class="sxs-lookup"><span data-stu-id="83990-868">Users in the same group will register to the same Front End Server.</span></span></p></td>
<td><p><span data-ttu-id="83990-869">Lync Server 2013 中的新增新增服务。</span><span class="sxs-lookup"><span data-stu-id="83990-869">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-870">msRTCSIP-WebComponentsData</span><span class="sxs-lookup"><span data-stu-id="83990-870">msRTCSIP-WebComponentsData</span></span></p></td>
<td><p><span data-ttu-id="83990-871">这是一个多值属性。</span><span class="sxs-lookup"><span data-stu-id="83990-871">This is a multi-valued attribute.</span></span> <span data-ttu-id="83990-872">保留此属性供将来使用。</span><span class="sxs-lookup"><span data-stu-id="83990-872">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="83990-873">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-873">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-874">msRTCSIP-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="83990-874">msRTCSIP-WebComponentsPoolAddress</span></span></p></td>
<td><p><span data-ttu-id="83990-875">此单值属性指向 web 组件所属的池或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="83990-875">This single-valued attribute points to the pool or Standard Edition server to which the web components belong.</span></span></p>
<p><span data-ttu-id="83990-876">转发链接： <strong>链接 ID 11028</strong></span><span class="sxs-lookup"><span data-stu-id="83990-876">Forward link: <strong>Link ID 11028</strong></span></span></p>
<p><span data-ttu-id="83990-877">此前向链接属性的对应反向链接是 <strong>msRTCSIP-WebComponentsServers</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-877">The corresponding back link to this forward link attribute is <strong>msRTCSIP-WebComponentsServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-878">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-878">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-879">msRTCSIP-WebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="83990-879">msRTCSIP-WebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="83990-880">此属性是可分辨名称的多值列表。</span><span class="sxs-lookup"><span data-stu-id="83990-880">This attribute is a multi-valued list of distinguished names.</span></span> <span data-ttu-id="83990-881">此属性包含与此池关联的所有 Web 服务器的列表。</span><span class="sxs-lookup"><span data-stu-id="83990-881">This attribute contains a list of all Web servers associated with this pool.</span></span></p>
<p><span data-ttu-id="83990-882">反向链接： <strong>链接 ID 11029</strong></span><span class="sxs-lookup"><span data-stu-id="83990-882">Back link: <strong>Link ID 11029</strong></span></span></p>
<p><span data-ttu-id="83990-883">指向此 back 链接的相应正向链接是 <strong>msRTCSIP-WebComponentsPoolAddress</strong>。</span><span class="sxs-lookup"><span data-stu-id="83990-883">The corresponding forward link to this back link is <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="83990-884">Office 通信服务器2007中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-884">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-885">msRTCSIP-WMIInstanceId (过时) </span><span class="sxs-lookup"><span data-stu-id="83990-885">msRTCSIP-WMIInstanceId (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="83990-886">实时通信服务器2003中的新增项。</span><span class="sxs-lookup"><span data-stu-id="83990-886">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="83990-887">在实时通信服务器2005中已过时。</span><span class="sxs-lookup"><span data-stu-id="83990-887">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-888">OtherIPPhone</span><span class="sxs-lookup"><span data-stu-id="83990-888">OtherIPPhone</span></span></p></td>
<td><p><span data-ttu-id="83990-889">电话将使用此现有 Active Directory 属性指定手机的备用 TCP/IP 地址列表。</span><span class="sxs-lookup"><span data-stu-id="83990-889">This existing Active Directory attribute is used by telephony to specify the list of alternate TCP/IP addresses for a phone.</span></span></p></td>
<td><p><span data-ttu-id="83990-890">Windows Server 2008 操作系统中的新增操作。</span><span class="sxs-lookup"><span data-stu-id="83990-890">New in Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-891">PhoneOfficeOther</span><span class="sxs-lookup"><span data-stu-id="83990-891">PhoneOfficeOther</span></span></p></td>
<td><p><span data-ttu-id="83990-892">Lync Server 中的语音组件使用此现有 Active Directory 属性，仅适用于联系人对象，目的是将呼叫路由到统一消息自动助理和订阅者访问号码。</span><span class="sxs-lookup"><span data-stu-id="83990-892">This existing Active Directory attribute is used by the voice components in Lync Server, for contact objects only, for the purpose of routing calls to the unified messaging auto-attendant and subscriber access numbers.</span></span> <span data-ttu-id="83990-893">无条件呼叫转发地址存储在此多值属性中。</span><span class="sxs-lookup"><span data-stu-id="83990-893">The unconditional call forwarding address is stored in this multi-valued attribute.</span></span> <span data-ttu-id="83990-894">此帐户是为自动助理和订阅者访问的特定用途而创建的。</span><span class="sxs-lookup"><span data-stu-id="83990-894">This account is created for the specific purpose of auto-attendant and subscriber access.</span></span> <span data-ttu-id="83990-895">管理员不应修改此帐户的属性。</span><span class="sxs-lookup"><span data-stu-id="83990-895">This account’s attributes should not be modified by administrators.</span></span></p></td>
<td><p><span data-ttu-id="83990-896">Windows 2000 操作系统中的新增操作。</span><span class="sxs-lookup"><span data-stu-id="83990-896">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83990-897">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="83990-897">ProxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="83990-898">此现有 Active Directory 多值属性是 Windows 2000 中引入的基本 Active Directory 架构的一部分。</span><span class="sxs-lookup"><span data-stu-id="83990-898">This existing Active Directory multi-valued attribute is part of the base Active Directory schema introduced in Windows 2000.</span></span> <span data-ttu-id="83990-899">此属性包含用户电子邮件的各种 X400、X500 和 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="83990-899">This attribute contains the various X400, X500, and SMTP addresses of the user’s email.</span></span> <span data-ttu-id="83990-900">在实时通信服务器2003和更高版本中，使用 sip：标记将用户的 SIP URI 添加到此列表中 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="83990-900">In Live Communications Server 2003 and later, the user’s SIP URI is added to this list, using the &quot;sip:&quot; tag.</span></span></p>
<p><span data-ttu-id="83990-901">以下应用程序从该属性中搜索用户的 SIP URI：</span><span class="sxs-lookup"><span data-stu-id="83990-901">The following applications search the user’s SIP URI from this attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="83990-902">Microsoft Office Outlook 2003 消息传递和协作客户端</span><span class="sxs-lookup"><span data-stu-id="83990-902">Microsoft Office Outlook 2003 messaging and collaboration client</span></span></p></li>
<li><p><span data-ttu-id="83990-903">Microsoft Office SharePoint Server 2007</span><span class="sxs-lookup"><span data-stu-id="83990-903">Microsoft Office SharePoint Server 2007</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="83990-904">Windows 2000 操作系统中的新增操作。</span><span class="sxs-lookup"><span data-stu-id="83990-904">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83990-905">TelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="83990-905">TelephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="83990-906">此现有 Active Directory 属性包含用户的电话号码。</span><span class="sxs-lookup"><span data-stu-id="83990-906">This existing Active Directory attribute contains the telephone number for the user.</span></span></p></td>
<td><p><span data-ttu-id="83990-907">Windows 2000 操作系统中的新增操作。</span><span class="sxs-lookup"><span data-stu-id="83990-907">New in Windows 2000 operating system.</span></span></p></td>
</tr><span data-ttu-id="83990-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83990-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

