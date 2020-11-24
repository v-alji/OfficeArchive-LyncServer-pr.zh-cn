---
title: Skype for Business Online 中不使用作用域或标识的 cmdlet
description: Skype for Business Online 中不使用作用域或标识的 cmdlet。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that do not use a scope or an identity
ms:assetid: 9c50c732-3c64-4b6a-96fd-8f528eb739ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362824(v=OCS.15)
ms:contentKeyID: 56558839
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7d893c4cf9203c8657dfbdfd7fb2bf46dbdfe4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391961"
---
# <a name="cmdlets-in-skype-for-business-online-that-do-not-use-a-scope-or-an-identity"></a><span data-ttu-id="4d5b8-103">Skype for Business Online 中不使用作用域或标识的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="4d5b8-103">Cmdlets in Skype for Business Online that do not use a scope or an identity</span></span>

 


<span data-ttu-id="4d5b8-104">修改允许的列表和阻止的列表时使用的 cmdlet (列表，用于确定允许用户与) 通信的外部组织不使用作用域或标识。</span><span class="sxs-lookup"><span data-stu-id="4d5b8-104">The cmdlets used when modifying the allowed lists and blocked lists (lists that determine which outside organizations your users are allowed to communicate with) do not use either a scope or an Identity.</span></span> <span data-ttu-id="4d5b8-105">实际上， **CsEdgeAllowAllKnownDomains** cmdlet 没有任何参数。</span><span class="sxs-lookup"><span data-stu-id="4d5b8-105">In fact, the **New-CsEdgeAllowAllKnownDomains** cmdlet does not have any parameters whatsoever.</span></span> <span data-ttu-id="4d5b8-106">不使用作用域或标识的 cmdlet 为：</span><span class="sxs-lookup"><span data-stu-id="4d5b8-106">The cmdlets that do not use either a scope or an Identity are:</span></span>

  - <span data-ttu-id="4d5b8-107">[New-CsEdgeAllowAllKnownDomains](https://technet.microsoft.com/library/jj994088\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="4d5b8-107">[New-CsEdgeAllowAllKnownDomains](https://technet.microsoft.com/library/jj994088\(v=ocs.15\))</span></span>

  - <span data-ttu-id="4d5b8-108">[New-CsEdgeAllowList](https://technet.microsoft.com/library/jj994023\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="4d5b8-108">[New-CsEdgeAllowList](https://technet.microsoft.com/library/jj994023\(v=ocs.15\))</span></span>

  - <span data-ttu-id="4d5b8-109">[New-CsEdgeDomainPattern](https://technet.microsoft.com/library/jj994040\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="4d5b8-109">[New-CsEdgeDomainPattern](https://technet.microsoft.com/library/jj994040\(v=ocs.15\))</span></span>

<span data-ttu-id="4d5b8-110">请注意，对于 **CsEdgeAllowList** Cmdlet 和 **CsEdgeDomainPattern** Cmdlet，必须包含 Domain 参数。</span><span class="sxs-lookup"><span data-stu-id="4d5b8-110">Note that, with both the **New-CsEdgeAllowList** cmdlet and the **New-CsEdgeDomainPattern** cmdlet, you must include the Domain parameter.</span></span> <span data-ttu-id="4d5b8-111">例如：</span><span class="sxs-lookup"><span data-stu-id="4d5b8-111">For example:</span></span>

    $x = New-CsEdgeDomainPattern -Domain "fabrikam.com"

## <a name="see-also"></a><span data-ttu-id="4d5b8-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d5b8-112">See Also</span></span>


[<span data-ttu-id="4d5b8-113">Skype for Business Online 中的身份、范围和租户</span><span class="sxs-lookup"><span data-stu-id="4d5b8-113">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="4d5b8-114">[Lync Online Cmdlet](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="4d5b8-114">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

