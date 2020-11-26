---
title: Lync Server 2013：为用户禁用组呼叫装货
description: Lync Server 2013：禁用组呼叫用户的分拣。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disable Group Call Pickup for users
ms:assetid: 91b06f9e-2840-45a2-bbb3-6a29179b9a9f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945638(v=OCS.15)
ms:contentKeyID: 51541492
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3f5b4542cf7bb8ea5be524d2695701979ec2987
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429103"
---
# <a name="disable-group-call-pickup-for-users-in-lync-server-2013"></a><span data-ttu-id="8439c-103">在 Lync Server 2013 中禁用用户的组呼叫装货</span><span class="sxs-lookup"><span data-stu-id="8439c-103">Disable Group Call Pickup for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8439c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8439c-104">

<span> </span></span></span>

<span data-ttu-id="8439c-105">_**主题上次修改时间：** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="8439c-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="8439c-106">使用以下过程可禁用用户的组呼叫装货。</span><span class="sxs-lookup"><span data-stu-id="8439c-106">Use the following procedure to disable Group Call Pickup for a user.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8439c-107">当您为用户禁用组呼叫装货时，分配给该用户的呼叫装货组号码将不会保留。</span><span class="sxs-lookup"><span data-stu-id="8439c-107">When you disable Group Call Pickup for a user, the call pickup group number that was assigned to the user is not retained.</span></span> <span data-ttu-id="8439c-108">如果随后想要为该用户重新启用组呼叫装货，则必须使用/enablegrouppickup 参数再次分配呼叫装货组编号。</span><span class="sxs-lookup"><span data-stu-id="8439c-108">If you subsequently want to re-enable Group Call Pickup for that user, you must assign the call pickup group number again with the /enablegrouppickup parameter.</span></span>



</div>

<div>

## <a name="to-disable-group-call-pickup-for-a-user"></a><span data-ttu-id="8439c-109">为用户禁用组呼叫装货</span><span class="sxs-lookup"><span data-stu-id="8439c-109">To disable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="8439c-110">使用管理员权限登录安装了 SEFAUtil 工具的计算机。</span><span class="sxs-lookup"><span data-stu-id="8439c-110">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="8439c-111">在该命令行处，运行：</span><span class="sxs-lookup"><span data-stu-id="8439c-111">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /disablegrouppickup
    
    <span data-ttu-id="8439c-112">例如：</span><span class="sxs-lookup"><span data-stu-id="8439c-112">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /disablegrouppickup

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8439c-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8439c-113">See Also</span></span>


[<span data-ttu-id="8439c-114">向 Lync Server 2013 中的用户分配组呼叫的装货号码</span><span class="sxs-lookup"><span data-stu-id="8439c-114">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)  
[<span data-ttu-id="8439c-115">在 Lync Server 2013 中为用户启用组呼叫装货</span><span class="sxs-lookup"><span data-stu-id="8439c-115">Enable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-enable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="8439c-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8439c-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

