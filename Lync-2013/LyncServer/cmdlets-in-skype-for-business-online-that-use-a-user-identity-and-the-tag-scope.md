---
title: Skype for Business Online 中使用用户标识和标记作用域的 cmdlet
description: Skype for Business Online 中使用用户标识和标记作用域的 cmdlet。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a user identity and the tag scope
ms:assetid: 344a21b0-5301-4e77-853a-970bb1c11e1d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362781(v=OCS.15)
ms:contentKeyID: 56558838
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3e2ddbcc9c90096cea5fad4cb680f4ea1797ce48
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391958"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-user-identity-and-the-tag-scope"></a><span data-ttu-id="3c7ad-103">Skype for Business Online 中使用用户标识和标记作用域的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="3c7ad-103">Cmdlets in Skype for Business Online that use a user identity and the tag scope</span></span>

 


<span data-ttu-id="3c7ad-104">**授权-Cs** cmdlet (用于向用户分配策略) 需要两个标识符： (identity 参数) 的用户标识和 PolicyName 参数 (的每用户策略的标识。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-104">The **Grant-Cs** cmdlets (used for assigning policies to users) require two identifiers: a user identity (the Identity parameter) and the identity of a per-user policy (the PolicyName parameter).</span></span> <span data-ttu-id="3c7ad-105">例如，若要向用户 Ken Myer 分配语音策略 RedmondVoicePolicy，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="3c7ad-105">For example, to assign the voice policy, RedmondVoicePolicy, to the user Ken Myer, you use the following command:</span></span>

    Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "RedmondVoicePolicy"

<span data-ttu-id="3c7ad-106">向用户分配策略时需要注意两个事项。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-106">There are two things to keep in mind when assigning policies to users.</span></span> <span data-ttu-id="3c7ad-107">首先，只能分配每个用户的策略。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-107">First, only per-user policies can be assigned.</span></span> <span data-ttu-id="3c7ad-108">不能将全局策略分配给用户。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-108">You cannot assign the global policy to a user.</span></span> <span data-ttu-id="3c7ad-109">例如，此命令将失败：</span><span class="sxs-lookup"><span data-stu-id="3c7ad-109">For example, this command will fail:</span></span>

    Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "global"

<span data-ttu-id="3c7ad-110">此命令失败，因为无需分配全局策略。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-110">This command fails because there is no need to assign the global policy.</span></span> <span data-ttu-id="3c7ad-111">如果想要使用全局策略管理用户，请确保不要为该用户分配每用户策略。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-111">If you want to manage a user by using the global policy, just be sure that you do not assign that user a per-user policy.</span></span> <span data-ttu-id="3c7ad-112">如果没有为用户分配每用户策略，则将通过使用全局策略自动管理该用户。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-112">If no per-user policy has been assigned to a user, the user will automatically be managed by using the global policy.</span></span>


> [!NOTE]  
> <span data-ttu-id="3c7ad-113">如果用户以前已分配了每用户策略，并且想要取消分配该策略，并且用户改为由全局策略管理的用户，该怎么办？</span><span class="sxs-lookup"><span data-stu-id="3c7ad-113">What if the user has previously been assigned a per-user policy, and you want to unassign that policy and have the user managed by the global policy instead?</span></span> <span data-ttu-id="3c7ad-114">在这种情况下，你将首先使用以下语法，该语法通过向该用户授予 null 策略来取消每用户策略：</span><span class="sxs-lookup"><span data-stu-id="3c7ad-114">In that case, you’ll first use the following syntax, which unassigns a per-user policy by granting that user a null policy:</span></span><BR><span data-ttu-id="3c7ad-115">Grant-CsVoicePolicy-身份 "Ken Myer"-PolicyName $Null</span><span class="sxs-lookup"><span data-stu-id="3c7ad-115">Grant-CsVoicePolicy –Identity "Ken Myer" –PolicyName $Null</span></span>



<span data-ttu-id="3c7ad-116">其次，请记住，每个用户的策略是在标记作用域创建的。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-116">Second, keep in mind that per-user policies are created at the tag scope.</span></span> <span data-ttu-id="3c7ad-117">但是，你可以在指定策略名称时省略标记 **前缀** 。</span><span class="sxs-lookup"><span data-stu-id="3c7ad-117">However, you can omit the tag **prefix** when specifying a policy name.</span></span> <span data-ttu-id="3c7ad-118">这两个命令相同：</span><span class="sxs-lookup"><span data-stu-id="3c7ad-118">These two commands are identical:</span></span>

    Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "tag:RedmondVoicePolicy"
    Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "RedmondVoicePolicy"

<span data-ttu-id="3c7ad-119">如果你想要返回所有基于用户的策略的标识 (或者至少，指定类型的所有每用户策略（如语音策略) ），请使用如下所示的命令：</span><span class="sxs-lookup"><span data-stu-id="3c7ad-119">If you would like to return the identities for all your per-user policies (or, at least, all the per-user policies of specified type, such as voice policies), use a command similar to this:</span></span>

    Get-CsVoicePolicy -Filter "tag:*"

<span data-ttu-id="3c7ad-120">以下 cmdlet 使用用户标识和标记作用域：</span><span class="sxs-lookup"><span data-stu-id="3c7ad-120">The following cmdlets make use of both a user Identity and the tag scope:</span></span>

  - <span data-ttu-id="3c7ad-121">[授权-Set-csclientpolicy](https://technet.microsoft.com/library/gg412942\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3c7ad-121">[Grant-CsClientPolicy](https://technet.microsoft.com/library/gg412942\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3c7ad-122">[Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3c7ad-122">[Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3c7ad-123">[Grant-CsDialPlan](https://technet.microsoft.com/library/gg398547\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3c7ad-123">[Grant-CsDialPlan](https://technet.microsoft.com/library/gg398547\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3c7ad-124">[授权-CsExternalAccessPolicy](https://technet.microsoft.com/library/gg425942\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3c7ad-124">[Grant-CsExternalAccessPolicy](https://technet.microsoft.com/library/gg425942\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3c7ad-125">[授权-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/gg412829\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3c7ad-125">[Grant-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/gg412829\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3c7ad-126">[授权-CsVoicePolicy](https://technet.microsoft.com/library/gg398828\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3c7ad-126">[Grant-CsVoicePolicy](https://technet.microsoft.com/library/gg398828\(v=ocs.15\))</span></span>

## <a name="see-also"></a><span data-ttu-id="3c7ad-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c7ad-127">See Also</span></span>


[<span data-ttu-id="3c7ad-128">Skype for Business Online 中的身份、范围和租户</span><span class="sxs-lookup"><span data-stu-id="3c7ad-128">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="3c7ad-129">[Lync Online Cmdlet](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3c7ad-129">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

