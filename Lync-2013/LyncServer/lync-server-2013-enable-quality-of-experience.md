---
title: Lync Server 2013：启用体验质量
description: Lync Server 2013：启用体验质量。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Quality of Experience
ms:assetid: c8bb3c67-b324-4d94-8158-00c792c7ac42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182583(v=OCS.15)
ms:contentKeyID: 48185385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43746227395477596ff5e39809cf819c110287ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437530"
---
# <a name="enable-quality-of-experience-in-lync-server-2013"></a><span data-ttu-id="f978e-103">在 Lync Server 2013 中启用体验质量</span><span class="sxs-lookup"><span data-stu-id="f978e-103">Enable Quality of Experience in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f978e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f978e-104">

<span> </span></span></span>

<span data-ttu-id="f978e-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f978e-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f978e-106">用户体验质量 (QoE) 记录指示媒体质量以及有关呼叫和会话中所涉及参与者、设备名称、驱动程序、IP 地址和终结点类型的信息的数值型数据。</span><span class="sxs-lookup"><span data-stu-id="f978e-106">Quality of Experience (QoE) records numeric data that indicates the media quality and information about participants, device names, drivers, IP addresses, and endpoint types involved in calls and sessions.</span></span> <span data-ttu-id="f978e-107">有关详细信息，请参阅规划文档中的 [在 Lync Server 2013 中进行监视](lync-server-2013-planning-for-monitoring.md) 。</span><span class="sxs-lookup"><span data-stu-id="f978e-107">For details, see [Planning for monitoring in Lync Server 2013](lync-server-2013-planning-for-monitoring.md) in the Planning documentation.</span></span>

<span data-ttu-id="f978e-108">使用以下过程为整个组织或组织中的每个站点启用 QoE。</span><span class="sxs-lookup"><span data-stu-id="f978e-108">Use the following procedure to enable QoE for your whole organization or each site in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f978e-109">为了启用 QoE，必须首先配置监控和监控后端数据库。</span><span class="sxs-lookup"><span data-stu-id="f978e-109">To enable QoE, you must first configure monitoring and a monitoring back-end database.</span></span> <span data-ttu-id="f978e-110">有关详细信息，请参阅 <A href="lync-server-2013-deploying-monitoring.md">在 Lync Server 2013 中部署监视</A>。</span><span class="sxs-lookup"><span data-stu-id="f978e-110">For details, see <A href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-qoe-by-using-lync-server-control-panel"></a><span data-ttu-id="f978e-111">使用 Lync Server "控制面板" 启用 QoE</span><span class="sxs-lookup"><span data-stu-id="f978e-111">To enable QoE by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="f978e-112">从属于 RTCUniversalServerAdmins 组成员的用户帐户 (或具有等效的用户权限) 或分配给 CsServerAdministrator 或 CsAdministrator 角色，请登录到你部署 Lync Server 2013 的网络中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="f978e-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="f978e-113">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="f978e-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f978e-114">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="f978e-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f978e-115">在左侧导航栏中，单击“**监控和存档**”，然后单击“**用户体验质量数据**”。</span><span class="sxs-lookup"><span data-stu-id="f978e-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="f978e-116">在“**用户体验质量数据**”页上，单击表中相应的集合，再单击“**操作**”，然后单击“**启用 QoE**”。</span><span class="sxs-lookup"><span data-stu-id="f978e-116">On the **Quality of Experience Data** page, click the appropriate collection from the table, click **Action**, and then click **Enable QoE**.</span></span>

</div>

<div>

## <a name="enabling-qoe-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="f978e-117">使用 Windows PowerShell Cmdlet 启用 QoE</span><span class="sxs-lookup"><span data-stu-id="f978e-117">Enabling QoE by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="f978e-118">你可以使用 Windows PowerShell 和 **CsQoEConfiguration** Cmdlet 启用 QoE。</span><span class="sxs-lookup"><span data-stu-id="f978e-118">You can enable QoE by using Windows PowerShell and the **Set-CsQoEConfiguration** cmdlet.</span></span> <span data-ttu-id="f978e-119">你可以从 Lync Server 2013 命令行管理程序或 Windows PowerShell 的远程会话运行此 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f978e-119">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="f978e-120">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="f978e-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-qoe-for-a-single-location"></a><span data-ttu-id="f978e-121">对单个位置启用 QoE</span><span class="sxs-lookup"><span data-stu-id="f978e-121">To enable QoE for a single location</span></span>

  - <span data-ttu-id="f978e-122">要启用 QoE，请将 EnableQoE 参数设置为 True ($True)。</span><span class="sxs-lookup"><span data-stu-id="f978e-122">To enable QoE, set the EnableQoE parameter to True ($True).</span></span>
    
        Set-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $True

</div>

<div>

## <a name="to-disable-qoe-for-a-single-location"></a><span data-ttu-id="f978e-123">对单个位置禁用 QoE</span><span class="sxs-lookup"><span data-stu-id="f978e-123">To disable QoE for a single location</span></span>

  - <span data-ttu-id="f978e-p105">要禁用 QoE，请将 EnableQoE 参数设置为 False ($False)。这不会卸载监控。但会暂停 QoE 数据的收集和存储。</span><span class="sxs-lookup"><span data-stu-id="f978e-p105">To disable QoE, set the EnableQoE parameter to False ($False). This does not uninstall monitoring. It pauses the collection and storage of QoE data.</span></span>
    
        Set-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $False

</div>

<div>

## <a name="to-use-a-single-command-to-enable-qoe-in-multiple-locations"></a><span data-ttu-id="f978e-127">使用单个命令在多个位置启用 QoE</span><span class="sxs-lookup"><span data-stu-id="f978e-127">To use a single command to enable QoE in multiple locations</span></span>

  - <span data-ttu-id="f978e-128">以下命令可对组织中当前使用的所有 QoE 配置设置启用 QoE。</span><span class="sxs-lookup"><span data-stu-id="f978e-128">This command enables QoE for all the QoE configuration settings currently in use in your organization.</span></span>
    
        Get-CsQoEConfiguration | Set-CsQoEConfiguration "site:Redmond" -EnableQoE $True

</div>

<span data-ttu-id="f978e-129">有关详细信息，请参阅 [Set-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsQoEConfiguration)。</span><span class="sxs-lookup"><span data-stu-id="f978e-129">For details, see [Set-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsQoEConfiguration).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f978e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f978e-130">See Also</span></span>


[<span data-ttu-id="f978e-131">在 Lync Server 2013 中规划监控</span><span class="sxs-lookup"><span data-stu-id="f978e-131">Planning for monitoring in Lync Server 2013</span></span>](lync-server-2013-planning-for-monitoring.md)  
[<span data-ttu-id="f978e-132">在 Lync Server 2013 中部署监视</span><span class="sxs-lookup"><span data-stu-id="f978e-132">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="f978e-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f978e-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

