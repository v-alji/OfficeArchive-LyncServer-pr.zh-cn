---
title: Lync Server 2013：创建或修改网络区域
description: Lync Server 2013：创建或修改网络区域。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network regions
ms:assetid: bd08bb66-5976-4ece-b45c-7de19569f814
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182579(v=OCS.15)
ms:contentKeyID: 48185266
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b02a041272f0df27d2133ca26096caeb01816c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431412"
---
# <a name="creating-or-modifying-network-regions-in-lync-server-2013"></a><span data-ttu-id="edefe-103">在 Lync Server 2013 中创建或修改网络区域</span><span class="sxs-lookup"><span data-stu-id="edefe-103">Creating or modifying network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="edefe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="edefe-104">

<span> </span></span></span>

<span data-ttu-id="edefe-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="edefe-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="edefe-106">网络区域跨多个地理区域互连网络的各个部分。</span><span class="sxs-lookup"><span data-stu-id="edefe-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="edefe-107">每个网络区域必须与一个中心网站相关联。</span><span class="sxs-lookup"><span data-stu-id="edefe-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="edefe-108">中心网站是在其上运行呼叫许可控制 (CAC) 带宽策略服务的数据中心网站。</span><span class="sxs-lookup"><span data-stu-id="edefe-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="edefe-109">可以使用 Lync Server "控制面板" 配置网络区域。</span><span class="sxs-lookup"><span data-stu-id="edefe-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="edefe-110">网络区域包括用于确定音频和视频连接是否允许通过 Internet 的备用路径的设置。</span><span class="sxs-lookup"><span data-stu-id="edefe-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="edefe-111">从 Lync Server 控制面板中，您可以创建、修改或删除网络区域。</span><span class="sxs-lookup"><span data-stu-id="edefe-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="edefe-112">使用本主题创建和修改网络区域。</span><span class="sxs-lookup"><span data-stu-id="edefe-112">Use this topic to create and modify network regions.</span></span> <span data-ttu-id="edefe-113">有关删除现有网络区域的详细信息，请参阅 [在 Lync Server 2013 中删除现有网络区域](lync-server-2013-deleting-existing-network-regions.md)。</span><span class="sxs-lookup"><span data-stu-id="edefe-113">For details about deleting existing network regions, see [Deleting existing network regions in Lync Server 2013](lync-server-2013-deleting-existing-network-regions.md).</span></span>

<div>

## <a name="to-create-a-network-region"></a><span data-ttu-id="edefe-114">创建网络区域</span><span class="sxs-lookup"><span data-stu-id="edefe-114">To create a network region</span></span>

1.  <span data-ttu-id="edefe-115">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="edefe-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="edefe-116">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="edefe-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="edefe-117">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="edefe-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="edefe-118">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **区域**"。</span><span class="sxs-lookup"><span data-stu-id="edefe-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="edefe-119">在 " **区域** " 页面上，单击 " **新建**"。</span><span class="sxs-lookup"><span data-stu-id="edefe-119">On the **Region** page, click **New**.</span></span>

5.  <span data-ttu-id="edefe-120">在 " **新区域** " 页面上，在 " **名称** " 字段中键入值。</span><span class="sxs-lookup"><span data-stu-id="edefe-120">In the **New Region** page, type a value in the **Name** field.</span></span> <span data-ttu-id="edefe-121">此值在 Microsoft Lync Server 2013 部署中必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="edefe-121">This value must be unique within your Microsoft Lync Server 2013 deployment.</span></span>

6.  <span data-ttu-id="edefe-122">从 " **中心站点** " 下拉列表中，选择此网络区域的中心网站。</span><span class="sxs-lookup"><span data-stu-id="edefe-122">From the **Central site** drop-down list, select the central site for this network region.</span></span>

7.  <span data-ttu-id="edefe-123">默认情况下，" **启用音频备用路径** " 复选框处于选中状态。</span><span class="sxs-lookup"><span data-stu-id="edefe-123">The **Enable audio alternate path** check box is checked by default.</span></span> <span data-ttu-id="edefe-124">此字段确定当主路径中不存在足够带宽时是否将通过备用路径路由音频呼叫。</span><span class="sxs-lookup"><span data-stu-id="edefe-124">This field determines whether audio calls will be routed through an alternate path if adequate bandwidth does not exist in the primary path.</span></span> <span data-ttu-id="edefe-125">仅当需要关闭将卸载到 Internet 时，请清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="edefe-125">Clear this check box only if you need to turn off the offload to the Internet.</span></span> <span data-ttu-id="edefe-126">如果你的任何呼叫将是 Internet 呼叫，则必须选中此复选框，无论带宽设置如何。</span><span class="sxs-lookup"><span data-stu-id="edefe-126">If any of your calls will be Internet calls, this check box must be checked, regardless of bandwidth settings.</span></span>

8.  <span data-ttu-id="edefe-127">默认情况下，" **启用视频备用路径** " 复选框处于选中状态。</span><span class="sxs-lookup"><span data-stu-id="edefe-127">The **Enable video alternate path** check box is checked by default.</span></span> <span data-ttu-id="edefe-128">此字段确定当主路径中不存在足够带宽时，是否会通过备用路径路由视频呼叫。</span><span class="sxs-lookup"><span data-stu-id="edefe-128">This field determines whether video calls will be routed through an alternate path if adequate bandwidth does not exist in the primary path.</span></span> <span data-ttu-id="edefe-129">仅当需要关闭将卸载到 Internet 时，请清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="edefe-129">Clear this check box only if you need to turn off the offload to the Internet.</span></span> <span data-ttu-id="edefe-130">如果你的任何呼叫将是 Internet 呼叫，则必须选中此复选框，无论带宽设置如何。</span><span class="sxs-lookup"><span data-stu-id="edefe-130">If any of your calls will be Internet calls, this check box must be checked, regardless of bandwidth settings.</span></span>

9.  <span data-ttu-id="edefe-131"> (可选) 在 " **说明** " 字段中键入一个值，以提供有关无法单独以名称表示的此区域的详细信息。</span><span class="sxs-lookup"><span data-stu-id="edefe-131">(Optional) Type a value in the **Description** field to provide more information about this region that cannot be expressed by the name alone.</span></span>

10. <span data-ttu-id="edefe-132">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="edefe-132">Click **Commit**.</span></span>

<span data-ttu-id="edefe-133">**关联的网站** 表不用于创建网络区域。</span><span class="sxs-lookup"><span data-stu-id="edefe-133">The **Associated sites** table is not used for creating a network region.</span></span> <span data-ttu-id="edefe-134">创建或修改网站时，将网站与区域相关联。</span><span class="sxs-lookup"><span data-stu-id="edefe-134">You associate a site with a region when you create or modify the site.</span></span> <span data-ttu-id="edefe-135">有关详细信息，请参阅 [在 Lync Server 2013 中创建或修改网络站点](lync-server-2013-creating-or-modifying-network-sites.md)。</span><span class="sxs-lookup"><span data-stu-id="edefe-135">For details, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span></span>

</div>

<div>

## <a name="to-modify-a-network-region"></a><span data-ttu-id="edefe-136">修改网络区域</span><span class="sxs-lookup"><span data-stu-id="edefe-136">To modify a network region</span></span>

1.  <span data-ttu-id="edefe-137">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="edefe-137">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="edefe-138">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="edefe-138">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="edefe-139">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="edefe-139">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="edefe-140">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **区域**"。</span><span class="sxs-lookup"><span data-stu-id="edefe-140">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="edefe-141">在 " **区域** " 页面上，单击要修改的区域。</span><span class="sxs-lookup"><span data-stu-id="edefe-141">On the **Region** page, click the region that you want to modify.</span></span>

5.  <span data-ttu-id="edefe-142">在“编辑”菜单上，单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="edefe-142">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="edefe-143">在 " **编辑区域** " 页面上，您可以修改启用和禁用音频和视频备用路径的设置，并更改说明 (有关详细信息，请参阅本主题前面的 "创建网络区域" 一节。</span><span class="sxs-lookup"><span data-stu-id="edefe-143">On the **Edit Region** page, you can modify the settings for enabling and disabling audio and video alternate paths, and change the description (for details, see the "To create a network region" section earlier in this topic.</span></span>

7.  <span data-ttu-id="edefe-144">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="edefe-144">Click **Commit**.</span></span>

<span data-ttu-id="edefe-145">您不能修改此页面上的 **相关网站** 。</span><span class="sxs-lookup"><span data-stu-id="edefe-145">You cannot modify the **Associated sites** on this page.</span></span> <span data-ttu-id="edefe-146">将提供相关网站的列表以供参考，以便你知道在修改区域设置时将受到哪些网站的影响。</span><span class="sxs-lookup"><span data-stu-id="edefe-146">The list of associated sites is provided for reference so you are aware of which sites will be affected when you modify the region settings.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="edefe-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="edefe-147">See Also</span></span>


[<span data-ttu-id="edefe-148">在 Lync Server 2013 中删除现有网络区域</span><span class="sxs-lookup"><span data-stu-id="edefe-148">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)  
[<span data-ttu-id="edefe-149">在 Lync Server 2013 中配置 CAC 的网络区域</span><span class="sxs-lookup"><span data-stu-id="edefe-149">Configure network regions for CAC in Lync Server 2013</span></span>](lync-server-2013-configure-network-regions-for-cac.md)  


[<span data-ttu-id="edefe-150">New-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="edefe-150">New-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion)  
[<span data-ttu-id="edefe-151">Set-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="edefe-151">Set-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegion)  
[<span data-ttu-id="edefe-152">Remove-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="edefe-152">Remove-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegion)  
[<span data-ttu-id="edefe-153">Get-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="edefe-153">Get-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)  
  

<span data-ttu-id="edefe-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="edefe-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

