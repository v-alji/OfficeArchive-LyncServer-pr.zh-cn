---
title: Lync Server 2013：规划通话管理功能
description: Lync Server 2013：规划通话管理功能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for call management features
ms:assetid: 5f557345-5a04-45d6-b274-c02dbfe41b33
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398421(v=OCS.15)
ms:contentKeyID: 48184298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec990aad40baf33365e92e78ee8071216a2add1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391728"
---
# <a name="planning-for-call-management-features-in-lync-server-2013"></a><span data-ttu-id="19784-103">在 Lync Server 2013 中规划呼叫管理功能</span><span class="sxs-lookup"><span data-stu-id="19784-103">Planning for call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19784-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19784-104">

<span> </span></span></span>

<span data-ttu-id="19784-105">_**主题上次修改时间：** 2012-12-17_</span><span class="sxs-lookup"><span data-stu-id="19784-105">_**Topic Last Modified:** 2012-12-17_</span></span>

<span data-ttu-id="19784-106">企业语音呼叫管理功能控制如何传送和应答传入呼叫。</span><span class="sxs-lookup"><span data-stu-id="19784-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="19784-107">Lync Server 2013 提供下列呼叫管理功能：</span><span class="sxs-lookup"><span data-stu-id="19784-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="19784-108">**呼叫寄存**：允许语音用户暂时寄存呼叫，然后从同一电话或其他电话接听呼叫。</span><span class="sxs-lookup"><span data-stu-id="19784-108">**Call Park**:   Enables voice users to temporarily park a call and then pick it up from the same or another phone.</span></span>

  - <span data-ttu-id="19784-109">**组应答**：使语音用户能够应答为分配到呼叫应答组的其他语音用户响铃的呼叫。</span><span class="sxs-lookup"><span data-stu-id="19784-109">**Group Pickup**:   Enables voice users to pick up calls that are ringing for other voice users who are assigned to call pickup groups.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="19784-110">组装货是 Lync Server 2013 的累积更新的新增功能：2月2013。</span><span class="sxs-lookup"><span data-stu-id="19784-110">Group Pickup is new with Cumulative Updates for Lync Server 2013: February 2013.</span></span>

    
    </div>

  - <span data-ttu-id="19784-111">**响应组**：通过智能寻线或互动语音响应 (IVR) 问题和答案，将传入呼叫路由至代理组。</span><span class="sxs-lookup"><span data-stu-id="19784-111">**Response Group**:   Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="19784-112">**公告：**    对未分配号码的通话播放消息，或在别处路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="19784-112">**Announcement:**    Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="19784-113">如果计划部署企业语音，则可以选择实现任一或所有这些呼叫管理功能。</span><span class="sxs-lookup"><span data-stu-id="19784-113">If you plan to deploy Enterprise Voice, you can choose to implement any or all of these call management features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="19784-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="19784-114">In This Section</span></span>

  - [<span data-ttu-id="19784-115">在 Lync Server 2013 中规划呼叫寄存</span><span class="sxs-lookup"><span data-stu-id="19784-115">Planning for Call Park in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-park.md)

  - [<span data-ttu-id="19784-116">在 Lync Server 2013 中规划组呼叫装货</span><span class="sxs-lookup"><span data-stu-id="19784-116">Planning for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-planning-for-group-call-pickup.md)

  - [<span data-ttu-id="19784-117">在 Lync Server 2013 中规划响应组</span><span class="sxs-lookup"><span data-stu-id="19784-117">Planning for response groups in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-groups.md)

  - [<span data-ttu-id="19784-118">在 Lync Server 2013 中规划通知</span><span class="sxs-lookup"><span data-stu-id="19784-118">Planning for announcements in Lync Server 2013</span></span>](lync-server-2013-planning-for-announcements.md)

<span data-ttu-id="19784-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19784-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

