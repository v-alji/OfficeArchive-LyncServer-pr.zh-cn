---
title: Lync Server 2013：规划 Exchange 统一消息集成
description: Lync Server 2013：规划 Exchange 统一消息集成。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Exchange Unified Messaging integration
ms:assetid: e7c63a71-2d99-4aa9-b649-36c1a431bdf1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399031(v=OCS.15)
ms:contentKeyID: 48185880
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31296444d21a86a7837da3e29fc2152f3ca96ccc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442997"
---
# <a name="planning-for-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="e5f47-103">在 Lync Server 2013 中规划 Exchange 统一消息集成</span><span class="sxs-lookup"><span data-stu-id="e5f47-103">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e5f47-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e5f47-104">

<span> </span></span></span>

<span data-ttu-id="e5f47-105">_**主题上次修改时间：** 2012-10-13_</span><span class="sxs-lookup"><span data-stu-id="e5f47-105">_**Topic Last Modified:** 2012-10-13_</span></span>

<span data-ttu-id="e5f47-106">Lync Server 2013 支持与 Exchange 统一消息 (UM) ，以便将语音消息和电子邮件消息合并到单个消息传递基础结构中。</span><span class="sxs-lookup"><span data-stu-id="e5f47-106">Lync Server 2013 supports integration with Exchange Unified Messaging (UM) for combining voice messaging and email messaging into a single messaging infrastructure.</span></span> <span data-ttu-id="e5f47-107">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 和 Microsoft Exchange Server 2010 中，Exchange 统一消息 (UM) 是你可以安装和配置的若干 Exchange Server 角色之一。</span><span class="sxs-lookup"><span data-stu-id="e5f47-107">In Microsoft Exchange Server 2007 Service Pack 1 (SP1) and Microsoft Exchange Server 2010, Exchange Unified Messaging (UM) is one of several Exchange server roles that you can install and configure.</span></span>

<span data-ttu-id="e5f47-108">在 Microsoft Exchange Server 2013 中，Exchange UM 在 Exchange 邮箱服务器上作为服务运行。</span><span class="sxs-lookup"><span data-stu-id="e5f47-108">In Microsoft Exchange Server 2013, Exchange UM runs as a service on an Exchange Mailbox server.</span></span> <span data-ttu-id="e5f47-109">对于 Lync Server 2013 企业语音部署，统一消息将语音消息和电子邮件合并到一个可通过电话 (Outlook Voice Access) 或计算机上的应用程序。</span><span class="sxs-lookup"><span data-stu-id="e5f47-109">For Lync Server 2013 Enterprise Voice deployments, Unified Messaging combines voice messaging and email messaging into a single store that is available from a telephone (Outlook Voice Access) or a computer.</span></span> <span data-ttu-id="e5f47-110">统一消息和 Lync Server 2013 协同工作，向企业语音用户提供呼叫应答、Outlook Voice Access 和自动助理服务。</span><span class="sxs-lookup"><span data-stu-id="e5f47-110">Unified Messaging and Lync Server 2013 work together to provide call answering, Outlook Voice Access, and auto-attendant services to users of Enterprise Voice.</span></span>

<span data-ttu-id="e5f47-111">有关 Microsoft Exchange Server 2013 中的体系结构更改的详细信息，请参阅 Microsoft Exchange Server 2013 文档中的 "语音体系结构更改" [https://go.microsoft.com/fwlink/p/?LinkId=266730](https://go.microsoft.com/fwlink/p/?linkid=266730) 。</span><span class="sxs-lookup"><span data-stu-id="e5f47-111">For more information about the architecture changes in Microsoft Exchange Server 2013, see “Voice Architecture Changes” in the Microsoft Exchange Server 2013 documentation at [https://go.microsoft.com/fwlink/p/?LinkId=266730](https://go.microsoft.com/fwlink/p/?linkid=266730).</span></span>

<span data-ttu-id="e5f47-112">为了使这些功能在本地 Exchange UM 部署中受支持，必须运行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="e5f47-112">For these features to be supported in an on-premises Exchange UM deployment, you must be running one of the following:</span></span>

  - <span data-ttu-id="e5f47-113">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 或最新 service pack</span><span class="sxs-lookup"><span data-stu-id="e5f47-113">Microsoft Exchange Server 2007 Service Pack 1 (SP1) or latest service pack</span></span>

  - <span data-ttu-id="e5f47-114">Microsoft Exchange Server 2010 或最新服务包</span><span class="sxs-lookup"><span data-stu-id="e5f47-114">Microsoft Exchange Server 2010 or latest service pack</span></span>

  - <span data-ttu-id="e5f47-115">Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5f47-115">Microsoft Exchange Server 2013</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e5f47-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="e5f47-116">In This Section</span></span>

  - [<span data-ttu-id="e5f47-117">集成统一消息和 Lync Server 2013 的功能</span><span class="sxs-lookup"><span data-stu-id="e5f47-117">Features of integrated Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-features-of-integrated-unified-messaging.md)

  - [<span data-ttu-id="e5f47-118">Lync Server 2013 中的本地统一消息的组件和拓扑</span><span class="sxs-lookup"><span data-stu-id="e5f47-118">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-on-premises-unified-messaging.md)

  - [<span data-ttu-id="e5f47-119">集成本地统一消息与 Lync Server 2013 的指南</span><span class="sxs-lookup"><span data-stu-id="e5f47-119">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

  - [<span data-ttu-id="e5f47-120">集成本地统一消息与 Lync Server 2013 的部署过程</span><span class="sxs-lookup"><span data-stu-id="e5f47-120">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="e5f47-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e5f47-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

