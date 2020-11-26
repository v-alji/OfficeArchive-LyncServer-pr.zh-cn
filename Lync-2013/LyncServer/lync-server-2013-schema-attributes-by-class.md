---
title: Lync Server 2013：按类分类的架构属性
description: Lync Server 2013：按类的架构属性。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes by class
ms:assetid: 72726b43-f1ea-458c-9304-a26e8a12128c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398544(v=OCS.15)
ms:contentKeyID: 48184468
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3cd31e42ce825049903310d6021e13086fe07afd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441989"
---
# <a name="schema-attributes-by-class-in-lync-server-2013"></a><span data-ttu-id="6b85f-103">Lync Server 2013 中按类分类的架构属性</span><span class="sxs-lookup"><span data-stu-id="6b85f-103">Schema attributes by class in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b85f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b85f-104">

<span> </span></span></span>

<span data-ttu-id="6b85f-105">_**主题上次修改时间：** 2012-08-29_</span><span class="sxs-lookup"><span data-stu-id="6b85f-105">_**Topic Last Modified:** 2012-08-29_</span></span>

<span data-ttu-id="6b85f-106">此部分列出了可以包含在每个 Lync Server 2013 类中的架构属性以及可以包含在其他类中的类。</span><span class="sxs-lookup"><span data-stu-id="6b85f-106">This section lists the schema attributes that can be contained in each Lync Server 2013 class and the classes that can be contained in other classes.</span></span> <span data-ttu-id="6b85f-107">有关所有类及其说明的列表，请参阅 [Lync Server 2013 中的架构类和说明](lync-server-2013-schema-classes-and-descriptions.md)。</span><span class="sxs-lookup"><span data-stu-id="6b85f-107">For a list of all the classes and their descriptions, see [Schema classes and descriptions in Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span></span> <span data-ttu-id="6b85f-108">有关所有属性及其说明的列表，请参阅 [Lync Server 2013 中的架构属性和说明](lync-server-2013-schema-attributes-and-descriptions.md)。</span><span class="sxs-lookup"><span data-stu-id="6b85f-108">For a list of all the attributes and their descriptions, see [Schema attributes and descriptions in Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span></span>

<div>

## <a name="attributes-by-class"></a><span data-ttu-id="6b85f-109">按类分类的属性</span><span class="sxs-lookup"><span data-stu-id="6b85f-109">Attributes by Class</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b85f-110">种类</span><span class="sxs-lookup"><span data-stu-id="6b85f-110">Class</span></span></th>
<th><span data-ttu-id="6b85f-111">可能包含这些属性</span><span class="sxs-lookup"><span data-stu-id="6b85f-111">May contain these attributes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-112">联系人</span><span class="sxs-lookup"><span data-stu-id="6b85f-112">Contact</span></span></p></td>
<td><p><span data-ttu-id="6b85f-113">SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-113">msDS-SourceObjectDN</span></span></p>
<p><span data-ttu-id="6b85f-114">msRTCSIP-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="6b85f-114">msRTCSIP-AcpInfo</span></span></p>
<p><span data-ttu-id="6b85f-115">msRTCSIP-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="6b85f-115">msRTCSIP-ApplicationDestination</span></span></p>
<p><span data-ttu-id="6b85f-116">msRTCSIP-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="6b85f-116">msRTCSIP-ApplicationOptions</span></span></p>
<p><span data-ttu-id="6b85f-117">msRTCSIP-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="6b85f-117">msRTCSIP-ApplicationPrimaryLanguage</span></span></p>
<p><span data-ttu-id="6b85f-118">msRTCSIP-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="6b85f-118">msRTCSIP-ApplicationSecondaryLanguages</span></span></p>
<p><span data-ttu-id="6b85f-119">msRTCSIP-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="6b85f-119">msRTCSIP-ArchivingEnabled</span></span></p>
<p><span data-ttu-id="6b85f-120">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="6b85f-120">msRTCSIP-DeploymentLocator</span></span></p>
<p><span data-ttu-id="6b85f-121">msRTCSIP-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="6b85f-121">msRTCSIP-FederationEnabled</span></span></p>
<p><span data-ttu-id="6b85f-122">msRTCSIP-GroupingID</span><span class="sxs-lookup"><span data-stu-id="6b85f-122">msRTCSIP-GroupingID</span></span></p>
<p><span data-ttu-id="6b85f-123">msRTCSIP-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="6b85f-123">msRTCSIP-InternetAccessEnabled</span></span></p>
<p><span data-ttu-id="6b85f-124">msRTCSIP-行</span><span class="sxs-lookup"><span data-stu-id="6b85f-124">msRTCSIP-Line</span></span></p>
<p><span data-ttu-id="6b85f-125">msRTCSIP-LineServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-125">msRTCSIP-LineServer</span></span></p>
<p><span data-ttu-id="6b85f-126">msRTCSIP-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="6b85f-126">msRTCSIP-OptionFlags</span></span></p>
<p><span data-ttu-id="6b85f-127">msRTCSIP-OriginatorSid</span><span class="sxs-lookup"><span data-stu-id="6b85f-127">msRTCSIP-OriginatorSid</span></span></p>
<p><span data-ttu-id="6b85f-128">msRTCSIP-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="6b85f-128">msRTCSIP-OwnerUrn</span></span></p>
<p><span data-ttu-id="6b85f-129">msRTCSIP-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-129">msRTCSIP-PrimaryHomeServer</span></span></p>
<p><span data-ttu-id="6b85f-130">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="6b85f-130">msRTCSIP-PrimaryUserAddress</span></span></p>
<p><span data-ttu-id="6b85f-131">msRTCSIP-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="6b85f-131">msRTCSIP-PrivateLine</span></span></p>
<p><span data-ttu-id="6b85f-132">msRTCSIP-ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="6b85f-132">msRTCSIP-ProxyAddresses</span></span></p>
<p><span data-ttu-id="6b85f-133">msRTCSIP-SourceObjectType</span><span class="sxs-lookup"><span data-stu-id="6b85f-133">msRTCSIP-SourceObjectType</span></span></p>
<p><span data-ttu-id="6b85f-134">msRTCSIP-TargetHomeServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-134">msRTCSIP-TargetHomeServer</span></span></p>
<p><span data-ttu-id="6b85f-135">msRTCSIP-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="6b85f-135">msRTCSIP-TargetUserPolicies</span></span></p>
<p><span data-ttu-id="6b85f-136">msRTCSIP-TenantId</span><span class="sxs-lookup"><span data-stu-id="6b85f-136">msRTCSIP-TenantId</span></span></p>
<p><span data-ttu-id="6b85f-137">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="6b85f-137">msRTCSIP-UserEnabled</span></span></p>
<p><span data-ttu-id="6b85f-138">msRTCSIP-UserExtension</span><span class="sxs-lookup"><span data-stu-id="6b85f-138">msRTCSIP-UserExtension</span></span></p>
<p><span data-ttu-id="6b85f-139">msRTCSIP-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="6b85f-139">msRTCSIP-UserLocationProfile</span></span></p>
<p><span data-ttu-id="6b85f-140">msRTCSIP-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="6b85f-140">msRTCSIP-UserPolicies</span></span></p>
<p><span data-ttu-id="6b85f-141">msRTCSIP-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="6b85f-141">msRTCSIP-UserPolicy</span></span></p>
<p><span data-ttu-id="6b85f-142">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="6b85f-142">msRTCSIP-UserRoutingGroupId</span></span></p>
<p><span data-ttu-id="6b85f-143">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="6b85f-143">ProxyAddresses</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-144">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="6b85f-144">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="6b85f-145">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="6b85f-145">msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="6b85f-146">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="6b85f-146">msExchUserHoldPolicies</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-147">msRTCSIP-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="6b85f-147">msRTCSIP-ApplicationServerService</span></span></p></td>
<td><p><span data-ttu-id="6b85f-148">msRTCSIP-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="6b85f-148">msRTCSIP-ApplicationServerBL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-149">msRTCSIP-ApplicationServerSettings</span><span class="sxs-lookup"><span data-stu-id="6b85f-149">msRTCSIP-ApplicationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="6b85f-150">msRTCSIP-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="6b85f-150">msRTCSIP-ApplicationList</span></span></p>
<p><span data-ttu-id="6b85f-151">msRTCSIP-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="6b85f-151">msRTCSIP-ApplicationServerPoolLink</span></span></p>
<p><span data-ttu-id="6b85f-152">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="6b85f-152">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="6b85f-153">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-153">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-154">msRTCSIP-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="6b85f-154">msRTCSIP-ConferenceDirectory</span></span></p></td>
<td><p><span data-ttu-id="6b85f-155">msRTCSIP-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="6b85f-155">msRTCSIP-ConferenceDirectoryHomePool</span></span></p>
<p><span data-ttu-id="6b85f-156">msRTCSIP-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="6b85f-156">msRTCSIP-ConferenceDirectoryId</span></span></p>
<p><span data-ttu-id="6b85f-157">msRTCSIP-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="6b85f-157">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p>
<p><span data-ttu-id="6b85f-158">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="6b85f-158">msRTCSIP-ExtensionData</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-159">msRTCSIP-DefaultCWABank</span><span class="sxs-lookup"><span data-stu-id="6b85f-159">msRTCSIP-DefaultCWABank</span></span></p></td>
<td><p><span data-ttu-id="6b85f-160">msRTCSIP-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="6b85f-160">msRTCSIP-DefaultCWAExternalURL</span></span></p>
<p><span data-ttu-id="6b85f-161">msRTCSIP-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="6b85f-161">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-162">msRTCSIP-域</span><span class="sxs-lookup"><span data-stu-id="6b85f-162">msRTCSIP-Domain</span></span></p></td>
<td><p><span data-ttu-id="6b85f-163">msRTCSIP-默认值</span><span class="sxs-lookup"><span data-stu-id="6b85f-163">msRTCSIP-Default</span></span></p>
<p><span data-ttu-id="6b85f-164">msRTCSIP-DomainData</span><span class="sxs-lookup"><span data-stu-id="6b85f-164">msRTCSIP-DomainData</span></span></p>
<p><span data-ttu-id="6b85f-165">msRTCSIP-域名</span><span class="sxs-lookup"><span data-stu-id="6b85f-165">msRTCSIP-DomainName</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-166">msRTCSIP-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="6b85f-166">msRTCSIP-EdgeProxy</span></span></p></td>
<td><p><span data-ttu-id="6b85f-167">msRTCSIP-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="6b85f-167">msRTCSIP-EdgeProxyData</span></span></p>
<p><span data-ttu-id="6b85f-168">msRTCSIP-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-168">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-169">msRTCSIP-EnterpriseMCUSettings</span><span class="sxs-lookup"><span data-stu-id="6b85f-169">msRTCSIP-EnterpriseMCUSettings</span></span></p></td>
<td><p><span data-ttu-id="6b85f-170">msRTCSIP-MCUData</span><span class="sxs-lookup"><span data-stu-id="6b85f-170">msRTCSIP-MCUData</span></span></p>
<p><span data-ttu-id="6b85f-171">msRTCSIP-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="6b85f-171">msRTCSIP-MCUFactoryAddress</span></span></p>
<p><span data-ttu-id="6b85f-172">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-172">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-173">msRTCSIP-EnterpriseMediationServerSettings</span><span class="sxs-lookup"><span data-stu-id="6b85f-173">msRTCSIP-EnterpriseMediationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="6b85f-174">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="6b85f-174">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="6b85f-175">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-175">msRTCSIP-ServerVersion</span></span></p>
<p><span data-ttu-id="6b85f-176">msRTCSIP-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="6b85f-176">msRTCSIP-TrustedServiceLinks</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-177">msRTCSIP-EnterpriseServerSettings</span><span class="sxs-lookup"><span data-stu-id="6b85f-177">msRTCSIP-EnterpriseServerSettings</span></span></p></td>
<td><p><span data-ttu-id="6b85f-178">msRTCSIP-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="6b85f-178">msRTCSIP-EnterpriseServices</span></span></p>
<p><span data-ttu-id="6b85f-179">msRTCSIP-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="6b85f-179">msRTCSIP-PoolAddress</span></span></p>
<p><span data-ttu-id="6b85f-180">msRTCSIP-ServerData</span><span class="sxs-lookup"><span data-stu-id="6b85f-180">msRTCSIP-ServerData</span></span></p>
<p><span data-ttu-id="6b85f-181">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-181">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-182">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="6b85f-182">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="6b85f-183">msRTCSIP-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-183">msRTCSIP-BackEndServer</span></span></p>
<p><span data-ttu-id="6b85f-184">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="6b85f-184">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="6b85f-185">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-185">msRTCSIP-MirrorBackEndServer</span></span></p>
<p><span data-ttu-id="6b85f-186">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-186">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-187">msRTCSIP-LocalNormalization</span><span class="sxs-lookup"><span data-stu-id="6b85f-187">msRTCSIP-LocalNormalization</span></span></p></td>
<td><p><span data-ttu-id="6b85f-188">msRTCSIP-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="6b85f-188">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-189">msRTCSIP-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="6b85f-189">msRTCSIP-LocationContactMapping</span></span></p></td>
<td><p><span data-ttu-id="6b85f-190">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="6b85f-190">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="6b85f-191">msRTCSIP-MappingContact</span><span class="sxs-lookup"><span data-stu-id="6b85f-191">msRTCSIP-MappingContact</span></span></p>
<p><span data-ttu-id="6b85f-192">msRTCSIP-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="6b85f-192">msRTCSIP-MappingLocation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-193">msRTCSIP-LocationProfile</span><span class="sxs-lookup"><span data-stu-id="6b85f-193">msRTCSIP-LocationProfile</span></span></p></td>
<td><p><span data-ttu-id="6b85f-194">msRTCSIP-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="6b85f-194">msRTCSIP-ExternalAccessCode</span></span></p>
<p><span data-ttu-id="6b85f-195">msRTCSIP-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="6b85f-195">msRTCSIP-LocationProfileOptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-196">msRTCSIP-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="6b85f-196">msRTCSIP-MCUFactory</span></span></p></td>
<td><p><span data-ttu-id="6b85f-197">msRTCSIP-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="6b85f-197">msRTCSIP-MCUFactoryData</span></span></p>
<p><span data-ttu-id="6b85f-198">msRTCSIP-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="6b85f-198">msRTCSIP-MCUFactoryProviderID</span></span></p>
<p><span data-ttu-id="6b85f-199">msRTCSIP-MCUServers</span><span class="sxs-lookup"><span data-stu-id="6b85f-199">msRTCSIP-MCUServers</span></span></p>
<p><span data-ttu-id="6b85f-200">msRTCSIP-MCUType</span><span class="sxs-lookup"><span data-stu-id="6b85f-200">msRTCSIP-MCUType</span></span></p>
<p><span data-ttu-id="6b85f-201">msRTCSIP-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="6b85f-201">msRTCSIP-MCUVendor</span></span></p>
<p><span data-ttu-id="6b85f-202">msRTCSIP-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="6b85f-202">msRTCSIP-PoolAddresses</span></span></p>
<p><span data-ttu-id="6b85f-203">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-203">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-204">msRTCSIP-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="6b85f-204">msRTCSIP-MCUFactoryService</span></span></p></td>
<td><p><span data-ttu-id="6b85f-205">msRTCSIP-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="6b85f-205">msRTCSIP-MCUFactoryPath</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-206">msRTCSIP-移动性</span><span class="sxs-lookup"><span data-stu-id="6b85f-206">msRTCSIP-Mobility</span></span></p></td>
<td><p><span data-ttu-id="6b85f-207">msRTCSIP-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="6b85f-207">msRTCSIP-MobilityFlags</span></span></p>
<p><span data-ttu-id="6b85f-208">msRTCSIP-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6b85f-208">msRTCSIP-MobilityPolicy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-209">msRTCSIP-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-209">msRTCSIP-MonitoringServer</span></span></p></td>
<td><p><span data-ttu-id="6b85f-210">dnsHostName</span><span class="sxs-lookup"><span data-stu-id="6b85f-210">dnsHostName</span></span></p>
<p><span data-ttu-id="6b85f-211">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="6b85f-211">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="6b85f-212">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-212">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-213">msRTCSIP-Pool</span><span class="sxs-lookup"><span data-stu-id="6b85f-213">msRTCSIP-Pool</span></span></p></td>
<td><p><span data-ttu-id="6b85f-214">msRTCSIP-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="6b85f-214">msRTCSIP-ApplicationList</span></span></p>
<p><span data-ttu-id="6b85f-215">msRTCSIP-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-215">msRTCSIP-BackEndServer</span></span></p>
<p><span data-ttu-id="6b85f-216">msRTCSIP-dnsHostName</span><span class="sxs-lookup"><span data-stu-id="6b85f-216">msRTCSIP-dnsHostName</span></span></p>
<p><span data-ttu-id="6b85f-217">msRTCSIP-PoolData</span><span class="sxs-lookup"><span data-stu-id="6b85f-217">msRTCSIP-PoolData</span></span></p>
<p><span data-ttu-id="6b85f-218">msRTCSIP-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="6b85f-218">msRTCSIP-PoolDisplayName</span></span></p>
<p><span data-ttu-id="6b85f-219">msRTCSIP-PoolDomainFQDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-219">msRTCSIP-PoolDomainFQDN</span></span></p>
<p><span data-ttu-id="6b85f-220">msRTCSIP-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="6b85f-220">msRTCSIP-PoolFunctionality</span></span></p>
<p><span data-ttu-id="6b85f-221">msRTCSIP-PoolType</span><span class="sxs-lookup"><span data-stu-id="6b85f-221">msRTCSIP-PoolType</span></span></p>
<p><span data-ttu-id="6b85f-222">msRTCSIP-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-222">msRTCSIP-PoolVersion</span></span></p>
<p><span data-ttu-id="6b85f-223">msRTCSIP-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="6b85f-223">msRTCSIP-TrustedServiceLinks</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-224">msRTCSIP-PoolService</span><span class="sxs-lookup"><span data-stu-id="6b85f-224">msRTCSIP-PoolService</span></span></p></td>
<td><p><span data-ttu-id="6b85f-225">msRTCSIP-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="6b85f-225">msRTCSIP-FrontEndServers</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-226">msRTCSIP-状态</span><span class="sxs-lookup"><span data-stu-id="6b85f-226">msRTCSIP-Presence</span></span></p></td>
<td><p><span data-ttu-id="6b85f-227">msRTCSIP-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="6b85f-227">msRTCSIP-PresenceFlags</span></span></p>
<p><span data-ttu-id="6b85f-228">msRTCSIP-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="6b85f-228">msRTCSIP-PresencePolicy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-229">msRTCSIP-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="6b85f-229">msRTCSIP-TrustedMCU</span></span></p></td>
<td><p><span data-ttu-id="6b85f-230">msRTCSIP-MCUType</span><span class="sxs-lookup"><span data-stu-id="6b85f-230">msRTCSIP-MCUType</span></span></p>
<p><span data-ttu-id="6b85f-231">msRTCSIP-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="6b85f-231">msRTCSIP-MCUVendor</span></span></p>
<p><span data-ttu-id="6b85f-232">msRTCSIP-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-232">msRTCSIP-RoutingPoolDN</span></span></p>
<p><span data-ttu-id="6b85f-233">msRTCSIP-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="6b85f-233">msRTCSIP-TrustedMCUData</span></span></p>
<p><span data-ttu-id="6b85f-234">msRTCSIP-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-234">msRTCSIP-TrustedMCUFQDN</span></span></p>
<p><span data-ttu-id="6b85f-235">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-235">msRTCSIP-TrustedServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-236">msRTCSIP-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="6b85f-236">msRTCSIP-TrustedProxy</span></span></p></td>
<td><p><span data-ttu-id="6b85f-237">msRTCSIP-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="6b85f-237">msRTCSIP-TrustedProxyData</span></span></p>
<p><span data-ttu-id="6b85f-238">msRTCSIP-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-238">msRTCSIP-TrustedProxyFQDN</span></span></p>
<p><span data-ttu-id="6b85f-239">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-239">msRTCSIP-TrustedServerVersion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-240">msRTCSIP-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-240">msRTCSIP-TrustedServer</span></span></p></td>
<td><p><span data-ttu-id="6b85f-241">msRTCSIP-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="6b85f-241">msRTCSIP-TrustedServerData</span></span></p>
<p><span data-ttu-id="6b85f-242">msRTCSIP-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-242">msRTCSIP-TrustedServerFQDN</span></span></p>
<p><span data-ttu-id="6b85f-243">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-243">msRTCSIP-TrustedServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-244">msRTCSIP-TrustedService</span><span class="sxs-lookup"><span data-stu-id="6b85f-244">msRTCSIP-TrustedService</span></span></p></td>
<td><p><span data-ttu-id="6b85f-245">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="6b85f-245">msRTCSIP-ExtensionData</span></span></p>
<p><span data-ttu-id="6b85f-246">msRTCSIP-可路由</span><span class="sxs-lookup"><span data-stu-id="6b85f-246">msRTCSIP-Routable</span></span></p>
<p><span data-ttu-id="6b85f-247">msRTCSIP-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-247">msRTCSIP-RoutingPoolDN</span></span></p>
<p><span data-ttu-id="6b85f-248">msRTCSIP-ServerBL</span><span class="sxs-lookup"><span data-stu-id="6b85f-248">msRTCSIP-ServerBL</span></span></p>
<p><span data-ttu-id="6b85f-249">msRTCSIP-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-249">msRTCSIP-TrustedServerFQDN</span></span></p>
<p><span data-ttu-id="6b85f-250">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-250">msRTCSIP-TrustedServerVersion</span></span></p>
<p><span data-ttu-id="6b85f-251">msRTCSIP-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="6b85f-251">msRTCSIP-TrustedServiceFlags</span></span></p>
<p><span data-ttu-id="6b85f-252">msRTCSIP-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="6b85f-252">msRTCSIP-TrustedServicePort</span></span></p>
<p><span data-ttu-id="6b85f-253">msRTCSIP-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="6b85f-253">msRTCSIP-TrustedServiceType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-254">msRTCSIP-TrustedWebComponentsServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-254">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
<td><p><span data-ttu-id="6b85f-255">msRTCSIP-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="6b85f-255">msRTCSIP-TrustedWebComponentsServerData</span></span></p>
<p><span data-ttu-id="6b85f-256">msRTCSIP-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="6b85f-256">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p>
<p><span data-ttu-id="6b85f-257">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-257">msRTCSIP-TrustedServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-258">msRTCSIP-WebComponentsService</span><span class="sxs-lookup"><span data-stu-id="6b85f-258">msRTCSIP-WebComponentsService</span></span></p></td>
<td><p><span data-ttu-id="6b85f-259">msRTCSIP-WebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="6b85f-259">msRTCSIP-WebComponentsServers</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-260">msRTCSIP-WebComponentSettings</span><span class="sxs-lookup"><span data-stu-id="6b85f-260">msRTCSIP-WebComponentSettings</span></span></p></td>
<td><p><span data-ttu-id="6b85f-261">msRTCSIP-WebComponentsData</span><span class="sxs-lookup"><span data-stu-id="6b85f-261">msRTCSIP-WebComponentsData</span></span></p>
<p><span data-ttu-id="6b85f-262">msRTCSIP-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="6b85f-262">msRTCSIP-WebComponentsPoolAddress</span></span></p>
<p><span data-ttu-id="6b85f-263">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6b85f-263">msRTCSIP-ServerVersion</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-264">用户</span><span class="sxs-lookup"><span data-stu-id="6b85f-264">User</span></span></p></td>
<td><p><span data-ttu-id="6b85f-265">msRTCSIP-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="6b85f-265">msRTCSIP-AcpInfo</span></span></p>
<p><span data-ttu-id="6b85f-266">msRTCSIP-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="6b85f-266">msRTCSIP-ApplicationOptions</span></span></p>
<p><span data-ttu-id="6b85f-267">msRTCSIP-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="6b85f-267">msRTCSIP-ArchivingEnabled</span></span></p>
<p><span data-ttu-id="6b85f-268">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="6b85f-268">msRTCSIP-DeploymentLocator</span></span></p>
<p><span data-ttu-id="6b85f-269">msRTCSIP-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="6b85f-269">msRTCSIP-FederationEnabled</span></span></p>
<p><span data-ttu-id="6b85f-270">msRTCSIP-GroupingID</span><span class="sxs-lookup"><span data-stu-id="6b85f-270">msRTCSIP-GroupingID</span></span></p>
<p><span data-ttu-id="6b85f-271">msRTCSIP-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="6b85f-271">msRTCSIP-InternetAccessEnabled</span></span></p>
<p><span data-ttu-id="6b85f-272">msRTCSIP-行</span><span class="sxs-lookup"><span data-stu-id="6b85f-272">msRTCSIP-Line</span></span></p>
<p><span data-ttu-id="6b85f-273">msRTCSIP-LineServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-273">msRTCSIP-LineServer</span></span></p>
<p><span data-ttu-id="6b85f-274">msRTCSIP-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="6b85f-274">msRTCSIP-OptionFlags</span></span></p>
<p><span data-ttu-id="6b85f-275">msRTCSIP-OriginatorSid</span><span class="sxs-lookup"><span data-stu-id="6b85f-275">msRTCSIP-OriginatorSid</span></span></p>
<p><span data-ttu-id="6b85f-276">msRTCSIP-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="6b85f-276">msRTCSIP-OwnerUrn</span></span></p>
<p><span data-ttu-id="6b85f-277">msRTCSIP-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-277">msRTCSIP-PrimaryHomeServer</span></span></p>
<p><span data-ttu-id="6b85f-278">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="6b85f-278">msRTCSIP-PrimaryUserAddress</span></span></p>
<p><span data-ttu-id="6b85f-279">msRTCSIP-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="6b85f-279">msRTCSIP-PrivateLine</span></span></p>
<p><span data-ttu-id="6b85f-280">msRTCSIP-TargetHomeServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-280">msRTCSIP-TargetHomeServer</span></span></p>
<p><span data-ttu-id="6b85f-281">msRTCSIP-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="6b85f-281">msRTCSIP-TargetUserPolicies</span></span></p>
<p><span data-ttu-id="6b85f-282">msRTCSIP-TenantId</span><span class="sxs-lookup"><span data-stu-id="6b85f-282">msRTCSIP-TenantId</span></span></p>
<p><span data-ttu-id="6b85f-283">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="6b85f-283">msRTCSIP-UserEnabled</span></span></p>
<p><span data-ttu-id="6b85f-284">msRTCSIP-UserExtension</span><span class="sxs-lookup"><span data-stu-id="6b85f-284">msRTCSIP-UserExtension</span></span></p>
<p><span data-ttu-id="6b85f-285">msRTCSIP-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="6b85f-285">msRTCSIP-UserLocationProfile</span></span></p>
<p><span data-ttu-id="6b85f-286">msRTCSIP-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="6b85f-286">msRTCSIP-UserPolicies</span></span></p>
<p><span data-ttu-id="6b85f-287">msRTCSIP-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="6b85f-287">msRTCSIP-UserPolicy</span></span></p>
<p><span data-ttu-id="6b85f-288">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="6b85f-288">msRTCSIP-UserRoutingGroupId</span></span></p>
<p><span data-ttu-id="6b85f-289">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="6b85f-289">ProxyAddresses</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="classes-contained-in-other-classes"></a><span data-ttu-id="6b85f-290">包含在其他类中的类</span><span class="sxs-lookup"><span data-stu-id="6b85f-290">Classes Contained in Other Classes</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b85f-291">种类</span><span class="sxs-lookup"><span data-stu-id="6b85f-291">Class</span></span></th>
<th><span data-ttu-id="6b85f-292">可能包含此类</span><span class="sxs-lookup"><span data-stu-id="6b85f-292">May contain this class</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-293">serviceConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="6b85f-293">serviceConnectionPoint</span></span></p></td>
<td><p><span data-ttu-id="6b85f-294">msRTCSIP-服务器</span><span class="sxs-lookup"><span data-stu-id="6b85f-294">msRTCSIP-Server</span></span></p>
<p><span data-ttu-id="6b85f-295">msRTCSIP-PoolService</span><span class="sxs-lookup"><span data-stu-id="6b85f-295">msRTCSIP-PoolService</span></span></p>
<p><span data-ttu-id="6b85f-296">msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="6b85f-296">msRTCSIP-MCU</span></span></p>
<p><span data-ttu-id="6b85f-297">msRTCSIP-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="6b85f-297">msRTCSIP-MCUFactoryService</span></span></p>
<p><span data-ttu-id="6b85f-298">msRTCSIP-WebComponents</span><span class="sxs-lookup"><span data-stu-id="6b85f-298">msRTCSIP-WebComponents</span></span></p>
<p><span data-ttu-id="6b85f-299">msRTCSIP-WebComponentsService</span><span class="sxs-lookup"><span data-stu-id="6b85f-299">msRTCSIP-WebComponentsService</span></span></p>
<p><span data-ttu-id="6b85f-300">msRTCSIP-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="6b85f-300">msRTCSIP-ApplicationServerService</span></span></p>
<p><span data-ttu-id="6b85f-301">msRTCSIP-服务</span><span class="sxs-lookup"><span data-stu-id="6b85f-301">msRTCSIP-Service</span></span></p>
<p><span data-ttu-id="6b85f-302">msRTCSIP-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="6b85f-302">msRTCSIP-ConnectionPoint</span></span></p>
<p><span data-ttu-id="6b85f-303">msRTCSIP-MediationServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-303">msRTCSIP-MediationServer</span></span></p>
<p><span data-ttu-id="6b85f-304">msRTCSIP-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-304">msRTCSIP-ApplicationServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-305">msRTCSIP-服务</span><span class="sxs-lookup"><span data-stu-id="6b85f-305">msRTCSIP-Service</span></span></p></td>
<td><p><span data-ttu-id="6b85f-306">msRTCSIP-GlobalContainer</span><span class="sxs-lookup"><span data-stu-id="6b85f-306">msRTCSIP-GlobalContainer</span></span></p>
<p><span data-ttu-id="6b85f-307">msRTCSIP-池</span><span class="sxs-lookup"><span data-stu-id="6b85f-307">msRTCSIP-Pools</span></span></p>
<p><span data-ttu-id="6b85f-308">msRTCSIP-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="6b85f-308">msRTCSIP-MCUFactories</span></span></p>
<p><span data-ttu-id="6b85f-309">msRTCSIP-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="6b85f-309">msRTCSIP-TrustedMCUs</span></span></p>
<p><span data-ttu-id="6b85f-310">msRTCSIP-TrustedWebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="6b85f-310">msRTCSIP-TrustedWebComponentsServers</span></span></p>
<p><span data-ttu-id="6b85f-311">msRTCSIP-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="6b85f-311">msRTCSIP-TrustedProxies</span></span></p>
<p><span data-ttu-id="6b85f-312">msRTCSIP-TrustedServices</span><span class="sxs-lookup"><span data-stu-id="6b85f-312">msRTCSIP-TrustedServices</span></span></p>
<p><span data-ttu-id="6b85f-313">msRTCSIP-ApplicationContacts</span><span class="sxs-lookup"><span data-stu-id="6b85f-313">msRTCSIP-ApplicationContacts</span></span></p>
<p><span data-ttu-id="6b85f-314">msRTCSIP-LocationContactMappings</span><span class="sxs-lookup"><span data-stu-id="6b85f-314">msRTCSIP-LocationContactMappings</span></span></p>
<p><span data-ttu-id="6b85f-315">msRTCSIP-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="6b85f-315">msRTCSIP-ConferenceDirectories</span></span></p>
<p><span data-ttu-id="6b85f-316">msRTCSIP-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="6b85f-316">msRTCSIP-GlobalTopologySettings</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-317">msRTCSIP-GlobalContainer</span><span class="sxs-lookup"><span data-stu-id="6b85f-317">msRTCSIP-GlobalContainer</span></span></p></td>
<td><p><span data-ttu-id="6b85f-318">msRTCSIP-域</span><span class="sxs-lookup"><span data-stu-id="6b85f-318">msRTCSIP-Domain</span></span></p>
<p><span data-ttu-id="6b85f-319">msRTCSIP-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-319">msRTCSIP-TrustedServer</span></span></p>
<p><span data-ttu-id="6b85f-320">msRTCSIP-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="6b85f-320">msRTCSIP-EdgeProxy</span></span></p>
<p><span data-ttu-id="6b85f-321">msRTCSIP-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-321">msRTCSIP-MonitoringServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-322">msRTCSIP-池</span><span class="sxs-lookup"><span data-stu-id="6b85f-322">msRTCSIP-Pools</span></span></p></td>
<td><p><span data-ttu-id="6b85f-323">msRTCSIP-Pool</span><span class="sxs-lookup"><span data-stu-id="6b85f-323">msRTCSIP-Pool</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-324">msRTCSIP-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="6b85f-324">msRTCSIP-MCUFactories</span></span></p></td>
<td><p><span data-ttu-id="6b85f-325">msRTCSIP-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="6b85f-325">msRTCSIP-MCUFactory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-326">msRTCSIP-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="6b85f-326">msRTCSIP-TrustedMCUs</span></span></p></td>
<td><p><span data-ttu-id="6b85f-327">msRTCSIP-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="6b85f-327">msRTCSIP-TrustedMCU</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-328">msRTCSIP-TrustedWebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="6b85f-328">msRTCSIP-TrustedWebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="6b85f-329">msRTCSIP-TrustedWebComponentsServer</span><span class="sxs-lookup"><span data-stu-id="6b85f-329">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-330">msRTCSIP-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="6b85f-330">msRTCSIP-TrustedProxies</span></span></p></td>
<td><p><span data-ttu-id="6b85f-331">msRTCSIP-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="6b85f-331">msRTCSIP-TrustedProxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-332">msRTCSIP-TrustedServices</span><span class="sxs-lookup"><span data-stu-id="6b85f-332">msRTCSIP-TrustedServices</span></span></p></td>
<td><p><span data-ttu-id="6b85f-333">msRTCSIP-TrustedService</span><span class="sxs-lookup"><span data-stu-id="6b85f-333">msRTCSIP-TrustedService</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-334">msRTCSIP-LocationContactMappings</span><span class="sxs-lookup"><span data-stu-id="6b85f-334">msRTCSIP-LocationContactMappings</span></span></p></td>
<td><p><span data-ttu-id="6b85f-335">msRTCSIP-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="6b85f-335">msRTCSIP-LocationContactMapping</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b85f-336">msRTCSIP-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="6b85f-336">msRTCSIP-ConferenceDirectories</span></span></p></td>
<td><p><span data-ttu-id="6b85f-337">msRTCSIP-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="6b85f-337">msRTCSIP-ConferenceDirectory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b85f-338">msRTCSIP-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="6b85f-338">msRTCSIP-GlobalTopologySettings</span></span></p></td>
<td><p><span data-ttu-id="6b85f-339">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="6b85f-339">msRTCSIP-GlobalTopologySetting</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6b85f-340">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b85f-340">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

