---
title: Lync Server 2013：配置 DNS 主机记录
description: Lync Server 2013：配置 DNS 主机记录。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS Host records
ms:assetid: 78a1afcf-41c8-4da5-8740-c6570c19078c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398593(v=OCS.15)
ms:contentKeyID: 48184577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7fd403402d0d2f089d7fc92a62296a56df0cf2e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434037"
---
# <a name="configure-dns-host-records-for-lync-server-2013"></a><span data-ttu-id="23a59-103">配置 Lync Server 2013 的 DNS 主机记录</span><span class="sxs-lookup"><span data-stu-id="23a59-103">Configure DNS Host records for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23a59-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23a59-104">

<span> </span></span></span>

<span data-ttu-id="23a59-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="23a59-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="23a59-106">若要成功完成此过程，你应至少以域管理员组的成员或 DnsAdmins 组的成员的身份登录到服务器或域。</span><span class="sxs-lookup"><span data-stu-id="23a59-106">To successfully complete this procedure, you should be logged on to the server or domain at minimum as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<div>

## <a name="to-configure-dns-host-a-records"></a><span data-ttu-id="23a59-107">配置 DNS 主机 A 记录</span><span class="sxs-lookup"><span data-stu-id="23a59-107">To configure DNS Host A records</span></span>

1.  <span data-ttu-id="23a59-108">在域名系统 (DNS) 服务器上，单击 " **开始**"，单击 " **管理工具**"，然后单击 " **DNS**"。</span><span class="sxs-lookup"><span data-stu-id="23a59-108">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="23a59-109">在您的域的控制台树中，展开 " **正向查找区域**"，然后右键单击将安装 Lync Server 2013 的域。</span><span class="sxs-lookup"><span data-stu-id="23a59-109">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="23a59-110">单击 " **新建主机" (A 或 AAAA)**。</span><span class="sxs-lookup"><span data-stu-id="23a59-110">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="23a59-111">单击 " **名称**"，键入池的主机名 (域名是从定义记录的区域中假定的，不需要作为 A 记录) 的一部分输入。</span><span class="sxs-lookup"><span data-stu-id="23a59-111">Click **Name**, type the host name for the pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="23a59-112">单击 " **IP 地址**"，键入前端池的负载平衡器的虚拟 IP (VIP) 。</span><span class="sxs-lookup"><span data-stu-id="23a59-112">Click **IP Address**, type the virtual IP (VIP) of the load balancer for the Front End pool.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="23a59-113">在使用控制器池的部署中，主机 (简单 Url 的) 记录应指向控制器负载平衡器的 VIP。</span><span class="sxs-lookup"><span data-stu-id="23a59-113">In deployments that use a Director pool, the host (A) records for the simple URLs should point to the VIP of the Director load balancer.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="23a59-114">如果仅部署一个连接到拓扑的企业版服务器或 Director 而不使用负载平衡器，或者如果你部署标准版服务器，请键入企业版服务器、标准版服务器或 Director 的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="23a59-114">If you deploy only one Enterprise Edition server or Director that is connected to the topology without a load balancer, or if you deploy a Standard Edition server, type the IP address of the Enterprise Edition server, Standard Edition server, or Director.</span></span> <span data-ttu-id="23a59-115">如果在一个池中部署多个企业版服务器或控制器，则需要负载平衡器。</span><span class="sxs-lookup"><span data-stu-id="23a59-115">A load balancer is required if you deploy more than one Enterprise Edition server or Director in a pool.</span></span> <span data-ttu-id="23a59-116">负载平衡器不与标准版服务器一起使用。</span><span class="sxs-lookup"><span data-stu-id="23a59-116">Load balancers are not used with Standard Edition servers.</span></span>

    
    </div>

6.  <span data-ttu-id="23a59-117">单击 " **添加主机**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="23a59-117">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="23a59-118">若要创建其他 A 记录，请重复步骤4和步骤5。</span><span class="sxs-lookup"><span data-stu-id="23a59-118">To create an additional A record, repeat steps 4 and 5.</span></span>

8.  <span data-ttu-id="23a59-119">完成创建所需的所有记录后，单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="23a59-119">When you are finished creating all the A records that you need, click **Done**.</span></span>

<span data-ttu-id="23a59-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23a59-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

