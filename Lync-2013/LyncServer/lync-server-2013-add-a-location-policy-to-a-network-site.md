---
title: Lync Server 2013：向网络网站添加位置策略
description: Lync Server 2013：将位置策略添加到网络网站。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add a location policy to a network site
ms:assetid: 43bfab8a-3d6b-4ca4-8425-879fd910502e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425936(v=OCS.15)
ms:contentKeyID: 48183980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20f71d3144e2ef730de5dae46be16138b5d36c42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439393"
---
# <a name="add-a-location-policy-to-a-network-site-in-lync-server-2013"></a><span data-ttu-id="bb6d8-103">在 Lync Server 2013 中将位置策略添加到网络网站</span><span class="sxs-lookup"><span data-stu-id="bb6d8-103">Add a location policy to a network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb6d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb6d8-104">

<span> </span></span></span>

<span data-ttu-id="bb6d8-105">_**主题上次修改时间：** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="bb6d8-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="bb6d8-106">以下示例显示了如何将在 [Lync Server 2013 的创建位置](lync-server-2013-create-location-policies.md)策略中定义的 **Redmond** 位置策略添加到现有网络网站，以及如何创建使用 **雷德蒙** 的位置策略的新网络网站。</span><span class="sxs-lookup"><span data-stu-id="bb6d8-106">The following examples show how to add the **Redmond** location policy defined in [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md) to an existing network site and how to create a new network site that uses the **Redmond** location policy.</span></span>

<span data-ttu-id="bb6d8-107">有关使用网络站点的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="bb6d8-107">For details about working with network sites, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="bb6d8-108">**New-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="bb6d8-108">**New-CsNetworkSite**</span></span>

  - <span data-ttu-id="bb6d8-109">**Get-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="bb6d8-109">**Get-CsNetworkSite**</span></span>

  - <span data-ttu-id="bb6d8-110">**Set-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="bb6d8-110">**Set-CsNetworkSite**</span></span>

  - <span data-ttu-id="bb6d8-111">**Remove-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="bb6d8-111">**Remove-CsNetworkSite**</span></span>

<div>

## <a name="to-assign-a-location-policy-to-an-existing-network-site"></a><span data-ttu-id="bb6d8-112">为现有网络站点分配位置策略</span><span class="sxs-lookup"><span data-stu-id="bb6d8-112">To assign a location policy to an existing network site</span></span>

1.  <span data-ttu-id="bb6d8-113">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="bb6d8-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="bb6d8-114">运行以下 cmdlet 以修改现有网络站点。</span><span class="sxs-lookup"><span data-stu-id="bb6d8-114">Run the following cmdlets to modify an existing network site.</span></span>
    
    <span data-ttu-id="bb6d8-115">将带 **Redmond** 标记的位置策略分配给名为 **Redmond** 的现有网络站点。</span><span class="sxs-lookup"><span data-stu-id="bb6d8-115">Assign the **Redmond** tagged Location policy to an existing network site named **Redmond**.</span></span>
    
        Set-CsNetworkSite -Identity "Redmond" -NetworkRegionID "NorthAmerica" -LocationPolicy "Redmond"

</div>

<div>

## <a name="to-assign-a-location-policy-to-a-new-network-site"></a><span data-ttu-id="bb6d8-116">为新的网络站点分配位置策略</span><span class="sxs-lookup"><span data-stu-id="bb6d8-116">To assign a location policy to a new network site</span></span>

1.  <span data-ttu-id="bb6d8-117">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="bb6d8-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="bb6d8-118">运行以下 cmdlet 以创建新的网络站点。</span><span class="sxs-lookup"><span data-stu-id="bb6d8-118">Run the following cmdlet to create a new network site.</span></span>
    
    <span data-ttu-id="bb6d8-119">在网络区域中创建新的网络站点，并分配带 **Redmond** 标记的位置策略。</span><span class="sxs-lookup"><span data-stu-id="bb6d8-119">Create a new network site in the network region and assign the **Redmond** tagged Location policy.</span></span>
    
        New-CsNetworkSite -Identity "Redmond" -NetworkRegionID "NorthAmerica" -LocationPolicy "Redmond"

<span data-ttu-id="bb6d8-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb6d8-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

