---
title: Lync Server 2013：为会议 Location-Based 路由
description: Lync Server 2013：为会议 Location-Based 路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing for conferencing
ms:assetid: e1acb1ba-0ed2-4abf-8a7b-1ca3049e95e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362849(v=OCS.15)
ms:contentKeyID: 56335087
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 979c835e03bbf87c9a9bf86b030cb9a8f4e138e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426541"
---
# <a name="location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="a45fe-103">Location-Based Lync Server 2013 中的会议路由</span><span class="sxs-lookup"><span data-stu-id="a45fe-103">Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a45fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a45fe-104">

<span> </span></span></span>

<span data-ttu-id="a45fe-105">_**主题上次修改时间：** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="a45fe-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="a45fe-106">Location-Based 路由使您能够根据呼叫中各方的位置限制 VoIP 终结点和 PSTN 终结点之间的通话路由。</span><span class="sxs-lookup"><span data-stu-id="a45fe-106">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="a45fe-107">使用 Lync Server 2013 的累积更新2，Location-Based 的路由规则可以在 Lync 会议上强制执行， (这种会议) 阻止 PSTN 免绕过。</span><span class="sxs-lookup"><span data-stu-id="a45fe-107">With Cumulative Update 2 of Lync Server 2013, Location-Based Routing rules can be enforced on Lync meetings (i.e. conferences) to prevent PSTN toll bypass.</span></span> <span data-ttu-id="a45fe-108">应用程序监视活动会议并根据参与的用户的位置强制执行 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="a45fe-108">The application monitors an active conference and enforces Location-Based Routing restrictions based on the location of users participating.</span></span> <span data-ttu-id="a45fe-109">Location-Based 路由会议应用程序还支持将 Location-Based 路由限制强制用于涉及 PSTN 终结点的咨询式转移。</span><span class="sxs-lookup"><span data-stu-id="a45fe-109">The Location-Based Routing Conferencing application additionally enables the enforcement of Location-Based Routing restrictions to consultative transfers involving PSTN endpoints.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a45fe-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="a45fe-110">In This Section</span></span>

  - [<span data-ttu-id="a45fe-111">Lync Server 2013 中的会议 Location-Based 路由概述</span><span class="sxs-lookup"><span data-stu-id="a45fe-111">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="a45fe-112">Lync Server 2013 中基于位置的路由和咨询式呼叫转移</span><span class="sxs-lookup"><span data-stu-id="a45fe-112">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-and-consultative-call-transfers.md)

  - [<span data-ttu-id="a45fe-113">Lync Server 2013 中的会议 Location-Based 路由要求</span><span class="sxs-lookup"><span data-stu-id="a45fe-113">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-requirements-for-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="a45fe-114">Lync Server 2013 中会议的基于位置的路由的配置</span><span class="sxs-lookup"><span data-stu-id="a45fe-114">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-configuration-of-location-based-routing-for-conferencing.md)

<span data-ttu-id="a45fe-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a45fe-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

