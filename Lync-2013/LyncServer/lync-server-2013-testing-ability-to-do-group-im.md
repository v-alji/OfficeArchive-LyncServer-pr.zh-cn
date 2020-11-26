---
title: Lync Server 2013：测试待办事项组 IM 的能力
description: Lync Server 2013：测试是否能够进行群组 IM。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to do group IM
ms:assetid: ca5545bc-51ac-490f-b96b-917bb742ad04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743839(v=OCS.15)
ms:contentKeyID: 63969652
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f6988a0c1a7ba569f7b4da098ae741beab5e14fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441100"
---
# <a name="testing-ability-to-do-group-im-in-lync-server-2013"></a><span data-ttu-id="d3dee-103">在 Lync Server 2013 中进行群组 IM 测试的功能</span><span class="sxs-lookup"><span data-stu-id="d3dee-103">Testing ability to do group IM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3dee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3dee-104">

<span> </span></span></span>

<span data-ttu-id="d3dee-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="d3dee-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3dee-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="d3dee-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="d3dee-107">每天</span><span class="sxs-lookup"><span data-stu-id="d3dee-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3dee-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="d3dee-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="d3dee-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d3dee-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3dee-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="d3dee-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="d3dee-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="d3dee-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="d3dee-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsGroupIM cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="d3dee-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupIM cmdlet.</span></span> <span data-ttu-id="d3dee-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d3dee-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="d3dee-114">说明</span><span class="sxs-lookup"><span data-stu-id="d3dee-114">Description</span></span>

<span data-ttu-id="d3dee-115">Test-CsGroupIM cmdlet 验证组织中的用户是否可以执行群组即时消息会话。</span><span class="sxs-lookup"><span data-stu-id="d3dee-115">The Test-CsGroupIM cmdlet verifies that users in your organization can conduct group instant messaging sessions.</span></span> <span data-ttu-id="d3dee-116">运行 Test CsGroupIM 时，cmdlet 会尝试登录一对 Lync Server 的测试用户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-116">When you run Test-CsGroupIM, the cmdlet attempts to sign in a pair of test users to Lync Server.</span></span> <span data-ttu-id="d3dee-117">如果成功，Test-CsGroupIM 使用第一个测试用户创建新会议，然后邀请第二位用户加入会议。</span><span class="sxs-lookup"><span data-stu-id="d3dee-117">If successful, Test-CsGroupIM creates a new conference using the first test user, then invites the second user to join the conference.</span></span> <span data-ttu-id="d3dee-118">在交换邮件之后，两个用户都将从系统断开连接。</span><span class="sxs-lookup"><span data-stu-id="d3dee-118">After an exchange of messages, both users are then disconnected from the system.</span></span> <span data-ttu-id="d3dee-119">请注意，所有这些操作都不需要用户交互，并且不会影响任何实际用户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-119">Note that all of this happens without any user interaction, and without affecting any actual users.</span></span> <span data-ttu-id="d3dee-120">例如，假设测试帐户 sip:kenmyer@litwareinc.com 对应于具有真实 Lync 服务器帐户的真实用户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-120">For example, suppose that the test account sip:kenmyer@litwareinc.com corresponds to a real user who has a real Lync Server account.</span></span> <span data-ttu-id="d3dee-121">在这种情况下，将在不中断真正的 Ken Myer 的情况下执行测试。</span><span class="sxs-lookup"><span data-stu-id="d3dee-121">In that case, the test will be conducted without any disruption to the real Ken Myer.</span></span> <span data-ttu-id="d3dee-122">例如，即使 Ken Myer 测试帐户从系统注销，此人仍将保持登录状态。</span><span class="sxs-lookup"><span data-stu-id="d3dee-122">For example, even when the Ken Myer test account logs off from the system, Ken Myer the person will remain logged on.</span></span> <span data-ttu-id="d3dee-123">同样，真正的 Ken Myer 将不会收到加入会议的邀请。</span><span class="sxs-lookup"><span data-stu-id="d3dee-123">Likewise, the real Ken Myer won't receive an invitation to join the conference.</span></span> <span data-ttu-id="d3dee-124">该邀请将发送给并接受测试帐户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-124">That invitation will be sent to, and accepted by, the test account.</span></span>

<span data-ttu-id="d3dee-125">有关详细信息，请参阅 [CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="d3dee-125">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="d3dee-126">运行测试</span><span class="sxs-lookup"><span data-stu-id="d3dee-126">Running the test</span></span>

<span data-ttu-id="d3dee-127">可以使用一对预配置的测试帐户运行 Test-CsGroupIM cmdlet (参阅设置用于运行 Lync Server 测试的测试帐户) 或为 Lync Server 启用的任何两个用户的帐户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-127">The Test-CsGroupIM cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="d3dee-128">若要使用测试帐户运行此检查，只需指定正在测试的 Lync Server 池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d3dee-128">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="d3dee-129">例如：</span><span class="sxs-lookup"><span data-stu-id="d3dee-129">For example:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="d3dee-130">若要使用实际的用户帐户运行此检查，必须为每个帐户 (包含帐户名称和密码) 的对象创建两个 Lync Server Management Shell 凭据对象。</span><span class="sxs-lookup"><span data-stu-id="d3dee-130">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="d3dee-131">然后，当你调用 Test-CsGroupIM 时，你必须包含这些凭据对象和两个帐户的 SIP 地址：</span><span class="sxs-lookup"><span data-stu-id="d3dee-131">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsGroupIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsGroupIm -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="d3dee-132">有关详细信息，请参阅 [CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="d3dee-132">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="d3dee-133">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="d3dee-133">Determining Success or Failure</span></span>

<span data-ttu-id="d3dee-134">如果两个用户可以完成组即时消息会话，你将收到与以下内容类似的输出：结果属性标记为 **成功：**</span><span class="sxs-lookup"><span data-stu-id="d3dee-134">If the two users can complete a group instant messaging session, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="d3dee-135">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d3dee-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="d3dee-136">结果：成功</span><span class="sxs-lookup"><span data-stu-id="d3dee-136">Result : Success</span></span>

<span data-ttu-id="d3dee-137">延迟：00：00：06.3812203</span><span class="sxs-lookup"><span data-stu-id="d3dee-137">Latency : 00:00:06.3812203</span></span>

<span data-ttu-id="d3dee-138">时发生</span><span class="sxs-lookup"><span data-stu-id="d3dee-138">Error :</span></span>

<span data-ttu-id="d3dee-139">自检</span><span class="sxs-lookup"><span data-stu-id="d3dee-139">Diagnosis :</span></span>

<span data-ttu-id="d3dee-140">如果两个用户无法完成即时消息会话，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="d3dee-140">If the two users can't able to complete the instant messaging session, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="d3dee-141">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d3dee-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="d3dee-142">结果：失败</span><span class="sxs-lookup"><span data-stu-id="d3dee-142">Result : Failure</span></span>

<span data-ttu-id="d3dee-143">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="d3dee-143">Latency : 00:00:00</span></span>

<span data-ttu-id="d3dee-144">错误：404，未找到</span><span class="sxs-lookup"><span data-stu-id="d3dee-144">Error : 404, Not Found</span></span>

<span data-ttu-id="d3dee-145">诊断： ErrorCode = 4005，Source = atl-cs-001.litwareinc.com，</span><span class="sxs-lookup"><span data-stu-id="d3dee-145">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="d3dee-146">原因 = 没有为 SIP 启用目标 URI，或者没有为其启用目标 URI</span><span class="sxs-lookup"><span data-stu-id="d3dee-146">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="d3dee-147">并存.</span><span class="sxs-lookup"><span data-stu-id="d3dee-147">exist.</span></span>

<span data-ttu-id="d3dee-148">Microsoft DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="d3dee-148">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="d3dee-149">以前的输出表明测试失败的原因是至少有一个测试帐户无效，原因是帐户不存在或者用户尚未启用 Lync Server。</span><span class="sxs-lookup"><span data-stu-id="d3dee-149">The previous output states that the test failed because at least one of the test accounts was not valid, either because the account does not exist or because the user has not been enabled for Lync Server.</span></span> <span data-ttu-id="d3dee-150">你可以通过运行类似如下所示的命令来验证帐户是否存在以及是否已启用 nm-ocs-第14级帐户：</span><span class="sxs-lookup"><span data-stu-id="d3dee-150">You can verify the account exists, and whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to this:</span></span>

    "Ken Myer", "David Longmire" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="d3dee-151">如果 Test-CsGroupIM 失败，则可能需要重新运行测试，这一次包括 Verbose 参数：</span><span class="sxs-lookup"><span data-stu-id="d3dee-151">If Test-CsGroupIM fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="d3dee-152">当包含 Verbose 参数时，Test-CsGroupIM 将返回它在检查指定用户是否参与组即时消息会话的能力时尝试的每个操作的分步帐户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-152">When the Verbose parameter is included, Test-CsGroupIM will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in a group instant messaging sessions.</span></span> <span data-ttu-id="d3dee-153">例如，如果你的测试失败，并且你被告知一个或多个用户帐户无效，则可以使用 Verbose 参数重新运行测试并确定无效的用户帐户：</span><span class="sxs-lookup"><span data-stu-id="d3dee-153">For example, if your test fails and you are told that one or more of the user accounts is not valid, you can rerun the test using the Verbose parameter and determine which user account is not valid:</span></span>

<span data-ttu-id="d3dee-154">正在发送注册请求：</span><span class="sxs-lookup"><span data-stu-id="d3dee-154">Sending Registration request:</span></span>

 <span data-ttu-id="d3dee-155">目标 Fqdn = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d3dee-155">Target Fqdn      = atl-cs-001.litwareinc.com</span></span>

 <span data-ttu-id="d3dee-156">用户 SIP 地址 = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d3dee-156">User SIP Address = sip:kenmyer@litwareinc.com</span></span>

 <span data-ttu-id="d3dee-157">注册端口 = 5061</span><span class="sxs-lookup"><span data-stu-id="d3dee-157">Register Port    = 5061</span></span>

<span data-ttu-id="d3dee-158">已选择身份验证类型 "IWA"。</span><span class="sxs-lookup"><span data-stu-id="d3dee-158">Auth type 'IWA' is selected.</span></span>

<span data-ttu-id="d3dee-159">"登录被拒绝" 异常。</span><span class="sxs-lookup"><span data-stu-id="d3dee-159">An exception 'The log on was denied.</span></span> <span data-ttu-id="d3dee-160">检查是否正在使用正确的凭据，帐户是否处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="d3dee-160">Check that the correct credentials are being used and the account is active'</span></span>

<span data-ttu-id="d3dee-161">正如你所见，在此示例中，具有 SIP 地址 sip:kenmyer@litwareinc.com 的用户无法登录。</span><span class="sxs-lookup"><span data-stu-id="d3dee-161">As you can see, in this example the user who has the SIP address sip:kenmyer@litwareinc.com was not able to log on.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="d3dee-162">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="d3dee-162">Reasons why the test might have failed</span></span>

<span data-ttu-id="d3dee-163">下面是 Test-CsGroupIM 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="d3dee-163">Here are some common reasons why Test-CsGroupIM might fail:</span></span>

  - <span data-ttu-id="d3dee-164">您指定了一个不正确的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-164">You specified an incorrect user account.</span></span> <span data-ttu-id="d3dee-165">你可以通过运行类似如下所示的命令来验证用户帐户是否存在：</span><span class="sxs-lookup"><span data-stu-id="d3dee-165">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="d3dee-166">用户帐户有效，但当前没有为 Lync Server 启用该帐户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-166">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="d3dee-167">若要验证是否已启用 Lync Server 的用户帐户，请运行类似如下的命令：</span><span class="sxs-lookup"><span data-stu-id="d3dee-167">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
    <span data-ttu-id="d3dee-168">Get-CsUser "sip:kenmyer@litwareinc.com" |Select-Object 启用</span><span class="sxs-lookup"><span data-stu-id="d3dee-168">Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled</span></span>
    
    <span data-ttu-id="d3dee-169">如果 Enabled 属性设置为 False，则表示当前未对 Lync Server 启用用户。</span><span class="sxs-lookup"><span data-stu-id="d3dee-169">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="d3dee-170">即时消息服务可能不可用。</span><span class="sxs-lookup"><span data-stu-id="d3dee-170">The instant messaging service might not be available.</span></span> <span data-ttu-id="d3dee-171">使用 Lync Server，你可以配置系统，以便在无法访问存档数据库时即时消息不可用。</span><span class="sxs-lookup"><span data-stu-id="d3dee-171">With Lync Server, you can configure the system so that instant messaging is not available if the archiving database cannot be accessed.</span></span> <span data-ttu-id="d3dee-172">你可以通过运行如下所示的命令来验证该命令：</span><span class="sxs-lookup"><span data-stu-id="d3dee-172">You can verify that by running a command similar to the following:</span></span>
    
        Get-CsArchivingConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object BlockOnArchiveFailure
    
    <span data-ttu-id="d3dee-173">如果 BlockOnArchiveFailure 设置为 True，则应确定存档数据库是否可用。</span><span class="sxs-lookup"><span data-stu-id="d3dee-173">If BlockOnArchiveFailure is set to True, then you should determine whether or not the archiving database is available.</span></span> <span data-ttu-id="d3dee-174">你可以使用以下命令返回存档数据库的位置：</span><span class="sxs-lookup"><span data-stu-id="d3dee-174">You can return the locations of your archiving databases by using the following command:</span></span>
    
        Get-CsService -ArchivingDatabase

  - <span data-ttu-id="d3dee-175">存档服务器可能不可用。</span><span class="sxs-lookup"><span data-stu-id="d3dee-175">The Archiving Server might not be available.</span></span> <span data-ttu-id="d3dee-176">你可以使用以下命令检索存档服务器的 FQDN：</span><span class="sxs-lookup"><span data-stu-id="d3dee-176">You can retrieve the FQDN of your Archiving Servers by using this command:</span></span>
    
        Get-CsService -ArchivingServer
    
    <span data-ttu-id="d3dee-177">然后，你可以 ping 相应的服务器以验证其是否可用。</span><span class="sxs-lookup"><span data-stu-id="d3dee-177">You can then ping the appropriate server to verify that it is available.</span></span> <span data-ttu-id="d3dee-178">例如：</span><span class="sxs-lookup"><span data-stu-id="d3dee-178">For example:</span></span>
    
        ping atl-archiving-001.litwareinc.com

<span data-ttu-id="d3dee-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3dee-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

