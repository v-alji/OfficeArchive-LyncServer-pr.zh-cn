---
title: Lync Server 2013：在拓扑中定义可选控制器拓扑
description: Lync Server 2013：定义拓扑中的可选导演拓扑。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define optional Director topologies in your topology
ms:assetid: 8e9a659d-23b0-401d-b296-59c7df414d49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398717(v=OCS.15)
ms:contentKeyID: 48184808
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bc82108d4277969489739fc81db07ec6f96bb96
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431048"
---
# <a name="define-optional-director-topologies-in-your-topology-for-lync-server-2013"></a><span data-ttu-id="8a1a3-103">针对 Lync Server 2013 在拓扑中定义可选控制器拓扑</span><span class="sxs-lookup"><span data-stu-id="8a1a3-103">Define optional Director topologies in your topology for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a1a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a1a3-104">

<span> </span></span></span>

<span data-ttu-id="8a1a3-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="8a1a3-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="8a1a3-106">Lync Server 2013 控制器可以是单实例服务器，也可以作为多个控制器的负载平衡池进行安装以实现更高的可用性和容量。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-106">Lync Server 2013 Directors can be single-instance servers or they can be installed as a load-balanced pool of multiple Directors for higher availability and capacity.</span></span> <span data-ttu-id="8a1a3-107">硬件负载平衡和域名系统 (的 DNS) 负载平衡均受支持。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-107">Both hardware load balancing and Domain Name System (DNS) load balancing are supported.</span></span> <span data-ttu-id="8a1a3-108">本主题介绍如何为控制器池配置 DNS 负载平衡。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-108">This topic explains how to configure DNS load balancing for Director pools.</span></span>

<span data-ttu-id="8a1a3-109">若要在添加或删除服务器角色时成功发布、启用或禁用拓扑，您应以 **RTCUniversalServerAdmins** 和 **域管理员** 组成员的用户身份登录。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-109">To successfully publish, enable, or disable a topology when you add or remove a server role, you should be logged on as a user who is a member of the **RTCUniversalServerAdmins** and **Domain Admins** groups.</span></span> <span data-ttu-id="8a1a3-110">你还可以委派适当的管理员权限来添加服务器角色。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-110">You can also delegate the proper administrator rights and permissions for adding server roles.</span></span> <span data-ttu-id="8a1a3-111">有关详细信息，请参阅在标准版服务器或企业版服务器部署文档中 [Lync Server 2013 中的 "委派设置权限](lync-server-2013-delegate-setup-permissions.md) "。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-111">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="8a1a3-112">对于其他配置更改，仅需要 **RTCUniversalServerAdmins** 组中的成员身份。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-112">For other configuration changes, only membership in the **RTCUniversalServerAdmins** group is required.</span></span>

<span data-ttu-id="8a1a3-113">本主题介绍了为两个控制器拓扑定义和发布拓扑的步骤：</span><span class="sxs-lookup"><span data-stu-id="8a1a3-113">This topic describes the steps to define and publish the topology for the two Director topologies:</span></span>

  - <span data-ttu-id="8a1a3-114">若要定义 Director (单实例) </span><span class="sxs-lookup"><span data-stu-id="8a1a3-114">To define the Director (single instance)</span></span>

  - <span data-ttu-id="8a1a3-115">若要定义控制器 (多个控制器池) </span><span class="sxs-lookup"><span data-stu-id="8a1a3-115">To define the Director (multiple Director pool)</span></span>

<div>

## <a name="to-define-the-director-single-instance"></a><span data-ttu-id="8a1a3-116">若要定义 Director (单实例) </span><span class="sxs-lookup"><span data-stu-id="8a1a3-116">To define the Director (single instance)</span></span>

1.  <span data-ttu-id="8a1a3-117">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-117">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="8a1a3-118">在 "欢迎" 页面上，单击 " **从现有部署下载拓扑**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-118">On the welcome page, click **Download Topology from Existing Deployment**.</span></span>

3.  <span data-ttu-id="8a1a3-119">在 " **将拓扑另存为** " 对话框中，键入现有拓扑的本地副本的名称和位置，然后单击 " **保存**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-119">In the **Save Topology As** dialog box, type the name and location of the local copy of the existing topology, and then click **Save**.</span></span>

4.  <span data-ttu-id="8a1a3-120">展开计划添加 Director 的网站，右键单击 " **控制器池**"，然后单击 " **新建控制器池**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-120">Expand the site in which you plan to add the Director, right-click **Director pools**, and then click **New Director Pool**.</span></span>

5.  <span data-ttu-id="8a1a3-121">在 " **定义控制器池 FQDN** " 对话框中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="8a1a3-121">In the **Define the Director pool FQDN** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="8a1a3-122">在 " **池 FQDN**" 中，键入 Director 池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-122">In **Pool FQDN**, type the FQDN for the Director pool.</span></span>
    
      - <span data-ttu-id="8a1a3-123">单击 " **单计算机池**"，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-123">Click **Single computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="8a1a3-124">在 " **定义文件共享** " 对话框中，执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="8a1a3-124">In the **Define the file share** dialog box, do one of the following:</span></span>
    
    1.  <span data-ttu-id="8a1a3-125">若要使用现有文件共享，请单击 " **使用以前定义的文件共享**"，从列表中选择文件共享，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-125">To use an existing file share, click **Use a previously defined file share**, select a file share from the list, and then click **Next**.</span></span>
    
    2.  <span data-ttu-id="8a1a3-126">若要创建新的文件共享，请单击 " **定义新的文件共享**"，在 " **文件服务器 FQDN**" 中键入文件共享位置的 FQDN，在 " **文件共享**" 中键入共享的名称，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-126">To create a new file share, click **Define a new file share**, type the FQDN for the location of the file share in **File Server FQDN**, type the name of the share in **File Share**, and then click **Next**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8a1a3-127">您在此步骤中指定或创建的文件共享必须存在或在发布拓扑之前创建。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-127">The file share that you specify or create in this step must exist or be created prior to publishing the topology.</span></span><BR><span data-ttu-id="8a1a3-128">不会实际使用分配给 Director 的文件共享，因此你可以分配组织中任何池的文件共享。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-128">The file share assigned to a Director is not actually used, so you can assign the file share of any pool in the organization.</span></span>

    
    </div>

7.  <span data-ttu-id="8a1a3-129">在 " **指定 Web 服务 URL** " 对话框的 " **外部基础 URL**" 中，指定控制器的 FQDN，然后单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-129">In the **Specify the Web Services URL** dialog box, in **External Base URL**, specify the FQDN for the Directors, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8a1a3-130">该名称必须可从 Internet DNS 服务器解析，并指向反向代理的公共 IP 地址，后者侦听该 URL 的 HTTP/HTTPS 请求并将它们代理到该 Director 上的外部 Web 服务虚拟目录。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-130">The name must be resolvable from Internet DNS servers and point to the public IP address of the reverse proxy, which listens for HTTP/HTTPS requests to that URL and proxies them to the external Web Services virtual directory on that Director.</span></span>

    
    </div>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="8a1a3-131">如果您有多个前端池或前端服务器，则外部 Web 服务 FQDN 必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-131">If you have more than one Front End pool or Front End Server the external Web services FQDN must be unique.</span></span> <span data-ttu-id="8a1a3-132">例如，如果你将前端服务器的外部 Web 服务 FQDN 定义为 <STRONG>pool01.contoso.com</STRONG>，则不能将 <STRONG>Pool01.contoso.com</STRONG> 用于其他前端池或前端服务器。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-132">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span> <span data-ttu-id="8a1a3-133">如果你还部署控制器，则为任何控制器或控制器池定义的外部 Web 服务 FQDN 必须是任何其他 Director 或控制器池以及任何前端池或前端服务器的唯一。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-133">If you are also deploying Directors, the external Web services FQDN defined for any Director or Director pool must be unique from any other Director or Director pool as well as any Front End pool or Front End Server.</span></span> <span data-ttu-id="8a1a3-134">如果决定使用自定义的 FQDN 替代内部 web 服务，则每个 FQDN 都必须与任何其他前端池、Director 或控制器池唯一。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-134">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

8.  <span data-ttu-id="8a1a3-135">发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-135">Publish the topology.</span></span>

</div>

<div>

## <a name="to-define-the-director-multiple-director-pool"></a><span data-ttu-id="8a1a3-136">若要定义控制器 (多个控制器池) </span><span class="sxs-lookup"><span data-stu-id="8a1a3-136">To define the Director (multiple Director pool)</span></span>

1.  <span data-ttu-id="8a1a3-137">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-137">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="8a1a3-138">在 "欢迎" 页面上，单击 " **从现有部署下载拓扑**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-138">On the welcome page, click **Download Topology from Existing Deployment**.</span></span>

3.  <span data-ttu-id="8a1a3-139">在 " **将拓扑另存为** " 对话框中，键入现有拓扑的本地副本的名称和位置，然后单击 " **保存**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-139">In the **Save Topology As** dialog box, type the name and location of the local copy of the existing topology, and then click **Save**.</span></span>

4.  <span data-ttu-id="8a1a3-140">展开计划添加 Director 的网站，右键单击 " **控制器池**"，然后单击 " **新建控制器池**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-140">Expand the site in which you plan to add the Director, right-click **Director pools**, and then click **New Director Pool**.</span></span>

5.  <span data-ttu-id="8a1a3-141">在 " **定义控制器池 FQDN** " 对话框中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="8a1a3-141">In the **Define the Director pool FQDN** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="8a1a3-142">在 " **池 FQDN**" 中，键入 Director 池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-142">In **Pool FQDN**, type the FQDN for the Director pool.</span></span>
    
      - <span data-ttu-id="8a1a3-143">单击 " **多台计算机池**"，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-143">Click **Multiple computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="8a1a3-144">在 " **定义此池内的计算机** " 对话框中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="8a1a3-144">In the **Define the computers in this pool** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="8a1a3-145">指定第一个池成员的计算机 FQDN，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-145">Specify the computer FQDN of the first pool member, and then click **Add**.</span></span>
    
      - <span data-ttu-id="8a1a3-146">对要添加的每台计算机重复上一步骤。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-146">Repeat the previous step for each computer that you want to add.</span></span> <span data-ttu-id="8a1a3-147">完成后，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-147">When you are finished, click **Next**.</span></span>

7.  <span data-ttu-id="8a1a3-148">在 " **定义文件共享** " 对话框中，执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="8a1a3-148">In the **Define the file share** dialog box, do one of the following:</span></span>
    
      - <span data-ttu-id="8a1a3-149">若要使用现有文件共享，请单击 " **使用以前定义的文件共享**"，从列表中选择文件共享，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-149">To use an existing file share, click **Use a previously defined file share**, select a file share from the list, and then click **Next**.</span></span>
    
      - <span data-ttu-id="8a1a3-150">若要创建新的文件共享，请单击 " **定义新的文件共享**"，在 " **文件服务器 FQDN**" 中键入文件共享位置的 FQDN，在 " **文件共享**" 中键入共享的名称，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-150">To create a new file share, click **Define a new file share**, type the FQDN for the location of the file share in **File Server FQDN**, type the name of the share in **File Share**, and then click **Next**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8a1a3-151">您在此步骤中指定或创建的文件共享必须存在或在发布拓扑之前创建。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-151">The file share that you specify or create in this step must exist or be created prior to publishing the topology.</span></span><BR><span data-ttu-id="8a1a3-152">不会实际使用分配给 Director 的文件共享，因此你可以分配组织中任何池的文件共享。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-152">The file share assigned to a Director is not actually used, so you can assign the file share of any pool in the organization.</span></span>

    
    </div>

8.  <span data-ttu-id="8a1a3-153">在 " **指定 Web 服务 URL** " 对话框的 " **外部基础 URL**" 中，指定控制器的 FQDN，然后单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-153">In the **Specify the Web Services URL** dialog box, in **External Base URL**, specify the FQDN for the Directors, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8a1a3-154">该名称必须可从 Internet DNS 服务器解析，并指向反向代理的公共 IP 地址，后者侦听发送到该 URL 的 HTTP/HTTPS 请求，并将它们代理到该 Director 池中的外部 Web 服务虚拟目录。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-154">The name must be resolvable from Internet DNS servers and point to the public IP address of the reverse proxy, which listens for HTTP/HTTPS requests sent to that URL and proxies them to the external Web Services virtual directory on that Director pool.</span></span>

    
    </div>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="8a1a3-155">如果您有多个前端池或前端服务器，则外部 Web 服务 FQDN 必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-155">If you have more than one Front End pool or Front End Server the external Web services FQDN must be unique.</span></span> <span data-ttu-id="8a1a3-156">例如，如果你将前端服务器的外部 Web 服务 FQDN 定义为 <STRONG>pool01.contoso.com</STRONG>，则不能将 <STRONG>Pool01.contoso.com</STRONG> 用于其他前端池或前端服务器。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-156">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span> <span data-ttu-id="8a1a3-157">如果你还部署控制器，则为任何控制器或控制器池定义的外部 Web 服务 FQDN 必须是任何其他 Director 或控制器池以及任何前端池或前端服务器的唯一。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-157">If you are also deploying Directors, the external Web services FQDN defined for any Director or Director pool must be unique from any other Director or Director pool as well as any Front End pool or Front End Server.</span></span> <span data-ttu-id="8a1a3-158">如果决定使用自定义的 FQDN 替代内部 web 服务，则每个 FQDN 都必须与任何其他前端池、Director 或控制器池唯一。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-158">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

9.  <span data-ttu-id="8a1a3-159">发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="8a1a3-159">Publish the topology.</span></span>

<span data-ttu-id="8a1a3-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a1a3-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

