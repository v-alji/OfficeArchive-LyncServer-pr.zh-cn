---
title: Skype for Business Online 中使用用户标识的 cmdlet
description: Skype for Business Online 中使用用户标识的 cmdlet。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a user identity
ms:assetid: be87409f-6372-4c70-91ac-6ef13dfbe65a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362842(v=OCS.15)
ms:contentKeyID: 56558859
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 29f838317f8b2779de862eb2df82ae1b348871e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391956"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-user-identity"></a><span data-ttu-id="e86be-103">Skype for Business Online 中使用用户标识的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e86be-103">Cmdlets in Skype for Business Online that use a user identity</span></span>

 


<span data-ttu-id="e86be-104">在 Skype for Business Online 中，可以通过多种不同的方式引用单个用户标识：</span><span class="sxs-lookup"><span data-stu-id="e86be-104">In Skype for Business Online, there are a number of different ways to reference an individual user Identity:</span></span>

  - <span data-ttu-id="e86be-105">使用用户的 Active Directory 域服务显示名称。</span><span class="sxs-lookup"><span data-stu-id="e86be-105">Use the user’s Active Directory Domain Services display name.</span></span> <span data-ttu-id="e86be-106">例如：</span><span class="sxs-lookup"><span data-stu-id="e86be-106">For example:</span></span>
    
        -Identity "Ken Myer"

  - <span data-ttu-id="e86be-107">使用用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="e86be-107">Use the user’s SIP address.</span></span> <span data-ttu-id="e86be-108">例如：</span><span class="sxs-lookup"><span data-stu-id="e86be-108">For example:</span></span>
    
        -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="e86be-109">使用用户的 UPN。</span><span class="sxs-lookup"><span data-stu-id="e86be-109">Use the user’s UPN.</span></span> <span data-ttu-id="e86be-110">例如：</span><span class="sxs-lookup"><span data-stu-id="e86be-110">For example:</span></span>
    
        -Identity " kenmyer@litwareinc.com"

  - <span data-ttu-id="e86be-111">使用用户的 Active Directory 域服务可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="e86be-111">Use the user’s Active Directory Domain Services distinguished name.</span></span> <span data-ttu-id="e86be-112">例如：</span><span class="sxs-lookup"><span data-stu-id="e86be-112">For example:</span></span>
    
        -Identity "CN=48ebd1ba-95d4-460c-b751-811ebf0c4611,OU=fa8226f5-14fa-46da-8 236-039b25bc7a27,OU=Lync Online Tenants,DC=litwareinc,DC=com"

<span data-ttu-id="e86be-113">以下 cmdlet 接受用户标识：</span><span class="sxs-lookup"><span data-stu-id="e86be-113">The following cmdlets accept a user Identity:</span></span>

  - <span data-ttu-id="e86be-114">[Disable-CsMeetingRoom](https://technet.microsoft.com/library/jj204723\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-114">[Disable-CsMeetingRoom](https://technet.microsoft.com/library/jj204723\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-115">[Enable-CsMeetingRoom](https://technet.microsoft.com/library/jj205062\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-115">[Enable-CsMeetingRoom](https://technet.microsoft.com/library/jj205062\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-116">[Get-CsExUmContact](https://technet.microsoft.com/library/gg412725\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-116">[Get-CsExUmContact](https://technet.microsoft.com/library/gg412725\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-117">[Get-CsMeetingRoom](https://technet.microsoft.com/library/jj205277\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-117">[Get-CsMeetingRoom](https://technet.microsoft.com/library/jj205277\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-118">[Get-CsOnlineUser](https://technet.microsoft.com/library/jj994026\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-118">[Get-CsOnlineUser](https://technet.microsoft.com/library/jj994026\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-119">[Get-CsUserAcp](https://technet.microsoft.com/library/gg398978\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-119">[Get-CsUserAcp](https://technet.microsoft.com/library/gg398978\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-120">[New-CsExUmContact](https://technet.microsoft.com/library/gg398139\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-120">[New-CsExUmContact](https://technet.microsoft.com/library/gg398139\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-121">[Remove-CsExUmContact](https://technet.microsoft.com/library/gg398946\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-121">[Remove-CsExUmContact](https://technet.microsoft.com/library/gg398946\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-122">[Remove-CsUserAcp](https://technet.microsoft.com/library/gg398982\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-122">[Remove-CsUserAcp](https://technet.microsoft.com/library/gg398982\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-123">[Set-CsExUmContact](https://technet.microsoft.com/library/gg412944\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-123">[Set-CsExUmContact](https://technet.microsoft.com/library/gg412944\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-124">[Set-CsMeetingRoom](https://technet.microsoft.com/library/jj204831\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-124">[Set-CsMeetingRoom](https://technet.microsoft.com/library/jj204831\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e86be-125">[Set-CsUserAcp](https://technet.microsoft.com/library/gg413018\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-125">[Set-CsUserAcp](https://technet.microsoft.com/library/gg413018\(v=ocs.15\))</span></span>

<span data-ttu-id="e86be-126">请注意，在调用其中一个 " **获取 Cs** " cmdlet 时无需指定用户标识。</span><span class="sxs-lookup"><span data-stu-id="e86be-126">Note that you do not need to specify a user Identity when calling one of the **Get-Cs** cmdlets.</span></span> <span data-ttu-id="e86be-127">在这种情况下，cmdlet 将返回指定项目的所有实例。</span><span class="sxs-lookup"><span data-stu-id="e86be-127">In this case, the cmdlets return all the instances of the specified item.</span></span> <span data-ttu-id="e86be-128">例如，此命令将返回已启用 Skype for Business Online 的所有用户的相关信息：</span><span class="sxs-lookup"><span data-stu-id="e86be-128">For example, this command returns information about all the users who have been enabled for Skype for Business Online:</span></span>

    Get-CsOnlineUser

<span data-ttu-id="e86be-129">只有当你希望返回特定用户的信息时，Identity 参数才是必需的：</span><span class="sxs-lookup"><span data-stu-id="e86be-129">The Identity parameter is required only if you want to return information for a specific user:</span></span>

    Get-CsOnlineUser -Identity "Ken Myer"

## <a name="see-also"></a><span data-ttu-id="e86be-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e86be-130">See Also</span></span>


[<span data-ttu-id="e86be-131">Skype for Business Online 中的身份、范围和租户</span><span class="sxs-lookup"><span data-stu-id="e86be-131">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="e86be-132">[Lync Online Cmdlet](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e86be-132">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

