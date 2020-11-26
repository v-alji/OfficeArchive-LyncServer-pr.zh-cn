---
title: Lync Server 2013：规划安全性
description: Lync Server 2013：规划安全。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for security
ms:assetid: 17eeba87-cafa-4e9b-852d-c017a7d10d59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn342827(v=OCS.15)
ms:contentKeyID: 56107267
ms.date: 06/22/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1abc02aa3f42a6b12c66c621b071e0b3ddb545c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424441"
---
# <a name="planning-for-security-in-lync-server-2013"></a><span data-ttu-id="b5ac7-103">规划 Lync Server 2013 的安全性</span><span class="sxs-lookup"><span data-stu-id="b5ac7-103">Planning for security in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b5ac7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b5ac7-104">

<span> </span></span></span>

<span data-ttu-id="b5ac7-105">_**主题上次修改时间：** 2016-06-22_</span><span class="sxs-lookup"><span data-stu-id="b5ac7-105">_**Topic Last Modified:** 2016-06-22_</span></span>

<span data-ttu-id="b5ac7-106">使用此安全部分评估和管理 Lync Server 2013 部署的安全风险。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-106">Use this security section to assess and manage security risks to your deployment of Lync Server 2013.</span></span>

<span data-ttu-id="b5ac7-107">即使您的 Lync Server 2013 部署适中，您的网络中也可能有自己的安全文档的组件。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-107">Even if your Lync Server 2013 deployment is modest, you probably have components in your network that have their own security documentation.</span></span> <span data-ttu-id="b5ac7-108">因此，此部分不太可能涵盖与你的部署相关的所有组件和区域的安全的所有方面。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-108">Therefore, it is unlikely that this section covers all aspects of security for all components and areas that are pertinent to your deployment.</span></span>

<span data-ttu-id="b5ac7-109">将此部分用作解决 Lync Server 2013 部署安全的起始点。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-109">Use this section as a starting point to address the security of your Lync Server 2013 deployment.</span></span> <span data-ttu-id="b5ac7-110">它提供了用于评估和管理最常见的安全风险的一般指南和最佳做法。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-110">It provides general guidelines and best practices for assessing and managing the most common security risks.</span></span> <span data-ttu-id="b5ac7-111">在每个主题的结尾列出了其他产品和安全资源。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-111">Additional product and security resources are listed at the end of each topic.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b5ac7-112">安全性是一个不断发展的主题。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-112">Security is a constantly evolving topic.</span></span> <span data-ttu-id="b5ac7-113">随着新威胁和解决方案的出现，已过时的文档、解决方案、方法和过程应更换为最新的资料。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-113">As new threats and solutions arise, outdated documents, solutions, methods, and procedures should be replaced with up-to-date material.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b5ac7-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="b5ac7-114">In This Section</span></span>

  - [<span data-ttu-id="b5ac7-115">Lync Server 2013 中的关键安全功能</span><span class="sxs-lookup"><span data-stu-id="b5ac7-115">Key security features in Lync Server 2013</span></span>](lync-server-2013-key-security-features.md)

  - [<span data-ttu-id="b5ac7-116">现代日计算中的常见安全威胁</span><span class="sxs-lookup"><span data-stu-id="b5ac7-116">Common security threats in modern day computing</span></span>](lync-server-2013-common-security-threats-in-modern-day-computing.md)

  - [<span data-ttu-id="b5ac7-117">Lync Server 2013 的病毒扫描排除</span><span class="sxs-lookup"><span data-stu-id="b5ac7-117">Antivirus scanning exclusions for Lync Server 2013</span></span>](lync-server-2013-antivirus-scanning-exclusions.md)

  - [<span data-ttu-id="b5ac7-118">Lync Server 2013 的安全框架</span><span class="sxs-lookup"><span data-stu-id="b5ac7-118">Security framework for Lync Server 2013</span></span>](lync-server-2013-security-framework-for-lync-server.md)

  - [<span data-ttu-id="b5ac7-119">解决 Lync Server 2013 的核心基础结构威胁</span><span class="sxs-lookup"><span data-stu-id="b5ac7-119">Addressing threats to your core infrastructure for Lync Server 2013</span></span>](lync-server-2013-addressing-threats-to-your-core-infrastructure.md)

  - [<span data-ttu-id="b5ac7-120">在 Lync Server 2013 中部署一个 SQL Server 非标准端口和别名。</span><span class="sxs-lookup"><span data-stu-id="b5ac7-120">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>](deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013.md)

<span data-ttu-id="b5ac7-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b5ac7-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

