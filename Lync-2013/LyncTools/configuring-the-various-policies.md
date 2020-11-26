---
title: 配置各种策略
description: 配置各种策略。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring the Various Policies
ms:assetid: e3b3cbda-7c17-470b-acb0-82fdcc473184
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945610(v=OCS.15)
ms:contentKeyID: 51541436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 746d299ac605c7dfe89a957246d47309dfbc0a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440048"
---
# <a name="configuring-the-various-policies"></a><span data-ttu-id="698ff-103">配置各种策略</span><span class="sxs-lookup"><span data-stu-id="698ff-103">Configuring the Various Policies</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="698ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="698ff-104">

<span> </span></span></span>

<span data-ttu-id="698ff-105">_**主题上次修改时间：** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="698ff-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<div>

<span data-ttu-id="698ff-106">下面是在运行 Lync Server 2013 应力和性能工具之前，您可以在 Lync Server 2013 拓扑中配置的各种策略。</span><span class="sxs-lookup"><span data-stu-id="698ff-106">Here are the various policies that you can configure in your Lync Server 2013 topology, prior to running the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="configuring-the-archiving-policy"></a><span data-ttu-id="698ff-107">配置存档策略</span><span class="sxs-lookup"><span data-stu-id="698ff-107">Configuring the Archiving Policy</span></span>

<span data-ttu-id="698ff-108">请参阅示例脚本 ArchivingPolicy.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-108">See the example script ArchivingPolicy.ps1.</span></span> <span data-ttu-id="698ff-109">只有在拓扑中部署了存档服务器时，才需要使用此脚本。</span><span class="sxs-lookup"><span data-stu-id="698ff-109">You need to use this script only if an Archiving Server is deployed in your topology.</span></span> <span data-ttu-id="698ff-110">有关详细信息，请参阅 Lync server 2013 文档和 cmdlet 有关 [在 Lync Server 2013 中存档和监视 cmdlet](https://technet.microsoft.com/library/gg415629\(v=ocs.15\))的帮助。</span><span class="sxs-lookup"><span data-stu-id="698ff-110">For details, see the Lync Server 2013 documentation and cmdlet Help for [Archiving and Monitoring cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-conferencing-policy"></a><span data-ttu-id="698ff-111">配置会议策略</span><span class="sxs-lookup"><span data-stu-id="698ff-111">Configuring the Conferencing Policy</span></span>

<span data-ttu-id="698ff-112">请参阅示例脚本 MeetingPolicy.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-112">See the example script MeetingPolicy.ps1.</span></span> <span data-ttu-id="698ff-113">有关详细信息，请参阅 lync server 2013 文档和 [Lync server 2013 中的 Web 会议](https://technet.microsoft.com/library/gg415675\(v=ocs.15\))Cmdlet cmdlet 帮助。</span><span class="sxs-lookup"><span data-stu-id="698ff-113">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Web conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-contacts-policy"></a><span data-ttu-id="698ff-114">配置联系人策略</span><span class="sxs-lookup"><span data-stu-id="698ff-114">Configuring the Contacts Policy</span></span>

<span data-ttu-id="698ff-115">请参阅示例 ContactsPolicy.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-115">See the example ContactsPolicy.ps1.</span></span> <span data-ttu-id="698ff-116">有关详细信息，请参阅 Lync server 2013 文档以及 [Lync server 2013 中的 IM 和状态 cmdlet](https://technet.microsoft.com/library/gg398611\(v=ocs.15\))的 cmdlet 帮助。</span><span class="sxs-lookup"><span data-stu-id="698ff-116">For details, see the Lync Server 2013 documentation and the cmdlet Help for [IM and presence cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-federation-policy"></a><span data-ttu-id="698ff-117">配置联合身份验证策略</span><span class="sxs-lookup"><span data-stu-id="698ff-117">Configuring the Federation Policy</span></span>

<span data-ttu-id="698ff-118">请参阅示例 FederationPolicy.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-118">See the example FederationPolicy.ps1.</span></span> <span data-ttu-id="698ff-119">有关详细信息，请参阅 lync server 2013 文档和 lync server 2013 中的 [Edge 服务器 cmdlet](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) 以及 [lync server 2013 中的联盟和外部访问 cmdlet](https://technet.microsoft.com/library/gg415651\(v=ocs.15\))中的 cmdlet 帮助。</span><span class="sxs-lookup"><span data-stu-id="698ff-119">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Edge Server cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) and [Federation and external access cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-call-admission-control-policy"></a><span data-ttu-id="698ff-120">配置呼叫许可控制策略</span><span class="sxs-lookup"><span data-stu-id="698ff-120">Configuring the Call Admission Control Policy</span></span>

<span data-ttu-id="698ff-121">请参阅示例 BandwidthPolicy.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-121">See the example BandwidthPolicy.ps1.</span></span> <span data-ttu-id="698ff-122">有关详细信息，请参阅 lync server 2013 文档 [概述 lync server 2013 中的呼叫许可控制](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) 和 [lync server 2013 中的呼叫许可控制 Cmdlet](https://technet.microsoft.com/library/gg415676\(v=ocs.15\))的 cmdlet 帮助。</span><span class="sxs-lookup"><span data-stu-id="698ff-122">For details, see the Lync Server 2013 documentation [Overview of call admission control in Lync Server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) and the cmdlet Help for [Call admission control cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-voice-routing-rules"></a><span data-ttu-id="698ff-123">配置语音路由规则</span><span class="sxs-lookup"><span data-stu-id="698ff-123">Configuring the Voice Routing Rules</span></span>

<span data-ttu-id="698ff-124">请参阅示例 RoutingRules.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-124">See the example RoutingRules.ps1.</span></span> <span data-ttu-id="698ff-125">配置语音路由规则时，请注意电话上下文 (即/Location 配置文件或/SimpleName) 和内部/外部区域代码，以便你可以在创建用户时以及在 LyncPerfTool (配置期间为其指定，特别是适用于 PSTN-UC 和 UC-PSTN) 。</span><span class="sxs-lookup"><span data-stu-id="698ff-125">When you configure the voice routing rules, take note of the Phone Context (that is, /Location Profile or /SimpleName) and Internal/External Area Codes so that you can specify them when creating users and during LyncPerfTool configuration (specifically for PSTN-UC and UC-PSTN).</span></span> <span data-ttu-id="698ff-126">例如，RoutingRules.ps1 示例中 **CsDialPlan** cmdlet 的调用中的 SimpleName 参数应用于 UserProfileGenerator.exe 的下图中的 LocationProfile 值。</span><span class="sxs-lookup"><span data-stu-id="698ff-126">For example, the SimpleName parameter in the call to the **New-CsDialPlan** cmdlet in the RoutingRules.ps1 example should be used for the LocationProfile value in the following figure of UserProfileGenerator.exe.</span></span>

<span data-ttu-id="698ff-127">![示例语音路由规则。](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "示例语音路由规则。")</span><span class="sxs-lookup"><span data-stu-id="698ff-127">![Sample voice routing rule.](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Sample voice routing rule.")</span></span>

<span data-ttu-id="698ff-128">有关详细信息，请参阅 lync server 2013 文档和适用于 [Lync server 2013 中的企业语音 cmdlet](https://technet.microsoft.com/library/gg415658\(v=ocs.15\))的 cmdlet 帮助。</span><span class="sxs-lookup"><span data-stu-id="698ff-128">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Enterprise Voice cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-conferencing-attendant-application"></a><span data-ttu-id="698ff-129">配置会议助理应用程序</span><span class="sxs-lookup"><span data-stu-id="698ff-129">Configuring Conferencing Attendant application</span></span>

<span data-ttu-id="698ff-130">请参阅示例 ConferenceAutoAttendantConfiguration.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-130">See the example ConferenceAutoAttendantConfiguration.ps1.</span></span> <span data-ttu-id="698ff-131">请记下 (1121111111 的 ConferencingAutoAttendant 电话号码（默认情况下) ），以便你可以在 LyncPerf 工具配置工具中键入它以进行配置生成。</span><span class="sxs-lookup"><span data-stu-id="698ff-131">Take note of the ConferencingAutoAttendant phone number (1121111111, by default), so that you can type it into the LyncPerf Tool Configuration tool for configuration generation.</span></span>

<span data-ttu-id="698ff-132">![配置会议助理应用程序](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "配置会议助理应用程序")</span><span class="sxs-lookup"><span data-stu-id="698ff-132">![Configuring the Conferencing Attendant application](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Configuring the Conferencing Attendant application")</span></span>

<span data-ttu-id="698ff-133">有关详细信息，请参阅 lync server 2013 文档和 lync server 2013 中的 [Web 会议](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) Cmdlet 和 [lync server 2013 中的电话拨入式会议 cmdlet](https://technet.microsoft.com/library/gg415630\(v=ocs.15\))中的 cmdlet 帮助。</span><span class="sxs-lookup"><span data-stu-id="698ff-133">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Web conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) and [Dial-in conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-lync-server-call-park-service"></a><span data-ttu-id="698ff-134">配置 Lync Server 呼叫寄存服务</span><span class="sxs-lookup"><span data-stu-id="698ff-134">Configuring Lync Server Call Park Service</span></span>

<span data-ttu-id="698ff-135">默认情况下，通话寄存处于禁用状态。</span><span class="sxs-lookup"><span data-stu-id="698ff-135">Call Park is disabled by default.</span></span> <span data-ttu-id="698ff-136">请参阅示例 CallParkConfiguration.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-136">See the example CallParkConfiguration.ps1.</span></span> <span data-ttu-id="698ff-137">有关详细信息，请参阅 Lync server 2013 文档和 cmdlet 帮助，了解如何 [在 Lync server 2013 中调用寄存应用程序 cmdlet](https://technet.microsoft.com/library/gg415639\(v=ocs.15\))。</span><span class="sxs-lookup"><span data-stu-id="698ff-137">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Call Park application cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-emergency-calls"></a><span data-ttu-id="698ff-138">配置紧急呼叫</span><span class="sxs-lookup"><span data-stu-id="698ff-138">Configuring Emergency Calls</span></span>

<span data-ttu-id="698ff-139">执行以下步骤来配置紧急呼叫的压力和性能测试。</span><span class="sxs-lookup"><span data-stu-id="698ff-139">Perform the following steps to configure stress and performance testing for emergency calls.</span></span>

1.  <span data-ttu-id="698ff-140">设置紧急呼叫的语音路线。</span><span class="sxs-lookup"><span data-stu-id="698ff-140">Set up a voice route for emergency calls.</span></span> <span data-ttu-id="698ff-141">有关设置此语音路线的示例，请参阅注释 "E911 到 PSTN" 下的 "RoutingRules.ps1 脚本"。</span><span class="sxs-lookup"><span data-stu-id="698ff-141">See the RoutingRules.ps1 script under the comment "Route E911 to PSTN" for an example of setting up this voice route.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="698ff-142">RoutingRules.ps1 中的示例命令具有包含数字119的数字模式，而不是911。</span><span class="sxs-lookup"><span data-stu-id="698ff-142">The example command in RoutingRules.ps1 has a number pattern that includes the number 119 rather than 911.</span></span> <span data-ttu-id="698ff-143">应避免使用 911 (或实际的本地紧急号码) ，以防止在负载测试期间意外呼叫本地紧急操作员。</span><span class="sxs-lookup"><span data-stu-id="698ff-143">You should avoid using 911 (or your actual local emergency number) to prevent accidental calls to your local emergency operators during load testing.</span></span> <span data-ttu-id="698ff-144">此配置仅供模拟之用。</span><span class="sxs-lookup"><span data-stu-id="698ff-144">This configuration is for simulation purposes only.</span></span>

    
    </div>

2.  <span data-ttu-id="698ff-145">通过填写 UserProvisioningTool 中的 " **iis** " 选项卡上的值来配置地址，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="698ff-145">Configure addresses by filling in the values on the **LIS** tab in the UserProvisioningTool, as shown in the following figure.</span></span>
    
    <span data-ttu-id="698ff-146">![配置位置信息服务。](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "配置位置信息服务。")</span><span class="sxs-lookup"><span data-stu-id="698ff-146">![Configuring the Location Information Service.](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Configuring the Location Information Service.")</span></span>  

3.  <span data-ttu-id="698ff-147">单击 " **生成 .Lis 配置文件**"。</span><span class="sxs-lookup"><span data-stu-id="698ff-147">Click **Generate LIS Config Files**.</span></span>

4.  <span data-ttu-id="698ff-148">将生成用于端口、子网、交换机和无线访问点 (WAPs) 和适用于 Lync Server 2013 应力和性能工具的 XML 文件的 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="698ff-148">CSV files for ports, subnets, switches, and wireless access points (WAPs), and an XML file for the Lync Server 2013 Stress and Performance Tool, are generated.</span></span> <span data-ttu-id="698ff-149">在使用 LisConfiguration.ps1 脚本配置位置信息服务 (.LIS) 时，CSV 文件将用作) 同一文件夹中 (的输入。</span><span class="sxs-lookup"><span data-stu-id="698ff-149">The CSV files are to be used as inputs (in the same folder) when configuring Location Information service (LIS) with the LisConfiguration.ps1 script.</span></span> <span data-ttu-id="698ff-150">将生成的 Locations0.xml 文件移动到 Lync Server 2013 应力和性能工具可执行文件所在的文件夹中， ( # A1) ，它将运行位置配置文件 (拨号计划) 方案。</span><span class="sxs-lookup"><span data-stu-id="698ff-150">Move the generated Locations0.xml file to the same folder as the Lync Server 2013 Stress and Performance Tool executable (LyncPerfTool.exe), which will run location profile (dial plan) scenarios.</span></span>

</div>

<div>

## <a name="creating-enabling-configuring-and-disabling-users"></a><span data-ttu-id="698ff-151">创建、启用、配置和禁用用户</span><span class="sxs-lookup"><span data-stu-id="698ff-151">Creating, Enabling, Configuring and Disabling Users</span></span>

<span data-ttu-id="698ff-152">在运行以下脚本之前，应创建所有用户。</span><span class="sxs-lookup"><span data-stu-id="698ff-152">You should create all your users before running the following scripts.</span></span> <span data-ttu-id="698ff-153">按照 [创建用户和联系人](create-users-and-contacts.md) 中的说明创建用户。</span><span class="sxs-lookup"><span data-stu-id="698ff-153">Follow the instructions in [Create Users and Contacts](create-users-and-contacts.md) to create users.</span></span> <span data-ttu-id="698ff-154">有关详细信息，请参阅 [move-csuser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\))、 [move-csuser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\))和 [Disable-move-csuser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) cmdlet 的 Lync Server 2013 cmdlet 文档。</span><span class="sxs-lookup"><span data-stu-id="698ff-154">For details, see the Lync Server 2013 cmdlet documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)), [Set-CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\)), and [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) cmdlets.</span></span>

</div>

<div>

## <a name="configuring-response-group-application"></a><span data-ttu-id="698ff-155">配置响应组应用程序</span><span class="sxs-lookup"><span data-stu-id="698ff-155">Configuring Response Group application</span></span>

<span data-ttu-id="698ff-156">请参阅示例 ResponseGroupConfiguration.ps1。</span><span class="sxs-lookup"><span data-stu-id="698ff-156">See the example ResponseGroupConfiguration.ps1.</span></span> <span data-ttu-id="698ff-157">有关详细信息，请参阅 Lync server 2013 文档和 cmdlet 帮助，了解 [Lync server 2013 中的响应组应用程序 cmdlet](https://technet.microsoft.com/library/gg415654\(v=ocs.15\))。若要查看响应组应用程序配置，请参阅 `https://<poolfqdn>/RgsConfig/` ，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="698ff-157">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Response Group application cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)).To review the Response Group application configuration, see `https://<poolfqdn>/RgsConfig/`, as shown in the following figure.</span></span>

<span data-ttu-id="698ff-158">![响应组配置工具。](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "响应组配置工具。")</span><span class="sxs-lookup"><span data-stu-id="698ff-158">![The Response Group Configuration Tool.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "The Response Group Configuration Tool.")</span></span>

<span data-ttu-id="698ff-159"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="698ff-159"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

