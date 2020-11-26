---
title: Lync Server 2013：配置网络站点链接
description: Lync Server 2013：配置网络站点链接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring network site links
ms:assetid: 7e9147ae-e727-46c8-8c1a-6c13201f09be
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521023(v=OCS.15)
ms:contentKeyID: 48184622
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 68b4ecce15b8f3ba5a5717c73a8f97f8a0633b58
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432889"
---
# <a name="configuring-network-site-links-in-lync-server-2013"></a><span data-ttu-id="34bdc-103">在 Lync Server 2013 中配置网络站点链接</span><span class="sxs-lookup"><span data-stu-id="34bdc-103">Configuring network site links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34bdc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34bdc-104">

<span> </span></span></span>

<span data-ttu-id="34bdc-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="34bdc-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="34bdc-106">在呼叫许可控制 (CAC) 配置中，你可以创建网络间策略来定义直接链接的网站之间的带宽限制。</span><span class="sxs-lookup"><span data-stu-id="34bdc-106">Within a call admission control (CAC) configuration, you can create network inter-site policies that define bandwidth limitations between sites that are directly linked.</span></span> <span data-ttu-id="34bdc-107">当网络站点共享直接链接时，可以在这两个站点之间定义音频和视频连接的带宽限制。</span><span class="sxs-lookup"><span data-stu-id="34bdc-107">When network sites share a direct link, bandwidth limitations for audio and video connections can be defined between those two sites.</span></span> <span data-ttu-id="34bdc-108">无法使用 Lync Server 控制面板配置网络网站策略，只能通过 Lync Server 命令行管理程序使用 cmdlet 执行此操作。</span><span class="sxs-lookup"><span data-stu-id="34bdc-108">You cannot use the Lync Server Control Panel to configure network site policies, this can be done only by using cmdlets from the Lync Server Management Shell.</span></span> <span data-ttu-id="34bdc-109">你可以从 Lync Server 命令行管理程序中创建、修改和删除网络站点链接 (也称为网络站点内策略) 。</span><span class="sxs-lookup"><span data-stu-id="34bdc-109">You can create, modify, and remove a network site link (also known as a network inter-site policy) from the Lync Server Management Shell.</span></span>

<div>

## <a name="to-create-a-network-site-link"></a><span data-ttu-id="34bdc-110">创建网络站点链接</span><span class="sxs-lookup"><span data-stu-id="34bdc-110">To create a network site link</span></span>

1.  <span data-ttu-id="34bdc-111">以 RTCUniversalServerAdmins 组成员的身份或必要的用户权限登录到安装了 Lync Server 管理外壳的计算机，如在 [Lync Server 2013 中的 "委派设置权限](lync-server-2013-delegate-setup-permissions.md)" 中所述。</span><span class="sxs-lookup"><span data-stu-id="34bdc-111">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="34bdc-112">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="34bdc-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="34bdc-113">在命令提示符处，键入以下命令，替换适用于您的配置的有效值：</span><span class="sxs-lookup"><span data-stu-id="34bdc-113">From the command prompt, type the following command, substituting values that are valid for your configuration:</span></span>
    
        New-CsNetworkInterSitePolicy -Identity Reno_Portland -NetworkSiteID1 Reno -NetworkSiteID2 Portland -BWPolicyProfileID LowBWLimits
    
    <span data-ttu-id="34bdc-114">此示例创建一个名为 Reno 的新网络网站链接 \_ ，该链接设置 Reno 和网络站点之间的带宽限制。</span><span class="sxs-lookup"><span data-stu-id="34bdc-114">This example creates a new network site link named Reno\_Portland that sets bandwidth limitations between the Reno and Portland network sites.</span></span> <span data-ttu-id="34bdc-115">运行此命令之前，网络站点和带宽策略配置文件必须已经存在。</span><span class="sxs-lookup"><span data-stu-id="34bdc-115">The network sites and the bandwidth policy profile must already exist before running this command.</span></span>

<span data-ttu-id="34bdc-116">有关详细的参数说明，请参阅 Lync Server Management Shell 文档中的 " [新建-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy) "。</span><span class="sxs-lookup"><span data-stu-id="34bdc-116">For detailed parameter descriptions, see [New-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy) in the Lync Server Management Shell documentation.</span></span> <span data-ttu-id="34bdc-117">若要检索可应用于网络站点链接的带宽策略配置文件的列表，请调用 **CsNetworkBandwidthPolicyProfile** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34bdc-117">To retrieve a list of bandwidth policy profiles that can be applied to the network site link, call the **Get-CsNetworkBandwidthPolicyProfile** cmdlet.</span></span> <span data-ttu-id="34bdc-118">有关详细信息，请参阅 Lync Server Management Shell 文档中的 [CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) 。</span><span class="sxs-lookup"><span data-stu-id="34bdc-118">For details, see [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) in the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-modify-a-network-site-link"></a><span data-ttu-id="34bdc-119">修改网络站点链接</span><span class="sxs-lookup"><span data-stu-id="34bdc-119">To modify a network site link</span></span>

1.  <span data-ttu-id="34bdc-120">以 RTCUniversalServerAdmins 组成员的身份或必要的用户权限登录到安装了 Lync Server 管理外壳的计算机，如在 [Lync Server 2013 中的 "委派设置权限](lync-server-2013-delegate-setup-permissions.md)" 中所述。</span><span class="sxs-lookup"><span data-stu-id="34bdc-120">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="34bdc-121">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="34bdc-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="34bdc-122">使用 **CsNetworkInterSitePolicy** cmdlet 修改给定网络网站链接的属性。</span><span class="sxs-lookup"><span data-stu-id="34bdc-122">Use the **Set-CsNetworkInterSitePolicy** cmdlet to modify the properties of a given network site link.</span></span> <span data-ttu-id="34bdc-123">既可以修改 (，也可以修改所连接的网站) 或两者，也可以修改与链接关联的带宽策略配置文件。</span><span class="sxs-lookup"><span data-stu-id="34bdc-123">You can modify either (or both) or the connected sites, and you can modify the bandwidth policy profile associated with the link.</span></span> <span data-ttu-id="34bdc-124">下面是修改名为 Reno 的网站链接的带宽策略配置文件的示例 \_ ：</span><span class="sxs-lookup"><span data-stu-id="34bdc-124">Here is an example of modifying the bandwidth policy profile of a site link named Reno\_Portland:</span></span>
    
        Set-CsNetworkInterSitePolicy -Identity Reno_Portland -BWPolicyProfileID HighBWLimits

<span data-ttu-id="34bdc-125">有关详细的参数说明，请参阅 Lync Server Management Shell 文档中的 " [设置 CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy) "。</span><span class="sxs-lookup"><span data-stu-id="34bdc-125">For detailed parameter descriptions, see [Set-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy) in the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-delete-a-network-site-link"></a><span data-ttu-id="34bdc-126">删除网络网站链接</span><span class="sxs-lookup"><span data-stu-id="34bdc-126">To delete a network site link</span></span>

1.  <span data-ttu-id="34bdc-127">以 RTCUniversalServerAdmins 组成员的身份或必要的用户权限登录到安装了 Lync Server 管理外壳的计算机，如在 [Lync Server 2013 中的 "委派设置权限](lync-server-2013-delegate-setup-permissions.md)" 中所述。</span><span class="sxs-lookup"><span data-stu-id="34bdc-127">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="34bdc-128">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="34bdc-128">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="34bdc-129">使用 **CsNetworkInterSitePolicy** cmdlet 删除网络站点链接。</span><span class="sxs-lookup"><span data-stu-id="34bdc-129">Use the **Remove-CsNetworkInterSitePolicy** cmdlet to remove a network site link.</span></span> <span data-ttu-id="34bdc-130">以下示例删除 Reno 的 " \_ 上海" 网络网站链接：</span><span class="sxs-lookup"><span data-stu-id="34bdc-130">The following example deletes the Reno\_Portland network site link:</span></span>
    
        Remove-CsNetworkInterSitePolicy -Identity Reno_Portland

<span data-ttu-id="34bdc-131">有关详细的参数说明，请参阅 Lync Server Management Shell 文档中的 [Remove-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy) 。</span><span class="sxs-lookup"><span data-stu-id="34bdc-131">For detailed parameter descriptions, see [Remove-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy) in the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="34bdc-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="34bdc-132">See Also</span></span>


[<span data-ttu-id="34bdc-133">Lync Server 2013 中的呼叫许可控制 cmdlet</span><span class="sxs-lookup"><span data-stu-id="34bdc-133">Call admission control cmdlets in Lync Server 2013</span></span>](https://docs.microsoft.com/powershell/module/skype/)  


[<span data-ttu-id="34bdc-134">New-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="34bdc-134">New-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy)  
[<span data-ttu-id="34bdc-135">Set-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="34bdc-135">Set-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy)  
[<span data-ttu-id="34bdc-136">Remove-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="34bdc-136">Remove-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy)  
[<span data-ttu-id="34bdc-137">Get-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="34bdc-137">Get-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterSitePolicy)  
[<span data-ttu-id="34bdc-138">Get-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="34bdc-138">Get-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="34bdc-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34bdc-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

