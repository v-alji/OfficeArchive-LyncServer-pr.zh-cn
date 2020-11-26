---
title: 更新 DNS SRV 记录
description: 更新 DNS SRV 记录。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Update DNS SRV records
ms:assetid: 9542b91a-108c-4980-89ec-634905cbbf26
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688139(v=OCS.15)
ms:contentKeyID: 49733739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24161074e8f3bcf7e296a957588eeb59d5f2ad1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446547"
---
# <a name="update-dns-srv-records"></a><span data-ttu-id="cfbc4-103">更新 DNS SRV 记录</span><span class="sxs-lookup"><span data-stu-id="cfbc4-103">Update DNS SRV records</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cfbc4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cfbc4-104">

<span> </span></span></span>

<span data-ttu-id="cfbc4-105">_**主题上次修改时间：** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="cfbc4-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="cfbc4-106">若要成功完成此过程，你应作为域管理员组的成员或 DnsAdmins 组的成员登录到服务器或域。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-106">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="cfbc4-107">本主题介绍了如何在迁移到 Lync Server 2013 后更新域名系统 (DNS) 记录。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-107">This topic describes how to update the Domain Name System (DNS) records after migrating to Lync Server 2013.</span></span> <span data-ttu-id="cfbc4-108">将所有用户移到 Lync Server 2013 之后，但在取消旧版 Lync Server 2010 池或控制器之前，必须在每个 SIP 域的内部 DNS 中更新 DNS SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-108">After all users have been moved to Lync Server 2013, but before the legacy Lync Server 2010 pool or Director is decommissioned, you must update the DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="cfbc4-109">此过程假定你的内部 DNS 具有适用于你的 SIP 用户域的区域。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-109">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<span data-ttu-id="cfbc4-110">**配置 DNS SRV 记录**</span><span class="sxs-lookup"><span data-stu-id="cfbc4-110">**To configure a DNS SRV record**</span></span>

1.  <span data-ttu-id="cfbc4-111">在 DNS 服务器上，单击 " **开始**"，单击 " **管理工具**"，然后单击 " **DNS**"。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-111">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="cfbc4-112">在 SIP 域的控制台树中，展开 "**正向查找区域**"，展开安装了 Lync Server 2013 的 SIP 域，然后导航到 **\_ tcp** 设置。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-112">In the console tree for your SIP domain, expand **Forward Lookup Zones**, expand the SIP domain in which Lync Server 2013 is installed, and navigate to the **\_tcp** setting.</span></span>

3.  <span data-ttu-id="cfbc4-113">在右窗格中，右键单击 " **\_ sipinternaltls** "，然后选择 "**属性**"。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-113">In the right pane, right click **\_sipinternaltls** and select **Properties**.</span></span>

4.  <span data-ttu-id="cfbc4-114">在 **提供此服务的主机** 中，更新主机 FQDN 以指向 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-114">In **Host offering this service**, update the host FQDN to point to the Lync Server 2013 pool.</span></span>

5.  <span data-ttu-id="cfbc4-115">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-115">Click **OK**.</span></span>

<span data-ttu-id="cfbc4-116">**验证是否可以解析前端池或标准版服务器的 FQDN**</span><span class="sxs-lookup"><span data-stu-id="cfbc4-116">**To verify that the FQDN of the Front End pool or Standard Edition server can be resolved**</span></span>

1.  <span data-ttu-id="cfbc4-117">登录到域中的客户端计算机。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-117">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="cfbc4-118">单击 **“开始”**，然后单击 **“运行”**。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-118">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="cfbc4-119">在 " **打开** " 框中，键入 **cmd**，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-119">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="cfbc4-120">在命令提示符处，键入 **nslookup** \<FQDN of the Front End pool\> 或 \<FQDN of the Standard Edition server\> ，然后按 ENTER。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-120">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="cfbc4-121">验证您是否收到了解析为 FQDN 的相应 IP 地址的答复。</span><span class="sxs-lookup"><span data-stu-id="cfbc4-121">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="cfbc4-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cfbc4-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

