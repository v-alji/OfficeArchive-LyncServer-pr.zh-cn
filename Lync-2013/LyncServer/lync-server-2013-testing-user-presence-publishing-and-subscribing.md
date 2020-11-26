---
title: Lync Server 2013：测试用户状态发布和订阅
description: Lync Server 2013：测试用户状态发布和订阅。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user presence publishing and subscribing
ms:assetid: 27694c71-8e63-4aa4-b49f-fa06ccb81949
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743832(v=OCS.15)
ms:contentKeyID: 63969587
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90913f270fbd034ca4d2ea7cf3b93c255fc95c66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439709"
---
# <a name="testing-user-presence-publishing-and-subscribing-in-lync-server-2013"></a><span data-ttu-id="98406-103">在 Lync Server 2013 中测试用户状态发布和订阅</span><span class="sxs-lookup"><span data-stu-id="98406-103">Testing user presence publishing and subscribing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98406-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98406-104">

<span> </span></span></span>

<span data-ttu-id="98406-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="98406-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98406-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="98406-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="98406-107">每天</span><span class="sxs-lookup"><span data-stu-id="98406-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98406-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="98406-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="98406-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="98406-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98406-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="98406-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="98406-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="98406-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="98406-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsPresence cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="98406-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPresence cmdlet.</span></span> <span data-ttu-id="98406-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="98406-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPresence&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="98406-114">说明</span><span class="sxs-lookup"><span data-stu-id="98406-114">Description</span></span>

<span data-ttu-id="98406-115">Test-CsPresence 用于确定一对测试用户是否可以登录 Lync 服务器，然后交换联机状态信息。</span><span class="sxs-lookup"><span data-stu-id="98406-115">Test-CsPresence is used to determine whether a pair of test users can log on to Lync Server and then exchange presence information.</span></span> <span data-ttu-id="98406-116">为此，cmdlet 首先将两个用户记录到系统。</span><span class="sxs-lookup"><span data-stu-id="98406-116">To do this, the cmdlet first logs the two users on to the system.</span></span> <span data-ttu-id="98406-117">如果两次登录均成功，则第一个测试用户将要求接收来自第二个用户的状态信息。</span><span class="sxs-lookup"><span data-stu-id="98406-117">If both logons succeed, the first test user then asks to receive presence information from the second user.</span></span> <span data-ttu-id="98406-118">第二个用户发布此信息，并 Test-CsPresence 验证信息是否已成功传输到第一个用户。</span><span class="sxs-lookup"><span data-stu-id="98406-118">The second user publishes this information, and Test-CsPresence verifies that the information was successfully transmitted to the first user.</span></span> <span data-ttu-id="98406-119">在交换状态信息后，两个测试用户随后从 Lync Server 中注销。</span><span class="sxs-lookup"><span data-stu-id="98406-119">After the exchange of presence information, the two test users are then logged off from Lync Server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="98406-120">运行测试</span><span class="sxs-lookup"><span data-stu-id="98406-120">Running the test</span></span>

<span data-ttu-id="98406-121">可以使用一对预配置的测试帐户运行 Test-CsPresence cmdlet (参阅设置用于运行 Lync Server 测试的测试帐户) 或为 Lync Server 启用的任何两个用户的帐户。</span><span class="sxs-lookup"><span data-stu-id="98406-121">The Test-CsPresence cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="98406-122">若要使用测试帐户运行此检查，只需指定正在测试的 Lync Server 池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="98406-122">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="98406-123">例如：</span><span class="sxs-lookup"><span data-stu-id="98406-123">For example:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="98406-124">若要使用实际的用户帐户运行此检查，必须为每个帐户 (包含帐户名称和密码) 的对象创建两个 Windows PowerShell 凭据对象。</span><span class="sxs-lookup"><span data-stu-id="98406-124">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="98406-125">然后，当你调用 Test-CsPresence 时，你必须包含这些凭据对象和两个帐户的 SIP 地址：</span><span class="sxs-lookup"><span data-stu-id="98406-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsPresence:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -PublisherSipAddress "sip:kenmyer@litwareinc.com" -PublisherCredential $credential1 -SubscriberSipAddress "sip:davidlongmire@litwareinc.com" -SubscriberCredential $credential2

<span data-ttu-id="98406-126">有关详细信息，请参阅 [CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="98406-126">For more information, see the Help documentation for the [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="98406-127">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="98406-127">Determining success or failure</span></span>

<span data-ttu-id="98406-128">如果指定的用户可以交换状态信息，则将收到类似于此的输出，并将 Result 属性标记为 **成功：**</span><span class="sxs-lookup"><span data-stu-id="98406-128">If the specified users can exchange presence information, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="98406-129">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="98406-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="98406-130">结果：成功</span><span class="sxs-lookup"><span data-stu-id="98406-130">Result : Success</span></span>

<span data-ttu-id="98406-131">延迟：00：00：06.3280315</span><span class="sxs-lookup"><span data-stu-id="98406-131">Latency : 00:00:06.3280315</span></span>

<span data-ttu-id="98406-132">时发生</span><span class="sxs-lookup"><span data-stu-id="98406-132">Error :</span></span>

<span data-ttu-id="98406-133">自检</span><span class="sxs-lookup"><span data-stu-id="98406-133">Diagnosis :</span></span>

<span data-ttu-id="98406-134">如果两个用户不能交换状态信息，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="98406-134">If the two users can't exchange presence information, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="98406-135">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="98406-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="98406-136">结果：失败</span><span class="sxs-lookup"><span data-stu-id="98406-136">Result : Failure</span></span>

<span data-ttu-id="98406-137">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="98406-137">Latency : 00:00:00</span></span>

<span data-ttu-id="98406-138">错误：404，未找到</span><span class="sxs-lookup"><span data-stu-id="98406-138">Error : 404, Not Found</span></span>

<span data-ttu-id="98406-139">诊断： ErrorCode = 4005，Source = atl-cs-001.litwareinc.com，</span><span class="sxs-lookup"><span data-stu-id="98406-139">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="98406-140">原因 = 没有为 SIP 启用目标 URI，或者没有为其启用目标 URI</span><span class="sxs-lookup"><span data-stu-id="98406-140">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="98406-141">并存.</span><span class="sxs-lookup"><span data-stu-id="98406-141">exist.</span></span>

<span data-ttu-id="98406-142">Microsoft DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="98406-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="98406-143">例如，以前的输出表明，由于两个用户帐户中的至少一个帐户无效，测试失败：帐户不存在或尚未为 Lync Server 启用。</span><span class="sxs-lookup"><span data-stu-id="98406-143">For example, the previous output states that the test failed because at least one of the two user accounts is not valid: either the account does not exist or it has not been enabled for Lync Server.</span></span> <span data-ttu-id="98406-144">你可以通过运行如下命令来验证帐户是否存在，并确定是否为 Lync Server 启用了这些帐户：</span><span class="sxs-lookup"><span data-stu-id="98406-144">You can verify that the accounts exist, and determine whether they are enabled for Lync Server, by running a command similar to this:</span></span>

    "sip:kenmyer@litwareinc.com", "sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="98406-145">如果 Test-CsPresence 失败，则可能需要重新运行测试，这一次包括 Verbose 参数：</span><span class="sxs-lookup"><span data-stu-id="98406-145">If Test-CsPresence fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="98406-146">当包含详细参数时，Test-CsPresence 将返回它在检查指定用户登录到 Lync Server 的能力时尝试的每个操作的分步帐户。</span><span class="sxs-lookup"><span data-stu-id="98406-146">When the Verbose parameter is included, Test-CsPresence will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="98406-147">例如：</span><span class="sxs-lookup"><span data-stu-id="98406-147">For example:</span></span>

<span data-ttu-id="98406-148">注册请求遇到未知情况</span><span class="sxs-lookup"><span data-stu-id="98406-148">Registration Request hit against Unknown</span></span>

<span data-ttu-id="98406-149">"Register" 活动在 "0.0345791" 秒内完成。</span><span class="sxs-lookup"><span data-stu-id="98406-149">'Register' activity completed in '0.0345791' secs.</span></span>

<span data-ttu-id="98406-150">已开始 "SelfSubscribeActivity" 活动。</span><span class="sxs-lookup"><span data-stu-id="98406-150">'SelfSubscribeActivity' activity started.</span></span>

<span data-ttu-id="98406-151">"SelfSubscribeActivity" 活动在 "0.0041174" 秒内完成。</span><span class="sxs-lookup"><span data-stu-id="98406-151">'SelfSubscribeActivity' activity completed in '0.0041174' secs.</span></span>

<span data-ttu-id="98406-152">已开始 "SubscribePresence" 活动。</span><span class="sxs-lookup"><span data-stu-id="98406-152">'SubscribePresence' activity started.</span></span>

<span data-ttu-id="98406-153">"SubscribePresence" 活动在 "0.0038764" 秒内完成。</span><span class="sxs-lookup"><span data-stu-id="98406-153">'SubscribePresence' activity completed in '0.0038764' secs.</span></span>

<span data-ttu-id="98406-154">已开始 "PublishPresence" 活动。</span><span class="sxs-lookup"><span data-stu-id="98406-154">'PublishPresence' activity started.</span></span>

<span data-ttu-id="98406-155">在25秒内未收到异常的 "联机状态" 通知。 "</span><span class="sxs-lookup"><span data-stu-id="98406-155">An exception 'Presence notification is not received within 25 secs.'</span></span> <span data-ttu-id="98406-156">ruing 工作流 STPresenceWorkflow 执行失败。</span><span class="sxs-lookup"><span data-stu-id="98406-156">occurred ruing Workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STPresenceWorkflow execution.</span></span>

<span data-ttu-id="98406-157">在25秒内未收到状态通知这一事实可能表明网络问题阻止信息被交换。</span><span class="sxs-lookup"><span data-stu-id="98406-157">The fact that the presence notification was not received within 25 seconds might indicate that network issues are preventing information from being exchanged.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="98406-158">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="98406-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="98406-159">下面是 Test-CsPresence 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="98406-159">Here are some common reasons why Test-CsPresence might fail:</span></span>

  - <span data-ttu-id="98406-160">您指定了一个不正确的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="98406-160">You specified an incorrect user account.</span></span> <span data-ttu-id="98406-161">你可以通过运行类似如下所示的命令来验证用户帐户是否存在：</span><span class="sxs-lookup"><span data-stu-id="98406-161">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="98406-162">用户帐户有效，但当前没有为 Lync Server 启用该帐户。</span><span class="sxs-lookup"><span data-stu-id="98406-162">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="98406-163">若要验证是否已启用 Lync Server 的用户帐户，请运行类似如下的命令：</span><span class="sxs-lookup"><span data-stu-id="98406-163">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="98406-164">如果 Enabled 属性设置为 False，表示当前未对 Lync Server 启用用户。</span><span class="sxs-lookup"><span data-stu-id="98406-164">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="98406-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98406-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

