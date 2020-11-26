---
title: Lync Server 2013：定义 SIP/CSTA 网关 IP 地址
description: Lync Server 2013：定义 SIP/CSTA 网关 IP 地址。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define a SIP/CSTA gateway IP address
ms:assetid: ae944057-3ad6-4474-a09b-81a3d27bd50f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg602125(v=OCS.15)
ms:contentKeyID: 48185073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23286b2748df3af06f905a791bf0ee80c6f0a919
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431139"
---
# <a name="define-a-sipcsta-gateway-ip-address-in-lync-server-2013"></a><span data-ttu-id="906d2-103">在 Lync Server 2013 中定义 SIP/CSTA 网关 IP 地址</span><span class="sxs-lookup"><span data-stu-id="906d2-103">Define a SIP/CSTA gateway IP address in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="906d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="906d2-104">

<span> </span></span></span>

<span data-ttu-id="906d2-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="906d2-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="906d2-106">如果 Lync Server 将连接到你为远程呼叫控制部署的 SIP/CSTA 网关（使用 (TCP) 连接的传输控制协议），则必须在拓扑生成器中定义网关的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="906d2-106">If Lync Server will connect to the SIP/CSTA gateway that you deployed for remote call control by using a Transmission Control Protocol (TCP) connection, then you must define the IP address of the gateway in Topology Builder.</span></span> <span data-ttu-id="906d2-107">对于支持 (TLS) 连接的传输层安全性的网关，此步骤不是必需的。</span><span class="sxs-lookup"><span data-stu-id="906d2-107">This step is not necessary for gateways that support Transport Layer Security (TLS) connections.</span></span> <span data-ttu-id="906d2-108">对于支持 TLS 连接的任何网关，您可以跳过此过程并继续部署远程呼叫控制，方法是按照在 [Lync Server 2013 中启用 "远程呼叫控制" 的 "启用 Lync 用户](lync-server-2013-enable-lync-users-for-remote-call-control.md)" 中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="906d2-108">For any gateway that supports TLS connections, you can skip this procedure and continue deployment of remote call control by following the steps in [Enable Lync users for remote call control in Lync Server 2013](lync-server-2013-enable-lync-users-for-remote-call-control.md).</span></span>

<div>

## <a name="to-define-the-sipcsta-gateway-ip-address-by-using-topology-builder"></a><span data-ttu-id="906d2-109">使用拓扑生成器定义 SIP/CSTA 网关 IP 地址</span><span class="sxs-lookup"><span data-stu-id="906d2-109">To define the SIP/CSTA gateway IP address by using Topology Builder</span></span>

1.  <span data-ttu-id="906d2-110">以 Domain Admins 组和 RTCUniversalServerAdmins 组成员的身份登录安装了拓扑生成器的计算机。</span><span class="sxs-lookup"><span data-stu-id="906d2-110">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="906d2-111">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="906d2-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

3.  <span data-ttu-id="906d2-112">选择下载现有拓扑的选项。</span><span class="sxs-lookup"><span data-stu-id="906d2-112">Choose the option to download an existing topology.</span></span>

4.  <span data-ttu-id="906d2-113">展开 " **受信任的应用程序服务器** " 节点。</span><span class="sxs-lookup"><span data-stu-id="906d2-113">Expand the **Trusted application servers** node.</span></span>

5.  <span data-ttu-id="906d2-114">右键单击您创建的受信任的应用程序池，如在 [Lync Server 2013 中的 "配置远程呼叫控制的受信任的应用程序条目](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)" 中所述，然后单击 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="906d2-114">Right-click the trusted application pool that you created, as described in [Configure a trusted application entry for remote call control in Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md), and then click **Edit Properties**.</span></span>

6.  <span data-ttu-id="906d2-115">清除 " **启用将配置数据复制到此池** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="906d2-115">Clear the **Enable replication of configuration data to this pool** check box.</span></span>

7.  <span data-ttu-id="906d2-116">单击 " **将服务使用限制为所选 IP 地址**"。</span><span class="sxs-lookup"><span data-stu-id="906d2-116">Click **Limit service usage to selected IP addresses**.</span></span> <span data-ttu-id="906d2-117">默认设置是 **使用所有配置的 IP 地址**。</span><span class="sxs-lookup"><span data-stu-id="906d2-117">The default setting is **Use all configured IP addresses**.</span></span>

8.  <span data-ttu-id="906d2-118">在 " **主 IP 地址** " 文本框中，输入 SIP/CSTA 网关的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="906d2-118">In the **Primary IP address** text box, enter the IP address of the SIP/CSTA gateway.</span></span>

9.  <span data-ttu-id="906d2-119">若要更新中央管理存储中的拓扑，请在控制台树中单击 " **Lync Server**"，然后在 " **操作** " 窗格中单击 " **发布**"。</span><span class="sxs-lookup"><span data-stu-id="906d2-119">To update the topology in the Central Management store, in the console tree, click **Lync Server**, and then, from the **Actions** pane, click **Publish**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="906d2-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="906d2-120">See Also</span></span>


[<span data-ttu-id="906d2-121">在 Lync Server 2013 中为远程呼叫控制配置静态路由</span><span class="sxs-lookup"><span data-stu-id="906d2-121">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)  
[<span data-ttu-id="906d2-122">在 Lync Server 2013 中为远程呼叫控制配置受信任的应用程序项</span><span class="sxs-lookup"><span data-stu-id="906d2-122">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)  
  

<span data-ttu-id="906d2-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="906d2-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

