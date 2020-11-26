---
title: Lync Server 2013：创建网络区域链接
description: Lync Server 2013：创建网络区域链接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create network region links
ms:assetid: f8163910-8935-475d-88a2-3aa44feb9dbe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413047(v=OCS.15)
ms:contentKeyID: 48185873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6510d252ac1534a3a8e9f14d56acc8d0d8b60a6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431895"
---
# <a name="create-network-region-links-in-lync-server-2013"></a><span data-ttu-id="52d3f-103">在 Lync Server 2013 中创建网络区域链接</span><span class="sxs-lookup"><span data-stu-id="52d3f-103">Create network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52d3f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52d3f-104">

<span> </span></span></span>

<span data-ttu-id="52d3f-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="52d3f-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="52d3f-106">网络内的区域通过物理 WAN 连接进行链接。</span><span class="sxs-lookup"><span data-stu-id="52d3f-106">Regions within a network are linked through physical WAN connectivity.</span></span> <span data-ttu-id="52d3f-107">*网络区域链接* 会在为呼叫许可控制配置的两个区域之间创建一个链接 (CAC) ，并设置这些区域之间的音频和视频流量的带宽限制。</span><span class="sxs-lookup"><span data-stu-id="52d3f-107">A *network region link* creates a link between two regions configured for call admission control (CAC) and sets the bandwidth limitations on audio and video traffic between these regions.</span></span>

<span data-ttu-id="52d3f-108">有关使用网络区域链接的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="52d3f-108">For details about working with network region links, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="52d3f-109">New-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="52d3f-109">New-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegionLink)

  - [<span data-ttu-id="52d3f-110">Get-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="52d3f-110">Get-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)

  - [<span data-ttu-id="52d3f-111">Set-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="52d3f-111">Set-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegionLink)

  - [<span data-ttu-id="52d3f-112">Remove-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="52d3f-112">Remove-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegionLink)

<span data-ttu-id="52d3f-113">示例拓扑具有一条 North America 和 APAC 区域之间的链接，以及一条 EMEA 和 APAC 区域之间的链接。</span><span class="sxs-lookup"><span data-stu-id="52d3f-113">The example topology has a link between the North America and APAC regions, and a link between the EMEA and APAC regions.</span></span> <span data-ttu-id="52d3f-114">其中每个区域链接均受 WAN 带宽的约束，如示例中的区域链接带宽信息表中所述：在规划文档的 " [Lync Server 2013" 部分中收集对呼叫许可控制的要求](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="52d3f-114">Each of these region links is constrained by WAN bandwidth, as described in Region Link Bandwidth Information table in the [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) section of the Planning documentation.</span></span>

<div>

## <a name="to-create-network-region-links-by-using-lync-server-management-shell"></a><span data-ttu-id="52d3f-115">使用 Lync Server 命令行管理程序创建网络区域链接</span><span class="sxs-lookup"><span data-stu-id="52d3f-115">To create network region links by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="52d3f-116">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="52d3f-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="52d3f-117">运行 New-CsNetworkRegionLink cmdlet 创建区域链接并应用相应的带宽策略配置文件。</span><span class="sxs-lookup"><span data-stu-id="52d3f-117">Run the New-CsNetworkRegionLink cmdlet to create the region links and apply appropriate bandwidth policy profiles.</span></span> <span data-ttu-id="52d3f-118">例如，运行：</span><span class="sxs-lookup"><span data-stu-id="52d3f-118">For example, run:</span></span>
    
      ```powershell
        New-CsNetworkRegionLink -NetworkRegionLinkID NA-EMEA-LINK -NetworkRegionID1 NorthAmerica -NetworkRegionID2 EMEA -BWPolicyProfileID 50Mb_Link
      ```
    
      ```powershell
        New-CsNetworkRegionLink -NetworkRegionLinkID EMEA-APAC-LINK -NetworkRegionID1 EMEA -NetworkRegionID2 APAC -BWPolicyProfileID 25Mb_Link
      ```

</div>

<div>

## <a name="to-create-network-region-links-by-using-lync-server-control-panel"></a><span data-ttu-id="52d3f-119">使用 Lync Server "控制面板" 创建网络区域链接</span><span class="sxs-lookup"><span data-stu-id="52d3f-119">To create network region links by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="52d3f-120">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="52d3f-120">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="52d3f-121">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="52d3f-121">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="52d3f-122">在左侧导航栏中，单击“网络配置”。</span><span class="sxs-lookup"><span data-stu-id="52d3f-122">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="52d3f-123">单击“区域链接”导航按钮。</span><span class="sxs-lookup"><span data-stu-id="52d3f-123">Click the **Region Link** navigation button.</span></span>

4.  <span data-ttu-id="52d3f-124">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="52d3f-124">Click **New**.</span></span>

5.  <span data-ttu-id="52d3f-125">在“新建区域链接”页上，单击“名称”，然后键入网络区域链接的名称。</span><span class="sxs-lookup"><span data-stu-id="52d3f-125">On the **New Region Link** page, click **Name** and then type a name for the network region link.</span></span>

6.  <span data-ttu-id="52d3f-126">单击 " **网络区域 \# 1**"，然后在列表中单击要链接到 "网络区域 2" 的网络区域 \# 。</span><span class="sxs-lookup"><span data-stu-id="52d3f-126">Click **Network Region \#1**, and then click the network region in the list that you want to link to Network Region \#2.</span></span>

7.  <span data-ttu-id="52d3f-127">单击 " **网络区域 \# 2**"，然后在列表中单击要链接到 "网络区域 1" 的网络区域 \# 。</span><span class="sxs-lookup"><span data-stu-id="52d3f-127">Click **Network Region \#2**, and then click a network region in the list that you want to link to Network Region \#1.</span></span>

8.  <span data-ttu-id="52d3f-128">也可以选择单击“带宽策略”，然后选择要应用于网络区域链接的带宽策略配置文件。</span><span class="sxs-lookup"><span data-stu-id="52d3f-128">Optionally, click **Bandwidth policy**, and then select the bandwidth policy profile that you want to apply to the network region link.</span></span>
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="52d3f-129">仅在网络区域链接受带宽限制，并且您希望使用 CAC 控制该链接上的媒体流量时，应用带宽策略。</span><span class="sxs-lookup"><span data-stu-id="52d3f-129">Apply a bandwidth policy only if the network region link is bandwidth-constrained and you want to use CAC to control media traffic on that link.</span></span>

    
    </div>

9.  <span data-ttu-id="52d3f-130">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="52d3f-130">Click **Commit**.</span></span>

10. <span data-ttu-id="52d3f-131">要为拓扑完成网络区域链接的创建，请使用其他区域的设置重复步骤 4 至 9。</span><span class="sxs-lookup"><span data-stu-id="52d3f-131">To finish creating network region links for your topology, repeat steps 4 through 9 with settings for other regions.</span></span>

<span data-ttu-id="52d3f-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52d3f-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
