---
title: Lync Server 2013：创建网络站点间策略
description: Lync Server 2013：创建网络站点间策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create network intersite policies
ms:assetid: b0714aae-55dc-4587-b718-34a03f596b22
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412844(v=OCS.15)
ms:contentKeyID: 48185148
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9666efcb9c6da459a8e50eeae66cd1a513b46f65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431937"
---
# <a name="create-network-intersite-policies-in-lync-server-2013"></a><span data-ttu-id="a3a36-103">在 Lync Server 2013 中创建网络站点间策略</span><span class="sxs-lookup"><span data-stu-id="a3a36-103">Create network intersite policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3a36-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3a36-104">

<span> </span></span></span>

<span data-ttu-id="a3a36-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="a3a36-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="a3a36-106">*网络站点间策略* 定义具有直接 WAN 链接的站点之间的带宽限制。</span><span class="sxs-lookup"><span data-stu-id="a3a36-106">A *network intersite policy* defines bandwidth limitations between sites that have direct WAN links between them.</span></span>

<span data-ttu-id="a3a36-107">有关详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="a3a36-107">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="a3a36-108">New-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="a3a36-108">New-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="a3a36-109">Get-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="a3a36-109">Get-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="a3a36-110">Set-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="a3a36-110">Set-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="a3a36-111">Remove-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="a3a36-111">Remove-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy)

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a3a36-112">只有当两个网络站点之间有直接交叉链接时， <EM>才</EM> 需要网络站点间策略。</span><span class="sxs-lookup"><span data-stu-id="a3a36-112">A network intersite policy is required <EM>only</EM> if there is a direct cross link between two network sites.</span></span>



</div>

<span data-ttu-id="a3a36-113">在示例拓扑北美区域中，Reno 和 Albuquerque 站点之间具有直接链接。</span><span class="sxs-lookup"><span data-stu-id="a3a36-113">In the example topology North America region, there is a direct link between the Reno and Albuquerque sites.</span></span> <span data-ttu-id="a3a36-114">这两个网站需要应用相应带宽策略配置文件的站点间策略。</span><span class="sxs-lookup"><span data-stu-id="a3a36-114">These two sites require an intersite policy that applies an appropriate bandwidth policy profile.</span></span> <span data-ttu-id="a3a36-115">下面的示例应用 20Mb \_ 链接配置文件。</span><span class="sxs-lookup"><span data-stu-id="a3a36-115">The following example applies the 20Mb\_Link profile.</span></span>

<div>

## <a name="to-create-a-network-intersite-policy"></a><span data-ttu-id="a3a36-116">创建网络站点间策略</span><span class="sxs-lookup"><span data-stu-id="a3a36-116">To create a network intersite policy</span></span>

1.  <span data-ttu-id="a3a36-117">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="a3a36-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a3a36-118">运行 New-CsNetworkInterSitePolicy cmdlet 以创建网络站点间策略，并为具有直接交叉链接的两个站点应用相应的带宽策略配置文件。</span><span class="sxs-lookup"><span data-stu-id="a3a36-118">Run the New-CsNetworkInterSitePolicy cmdlet to create network intersite policies and apply an appropriate bandwidth policy profile for two sites that have a direct cross link.</span></span> <span data-ttu-id="a3a36-119">例如，运行：</span><span class="sxs-lookup"><span data-stu-id="a3a36-119">For example, run:</span></span>
    
        New-CsNetworkInterSitePolicy -InterNetworkSitePolicyID Reno_Albuquerque -NetworkSiteID1 Reno -NetworkSiteID2 Albuquerque -BWPolicyProfileID 20Mb_Link

3.  <span data-ttu-id="a3a36-120">根据需要重复步骤2，以便为具有直接交叉链接的所有网络站点对创建网络站点间策略。</span><span class="sxs-lookup"><span data-stu-id="a3a36-120">Repeat step 2 as needed to create network intersite policies for all network sites pairs that have a direct cross link.</span></span>

<span data-ttu-id="a3a36-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3a36-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

