---
title: 托管 Exchange UM 集成的 Lync Server 2013 支持
description: Lync Server 2013 支持托管 Exchange UM 集成。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for hosted Exchange UM integration
ms:assetid: c7573ec3-013c-48d9-b59b-2a5427e6da35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398821(v=OCS.15)
ms:contentKeyID: 48185376
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88920667d703bc634921903e8e3995cb65db6873
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391808"
---
# <a name="support-for-hosted-exchange-um-integration-in-lync-server-2013"></a><span data-ttu-id="90dce-103">Lync Server 2013 中的托管 Exchange UM 集成支持</span><span class="sxs-lookup"><span data-stu-id="90dce-103">Support for hosted Exchange UM integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90dce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90dce-104">

<span> </span></span></span>

<span data-ttu-id="90dce-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="90dce-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="90dce-106">Lync Server 2013 ExUM 路由应用程序支持与 Exchange 统一消息 (UM) 在本地环境中，Lync Server 2013 和 Exchange UM 都安装在您的企业内部，或在由服务提供商托管的 Exchange UM 中，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="90dce-106">The Lync Server 2013 ExUM Routing application supports integration with Exchange Unified Messaging (UM) in an on-premises environment, where Lync Server 2013 and Exchange UM are both installed locally within your enterprise, or in with Exchange UM hosted by a service provider, as shown in the following diagram.</span></span>

<span data-ttu-id="90dce-107">![本地 Lync Server Exchange UM 部署](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "本地 Lync Server Exchange UM 部署")</span><span class="sxs-lookup"><span data-stu-id="90dce-107">![On-premises Lync Server Exchange UM Deployment](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "On-premises Lync Server Exchange UM Deployment")</span></span>

<span data-ttu-id="90dce-108">支持下列模式：</span><span class="sxs-lookup"><span data-stu-id="90dce-108">The following modes are supported:</span></span>

  - <span data-ttu-id="90dce-109">**本地模式**   Lync Server 2013 和 Exchange UM 均部署在企业内的本地服务器上。</span><span class="sxs-lookup"><span data-stu-id="90dce-109">**On-premises Mode**   Lync Server 2013 and Exchange UM are both deployed on local servers within your enterprise.</span></span>

  - <span data-ttu-id="90dce-110">**跨界模式**   Lync Server 2013 部署在你的企业内的本地服务器上，Exchange UM 托管在一个联机服务提供商的设备（如 Microsoft Exchange Online 数据中心）中。</span><span class="sxs-lookup"><span data-stu-id="90dce-110">**Cross-premises Mode**   Lync Server 2013 is deployed on local servers within your enterprise and Exchange UM is hosted in an online service provider’s facility, such as a Microsoft Exchange Online data center.</span></span>

  - <span data-ttu-id="90dce-111">**混合模式**   您的 Lync Server 2013 部署在您的企业中的本地服务器上有一些用户邮箱，并且某些邮箱驻留在托管 Exchange 服务数据中心中。</span><span class="sxs-lookup"><span data-stu-id="90dce-111">**Mixed Mode**   Your Lync Server 2013 deployment has some user mailboxes homed on local servers running Microsoft Exchange Server within your enterprise and some mailboxes homed in a hosted Exchange service data center.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="90dce-112">在评估和 stepwise 用户迁移到托管 Exchange UM 的过程中，混合模式可用作过渡式解决方案，如果你选择在迁移其他用户之后将某些用户的 Exchange UM 服务保留在本地，则为永久解决方案。</span><span class="sxs-lookup"><span data-stu-id="90dce-112">Mixed mode can be used as a transitional solution during evaluation and stepwise migration of users to hosted Exchange UM, or as a permanent solution if you opt to keep some users’ Exchange UM services on-premises after migrating others.</span></span>

    
    </div>

<span data-ttu-id="90dce-113">若要将 Lync Server 2013 与托管 Exchange UM 集成，必须配置 *共享 SIP 地址空间* (也称为 *拆分域*) 。</span><span class="sxs-lookup"><span data-stu-id="90dce-113">To integrate Lync Server 2013 with hosted Exchange UM, you must configure a *shared SIP address space* (also called a *split domain*).</span></span> <span data-ttu-id="90dce-114">在此配置中，Lync Server 2013 和第三方托管 Exchange UM 服务提供商可以访问相同的 SIP 域地址空间。</span><span class="sxs-lookup"><span data-stu-id="90dce-114">In this configuration, both Lync Server 2013 and the third-party hosted Exchange UM service provider can access the same SIP domain address space.</span></span> <span data-ttu-id="90dce-115">有关详细信息，请参阅规划文档中的 [Lync Server 2013 中的托管 EXCHANGE UM 集成体系结构](lync-server-2013-hosted-exchange-um-integration-architecture.md) 。</span><span class="sxs-lookup"><span data-stu-id="90dce-115">For details, see [Hosted Exchange UM integration architecture in Lync Server 2013](lync-server-2013-hosted-exchange-um-integration-architecture.md) in the Planning documentation.</span></span>

<span data-ttu-id="90dce-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90dce-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

