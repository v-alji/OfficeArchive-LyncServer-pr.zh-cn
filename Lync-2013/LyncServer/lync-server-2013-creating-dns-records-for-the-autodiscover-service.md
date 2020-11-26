---
title: Lync Server 2013：为自动发现服务创建 DNS 记录
description: Lync Server 2013：为自动发现服务创建 DNS 记录。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating DNS records for the Autodiscover Service
ms:assetid: 3756ffe4-c6b1-492d-850e-42a832e06567
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690010(v=OCS.15)
ms:contentKeyID: 48183823
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6903e6b07001289db8b65e8cc962e8d8db4b248b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431510"
---
# <a name="creating-dns-records-for-the-autodiscover-service-in-lync-server-2013"></a><span data-ttu-id="0a544-103">在 Lync Server 2013 中为自动发现服务创建 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="0a544-103">Creating DNS records for the Autodiscover Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a544-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a544-104">

<span> </span></span></span>

<span data-ttu-id="0a544-105">_**主题上次修改时间：** 2014-06-20_</span><span class="sxs-lookup"><span data-stu-id="0a544-105">_**Topic Last Modified:** 2014-06-20_</span></span>

<span data-ttu-id="0a544-106">您的 Lync 移动用户将需要您启用自动发现，其中包括创建某些域名系统 (DNS) 记录的部分。</span><span class="sxs-lookup"><span data-stu-id="0a544-106">Your Lync Mobile users will need you to enable autodiscovery, and a part of that involves creating some Domain Name System (DNS) records.</span></span> <span data-ttu-id="0a544-107">根据你的需要，你需要满足以下要求：</span><span class="sxs-lookup"><span data-stu-id="0a544-107">Depending on your needs, you need the following:</span></span>

  - <span data-ttu-id="0a544-108">一个内部 DNS 记录，用于支持从你的组织的网络中连接的移动用户。</span><span class="sxs-lookup"><span data-stu-id="0a544-108">An internal DNS record to support mobile users who’re connecting from within your organization's network.</span></span>

  - <span data-ttu-id="0a544-109">支持从 Internet 连接的移动用户的外部 DNS 记录或公共 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="0a544-109">An external, or public, DNS record to support mobile users who’re connecting from the Internet</span></span>

<span data-ttu-id="0a544-110">为什么？</span><span class="sxs-lookup"><span data-stu-id="0a544-110">Why both?</span></span> <span data-ttu-id="0a544-111">你需要为每个 SIP 域创建一个内部 DNS 记录和一个外部 DNS 记录。</span><span class="sxs-lookup"><span data-stu-id="0a544-111">You need to create both an internal DNS record and an external DNS record for each SIP domain.</span></span>

<span data-ttu-id="0a544-112">你创建的 DNS 记录可以是 (主机) 记录或 CNAME 记录。</span><span class="sxs-lookup"><span data-stu-id="0a544-112">The DNS records you create can be either A (host) records or CNAME records.</span></span> <span data-ttu-id="0a544-113">为帮助你解决此问题，我们将指导你了解如何在下面创建这些内部和外部 DNS 记录。</span><span class="sxs-lookup"><span data-stu-id="0a544-113">To help you out, we’ll walk through how to create these internal and external DNS records below.</span></span> <span data-ttu-id="0a544-114">如果需要进一步阅读有关移动用户的 DNS 要求的详细信息，您可以查看 [Lync Server 2013 中的移动技术要求](lync-server-2013-technical-requirements-for-mobility.md)。</span><span class="sxs-lookup"><span data-stu-id="0a544-114">If you need to do some further reading about the DNS requirements for mobile users, you can check out [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

<div>

## <a name="creating-an-internal-dns-cname-record"></a><span data-ttu-id="0a544-115">创建内部 DNS CNAME 记录</span><span class="sxs-lookup"><span data-stu-id="0a544-115">Creating an internal DNS CNAME record</span></span>

1.  <span data-ttu-id="0a544-116">要创建内部 DNS 记录，您需要使用域管理员组的成员或 DnsAdmins 组的成员登录到您的网络中的 DNS 服务器上。</span><span class="sxs-lookup"><span data-stu-id="0a544-116">To make an internal DNS record, you’ll need to log on to a DNS server in your network with a domain account that’s either a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="0a544-117">打开 "DNS 管理" 管理单元：单击 " **开始**"，单击 " **管理工具**"，然后单击 " **DNS**"。</span><span class="sxs-lookup"><span data-stu-id="0a544-117">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="0a544-118">在 DNS 服务器的控制台树中，展开用于安装 Lync Server 2013 控制器池和前端池的 Active Directory 域的 " **正向查找区域** "。</span><span class="sxs-lookup"><span data-stu-id="0a544-118">In the console tree of the DNS server, expand **Forward Lookup Zones** for the Active Directory domain where your Lync Server 2013 Director pool and Front End pool are installed.</span></span> <span data-ttu-id="0a544-119"> (例如，contoso. 本地) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-119">(for example, contoso.local).</span></span>

4.  <span data-ttu-id="0a544-120">检查并查看是否存在针对内部 DNS 记录的控制器池的主机 A (AAAA 是否存在) 记录的主机 A 记录应存在于内部 Web 服务的内部 Web 服务完全限定的域名 (FQDN) 的 FQDN (例如，lyncwebdir01) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-120">Check and see if a host A (AAAA for IPv6) record exists for your Director pool for an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span> <span data-ttu-id="0a544-121">如果不在这里，你可能不会使用控制器池，并且你将需要为你的前端池或单个服务器 FQDN （如果你的设置）使用 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0a544-121">If it’s not here, you may not be using a Director pool, and you’ll need to use the FQDN for your Front End pool or even a single server FQDN, if that’s your setup.</span></span>

5.  <span data-ttu-id="0a544-122">请注意，请检查并查看是否存在针对内部 DNS 记录的前端池的主机 A (AAAA) 记录，主机 A (或 AAAA) 记录应存在于你的前端池的内部 Web 服务 FQDN (例如，lyncwebpool01) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-122">Keeping that in mind, check and see if a host A (AAAA for IPv6) record exists for your Front End pool for an internal DNS record, a host A (or AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span> <span data-ttu-id="0a544-123">如果不是，你需要记下前端服务器或标准版服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0a544-123">If it doesn’t, you’ll need to make note of the FQDN for the Front End Server or Standard Edition server.</span></span>

6.  <span data-ttu-id="0a544-124">知道存在 (或 AAAA) 记录的主机后，在 DNS 服务器的控制台树中，展开您的 SIP 域的 " **正向查找区域** " (例如，contoso.com ") "。</span><span class="sxs-lookup"><span data-stu-id="0a544-124">Once you know what host A (or AAAA) records exist, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

7.  <span data-ttu-id="0a544-125">右键单击 SIP 域名称，然后单击 " **新建别名 (CNAME)**"。</span><span class="sxs-lookup"><span data-stu-id="0a544-125">Right-click the SIP domain name, and then click **New Alias (CNAME)**.</span></span>

8.  <span data-ttu-id="0a544-126">在 " **别名名称**" 中，键入 lyncdiscoverinternal 作为内部自动发现服务 URL 的主机名。</span><span class="sxs-lookup"><span data-stu-id="0a544-126">In **Alias name**, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="0a544-127">在 " **完全限定的域名 (适用于目标主机的 FQDN)** 中，键入或浏览到你的控制器池的内部 WEB 服务 FQDN (例如，lyncwebdir01) ，然后单击 **" 确定 "**。</span><span class="sxs-lookup"><span data-stu-id="0a544-127">In **Fully qualified domain name (FQDN) for target host**, type or browse to the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local) and then click **OK**.</span></span>

10. <span data-ttu-id="0a544-128">必须在 Lync Server 2013 环境支持的每个 SIP 域的正向查找区域中创建新的自动发现 CNAME 记录。</span><span class="sxs-lookup"><span data-stu-id="0a544-128">You must create a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

</div>

<div>

## <a name="creating-an-external-dns-cname-record"></a><span data-ttu-id="0a544-129">创建外部 DNS CNAME 记录</span><span class="sxs-lookup"><span data-stu-id="0a544-129">Creating an external DNS CNAME record</span></span>

1.  <span data-ttu-id="0a544-130">若要创建外部 DNS CNAME 记录，你需要连接到你的公共 DNS 提供商，然后按照我们的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0a544-130">To create an external DNS CNAME record, you’re going to need to connect to your public DNS provider, and then follow our steps.</span></span> <span data-ttu-id="0a544-131">我们无法确切描述你在 DNS 提供商环境中所处的位置，因为可能有不同的管理外部 DNS 的方式，但我们希望这些步骤有所帮助。</span><span class="sxs-lookup"><span data-stu-id="0a544-131">We can’t describe exactly where you’re going in your DNS provider’s environment as there may be different ways of managing your external DNS, but we hope these steps help.</span></span>

2.  <span data-ttu-id="0a544-132">使用可在该环境中创建 DNS 记录的帐户登录到您的外部 DNS 提供商。</span><span class="sxs-lookup"><span data-stu-id="0a544-132">Log into your external DNS provider with an account that can create DNS records in that environment.</span></span>

3.  <span data-ttu-id="0a544-133">你应该已为此环境创建了一个 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="0a544-133">You should have a SIP domain created for this environment already.</span></span> <span data-ttu-id="0a544-134">展开此 SIP 域的 **正向查找区域** ，或者根据所使用的外部 DNS 接口选择它。</span><span class="sxs-lookup"><span data-stu-id="0a544-134">Expand the **Forward Lookup Zone** for this SIP domain, or otherwise select it depending on the external DNS interface being used.</span></span>

4.  <span data-ttu-id="0a544-135">你应该已经看到一个主机 A (AAAA) 你的控制器 (池的 AAAA，如 lyncwebexdir01.contoso.com) ，请确认这是。</span><span class="sxs-lookup"><span data-stu-id="0a544-135">You should already see a host A (AAAA for IPv6) record for your Director pool (such as lyncwebexdir01.contoso.com), so confirm that it’s there.</span></span> <span data-ttu-id="0a544-136">如果不是，则您可能没有使用控制器池。</span><span class="sxs-lookup"><span data-stu-id="0a544-136">If it’s not, then you may not be using a Director pool.</span></span> <span data-ttu-id="0a544-137">如果是这种情况，你需要使用前端池的 FQDN，或者，如果你为 Front-End server 或标准版服务器的单个服务器执行此操作，则需要使用它。</span><span class="sxs-lookup"><span data-stu-id="0a544-137">If that’s the case, you’ll need to use the FQDN of your Front End Pool, or if you’re doing this for a single server, for your Front-End server or Standard Edition server.</span></span>

5.  <span data-ttu-id="0a544-138">你还需要确认对于你的外部 Web 服务，) 记录的主机 A (AAAA 是否存在) 适用于你的外部 Web 服务的完全限定域名 (FQDN 对于你的前端池 (（如 lyncwebextpool01.contoso.com) ），如果没有前端池，则为你的单服务器 FQDN 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0a544-138">You’ll also need to confirm that a host A (AAAA for IPv6) record exists for your external Web Services Fully Qualified Domain Name (FQDN) for your Front End pool (such as lyncwebextpool01.contoso.com), or a FQDN for your single-server FQDN if you have no Front End pool.</span></span> <span data-ttu-id="0a544-139">如前面的步骤所述，如果没有控制器池，则需要以下内容。</span><span class="sxs-lookup"><span data-stu-id="0a544-139">As noted in the previous step, you’ll need this below if you don’t have a Director pool.</span></span>

6.  <span data-ttu-id="0a544-140">现在，按照适用于你的外部 DNS 提供程序的格式，选择用于创建 **新别名 (CNAME)** 的选项 (这可能是菜单选项或链接，具体取决于 DNS 提供商的格式) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-140">Now, in the appropriate format for your external DNS provider, choose the option for creating a **New Alias (CNAME)** (this may be a menu option or a link, depending on the format of the DNS provider).</span></span>

7.  <span data-ttu-id="0a544-141">应该有某种形式的 **别名** 文本框与内部 DNS，应输入 lyncdiscover 作为外部自动发现服务 URL 的主机名。</span><span class="sxs-lookup"><span data-stu-id="0a544-141">There should be some form of **Alias name** text box as with the internal DNS, you should enter lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

8.  <span data-ttu-id="0a544-142">还应该有某种形式的 **完全限定的域名 (FQDN) 用于目标主机** 文本框，下面是输入 Director 池的外部 WEB 服务 FQDN 的位置 (例如，lyncwebexdir01.contoso.com) 然后单击 "确定" 或 "执行外部 DNS 中的任何操作" 以接受此条目的创建。</span><span class="sxs-lookup"><span data-stu-id="0a544-142">There should also be some form of a **Fully qualified domain name (FQDN) for target host** text box, here’s where you’ll enter the external Web Services FQDN for your Director pool (for example, lyncwebexdir01.contoso.com) and then click OK or take whatever action in the external DNS to accept the creation of this entry.</span></span> <span data-ttu-id="0a544-143">如上面的步骤4中所述，如果你没有控制器池，你需要根据需要使用前端池 FQDN 或已设置的单服务器 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0a544-143">As noted in Step 4, above, if you don’t have a Director pool, you’ll need to use the Front End pool FQDN or the single-server FQDN you have set up, as appropriate.</span></span>

9.  <span data-ttu-id="0a544-144">你将需要在 Lync 2013 环境支持的每个 SIP 域的正向查找区域中创建新的自动发现 CNAME 记录。</span><span class="sxs-lookup"><span data-stu-id="0a544-144">You’ll need to make a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that’s supported in your Lync 2013 environment.</span></span>

</div>

<div>

## <a name="creating-an-internal-dns-a-record"></a><span data-ttu-id="0a544-145">创建内部 DNS A 记录</span><span class="sxs-lookup"><span data-stu-id="0a544-145">Creating an internal DNS A record</span></span>

1.  <span data-ttu-id="0a544-146">要创建内部 DNS 记录，请使用域管理员组的成员或 DnsAdmins 组的成员登录到您的网络中的 DNS 服务器。</span><span class="sxs-lookup"><span data-stu-id="0a544-146">To make an internal DNS record, log on to a DNS server in your network with a domain account that’s a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="0a544-147">打开 "DNS 管理" 管理单元：单击 " **开始**"，单击 " **管理工具**"，然后单击 " **DNS**"。</span><span class="sxs-lookup"><span data-stu-id="0a544-147">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="0a544-148">对于内部 DNS 记录，请在 DNS 服务器的控制台树中，展开您的 Active Directory 域的 **正向查找区域** (例如，contoso. 本地) 您的 Lync Server 2013 控制器池和前端池的安装位置。</span><span class="sxs-lookup"><span data-stu-id="0a544-148">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local) where your Lync Server 2013 Director pool and Front End pool are installed.</span></span>

4.  <span data-ttu-id="0a544-149">检查并查看是否存在针对内部 DNS 记录的控制器池的主机 A (AAAA 是否存在) 记录的主机 A 记录应存在于内部 Web 服务的内部 Web 服务完全限定的域名 (FQDN) 的 FQDN (例如，lyncwebdir01) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-149">Check and see if a host A (AAAA for IPv6) record exists for your Director pool for an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span> <span data-ttu-id="0a544-150">如果不在这里，您可能没有使用控制器池，并且您需要使用您的前端池的 IP 地址，甚至是单个服务器 IP 地址（如果您设置了）。</span><span class="sxs-lookup"><span data-stu-id="0a544-150">If it’s not here, you may not be using a Director pool, and you’ll need to use the IP address for your Front End pool or even a single server IP address, if that’s your setup.</span></span>

5.  <span data-ttu-id="0a544-151">请注意，请检查并查看是否存在针对内部 DNS 记录的前端池的主机 A (AAAA) 记录，主机 A (或 AAAA) 记录应存在于你的前端池的内部 Web 服务 FQDN (例如，lyncwebpool01) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-151">Keeping that in mind, check and see if a host A (AAAA for IPv6) record exists for your Front End pool for an internal DNS record, a host A (or AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span> <span data-ttu-id="0a544-152">如果不是，你需要记下前端服务器或标准版服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="0a544-152">If it doesn’t, you’ll need to make note of the IP address for the Front End Server or Standard Edition server.</span></span>

6.  <span data-ttu-id="0a544-153">知道存在 (或 AAAA) 记录的主机后，在 DNS 服务器的控制台树中，展开您的 SIP 域的 " **正向查找区域** " (例如，contoso.com ") "。</span><span class="sxs-lookup"><span data-stu-id="0a544-153">Once you know what host A (or AAAA) records exist, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

7.  <span data-ttu-id="0a544-154">右键单击 SIP 域名称，然后单击 " **新建主机 (A 或 AAAA)**。</span><span class="sxs-lookup"><span data-stu-id="0a544-154">Right-click the SIP domain name, and then click **New Host (A or AAAA)**.</span></span>

8.  <span data-ttu-id="0a544-155">在 " **名称**" 中，键入 lyncdiscoverinternal 作为内部自动发现服务 URL 的主机名。</span><span class="sxs-lookup"><span data-stu-id="0a544-155">In **Name**, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="0a544-156">在 " **IP 地址**" 中，键入 director (的内部 WEB 服务 IP 地址，或者，如果使用负载平衡器，请键入控制器负载平衡器) 的虚拟 IP (VIP) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-156">In **IP Address**, type the internal Web Services IP address of the Director (or, if you use a load balancer, type the virtual IP (VIP) of the Director load balancer).</span></span> <span data-ttu-id="0a544-157">如上面的步骤4所述，如果未使用 Director，可能需要输入前端服务器或标准版服务器的 IP 地址，或者，如果使用负载平衡器，请键入前端池负载平衡器的 VIP。</span><span class="sxs-lookup"><span data-stu-id="0a544-157">As noted in Step 4 above, if you aren’t using a Director, you may need to enter the IP address of the Front End Server or Standard Edition server or, if you use a load balancer, type the VIP of the Front End pool load balancer.</span></span>

10. <span data-ttu-id="0a544-158">单击 " **添加主机**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="0a544-158">Click **Add Host**, and then click **OK**.</span></span>

11. <span data-ttu-id="0a544-159">若要创建其他 A 或 AAAA 记录，请重复步骤8到步骤10，请记住，你需要在 Lync Server 2013 环境支持的每个 SIP 域的正向查找区域中创建新的自动发现 A 或 AAAA 记录。</span><span class="sxs-lookup"><span data-stu-id="0a544-159">To create an additional A or AAAA record, repeat steps 8 through 10, keeping in mind that you’ll need to create new Autodiscover A or AAAA records in the forward lookup zone of each SIP domain that’s supported in your Lync Server 2013 environment.</span></span>

12. <span data-ttu-id="0a544-160">为 IPv6 创建 (后，AAAA) 记录，请单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="0a544-160">When you are finished creating A (for IPv6, AAAA) records, click **Done**.</span></span>

</div>

<div>

## <a name="creating-an-external-dns-a-record"></a><span data-ttu-id="0a544-161">创建外部 DNS A 记录</span><span class="sxs-lookup"><span data-stu-id="0a544-161">Creating an external DNS A record</span></span>

1.  <span data-ttu-id="0a544-162">若要创建外部 DNS 记录，请连接到您的公共 DNS 提供商，然后按照我们的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="0a544-162">To create an external DNS record, connect to your public DNS provider, and then follow our steps.</span></span> <span data-ttu-id="0a544-163">我们无法确切描述你在 DNS 提供商环境中所处的位置，因为可能有不同的管理外部 DNS 的方式，但我们希望这些步骤有所帮助。</span><span class="sxs-lookup"><span data-stu-id="0a544-163">We can’t describe exactly where you’re going in your DNS provider’s environment as there may be different ways of managing your external DNS, but we hope these steps help.</span></span>

2.  <span data-ttu-id="0a544-164">您需要以可在该环境中创建 DNS 记录的帐户的形式登录。</span><span class="sxs-lookup"><span data-stu-id="0a544-164">You’ll need to be logged in as an account that can create DNS records in that environment.</span></span>

3.  <span data-ttu-id="0a544-165">对于外部 DNS 记录，请在 DNS 服务器的控制台树中，展开您的 SIP 域的 **正向查找区域** (例如，contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-165">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span> <span data-ttu-id="0a544-166">对于外部 DNS 记录，请在 DNS 服务器的控制台树中，展开您的 SIP 域的 **正向查找区域** (例如，contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="0a544-166">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="0a544-167">你应该已经看到了一个主机 A (AAAA for) 你的控制器池的应用 AAAA (如 lyncwebexdir01.contoso.com) ，因此请确认该地址是否存在以及 IP 地址是什么。</span><span class="sxs-lookup"><span data-stu-id="0a544-167">You should already see a host A (AAAA for IPv6) record for your Director pool (such as lyncwebexdir01.contoso.com), so confirm that it’s there and what the IP address is.</span></span> <span data-ttu-id="0a544-168">如果不是，则您可能没有使用控制器池。</span><span class="sxs-lookup"><span data-stu-id="0a544-168">If it’s not, then you may not be using a Director pool.</span></span> <span data-ttu-id="0a544-169">如果是这种情况，您需要使用您的前端池的 IP 地址，或者，如果对单个服务器执行此操作，请使用您的 Front-End 服务器或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="0a544-169">If that’s the case, you’ll need to use the IP address of your Front End Pool, or if you’re doing this for a single server, for your Front-End server or Standard Edition server.</span></span> <span data-ttu-id="0a544-170">请记住，你的服务器还可能位于负载平衡器后面，或者使用反向代理。</span><span class="sxs-lookup"><span data-stu-id="0a544-170">Keep in mind that your servers may also be behind a load-balancer, or using a reverse proxy.</span></span> <span data-ttu-id="0a544-171">请记下您的 IP 地址，并按照以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="0a544-171">Make note of the IP addresses as well for following the steps below.</span></span>

5.  <span data-ttu-id="0a544-172">你还需要确认对于你的外部 Web 服务，) 记录的主机 A (AAAA 是否存在) 适用于你的外部 Web 服务的完全限定域名 (FQDN 对于你的前端池 (（如 lyncwebextpool01.contoso.com) ），如果没有前端池，则为单服务器 Lync 安装的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="0a544-172">You’ll also need to confirm that a host A (AAAA for IPv6) record exists for your external Web Services Fully Qualified Domain Name (FQDN) for your Front End pool (such as lyncwebextpool01.contoso.com), or an IP address for your single-server Lync installation if you have no Front End pool.</span></span> <span data-ttu-id="0a544-173">如前面的步骤所述，如果没有控制器池，则需要以下内容。</span><span class="sxs-lookup"><span data-stu-id="0a544-173">As noted in the previous step, you’ll need this below if you don’t have a Director pool.</span></span>

6.  <span data-ttu-id="0a544-174">现在，按照适用于您的外部 DNS 提供商的格式，选择用于创建 **新主机 a 或 AAAA** 的选项 (此选项可能是菜单选项或链接，具体取决于 DNS 提供商) 的格式。</span><span class="sxs-lookup"><span data-stu-id="0a544-174">Now, in the appropriate format for your external DNS provider, choose the option for creating a **New Host A or AAAA** (this may be a menu option or a link, depending on the format of the DNS provider).</span></span>

7.  <span data-ttu-id="0a544-175">应存在一个用于输入 **名称** 的位置，键入 lyncdiscover 作为外部自动发现服务 URL 的主机名。</span><span class="sxs-lookup"><span data-stu-id="0a544-175">There should be a place to enter a **Name**, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

8.  <span data-ttu-id="0a544-176">还有一个 **Ip 地址** 文本框，你可以在此处输入你的用于你的 Director 池的 ip (例如，lyncwebexdir01.contoso.com) 池的负载平衡器 (的 ip 或可能导致相同) 的反向代理 ip，然后单击 "确定" 或执行外部 DNS 中的任何操作以接受此条目的创建。</span><span class="sxs-lookup"><span data-stu-id="0a544-176">There should also be an **IP Address** text box, here’s where you’ll enter the IP for your for your Director pool (for example, lyncwebexdir01.contoso.com) or possibly the IP of your pool’s load balancer (or a reverse proxy IP that leads to the same) and then click OK or take whatever action in the external DNS to accept the creation of this entry.</span></span> <span data-ttu-id="0a544-177">如上面的步骤4中所述，如果你没有控制器池，则需要根据需要使用前端池 IP 地址或已设置的单服务器 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="0a544-177">As noted in Step 4, above, if you don’t have a Director pool, you’ll need to use the Front End pool IP address or the single-server IP address you have set up, as appropriate.</span></span>

9.  <span data-ttu-id="0a544-178">你需要在 Lync 2013 环境支持的每个 SIP 域的正向查找区域中创建新的自动发现 A 或 AAAA 记录。</span><span class="sxs-lookup"><span data-stu-id="0a544-178">You’ll need to make a new Autodiscover A or AAAA record in the forward lookup zone of each SIP domain that’s supported in your Lync 2013 environment.</span></span>

<span data-ttu-id="0a544-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a544-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

