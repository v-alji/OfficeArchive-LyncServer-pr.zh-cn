---
title: 配置本地 Lync Server 与 Exchange Online 集成
description: 配置本地 Lync Server 与 Exchange Online 集成。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring on-premises Lync Server integration with Exchange Online
ms:assetid: 95a20117-2064-43c4-94fe-cac892cadb6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh533880(v=OCS.15)
ms:contentKeyID: 48184900
ms.date: 03/30/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59c612bcdcdf4803bd6f9f2b38f1f9bb7dbad016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432833"
---
# <a name="configuring-on-premises-lync-server-2013-integration-with-exchange-online"></a><span data-ttu-id="0c687-103">配置本地 Lync Server 2013 与 Exchange Online 集成</span><span class="sxs-lookup"><span data-stu-id="0c687-103">Configuring on-premises Lync Server 2013 integration with Exchange Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c687-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c687-104">

<span> </span></span></span>

<span data-ttu-id="0c687-105">_**主题上次修改时间：** 2018-03-30_</span><span class="sxs-lookup"><span data-stu-id="0c687-105">_**Topic Last Modified:** 2018-03-30_</span></span>

<span data-ttu-id="0c687-106">使用本地 Lync Server 2013 部署的客户可以在混合部署模式下在 Microsoft Exchange Online 中配置与 Microsoft Outlook Web App 的互操作性。</span><span class="sxs-lookup"><span data-stu-id="0c687-106">Customers who are using on-premises Lync Server 2013 deployments can configure interoperability with Microsoft Outlook Web App in Microsoft Exchange Online in a hybrid deployment mode.</span></span> <span data-ttu-id="0c687-107">互操作性功能包括单一登录和即时消息 (IM) 以及与 Outlook Web App 接口的状态集成。</span><span class="sxs-lookup"><span data-stu-id="0c687-107">Interoperability features include single sign on and instant messaging (IM) and presence integration with the Outlook Web App interface.</span></span> <span data-ttu-id="0c687-108">若要启用此集成，必须通过完成以下任务在本地 Lync Server 部署中配置边缘服务器：</span><span class="sxs-lookup"><span data-stu-id="0c687-108">To enable this integration, you must configure the Edge Server in your on-premises Lync Server deployment by completing the following tasks:</span></span>

  - <span data-ttu-id="0c687-109">配置共享的 SIP 地址空间</span><span class="sxs-lookup"><span data-stu-id="0c687-109">Configure a shared SIP address space</span></span>

  - <span data-ttu-id="0c687-110">在边缘服务器上配置托管提供商</span><span class="sxs-lookup"><span data-stu-id="0c687-110">Configure a hosting provider on the Edge Server</span></span>

  - <span data-ttu-id="0c687-111">验证更新的中央管理存储的复制</span><span class="sxs-lookup"><span data-stu-id="0c687-111">Verify replication of the updated Central Management store</span></span>

<span data-ttu-id="0c687-112">如果 Lync Server 2013 与 Exchange Online 集成，则尝试从 OWA 登录 IM 的用户被视为远程用户或外部用户。</span><span class="sxs-lookup"><span data-stu-id="0c687-112">If Lync Server 2013 is integrated with Exchange Online, a user who is trying to sign in to IM from OWA is considered a remote or external user.</span></span> <span data-ttu-id="0c687-113">在此方案中，此用户必须分配有以下选项的外部访问策略：</span><span class="sxs-lookup"><span data-stu-id="0c687-113">In this scenario, this user must have an external access policy assigned that has the following option selected:</span></span>

<span data-ttu-id="0c687-114">**启用与远程用户的通信**</span><span class="sxs-lookup"><span data-stu-id="0c687-114">**Enable communications with remote users**</span></span>

<span data-ttu-id="0c687-115">如果你希望你的组织内的用户（如出差的远程办公和用户）能够通过 Internet 连接到 Lync 服务器，请启用此选项。</span><span class="sxs-lookup"><span data-stu-id="0c687-115">Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server over the Internet.</span></span>

<span data-ttu-id="0c687-116">有关详细信息，请参阅 [在 Lync Server 2013 中管理外部访问策略](lync-server-2013-manage-external-access-policy-for-your-organization.md)。</span><span class="sxs-lookup"><span data-stu-id="0c687-116">For more information, see [Manage external access policy in Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span></span>

<div>

## <a name="configure-a-shared-sip-address-space"></a><span data-ttu-id="0c687-117">配置共享的 SIP 地址空间</span><span class="sxs-lookup"><span data-stu-id="0c687-117">Configure a Shared SIP Address Space</span></span>

<span data-ttu-id="0c687-118">若要将本地 Lync Server 2013 与 Exchange Online 集成，必须配置共享 SIP 地址空间。</span><span class="sxs-lookup"><span data-stu-id="0c687-118">To integrate on-premises Lync Server 2013 with Exchange Online, you must configure a shared SIP address space.</span></span> <span data-ttu-id="0c687-119">Lync Server 和 Exchange Online 服务均支持相同的 SIP 域地址空间。</span><span class="sxs-lookup"><span data-stu-id="0c687-119">The same SIP domain address space is supported by both Lync Server and the Exchange Online service.</span></span>

<span data-ttu-id="0c687-120">通过使用 Lync Server Management Shell，使用以下示例中显示的参数运行 **CSAccessEdgeConfiguration** cmdlet 来配置联盟的边缘服务器：</span><span class="sxs-lookup"><span data-stu-id="0c687-120">Using the Lync Server Management Shell, configure the Edge Server for federation by running the **Set-CSAccessEdgeConfiguration** cmdlet, using the parameters that are displayed in the following example:</span></span>

    Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

  - <span data-ttu-id="0c687-121">**AllowFederatedUsers** 指定是否允许内部用户与来自联盟域的用户进行通信。</span><span class="sxs-lookup"><span data-stu-id="0c687-121">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains.</span></span> <span data-ttu-id="0c687-122">此属性还确定内部用户是否可以使用 Lync Server 和 Exchange Online 与共享 SIP 地址空间方案中的用户进行通信。</span><span class="sxs-lookup"><span data-stu-id="0c687-122">This property also determines whether internal users can communicate with users in a shared SIP address space scenario with Lync Server and Exchange Online.</span></span>

<span data-ttu-id="0c687-123">有关如何使用 Lync Server 命令行管理程序的详细信息，请参阅 [Lync server 2013 命令行管理](lync-server-2013-lync-server-management-shell.md)程序。</span><span class="sxs-lookup"><span data-stu-id="0c687-123">For details about how to use the Lync Server Management Shell, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="configure-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="0c687-124">在边缘服务器上配置宿主提供程序</span><span class="sxs-lookup"><span data-stu-id="0c687-124">Configure a Hosting Provider on the Edge Server</span></span>

<span data-ttu-id="0c687-125">使用 Lync Server Management Shell 配置边缘服务器上的托管提供程序。</span><span class="sxs-lookup"><span data-stu-id="0c687-125">Use the Lync Server Management Shell to configure a hosting provider on the Edge Server.</span></span> <span data-ttu-id="0c687-126">若要执行此操作，请使用以下示例中的参数运行 **CsHostingProvider** cmdlet：</span><span class="sxs-lookup"><span data-stu-id="0c687-126">To do this, run the **New-CsHostingProvider** cmdlet, using the parameters in the following example:</span></span>

    New-CsHostingProvider -Identity "Exchange Online" -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFqdn "exap.um.outlook.com" -IsLocal $False -VerificationLevel UseSourceVerification

<div>


> [!NOTE]
> <span data-ttu-id="0c687-127">如果您在中国使用 21Vianet 运营的 Office 365，请将此示例中 <STRONG>ProxyFqdn</STRONG> 参数的值（“exap.um.outlook.com”）替换为 21Vianet 运营的服务的 FQDN：“exap.um.partner.outlook.cn”。</span><span class="sxs-lookup"><span data-stu-id="0c687-127">If you are using Office 365 operated by 21Vianet in China, replace the value for the <STRONG>ProxyFqdn</STRONG> parameter in this example ("exap.um.outlook.com") with the FQDN for the service operated by 21Vianet: "exap.um.partner.outlook.cn".</span></span>



</div>

  - <span data-ttu-id="0c687-128">**Identity** 将为您创建的宿主提供程序指定一个唯一的字符串值标识符（例如“Exchange Online”）。</span><span class="sxs-lookup"><span data-stu-id="0c687-128">**Identity** specifies a unique string value identifier for the hosting provider that you are creating (for example, "Exchange Online").</span></span> <span data-ttu-id="0c687-129">包含空格的值必须用双引号引起来。</span><span class="sxs-lookup"><span data-stu-id="0c687-129">Values that contain spaces must be in double quotation marks.</span></span>

  - <span data-ttu-id="0c687-130">**Enabled** 指示您的域与承载服务提供商之间的网络连接是否已启用。</span><span class="sxs-lookup"><span data-stu-id="0c687-130">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled.</span></span> <span data-ttu-id="0c687-131">必须将其设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="0c687-131">This must be set to **True**.</span></span>

  - <span data-ttu-id="0c687-132">**EnabledSharedAddressSpace** 指示是否将在共享的 SIP 地址空间方案中使用托管提供程序。</span><span class="sxs-lookup"><span data-stu-id="0c687-132">**EnabledSharedAddressSpace** indicates whether the hosting provider will be used in a shared SIP address space scenario.</span></span> <span data-ttu-id="0c687-133">必须将其设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="0c687-133">This must be set to **True**.</span></span>

  - <span data-ttu-id="0c687-134">**HostsOCSUsers** 指示托管提供商是否用于托管 Office 通信服务器或 Lync 服务器。</span><span class="sxs-lookup"><span data-stu-id="0c687-134">**HostsOCSUsers** indicates whether the hosting provider is used to host Office Communications Server or Lync Server.</span></span> <span data-ttu-id="0c687-135">必须将其设置为 **False**。</span><span class="sxs-lookup"><span data-stu-id="0c687-135">This must be set to **False**.</span></span>

  - <span data-ttu-id="0c687-136">**ProxyFQDN** 指定宿主提供程序所使用的代理服务器的完全限定域名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="0c687-136">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider.</span></span> <span data-ttu-id="0c687-137">对于 Exchange Online，FQDN 为 exap.um.outlook.com。</span><span class="sxs-lookup"><span data-stu-id="0c687-137">For Exchange Online, the FQDN is exap.um.outlook.com.</span></span>

  - <span data-ttu-id="0c687-138">**IsLocal** 指示你的 Lync server 拓扑中是否包含托管提供程序使用的代理服务器。</span><span class="sxs-lookup"><span data-stu-id="0c687-138">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server topology.</span></span> <span data-ttu-id="0c687-139">必须将其设置为 **False**。</span><span class="sxs-lookup"><span data-stu-id="0c687-139">This must be set to **False**.</span></span>

  - <span data-ttu-id="0c687-140">**VerificationLevel** 指示发送到托管提供商的邮件或从托管提供商发送的邮件所允许的验证级别。</span><span class="sxs-lookup"><span data-stu-id="0c687-140">**VerificationLevel** indicates the verification level allowed for messages that are sent to and from the hosted provider.</span></span> <span data-ttu-id="0c687-141">指定 **UseSourceVerification**。</span><span class="sxs-lookup"><span data-stu-id="0c687-141">Specify **UseSourceVerification**.</span></span> <span data-ttu-id="0c687-142">此选项依赖于从托管提供程序发送的消息中包含的验证级别。</span><span class="sxs-lookup"><span data-stu-id="0c687-142">This option relies on the verification level that is included in messages that are sent from the hosting provider.</span></span> <span data-ttu-id="0c687-143">如果未指定此级别，邮件将因无法验证而被拒绝。</span><span class="sxs-lookup"><span data-stu-id="0c687-143">If this level is not specified, the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="verify-replication-of-the-updated-central-management-store"></a><span data-ttu-id="0c687-144">确保复制更新后的中央管理存储</span><span class="sxs-lookup"><span data-stu-id="0c687-144">Verify Replication of the Updated Central Management Store</span></span>

<span data-ttu-id="0c687-145">通过使用上述部分中的 cmdlet 所做的更改会自动应用到边缘服务器，并且通常需要的时间不超过一分钟才能进行复制。</span><span class="sxs-lookup"><span data-stu-id="0c687-145">The changes that you made by using the cmdlets in the preceding sections are automatically applied to the Edge Server, and generally take less than one minute to replicate.</span></span> <span data-ttu-id="0c687-146">你可以使用以下 cmdlet 验证复制状态以及是否已将更改应用到 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="0c687-146">You can verify the replication status and that the changes were applied to your Edge Server by using the following cmdlets.</span></span>

<span data-ttu-id="0c687-147">若要在 Lync Server 部署中的内部服务器上验证复制更新，请运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="0c687-147">To verify replication updates on a server internal in your Lync Server deployment, run the following cmdlet:</span></span>

    Get-CsManagementStoreReplicationStatus

<span data-ttu-id="0c687-148">若要验证是否已应用更改，请在 Edge 服务器上运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="0c687-148">To verify that the changes were applied, run the following cmdlet on the Edge Server:</span></span>

    Get-CsHostingProvider -LocalStore

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0c687-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0c687-149">See Also</span></span>


[<span data-ttu-id="0c687-150">在托管 Exchange UM 上提供 Lync Server 2013 用户语音邮件</span><span class="sxs-lookup"><span data-stu-id="0c687-150">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md)  
[<span data-ttu-id="0c687-151">Lync Server 2013 中的托管 Exchange 统一消息集成</span><span class="sxs-lookup"><span data-stu-id="0c687-151">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-unified-messaging-integration.md)  
  

<span data-ttu-id="0c687-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c687-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
