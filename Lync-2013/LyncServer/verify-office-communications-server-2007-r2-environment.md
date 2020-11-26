---
title: 验证 Office Communications Server 2007 R2 环境
description: 验证 Office 通信服务器 2007 R2 环境。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify Office Communications Server 2007 R2 environment
ms:assetid: e051bdd5-e7ef-4754-8705-900b2c57f37c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721906(v=OCS.15)
ms:contentKeyID: 49733840
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eb200941b3a35ece2b587bcfc89be743c9960d1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443630"
---
# <a name="verify-office-communications-server-2007-r2-environment"></a><span data-ttu-id="92ca4-103">验证 Office Communications Server 2007 R2 环境</span><span class="sxs-lookup"><span data-stu-id="92ca4-103">Verify Office Communications Server 2007 R2 environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="92ca4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="92ca4-104">

<span> </span></span></span>

<span data-ttu-id="92ca4-105">_**主题上次修改时间：** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="92ca4-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="92ca4-106">在使用 Office 通信服务器 2007 R2 在共存状态中部署 Lync Server 2013 之前，需要验证 Office 通信服务器是否已配置和启动 2007 R2 服务。</span><span class="sxs-lookup"><span data-stu-id="92ca4-106">Prior to deploying Lync Server 2013 in a coexistence state with Office Communications Server 2007 R2, you need to verify the Office Communications Server 2007 R2 services are configured and started.</span></span>

<span data-ttu-id="92ca4-107">**验证池是否已使用 Office 通信服务器 2007 R2 管理工具启动**</span><span class="sxs-lookup"><span data-stu-id="92ca4-107">**Verify the Pool is started using the Office Communications Server 2007 R2 Administrative Tool**</span></span>

1.  <span data-ttu-id="92ca4-108">打开 Office 通信服务器 2007 R2 管理工具。</span><span class="sxs-lookup"><span data-stu-id="92ca4-108">Open the Office Communications Server 2007 R2 administrative tool.</span></span>

2.  <span data-ttu-id="92ca4-109">展开 " **林** " 节点，展开 " **标准版服务器** " 或 " **企业版池** " 节点，然后展开 "池" 或 "服务器名称"。</span><span class="sxs-lookup"><span data-stu-id="92ca4-109">Expand the **Forest** node, expand the **Standard Edition Servers** or **Enterprise pools** node, and then expand the pool or server name.</span></span>

3.  <span data-ttu-id="92ca4-110">确保服务在标准版服务器或企业版池上运行。</span><span class="sxs-lookup"><span data-stu-id="92ca4-110">Ensure that the services are running on the Standard Edition server or Enterprise pool.</span></span>
    
    <span data-ttu-id="92ca4-111">![Office 通信服务器 2007 R2 管理控制台](images/JJ721906.76897b6d-f433-47d2-930d-0816fc30a3c2(OCS.15).jpg "Office 通信服务器 2007 R2 管理控制台")</span><span class="sxs-lookup"><span data-stu-id="92ca4-111">![Office Communications Server 2007 R2 Admin Console](images/JJ721906.76897b6d-f433-47d2-930d-0816fc30a3c2(OCS.15).jpg "Office Communications Server 2007 R2 Admin Console")</span></span>

<span data-ttu-id="92ca4-112">**查看针对 Office 通信服务器 2007 R2 配置的用户**</span><span class="sxs-lookup"><span data-stu-id="92ca4-112">**Review Users configured for Office Communications Server 2007 R2**</span></span>

1.  <span data-ttu-id="92ca4-113">打开 Office 通信服务器 2007 R2 管理工具。</span><span class="sxs-lookup"><span data-stu-id="92ca4-113">Open the Office Communications Server 2007 R2 administrative tool.</span></span>

2.  <span data-ttu-id="92ca4-114">展开 " **林** " 节点，展开 " **标准版服务器** " 或 " **企业版池** " 节点，然后展开 "池" 或 "服务器名称"。</span><span class="sxs-lookup"><span data-stu-id="92ca4-114">Expand the **Forest** node, expand the **Standard Edition Servers** or **Enterprise pools** node, and then expand the pool or server name.</span></span>

3.  <span data-ttu-id="92ca4-115">单击 " **用户**"。</span><span class="sxs-lookup"><span data-stu-id="92ca4-115">Click **Users**.</span></span>

4.  <span data-ttu-id="92ca4-116">验证 Office 通信服务器 2007 R2 用户的列表。</span><span class="sxs-lookup"><span data-stu-id="92ca4-116">Verify the list of Office Communications Server 2007 R2 users.</span></span>
    
    <span data-ttu-id="92ca4-117">![OCS 管理工具中的用户列表](images/JJ721906.f6bb7c4f-cbed-4389-8d0a-69a28577f17a(OCS.15).jpg "OCS 管理工具中的用户列表")</span><span class="sxs-lookup"><span data-stu-id="92ca4-117">![List fo users in OCS Admin tool](images/JJ721906.f6bb7c4f-cbed-4389-8d0a-69a28577f17a(OCS.15).jpg "List fo users in OCS Admin tool")</span></span>

<span data-ttu-id="92ca4-118">**验证旧版 XMPP 联盟合作伙伴配置**</span><span class="sxs-lookup"><span data-stu-id="92ca4-118">**Verify legacy XMPP Federated Partner Configuration**</span></span>

1.  <span data-ttu-id="92ca4-119">从旧的 XMPP 服务器中，导航到 "管理工具 \\ 服务" 小程序。</span><span class="sxs-lookup"><span data-stu-id="92ca4-119">From the legacy XMPP server, navigate to the Administrative Tools\\Services applet.</span></span>

2.  <span data-ttu-id="92ca4-120">验证是否已启动 Office 通信服务器 XMPP 网关服务。</span><span class="sxs-lookup"><span data-stu-id="92ca4-120">Verify that the Office Communications Server XMPP Gateway service is started.</span></span>
    
    <span data-ttu-id="92ca4-121">![Office 通信服务器 XMPP 网关服务](images/JJ721906.23223724-3c4b-4cb9-ace2-1cab2c3c91c3(OCS.15).jpg "Office 通信服务器 XMPP 网关服务")</span><span class="sxs-lookup"><span data-stu-id="92ca4-121">![Office Communications Server XMPP Gateway Service](images/JJ721906.23223724-3c4b-4cb9-ace2-1cab2c3c91c3(OCS.15).jpg "Office Communications Server XMPP Gateway Service")</span></span>

<span data-ttu-id="92ca4-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="92ca4-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

