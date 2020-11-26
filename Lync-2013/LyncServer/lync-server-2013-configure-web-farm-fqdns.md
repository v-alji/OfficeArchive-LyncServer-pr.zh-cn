---
title: Lync Server 2013：配置 Web 场 FQDN
description: Lync Server 2013：配置 web 场 Fqdn。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure web farm FQDNs
ms:assetid: cb25dbbd-dcea-4997-8e14-e5007dd7d3ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429722(v=OCS.15)
ms:contentKeyID: 48185481
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8a07faac4d4809ffe10e7ca3699e7441e6dbcb7b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433547"
---
# <a name="configure-web-farm-fqdns-for-lync-server-2013"></a><span data-ttu-id="411a9-103">为 Lync Server 2013 配置 Web 场 FQDN</span><span class="sxs-lookup"><span data-stu-id="411a9-103">Configure web farm FQDNs for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="411a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="411a9-104">

<span> </span></span></span>

<span data-ttu-id="411a9-105">_**主题上次修改时间：** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="411a9-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="411a9-106">在拓扑生成器中定义了标准版服务器、前端池、控制器或控制器池的配置时，请将外部 web 服务的完全限定的域名配置 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="411a9-106">When you defined the configuration of the Standard Edition server, Front End pool, Director or Director pool in Topology Builder, you configure an external web services fully qualified domain name (FQDN).</span></span> <span data-ttu-id="411a9-107">在托管在标准版服务器或前端池中的客户端登录过程中，已配置的 web 服务 Fqdn 通过带内预配的方式发送。</span><span class="sxs-lookup"><span data-stu-id="411a9-107">During the log on process of a client homed in the Standard Edition server or Front End pool, the configured web services FQDNs are sent by way of in-band provisioning.</span></span> <span data-ttu-id="411a9-108">如果需要添加或更改外部 web 服务 URL，请使用拓扑生成器配置或重新配置 web 服务配置，方法是使用本主题中的过程。</span><span class="sxs-lookup"><span data-stu-id="411a9-108">If you need to add or change the external web services URL, you use Topology Builder to configure or reconfigure the web services configuration using the procedure in this topic.</span></span>

<div>

## <a name="to-configure-an-external-pool-fqdn-for-web-services"></a><span data-ttu-id="411a9-109">为 web 服务配置外部池 FQDN</span><span class="sxs-lookup"><span data-stu-id="411a9-109">To configure an external pool FQDN for web services</span></span>

1.  <span data-ttu-id="411a9-110">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="411a9-110">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="411a9-111">在拓扑生成器中，在 " **标准版前端**"、" **企业版前端**" 和 " **控制器**" 下的控制台树中，右键单击需要编辑的池名称，然后单击 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="411a9-111">In Topology Builder, in the console tree under **Standard Edition Front Ends**, **Enterprise Edition Front Ends**, and **Directors**, right-click the pool name that you need to edit, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="411a9-112">在 " **Web 服务** " 部分中，添加或编辑 **外部 Web 服务 FQDN**。</span><span class="sxs-lookup"><span data-stu-id="411a9-112">In the **Web services** section, add or edit the **External web services FQDN**.</span></span>

4.  <span data-ttu-id="411a9-113">查看和调整 HTTP 和 HTTPS 的 **侦听端口** 。</span><span class="sxs-lookup"><span data-stu-id="411a9-113">Review and adjust the **Listening ports** for both HTTP and HTTPS.</span></span> <span data-ttu-id="411a9-114">默认值将为：</span><span class="sxs-lookup"><span data-stu-id="411a9-114">The defaults will be:</span></span>
    
      - <span data-ttu-id="411a9-115">**侦听端口：** HTTP 8080，HTTPS 4443</span><span class="sxs-lookup"><span data-stu-id="411a9-115">**Listening ports:** HTTP 8080, HTTPS 4443</span></span>
    
      - <span data-ttu-id="411a9-116">**已发布的端口：** HTTP 80，HTTPS 443</span><span class="sxs-lookup"><span data-stu-id="411a9-116">**Published ports:** HTTP 80, HTTPS 443</span></span>
    
    <span data-ttu-id="411a9-117">如果 **侦听端口** 是外部 web 服务将配置为接收来自反向代理的请求的端口，并且 **已发布的端口** 是由反向代理在外部发布的端口，并且在带内配置期间将其传递给客户端。</span><span class="sxs-lookup"><span data-stu-id="411a9-117">Where the **Listening ports** is the port that the external web services will be configured to receive requests from the reverse proxy, and the **Published ports** is the ports that are published externally by the reverse proxy and is communicated to clients during in-band provisioning.</span></span>

5.  <span data-ttu-id="411a9-118">完成添加和更新后，单击 **"确定"** 以继续。</span><span class="sxs-lookup"><span data-stu-id="411a9-118">When you have completed your additions and updates, click **OK** to continue.</span></span>

6.  <span data-ttu-id="411a9-119">右键单击 " **Lync Server 2013**"，然后单击 " **发布**"。</span><span class="sxs-lookup"><span data-stu-id="411a9-119">Right-click **Lync Server 2013**, and then click **Publish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="411a9-120">发布成功完成后，可能会显示一个链接，通知你有需要采取的其他步骤。</span><span class="sxs-lookup"><span data-stu-id="411a9-120">After publishing successfully completes, a link may be presented that informs you that there are additional steps that need to be taken.</span></span> <span data-ttu-id="411a9-121">链接（如果单击）会打开受拓扑生成器中所做更改影响的服务器的列表，该列表要求你在列出的每台服务器上重新运行 Lync Server 部署向导，以便更新添加、删除或更改的组件的配置。</span><span class="sxs-lookup"><span data-stu-id="411a9-121">The link, if clicked, opens a list of servers affected by the changes made in Topology Builder that will require you to re-run the Lync Server Deployment Wizard on each listed server to update the configuration for added, removed, or changed components.</span></span>

    
    </div>

7.  <span data-ttu-id="411a9-122">为组织中的每个标准版服务器、前端池、控制器或控制器池重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="411a9-122">Repeat these steps for each Standard Edition server, Front End pool, Director or Director pool in the organization.</span></span>

<span data-ttu-id="411a9-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="411a9-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

