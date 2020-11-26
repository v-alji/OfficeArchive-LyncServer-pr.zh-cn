---
title: Lync Server 2013：将用户迁移到统一联系人存储
description: Lync Server 2013：将用户迁移到统一联系人存储。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrate users to unified contact store
ms:assetid: 215a8ec1-d63e-4fdf-b73d-75aeb9dddb43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204737(v=OCS.15)
ms:contentKeyID: 48183600
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e9ee9850cc723ae132f15d7c0c6b3769e1240ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425589"
---
# <a name="migrate-users-to-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="abfc7-103">在 Lync Server 2013 中将用户迁移到统一联系人存储</span><span class="sxs-lookup"><span data-stu-id="abfc7-103">Migrate users to unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abfc7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abfc7-104">

<span> </span></span></span>

<span data-ttu-id="abfc7-105">_**主题上次修改时间：** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="abfc7-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="abfc7-106">当用户执行以下操作时，用户的联系人会自动迁移到 Exchange 2013 服务器：</span><span class="sxs-lookup"><span data-stu-id="abfc7-106">A user's contacts are automatically migrated to the Exchange 2013 server when the user:</span></span>

  - <span data-ttu-id="abfc7-107">为其分配了将 UcsAllowed 设置为 True 的用户服务策略。</span><span class="sxs-lookup"><span data-stu-id="abfc7-107">Has been assigned a user services policy that has UcsAllowed set to True.</span></span>

  - <span data-ttu-id="abfc7-108">已使用 Exchange 2013 邮箱进行了设置，并且至少已登录到邮箱一次。</span><span class="sxs-lookup"><span data-stu-id="abfc7-108">Has been provisioned with an Exchange 2013 mailbox and has signed into the mailbox at least once.</span></span>

  - <span data-ttu-id="abfc7-109">使用 Lync 2013 胖客户端登录。</span><span class="sxs-lookup"><span data-stu-id="abfc7-109">Logs in by using a Lync 2013 rich client.</span></span>

<span data-ttu-id="abfc7-110">如果用户使用 Lync 2010 或早期版本的客户端登录，或者如果用户未连接到 Exchange 2013 服务器，则将忽略用户服务策略，并且用户的联系人保留在 Lync Server 中。</span><span class="sxs-lookup"><span data-stu-id="abfc7-110">If the user logs in with a Lync 2010 or earlier client, or if the user is not connected to an Exchange 2013 server, the user services policy is ignored and the user's contacts remain in Lync Server.</span></span>

<span data-ttu-id="abfc7-111">您可以通过以下任一方法来确定是否已迁移用户的联系人：</span><span class="sxs-lookup"><span data-stu-id="abfc7-111">You can determine whether a user's contacts have been migrated by using either of the following methods:</span></span>

  - <span data-ttu-id="abfc7-112">在客户端计算机上检查以下注册表项：</span><span class="sxs-lookup"><span data-stu-id="abfc7-112">Check the following registry key on the client computer:</span></span>
    
    <span data-ttu-id="abfc7-113">HKEY \_ 当前 \_ 用户 \\ 软件 \\ Microsoft \\ Office \\ 15.0 \\ Lync \\ \<SIP URL\> \\ UCS</span><span class="sxs-lookup"><span data-stu-id="abfc7-113">HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\\\<SIP URL\>\\UCS</span></span>
    
    <span data-ttu-id="abfc7-114">如果用户的联系人存储在 Exchange 2013 中，则此注册表项包含值为2165的 InUCSMode 值。</span><span class="sxs-lookup"><span data-stu-id="abfc7-114">If the user's contacts are stored in Exchange 2013, this key contains a value of InUCSMode with a value of 2165.</span></span>

  - <span data-ttu-id="abfc7-115">运行 **Test-CsUnifiedContactStore** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abfc7-115">Run the **Test-CsUnifiedContactStore** cmdlet.</span></span> <span data-ttu-id="abfc7-116">在 Lync Server Management Shell 命令行中，键入：</span><span class="sxs-lookup"><span data-stu-id="abfc7-116">At the Lync Server Management Shell command line, type:</span></span>
    
        Test-CsUnifiedContactStore -UserSipAddress "sip:kenmyer@litwareinc.com" -TargetFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="abfc7-117">如果 **Test-CsUnifiedContactStore** 成功，表明用户的联系人已迁移到统一联系人存储中。</span><span class="sxs-lookup"><span data-stu-id="abfc7-117">If **Test-CsUnifiedContactStore** succeeds, the user's contacts were migrated to unified contact store.</span></span>

<span data-ttu-id="abfc7-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abfc7-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

