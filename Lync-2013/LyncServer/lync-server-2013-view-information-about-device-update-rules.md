---
title: Lync Server 2013：查看有关设备更新规则的信息
description: Lync Server 2013：查看有关设备更新规则的信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View information about Device Update rules
ms:assetid: d6677ca4-024b-4816-8511-8d7630788107
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994077(v=OCS.15)
ms:contentKeyID: 51803988
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aecfd0dd778b576ea4a672e550f9e27d7ca463e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446295"
---
# <a name="view-information-about-device-update-rules-in-lync-server-2013"></a><span data-ttu-id="c9a26-103">查看有关 Lync Server 2013 中的设备更新规则的信息</span><span class="sxs-lookup"><span data-stu-id="c9a26-103">View information about Device Update rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9a26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9a26-104">

<span> </span></span></span>

<span data-ttu-id="c9a26-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="c9a26-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="c9a26-106">查看有关已导入的设备更新规则的详细信息，包括更新适用于的设备的类型、模型和品牌;更新的版本和类型;以及更新的区域设置和池。</span><span class="sxs-lookup"><span data-stu-id="c9a26-106">View details about device update rules that have already been imported, including the type, model, and brand of devices the update applies to; version and type of update; and locale and pool for the update.</span></span> <span data-ttu-id="c9a26-107">信息可用于所有导入的设备更新规则，这些规则是待审批、已部署 (批准的) 、回调 (还原) 以及你决定不使用 (重置) 。</span><span class="sxs-lookup"><span data-stu-id="c9a26-107">Information is available for all imported device update rules—those that are pending approval, deployed (approved), recalled (restored), and those you’ve decided not to use (reset).</span></span> <span data-ttu-id="c9a26-108">从 Lync Server "控制面板" 或 Windows PowerShell 中访问此信息。</span><span class="sxs-lookup"><span data-stu-id="c9a26-108">Access this information from either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c9a26-109">有关如何导入、批准、重置、还原和删除规则的详细信息，请参阅 <A href="lync-server-2013-device-update-rules.md">Lync Server 2013 中的设备更新规则中</A>列出的主题。</span><span class="sxs-lookup"><span data-stu-id="c9a26-109">For details about how to import, approve, reset, restore, and remove rules, see the topics listed at <A href="lync-server-2013-device-update-rules.md">Device Update rules in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-view-device-update-rules-by-using-lync-server-control-panel"></a><span data-ttu-id="c9a26-110">使用 Lync Server "控制面板" 查看设备更新规则</span><span class="sxs-lookup"><span data-stu-id="c9a26-110">To view device update rules by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="c9a26-111">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="c9a26-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="c9a26-112">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="c9a26-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c9a26-113">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="c9a26-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c9a26-114">在左侧导航栏中，单击 " **客户端**"，然后单击 " **设备更新** " 导航按钮。</span><span class="sxs-lookup"><span data-stu-id="c9a26-114">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span> <span data-ttu-id="c9a26-115">" **设备更新** " 页面上列出了导入的规则。</span><span class="sxs-lookup"><span data-stu-id="c9a26-115">Imported rules are listed on the **Device Update** page.</span></span>

</div>

<div>

## <a name="viewing-device-update-rules-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="c9a26-116">使用 Windows PowerShell Cmdlet 查看设备更新规则</span><span class="sxs-lookup"><span data-stu-id="c9a26-116">Viewing Device Update Rules by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="c9a26-117">还可以使用 Windows PowerShell 和 **CsDeviceUpdateRule** cmdlet 查看有关所有设备更新规则的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c9a26-117">Detailed information about all your device update rules can also be viewed by using Windows PowerShell and the **Get-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="c9a26-118">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="c9a26-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c9a26-119">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> 。</span><span class="sxs-lookup"><span data-stu-id="c9a26-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-view-all-your-device-update-rules"></a><span data-ttu-id="c9a26-120">查看所有设备更新规则</span><span class="sxs-lookup"><span data-stu-id="c9a26-120">To view all your device update rules</span></span>

  - <span data-ttu-id="c9a26-121">以下命令将返回有关所有设备更新规则的信息，这些规则已配置为在您的组织中使用：</span><span class="sxs-lookup"><span data-stu-id="c9a26-121">The following command returns information about all the device updates rules configured for use in your organization:</span></span>
    
        Get-CsDeviceUpdateRule
    
    <span data-ttu-id="c9a26-122">该命令将针对每个设备更新规则返回类似于以下内容的信息：</span><span class="sxs-lookup"><span data-stu-id="c9a26-122">The command returns information similar to the following for each of your device update rules:</span></span>
    
        Identity        : Service:WebServer:pool0.vdomain.com/2de8cbf6-9441-4f61-b755-1e4bef1effde
        Id              : 2de8cbf6-9441-4f61-b755-1e4bef1effde
        DeviceType      : UCPhone
        Brand           : Microsoft
        Model           : CPE
        Revision        : A
        Locale          : ENU
        UpdateType      : CPE
        ApprovedVersion :
        RestoreVersion  :
        PendingVersion  : 4.0.7577.4066

</div>

<div>

## <a name="to-view-all-the-device-update-rules-on-a-specific-web-server"></a><span data-ttu-id="c9a26-123">查看特定 web 服务器上的所有设备更新规则</span><span class="sxs-lookup"><span data-stu-id="c9a26-123">To view all the device update rules on a specific web server</span></span>

  - <span data-ttu-id="c9a26-124">若要查看特定计算机上的设备更新规则，请使用筛选器参数，后跟服务器标识和通配符 (\*) 。</span><span class="sxs-lookup"><span data-stu-id="c9a26-124">To view the device update rules on a specific computer, use the Filter parameter followed by the server Identity and the wildcard character (\*).</span></span> <span data-ttu-id="c9a26-125">例如：</span><span class="sxs-lookup"><span data-stu-id="c9a26-125">For example:</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*"

</div>

<span data-ttu-id="c9a26-126">有关详细信息，请参阅 [CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Get-CsDeviceUpdateRule) Cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="c9a26-126">For details, see the Help topic for the [Get-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Get-CsDeviceUpdateRule) cmdlet.</span></span>

<span data-ttu-id="c9a26-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9a26-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

