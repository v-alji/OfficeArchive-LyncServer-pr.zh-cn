---
title: Lync Server 2013：将子网与网络站点相关联
description: Lync Server 2013：将子网与网络站点相关联。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate a subnet with a network site
ms:assetid: aa69e3ac-542a-4ba1-9582-2e6bee29f633
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412804(v=OCS.15)
ms:contentKeyID: 48185043
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ed8708b9280455355a010984d09fc91da3313f95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438269"
---
# <a name="associate-a-subnet-with-a-network-site-in-lync-server-2013"></a><span data-ttu-id="987e8-103">在 Lync Server 2013 中将子网与网络站点相关联</span><span class="sxs-lookup"><span data-stu-id="987e8-103">Associate a subnet with a network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="987e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="987e8-104">

<span> </span></span></span>

<span data-ttu-id="987e8-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="987e8-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="987e8-106">你的网络中的每个子网都必须与特定的网络站点相关联，因为子网信息用于确定在启动新会话时终结点所在的网络站点。</span><span class="sxs-lookup"><span data-stu-id="987e8-106">Every subnet in your network must be associated with a specific network site, because subnet information is used to determine the network site on which an endpoint is located while a new session is initiated.</span></span> <span data-ttu-id="987e8-107">当会话中每个方的位置已知时，高级企业语音功能可以应用该信息来确定如何处理呼叫设置或路由。</span><span class="sxs-lookup"><span data-stu-id="987e8-107">When the location of each party in a session is known, advanced Enterprise Voice features can apply that information to determine how to handle the call setup or routing.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="987e8-108">必须将部署中音频/视频边缘服务器的所有已配置公用 IP 地址添加到网络配置设置中。</span><span class="sxs-lookup"><span data-stu-id="987e8-108">All configured public IP addresses of the Audio/Video Edge Servers in your deployment must be added to your network configuration settings.</span></span> <span data-ttu-id="987e8-109">这些 IP 地址是作为掩码为 32 的子网进行添加的。</span><span class="sxs-lookup"><span data-stu-id="987e8-109">These IP addresses are added as subnets with a mask of 32.</span></span> <span data-ttu-id="987e8-110">关联的网络站点应与相应的已配置网络站点相对应。</span><span class="sxs-lookup"><span data-stu-id="987e8-110">The associated network site should correspond to the appropriate configured network site.</span></span> <span data-ttu-id="987e8-111">例如，与中央站点芝加哥的 A/V 边缘服务器对应的公共 IP 地址将为 NetworkSiteID 芝加哥。</span><span class="sxs-lookup"><span data-stu-id="987e8-111">For example, the public IP address that corresponds to the A/V Edge Server in central site Chicago would be NetworkSiteID Chicago.</span></span> <span data-ttu-id="987e8-112">有关公共 IP 地址的详细信息，请参阅在规划文档中 <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">确定 Lync Server 2013 的外部 A/V 防火墙和端口要求</A> 。</span><span class="sxs-lookup"><span data-stu-id="987e8-112">For details about public IP addresses, see <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">Determine external A/V firewall and port requirements for Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="987e8-p103">生成关键运行状况指示器 (KHI) 警报，指定存在于网络中但不与子网关联的 IP 地址列表，或指定包含 IP 地址的子网不与网络站点相关联。该警报在 8 小时内只产生一次。相关的警报信息和示例如下所示：</span><span class="sxs-lookup"><span data-stu-id="987e8-p103">A Key Health Indicator (KHI) alert is raised, specifying a list of IP addresses that are present in your network but are either not associated with a subnet, or the subnet that includes the IP addresses is not associated with a network site. This alert will not be raised more than once within an 8-hour period. The relevant alert information and an example are as follows:</span></span><BR><span data-ttu-id="987e8-116"><STRONG>来源：</STRONG> CS 带宽策略服务 (核心) </span><span class="sxs-lookup"><span data-stu-id="987e8-116"><STRONG>Source:</STRONG> CS Bandwidth Policy Service (Core)</span></span><BR><span data-ttu-id="987e8-117"><STRONG>事件号码：</STRONG> 36034</span><span class="sxs-lookup"><span data-stu-id="987e8-117"><STRONG>Event number:</STRONG> 36034</span></span><BR><span data-ttu-id="987e8-118"><STRONG>级别：</STRONG> 2</span><span class="sxs-lookup"><span data-stu-id="987e8-118"><STRONG>Level:</STRONG> 2</span></span><BR><span data-ttu-id="987e8-119"><STRONG>说明：</STRONG> 以下 IP 地址的子网： &lt; IP 地址列表 &gt; 未配置或子网未与网络站点关联。</span><span class="sxs-lookup"><span data-stu-id="987e8-119"><STRONG>Description:</STRONG> The subnets for the following IP addresses: &lt;List of IP Addresses&gt; are either not configured or the subnets are not associated to a Network Site.</span></span><BR><span data-ttu-id="987e8-120"><STRONG>原因：</STRONG> 网络配置设置中缺少对应 IP 地址的子网，或者子网未与网络站点关联。</span><span class="sxs-lookup"><span data-stu-id="987e8-120"><STRONG>Cause:</STRONG> The subnets for the corresponding IP addresses are missing from the network configuration settings or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="987e8-121"><STRONG>解决方案：</STRONG> 将对应于 IP 地址列表的子网添加到网络配置设置中，并将每个子网关联到网络站点。</span><span class="sxs-lookup"><span data-stu-id="987e8-121"><STRONG>Resolution:</STRONG> Add subnets corresponding to the list of IP addresses into the network configuration settings and associate every subnet to a network site.</span></span><BR><span data-ttu-id="987e8-p104">例如，如果警报中的 IP 地址列表指定 10.121.248.226 和 10.121.249.20，则可能是这些 IP 地址没有与子网关联，或者与其关联的子网不属于网络站点。如果 10.121.248.0/24 和 10.121.249.0/24 是与这些地址对应的子网，则可按如下所示解决此问题：</span><span class="sxs-lookup"><span data-stu-id="987e8-p104">For example, if the IP address list in the alert specifies 10.121.248.226 and 10.121.249.20, either these IP addresses are not associated with a subnet or the subnet they are associated with does not belong to a network site. If 10.121.248.0/24 and 10.121.249.0/24 are the corresponding subnets for these addresses, you can resolve this issue as follows:</span></span> 
> <OL>
> <LI>
> <P><span data-ttu-id="987e8-124">确保 IP 地址 10.121.248.226 与子网 10.121.248.0/24 相关联，IP 地址 10.121.249.20 与子网 10.121.249.0/24 相关联。</span><span class="sxs-lookup"><span data-stu-id="987e8-124">Be sure that IP address 10.121.248.226 is associated with the 10.121.248.0/24 subnet and IP address 10.121.249.20 is associated with the 10.121.249.0/24 subnet.</span></span></P>
> <LI>
> <P><span data-ttu-id="987e8-125">确保子网 10.121.248.0/24 和 10.121.249.0/24 分别与一个网络站点相关联。</span><span class="sxs-lookup"><span data-stu-id="987e8-125">Be sure that the 10.121.248.0/24 and 10.121.249.0/24 subnets are each associated with a network site.</span></span></P></LI></OL>



</div>

<span data-ttu-id="987e8-126">有关使用网络子网的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="987e8-126">For details about working with network subnets, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="987e8-127">New-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="987e8-127">New-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)

  - [<span data-ttu-id="987e8-128">Get-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="987e8-128">Get-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet)

  - [<span data-ttu-id="987e8-129">Set-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="987e8-129">Set-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSubnet)

  - [<span data-ttu-id="987e8-130">Remove-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="987e8-130">Remove-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSubnet)

<div>


> [!TIP]  
> <span data-ttu-id="987e8-131">如果你正在使用大量子网，建议使用逗号分隔的值 (CSV) 文件，以便将子网与网站相关联。</span><span class="sxs-lookup"><span data-stu-id="987e8-131">If you are working with a large number of subnets, we recommend using a comma-separated values (CSV) file to associate the subnets to sites.</span></span> <span data-ttu-id="987e8-132">CSV 文件必须具有以下四列： <STRONG>IPAddress</STRONG>、 <STRONG>mask</STRONG>、 <STRONG>description</STRONG>、 <STRONG>NetworkSiteID</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="987e8-132">The CSV file must have the following four columns: <STRONG>IPAddress</STRONG>, <STRONG>mask</STRONG>, <STRONG>description</STRONG>, <STRONG>NetworkSiteID</STRONG>.</span></span>



</div>

<div>

## <a name="to-associate-a-subnet-with-a-network-site-by-using-management-shell"></a><span data-ttu-id="987e8-133">使用命令行管理程序将子网与网络站点相关联</span><span class="sxs-lookup"><span data-stu-id="987e8-133">To associate a subnet with a network site by using Management Shell</span></span>

1.  <span data-ttu-id="987e8-134">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="987e8-134">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="987e8-135">运行 **New-CsNetworkSubnet** cmdlet 将子网与网络站点相关联：</span><span class="sxs-lookup"><span data-stu-id="987e8-135">Run the **New-CsNetworkSubnet** cmdlet to associate a subnet with a network site:</span></span>
    
        New-CsNetworkSubnet -SubnetID <String> -MaskBits <Int32> -NetworkSiteID <String>
    
    <span data-ttu-id="987e8-136">例如：</span><span class="sxs-lookup"><span data-stu-id="987e8-136">For example:</span></span>
    
        New-CsNetworkSubnet -SubnetID 172.11.12.13 - MaskBits 20 -NetworkSiteID Chicago
    
    <span data-ttu-id="987e8-137">在此示例中，创建了子网 172.11.12.13 与网络站点“Chicago”之间的关联。</span><span class="sxs-lookup"><span data-stu-id="987e8-137">In this example, you created an association between the subnet 172.11.12.13 and the network site “Chicago”.</span></span>

3.  <span data-ttu-id="987e8-138">为拓扑中的所有子网重复步骤 2。</span><span class="sxs-lookup"><span data-stu-id="987e8-138">Repeat step 2 for all subnets in your topology.</span></span>

</div>

<div>

## <a name="to-associate-subnets-with-network-sites-by-importing-a-csv-file"></a><span data-ttu-id="987e8-139">通过导入 CSV 文件将子网与网络站点关联</span><span class="sxs-lookup"><span data-stu-id="987e8-139">To associate subnets with network sites by importing a CSV file</span></span>

1.  <span data-ttu-id="987e8-p106">创建包含要添加的所有子网的 CSV 文件。例如，创建名为 **subnet.csv** 并包含以下内容的文件：</span><span class="sxs-lookup"><span data-stu-id="987e8-p106">Create a CSV file that includes all of the subnets you want to add. For example, create a file named **subnet.csv** with the following content:</span></span>
    
    `IPAddress, mask, description, NetworkSiteID`
    
    `172.11.12.0, 24, "NA:Subnet in Portland", Portland`
    
    `172.11.13.0, 24, "NA:Subnet in Reno", Reno`
    
    `172.11.14.0, 25, "EMEA:Subnet in Warsaw", Warsaw`
    
    `172.11.15.0, 31, "EMEA:Subnet in Paris", Paris`

2.  <span data-ttu-id="987e8-142">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="987e8-142">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="987e8-143">运行以下 cmdlet 以导入 **subnet.csv**，然后将其内容存储在 Lync Server management store 中：</span><span class="sxs-lookup"><span data-stu-id="987e8-143">Run the following cmdlet to import **subnet.csv**, and then store its contents in the Lync Server management store:</span></span>
    
        import-csv subnet.csv | foreach {New-CSNCSSubnet  _.IPAddress -MaskBits $_.mask -Description $_.description -NetworkSiteID $_.NetworkSiteID}

</div>

<div>

## <a name="to-associate-a-subnet-with-a-network-site-by-using-lync-server-control-panel"></a><span data-ttu-id="987e8-144">使用 Lync Server "控制面板" 将子网与网络站点相关联</span><span class="sxs-lookup"><span data-stu-id="987e8-144">To associate a subnet with a network site by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="987e8-145">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="987e8-145">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="987e8-146">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="987e8-146">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="987e8-147">在左侧导航栏中，单击“网络配置”。</span><span class="sxs-lookup"><span data-stu-id="987e8-147">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="987e8-148">单击“子网”导航按钮。</span><span class="sxs-lookup"><span data-stu-id="987e8-148">Click the **Subnet** navigation button.</span></span>

4.  <span data-ttu-id="987e8-149">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="987e8-149">Click **New**.</span></span>

5.  <span data-ttu-id="987e8-150">在“新建子网”页上，单击“子网 ID”，然后键入由要与网络站点关联的子网定义的 IP 地址范围中的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="987e8-150">On the **New Subnet** page, click **Subnet ID**, and then type the first address in the IP address range defined by the subnet you want to associate with a network site.</span></span>

6.  <span data-ttu-id="987e8-151">单击“掩码”，然后键入要应用于子网的位掩码。</span><span class="sxs-lookup"><span data-stu-id="987e8-151">Click **Mask**, and then type the bitmask to apply to the subnet.</span></span>

7.  <span data-ttu-id="987e8-152">单击“网络站点 ID”，然后选择要向其中添加此子网的站点的站点 ID。</span><span class="sxs-lookup"><span data-stu-id="987e8-152">Click **Network site ID**, and then select the site ID of the site to which you are adding this subnet.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="987e8-153">如果尚未创建网络站点，该列表将为空。</span><span class="sxs-lookup"><span data-stu-id="987e8-153">If you have not yet created network sites, this list will be empty.</span></span> <span data-ttu-id="987e8-154">有关此过程的详细信息，请参阅 <A href="lync-server-2013-create-or-modify-a-network-site.md">在 Lync Server 2013 中创建或修改网络网站</A>。</span><span class="sxs-lookup"><span data-stu-id="987e8-154">For details about the procedure, see <A href="lync-server-2013-create-or-modify-a-network-site.md">Create or modify a network site in Lync Server 2013</A>.</span></span> <span data-ttu-id="987e8-155">还可以通过运行 <STRONG>Get-CsNetworkSite</STRONG> cmdlet 检索部署的站点 ID。</span><span class="sxs-lookup"><span data-stu-id="987e8-155">You can also retrieve site IDs for your deployment by running the <STRONG>Get-CsNetworkSite</STRONG> cmdlet.</span></span> <span data-ttu-id="987e8-156">有关详细信息，请参阅 Lync Server Management Shell 文档。</span><span class="sxs-lookup"><span data-stu-id="987e8-156">For details, see the Lync Server Management Shell documentation.</span></span>

    
    </div>

8.  <span data-ttu-id="987e8-157">（可选）单击“说明”，然后键入其他信息来说明此子网。</span><span class="sxs-lookup"><span data-stu-id="987e8-157">Optionally, click **Description**, and then type additional information to describe this subnet.</span></span>

9.  <span data-ttu-id="987e8-158">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="987e8-158">Click **Commit**.</span></span>

<span data-ttu-id="987e8-159">重复这些步骤以向网络站点中添加其他子网。</span><span class="sxs-lookup"><span data-stu-id="987e8-159">Repeat these steps to add other subnets to a network site.</span></span>

<span data-ttu-id="987e8-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="987e8-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

