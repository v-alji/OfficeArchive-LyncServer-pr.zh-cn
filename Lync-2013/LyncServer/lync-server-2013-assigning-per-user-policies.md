---
title: Lync Server 2013：分配每用户策略
description: Lync Server 2013：分配每个用户的策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user policies
ms:assetid: a4ed0120-d9e5-4eb2-acfd-8de2cb503652
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182561(v=OCS.15)
ms:contentKeyID: 48184971
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a99156f9413926251c27dfee40677976b80b7ea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438293"
---
# <a name="assigning-per-user-policies-in-lync-server-2013"></a><span data-ttu-id="270f7-103">在 Lync Server 2013 中分配每个用户的策略</span><span class="sxs-lookup"><span data-stu-id="270f7-103">Assigning per-user policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="270f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="270f7-104">

<span> </span></span></span>

<span data-ttu-id="270f7-105">_**主题上次修改时间：** 2012-10-14_</span><span class="sxs-lookup"><span data-stu-id="270f7-105">_**Topic Last Modified:** 2012-10-14_</span></span>

<span data-ttu-id="270f7-106">你可以将某些策略分配给用户或用户组，以指定与分配给其他用户的策略（如全局策略）中定义的设置不同的特定设置。</span><span class="sxs-lookup"><span data-stu-id="270f7-106">You can assign certain policies to a user or a group of users in order to specify particular settings that deviate from the settings defined in policies assigned to other users, such as global policies.</span></span> <span data-ttu-id="270f7-107">这些策略称为每用户策略。</span><span class="sxs-lookup"><span data-stu-id="270f7-107">These policies are called per-user policies.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="270f7-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="270f7-108">In This Section</span></span>

  - [<span data-ttu-id="270f7-109">在 Lync Server 2013 中分配每用户会议策略</span><span class="sxs-lookup"><span data-stu-id="270f7-109">Assign a per-user conferencing policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-conferencing-policy.md)

  - [<span data-ttu-id="270f7-110">在 Lync Server 2013 中分配每用户客户端版本策略</span><span class="sxs-lookup"><span data-stu-id="270f7-110">Assign a per-user client version policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-client-version-policy.md)

  - [<span data-ttu-id="270f7-111">在 Lync Server 2013 中分配每用户 PIN 策略</span><span class="sxs-lookup"><span data-stu-id="270f7-111">Assign a per-user PIN policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-pin-policy.md)

  - [<span data-ttu-id="270f7-112">在 Lync Server 2013 中将外部用户访问策略分配到启用 Lync 的用户</span><span class="sxs-lookup"><span data-stu-id="270f7-112">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)

  - [<span data-ttu-id="270f7-113">在 Lync Server 2013 中分配每用户存档策略</span><span class="sxs-lookup"><span data-stu-id="270f7-113">Assign a per-user archiving policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-archiving-policy.md)

  - [<span data-ttu-id="270f7-114">在 Lync Server 2013 中分配每用户位置策略</span><span class="sxs-lookup"><span data-stu-id="270f7-114">Assign a per-user location policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-location-policy.md)

  - [<span data-ttu-id="270f7-115">在 Lync Server 2013 中分配每用户移动策略</span><span class="sxs-lookup"><span data-stu-id="270f7-115">Assign a per-user mobility policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-mobility-policy.md)

  - [<span data-ttu-id="270f7-116">在 Lync Server 2013 中分配每用户持久聊天策略</span><span class="sxs-lookup"><span data-stu-id="270f7-116">Assign a per-user Persistent Chat policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-persistent-chat-policy.md)

  - [<span data-ttu-id="270f7-117">在 Lync Server 2013 中分配每个用户的拨号计划策略</span><span class="sxs-lookup"><span data-stu-id="270f7-117">Assign a per-user dial plan policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-dial-plan-policy.md)

  - [<span data-ttu-id="270f7-118">在 Lync Server 2013 中分配每用户语音策略</span><span class="sxs-lookup"><span data-stu-id="270f7-118">Assign a per-user voice policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-voice-policy.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="270f7-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="270f7-119">See Also</span></span>


[<span data-ttu-id="270f7-120">在 Lync Server 2013 中管理用户</span><span class="sxs-lookup"><span data-stu-id="270f7-120">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="270f7-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="270f7-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

