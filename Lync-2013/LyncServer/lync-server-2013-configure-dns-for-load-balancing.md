---
title: Lync Server 2013：配置 DNS 负载平衡
description: Lync Server 2013：为负载平衡配置 DNS。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS for load balancing
ms:assetid: 1b2e8414-8676-4872-8ecf-ea07196f74de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398251(v=OCS.15)
ms:contentKeyID: 48183540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b13db22d65ee67723ebc0a31544137d467d5c6b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392400"
---
# <a name="configure-dns-for-load-balancing-in-lync-server-2013"></a><span data-ttu-id="caeef-103">在 Lync Server 2013 中配置 DNS 负载平衡</span><span class="sxs-lookup"><span data-stu-id="caeef-103">Configure DNS for load balancing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="caeef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="caeef-104">

<span> </span></span></span>

<span data-ttu-id="caeef-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="caeef-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="caeef-106">若要成功完成此过程，你应至少作为域管理员组的成员或 DnsAdmins 组的成员登录到服务器或域。</span><span class="sxs-lookup"><span data-stu-id="caeef-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="caeef-107">域名系统 (DNS) 负载平衡平衡 Lync Server 2013 （如 SIP 流量和媒体流量）独有的网络流量。</span><span class="sxs-lookup"><span data-stu-id="caeef-107">Domain Name System (DNS) Load Balancing balances the network traffic that is unique to Lync Server 2013, such as SIP traffic and media traffic.</span></span> <span data-ttu-id="caeef-108">对于前端池、边缘池、控制器池和独立的中介池，DNS 负载平衡受支持。</span><span class="sxs-lookup"><span data-stu-id="caeef-108">DNS load balancing is supported for Front End pools, Edge pools, Director pools, and stand-alone Mediation pools.</span></span> <span data-ttu-id="caeef-109">配置为使用 DNS 负载平衡的池必须具有两个完全限定的域名 (Fqdn) 定义的名称：由 DNS 负载平衡 (使用的常规池 FQDN 例如，pool1.contoso.com) 和解析为池中服务器的物理 Ip 的常规池 FQDN，以及池的 Web 服务的另一个 FQDN (例如，web1.contoso.net ") "，它可以解析为池的虚拟 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="caeef-109">A pool that is configured to use DNS load balancing must have two fully qualified domain names (FQDNs) defined: the regular pool FQDN that is used by DNS load balancing (for example, pool1.contoso.com) and that resolves to the physical IPs of the servers in the pool, and another FQDN for the pool’s Web Services (for example, web1.contoso.net), which resolves to the virtual IP address of the pool.</span></span> <span data-ttu-id="caeef-110">有关 DNS 负载平衡的详细信息，请参阅规划文档中 [Lync Server 2013 中的 "DNS 负载平衡](lync-server-2013-dns-load-balancing.md) "。</span><span class="sxs-lookup"><span data-stu-id="caeef-110">For details about DNS Load Balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="caeef-111">客户端到服务器 HTTPS 流量仍需要硬件负载平衡。</span><span class="sxs-lookup"><span data-stu-id="caeef-111">Hardware load balancing is still required for client to server HTTPS traffic.</span></span>



</div>

<span data-ttu-id="caeef-112">在可以使用 DNS 负载平衡之前，必须执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="caeef-112">Before you can use DNS load balancing, you must do the following:</span></span>

1.  <span data-ttu-id="caeef-113">替代内部 Web 服务池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="caeef-113">Override the internal Web Services pool FQDN.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="caeef-114">如果决定使用自定义的 FQDN 替代内部 web 服务，则每个 FQDN 都必须与任何其他前端池、Director 或控制器池唯一。</span><span class="sxs-lookup"><span data-stu-id="caeef-114">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

2.  <span data-ttu-id="caeef-115">创建 DNS A 主机记录以将池 FQDN 解析为池中所有服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="caeef-115">Create DNS A host records to resolve the pool FQDN to the IP addresses of all the servers in the pool.</span></span>

3.  <span data-ttu-id="caeef-116">启用 IP 地址随机化，或者对于 Windows Server DNS，启用循环复用。</span><span class="sxs-lookup"><span data-stu-id="caeef-116">Enable IP Address randomization or, for Windows Server DNS, enable round robin.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="caeef-117">默认情况下，应启用循环复用。</span><span class="sxs-lookup"><span data-stu-id="caeef-117">Round robin should be enabled by default.</span></span>

    
    </div>

<div>

## <a name="to-override-internal-web-services-fqdn"></a><span data-ttu-id="caeef-118">替代内部 Web 服务 FQDN</span><span class="sxs-lookup"><span data-stu-id="caeef-118">To override internal Web services FQDN</span></span>

1.  <span data-ttu-id="caeef-119">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="caeef-119">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="caeef-120">从控制台树中，展开 "企业版前端池" 节点。</span><span class="sxs-lookup"><span data-stu-id="caeef-120">From the console tree, expand the Enterprise Edition Front End pools node.</span></span>

3.  <span data-ttu-id="caeef-121">右键单击该池，单击 " **编辑属性**"，然后单击 " **Web 服务**"。</span><span class="sxs-lookup"><span data-stu-id="caeef-121">Right-click the pool, click **Edit Properties**, and then click **Web Services**.</span></span>

4.  <span data-ttu-id="caeef-122">在 " **内部 web 服务**" 下，选中 " **替代 FQDN** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="caeef-122">Below **Internal web services**, select the **Override FQDN** check box.</span></span>

5.  <span data-ttu-id="caeef-123">键入将解析为池中服务器的物理 IP 地址的池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="caeef-123">Type the pool FQDN that resolves to the physical IP addresses of the servers in the pool.</span></span>

6.  <span data-ttu-id="caeef-124">在 " **外部 web 服务**" 下，键入解析为池的虚拟 IP 地址的外部池 FQDN，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="caeef-124">Below **External web services**, type the external pool FQDN that resolves to the virtual IP addresses of the pool, and then click **OK**.</span></span>

7.  <span data-ttu-id="caeef-125">在控制台树中，单击 " **Lync Server 2013**"，然后在 " **操作** " 窗格中，单击 " **发布拓扑**"。</span><span class="sxs-lookup"><span data-stu-id="caeef-125">From the console tree, click **Lync Server 2013**, and then in the **Actions** pane, click **Publish Topology**.</span></span>

</div>

<div>

## <a name="to-create-dns-host-a-records-for-all-internal-pool-servers"></a><span data-ttu-id="caeef-126">若要创建 DNS 主机 (所有内部池服务器的) 记录</span><span class="sxs-lookup"><span data-stu-id="caeef-126">To create DNS Host (A) Records for all internal pool servers</span></span>

1.  <span data-ttu-id="caeef-127">单击 " **开始**"，单击 " **所有程序**"，单击 " **管理工具**"，然后单击 " **DNS**"。</span><span class="sxs-lookup"><span data-stu-id="caeef-127">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="caeef-128">在 " **DNS 管理器**" 中，单击管理记录的 DNS 服务器以将其展开。</span><span class="sxs-lookup"><span data-stu-id="caeef-128">In **DNS Manager**, click the DNS Server that manages your records to expand it.</span></span>

3.  <span data-ttu-id="caeef-129">单击 " **正向查找区域** " 将其展开。</span><span class="sxs-lookup"><span data-stu-id="caeef-129">Click **Forward Lookup Zones** to expand it.</span></span>

4.  <span data-ttu-id="caeef-130">右键单击需要添加记录的 DNS 域，然后单击 " **新建主机" (A 或 AAAA)**。</span><span class="sxs-lookup"><span data-stu-id="caeef-130">Right-click the DNS domain that you need to add records to, and then click **New Host (A or AAAA)**.</span></span>

5.  <span data-ttu-id="caeef-131">在 " **名称** " 框中，键入主机记录的名称 (域名将自动追加) 。</span><span class="sxs-lookup"><span data-stu-id="caeef-131">In the **Name** box, type the name of the host record (the domain name will be automatically appended).</span></span>

6.  <span data-ttu-id="caeef-132">在 "IP 地址" 框中，键入单个前端服务器的 IP 地址，然后选择 " **创建关联的指针 (PTR") 记录** 或 **允许任何经过身份验证的用户使用同一所有者名称更新 DNS 记录**（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="caeef-132">In the IP Address box, type the IP address of the individual Front End Server and then select **Create associated pointer (PTR) record** or **Allow any authenticated user to update DNS records with the same owner name**, if applicable.</span></span>

7.  <span data-ttu-id="caeef-133">继续为将参与 DNS 负载平衡的所有成员前端服务器创建记录。</span><span class="sxs-lookup"><span data-stu-id="caeef-133">Continue creating records for all member Front End Servers that will participate in DNS Load Balancing.</span></span>
    
    <span data-ttu-id="caeef-134">例如，如果你有一个名为 pool1.contoso.com 和三个前端服务器的池，你将创建以下 DNS 条目：</span><span class="sxs-lookup"><span data-stu-id="caeef-134">For example, if you had a pool named pool1.contoso.com and three Front End Servers, you would create the following DNS entries:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="caeef-135">FQDN</span><span class="sxs-lookup"><span data-stu-id="caeef-135">FQDN</span></span></th>
    <th><span data-ttu-id="caeef-136">类型</span><span class="sxs-lookup"><span data-stu-id="caeef-136">Type</span></span></th>
    <th><span data-ttu-id="caeef-137">数据</span><span class="sxs-lookup"><span data-stu-id="caeef-137">Data</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="caeef-138">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="caeef-138">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="caeef-139">主机 () </span><span class="sxs-lookup"><span data-stu-id="caeef-139">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="caeef-140">192.168.1.1</span><span class="sxs-lookup"><span data-stu-id="caeef-140">192.168.1.1</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="caeef-141">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="caeef-141">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="caeef-142">主机 () </span><span class="sxs-lookup"><span data-stu-id="caeef-142">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="caeef-143">192.168.1.2</span><span class="sxs-lookup"><span data-stu-id="caeef-143">192.168.1.2</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="caeef-144">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="caeef-144">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="caeef-145">主机 () </span><span class="sxs-lookup"><span data-stu-id="caeef-145">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="caeef-146">192.168.1.3</span><span class="sxs-lookup"><span data-stu-id="caeef-146">192.168.1.3</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="caeef-147">有关创建) 记录 (DNS 主机的详细信息，请参阅 [配置 Lync Server 2013 的 Dns 主机记录](lync-server-2013-configure-dns-host-records.md)。</span><span class="sxs-lookup"><span data-stu-id="caeef-147">For details about creating DNS Host (A) records, see [Configure DNS Host records for Lync Server 2013](lync-server-2013-configure-dns-host-records.md).</span></span>

</div>

<div>

## <a name="to-enable-round-robin-for-windows-server"></a><span data-ttu-id="caeef-148">为 Windows Server 启用循环复用</span><span class="sxs-lookup"><span data-stu-id="caeef-148">To enable round robin for Windows Server</span></span>

1.  <span data-ttu-id="caeef-149">单击 " **开始**"，单击 " **所有程序**"，单击 " **管理工具**"，然后单击 " **DNS**"。</span><span class="sxs-lookup"><span data-stu-id="caeef-149">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="caeef-150">展开 " **DNS**"，右键单击要配置的 DNS 服务器，然后单击 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="caeef-150">Expand **DNS**, right-click the DNS server you want to configure, and then click **Properties**.</span></span>

3.  <span data-ttu-id="caeef-151">单击 " **高级** " 选项卡，选择 " **启用循环** " 和 " **启用网络掩码排序**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="caeef-151">Click the **Advanced** tab, select **Enable round robin** and **Enable netmask ordering**, and then click **OK**.</span></span>
    
    <span data-ttu-id="caeef-152">!["DNS 循环复用" 对话框](images/Gg398251.e7bf6125-8d78-4460-8401-0a8e7e21d305(OCS.15).jpg ""DNS 循环复用" 对话框")</span><span class="sxs-lookup"><span data-stu-id="caeef-152">![DNS Round Robin dialog box](images/Gg398251.e7bf6125-8d78-4460-8401-0a8e7e21d305(OCS.15).jpg "DNS Round Robin dialog box")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="caeef-153">默认情况下，应启用此功能。</span><span class="sxs-lookup"><span data-stu-id="caeef-153">This feature should be enabled by default.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="caeef-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="caeef-154">See Also</span></span>


[<span data-ttu-id="caeef-155">Lync Server 2013 中的 DNS 负载平衡</span><span class="sxs-lookup"><span data-stu-id="caeef-155">DNS load balancing in Lync Server 2013</span></span>](lync-server-2013-dns-load-balancing.md)  
  

<span data-ttu-id="caeef-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="caeef-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

