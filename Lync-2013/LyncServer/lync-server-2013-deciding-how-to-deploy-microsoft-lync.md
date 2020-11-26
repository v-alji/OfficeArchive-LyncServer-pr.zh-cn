---
title: Lync Server 2013：确定如何部署 Microsoft Lync
description: Lync Server 2013：确定如何部署 Microsoft Lync。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431230"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a><span data-ttu-id="e4f98-103">确定如何部署 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4f98-103">Deciding how to deploy Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4f98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4f98-104">

<span> </span></span></span>

<span data-ttu-id="e4f98-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="e4f98-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="e4f98-106">规划 Lync 时，第一个主要决策是如何部署 Microsoft Lync：在本地 Lync Server 2013 或在云中通过 Microsoft 365 或 Office 365 进行 Lync Online。</span><span class="sxs-lookup"><span data-stu-id="e4f98-106">When planning for Lync, the first major decision is how to deploy Microsoft Lync: as Lync Server 2013 on premises, or Lync Online with Microsoft 365 or Office 365 in the cloud.</span></span>

  - <span data-ttu-id="e4f98-107">**Lync Server 2013 本地** 版：此选项提供了完整的 Lync 功能集，并提供了配置、自定义和操作部署的绝佳灵活性。</span><span class="sxs-lookup"><span data-stu-id="e4f98-107">**Lync Server 2013 on-premises** : This choice provides the complete Lync feature set and provides ultimate flexibility in configuring, customizing, and operating your deployment.</span></span> <span data-ttu-id="e4f98-108">所有服务器都安装在现场并由你的组织维护。</span><span class="sxs-lookup"><span data-stu-id="e4f98-108">All servers are installed onsite and maintained by your organization.</span></span> <span data-ttu-id="e4f98-109">本地部署提供了各种 Lync Server 功能。</span><span class="sxs-lookup"><span data-stu-id="e4f98-109">An on-premises deployment provides the full range of Lync Server features.</span></span>

  - <span data-ttu-id="e4f98-110">**云中的 Lync Online** Lync Online 适用于希望基于云的即时消息、状态和会议的成本和灵活性优势的组织，而不牺牲 Lync 服务器的企业级功能。</span><span class="sxs-lookup"><span data-stu-id="e4f98-110">**Lync Online in the cloud** Lync Online is designed for organizations that want the cost and agility benefits of cloud-based instant messaging, presence, and meetings without sacrificing the business-class capabilities of Lync Server.</span></span> <span data-ttu-id="e4f98-111">通过 Lync Online，Microsoft 部署和维护所需的服务器基础结构，并处理持续维护、修补和升级。</span><span class="sxs-lookup"><span data-stu-id="e4f98-111">With Lync Online, Microsoft deploys and maintains the required server infrastructure, and handles ongoing maintenance, patches, and upgrades.</span></span> <span data-ttu-id="e4f98-112">本地部署中提供的某些功能在 Lync Online 中不可用。</span><span class="sxs-lookup"><span data-stu-id="e4f98-112">Some features available in an on-premises deployment are not available in Lync Online.</span></span>

<span data-ttu-id="e4f98-113">哪种类型的部署最适合你取决于要部署的工作负荷以及你的组织的地理和业务状态。</span><span class="sxs-lookup"><span data-stu-id="e4f98-113">Which type of deployment would be best for you depends on the workloads you want to deploy, and your organization’s geographical and business status.</span></span>

<div>

## <a name="lync-server"></a><span data-ttu-id="e4f98-114">Lync Server</span><span class="sxs-lookup"><span data-stu-id="e4f98-114">Lync Server</span></span>

<span data-ttu-id="e4f98-115">本地 Lync 服务器部署最适用于以下情况：</span><span class="sxs-lookup"><span data-stu-id="e4f98-115">An on-premises Lync Server deployment is best for the following scenarios:</span></span>

  - <span data-ttu-id="e4f98-116">**完整的企业语音功能**   如果你计划部署完整的企业语音解决方案以替换 PBX 或使用高级呼叫功能，则需要本地 Lync 服务器部署。</span><span class="sxs-lookup"><span data-stu-id="e4f98-116">**Full Enterprise Voice Capabilities**   If you plan to deploy a full Enterprise Voice solution to replace your PBX or which uses advanced calling features, an on-premises Lync Server deployment is required.</span></span> <span data-ttu-id="e4f98-117">本地支持与 PBX 系统和中继的直接连接，以及高级电话功能（如响应组和呼叫寄存）。</span><span class="sxs-lookup"><span data-stu-id="e4f98-117">On-premises supports direct connectivity with PBX systems and trunks, and advanced phone features such as response groups and call park.</span></span> <span data-ttu-id="e4f98-118">Lync Online 目前不支持这些功能。</span><span class="sxs-lookup"><span data-stu-id="e4f98-118">Lync Online does not currently support these features.</span></span>

  - <span data-ttu-id="e4f98-119">**媒体质量控件**   如果你需要各种媒体质量保证功能（如呼叫许可控制 (CAC) 和服务质量 (QoS) 功能），你将需要内部部署。</span><span class="sxs-lookup"><span data-stu-id="e4f98-119">**Media Quality Controls**   If you want the full range of media quality assurance features, such as Call Admission Control (CAC) and Quality of Service (QoS) features, you will want an on-premises deployment .</span></span>

  - <span data-ttu-id="e4f98-120">**持久聊天**   如果你需要为你的组织部署持久聊天，你必须选择本地部署。</span><span class="sxs-lookup"><span data-stu-id="e4f98-120">**Persistent Chat**   If you need to deploy Persistent chat for your organization, you must choose an on-premises deployment.</span></span>

  - <span data-ttu-id="e4f98-121">**第三方服务器应用程序**   只有本地部署才能与使用 Microsoft 统一通信托管 API (UCMA) 的受信任的第三方应用程序配合使用。</span><span class="sxs-lookup"><span data-stu-id="e4f98-121">**3rd-Party Server Applications**   Only on-premises deployments can work with trusted 3rd-party applications that use the Microsoft Unified Communications Managed API (UCMA).</span></span>

  - <span data-ttu-id="e4f98-122">**需要地区支持的多国/多地区公司**   如果您有多个国家或地区的数据中心，并且需要在区域基础上部署和管理服务器，则最好使用内部部署，因为它提供了这种类型的区域管理功能。</span><span class="sxs-lookup"><span data-stu-id="e4f98-122">**Multi-National/Multi-Regional Companies Needing Regional Support**   If you have datacenters in multiple countries or regions and need servers to be deployed and managed on a regional basis, an on-premises deployment is best, as it provides this type of regional management capabilities.</span></span>

  - <span data-ttu-id="e4f98-123">**完全控制策略、报告和升级**   使用本地 Lync 服务器部署，你可以访问完整的服务器和客户端策略集、监视和其他报告以及升级计时。</span><span class="sxs-lookup"><span data-stu-id="e4f98-123">**Complete control over policies, reports, and upgrades**   With an on premises Lync Server deployment, you have access to the full set of server and client policies, Monitoring and other reports, and timing of upgrades.</span></span> <span data-ttu-id="e4f98-124">Lync Online 提供了策略设置和报告的子集，并提供了一个限制的有效窗口，可用于接受升级。</span><span class="sxs-lookup"><span data-stu-id="e4f98-124">Lync Online provides a subset of policy setting and reports, and provides a limited, though significant, window for accepting upgrades.</span></span>

</div>

<div>

## <a name="lync-online"></a><span data-ttu-id="e4f98-125">Lync Online</span><span class="sxs-lookup"><span data-stu-id="e4f98-125">Lync Online</span></span>

<span data-ttu-id="e4f98-126">如果上述列表中的任何因素对您来说都不重要，则您可能希望选择 Lync Online，以获得更简单的部署和可管理性。</span><span class="sxs-lookup"><span data-stu-id="e4f98-126">If none of the factors in the preceding list are critical for you, you may want to choose Lync Online, for simpler deployment and manageability.</span></span> <span data-ttu-id="e4f98-127">Lync Online 提供了一种强大的 IM、状态和会议功能集，还支持在您的组织中的用户之间通过 IP 进行语音和视频通话。</span><span class="sxs-lookup"><span data-stu-id="e4f98-127">Lync Online provides a robust IM, presence and conferencing feature set, and also enables voice and video calls over IP between users in your organization.</span></span>

<span data-ttu-id="e4f98-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4f98-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
