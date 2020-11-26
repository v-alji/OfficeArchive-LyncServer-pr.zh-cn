---
title: 为与托管 Exchange UM 的集成创建 DNS SRV 记录
description: 创建用于与托管 Exchange UM 集成的 DNS SRV 记录。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a DNS SRV record for integration with hosted Exchange UM
ms:assetid: 8ea590ae-58ea-4ca5-9853-e0708b3ea760
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh500728(v=OCS.15)
ms:contentKeyID: 48184770
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694a595977abe33bebbb5fbcf2a508c9bb4e35a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432231"
---
# <a name="create-a-dns-srv-record-for-integration-with-hosted-exchange-um"></a><span data-ttu-id="66fb2-103">为与托管 Exchange UM 的集成创建 DNS SRV 记录</span><span class="sxs-lookup"><span data-stu-id="66fb2-103">Create a DNS SRV record for integration with hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66fb2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66fb2-104">

<span> </span></span></span>

<span data-ttu-id="66fb2-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="66fb2-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="66fb2-106">本主题介绍了如何配置域名系统 (Lync Server 2013 Edge 服务器路由到 Exchange Exchange 服务（如 Microsoft Exchange Online）所需的 DNS) SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="66fb2-106">This topic describes how to configure the Domain Name System (DNS) SRV record that is required for a Lync Server 2013 Edge Server to route to a hosted Exchange service such as Microsoft Exchange Online.</span></span>

<div>

## <a name="to-create-an-external-dns-srv-record-for-the-hosted-exchange-service"></a><span data-ttu-id="66fb2-107">为托管 Exchange 服务创建外部 DNS SRV 记录</span><span class="sxs-lookup"><span data-stu-id="66fb2-107">To create an external DNS SRV record for the hosted Exchange service</span></span>

1.  <span data-ttu-id="66fb2-108">以 DnsAdmins 组成员的身份登录外部 DNS 服务器。</span><span class="sxs-lookup"><span data-stu-id="66fb2-108">Log on to the external DNS server as a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="66fb2-109">单击 " **开始**"，单击 " **管理工具**"，然后单击 " **DNS**"。</span><span class="sxs-lookup"><span data-stu-id="66fb2-109">Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="66fb2-110">在 SIP 域的控制台树中，展开 " **正向查找区域**"，然后选择将在其中安装 Lync Server 2013 的 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="66fb2-110">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and select the SIP domain in which Lync Server 2013 will be installed.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="66fb2-111">你必须在安装了 Lync Server 或将安装 Lync Server 的 SIP 域中创建 DNS SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="66fb2-111">You must create the DNS SRV record in the SIP domain in which Lync Server is or will be installed.</span></span> <span data-ttu-id="66fb2-112">创建 SRV 记录时，用于提供此服务字段的主机的 FQDN 必须是 Edge 池的外部 FQDN。</span><span class="sxs-lookup"><span data-stu-id="66fb2-112">When you create the SRV record, the FQDN used for the Host offering this service field must be the external FQDN of the Edge pool.</span></span> <span data-ttu-id="66fb2-113">例如，如果 Edge 池的外部 FQDN 是 edge01.contoso.net，请输入该值。</span><span class="sxs-lookup"><span data-stu-id="66fb2-113">For example, if the external FQDN of your Edge pool is edge01.contoso.net, enter that value.</span></span> <span data-ttu-id="66fb2-114">这还必须与 DNS 主机位于同一域中 () 记录。</span><span class="sxs-lookup"><span data-stu-id="66fb2-114">This must also be in the same domain as the DNS Hosts (A) record.</span></span>

    
    </div>

4.  <span data-ttu-id="66fb2-115">右键单击所选的域，然后单击 " **其他新记录**"。</span><span class="sxs-lookup"><span data-stu-id="66fb2-115">Right-click the selected domain, and then click **Other New Records**.</span></span>

5.  <span data-ttu-id="66fb2-116">在 " **资源记录类型**" 中，单击 " **服务位置" (SRV)**，然后单击 " **创建记录**"。</span><span class="sxs-lookup"><span data-stu-id="66fb2-116">In **Resource Record Type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

6.  <span data-ttu-id="66fb2-117">在 "**新建资源记录**" 中，单击 "**服务**"，然后键入 " **\_ sipfederationtls**"。</span><span class="sxs-lookup"><span data-stu-id="66fb2-117">In **New Resource Record**, click **Service**, and then type **\_sipfederationtls**.</span></span>

7.  <span data-ttu-id="66fb2-118">单击 "**协议**"，然后键入 " **\_ tcp**"。</span><span class="sxs-lookup"><span data-stu-id="66fb2-118">Click **Protocol**, and then type **\_tcp**.</span></span>

8.  <span data-ttu-id="66fb2-119">单击 " **端口号**"，然后键入 **5061**。</span><span class="sxs-lookup"><span data-stu-id="66fb2-119">Click **Port Number**, and then type **5061**.</span></span>

9.  <span data-ttu-id="66fb2-120">单击 " **主机提供此服务**"，然后键入 lync Server 2013 Edge 的完全限定的域名 (FQDN) ，为受信任的外部客户端提供对 lync server 2013 系统的访问权限。</span><span class="sxs-lookup"><span data-stu-id="66fb2-120">Click **Host offering this service**, and then type the fully qualified domain name (FQDN) of the Lync Server 2013 Edge pool that provides access to your Lync Server 2013 system for trusted external clients.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="66fb2-121">域还必须在 Exchange Online 设置中设置为权威的 "接受域"。</span><span class="sxs-lookup"><span data-stu-id="66fb2-121">The domain must also be set up as an authoritative, accepted domain in your Exchange Online settings.</span></span> <span data-ttu-id="66fb2-122">有关详细信息，请参阅在中创建接受的域 <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A> 。</span><span class="sxs-lookup"><span data-stu-id="66fb2-122">For details, see Create Accepted Domains at <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A>.</span></span>

    
    </div>

10. <span data-ttu-id="66fb2-123">单击 **"确定**"，然后单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="66fb2-123">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-that-the-dns-srv-record-was-created-successfully"></a><span data-ttu-id="66fb2-124">验证是否已成功创建 DNS SRV 记录</span><span class="sxs-lookup"><span data-stu-id="66fb2-124">To verify that the DNS SRV record was created successfully</span></span>

1.  <span data-ttu-id="66fb2-125">登录到域中的客户端计算机。</span><span class="sxs-lookup"><span data-stu-id="66fb2-125">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="66fb2-126">单击 **“开始”**，然后单击 **“运行”**。</span><span class="sxs-lookup"><span data-stu-id="66fb2-126">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="66fb2-127">在命令提示符处，运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="66fb2-127">At the command prompt, run the following command:</span></span>
    
        nslookup <FQDN Lync Edge Pool>

4.  <span data-ttu-id="66fb2-128">验证您是否收到了解析为 FQDN 的相应 IP 地址的答复。</span><span class="sxs-lookup"><span data-stu-id="66fb2-128">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="66fb2-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="66fb2-129">See Also</span></span>


[<span data-ttu-id="66fb2-130">在 Lync Server 2013 中为反向代理服务器创建 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="66fb2-130">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)  
  

<span data-ttu-id="66fb2-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66fb2-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

