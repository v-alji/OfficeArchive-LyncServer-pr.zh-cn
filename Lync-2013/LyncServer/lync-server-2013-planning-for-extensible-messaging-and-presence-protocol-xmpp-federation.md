---
title: 规划可扩展消息和状态协议 (XMPP) 联盟
description: 规划可扩展消息和状态协议 (XMPP) 联盟。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for extensible messaging and presence protocol (XMPP) federation
ms:assetid: 952b33e2-1f58-4831-9a39-1dfec2a316ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205107(v=OCS.15)
ms:contentKeyID: 48184892
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 511273b69181334821f446bcc4424641367ecf51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424567"
---
# <a name="planning-for-extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="3a5c2-103">在 Lync Server 2013 中规划可扩展消息和状态协议 (XMPP) 联盟</span><span class="sxs-lookup"><span data-stu-id="3a5c2-103">Planning for extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3a5c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3a5c2-104">

<span> </span></span></span>

<span data-ttu-id="3a5c2-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="3a5c2-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="3a5c2-106">以前版本的 Lync Server 和 Office 通信服务器提供了可扩展消息和状态协议 (XMPP) 网关，可部署为单独的服务器角色，以便允许与 XMPP 部署进行联盟。</span><span class="sxs-lookup"><span data-stu-id="3a5c2-106">Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments.</span></span> <span data-ttu-id="3a5c2-107">在 Microsoft Lync Server 2013 中，XMPP 功能可以部署为功能。</span><span class="sxs-lookup"><span data-stu-id="3a5c2-107">In Microsoft Lync Server 2013, the XMPP functionality can be deployed as a feature.</span></span> <span data-ttu-id="3a5c2-108">XMPP 功能在两个部分中安装：在边缘服务器上运行的 XMPP 代理和在前端服务器上运行的 XMPP 网关。</span><span class="sxs-lookup"><span data-stu-id="3a5c2-108">XMPP functionality is installed in two parts: an XMPP proxy that runs on the Edge Server and the XMPP gateway that runs on the Front End Servers.</span></span>

<span data-ttu-id="3a5c2-109">在 [Lync Server 2013 中部署外部用户访问权限](lync-server-2013-deploying-external-user-access.md) 中介绍了 XMPP 的部署和配置在你的防火墙上部署外部用户访问，并通过在防火墙上定义端口和协议规则、配置证书以及添加 DNS 记录。</span><span class="sxs-lookup"><span data-stu-id="3a5c2-109">Deployment and configuration of XMPP is covered in [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) You plan for supporting XMPP in your organization by defining port and protocol rules on your firewall, configuration of certificates, and adding DNS records.</span></span> <span data-ttu-id="3a5c2-110">本节中的以下主题概述了为部署成功规划 XMPP 联合所需的信息。</span><span class="sxs-lookup"><span data-stu-id="3a5c2-110">The following topics in this section summarize the information that you will need to successfully plan XMPP federation for your deployment.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="3a5c2-p103">Microsoft 已测试 Lync Server 2013 的 XMPP 功能，并且支持该功能与 Google Talk 进行即时消息传递联盟。对于任何其他 XMPP 系统，请与第三方供应商联系，以确认它们是否支持与 Lync Server 2013 联盟以及获取任何部署或疑难解答建议。</span><span class="sxs-lookup"><span data-stu-id="3a5c2-p103">The XMPP capability of Lync Server 2013 is tested and supported by Microsoft for instant messaging federation with Google Talk. For any other XMPP systems contact the third-party vendor to verify that they support federation with Lync Server 2013, and for any deployment or troubleshooting recommendations.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3a5c2-113">本节内容</span><span class="sxs-lookup"><span data-stu-id="3a5c2-113">In This Section</span></span>

  - [<span data-ttu-id="3a5c2-114">证书摘要-可扩展消息和状态协议 (XMPP 在 Lync Server 2013 中) 联盟</span><span class="sxs-lookup"><span data-stu-id="3a5c2-114">Certificate summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-extensible-messaging-and-presence-protocol-xmpp-federation.md)

  - [<span data-ttu-id="3a5c2-115">端口摘要-可扩展消息和状态协议 (XMPP 在 Lync Server 2013 中) 联盟</span><span class="sxs-lookup"><span data-stu-id="3a5c2-115">Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>](lync-server-2013-port-summary-extensible-messaging-and-presence-protocol-xmpp-federation.md)

  - [<span data-ttu-id="3a5c2-116">DNS 摘要-可扩展消息和状态协议 (XMPP 在 Lync Server 2013 中) 联盟</span><span class="sxs-lookup"><span data-stu-id="3a5c2-116">DNS summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>](lync-server-2013-dns-summary-extensible-messaging-and-presence-protocol-xmpp-federation.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3a5c2-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a5c2-117">See Also</span></span>


[<span data-ttu-id="3a5c2-118">在 Lync Server 2013 中设置 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="3a5c2-118">Setting up XMPP federation in Lync Server 2013</span></span>](lync-server-2013-setting-up-xmpp-federation.md)  
[<span data-ttu-id="3a5c2-119">在 Lync Server 2013 中配置策略以控制 XMPP 联盟用户访问</span><span class="sxs-lookup"><span data-stu-id="3a5c2-119">Configure policies to control XMPP federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-xmpp-federated-user-access.md)  


[<span data-ttu-id="3a5c2-120">在 Lync Server 2013 中管理组织的 XMPP 联盟伙伴</span><span class="sxs-lookup"><span data-stu-id="3a5c2-120">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
<span data-ttu-id="3a5c2-121">[CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg425805(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3a5c2-121">[Get-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg425805(v=OCS.15))</span></span>  
<span data-ttu-id="3a5c2-122">[Get-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ204981(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3a5c2-122">[Get-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ204981(v=OCS.15))</span></span>  
<span data-ttu-id="3a5c2-123">[Get-CsXmppGatewayConfiguration](https://technet.microsoft.com/library/JJ204869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="3a5c2-123">[Get-CsXmppGatewayConfiguration](https://technet.microsoft.com/library/JJ204869(v=OCS.15))</span></span>  
  

<span data-ttu-id="3a5c2-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3a5c2-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

