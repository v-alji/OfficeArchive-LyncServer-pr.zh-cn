---
title: Lync Server 2013：规划外部用户访问
description: Lync Server 2013：规划外部用户访问。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for external user access
ms:assetid: ea098933-eff5-461e-aba3-e7f128784dc2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399048(v=OCS.15)
ms:contentKeyID: 48185903
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8f1854791ed837b963d4c80f3467e4e89555592
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391732"
---
# <a name="planning-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="93b86-103">在 Lync Server 2013 中规划外部用户访问</span><span class="sxs-lookup"><span data-stu-id="93b86-103">Planning for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93b86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93b86-104">

<span> </span></span></span>

<span data-ttu-id="93b86-105">_**主题上次修改时间：** 2013-01-19_</span><span class="sxs-lookup"><span data-stu-id="93b86-105">_**Topic Last Modified:** 2013-01-19_</span></span>

<span data-ttu-id="93b86-106">大多数组织中的通信涉及不在内部网络内部的服务和用户。</span><span class="sxs-lookup"><span data-stu-id="93b86-106">Communications in most organizations involve services and users that are not inside your internal network.</span></span> <span data-ttu-id="93b86-107">这些服务和用户包括临时或永久离开的员工、客户或合作伙伴组织的员工、使用公共即时消息的用户、 (IM) 服务以及你邀请加入会议和演示文稿的潜在客户、合作伙伴和匿名用户。</span><span class="sxs-lookup"><span data-stu-id="93b86-107">These services and users include employees who are temporarily or permanently offsite, employees of customer or partner organizations, people who use public instant messaging (IM) services, and potential customers, partners and anonymous users whom you invite to meetings and presentations.</span></span> <span data-ttu-id="93b86-108">在本文档中，这些人统称为 *外部用户*。</span><span class="sxs-lookup"><span data-stu-id="93b86-108">In this documentation, these people are collectively referred to as *external users*.</span></span>

<span data-ttu-id="93b86-109">使用 Microsoft Lync Server 2013，你组织中的用户可以使用 IM 和状态与外部用户进行通信，并且他们可以使用您的非现场员工和其他类型的外部用户的音频/视频 (A/V) 会议和 web 会议。</span><span class="sxs-lookup"><span data-stu-id="93b86-109">With Microsoft Lync Server 2013, users in your organization can use IM and presence to communicate with external users, and they can participate in audio/video (A/V) conferencing and web conferencing with your offsite employees and other types of external users.</span></span> <span data-ttu-id="93b86-110">您还可以通过移动设备和企业语音支持外部访问。</span><span class="sxs-lookup"><span data-stu-id="93b86-110">You can also support external access from mobile devices and over Enterprise Voice.</span></span> <span data-ttu-id="93b86-111">不是组织成员的外部用户可以参与 Lync Server 2013 会议，从而允许匿名与会者参与。</span><span class="sxs-lookup"><span data-stu-id="93b86-111">External users who are not members of your organization can participate in Lync Server 2013 meetings, allowing anonymous attendees.</span></span>

<span data-ttu-id="93b86-112">若要支持整个组织的防火墙中的通信，请在外围网络中部署 Lync Server 2013 Edge 服务器 (也称为 DMZ、隔离区域和屏蔽子网) 。</span><span class="sxs-lookup"><span data-stu-id="93b86-112">To support communications across your organization’s firewall, you deploy Lync Server 2013 Edge Server in your perimeter network (also known as DMZ, demilitarized zone, and screened subnet).</span></span> <span data-ttu-id="93b86-113">边缘服务器控制防火墙外的用户可以如何连接到内部 Lync Server 2013 部署。</span><span class="sxs-lookup"><span data-stu-id="93b86-113">The Edge Server controls how users outside the firewall can connect to your internal Lync Server 2013 deployment.</span></span> <span data-ttu-id="93b86-114">它还控制与来源于防火墙的外部用户的通信。</span><span class="sxs-lookup"><span data-stu-id="93b86-114">It also controls communications with external users that originate within the firewall.</span></span>

<span data-ttu-id="93b86-115">可以在一个或多个位置部署一个或多个边缘服务器，具体取决于你的要求。</span><span class="sxs-lookup"><span data-stu-id="93b86-115">Depending on your requirements, you can deploy one or more Edge Servers in one or more locations.</span></span> <span data-ttu-id="93b86-116">本部分介绍 Lync Server 2013 中的外部用户访问方案，并介绍如何规划边缘和反向代理拓扑。</span><span class="sxs-lookup"><span data-stu-id="93b86-116">This section describes scenarios for external user access in Lync Server 2013, and it explains how to plan your edge and reverse proxy topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="93b86-117">虽然您需要一个 Edge 服务器来支持企业语音和外部用户访问，但本部分重点介绍 IM、状态、A/V 会议、联盟、web 会议和 Lync Mobile 的支持。</span><span class="sxs-lookup"><span data-stu-id="93b86-117">Although you need an Edge Server to support Enterprise Voice and external user access, this section focuses on support for IM, presence, A/V conferencing, federation, web conferencing, and Lync Mobile.</span></span> <span data-ttu-id="93b86-118">有关企业语音支持的详细信息，请参阅规划文档中的 <A href="lync-server-2013-planning-for-enterprise-voice.md">Lync Server 2013 中的 "规划企业语音</A> "。</span><span class="sxs-lookup"><span data-stu-id="93b86-118">For details about support for Enterprise Voice, see <A href="lync-server-2013-planning-for-enterprise-voice.md">Planning for Enterprise Voice in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="93b86-119">本节内容</span><span class="sxs-lookup"><span data-stu-id="93b86-119">In This Section</span></span>

  - [<span data-ttu-id="93b86-120">Lync Server 2013 中影响边缘服务器规划的更改</span><span class="sxs-lookup"><span data-stu-id="93b86-120">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)

  - [<span data-ttu-id="93b86-121">Lync Server 2013 的外部用户访问组件的系统要求</span><span class="sxs-lookup"><span data-stu-id="93b86-121">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)

  - [<span data-ttu-id="93b86-122">Lync Server 2013 中的外部用户访问概述</span><span class="sxs-lookup"><span data-stu-id="93b86-122">Overview of external user access in Lync Server 2013</span></span>](lync-server-2013-overview-of-external-user-access.md)

  - [<span data-ttu-id="93b86-123">了解 Lync Server 2013 中的自动发现</span><span class="sxs-lookup"><span data-stu-id="93b86-123">Understanding Autodiscover in Lync Server 2013</span></span>](lync-server-2013-understanding-autodiscover.md)

  - [<span data-ttu-id="93b86-124">在 Lync Server 2013 中选择拓扑</span><span class="sxs-lookup"><span data-stu-id="93b86-124">Choosing a topology in Lync Server 2013</span></span>](lync-server-2013-choosing-a-topology.md)

  - [<span data-ttu-id="93b86-125">Lync Server 2013 中的数据收集</span><span class="sxs-lookup"><span data-stu-id="93b86-125">Data collection in Lync Server 2013</span></span>](lync-server-2013-data-collection.md)

  - [<span data-ttu-id="93b86-126">确定 Lync Server 2013 的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="93b86-126">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)

  - [<span data-ttu-id="93b86-127">确定 Lync Server 2013 的外部 A/V 防火墙和端口要求</span><span class="sxs-lookup"><span data-stu-id="93b86-127">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)

  - [<span data-ttu-id="93b86-128">在 Lync Server 2013 中规划边缘服务器证书</span><span class="sxs-lookup"><span data-stu-id="93b86-128">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)

  - [<span data-ttu-id="93b86-129">Lync Server 2013 中的外部用户访问方案</span><span class="sxs-lookup"><span data-stu-id="93b86-129">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)

<span data-ttu-id="93b86-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93b86-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

