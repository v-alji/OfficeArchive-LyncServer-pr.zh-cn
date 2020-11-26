---
title: Lync Server 2013：部署企业语音
description: Lync Server 2013：部署企业语音。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Enterprise Voice
ms:assetid: b5b593a6-ac30-461c-8c8c-0041e2c9ab04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412876(v=OCS.15)
ms:contentKeyID: 48185207
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5cc1c891d81db158c1d28e4a3e918a9dae37744c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430012"
---
# <a name="deploying-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="fbb35-103">在 Lync Server 2013 中部署企业语音</span><span class="sxs-lookup"><span data-stu-id="fbb35-103">Deploying Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fbb35-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fbb35-104">

<span> </span></span></span>

<span data-ttu-id="fbb35-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="fbb35-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="fbb35-106">Lync Server 2013，企业语音是 Lync Server 2013 基础结构的一部分。</span><span class="sxs-lookup"><span data-stu-id="fbb35-106">Lync Server 2013, Enterprise Voice is part of the Lync Server 2013 infrastructure.</span></span>

<span data-ttu-id="fbb35-107">部署企业语音需要：</span><span class="sxs-lookup"><span data-stu-id="fbb35-107">Deploying Enterprise Voice requires that you:</span></span>

<div id="sectionSection0" class="section">

1.  <span data-ttu-id="fbb35-108">查看规划文档的 " [Lync Server 2013 中的企业语音规划](lync-server-2013-planning-for-enterprise-voice.md) " 部分。</span><span class="sxs-lookup"><span data-stu-id="fbb35-108">Review the [Planning for Enterprise Voice in Lync Server 2013](lync-server-2013-planning-for-enterprise-voice.md) section of the Planning documentation.</span></span>

2.  <span data-ttu-id="fbb35-109">最终确定要与此工作负荷一起部署的功能和组件的计划。</span><span class="sxs-lookup"><span data-stu-id="fbb35-109">Finalize plans for features and components to deploy with this workload.</span></span>

3.  <span data-ttu-id="fbb35-110">运行规划工具以设计反映部署决策的拓扑。</span><span class="sxs-lookup"><span data-stu-id="fbb35-110">Run Planning Tool to design a topology that reflects your deployment decisions.</span></span>

4.  <span data-ttu-id="fbb35-111">如在 "部署文档" 中的 [Lync Server 2013 中定义和配置拓扑](lync-server-2013-defining-and-configuring-the-topology.md) 中所述，在拓扑生成器中打开拓扑设计。</span><span class="sxs-lookup"><span data-stu-id="fbb35-111">Open the topology design in Topology Builder, as described in [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fbb35-112">拓扑生成器的安装是内部池的部署过程的一部分。</span><span class="sxs-lookup"><span data-stu-id="fbb35-112">Installation of Topology Builder is part of the deployment process for the internal pool.</span></span> <span data-ttu-id="fbb35-113">有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-install-lync-server-administrative-tools.md">安装 Lync Server 2013 管理工具</A> 。</span><span class="sxs-lookup"><span data-stu-id="fbb35-113">For details, see <A href="lync-server-2013-install-lync-server-administrative-tools.md">Install Lync Server 2013 administrative tools</A> in the Deployment documentation.</span></span>

    
    </div>

<span data-ttu-id="fbb35-114">此外，您还必须已在中心站点和分支站点上部署了 Lync Server、企业版和与您选择部署的参考拓扑对应的分支站点。</span><span class="sxs-lookup"><span data-stu-id="fbb35-114">Additionally, you must have already deployed Lync Server, Enterprise Edition at central sites and branch sites that correspond to the reference topology that you choose to deploy.</span></span> <span data-ttu-id="fbb35-115">只有在为至少一个内部池定义、发布和安装文件后，才能部署企业语音组件，并且必须使用拓扑生成器定义和发布内部池。</span><span class="sxs-lookup"><span data-stu-id="fbb35-115">You can’t deploy Enterprise Voice components until you have defined, published, and installed files for at least one internal pool, and you must use Topology Builder to define and publish an internal pool.</span></span>

</div>

<div id="sectionSection1" class="section">

<div class="subSection">

<span data-ttu-id="fbb35-116">若要查看可在何处部署企业语音服务器角色的参考拓扑 (以及它们与其他 Lync Server 2013 服务器角色) 的关系，请参阅规划文档中 [Lync server 2013 中的参考拓扑](lync-server-2013-reference-topologies.md) 。</span><span class="sxs-lookup"><span data-stu-id="fbb35-116">To view reference topologies with examples of where Enterprise Voice server roles can be deployed (and their relationship to one another and other Lync Server 2013 server roles), see [Reference topologies in Lync Server 2013](lync-server-2013-reference-topologies.md) in the Planning documentation.</span></span>

<span data-ttu-id="fbb35-117">若要查看阐释和解释一个示例呼叫许可控制部署（包括网络区域、网络站点和子网）的参考拓扑，请参阅在 "规划" 文档中 [收集 Lync Server 2013 中的呼叫许可控制要求](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="fbb35-117">To view a reference topology that illustrates and explains a sample call admission control deployment, including network regions, network sites, and subnets, see [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) in the Planning documentation.</span></span>

</div>

</div>

<div id="sectionSection2" class="section">

<div>


> [!IMPORTANT]  
> <span data-ttu-id="fbb35-118">若要在中心网站部署企业语音，请继续阅读本部分中的主题。</span><span class="sxs-lookup"><span data-stu-id="fbb35-118">To deploy Enterprise Voice at a central site, continue reading the topics in this section.</span></span> <span data-ttu-id="fbb35-119">若要在分支站点部署企业语音，请跳过部署文档中 <A href="lync-server-2013-deploying-branch-sites.md">Lync Server 2013 中的 "部署分支站点</A> "。</span><span class="sxs-lookup"><span data-stu-id="fbb35-119">To deploy Enterprise Voice at a branch site, skip to <A href="lync-server-2013-deploying-branch-sites.md">Deploying branch sites in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="fbb35-120">本节包含中介服务器并置到每个前端服务器或 Standard Edition Server 上的部署过程（推荐），以及独立的中介服务器池的部署过程。</span><span class="sxs-lookup"><span data-stu-id="fbb35-120">This section includes procedures for deployments in which a Mediation Server is collocated on each Front End Server or Standard Edition server, as recommended, and also for deployments with a stand-alone Mediation Server pool.</span></span>

<span data-ttu-id="fbb35-121">如果你使用拓扑生成器定义和发布在每台前端服务器或标准版服务器上 collocates 中介服务器的拓扑，则你可以跳过以下内容，因为部署向导已在安装用于前端服务器池或标准版服务器的文件时自动安装了中介服务器的文件：</span><span class="sxs-lookup"><span data-stu-id="fbb35-121">You can skip the following content if you used Topology Builder to define and publish a topology that collocates a Mediation Server on each Front End Server or Standard Edition server, because Deployment Wizard already automatically installed the files for Mediation Server when you installed files for your Front End Server pool or Standard Edition server:</span></span>

  - [<span data-ttu-id="fbb35-122">在 Lync Server 2013 中配置中继</span><span class="sxs-lookup"><span data-stu-id="fbb35-122">Configuring trunks in Lync Server 2013</span></span>](lync-server-2013-configuring-trunks.md)

<span data-ttu-id="fbb35-123">如果你使用拓扑生成器在独立池中定义和发布中介服务器，你可以使用以下内容：</span><span class="sxs-lookup"><span data-stu-id="fbb35-123">If you used Topology Builder to define and publish a Mediation Server in a stand-alone pool, you can use the following content:</span></span>

  - <span data-ttu-id="fbb35-124">验证你的拓扑是否符合 [Lync Server 2013 的企业语音先决条件](lync-server-2013-enterprise-voice-prerequisites.md)中所述的软件和环境先决条件。</span><span class="sxs-lookup"><span data-stu-id="fbb35-124">Verify that your topology meets the software and environment prerequisites, as described in [Enterprise Voice prerequisites for Lync Server 2013](lync-server-2013-enterprise-voice-prerequisites.md).</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fbb35-125">本节内容</span><span class="sxs-lookup"><span data-stu-id="fbb35-125">In This Section</span></span>

  - <span></span>  
    [<span data-ttu-id="fbb35-126">Lync Server 2013 的企业语音先决条件</span><span class="sxs-lookup"><span data-stu-id="fbb35-126">Enterprise Voice prerequisites for Lync Server 2013</span></span>](lync-server-2013-enterprise-voice-prerequisites.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-127">在 Lync Server 2013 中部署中介服务器和定义对等方</span><span class="sxs-lookup"><span data-stu-id="fbb35-127">Deploying Mediation Servers and defining peers in Lync Server 2013</span></span>](lync-server-2013-deploying-mediation-servers-and-defining-peers.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-128">在 Lync Server 2013 中配置中继</span><span class="sxs-lookup"><span data-stu-id="fbb35-128">Configuring trunks in Lync Server 2013</span></span>](lync-server-2013-configuring-trunks.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-129">在 Lync Server 2013 中配置拨号计划</span><span class="sxs-lookup"><span data-stu-id="fbb35-129">Configuring dial plans in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-plans.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-130">在 Lync Server 2013 中配置语音策略、PSTN 使用记录和语音路由</span><span class="sxs-lookup"><span data-stu-id="fbb35-130">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-131">在 Lync Server 2013 中导出和导入语音路由配置</span><span class="sxs-lookup"><span data-stu-id="fbb35-131">Exporting and importing voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-exporting-and-importing-voice-routing-configuration.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-132">在 Lync Server 2013 中测试语音路由</span><span class="sxs-lookup"><span data-stu-id="fbb35-132">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-133">将挂起的更改发布到 Lync Server 2013 中的语音路由配置</span><span class="sxs-lookup"><span data-stu-id="fbb35-133">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-134">部署本地 Exchange UM 以提供 Lync Server 2013 语音邮件</span><span class="sxs-lookup"><span data-stu-id="fbb35-134">Deploying on-premises Exchange UM to provide Lync Server 2013 voice mail</span></span>](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-135">在托管 Exchange UM 上提供 Lync Server 2013 用户语音邮件</span><span class="sxs-lookup"><span data-stu-id="fbb35-135">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-136">配置本地 Lync Server 2013 与 Exchange Online 集成</span><span class="sxs-lookup"><span data-stu-id="fbb35-136">Configuring on-premises Lync Server 2013 integration with Exchange Online</span></span>](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-137">在 Lync Server 2013 中部署高级企业语音功能</span><span class="sxs-lookup"><span data-stu-id="fbb35-137">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)
    
      - [<span data-ttu-id="fbb35-138">关于 Lync Server 2013 中的网络区域、站点和子网</span><span class="sxs-lookup"><span data-stu-id="fbb35-138">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)
    
      - [<span data-ttu-id="fbb35-139">在 Lync Server 2013 中创建或修改网络区域</span><span class="sxs-lookup"><span data-stu-id="fbb35-139">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)
    
      - [<span data-ttu-id="fbb35-140">在 Lync Server 2013 中创建或修改网络站点</span><span class="sxs-lookup"><span data-stu-id="fbb35-140">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)
    
      - [<span data-ttu-id="fbb35-141">在 Lync Server 2013 中将子网与网络站点相关联</span><span class="sxs-lookup"><span data-stu-id="fbb35-141">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)
    
      - [<span data-ttu-id="fbb35-142">在 Lync Server 2013 中配置呼叫许可控制</span><span class="sxs-lookup"><span data-stu-id="fbb35-142">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)
    
      - [<span data-ttu-id="fbb35-143">在 Lync Server 2013 中配置增强型 9-1-1</span><span class="sxs-lookup"><span data-stu-id="fbb35-143">Configure Enhanced 9-1-1 in Lync Server 2013</span></span>](lync-server-2013-configure-enhanced-9-1-1.md)
    
      - [<span data-ttu-id="fbb35-144">在 Lync Server 2013 中配置媒体绕过</span><span class="sxs-lookup"><span data-stu-id="fbb35-144">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)

  - <span></span>  
    [<span data-ttu-id="fbb35-145">在 Lync Server 2013 中启用企业语音用户</span><span class="sxs-lookup"><span data-stu-id="fbb35-145">Enable users for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-enterprise-voice.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fbb35-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fbb35-146">See Also</span></span>


[<span data-ttu-id="fbb35-147">在 Lync Server 2013 中部署分支站点</span><span class="sxs-lookup"><span data-stu-id="fbb35-147">Deploying branch sites in Lync Server 2013</span></span>](lync-server-2013-deploying-branch-sites.md)  
[<span data-ttu-id="fbb35-148">在 Lync Server 2013 中配置拨入式会议</span><span class="sxs-lookup"><span data-stu-id="fbb35-148">Configuring dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-in-conferencing.md)  
[<span data-ttu-id="fbb35-149">在 Lync Server 2013 中配置呼叫寄存</span><span class="sxs-lookup"><span data-stu-id="fbb35-149">Configuring Call Park in Lync Server 2013</span></span>](lync-server-2013-configuring-call-park.md)  
[<span data-ttu-id="fbb35-150">在 Lync Server 2013 中配置未分配号码的通知</span><span class="sxs-lookup"><span data-stu-id="fbb35-150">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-configuring-announcements-for-unassigned-numbers.md)  
[<span data-ttu-id="fbb35-151">在 Lync Server 2013 中部署监视</span><span class="sxs-lookup"><span data-stu-id="fbb35-151">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="fbb35-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fbb35-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

