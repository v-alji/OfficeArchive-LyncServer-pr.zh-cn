---
title: Lync Server 2013：设置 Lync 联盟
description: Lync Server 2013：设置 Lync 联合。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392372"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="97b50-103">在 Lync Server 2013 中设置 Lync 联盟</span><span class="sxs-lookup"><span data-stu-id="97b50-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97b50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97b50-104">

<span> </span></span></span>

<span data-ttu-id="97b50-105">_**主题上次修改时间** ：2014-03-27_</span><span class="sxs-lookup"><span data-stu-id="97b50-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="97b50-106">如果已部署 Edge 服务器，则直接添加联合方案功能。</span><span class="sxs-lookup"><span data-stu-id="97b50-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="97b50-107">如果尚未设置边缘服务器，必须先进行设置。</span><span class="sxs-lookup"><span data-stu-id="97b50-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="97b50-108">有关详细信息，请参阅部署文档中的规划文档和在[Lync Server 2013](lync-server-2013-deploying-external-user-access.md)中部署外部用户访问中的规划 Lync Server [2013](lync-server-2013-planning-for-external-user-access.md)中的外部用户访问。</span><span class="sxs-lookup"><span data-stu-id="97b50-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="97b50-109">如果您打算设置 XMPP 联合身份验证、Lync 联合身份验证或公共即时消息连接的任意组合，您可以同时部署它们，也可以一次部署一个。</span><span class="sxs-lookup"><span data-stu-id="97b50-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="97b50-110">如果您通过拓扑生成器和 Lync Server 命令行管理程序配置选项，然后在为一种、两种或所有三种联合身份验证类型配置选项后，在 Edge 服务器上运行部署向导，您可以减少所需的步骤数。</span><span class="sxs-lookup"><span data-stu-id="97b50-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="97b50-111">在拓扑生成器和部署向导中设置 Lync 联合身份验证</span><span class="sxs-lookup"><span data-stu-id="97b50-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="97b50-112">在前端服务器上，打开"拓扑生成器"。</span><span class="sxs-lookup"><span data-stu-id="97b50-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="97b50-113">展开"边缘池"，然后右键单击 Edge 服务器或边缘服务器池。</span><span class="sxs-lookup"><span data-stu-id="97b50-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="97b50-114">选择"编辑属性"。</span><span class="sxs-lookup"><span data-stu-id="97b50-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="97b50-115">在"常规"下的"编辑属性"中，选择"启用此 Edge 池 (端口 5061) 。</span><span class="sxs-lookup"><span data-stu-id="97b50-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="97b50-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="97b50-116">Click OK.</span></span>

3.  <span data-ttu-id="97b50-117">单击"操作"，选择"拓扑"，然后选择"发布"。</span><span class="sxs-lookup"><span data-stu-id="97b50-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="97b50-118">当系统提示发布拓扑时，请单击"下一步"。</span><span class="sxs-lookup"><span data-stu-id="97b50-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="97b50-119">完成发布后，单击"完成"。</span><span class="sxs-lookup"><span data-stu-id="97b50-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="97b50-120">在 Edge 服务器上，打开 Lync Server 部署向导。</span><span class="sxs-lookup"><span data-stu-id="97b50-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="97b50-121">单击"安装或更新 Lync Server System"，然后单击"设置或删除 Lync Server 组件"。</span><span class="sxs-lookup"><span data-stu-id="97b50-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="97b50-122">再次单击"运行"。</span><span class="sxs-lookup"><span data-stu-id="97b50-122">Click Run Again.</span></span>

5.  <span data-ttu-id="97b50-123">在"设置 Lync Server 组件"中，单击"下一步"。</span><span class="sxs-lookup"><span data-stu-id="97b50-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="97b50-124">摘要屏幕将在执行操作时显示操作。</span><span class="sxs-lookup"><span data-stu-id="97b50-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="97b50-125">部署完成后，单击"查看日志"以查看可用的日志文件。</span><span class="sxs-lookup"><span data-stu-id="97b50-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="97b50-126">单击"完成"完成部署。</span><span class="sxs-lookup"><span data-stu-id="97b50-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="97b50-127">可以选择此选项，但只能将组织中一个 Edge 池或 Edge Server 发布到外部进行联合身份验证。</span><span class="sxs-lookup"><span data-stu-id="97b50-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="97b50-128">联合用户的所有访问（包括公共即时消息 (即时消息) 用户）通过同一边缘池或单个边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="97b50-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="97b50-129">例如，如果部署包括一个 Edge 池或一个部署于纽约且一个部署于伦敦的边缘服务器，并且你启用对纽约 Edge 池或单个 Edge Server 的联合身份验证支持，则联合用户的信号流量将经过纽约 Edge 池或单个边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="97b50-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="97b50-130">这同样适用于 London 用户的通信，尽管 London 内部用户呼叫 London 联盟用户时将使用 London 池或边缘服务器路由 A/V 流量。</span><span class="sxs-lookup"><span data-stu-id="97b50-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="97b50-131">配置与合作伙伴联合</span><span class="sxs-lookup"><span data-stu-id="97b50-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="97b50-132">若要设置与另一个 Microsoft Lync Server 2013、Lync Server 2010、Office Communications Server 2007 R2 或 Office Communicator 2007 的成功联合，请从下表中选择联合类型，并定义 DNS SRV 记录、DNS 主机 (A 或 AAAA for IPv6) 并配置适用于联合身份验证类型的策略：</span><span class="sxs-lookup"><span data-stu-id="97b50-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="97b50-133">联合身份验证类型</span><span class="sxs-lookup"><span data-stu-id="97b50-133">Federation type</span></span></th>
    <th><span data-ttu-id="97b50-134">DNS 记录</span><span class="sxs-lookup"><span data-stu-id="97b50-134">DNS Records</span></span></th>
    <th><span data-ttu-id="97b50-135">策略定义</span><span class="sxs-lookup"><span data-stu-id="97b50-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="97b50-136">注释</span><span class="sxs-lookup"><span data-stu-id="97b50-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="97b50-137">发现的合作伙伴域</span><span class="sxs-lookup"><span data-stu-id="97b50-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="97b50-138">配置格式为 _sipfederationtls._tcp 的 SRV 记录。 &lt;外部域名 &gt; 其中，SRV 记录的端口值为 TCP 5061，并且提供此服务的主机 <strong>定义为</strong> sip。</span><span class="sxs-lookup"><span data-stu-id="97b50-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="97b50-139">&lt;外部域名 &gt; – Access Edge 服务的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="97b50-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="97b50-140">有关创建 SRV 记录的详细信息，请参阅 <a href="lync-server-2013-configure-dns-for-edge-support.md">在 Lync Server 2013</a> 中为边缘支持配置 DNS</span><span class="sxs-lookup"><span data-stu-id="97b50-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="97b50-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">在 Lync Server 2013 中启用或禁用联盟和公共 IM 连接</a></span><span class="sxs-lookup"><span data-stu-id="97b50-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="97b50-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">在 Lync Server 2013 中启用或禁用联盟伙伴发现</a></span><span class="sxs-lookup"><span data-stu-id="97b50-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="97b50-143">以前的版本称为开放增强联合身份验证的这种类型的 <strong>联合</strong>。</span><span class="sxs-lookup"><span data-stu-id="97b50-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="97b50-144">此类型的联合身份验证需要创建 SRV 记录，并且允许其他合作伙伴发现你的联合。</span><span class="sxs-lookup"><span data-stu-id="97b50-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="97b50-145">允许的合作伙伴域</span><span class="sxs-lookup"><span data-stu-id="97b50-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="97b50-146">配置格式为 _sipfederationtls._tcp 的 SRV 记录。 &lt;外部域名 &gt; 其中，SRV 记录的端口值为 TCP 5061，并且提供此服务的主机 <strong>定义为</strong> sip。</span><span class="sxs-lookup"><span data-stu-id="97b50-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="97b50-147">&lt;外部域名 &gt; – Access Edge 服务的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="97b50-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="97b50-148">有关创建 SRV 记录的详细信息，请参阅 <a href="lync-server-2013-configure-dns-for-edge-support.md">在 Lync Server 2013</a> 中为边缘支持配置 DNS</span><span class="sxs-lookup"><span data-stu-id="97b50-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="97b50-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">在 Lync Server 2013 中启用或禁用联盟和公共 IM 连接</a></span><span class="sxs-lookup"><span data-stu-id="97b50-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="97b50-150">以前的版本称为"增强联合身份验证"的此类 <strong>联合</strong>身份验证。</span><span class="sxs-lookup"><span data-stu-id="97b50-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="97b50-151">对于此类联合身份验证，SRV 记录的创建是可选的，允许其他合作伙伴发现联合。</span><span class="sxs-lookup"><span data-stu-id="97b50-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="97b50-152">当然，这是开放式增强 <strong>联合</strong>身份验证或 <strong>已发现的合作伙伴域</strong></span><span class="sxs-lookup"><span data-stu-id="97b50-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="97b50-153">允许的合作伙伴服务器</span><span class="sxs-lookup"><span data-stu-id="97b50-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="97b50-154">在策略中将 SIP 域名和合作伙伴 Edge Server FQDN 配置为联合合作伙伴</span><span class="sxs-lookup"><span data-stu-id="97b50-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="97b50-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">在 Lync Server 2013 中启用或禁用联盟和公共 IM 连接</a></span><span class="sxs-lookup"><span data-stu-id="97b50-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="97b50-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">在 Lync Server 2013 中配置对允许的外部域的支持</a></span><span class="sxs-lookup"><span data-stu-id="97b50-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="97b50-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">在 Lync Server 2013 中配置对阻止的外部域的支持</a></span><span class="sxs-lookup"><span data-stu-id="97b50-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="97b50-158">此联合类型是一对一关系的定义，不允许发现其他联合合作伙伴。</span><span class="sxs-lookup"><span data-stu-id="97b50-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="97b50-159">显式配置每个联合合作伙伴。</span><span class="sxs-lookup"><span data-stu-id="97b50-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="97b50-160">在以前的版本中，这称为直接 <strong>联合</strong></span><span class="sxs-lookup"><span data-stu-id="97b50-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="97b50-161">托管提供商和公共 IM 提供程序</span><span class="sxs-lookup"><span data-stu-id="97b50-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="97b50-162">未为此类型的联合身份验证定义特定的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="97b50-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="97b50-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">在 Lync Server 2013 中启用或禁用联盟和公共 IM 连接</a></span><span class="sxs-lookup"><span data-stu-id="97b50-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="97b50-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">在 Lync Server 2013 中创建或编辑公共 SIP 联盟提供程序</a></span><span class="sxs-lookup"><span data-stu-id="97b50-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="97b50-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">在 Lync Server 2013 中创建或编辑托管的 SIP 联盟提供程序</a></span><span class="sxs-lookup"><span data-stu-id="97b50-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="97b50-166">此联合类型定义要为用户配置的服务和托管提供程序。</span><span class="sxs-lookup"><span data-stu-id="97b50-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="97b50-167">典型用途包括公共 IM 提供商（如 Windows Live Messenger、Yahoo！</span><span class="sxs-lookup"><span data-stu-id="97b50-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="97b50-168">和 AOL，以及 Lync Online 和 Microsoft 365 等托管提供商</span><span class="sxs-lookup"><span data-stu-id="97b50-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="97b50-169">从 2012 年 9 月 1 日起，Microsoft Lync 公共 IM 连接用户订阅许可证 ("PIC USL") 不再可用于购买新协议或续订协议。</span><span class="sxs-lookup"><span data-stu-id="97b50-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="97b50-170">具有活动许可证的客户将能够继续与 Yahoo！</span><span class="sxs-lookup"><span data-stu-id="97b50-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="97b50-171">Messenger，直到服务关闭日期。</span><span class="sxs-lookup"><span data-stu-id="97b50-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="97b50-172">AOL 和 Yahoo！ 的结束日期为 2014 年 6 月</span><span class="sxs-lookup"><span data-stu-id="97b50-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="97b50-173">已宣布。</span><span class="sxs-lookup"><span data-stu-id="97b50-173">has been announced.</span></span> <span data-ttu-id="97b50-174">有关详细信息，请参阅 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">支持 Lync Server 2013 中的公共即时消息连接</A>。</span><span class="sxs-lookup"><span data-stu-id="97b50-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="97b50-175">PIC USL 是 Lync Server 或 Office Communications Server 与 Yahoo！ 联合所需的按用户每月订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="97b50-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="97b50-176">Messenger。</span><span class="sxs-lookup"><span data-stu-id="97b50-176">Messenger.</span></span> <span data-ttu-id="97b50-177">Microsoft 提供此服务的能力取决于 Yahoo！ 的支持，而 Yahoo！ 的基础协议正在逐渐减少。</span><span class="sxs-lookup"><span data-stu-id="97b50-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="97b50-178">Lync 比以往任何时候都更加强大，是一种强大的工具，用于跨组织和与世界各地的个人进行连接。</span><span class="sxs-lookup"><span data-stu-id="97b50-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="97b50-179">与 Windows Live Messenger 联合身份验证不需要除 Lync 标准 CAL 之外的其他用户/设备许可证。</span><span class="sxs-lookup"><span data-stu-id="97b50-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="97b50-180">Skype 联合身份验证将添加到此列表，使 Lync 用户能够使用即时消息和语音联系数亿用户。</span><span class="sxs-lookup"><span data-stu-id="97b50-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="97b50-181">为 IPv6 记录和 DNS SRV (A 或 AAAA 定义和) DNS 主机</span><span class="sxs-lookup"><span data-stu-id="97b50-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="97b50-182">使用 Lync Server 控制面板或 Lync Server 命令行管理程序以及相应的 cmdlet 定义和配置任何策略。</span><span class="sxs-lookup"><span data-stu-id="97b50-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="97b50-183">有关 Lync Server Management Shell cmdlet 的详细信息，请参阅[Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)中的联合和外部访问 cmdlet</span><span class="sxs-lookup"><span data-stu-id="97b50-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="97b50-184">Lync Room System (LRS) 未显示由联盟 Lync 合作伙伴中的组织者发送的会议的"加入"按钮。</span><span class="sxs-lookup"><span data-stu-id="97b50-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="97b50-185">若要在 LRS 上显示会议加入链接，发送组织必须使用以下 cmdlet 启用 TNEF：</span><span class="sxs-lookup"><span data-stu-id="97b50-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="97b50-186">请注意，这不特定于 LRS。</span><span class="sxs-lookup"><span data-stu-id="97b50-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="97b50-187">在这种情况下，Outlook 和 Lync 不会显示"加入"链接，因为不会传输 MAPI 属性，但在 Outlook 中，用户可以打开会议邀请并单击会议 URL。</span><span class="sxs-lookup"><span data-stu-id="97b50-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="97b50-188">当 TNEFEnabled 设置为 true Exchange 2013 时，不会删除 MAPI 属性（包括 OnlineMeetingExternalLink）并且提醒上会显示"联接"按钮。</span><span class="sxs-lookup"><span data-stu-id="97b50-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="97b50-189">另请参阅</span><span class="sxs-lookup"><span data-stu-id="97b50-189">See Also</span></span>


[<span data-ttu-id="97b50-190">在 Lync Server 2013 中规划 SIP、XMPP 联合和公共即时消息</span><span class="sxs-lookup"><span data-stu-id="97b50-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="97b50-191">管理对 Lync Server 2013 的联盟和外部访问</span><span class="sxs-lookup"><span data-stu-id="97b50-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="97b50-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97b50-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

