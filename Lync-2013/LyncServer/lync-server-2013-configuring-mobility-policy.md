---
title: Lync Server 2013：配置移动策略
description: Lync Server 2013：配置移动策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring mobility policy
ms:assetid: 595536e0-9bb3-49a3-8d13-1a77351ebc62
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690018(v=OCS.15)
ms:contentKeyID: 48184204
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbbf7f9db54c8436f2db24d593dbd7a1372d5e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432917"
---
# <a name="configuring-mobility-policy-in-lync-server-2013"></a><span data-ttu-id="0c297-103">在 Lync Server 2013 中配置移动策略</span><span class="sxs-lookup"><span data-stu-id="0c297-103">Configuring mobility policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c297-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c297-104">

<span> </span></span></span>

<span data-ttu-id="0c297-105">_**主题上次修改时间：** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="0c297-105">_**Topic Last Modified:** 2013-02-13_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="0c297-106">Lync Server 2013 提供了移动性策略，这些策略确定谁可以使用移动功能、通过工作进行呼叫、通过 IP 进行语音 (VoIP) 或视频，以及 VoIP 或视频是否需要 WiFi。</span><span class="sxs-lookup"><span data-stu-id="0c297-106">Lync Server 2013 provides mobility policies that determine who can use mobility features, Call via Work, voice over IP (VoIP) or video, and whether WiFi will be required for either VoIP or video.</span></span> <span data-ttu-id="0c297-107">通过 "通过工作电话呼叫" 功能，移动用户可以通过使用工作电话号码（而不是移动电话号码）在移动电话上拨打和接听电话。</span><span class="sxs-lookup"><span data-stu-id="0c297-107">The Call via Work feature enables a mobile user to make and receive calls on a mobile phone by using a work phone number instead of the mobile phone number.</span></span> <span data-ttu-id="0c297-108">此功能可防止被呼叫方看到呼叫方的移动电话号码，并使用户可以避免出站通话费用。</span><span class="sxs-lookup"><span data-stu-id="0c297-108">This feature prevents the called party from seeing the caller's mobile phone number and enables a user to avoid outbound calling charges.</span></span> <span data-ttu-id="0c297-109">配置 VoIP 和视频使用户可以接收和进行 VoIP 呼叫和视频。</span><span class="sxs-lookup"><span data-stu-id="0c297-109">Configuring VoIP and video makes it possible for users to receive and make VoIP calls and video.</span></span> <span data-ttu-id="0c297-110">WiFi 使用的设置定义用户的设备是否需要在移动数据网络上使用 WiFi 网络。</span><span class="sxs-lookup"><span data-stu-id="0c297-110">Settings for WiFi usage define if a user’s device will be required to use a WiFi network over a cellular data network.</span></span>

<span data-ttu-id="0c297-111">默认情况下，移动、通过工作进行呼叫，并启用 VoIP 和视频功能。</span><span class="sxs-lookup"><span data-stu-id="0c297-111">By default, mobility, Call via Work, and the VoIP and video features are enabled.</span></span> <span data-ttu-id="0c297-112">已禁用 VoIp 和视频需要 WiFi 的设置。</span><span class="sxs-lookup"><span data-stu-id="0c297-112">The settings to require WiFi for VoIp and video are disabled.</span></span> <span data-ttu-id="0c297-113">管理员可以通过运行 cmdlet 来确定哪些用户有权访问这些功能。</span><span class="sxs-lookup"><span data-stu-id="0c297-113">Administrators can determine who has access to these features by running a cmdlet.</span></span> <span data-ttu-id="0c297-114">你可以将选项设置为 "全局"、"按网站" 或 "由用户"。</span><span class="sxs-lookup"><span data-stu-id="0c297-114">You can turn options off globally, by site, or by user.</span></span>

<span data-ttu-id="0c297-115">若要能够通过工作使用移动功能和通话，用户必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="0c297-115">To be able to use mobility features and Call via Work, users must meet the following prerequisites:</span></span>

  - <span data-ttu-id="0c297-116">必须为 Lync Server 2013 启用用户。</span><span class="sxs-lookup"><span data-stu-id="0c297-116">Users must be enabled for Lync Server 2013.</span></span>

  - <span data-ttu-id="0c297-117">必须为用户启用企业语音。</span><span class="sxs-lookup"><span data-stu-id="0c297-117">Users must be enabled for Enterprise Voice.</span></span>

  - <span data-ttu-id="0c297-118">必须为用户分配一个将 **EnableMobility** 选项设置为 True 的移动策略。</span><span class="sxs-lookup"><span data-stu-id="0c297-118">Users must be assigned a mobility policy that has the **EnableMobility** option set to True.</span></span>

<span data-ttu-id="0c297-119">为使用户能够通过工作使用呼叫，他们必须满足以下两个额外的先决条件：</span><span class="sxs-lookup"><span data-stu-id="0c297-119">For users to be able to use Call via Work, they must meet the following two additional prerequisites:</span></span>

  - <span data-ttu-id="0c297-120">必须为用户分配已选中 " **启用同时拨打的电话** " 选项的语音策略。</span><span class="sxs-lookup"><span data-stu-id="0c297-120">Users must be assigned a voice policy that has the **Enable simultaneous ringing of phones** option selected.</span></span>

  - <span data-ttu-id="0c297-121">必须为用户分配一个将 **EnableOutsideVoice** 选项设置为 True 的移动策略。</span><span class="sxs-lookup"><span data-stu-id="0c297-121">Users must be assigned a mobility policy that has the **EnableOutsideVoice** option set to True.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0c297-122">未启用企业语音的用户可以使用其移动设备使 Lync 通过 IP 上的 Lync 语音呼叫 (VoIP) 呼叫，或通过使用其移动设备上的 "单击以加入" 链接来加入会议（如果为语音策略指定了相应的选项）。</span><span class="sxs-lookup"><span data-stu-id="0c297-122">Users who are not enabled for Enterprise Voice can use their mobile devices to make Lync to Lync Voice over IP (VoIP) calls, or can join conferences by using the Click to Join link on their mobile devices, if you assign those users the appropriate options for voice policy.</span></span> <span data-ttu-id="0c297-123">有关详细信息，请参阅 <A href="lync-server-2013-defining-your-mobility-requirements.md">定义 Lync Server 2013 的移动性要求</A>。</span><span class="sxs-lookup"><span data-stu-id="0c297-123">For details, see <A href="lync-server-2013-defining-your-mobility-requirements.md">Defining your mobility requirements for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="0c297-124">有关为 Lync Server 2013 启用用户的详细信息，请参阅 [禁用或重新启用 Lync server 2013 的用户帐户](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)。</span><span class="sxs-lookup"><span data-stu-id="0c297-124">For details about enabling users for Lync Server 2013, see [Disable or re-enable user account for Lync Server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md).</span></span> <span data-ttu-id="0c297-125">有关为企业语音启用用户的详细信息，请参阅 [在 Lync Server 2013 中启用企业语音用户](lync-server-2013-enable-users-for-enterprise-voice.md)。</span><span class="sxs-lookup"><span data-stu-id="0c297-125">For details about enabling users for Enterprise Voice, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span> <span data-ttu-id="0c297-126">有关设置语音策略选项的详细信息，请参阅 [在 Lync Server 2013 中修改语音策略和配置 PSTN 使用记录](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)。</span><span class="sxs-lookup"><span data-stu-id="0c297-126">For details about setting voice policy options, see [Modify a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md).</span></span>

<div>

## <a name="to-modify-global-mobility-policy"></a><span data-ttu-id="0c297-127">修改全局移动策略</span><span class="sxs-lookup"><span data-stu-id="0c297-127">To modify global mobility policy</span></span>

1.  <span data-ttu-id="0c297-128">登录到安装了 Lync Server 命令行管理器和 Ocscore 的任何计算机作为 CsAdministrator 角色的成员。</span><span class="sxs-lookup"><span data-stu-id="0c297-128">Log on to any computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="0c297-129">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="0c297-129">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="0c297-130">通过全球工作，关闭对移动和通话的访问。</span><span class="sxs-lookup"><span data-stu-id="0c297-130">Turn off access to mobility and Call via Work globally.</span></span> <span data-ttu-id="0c297-131">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="0c297-131">At the command line, type:</span></span>
    
        Set-CsMobilityPolicy -EnableMobility $False -EnableOutsideVoice $False
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0c297-132">您可以通过工作来关闭呼叫，而无需关闭移动访问。</span><span class="sxs-lookup"><span data-stu-id="0c297-132">You can turn off Call via Work without turning off access to mobility.</span></span> <span data-ttu-id="0c297-133">但是，如果未关闭 "通过工作进行呼叫"，则无法关闭行动。</span><span class="sxs-lookup"><span data-stu-id="0c297-133">However, you cannot turn off mobility without also turning off Call via Work.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-mobility-policy-by-site"></a><span data-ttu-id="0c297-134">按网站修改移动策略</span><span class="sxs-lookup"><span data-stu-id="0c297-134">To modify mobility policy by site</span></span>

1.  <span data-ttu-id="0c297-135">登录到安装了 Lync Server 命令行管理器和 Ocscore 的任何计算机作为 CsAdministrator 角色的成员。</span><span class="sxs-lookup"><span data-stu-id="0c297-135">Log on to any computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="0c297-136">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="0c297-136">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="0c297-137">创建网站级策略，关闭 VoIP 和视频，并启用 IP 音频的 WiFi 和视频，并按站点启用 IP 视频的 WiFi。</span><span class="sxs-lookup"><span data-stu-id="0c297-137">Create a site-level policy, and turn off VoIP and video, and enable Require WiFi for IP Audio and for IP Video by site.</span></span> <span data-ttu-id="0c297-138">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="0c297-138">At the command line, type:</span></span>
    
        New-CsMobilityPolicy -Identity site:<site identifier> -EnableIPAudioVideo $False -RequireWiFiForIPAudio $True -RequireWiFiForIPVideo $True

</div>

<div>

## <a name="to-modify-mobility-policy-by-user"></a><span data-ttu-id="0c297-139">按用户修改移动策略</span><span class="sxs-lookup"><span data-stu-id="0c297-139">To modify mobility policy by user</span></span>

1.  <span data-ttu-id="0c297-140">登录到安装了 Lync Server 命令行管理器和 Ocscore 的任何计算机作为 CsAdministrator 角色的成员。</span><span class="sxs-lookup"><span data-stu-id="0c297-140">Log on to any computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="0c297-141">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="0c297-141">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="0c297-142">创建用户级移动策略，并通过用户的工作方式关闭移动性和呼叫。</span><span class="sxs-lookup"><span data-stu-id="0c297-142">Create user level mobility policies and turn off mobility and Call via Work by user.</span></span> <span data-ttu-id="0c297-143">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="0c297-143">At the command line, type:</span></span>
    
        New-CsMobilityPolicy -Identity <policy name> -EnableMobility $False -EnableOutsideVoice $False
        Grant-CsMobilityPolicy -Identity <user identifier> -PolicyName <policy name>
    
    <span data-ttu-id="0c297-144">您可以通过工作来关闭呼叫，而无需关闭移动访问。</span><span class="sxs-lookup"><span data-stu-id="0c297-144">You can turn off Call via Work without turning off access to mobility.</span></span> <span data-ttu-id="0c297-145">但是，如果未关闭 "通过工作进行呼叫"，则无法关闭行动。</span><span class="sxs-lookup"><span data-stu-id="0c297-145">However, you cannot turn off mobility without also turning off Call via Work.</span></span>
    
    <span data-ttu-id="0c297-146">例如：</span><span class="sxs-lookup"><span data-stu-id="0c297-146">For example:</span></span>
    
        New-CsMobilityPolicy "tag:disableOutsideVoice" -EnableOutsideVoice $False
        Grant-CsMobilityPolicy -Identity -MobileUser1@contoso.com -PolicyName Tag:disableOutsideVoice

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0c297-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0c297-147">See Also</span></span>


[<span data-ttu-id="0c297-148">禁用或重新启用 Lync Server 2013 的用户帐户</span><span class="sxs-lookup"><span data-stu-id="0c297-148">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[<span data-ttu-id="0c297-149">在 Lync Server 2013 中启用企业语音用户</span><span class="sxs-lookup"><span data-stu-id="0c297-149">Enable users for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-enterprise-voice.md)  
[<span data-ttu-id="0c297-150">在 Lync Server 2013 中修改语音策略和配置 PSTN 使用记录</span><span class="sxs-lookup"><span data-stu-id="0c297-150">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)  


[<span data-ttu-id="0c297-151">定义您的 Lync Server 2013 移动要求</span><span class="sxs-lookup"><span data-stu-id="0c297-151">Defining your mobility requirements for Lync Server 2013</span></span>](lync-server-2013-defining-your-mobility-requirements.md)  


[<span data-ttu-id="0c297-152">New-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0c297-152">New-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy)  
[<span data-ttu-id="0c297-153">Set-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0c297-153">Set-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy)  
[<span data-ttu-id="0c297-154">Get-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0c297-154">Get-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy)  
[<span data-ttu-id="0c297-155">Grant-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0c297-155">Grant-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy)  
[<span data-ttu-id="0c297-156">Remove-CsMobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0c297-156">Remove-CsMobilityPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy)  
  

<span data-ttu-id="0c297-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c297-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

