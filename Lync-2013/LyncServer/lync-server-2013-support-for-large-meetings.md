---
title: Lync Server 2013 大型会议支持
description: Lync Server 2013 支持大型会议。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for large meetings
ms:assetid: 8f0446d5-1ed9-4ea0-bb97-6c062a98a1eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205090(v=OCS.15)
ms:contentKeyID: 48184820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb37cbfb95e36b9a07604eb4fbbc548e4d7ce9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423664"
---
# <a name="support-for-large-meetings-in-lync-server-2013"></a><span data-ttu-id="3ec82-103">Lync Server 2013 中的大型会议支持</span><span class="sxs-lookup"><span data-stu-id="3ec82-103">Support for large meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3ec82-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3ec82-104">

<span> </span></span></span>

<span data-ttu-id="3ec82-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="3ec82-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="3ec82-106">Lync Server 2013 可通过音频/视频 (A/V) 会议（包括共享 PowerPoint 演示文稿）支持最多1000个参与者的会议。</span><span class="sxs-lookup"><span data-stu-id="3ec82-106">Lync Server 2013 can support meetings with up to 1000 participants using audio/video (A/V) conferencing, including sharing PowerPoint presentations.</span></span> <span data-ttu-id="3ec82-107">若要实现此支持，需要配置专用池来支持大型会议，并且需要以某种方式管理该池以确保一次仅主持一个大型会议。</span><span class="sxs-lookup"><span data-stu-id="3ec82-107">This support requires a dedicated pool configured to support large meetings and managed in a way that ensures hosting of only a single large meeting at a time.</span></span>

<span data-ttu-id="3ec82-108">本部分介绍如何使用专用 Lync Server 2013 池支持大型会议。</span><span class="sxs-lookup"><span data-stu-id="3ec82-108">This section describes how to support large meetings using a dedicated Lync Server 2013 pool.</span></span> <span data-ttu-id="3ec82-109">它介绍了可伸缩性注意事项和针对专用池的实现要求，包括拓扑、硬件、软件和配置要求。</span><span class="sxs-lookup"><span data-stu-id="3ec82-109">It describes scalability considerations and the implementation requirements for a dedicated pool, including topology, hardware, software, and configuration requirements.</span></span> <span data-ttu-id="3ec82-110">它还提供了一组最佳做法建议，用于支持大型会议、由 Lync Server 工程团队执行的服务器可伸缩性测试的测试方法和结果的摘要以及有关大型会议支持的常见问题的答案。</span><span class="sxs-lookup"><span data-stu-id="3ec82-110">It also provides a set of best practice recommendations for supporting large meetings, a summary of the test methods and results of server scalability testing conducted by the Lync Server engineering team, and the answers to frequently asked questions about support for large meetings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3ec82-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="3ec82-111">In This Section</span></span>

  - [<span data-ttu-id="3ec82-112">Lync Server 2013 中的会议可伸缩性概述</span><span class="sxs-lookup"><span data-stu-id="3ec82-112">Overview of conferencing scalability in Lync Server 2013</span></span>](lync-server-2013-conferencing-scalability-overview.md)

  - [<span data-ttu-id="3ec82-113">使用 Lync Server 2013 支持大型会议</span><span class="sxs-lookup"><span data-stu-id="3ec82-113">Supporting large meetings using Lync Server 2013</span></span>](lync-server-2013-supporting-large-meetings.md)

  - [<span data-ttu-id="3ec82-114">适用于 Lync Server 2013 的大型会议支持常见问题</span><span class="sxs-lookup"><span data-stu-id="3ec82-114">Large meeting support FAQ for Lync Server 2013</span></span>](lync-server-2013-large-meeting-support-faq.md)

<span data-ttu-id="3ec82-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3ec82-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

