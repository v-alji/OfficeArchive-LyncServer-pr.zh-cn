---
title: Lync Server 2013：配置 Lync Server 以使用统一联系人存储
description: Lync Server 2013：将 Lync Server 配置为使用统一联系人存储。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Lync Server 2013 to use the unified contact store
ms:assetid: 6aa17ae3-764e-4986-a900-85a3cdb8c1fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688083(v=OCS.15)
ms:contentKeyID: 49733680
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6905d2e393fec36fe5db3e40ee20087c0cca0991
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432959"
---
# <a name="configuring-microsoft-lync-server-2013-to-use-the-unified-contact-store"></a><span data-ttu-id="8af38-103">将 Microsoft Lync Server 2013 配置为使用统一联系人存储</span><span class="sxs-lookup"><span data-stu-id="8af38-103">Configuring Microsoft Lync Server 2013 to use the unified contact store</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8af38-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8af38-104">

<span> </span></span></span>

<span data-ttu-id="8af38-105">_**主题上次修改时间：** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="8af38-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="8af38-106">"统一联系人存储" 使用户能够维护单个联系人列表，然后让这些联系人在多个应用程序中可用，包括 Microsoft Lync 2013、Microsoft Outlook 2013 和 Microsoft Outlook Web App 2013。</span><span class="sxs-lookup"><span data-stu-id="8af38-106">The unified contact store enables users to maintain a single contacts list and then have those contacts available in multiple applications, including Microsoft Lync 2013, Microsoft Outlook 2013, and Microsoft Outlook Web App 2013.</span></span> <span data-ttu-id="8af38-107">为用户启用统一联系人存储时，用户的联系人不存储在 Microsoft Lync Server 2013 中，然后使用 SIP 协议进行检索。</span><span class="sxs-lookup"><span data-stu-id="8af38-107">When you enable the unified contact store for a user that user's contacts are not stored in Microsoft Lync Server 2013 and then retrieved using the SIP protocol.</span></span> <span data-ttu-id="8af38-108">相反，他/她的联系人存储在 Microsoft Exchange Server 2013 中，并且通过使用 Exchange Web 服务进行检索。</span><span class="sxs-lookup"><span data-stu-id="8af38-108">Instead, his or her contacts are stored in Microsoft Exchange Server 2013 and are retrieved by using Exchange Web Services.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8af38-109">从技术上讲，联系人信息存储在用户的 Exchange 2013 邮箱中找到的一对文件夹中。</span><span class="sxs-lookup"><span data-stu-id="8af38-109">Technically, contact information is stored in a pair of folders found in the user's Exchange 2013 mailbox.</span></span> <span data-ttu-id="8af38-110">联系人本身存储在名为 "Lync 联系人" 的文件夹中，这些联系人对最终用户可见;有关联系人的元数据存储在对最终用户不可见的子文件夹中。</span><span class="sxs-lookup"><span data-stu-id="8af38-110">The contacts themselves are stored in a folder named Lync Contacts which is visible to end users; metadata about the contacts are stored in a subfolder that is not visible to end users.</span></span>



</div>

<div>

## <a name="enabling-the-unified-contact-store-for-a-user"></a><span data-ttu-id="8af38-111">为用户启用统一的联系人存储库</span><span class="sxs-lookup"><span data-stu-id="8af38-111">Enabling the Unified Contact Store for a User</span></span>

<span data-ttu-id="8af38-112">如果你已在 Lync Server 2013 和 Exchange 2013 之间配置了服务器到服务器身份验证，则你还启用了统一联系人存储的使用;不需要额外的服务器配置。</span><span class="sxs-lookup"><span data-stu-id="8af38-112">If you have already configured server-to-server authentication between Lync Server 2013 and Exchange 2013 then you have also enabled the use of the unified contact store; no additional server configuration is required.</span></span> <span data-ttu-id="8af38-113">但是，若要将用户的联系人移至统一的联系人存储库，则需要执行额外的用户帐户配置。</span><span class="sxs-lookup"><span data-stu-id="8af38-113">However, additional user account configuration is required in order to move a user's contacts into the unified contact store.</span></span> <span data-ttu-id="8af38-114">默认情况下，用户联系人保留在 Lync Server 中，而不是在统一联系人存储中。</span><span class="sxs-lookup"><span data-stu-id="8af38-114">By default, user contacts are kept in Lync Server and not in the unified contact store.</span></span>

<span data-ttu-id="8af38-115">通过使用 Lync Server 用户服务策略管理对统一联系人存储的访问。</span><span class="sxs-lookup"><span data-stu-id="8af38-115">Access to the unified contact store is managed by using Lync Server user services policies.</span></span> <span data-ttu-id="8af38-116">用户服务器策略只具有一个属性 (UcsAllowed)；此属性用于确定存储用户联系人的位置。</span><span class="sxs-lookup"><span data-stu-id="8af38-116">User server policies have only a single property (UcsAllowed); this property is used to determine the location where a user's contacts are stored.</span></span> <span data-ttu-id="8af38-117">如果用户由用户服务策略管理，其中 UcsAllowed 已设置为 True ($True) 则用户的联系人将存储在统一联系人存储中。</span><span class="sxs-lookup"><span data-stu-id="8af38-117">If a user is managed by a user services policy where UcsAllowed has been set to True ($True) then the user's contacts will be stored in the unified contact store.</span></span> <span data-ttu-id="8af38-118">如果用户由用户服务策略管理，其中 UcsAllowed 已设置为 False ($False) 那么他/她的联系人将存储在 Lync Server 中。</span><span class="sxs-lookup"><span data-stu-id="8af38-118">If the user is managed by a user services policy where UcsAllowed has been set to False ($False) then his or her contacts will be stored in Lync Server.</span></span>

<span data-ttu-id="8af38-119">安装 Lync Server 2013 时，将同时安装单个用户服务策略 (在全局范围内配置) 。</span><span class="sxs-lookup"><span data-stu-id="8af38-119">When you install Lync Server 2013 a single user services policy (configured at the global scope) is installed as well.</span></span> <span data-ttu-id="8af38-120">此策略中的 UcsAllowed 值将设置为 True，这意味着在默认情况下，用户联系人将存储在统一联系人存储中（假设已部署和配置它）。</span><span class="sxs-lookup"><span data-stu-id="8af38-120">The UcsAllowed value in this policy is set to True, meaning that, by default, user contacts will be stored in the unified contact store (assuming this has been deployed and configured).</span></span> <span data-ttu-id="8af38-121">若要将所有用户联系人迁移到统一联系人存储，根本不必执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="8af38-121">If you want to migrate all of your user contacts to the unified contact store you do not have to do anything at all.</span></span>

<span data-ttu-id="8af38-122">如果您不想将所有联系人都迁移到统一联系人存储，您可以通过在全局策略中将 UcsAllowed 属性设置为 False 来对所有用户禁用统一联系人存储：</span><span class="sxs-lookup"><span data-stu-id="8af38-122">If you would prefer not to migrate all your contacts to the unified contact store you can disable the unified contact store for all users by setting the UcsAllowed property in the global policy to False:</span></span>

    Set-CsUserServicesPolicy -Identity global -UcsAllowed $False

<span data-ttu-id="8af38-123">在全局策略中禁用统一联系人存储后，您可以创建允许使用统一联系人存储的基于用户的策略;这允许你让某些用户在 "统一联系人" 存储中保留其联系人，而其他用户继续在 Lync Server 中保留其联系人。</span><span class="sxs-lookup"><span data-stu-id="8af38-123">After you have disabled the unified contact store in the global policy you can then create a per-user policy that enables the use of the unified contact store; this allows you to have some users keep their contacts in the unified contact store while other users continue to keep their contacts in Lync Server.</span></span> <span data-ttu-id="8af38-124">可通过使用与以下命令类似的命令来创建每用户的用户服务策略：</span><span class="sxs-lookup"><span data-stu-id="8af38-124">You can create a per-user user services policy by using a command similar to this:</span></span>

    New-CsUserServicesPolicy -Identity "AllowUnifiedContactStore" -UcsAllowed $True

<span data-ttu-id="8af38-p107">在创建新的策略后，您必须将此策略分配给应有权访问统一的联系人存储库的任何用户。可通过使用与以下内容类似的命令来将每用户策略分配给用户：</span><span class="sxs-lookup"><span data-stu-id="8af38-p107">After you have created the new policy you must then assign that policy to any user who should have access to the unified contact store. Per-user policies can be assigned to users by using commands similar to this:</span></span>

    Grant-CsUserServicesPolicy -Identity "Ken Myer" -PolicyName "AllowUnifiedContactStore"

<span data-ttu-id="8af38-127">分配策略后，Lync 服务器将开始将用户的联系人迁移到 "统一联系人存储"。</span><span class="sxs-lookup"><span data-stu-id="8af38-127">After the policy has been assigned Lync Server will begin to migrate the user's contacts to the unified contact store.</span></span> <span data-ttu-id="8af38-128">完成迁移后，用户将在 Exchange 中存储其联系人，而不是 Lync Server。</span><span class="sxs-lookup"><span data-stu-id="8af38-128">After migration is complete, the user will then have his or her contacts stored in Exchange rather than Lync Server.</span></span> <span data-ttu-id="8af38-129">如果用户在迁移完成时登录到 Lync 2013，则会出现一个消息框，系统将要求用户注销 Lync，然后重新登录以完成该过程。</span><span class="sxs-lookup"><span data-stu-id="8af38-129">If the user happens to be logged on to Lync 2013 at the time migration completes, a message box will appear and he or she will be asked to log off of Lync and then log back on in order to finalize the process.</span></span> <span data-ttu-id="8af38-130">如果未向用户分配此每用户策略，则用户的联系人不会存储到统一联系人存储中。</span><span class="sxs-lookup"><span data-stu-id="8af38-130">Users who have not been assigned this per-user policy will not have their contacts migrated to the unified contact store.</span></span> <span data-ttu-id="8af38-131">这是因为这些用户受全局策略管理，而全局策略中已禁止使用统一联系人存储。</span><span class="sxs-lookup"><span data-stu-id="8af38-131">That’s because those users are being managed by the global policy, and use of the unified contact store has been disabled in the global policy.</span></span>

<span data-ttu-id="8af38-132">你可以通过在 Lync Server Management Shell 中运行 [CsUnifiedContactStore](https://docs.microsoft.com/powershell/module/skype/Test-CsUnifiedContactStore) cmdlet 来验证用户的联系人是否已成功迁移到统一联系人存储：</span><span class="sxs-lookup"><span data-stu-id="8af38-132">You can verify that a user's contacts have successfully been migrated to the unified contact store by running the [Test-CsUnifiedContactStore](https://docs.microsoft.com/powershell/module/skype/Test-CsUnifiedContactStore) cmdlet from within the Lync Server Management Shell:</span></span>

    Test-CsUnifiedContactStore -UserSipAddress "sip:kenmyer@litwareinc.com" -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="8af38-133">如果 Test-CsUnifiedContactStore 成功，则表示已将用户 sip:kenmyer@litwareinc.com 的联系人迁移到统一的联系人存储库中。</span><span class="sxs-lookup"><span data-stu-id="8af38-133">If Test-CsUnifiedContactStore succeeds that means that the contacts for the user sip:kenmyer@litwareinc.com have been migrated to the unified contact store.</span></span>

</div>

<div>

## <a name="rolling-back-the-unified-contact-store"></a><span data-ttu-id="8af38-134">回滚统一的联系人存储库</span><span class="sxs-lookup"><span data-stu-id="8af38-134">Rolling Back the Unified Contact Store</span></span>

<span data-ttu-id="8af38-135">如果需要从 "统一联系人存储" 中删除用户的联系人 (例如，如果用户需要在 Microsoft Lync Server 2010 上 rehomed，因此无法再使用 "统一联系人存储") 必须执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="8af38-135">If you need to remove a user's contacts from the unified contact store (for example, if the user needs to be rehomed on Microsoft Lync Server 2010 and thus can no longer use the unified contact store) you must do two things.</span></span> <span data-ttu-id="8af38-136">首先，您必须为用户分配一个新的用户服务策略，此策略禁止将联系人存储在统一的联系人存储库中。</span><span class="sxs-lookup"><span data-stu-id="8af38-136">First, you must assign the user a new user services policy, one that prohibits storing contacts in the unified contact store.</span></span> <span data-ttu-id="8af38-137"> (即，UcsAllowed 属性已设置为 $False 的策略。 ) 如果你没有这样的策略，则可以使用类似如下的命令创建一个策略：</span><span class="sxs-lookup"><span data-stu-id="8af38-137">(That is, a policy where the UcsAllowed property has been set to $False.) If you do not have such a policy you can create one using a command similar to this:</span></span>

    New-CsUserServicesPolicy -Identity NoUnifiedContactStore -UcsAllowed $False

<span data-ttu-id="8af38-138">然后，可通过使用与以下内容类似的命令分配此新的每用户策略 (NoUnifiedContactStore)：</span><span class="sxs-lookup"><span data-stu-id="8af38-138">You can then assign this new per-user policy (NoUnifiedContactStore) by using a command like this:</span></span>

    Grant-CsUserServicesPolicy -Identity "Ken Myer" -PolicyName NoUnifiedContactStore

<span data-ttu-id="8af38-139">上面的命令将新策略分配给用户 Ken Myer，并且还阻止将 Ken 的联系人迁移到统一的联系人存储库中。</span><span class="sxs-lookup"><span data-stu-id="8af38-139">The preceding command assigns the new policy to the user Ken Myer, and also prevents Ken's contacts from being migrated to the unified contact store.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8af38-140">在某些情况下，只需取消分配用户的当前用户服务策略，即可获得相同的网络效果。</span><span class="sxs-lookup"><span data-stu-id="8af38-140">In some cases you can achieve the same net effect by simply unassigning the user's current user services policy.</span></span> <span data-ttu-id="8af38-141">例如，假定 Ken Myer 具有启用统一的联系人存储库的每用户用户服务策略，但您的全局策略禁止使用统一的联系人存储库。</span><span class="sxs-lookup"><span data-stu-id="8af38-141">For example, suppose Ken Myer has a per-user user services policy the enables the unified contact store, but your global policy prohibits the use of the unified contact store.</span></span> <span data-ttu-id="8af38-142">在这种情况下，您可以取消分配 Ken 的每用户服务策略。</span><span class="sxs-lookup"><span data-stu-id="8af38-142">In that case, you could unassign Ken's per-user services policy.</span></span> <span data-ttu-id="8af38-143">在执行此操作后，Ken 将自动由全局策略管理，因此他将不再能够访问统一的联系人存储库。</span><span class="sxs-lookup"><span data-stu-id="8af38-143">When you do that, Ken will automatically be managed by the global policy, and thus will no longer have access to the unified contact store.</span></span><BR><span data-ttu-id="8af38-144">若要取消分配以前分配的每用户策略，请使用前面所示的相同命令，但这次将 PolicyName 参数设置为 null 值：</span><span class="sxs-lookup"><span data-stu-id="8af38-144">To unassign a previously-assigned per-user policy, use the same command as shown before, but this time set the PolicyName parameter to a null value:</span></span><BR><span data-ttu-id="8af38-145">Grant-CsUserServicesPolicy –Identity "Ken Myer" –PolicyName $Null</span><span class="sxs-lookup"><span data-stu-id="8af38-145">Grant-CsUserServicesPolicy –Identity "Ken Myer" –PolicyName $Null</span></span>



</div>

<span data-ttu-id="8af38-146">在使用统一的联系人存储库时，请务必记住术语“阻止将 Ken 的联系人迁移到统一的联系人存储库中”。</span><span class="sxs-lookup"><span data-stu-id="8af38-146">The terminology "prevents Ken's contacts from being migrated to the unified contact store" is important to keep in mind when working with the unified contact store.</span></span> <span data-ttu-id="8af38-147">仅为 Ken 分配一个新的用户服务策略并不会将其联系人从统一的联系人存储库中移出。</span><span class="sxs-lookup"><span data-stu-id="8af38-147">Simply assigning Ken a new user services policy will not move his contacts out of the unified contact store.</span></span> <span data-ttu-id="8af38-148">当用户登录到 Lync Server 2013 时，系统会检查用户的用户服务策略，以查看其联系人是否应保留在 "统一联系人" 存储中。</span><span class="sxs-lookup"><span data-stu-id="8af38-148">When a user logs on to Lync Server 2013, the system checks the user's user services policy to see whether his or her contacts should be kept in the unified contact store.</span></span> <span data-ttu-id="8af38-149">如果回答为“是”（即，在 UcsAllowed 属性设置为 $True 的情况下），则这些联系人将被迁移到统一的联系人存储库中（假定这些联系人尚未包含在统一的联系人存储库中）。</span><span class="sxs-lookup"><span data-stu-id="8af38-149">If the answer is yes (that is, if the UcsAllowed property is set to $True) then those contacts will be migrated to the unified contact store (assuming that those contacts are not already in the unified contact store).</span></span> <span data-ttu-id="8af38-150">如果答案为 "否"，则 Lync Server 只会忽略用户的联系人并转到其下一个任务。</span><span class="sxs-lookup"><span data-stu-id="8af38-150">If the answer is no, then Lync Server simply ignores the user's contacts and moves on to its next task.</span></span> <span data-ttu-id="8af38-151">这意味着 Lync Server 不会自动将用户的联系人从 "统一联系人存储" 移出，无论 UcsAllowed 属性的值如何。</span><span class="sxs-lookup"><span data-stu-id="8af38-151">That means that Lync Server will not automatically move a user's contacts from out of the unified contact store, regardless of the value of the UcsAllowed property.</span></span>

<span data-ttu-id="8af38-152">这还意味着，在为用户分配新的用户服务策略之后，必须运行 [CsUcsRollback](https://docs.microsoft.com/powershell/module/skype/Invoke-CsUcsRollback) cmdlet，以便将用户的联系人从 Exchange 2013 移出并返回到 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="8af38-152">That also means that, after assigning the user a new user services policy, you must then run the [Invoke-CsUcsRollback](https://docs.microsoft.com/powershell/module/skype/Invoke-CsUcsRollback) cmdlet in order to move the user's contacts out of Exchange 2013 and back to Lync Server 2013.</span></span> <span data-ttu-id="8af38-153">例如，在为 Ken Myer 分配一个新的用户服务策略后，可使用以下命令将用户的联系人从统一的联系人存储库中移出：</span><span class="sxs-lookup"><span data-stu-id="8af38-153">For example, after assigning Ken Myer a new user services policy you can then move his contacts out of the unified contact store by using the following command:</span></span>

    Invoke-CsUcsRollback -Identity "Ken Myer"

<span data-ttu-id="8af38-154">如果更改用户服务策略但不运行 Invoke-CsUcsRollback cmdlet，则不会从统一的联系人存储库中删除 Ken 的联系人。</span><span class="sxs-lookup"><span data-stu-id="8af38-154">If you change the user services policy but do not run the Invoke-CsUcsRollback cmdlet Ken's contacts will not be removed from the unified contact store.</span></span> <span data-ttu-id="8af38-155">如果运行 Invoke-CsUcsRollback 但不更改 Ken Myer 的用户服务策略，会出现什么情况？</span><span class="sxs-lookup"><span data-stu-id="8af38-155">What if you run Invoke-CsUcsRollback but do not change Ken Myer's user services policy?</span></span> <span data-ttu-id="8af38-156">在此情况下，会暂时从统一的联系人存储库中删除 Ken 的联系人。</span><span class="sxs-lookup"><span data-stu-id="8af38-156">In that case, Ken's contacts will be temporarily removed from the unified contact store.</span></span> <span data-ttu-id="8af38-157">请务必记住此删除是暂时性的这一事实。</span><span class="sxs-lookup"><span data-stu-id="8af38-157">The fact that this removal is temporary is important to keep in mind.</span></span> <span data-ttu-id="8af38-158">从 "统一联系人存储" 删除 Ken 联系人后，Lync Server 2013 将等待7天，然后检查哪些用户服务策略已分配给 Ken。</span><span class="sxs-lookup"><span data-stu-id="8af38-158">After Ken's contacts have been removed from the unified contact store, Lync Server 2013 will wait 7 days and then check to see which user services policy has been assigned to Ken.</span></span> <span data-ttu-id="8af38-159">如果仍为 Ken 分配了允许使用统一的联系人存储库的策略，则其联系人将被自动移回联系人存储库中。</span><span class="sxs-lookup"><span data-stu-id="8af38-159">If Ken is still assigned a policy that enables the user of the unified contact store, then his contacts will automatically be moved back to into the contact store.</span></span> <span data-ttu-id="8af38-160">若要从统一的联系人存储库中永久性删除联系人，您必须更改用户服务策略并运行 Invoke-CsUcsRollback cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8af38-160">To permanently remove contacts from the unified contact store you must change the user services policy in addition to running the Invoke-CsUcsRollback cmdlet.</span></span>

<span data-ttu-id="8af38-p114">由于存在可影响迁移的大量变量，因而很难估计将帐户完全迁移到统一存储库会用多长时间。但一般说来，迁移不会立即生效：即使迁移的联系人数量不多，完成迁移也可能要用 10 分钟或更长时间。</span><span class="sxs-lookup"><span data-stu-id="8af38-p114">Due to the large number of variables that can affect migration, it is difficult to estimate how long it will take before accounts are fully migrated to the unified contact store. As a general rule, however, migration does not take effect immediately: even when migrating a small number of contacts it might take 10 minutes or more before the move is complete.</span></span>

<span data-ttu-id="8af38-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8af38-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

