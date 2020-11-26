---
title: Lync Server 2013：创建响应组代理组
description: Lync Server 2013：创建响应组代理组。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Response Group agent groups
ms:assetid: 2a80de17-ead0-46e8-8a27-7a4e233dbde0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520969(v=OCS.15)
ms:contentKeyID: 48183688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a9420ee5f6fbd4b995c8542b848ef30f53e46fc4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431615"
---
# <a name="create-response-group-agent-groups-lync-server-2013"></a><span data-ttu-id="4b8f5-103">在 Lync Server 2013 中创建响应组代理组</span><span class="sxs-lookup"><span data-stu-id="4b8f5-103">Create Response Group agent groups Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b8f5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b8f5-104">

<span> </span></span></span>

<span data-ttu-id="4b8f5-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="4b8f5-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="4b8f5-106">创建代理组时要选择分配给该组的代理并指定其他组设置，如路由方法以及代理能否登录到组和从组注销。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-106">When you create an agent group, you select the agents that are assigned to the group and specify additional group settings, such as the routing method and whether an agent can sign in to and out of the group.</span></span>

<span data-ttu-id="4b8f5-107">必须登录和注销组的代理（不同于登录或注销 Lync 服务器的代理）称为 *正式代理*。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-107">An agent who must sign in and out of the group, which is different from signing in or out of Lync Server, is called a *formal agent*.</span></span> <span data-ttu-id="4b8f5-108">正式代理必须登录到组，然后才能接收路由至该组的呼叫。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-108">Formal agents must be signed in to the group before they can receive calls routed to the group.</span></span> <span data-ttu-id="4b8f5-109">这对于以兼职形式应答组中的呼叫的代理很有用。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-109">This can be useful for agents who answer calls from the group on a part-time basis.</span></span> <span data-ttu-id="4b8f5-110">正式代理通过单击 Lync 2013 中的菜单项来登录和注销其组，以打开 Windows Internet Explorer Internet 浏览器并显示网页控制台。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-110">Formal agents sign in and out of their groups by clicking a menu item in Lync 2013 to open the Windows Internet Explorer Internet browser and display a webpage console.</span></span>

<span data-ttu-id="4b8f5-111">不登录到组或从组注销的代理称为 *非正式代理*。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-111">An agent who does not sign in or out of the group is called an *informal agent*.</span></span> <span data-ttu-id="4b8f5-112">非正式代理在登录 Lync Server 时自动登录到该组，并且不能注销该组。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-112">Informal agents are automatically signed in to the group when they sign in to Lync Server, and they cannot sign out of the group.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4b8f5-113">仅本地用户可成为代理。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-113">Only on-premises users can be agents.</span></span> <span data-ttu-id="4b8f5-114">如果代理从本地移动到联机，则响应组调用将不会路由到该代理。</span><span class="sxs-lookup"><span data-stu-id="4b8f5-114">If an agent is moved from on-premises to online, Response Group calls will not be routed to that agent.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4b8f5-115">本节内容</span><span class="sxs-lookup"><span data-stu-id="4b8f5-115">In This Section</span></span>

[<span data-ttu-id="4b8f5-116">在 Lync Server 2013 中创建或修改代理组</span><span class="sxs-lookup"><span data-stu-id="4b8f5-116">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)

<span data-ttu-id="4b8f5-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b8f5-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

