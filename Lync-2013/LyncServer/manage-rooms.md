---
title: 管理聊天室
description: 管理会议室。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Manage rooms
ms:assetid: d4835cf4-cd09-4769-a08e-e92706861b64
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205292(v=OCS.15)
ms:contentKeyID: 48185505
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be093e14a68639fdde73b58936e1b2f5cf4424cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446154"
---
# <a name="manage-rooms"></a><span data-ttu-id="951e3-103">管理聊天室</span><span class="sxs-lookup"><span data-stu-id="951e3-103">Manage rooms</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="951e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="951e3-104">

<span> </span></span></span>

<span data-ttu-id="951e3-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="951e3-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="951e3-106">创建新的持久聊天服务器聊天室</span><span class="sxs-lookup"><span data-stu-id="951e3-106">To create a new Persistent Chat Server room</span></span>

    New-CsPersistentChatRoom -Name Foo1 -PersistentChatPoolFqdn client.contoso.com -Category client.contoso.com\Foo [other parameters]

<div>


> [!IMPORTANT]  
> <span data-ttu-id="951e3-107">如果满足下列条件之一，则不需要 -PersistentChatPoolFqdn：</span><span class="sxs-lookup"><span data-stu-id="951e3-107">-PersistentChatPoolFqdn is not needed if one of the following is true:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="951e3-108">只有一个持久聊天服务器池。</span><span class="sxs-lookup"><span data-stu-id="951e3-108">There is only one Persistent Chat Server pool.</span></span></P>
> <LI>
> <P><span data-ttu-id="951e3-109">您为类别提供了一个池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="951e3-109">You provide a pool FQDN to the category.</span></span></P>
> <LI>
> <P><span data-ttu-id="951e3-110">您提供了一个池 Fqdn 以添加聊天室。</span><span class="sxs-lookup"><span data-stu-id="951e3-110">You provide a pool FQDN to adding the room.</span></span></P></LI></UL>



</div>

<span data-ttu-id="951e3-111">对现有持久聊天服务器聊天室进行更改</span><span class="sxs-lookup"><span data-stu-id="951e3-111">To make changes to an existing Persistent Chat Server room</span></span>

    Set-CsPersistentChatRoom -Identity testCat -Members @{Add="sip:user1@contoso.com", "CN=container,DC=contoso,DC=com"}
    Set-CsPersistentChatRoom -Identity testCat -Managers @{Add="sip:user2@contoso.com"}
    Set-CsPersistentChatRoom -Identity testCat -Presenters @{Add="sip:user1@contoso.com"}

<span data-ttu-id="951e3-112">Windows PowerShell：成员、经理和演示者可以同时进行设置。</span><span class="sxs-lookup"><span data-stu-id="951e3-112">Windows PowerShell: Members, Managers and Presenters can be set simultaneously.</span></span> <span data-ttu-id="951e3-113">它们都应是主机类别的 AllowedMembers 减去 DeniedMembers 的子集。</span><span class="sxs-lookup"><span data-stu-id="951e3-113">They all should be the subset of AllowedMembers minus DeniedMembers of the host Category.</span></span> <span data-ttu-id="951e3-114">类型为 normal 的聊天室不能包含演示者。</span><span class="sxs-lookup"><span data-stu-id="951e3-114">A room that is type=normal cannot include Presenters.</span></span>

<div>

## <a name="create-get-set-clear-or-remove-a-room"></a><span data-ttu-id="951e3-115">创建、获取、设置、清除或删除聊天室</span><span class="sxs-lookup"><span data-stu-id="951e3-115">Create, Get, Set, Clear, or Remove a Room</span></span>

<span data-ttu-id="951e3-116">创建新聊天室</span><span class="sxs-lookup"><span data-stu-id="951e3-116">To create a new room</span></span>

    New-CsPersistentChatRoom -Name <String> [-PersistentChatPoolFqdn <String>]-Category <String> [-Description <String>] [-Disabled <Switch Parameter>] [-Type <Normal | Auditorium>] [-AddIn <String>] [-Privacy <ChatRoomPrivacy> {Open | Closed | Secret}] [-Invitations <Switch Parameter>]

<span data-ttu-id="951e3-117">设置会议室</span><span class="sxs-lookup"><span data-stu-id="951e3-117">To set a room</span></span>

    Set-CsPersistentChatRoom -Identity <String> [-Name <String>] [-Category <String>] [-Description <String>] [-Disabled <boolean>] [-Type <Normal | Auditorium>] [-AddIn <String>] [-Privacy <ChatRoomPrivacy> {Open | Closed | Secret}] [-Invitations <Enum>] [-Members <PSListModifier<String>>] [-Managers <PSListModifier<String>>] [-Presenters <PSListModifier<String>>] [-Force < Switch Parameter >] [-Confirm <Switch Parameter>][-WhatIf <Switch Parameter>]

<span data-ttu-id="951e3-118">获取聊天室</span><span class="sxs-lookup"><span data-stu-id="951e3-118">To get a room</span></span>

    Get-CsPersistentChatRoom -Identity <String>

<span data-ttu-id="951e3-119">或者</span><span class="sxs-lookup"><span data-stu-id="951e3-119">or</span></span>

    Get-CsPersistentChatRoom -filter <String> [-PersistentChatPoolFqdn <String>] [-SearchDescription] [-Member <String>] [-Manager <string>] [-Category <string>] [-Addin <string>] [-Disabled <bool>] [-Privacy <ChatRoomPrivacy> {Open | Closed | Secret}] [-Type <ChatRoomType> {Normal | Auditorium}] [-Invitations <ChatRoomInvitations> {False | Inherit}] [-ChatContentExceedsMB <int>] [-ResultSize <int>]

<span data-ttu-id="951e3-120">其中-筛选器仅支持名称和说明，并可帮助你查找名称/描述与关键字字符串匹配的聊天室。</span><span class="sxs-lookup"><span data-stu-id="951e3-120">where –filter supports only Name and Description and helps you find rooms whose Name/Description matches the keyword string.</span></span> <span data-ttu-id="951e3-121">PoolFqdn 在给定的持久聊天服务器池中进行搜索。</span><span class="sxs-lookup"><span data-stu-id="951e3-121">PoolFqdn searches in a given Persistent Chat Server pool.</span></span>

<span data-ttu-id="951e3-122">清除聊天室并从聊天室中清除消息</span><span class="sxs-lookup"><span data-stu-id="951e3-122">To clear a room and clear messages from a room</span></span>

    Clear-CsPersistentChatRoom [-Identity] <string> -EndDate <DateTime> [-WhatIf] [-Confirm]  [<CommonParameters>]

<span data-ttu-id="951e3-123">或者</span><span class="sxs-lookup"><span data-stu-id="951e3-123">or</span></span>

    Clear-CsPersistentChatRoom [-Instance] <ChatRoomObject> -EndDate <DateTime> [-WhatIf] [-Confirm] [<CommonParameters>]

<span data-ttu-id="951e3-124">删除聊天室</span><span class="sxs-lookup"><span data-stu-id="951e3-124">To remove a room</span></span>

    Remove-CsPersistentChatRoom [-Identity] <string> [-Force] [-WhatIf] [-Confirm]  [<CommonParameters>]

<span data-ttu-id="951e3-125">或者</span><span class="sxs-lookup"><span data-stu-id="951e3-125">or</span></span>

    Remove-CsPersistentChatRoom [-Instance] <ChatRoomObject> [-Force] [-WhatIf] [-Confirm]  [<CommonParameters>]

<span data-ttu-id="951e3-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="951e3-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

