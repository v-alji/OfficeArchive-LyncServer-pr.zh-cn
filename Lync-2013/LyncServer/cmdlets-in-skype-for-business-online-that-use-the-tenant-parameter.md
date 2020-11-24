---
title: Skype for Business Online 中使用租户参数的 cmdlet
description: Skype for Business Online 中使用租户参数的 cmdlet。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use the Tenant parameter
ms:assetid: e7fe7c12-fbe0-49c1-9e8c-eef6958f27d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362850(v=OCS.15)
ms:contentKeyID: 56558865
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff2b8053dd855a854fa26699770d3dafaa0dcbd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391906"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-the-tenant-parameter"></a><span data-ttu-id="d5824-103">Skype for Business Online 中使用租户参数的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d5824-103">Cmdlets in Skype for Business Online that use the Tenant parameter</span></span>

 


<span data-ttu-id="d5824-104">修改公共提供程序设置时，你始终需要提供租户标识;即使只有单个租户，也是如此。</span><span class="sxs-lookup"><span data-stu-id="d5824-104">When modifying your public provider settings, you always need to supply a Tenant identity; this is true even if you only have a single tenant.</span></span> <span data-ttu-id="d5824-105">例如，此命令将 Windows Live 设置为允许用户与之通信的唯一公共提供程序：</span><span class="sxs-lookup"><span data-stu-id="d5824-105">For example, this command sets Windows Live as the only public provider your users are allowed to communicate with:</span></span>

    Set-CsTenantPublicProvider -Tenant "bf19b7db-6960-41e5-a139-2aa373474354" -Provider "WindowsLive"

<span data-ttu-id="d5824-106">幸运的是，在每次运行其中一个 cmdlet 时，您无需键入租户 ID (例如 bf19b7db-6960-41e5-a139-2aa373474354) 。</span><span class="sxs-lookup"><span data-stu-id="d5824-106">Fortunately, you do not need to type the Tenant ID (for example, bf19b7db-6960-41e5-a139-2aa373474354) each time you run one of these cmdlets.</span></span> <span data-ttu-id="d5824-107">相反，你可以通过运行 [CsTenant](https://technet.microsoft.com/library/jj994044\(v=ocs.15\)) cmdlet 来检索租户 id，将租户 id 存储在一个变量中，然后在调用其他 cmdlet 之一时使用该变量。</span><span class="sxs-lookup"><span data-stu-id="d5824-107">Instead, you can retrieve the Tenant ID by running the [Get-CsTenant](https://technet.microsoft.com/library/jj994044\(v=ocs.15\)) cmdlet, storing the Tenant ID in a variable, and then using that variable when you call one of the other cmdlets.</span></span> <span data-ttu-id="d5824-108">例如：</span><span class="sxs-lookup"><span data-stu-id="d5824-108">For example:</span></span>

    $x = (Get-CsTenant).TenantId
    Set-CsTenantPublicProvider -Tenant $x -Provider "WindowsLive"

<span data-ttu-id="d5824-109">或者，你可以在单个命令中执行此操作，方法是检索租户 ID，然后将该值管道到 Set-CsTenantPublicProvider cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d5824-109">Alternatively, you can do this in a single command by retrieving the Tenant ID and then piping that value to the Set-CsTenantPublicProvider cmdlet:</span></span>

    Get-CsTenant | Select-Object TenantId | ForEach-Object {Set-CsTenantPublicProvider -Tenant $_.TenantId -Provider "WindowsLive"}

<span data-ttu-id="d5824-110">在调用 **CsTenant** cmdlet 时，无需指定租户 ID。</span><span class="sxs-lookup"><span data-stu-id="d5824-110">You do not need to specify the tenant ID when calling the **Get-CsTenant** cmdlet.</span></span> <span data-ttu-id="d5824-111">此命令将返回有关租户的信息：</span><span class="sxs-lookup"><span data-stu-id="d5824-111">This command returns information about your tenant:</span></span>

    Get-CsTenant

<span data-ttu-id="d5824-112">以下 cmdlet 接受租户标识。</span><span class="sxs-lookup"><span data-stu-id="d5824-112">The following cmdlets accept a tenant identity.</span></span> <span data-ttu-id="d5824-113">但是，在这些情况下，该参数是可选的，并且无需在调用 cmdlet 时输入。</span><span class="sxs-lookup"><span data-stu-id="d5824-113">However, in these cases, the parameter is optional and does not need to be entered when calling the cmdlet.</span></span> <span data-ttu-id="d5824-114">因此，Windows PowerShell 将根据您当前连接到的 Skype for business Online 租户有效地为您输入租户标识：</span><span class="sxs-lookup"><span data-stu-id="d5824-114">Instead, Windows PowerShell will effectively enter the tenant identity for you based on the Skype for Business Online tenant you are currently connected to:</span></span>

  - <span data-ttu-id="d5824-115">[Get-CsTenant](https://technet.microsoft.com/library/jj994044\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="d5824-115">[Get-CsTenant](https://technet.microsoft.com/library/jj994044\(v=ocs.15\))</span></span>

  - <span data-ttu-id="d5824-116">[Set-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994080\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="d5824-116">[Set-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994080\(v=ocs.15\))</span></span>

  - <span data-ttu-id="d5824-117">[Set-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994046\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="d5824-117">[Set-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994046\(v=ocs.15\))</span></span>

  - <span data-ttu-id="d5824-118">[Get-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994072\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="d5824-118">[Get-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994072\(v=ocs.15\))</span></span>

  - <span data-ttu-id="d5824-119">[Get-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994034\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="d5824-119">[Get-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994034\(v=ocs.15\))</span></span>

  - <span data-ttu-id="d5824-120">[Get-CsTenantLicensingConfiguration](https://technet.microsoft.com/library/dn362770\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="d5824-120">[Get-CsTenantLicensingConfiguration](https://technet.microsoft.com/library/dn362770\(v=ocs.15\))</span></span>

<span data-ttu-id="d5824-121">例如，可以使用以下命令调用 **CsTenantFederationConfiguration** cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d5824-121">For example, the **Get-CsTenantFederationConfiguration** cmdlet can be called by using this command:</span></span>

    Get-CsTenantFederationConfiguration

<span data-ttu-id="d5824-122">虽然不是必需的，但你可以在调用 Get-CsTenantFederationConfiguration 时包括租户参数：</span><span class="sxs-lookup"><span data-stu-id="d5824-122">Although not required, you can include the Tenant parameter when calling Get-CsTenantFederationConfiguration :</span></span>

    Get-CsTenantFederationConfiguration -Tenant "bf19b7db-6960-41e5-a139-2aa373474354"

## <a name="see-also"></a><span data-ttu-id="d5824-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5824-123">See Also</span></span>


[<span data-ttu-id="d5824-124">Skype for Business Online 中的身份、范围和租户</span><span class="sxs-lookup"><span data-stu-id="d5824-124">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="d5824-125">[Lync Online Cmdlet](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="d5824-125">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

