---
title: Lync Server 2013：禁用或启用聊天室
description: Lync Server 2013：禁用或启用聊天室。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling or enabling a chat room
ms:assetid: db0908fc-aae3-46e8-bc0b-245e9adfa1e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215883(v=OCS.15)
ms:contentKeyID: 48706011
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b81ce2614cebcf554c0390369068d8fd8b8f932
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437845"
---
# <a name="disabling-or-enabling-a-chat-room-in-lync-server-2013"></a><span data-ttu-id="f1985-103">在 Lync Server 2013 中禁用或启用聊天室</span><span class="sxs-lookup"><span data-stu-id="f1985-103">Disabling or enabling a chat room in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1985-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1985-104">

<span> </span></span></span>

<span data-ttu-id="f1985-105">_**主题上次修改时间：** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="f1985-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="f1985-106">如果永久聊天室的主题不再相关，您可以通过禁用该聊天室使用户无法使用该聊天室。</span><span class="sxs-lookup"><span data-stu-id="f1985-106">If the topic of a Persistent Chat room is no longer relevant, you can make the chat room unavailable to users by disabling it.</span></span> <span data-ttu-id="f1985-107">禁用聊天室时，所有成员将立即从聊天室断开。</span><span class="sxs-lookup"><span data-stu-id="f1985-107">When a chat room is disabled, all members are immediately disconnected from the room.</span></span> <span data-ttu-id="f1985-108">禁用聊天室后，用户无法重新加入或在聊天室搜索中找到该聊天室。</span><span class="sxs-lookup"><span data-stu-id="f1985-108">After a chat room is disabled, users cannot rejoin it or find it in chat room searches.</span></span>

<span data-ttu-id="f1985-109">已禁用的聊天室可在稍后由持久聊天管理员启用。</span><span class="sxs-lookup"><span data-stu-id="f1985-109">A disabled chat room can be enabled later by a Persistent Chat administrator.</span></span> <span data-ttu-id="f1985-110">如果聊天室被禁用，其成员关系列表和其他设置将被保留。</span><span class="sxs-lookup"><span data-stu-id="f1985-110">If a chat room is disabled, its membership list and other settings are preserved.</span></span> <span data-ttu-id="f1985-111">如果再次启用聊天室，则无需手动重新创建设置。</span><span class="sxs-lookup"><span data-stu-id="f1985-111">If you enable the room again, you do not need to manually re-create the settings.</span></span>

<span data-ttu-id="f1985-112">如果聊天室的历史记录持续存在 (聊天室历史记录持久性是适用于类别内所有聊天室的类别的可选设置;默认情况下，它将保持不变，但可以通过将类别的 " **启用" 聊天历史记录** 设置为 false) 来保持关闭状态，禁用聊天室时会保留内容。</span><span class="sxs-lookup"><span data-stu-id="f1985-112">If the chat room’s history persists (chat room history persistence is an optional setting on a category that applies to all rooms within the category; the default is that it is persisted, but can be turned off by setting the category’s **Enable Chat History** to false), the content is preserved when the chat room is disabled.</span></span> <span data-ttu-id="f1985-113">但是，在该聊天室处于禁用状态时，该内容不会显示在搜索中。</span><span class="sxs-lookup"><span data-stu-id="f1985-113">However, that content will not appear in searches during the time that the chat room remains in a disabled state.</span></span> <span data-ttu-id="f1985-114">如果随后启用该聊天室，则用户可以搜索禁用该聊天室之前发布的消息。</span><span class="sxs-lookup"><span data-stu-id="f1985-114">If you later enable the chat room, users can search for messages that were posted before the chat room was disabled.</span></span>

<span data-ttu-id="f1985-115">有关通过使用 Windows PowerShell 命令行界面禁用和启用聊天室的详细信息，请参阅 [使用 Windows powershell Cmdlet 配置持久聊天服务器](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)中的 "会议室管理"。</span><span class="sxs-lookup"><span data-stu-id="f1985-115">For details about disabling and enabling chat rooms by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span> <span data-ttu-id="f1985-116">若要禁用聊天室，请使用类似下面的命令：</span><span class="sxs-lookup"><span data-stu-id="f1985-116">To disable a chat room, use a command similar to this:</span></span>

    Set-CsPersistentChatRoom -Identity "atl-cs-001.litwareinc.com\ITChatRoom" -Disabled $True

<span data-ttu-id="f1985-117">若要启用聊天室，请将 Disabled 属性设置为 False：</span><span class="sxs-lookup"><span data-stu-id="f1985-117">To enabled a chat room, set the Disabled property to False:</span></span>

    Set-CsPersistentChatRoom -Identity "atl-cs-001.litwareinc.com\ITChatRoom" -Disabled $False

<span data-ttu-id="f1985-118">请注意，聊天室无法通过使用 Lync Server 控制面板启用或禁用。</span><span class="sxs-lookup"><span data-stu-id="f1985-118">Note that chat rooms cannot be enabled or disabled by using the Lync Server Control Panel.</span></span>

<span data-ttu-id="f1985-119">有关配置聊天室的详细信息，请参阅部署文档中 [Lync Server 2013](lync-server-2013-configure-rooms.md) 中的 "配置聊天室"。</span><span class="sxs-lookup"><span data-stu-id="f1985-119">For details about configuring chat rooms, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) in the Deployment documentation.</span></span>

<span data-ttu-id="f1985-120"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1985-120"></div>

<span> </span>

</div>

</div>

</span></span></div>

