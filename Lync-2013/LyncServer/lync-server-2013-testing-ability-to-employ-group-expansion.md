---
title: Lync Server 2013：测试使用组扩展的能力
description: Lync Server 2013：测试是否可以使用组扩展。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to employ group expansion
ms:assetid: 9b0fc954-6f9c-411a-ab32-94ebabc42de2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743836(v=OCS.15)
ms:contentKeyID: 63969634
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6267bc2099fc420c5c57e1ef80f4bf4491334938
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441107"
---
# <a name="testing-ability-to-employ-group-expansion-in-lync-server-2013"></a><span data-ttu-id="c3f8d-103">测试在 Lync Server 2013 中使用组扩展的能力</span><span class="sxs-lookup"><span data-stu-id="c3f8d-103">Testing ability to employ group expansion in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3f8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3f8d-104">

<span> </span></span></span>

<span data-ttu-id="c3f8d-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="c3f8d-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3f8d-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="c3f8d-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c3f8d-107">每天</span><span class="sxs-lookup"><span data-stu-id="c3f8d-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3f8d-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="c3f8d-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c3f8d-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c3f8d-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3f8d-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="c3f8d-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c3f8d-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c3f8d-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsGroupExpansion cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupExpansion cmdlet.</span></span> <span data-ttu-id="c3f8d-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupExpansion&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c3f8d-114">说明</span><span class="sxs-lookup"><span data-stu-id="c3f8d-114">Description</span></span>

<span data-ttu-id="c3f8d-115">Test-CsGroupExpansion cmdlet 使你可以确定组扩展是否在你的组织内工作。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-115">The Test-CsGroupExpansion cmdlet lets you determine whether group expansion is working within your organization.</span></span> <span data-ttu-id="c3f8d-116">启用组扩展后，用户将通讯组配置为联系人。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-116">When group expansion is enabled, users configure distribution groups as a contact.</span></span> <span data-ttu-id="c3f8d-117">这意味着，这些用户可以通过将邮件寻址到组而不是该组的单个成员来向所有组成员发送相同的即时消息。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-117">That means that those users can then send the same instant message to all the group members by addressing the message to the group instead of to individual members of that group.</span></span> <span data-ttu-id="c3f8d-118">组扩展使你能够快速轻松地查看所有组成员及其当前状态。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-118">Group expansion enables you to quickly and easily view all the group members and their current status.</span></span>

<span data-ttu-id="c3f8d-119">使用 Test-CsGroupExpansion cmdlet，使用组的电子邮件地址指定 Active Directory 通讯组。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-119">With the Test-CsGroupExpansion cmdlet, you specify an Active Directory distribution group by using the group’s email address.</span></span> <span data-ttu-id="c3f8d-120">然后，Test-CsGroupExpansion 使用组扩展检索组成员身份，并将检索到的列表与您提供的组电子邮件地址的成员身份进行比较。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-120">Test-CsGroupExpansion then uses group expansion to retrieve the group membership and compare the retrieved list to the membership of the group email address that you supplied.</span></span> <span data-ttu-id="c3f8d-121">如果两个列表匹配，则组扩展正常工作。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-121">If the two lists match, then group expansion is working correctly.</span></span> <span data-ttu-id="c3f8d-122">请注意，你可以通过两种方式测试组扩展：测试服务本身或测试关联的 web 服务。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-122">Note that you can test group expansion in two ways: by testing the service itself or by testing the associated web service.</span></span>

<span data-ttu-id="c3f8d-123">有关详细信息，请参阅 [CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-123">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c3f8d-124">运行测试</span><span class="sxs-lookup"><span data-stu-id="c3f8d-124">Running the test</span></span>

<span data-ttu-id="c3f8d-125">可以使用预配置的测试帐户运行 Test-CsGroupExpansion cmdlet (请参阅设置用于运行 Lync Server 测试的测试帐户) 或为 Lync Server 启用的任何用户的帐户。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-125">The Test-CsGroupExpansion cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who was enabled for Lync Server.</span></span> <span data-ttu-id="c3f8d-126">若要使用测试帐户运行此检查，只需指定要测试的 Lync Server 池的 FQDN 和有效通讯组的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the email address for a valid distribution group.</span></span> <span data-ttu-id="c3f8d-127">例如：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-127">For example:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com"

<span data-ttu-id="c3f8d-128">若要使用实际用户帐户运行此检查，必须首先创建一个 Lync Server 凭据对象，其中包含帐户名称和密码。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-128">To run this check using an actual user account, you must first create a Lync Server credentials object that contains the account name and password.</span></span> <span data-ttu-id="c3f8d-129">然后，在系统调用 Test-CsGroupExpansion 时，必须包含该凭据对象和分配给该帐户的 SIP 地址：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-129">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsGroupExpansion:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="c3f8d-130">有关详细信息，请参阅 [CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-130">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c3f8d-131">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="c3f8d-131">Determining success or failure</span></span>

<span data-ttu-id="c3f8d-132">如果指定的用户可以使用组扩展，则会收到与以下内容类似的输出：结果属性标记为 **成功：**</span><span class="sxs-lookup"><span data-stu-id="c3f8d-132">If the specified user can use group expansion, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="c3f8d-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="c3f8d-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="c3f8d-134">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c3f8d-134">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c3f8d-135">结果：成功</span><span class="sxs-lookup"><span data-stu-id="c3f8d-135">Result : Success</span></span>

<span data-ttu-id="c3f8d-136">延迟：00：00：01.1234976</span><span class="sxs-lookup"><span data-stu-id="c3f8d-136">Latency : 00:00:01.1234976</span></span>

<span data-ttu-id="c3f8d-137">时发生</span><span class="sxs-lookup"><span data-stu-id="c3f8d-137">Error :</span></span>

<span data-ttu-id="c3f8d-138">自检</span><span class="sxs-lookup"><span data-stu-id="c3f8d-138">Diagnosis :</span></span>

<span data-ttu-id="c3f8d-139">如果指定用户不能使用组扩展，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-139">If the specified user can't use group expansion, then the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="c3f8d-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="c3f8d-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="c3f8d-141">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c3f8d-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c3f8d-142">结果：失败</span><span class="sxs-lookup"><span data-stu-id="c3f8d-142">Result : Failure</span></span>

<span data-ttu-id="c3f8d-143">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="c3f8d-143">Latency : 00:00:00</span></span>

<span data-ttu-id="c3f8d-144">时发生</span><span class="sxs-lookup"><span data-stu-id="c3f8d-144">Error :</span></span>

<span data-ttu-id="c3f8d-145">自检</span><span class="sxs-lookup"><span data-stu-id="c3f8d-145">Diagnosis :</span></span>

<span data-ttu-id="c3f8d-146">Test-CsGroupExpansion：终结点无法注册。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-146">Test-CsGroupExpansion : The endpoint was unable to register.</span></span> <span data-ttu-id="c3f8d-147">有关特定原因，请参阅错误代码。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-147">See the ErrorCode for specific reason.</span></span>

<span data-ttu-id="c3f8d-148">以前的输出表明测试失败的原因是指定的用户无法向 Lync 服务器注册。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-148">The previous output states that the test failed because the specified user was unable to register with Lync Server.</span></span> <span data-ttu-id="c3f8d-149">如果测试帐户不存在或尚未为 Lync Server 启用，则通常会发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-149">This will typically occur if the test account does not exist or has not enabled for Lync Server.</span></span> <span data-ttu-id="c3f8d-150">你可以通过运行类似如下所示的命令来验证帐户是否存在，并确定是否已启用 nm-ocs-第14级帐户：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-150">You can verify that the account exists, and determine whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to the following:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="c3f8d-151">如果 Test-CsGroupExpansion 失败，则可能需要重新运行测试，这一次包括 Verbose 参数：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-151">If Test-CsGroupExpansion fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -Verbose

<span data-ttu-id="c3f8d-152">当包含详细参数时 Test-CsGroupExpansion 将返回它在检查指定用户登录到 Lync Server 的能力时尝试的每个操作的分步帐户。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-152">When the Verbose parameter is included Test-CsGroupExpansion will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="c3f8d-153">例如，以下输出表明找不到指定的通讯组：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-153">For example, this output indicates that the specified distribution group couldn't be found:</span></span>

<span data-ttu-id="c3f8d-154">正在尝试获取 web 票证。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-154">Trying to get web ticket.</span></span>

<span data-ttu-id="c3f8d-155">Web 服务 url： https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="c3f8d-155">Web Service url : https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="c3f8d-156">使用 NTLM/Kerb auth。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-156">Using NTLM/Kerb auth.</span></span>

<span data-ttu-id="c3f8d-157">GetWebTicketActivity 已完成。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-157">GetWebTicketActivity completed.</span></span>

<span data-ttu-id="c3f8d-158">已开始 "VerifyDistributionList" 活动。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-158">'VerifyDistributionList' activity started.</span></span>

<span data-ttu-id="c3f8d-159">DLX Web 服务响应状态为： NotFound。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-159">DLX Web Service Response Status is: NotFound.</span></span>

<span data-ttu-id="c3f8d-160">"VerifyDistributionList" 活动在 "0.2597923" 秒内完成。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-160">'VerifyDistributionList' activity completed in '0.2597923' secs.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c3f8d-161">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="c3f8d-161">Reasons why the test might have failed</span></span>

<span data-ttu-id="c3f8d-162">下面是 Test-CsGroupExpansion 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-162">Here are some common reasons why Test-CsGroupExpansion might fail:</span></span>

  - <span data-ttu-id="c3f8d-163">您指定了无效的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-163">You specified an invalid user account.</span></span> <span data-ttu-id="c3f8d-164">你可以通过运行类似如下所示的命令来验证用户帐户是否存在：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-164">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="c3f8d-165">用户帐户有效，但当前没有为 Lync Server 启用该帐户。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-165">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="c3f8d-166">若要验证是否已启用 Lync Server 的用户帐户，请运行类似如下的命令：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-166">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="c3f8d-167">如果 Enabled 属性设置为 False，则表示当前未对 Lync Server 启用用户。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-167">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="c3f8d-168">组扩展可能已禁用。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-168">Group expansion might be disabled.</span></span> <span data-ttu-id="c3f8d-169">可以关闭组扩展。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-169">It is possible to turn off group expansion.</span></span> <span data-ttu-id="c3f8d-170">如果组扩展已禁用，则 Test-CsGroupExpansion cmdlet 将失败。</span><span class="sxs-lookup"><span data-stu-id="c3f8d-170">If group expansion was disabled then the Test-CsGroupExpansion cmdlet will fail.</span></span> <span data-ttu-id="c3f8d-171">若要确定是否已启用组扩展，请使用类似下面的命令：</span><span class="sxs-lookup"><span data-stu-id="c3f8d-171">To determine whether group expansion is enabled, use a command similar to this:</span></span>
    
        Get-CsWebServiceConfiguration | Select-Object Identity, EnableGroupExpansion

<span data-ttu-id="c3f8d-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3f8d-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

