---
title: Lync Server 2013 规划
description: Lync Server 2013 计划。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning
ms:assetid: 6398cd91-8773-41bc-9b66-725d65ba9d66
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398447(v=OCS.15)
ms:contentKeyID: 48184302
ms.date: 12/10/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc4468300195760e7e994087875b5f49489828d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424399"
---
# <a name="planning-for-lync-server-2013"></a><span data-ttu-id="ab085-103">规划 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab085-103">Planning for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab085-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab085-104">

<span> </span></span></span>

<span data-ttu-id="ab085-105">_**主题上次修改时间：** 2014-12-09_</span><span class="sxs-lookup"><span data-stu-id="ab085-105">_**Topic Last Modified:** 2014-12-09_</span></span>

<span data-ttu-id="ab085-106">本部分中的主题介绍了如何为成功的 Lync 服务器部署进行规划。</span><span class="sxs-lookup"><span data-stu-id="ab085-106">The topics in this section describe how to plan for a successful Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ab085-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="ab085-107">In This Section</span></span>

  - [<span data-ttu-id="ab085-108">Lync Server 2013 的组织规划</span><span class="sxs-lookup"><span data-stu-id="ab085-108">Organization planning for Lync Server 2013</span></span>](lync-server-2013-planning-for-your-organization.md)

  - [<span data-ttu-id="ab085-109">确定 Lync Server 2013 的基础结构要求</span><span class="sxs-lookup"><span data-stu-id="ab085-109">Determining your infrastructure requirements for Lync Server 2013</span></span>](lync-server-2013-determining-your-infrastructure-requirements.md)

  - [<span data-ttu-id="ab085-110">Lync Server 2013 的网络规划</span><span class="sxs-lookup"><span data-stu-id="ab085-110">Network planning for Lync Server 2013</span></span>](lync-server-2013-network-planning.md)

  - [<span data-ttu-id="ab085-111">Lync Server 2013 的容量规划</span><span class="sxs-lookup"><span data-stu-id="ab085-111">Capacity planning for Lync Server 2013</span></span>](lync-server-2013-capacity-planning.md)

  - [<span data-ttu-id="ab085-112">在 Lync Server 2013 中规划高可用性和灾难恢复</span><span class="sxs-lookup"><span data-stu-id="ab085-112">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="ab085-113">在 Lync Server 2013 中规划可管理性和虚拟化</span><span class="sxs-lookup"><span data-stu-id="ab085-113">Planning for manageability and virtualization in Lync Server 2013</span></span>](lync-server-2013-planning-for-manageability-and-virtualization.md)

  - [<span data-ttu-id="ab085-114">在 Lync Server 2013 中规划前端服务器、即时消息和状态</span><span class="sxs-lookup"><span data-stu-id="ab085-114">Planning for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md)

  - [<span data-ttu-id="ab085-115">在 Lync Server 2013 中规划会议</span><span class="sxs-lookup"><span data-stu-id="ab085-115">Planning for conferencing in Lync Server 2013</span></span>](lync-server-2013-planning-for-conferencing.md)

  - [<span data-ttu-id="ab085-116">在 Lync Server 2013 中规划外部用户访问</span><span class="sxs-lookup"><span data-stu-id="ab085-116">Planning for external user access in Lync Server 2013</span></span>](lync-server-2013-planning-for-external-user-access.md)

  - [<span data-ttu-id="ab085-117">在 Lync Server 2013 中规划企业语音</span><span class="sxs-lookup"><span data-stu-id="ab085-117">Planning for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice.md)

  - [<span data-ttu-id="ab085-118">在 Lync Server 2013 中规划监控</span><span class="sxs-lookup"><span data-stu-id="ab085-118">Planning for monitoring in Lync Server 2013</span></span>](lync-server-2013-planning-for-monitoring.md)

  - [<span data-ttu-id="ab085-119">在 Lync Server 2013 中规划存档</span><span class="sxs-lookup"><span data-stu-id="ab085-119">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)

  - [<span data-ttu-id="ab085-120">在 Lync Server 2013 中规划持久聊天服务器</span><span class="sxs-lookup"><span data-stu-id="ab085-120">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)

  - [<span data-ttu-id="ab085-121">规划 Exchange Server 与 Lync Server 2013 的集成</span><span class="sxs-lookup"><span data-stu-id="ab085-121">Planning for Exchange Server integration with Lync Server 2013</span></span>](lync-server-2013-planning-for-exchange-server-integration.md)

  - [<span data-ttu-id="ab085-122">在 Lync Server 2013 中规划客户端和设备</span><span class="sxs-lookup"><span data-stu-id="ab085-122">Planning for clients and devices in Lync Server 2013</span></span>](lync-server-2013-planning-for-clients-and-devices.md)

  - [<span data-ttu-id="ab085-123">在 Lync Server 2013 中规划远程呼叫控制</span><span class="sxs-lookup"><span data-stu-id="ab085-123">Planning for remote call control in Lync Server 2013</span></span>](lync-server-2013-planning-for-remote-call-control.md)

  - [<span data-ttu-id="ab085-124">在 Lync Server 2013 中规划移动功能</span><span class="sxs-lookup"><span data-stu-id="ab085-124">Planning for mobility in Lync Server 2013</span></span>](lync-server-2013-planning-for-mobility.md)

  - [<span data-ttu-id="ab085-125">规划 Lync Server 2013 的安全性</span><span class="sxs-lookup"><span data-stu-id="ab085-125">Planning for security in Lync Server 2013</span></span>](lync-server-2013-planning-for-security.md)

<span data-ttu-id="ab085-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab085-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

