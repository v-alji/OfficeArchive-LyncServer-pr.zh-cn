---
title: Lync Server 2013：持久聊天服务器概述
description: Lync Server 2013：持久聊天服务器概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Persistent Chat Server
ms:assetid: 23f7c886-304d-495a-ae70-3cbb44241acd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425717(v=OCS.15)
ms:contentKeyID: 48183622
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bbcb396522611aca52bd2093f2fd49f376341356
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424756"
---
# <a name="overview-of-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="909a8-103">Lync Server 2013 中的持久聊天服务器概述</span><span class="sxs-lookup"><span data-stu-id="909a8-103">Overview of Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="909a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="909a8-104">

<span> </span></span></span>

<span data-ttu-id="909a8-105">_**主题上次修改时间：** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="909a8-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="909a8-106">Lync Server 2013，持久聊天服务器使用户能够参与在一段时间内保持的基于主题的多个对话。</span><span class="sxs-lookup"><span data-stu-id="909a8-106">Lync Server 2013, Persistent Chat Server enables users to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="909a8-107">持久聊天服务器可帮助您的组织执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="909a8-107">Persistent Chat Server can help your organization do the following:</span></span>

  - <span data-ttu-id="909a8-108">改进地理分散的团队和跨职能团队之间的通信。</span><span class="sxs-lookup"><span data-stu-id="909a8-108">Improve communication between geographically dispersed and cross-functional teams.</span></span> <span data-ttu-id="909a8-109">通过使用持久聊天，团队可以高效地与其他人共享信息、想法和决策。</span><span class="sxs-lookup"><span data-stu-id="909a8-109">By using Persistent Chat, teams can efficiently share information, ideas, and decisions with one another.</span></span> <span data-ttu-id="909a8-110">已发布到聊天室 (讨论论坛) 可以保留 (也就是说，可在一) 段时间内随时可用，以便来自不同地点和部门的人员可以参与，即使他们不在线。</span><span class="sxs-lookup"><span data-stu-id="909a8-110">The messages posted to chat rooms (discussion forums) can persist (that is, can be available over time), so that people from different locations and departments can participate, even when they are not simultaneously online.</span></span> <span data-ttu-id="909a8-111">当用户连接到聊天室时，backchat (会自动在聊天室中加载) 的可配置的聊天历史记录消息，以便为用户提供对话的上下文。</span><span class="sxs-lookup"><span data-stu-id="909a8-111">When a user connects to a chat room, backchat (a configurable number of chat-history messages) is automatically loaded in the chat room to give the user a context for the conversation.</span></span>

  - <span data-ttu-id="909a8-112">改善信息意识。</span><span class="sxs-lookup"><span data-stu-id="909a8-112">Improve information awareness.</span></span> <span data-ttu-id="909a8-113">通过使用客户端筛选器，用户可以定义条件（如邮件内容中的关键字或邮件中 "发件人" 字段的值），以便在永久聊天即时消息或聊天室消息中满足这些条件时接收通知。</span><span class="sxs-lookup"><span data-stu-id="909a8-113">By using client-side filters, users can define conditions—such as keywords in message content, or the value of the "from" field in a message—to receive notification when those conditions are met in Persistent Chat instant messages or chat room messages.</span></span> <span data-ttu-id="909a8-114">通过这种方式，用户可以随时了解最新兴趣的内容。</span><span class="sxs-lookup"><span data-stu-id="909a8-114">This way, users can stay up-to-date with the content that interests them most.</span></span>

  - <span data-ttu-id="909a8-115">通过其扩展的组织改善沟通。</span><span class="sxs-lookup"><span data-stu-id="909a8-115">Improve communication with their extended organization.</span></span> <span data-ttu-id="909a8-116">通过方便地与组织中的其他人协作处理较长时间的主题，并提供共享信息的持久位置，持久的聊天有助于改善通信。</span><span class="sxs-lookup"><span data-stu-id="909a8-116">By making it easy to collaborate over long-running topics with others in the organization, and by providing a persistent place to share information, Persistent Chat helps improve communication.</span></span>

  - <span data-ttu-id="909a8-117">减少信息超载。</span><span class="sxs-lookup"><span data-stu-id="909a8-117">Reduce information overload.</span></span> <span data-ttu-id="909a8-118">用户可以通过使用客户端筛选器关注聊天室和最感兴趣的消息，并可在其联系人列表中添加要关注的聊天室。</span><span class="sxs-lookup"><span data-stu-id="909a8-118">Users can follow chat rooms and messages of most interest by using client-side filters, and can add chat rooms they want to follow to their contact list.</span></span>

  - <span data-ttu-id="909a8-119">增加重要知识和信息的散布。</span><span class="sxs-lookup"><span data-stu-id="909a8-119">Increase dispersion of important knowledge and information.</span></span> <span data-ttu-id="909a8-120">文档和链接可以包含在对话中，供所有团队访问。</span><span class="sxs-lookup"><span data-stu-id="909a8-120">Documents and links can be included within conversations for access by all the team.</span></span> <span data-ttu-id="909a8-121">通过将问题发布到更广泛的团队，用户可以受益于主题专家的答复。</span><span class="sxs-lookup"><span data-stu-id="909a8-121">By posting questions to a broader team, users can benefit from responses by subject matter experts.</span></span> <span data-ttu-id="909a8-122">与其他信息系统的集成使重要的组织数据能够轻松地传达给大型组。</span><span class="sxs-lookup"><span data-stu-id="909a8-122">Integration with other information systems enables important organizational data to be easily communicated to large groups.</span></span>

<span data-ttu-id="909a8-123">要在 Lync Server 2013 中启用聊天室，请部署 Lync Server 2013 持久聊天。</span><span class="sxs-lookup"><span data-stu-id="909a8-123">To enable chat rooms in Lync Server 2013, deploy Lync Server 2013 Persistent Chat.</span></span> <span data-ttu-id="909a8-124">有关启用聊天室的信息，请参阅持续聊天帮助 <https://go.microsoft.com/fwlink/p/?linkid=270945> 。</span><span class="sxs-lookup"><span data-stu-id="909a8-124">For information about enabling chat rooms, see the Persistent Chat Help at <https://go.microsoft.com/fwlink/p/?linkid=270945>.</span></span> <span data-ttu-id="909a8-125">如果为 Lync Server 启用了用户，并且已部署 Lync Server 支持，则用户可以安装和使用 Lync 2013 持久聊天来提供聊天室支持。</span><span class="sxs-lookup"><span data-stu-id="909a8-125">If users are enabled for Lync Server, and Lync Server support is deployed, users can install and use Lync 2013 Persistent Chat to provide chat room support.</span></span>

<span data-ttu-id="909a8-126">如果您的组织需要遵守合规性规定，您可以选择部署持久的聊天合规性服务。</span><span class="sxs-lookup"><span data-stu-id="909a8-126">If your organization is required to follow compliance regulations, you can optionally deploy Persistent Chat Compliance service.</span></span>

<span data-ttu-id="909a8-127"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="909a8-127"></div>

<span> </span>

</div>

</div>

</span></span></div>

