---
title: 为远程呼叫控制配置受信任的应用程序项
description: 配置远程呼叫控制的受信任的应用程序条目。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a trusted application entry for remote call control
ms:assetid: 37777f93-8b24-40cf-808e-7c6230eb2132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558636(v=OCS.15)
ms:contentKeyID: 48183829
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa5341dc220853670cf000f5b0d5dc379c02fa51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434149"
---
# <a name="configure-a-trusted-application-entry-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="47d06-103">在 Lync Server 2013 中为远程呼叫控制配置受信任的应用程序项</span><span class="sxs-lookup"><span data-stu-id="47d06-103">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47d06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47d06-104">

<span> </span></span></span>

<span data-ttu-id="47d06-105">_**主题上次修改时间：** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="47d06-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="47d06-106">必须将 SIP/CSTA 网关配置为受信任的应用程序，Lync 服务器才能应用静态路由以将呼叫路由到网关。</span><span class="sxs-lookup"><span data-stu-id="47d06-106">The SIP/CSTA gateway must be configured as a trusted application in order for Lync Server to apply a static route to route calls to the gateway.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="47d06-107">如果你要从早期版本的 Lync Server 部署迁移用户，请确保已删除所有现有的受信任的应用程序条目 (以前称为已授权的主机条目) 你在执行本主题中的步骤之前为 SIP/CSTA 网关创建的。</span><span class="sxs-lookup"><span data-stu-id="47d06-107">If you're migrating users from a previous version of Lync Server deployment, be sure that you removed all existing trusted application entries (previously known as authorized host entries) you created for the SIP/CSTA gateway before following the procedures in this topic.</span></span> <span data-ttu-id="47d06-108">有关详细信息，请参阅 <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">在 Lync Server 2013 中删除旧版授权主机 (可选) </A>。</span><span class="sxs-lookup"><span data-stu-id="47d06-108">For details, see <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">Remove a legacy authorized host in Lync Server 2013 (optional)</A>.</span></span><BR><span data-ttu-id="47d06-109">如果你计划使用传输控制协议 (TCP) 连接来部署新的远程呼叫控制，则需要验证是否应在现有的受信任的应用程序和池上设置 " <STRONG>限制对所选 IP 地址的服务使用</STRONG> "，如果你想要对新的受信任的应用程序使用相同的 TCP 端口。</span><span class="sxs-lookup"><span data-stu-id="47d06-109">If you plan to deploy new remote call control by using a Transmission Control Protocol (TCP) connection, you need to verify that <STRONG>Limit service usage to selected IP addresses</STRONG> should be set on existing trusted applications and pools, if you want to use the same TCP port for the new trusted application.</span></span>



</div>

<div>

## <a name="to-configure-a-trusted-application-entry-for-the-sipcsta-gateway"></a><span data-ttu-id="47d06-110">为 SIP/CSTA 网关配置受信任的应用程序条目</span><span class="sxs-lookup"><span data-stu-id="47d06-110">To configure a trusted application entry for the SIP/CSTA gateway</span></span>

1.  <span data-ttu-id="47d06-111">登录到安装了 Lync Server 命令行管理程序的计算机上作为 RTCUniversalServerAdmins 组的成员或基于角色的访问控制 (已向其分配 **CsTrustedApplicationPool** CMDLET 的 RBAC) 角色。</span><span class="sxs-lookup"><span data-stu-id="47d06-111">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or a role-based access control (RBAC) role to which you have assigned the **New-CsTrustedApplicationPool** cmdlet.</span></span>

2.  <span data-ttu-id="47d06-112">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="47d06-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="47d06-113">若要创建受信任的应用程序条目，请执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="47d06-113">To create a trusted application entry, do one of the following:</span></span>
    
      - <span data-ttu-id="47d06-114">对于传输层安全性 (TLS) 连接，请在命令提示符处键入以下内容：</span><span class="sxs-lookup"><span data-stu-id="47d06-114">For a Transport Layer Security (TLS) connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplicationPool -Identity <FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        <span data-ttu-id="47d06-115">例如：</span><span class="sxs-lookup"><span data-stu-id="47d06-115">For example:</span></span>
        
            New-CsTrustedApplicationPool -Identity rccgateway.contoso.net -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true
    
      - <span data-ttu-id="47d06-116">对于 TCP) 连接的传输控制协议 (，请在命令提示符处键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="47d06-116">For a Transmission Control Protocol (TCP) connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplicationPool -Identity <IP address or FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        <span data-ttu-id="47d06-117">例如：</span><span class="sxs-lookup"><span data-stu-id="47d06-117">For example:</span></span>
        
            New-CsTrustedApplicationPool -Identity 192.168.0.240 -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true

4.  <span data-ttu-id="47d06-118">若要向池中添加受信任的应用程序，请执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="47d06-118">To add the trusted application to the pool, do one of the following:</span></span>
    
      - <span data-ttu-id="47d06-119">对于 TLS 连接，请在命令提示符处键入以下内容：</span><span class="sxs-lookup"><span data-stu-id="47d06-119">For a TLS connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway>
        
        <span data-ttu-id="47d06-120">例如：</span><span class="sxs-lookup"><span data-stu-id="47d06-120">For example:</span></span>
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn rccgateway.contoso.net -Port 5065
    
      - <span data-ttu-id="47d06-121">对于 TCP 连接，请在命令提示符处键入以下内容：</span><span class="sxs-lookup"><span data-stu-id="47d06-121">For a TCP connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <IP address or FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway> -EnableTcp
        
        <span data-ttu-id="47d06-122">例如：</span><span class="sxs-lookup"><span data-stu-id="47d06-122">For example:</span></span>
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn 192.169.0.240 -Port 5065 -EnableTcp

5.  <span data-ttu-id="47d06-123">若要实现对拓扑的已发布更改，请在命令提示符处键入以下内容：</span><span class="sxs-lookup"><span data-stu-id="47d06-123">To implement the published changes you have made to the topology, type the following at the command prompt:</span></span>
    
        Enable-CsTopology

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="47d06-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="47d06-124">See Also</span></span>


[<span data-ttu-id="47d06-125">在 Lync Server 2013 中为远程呼叫控制配置静态路由</span><span class="sxs-lookup"><span data-stu-id="47d06-125">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)  
[<span data-ttu-id="47d06-126">在 Lync Server 2013 中定义 SIP/CSTA 网关 IP 地址</span><span class="sxs-lookup"><span data-stu-id="47d06-126">Define a SIP/CSTA gateway IP address in Lync Server 2013</span></span>](lync-server-2013-define-a-sip-csta-gateway-ip-address.md)  
  

<span data-ttu-id="47d06-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47d06-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

