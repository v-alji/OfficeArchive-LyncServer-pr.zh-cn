---
title: Skype for Business Online 中仅使用全局范围的 cmdlet
description: Skype for Business Online 中仅使用全局范围的 cmdlet。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use only the global scope
ms:assetid: 0ffd3bc9-a6a1-4c2e-8d52-e599acc49d2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362771(v=OCS.15)
ms:contentKeyID: 56558800
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a2f59806128ceea825a4cdd966e85852b98079b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392061"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-only-the-global-scope"></a><span data-ttu-id="fb021-103">Skype for Business Online 中仅使用全局范围的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb021-103">Cmdlets in Skype for Business Online that use only the global scope</span></span>

 


<span data-ttu-id="fb021-104">许多 Skype for Business Online 设置仅在 *全局范围内* 可用。</span><span class="sxs-lookup"><span data-stu-id="fb021-104">A number of Skype for Business Online settings are available only at the *global scope*.</span></span> <span data-ttu-id="fb021-105">这意味着有一个设置集合，这些设置适用于分配给该租户的所有用户。</span><span class="sxs-lookup"><span data-stu-id="fb021-105">This means that there is a single collection of settings that applies to all the users who are assigned to that tenant.</span></span> <span data-ttu-id="fb021-106"> (每个租户都有其自己唯一的全局设置集合。 ) 当你使用限制为全局范围的 cmdlet 时，Identity 参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="fb021-106">(Each tenant has its own unique collection of global settings.) When you are using cmdlets that are limited to the global scope, the Identity parameter is optional.</span></span> <span data-ttu-id="fb021-107">例如，若要检索会议配置设置，您可以使用此命令：</span><span class="sxs-lookup"><span data-stu-id="fb021-107">For example, to retrieve meeting configuration settings, you can use this command:</span></span>

    Get-CsMeetingConfiguration -Identity "global"

<span data-ttu-id="fb021-108">或者，你可以省略 Identity 参数，而改为使用以下更简单的命令：</span><span class="sxs-lookup"><span data-stu-id="fb021-108">Alternatively, you can omit the Identity parameter and use this simpler command instead:</span></span>

    Get-CsMeetingConfiguration

<span data-ttu-id="fb021-109">由于只有一个全局会议配置设置集合，因此这两个命令将返回完全相同的信息。</span><span class="sxs-lookup"><span data-stu-id="fb021-109">Because there is only one global collection of meeting configuration settings, the two commands return the exact same information.</span></span> <span data-ttu-id="fb021-110">使用其中一个 **Set-Cs** cmdlet 时，也可以省略 Identity 参数。</span><span class="sxs-lookup"><span data-stu-id="fb021-110">The Identity parameter can also be omitted when using one of the **Set-Cs** cmdlets.</span></span> <span data-ttu-id="fb021-111">这两个命令相同：</span><span class="sxs-lookup"><span data-stu-id="fb021-111">These two commands are identical:</span></span>

    Set-CsMeetingConfiguration -Identity "global" -AdmitAnonymousUsersByDefault $False
    Set-CsMeetingConfiguration -AdmitAnonymousUsersByDefault $False

<span data-ttu-id="fb021-112">这两个命令是相同的，因为默认情况下，如果不包含 Identity 参数，Windows PowerShell 将修改全局集合。</span><span class="sxs-lookup"><span data-stu-id="fb021-112">The two commands are identical because, by default, Windows PowerShell will modify the global collection if you do not include the Identity parameter.</span></span>

<span data-ttu-id="fb021-113">以下 cmdlet 仅在全局范围内运行：</span><span class="sxs-lookup"><span data-stu-id="fb021-113">The following cmdlets operate only at the global scope:</span></span>

  - <span data-ttu-id="fb021-114">[CsImFilterConfiguration](https://technet.microsoft.com/library/gg398980\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-114">[Get-CsImFilterConfiguration](https://technet.microsoft.com/library/gg398980\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-115">[Get-CsMeetingConfiguration](https://technet.microsoft.com/library/gg425875\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-115">[Get-CsMeetingConfiguration](https://technet.microsoft.com/library/gg425875\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-116">[CsPrivacyConfiguration](https://technet.microsoft.com/library/gg413002\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-116">[Get-CsPrivacyConfiguration](https://technet.microsoft.com/library/gg413002\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-117">[Get-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994072\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-117">[Get-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994072\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-118">[Get-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994034\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-118">[Get-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994034\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-119">[Get-CsTenantLicensingConfiguration](https://technet.microsoft.com/library/dn362770\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-119">[Get-CsTenantLicensingConfiguration](https://technet.microsoft.com/library/dn362770\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-120">[Get-CsTenantPublicProvider](https://technet.microsoft.com/library/jj994016\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-120">[Get-CsTenantPublicProvider](https://technet.microsoft.com/library/jj994016\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-121">[Remove-CsVoicePolicy](https://technet.microsoft.com/library/gg398309\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-121">[Remove-CsVoicePolicy](https://technet.microsoft.com/library/gg398309\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-122">[Set-CsMeetingConfiguration](https://technet.microsoft.com/library/gg398648\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-122">[Set-CsMeetingConfiguration](https://technet.microsoft.com/library/gg398648\(v=ocs.15\))</span></span>

  - <span data-ttu-id="fb021-123">[Set-CsPrivacyConfiguration](https://technet.microsoft.com/library/gg398484\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-123">[Set-CsPrivacyConfiguration](https://technet.microsoft.com/library/gg398484\(v=ocs.15\))</span></span>

<span data-ttu-id="fb021-124">请注意， **CsVoicePolicy** cmdlet 是异常的一些内容。</span><span class="sxs-lookup"><span data-stu-id="fb021-124">Note that the **Remove-CsVoicePolicy** cmdlet is something of an anomaly.</span></span> <span data-ttu-id="fb021-125">首先，此 cmdlet 需要包含 Identity 参数：</span><span class="sxs-lookup"><span data-stu-id="fb021-125">First, this cmdlet does require you to include the Identity parameter:</span></span>

    Remove-CsVoicePolicy -Identity "global"

<span data-ttu-id="fb021-126">第二， **CsVoicePolicy** cmdlet 不会真正删除全局语音策略;Skype for business Online 不允许删除全局策略或配置设置。</span><span class="sxs-lookup"><span data-stu-id="fb021-126">Second, the **Remove-CsVoicePolicy** cmdlet does not actually delete the global voice policy; Skype for Business Online does not allow you to delete global policies or configuration settings.</span></span> <span data-ttu-id="fb021-127">Cmdlet 的用途是使你能够将全局语音策略中的所有属性重置为其默认值。</span><span class="sxs-lookup"><span data-stu-id="fb021-127">What the cmdlet does do is enable you to reset all the properties in the global voice policy to their default values.</span></span> <span data-ttu-id="fb021-128">例如，默认情况下，AllowCallForwarding 属性设置为 False。</span><span class="sxs-lookup"><span data-stu-id="fb021-128">For example, by default, the AllowCallForwarding property is set to False.</span></span> <span data-ttu-id="fb021-129">但是，AllowCallForwarding 可能已修改，值现在设置为 True。</span><span class="sxs-lookup"><span data-stu-id="fb021-129">However, AllowCallForwarding may have been modified, with the value now set to True.</span></span> <span data-ttu-id="fb021-130">当你运行 **CsVoicePolicy** cmdlet 时，AllowCallForwarding 属性将还原为其默认值： False。</span><span class="sxs-lookup"><span data-stu-id="fb021-130">When you run the **Remove-CsVoicePolicy** cmdlet, the AllowCallForwarding property will revert to its default value: False.</span></span> <span data-ttu-id="fb021-131">下表总结了此方案：</span><span class="sxs-lookup"><span data-stu-id="fb021-131">The following table summarizes this scenario:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb021-132">AllowCallForwarding 值</span><span class="sxs-lookup"><span data-stu-id="fb021-132">AllowCallForwarding Value</span></span></th>
<th><span data-ttu-id="fb021-133">使用场景</span><span class="sxs-lookup"><span data-stu-id="fb021-133">Scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb021-134">False</span><span class="sxs-lookup"><span data-stu-id="fb021-134">False</span></span></p></td>
<td><p><span data-ttu-id="fb021-135">默认值</span><span class="sxs-lookup"><span data-stu-id="fb021-135">Default value</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb021-136">True</span><span class="sxs-lookup"><span data-stu-id="fb021-136">True</span></span></p></td>
<td><p><span data-ttu-id="fb021-137">修改全局策略后</span><span class="sxs-lookup"><span data-stu-id="fb021-137">After the global policy has been modified</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb021-138">False</span><span class="sxs-lookup"><span data-stu-id="fb021-138">False</span></span></p></td>
<td><p><span data-ttu-id="fb021-139"><strong>CsVoicePolicy</strong> cmdlet 已运行后</span><span class="sxs-lookup"><span data-stu-id="fb021-139">After <strong>Remove-CsVoicePolicy</strong> cmdlet has been run</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="fb021-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb021-140">See Also</span></span>


[<span data-ttu-id="fb021-141">Skype for Business Online 中的身份、范围和租户</span><span class="sxs-lookup"><span data-stu-id="fb021-141">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="fb021-142">[Lync Online Cmdlet](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="fb021-142">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

