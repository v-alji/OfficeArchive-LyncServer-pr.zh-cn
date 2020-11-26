---
title: Lync Server 2013：管理类别、聊天室和加载项
description: Lync Server 2013：管理类别、会议室和外接程序。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing categories, rooms, and add-ins
ms:assetid: a9807031-7369-4a51-9369-6f09bec24141
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412799(v=OCS.15)
ms:contentKeyID: 48185100
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba09ed3e021ba24f424d28bbb2c5c379ab975741
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425953"
---
# <a name="managing-categories-rooms-and-add-ins-in-lync-server-2013"></a><span data-ttu-id="c6798-103">在 Lync Server 2013 中管理类别、聊天室和加载项</span><span class="sxs-lookup"><span data-stu-id="c6798-103">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c6798-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c6798-104">

<span> </span></span></span>

<span data-ttu-id="c6798-105">_**主题上次修改时间：** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="c6798-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="c6798-106">在 Lync Server 2013 控制面板中，或通过使用 Windows PowerShell cmdlet，持久聊天管理员可以使用 **持久聊天** 页面创建类别和加载项。对于管理持久聊天室，管理员可以使用 Windows PowerShell cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6798-106">In Lync Server 2013 Control Panel, or by using Windows PowerShell cmdlets, Persistent Chat Administrators can use the **Persistent Chat** page to create categories and add-ins. For managing Persistent Chat rooms, Administrators can use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="c6798-107">或者，如果持久聊天管理员也是 SIP 启用的，则他们可以使用 Lync 客户端启动网页来创建和管理聊天室。</span><span class="sxs-lookup"><span data-stu-id="c6798-107">Alternatively, if the Persistent Chat administrator is also SIP-enabled, they can use the Lync client to launch a web page to create and manage chat rooms.</span></span>

<span data-ttu-id="c6798-108">以下主题介绍如何创建和使用类别和聊天室。</span><span class="sxs-lookup"><span data-stu-id="c6798-108">The following topics describe how to create and work with categories and chat rooms.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c6798-109">本节内容</span><span class="sxs-lookup"><span data-stu-id="c6798-109">In This Section</span></span>

  - [<span data-ttu-id="c6798-110">在 Lync Server 2013 中创建或编辑新类别</span><span class="sxs-lookup"><span data-stu-id="c6798-110">Creating or editing a new category in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-category.md)

  - [<span data-ttu-id="c6798-111">在 Lync Server 2013 中创建或编辑新聊天室</span><span class="sxs-lookup"><span data-stu-id="c6798-111">Creating or editing a new room in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-room.md)

  - [<span data-ttu-id="c6798-112">在 Lync Server 2013 中创建新的聊天室外接程序</span><span class="sxs-lookup"><span data-stu-id="c6798-112">Creating new add-ins for rooms in Lync Server 2013</span></span>](lync-server-2013-creating-new-add-ins-for-rooms.md)

  - [<span data-ttu-id="c6798-113">在 Lync Server 2013 中设置谁可以在大会堂聊天室发布消息</span><span class="sxs-lookup"><span data-stu-id="c6798-113">Setting who can post messages in an auditorium chat room in Lync Server 2013</span></span>](lync-server-2013-setting-who-can-post-messages-in-an-auditorium-chat-room.md)

  - [<span data-ttu-id="c6798-114">在 Lync Server 2013 中禁用或启用聊天室</span><span class="sxs-lookup"><span data-stu-id="c6798-114">Disabling or enabling a chat room in Lync Server 2013</span></span>](lync-server-2013-disabling-or-enabling-a-chat-room.md)

  - [<span data-ttu-id="c6798-115">在 Lync Server 2013 中将聊天室从一个类别移动到另一个类别</span><span class="sxs-lookup"><span data-stu-id="c6798-115">Moving a chat room from one category to another in Lync Server 2013</span></span>](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md)

  - [<span data-ttu-id="c6798-116">在 Lync Server 2013 中删除聊天室或类别</span><span class="sxs-lookup"><span data-stu-id="c6798-116">Deleting a chat room or category in Lync Server 2013</span></span>](lync-server-2013-deleting-a-chat-room-or-category.md)

  - [<span data-ttu-id="c6798-117">在 Lync Server 2013 中删除消息或清除作废的消息</span><span class="sxs-lookup"><span data-stu-id="c6798-117">Deleting a message or purging obsolete messages in Lync Server 2013</span></span>](lync-server-2013-deleting-a-message-or-purging-obsolete-messages.md)

<span data-ttu-id="c6798-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c6798-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

