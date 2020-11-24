---
title: Skype for Business Online 中使用全局范围和标记范围的 cmdlet
description: Skype for Business Online 中使用全局范围和标签范围的 cmdlet。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use the global scope and the tag scope
ms:assetid: 1e2bc055-8a72-425e-967b-e253add7018c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362774(v=OCS.15)
ms:contentKeyID: 56558824
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba89ebe7322159027c5de765117afd366cb3dc23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391910"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-the-global-scope-and-the-tag-scope"></a><span data-ttu-id="8ed0c-103">Skype for Business Online 中使用全局范围和标记范围的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ed0c-103">Cmdlets in Skype for Business Online that use the global scope and the tag scope</span></span>

 


<span data-ttu-id="8ed0c-104">在 Skype for Business Online 中，可以在 *全局范围内* 或在 *标记范围内* 配置策略 (或 *按用户范围*) 。</span><span class="sxs-lookup"><span data-stu-id="8ed0c-104">In Skype for Business Online, policies can be configured at either the *global scope* or at the *tag scope* (or *per-user scope*).</span></span> <span data-ttu-id="8ed0c-105">使用 **Cs** cmdlet 时，无需指定范围或标识。</span><span class="sxs-lookup"><span data-stu-id="8ed0c-105">When using the **Get-Cs** cmdlets, you do not have to specify a scope or identity.</span></span> <span data-ttu-id="8ed0c-106">如果您调用其中一个 cmdlet 且不带任何参数，则将返回所有相关项。</span><span class="sxs-lookup"><span data-stu-id="8ed0c-106">If you call one of these cmdlets without any parameters, then all the relevant items will be returned.</span></span> <span data-ttu-id="8ed0c-107">例如，此命令将返回有关所有外部访问策略的信息：</span><span class="sxs-lookup"><span data-stu-id="8ed0c-107">For example, this command returns information about all your external access policies:</span></span>

    Get-CsExternalAccessPolicy

<span data-ttu-id="8ed0c-108">如果要限制返回的数据，只需包含 Identity 参数或 Filter 参数。</span><span class="sxs-lookup"><span data-stu-id="8ed0c-108">You need to include only the Identity parameter or the Filter parameter if you want to limit the returned data.</span></span> <span data-ttu-id="8ed0c-109">例如，若要仅返回全局策略，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="8ed0c-109">For example, to return only the global policy, use this command:</span></span>

    Get-CsExternalAccessPolicy -Identity "global"

<span data-ttu-id="8ed0c-110">若要返回具有 "RedmondAccessPolicy" 标识的每用户策略，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="8ed0c-110">To return a per-user policy that has the Identity “RedmondAccessPolicy”, use this command:</span></span>

    Get-CsExternalAccessPolicy -Identity "RedmondAccessPolicy"


> [!NOTE]  
> <span data-ttu-id="8ed0c-111">引用每用户策略时，标记 <STRONG>前缀</STRONG> 是可选的。</span><span class="sxs-lookup"><span data-stu-id="8ed0c-111">When referencing a per-user policy, the tag <STRONG>prefix</STRONG> is optional.</span></span> <span data-ttu-id="8ed0c-112">此语法（包括前缀）也有效：</span><span class="sxs-lookup"><span data-stu-id="8ed0c-112">This syntax, which includes the prefix, is also valid:</span></span><BR><span data-ttu-id="8ed0c-113">Get-CsExternalAccessPolicy-Identity "tag： RedmondAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="8ed0c-113">Get-CsExternalAccessPolicy –Identity "tag:RedmondAccessPolicy"</span></span>



<span data-ttu-id="8ed0c-114">若要返回除全局策略之外的所有策略 (也就是说，所有基于用户的策略) ，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="8ed0c-114">To return all policies except the global policies (that is, all the per-user policies), use this command:</span></span>

    Get-CsExternalAccessPolicy -Filter "tag:*"

<span data-ttu-id="8ed0c-115">以下 cmdlet 对全局范围和每用户 (标记) 作用域进行操作：</span><span class="sxs-lookup"><span data-stu-id="8ed0c-115">The following cmdlets operate against both the global scope and the per-user (tag) scope:</span></span>

  - <span data-ttu-id="8ed0c-116">[Set-csclientpolicy](https://technet.microsoft.com/library/gg398830\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="8ed0c-116">[Get-CsClientPolicy](https://technet.microsoft.com/library/gg398830\(v=ocs.15\))</span></span>

  - <span data-ttu-id="8ed0c-117">[Get-CsConferencingPolicy](https://technet.microsoft.com/library/gg398293\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="8ed0c-117">[Get-CsConferencingPolicy](https://technet.microsoft.com/library/gg398293\(v=ocs.15\))</span></span>

  - <span data-ttu-id="8ed0c-118">[Get-CsDialPlan](https://technet.microsoft.com/library/gg413043\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="8ed0c-118">[Get-CsDialPlan](https://technet.microsoft.com/library/gg413043\(v=ocs.15\))</span></span>

  - <span data-ttu-id="8ed0c-119">[CsExternalAccessPolicy](https://technet.microsoft.com/library/gg425805\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="8ed0c-119">[Get-CsExternalAccessPolicy](https://technet.microsoft.com/library/gg425805\(v=ocs.15\))</span></span>

  - <span data-ttu-id="8ed0c-120">[CsHostedVoicemailPolicy](https://technet.microsoft.com/library/gg398348\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="8ed0c-120">[Get-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/gg398348\(v=ocs.15\))</span></span>

  - <span data-ttu-id="8ed0c-121">[Get-CsPresencePolicy](https://technet.microsoft.com/library/gg398463\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="8ed0c-121">[Get-CsPresencePolicy](https://technet.microsoft.com/library/gg398463\(v=ocs.15\))</span></span>

  - <span data-ttu-id="8ed0c-122">[CsVoicePolicy](https://technet.microsoft.com/library/gg398101\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="8ed0c-122">[Get-CsVoicePolicy](https://technet.microsoft.com/library/gg398101\(v=ocs.15\))</span></span>


> [!NOTE]  
> <span data-ttu-id="8ed0c-123">尽管名称、拨号计划和功能，请说出策略。</span><span class="sxs-lookup"><span data-stu-id="8ed0c-123">Despite the name, dial plans are, functionally speaking, policies.</span></span> <span data-ttu-id="8ed0c-124">使用 " <EM>拨号计划</EM> " 而不是 "拨号策略"，以保留早期版本的 Lync Server 所使用的术语。</span><span class="sxs-lookup"><span data-stu-id="8ed0c-124">The term <EM>dial plan</EM> is used instead of, for example, dialing policy, in order to preserve the terminology used with previous versions of Lync Server.</span></span>



## <a name="see-also"></a><span data-ttu-id="8ed0c-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8ed0c-125">See Also</span></span>


[<span data-ttu-id="8ed0c-126">Skype for Business Online 中的身份、范围和租户</span><span class="sxs-lookup"><span data-stu-id="8ed0c-126">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="8ed0c-127">[Lync Online Cmdlet](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="8ed0c-127">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

