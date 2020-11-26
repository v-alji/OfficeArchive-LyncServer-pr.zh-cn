---
title: Lync Server 2013：测试 UCWA 会议
description: Lync Server 2013：测试 UCWA 会议。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing UCWA conferencing
ms:assetid: 62b3866a-0759-4b1f-99ec-5a68d6a74f00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727306(v=OCS.15)
ms:contentKeyID: 63969610
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37f88a683abb67d55211422fc4dcf45fc1d5c966
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439735"
---
# <a name="testing-ucwa-conferencing-in-lync-server-2013"></a><span data-ttu-id="daf8e-103">在 Lync Server 2013 中测试 UCWA 会议</span><span class="sxs-lookup"><span data-stu-id="daf8e-103">Testing UCWA conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="daf8e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="daf8e-104">

<span> </span></span></span>

<span data-ttu-id="daf8e-105">_**主题上次修改时间：** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="daf8e-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf8e-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="daf8e-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="daf8e-107">每天</span><span class="sxs-lookup"><span data-stu-id="daf8e-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf8e-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="daf8e-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="daf8e-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="daf8e-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf8e-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="daf8e-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="daf8e-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="daf8e-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="daf8e-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 <strong>CsUcwaConference</strong> cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="daf8e-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsUcwaConference</strong> cmdlet.</span></span> <span data-ttu-id="daf8e-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="daf8e-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsUcwaConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="daf8e-114">说明</span><span class="sxs-lookup"><span data-stu-id="daf8e-114">Description</span></span>

<span data-ttu-id="daf8e-115">**CsUcwaConference** cmdlet 验证一对测试用户是否可以使用统一通信 Web API (UCWA) 来安排、加入和召开联机会议。</span><span class="sxs-lookup"><span data-stu-id="daf8e-115">The **Test-CsUcwaConference** cmdlet verifies that a pair of test users can schedule, join, and then conduct an online conference using the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="daf8e-116">为此，cmdlet 使用 Lync Server web ticket 服务对这两个测试用户进行身份验证，并使用 Lync Server 注册它们。</span><span class="sxs-lookup"><span data-stu-id="daf8e-116">To do this, the cmdlet uses the Lync Server web ticket service to authenticate the two test users and register them with Lync Server.</span></span> <span data-ttu-id="daf8e-117">然后，该 cmdlet 使用组织者凭据启动会议，并邀请参与者加入会议。</span><span class="sxs-lookup"><span data-stu-id="daf8e-117">The cmdlet then starts a conference using the organizer credentials and invites the participant to join the meeting.</span></span> <span data-ttu-id="daf8e-118">加入会议后， **CsUcwaConference** cmdlet 验证用户是否可以执行诸如 exchange 即时消息和执行池之类的操作，然后断开会议并注销两个测试用户。</span><span class="sxs-lookup"><span data-stu-id="daf8e-118">After the meeting is joined, the **Test-CsUcwaConference** cmdlet verifies that the users can do such things as exchange instant message and conduct pools, then disconnects the conference and unregisters the two test users.</span></span> <span data-ttu-id="daf8e-119">计划的会议在测试完成后也会被删除。</span><span class="sxs-lookup"><span data-stu-id="daf8e-119">The scheduled conference will also be deleted when the test is finished.</span></span>

<span data-ttu-id="daf8e-120">**CsUcwaConference** cmdlet 还可用于确定匿名用户是否可以加入联机会议。</span><span class="sxs-lookup"><span data-stu-id="daf8e-120">The **Test-CsUcwaConference** cmdlet can also be used to determine whether anonymous users can join online conferences.</span></span>

<span data-ttu-id="daf8e-121">请注意，除非在该池中安装了 UCWA，否则不应针对 Microsoft Lync Server 2010 池运行 **CsUcwaConference** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="daf8e-121">Note that the **Test-CsUcwaConference** cmdlet should not be run against a Microsoft Lync Server 2010 pool unless UCWA was installed on that pool.</span></span> <span data-ttu-id="daf8e-122">如果 UCWA 尚未安装，则对 **CsUcwaConference** cmdlet 的调用将失败。</span><span class="sxs-lookup"><span data-stu-id="daf8e-122">If UCWA has not been installed then the call to the **Test-CsUcwaConference** cmdlet will fail.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="daf8e-123">运行测试</span><span class="sxs-lookup"><span data-stu-id="daf8e-123">Running the test</span></span>

<span data-ttu-id="daf8e-124">示例1中所示的命令验证一对测试用户是否可以参与 pool atl-cs-001.litwareinc.com 上的 UCWA 会议。</span><span class="sxs-lookup"><span data-stu-id="daf8e-124">The command shown in Example 1 verifies that a pair of test users can participate in an UCWA conference on the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="daf8e-125">请注意，如果尚未预定义一对 atl-cs-001.litwareinc.com 的运行状况监视配置测试用户，此命令将失败。</span><span class="sxs-lookup"><span data-stu-id="daf8e-125">Note that this command will fail if you have not predefined a pair of health monitoring configuration test users for atl-cs-001.litwareinc.com.</span></span>

    Test-CsUcwaConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="daf8e-126">示例2中所示的命令测试一对用户 (litwareinc \\ pilar 和 litwareinc \\ kenmyer) 参与 UCWA 会议的能力。</span><span class="sxs-lookup"><span data-stu-id="daf8e-126">The commands shown in Example 2 test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to participate in an UCWA conference.</span></span> <span data-ttu-id="daf8e-127">为此，示例中的第一个命令使用 Get-Credential cmdlet 创建 Windows PowerShell 命令行界面凭据对象，该对象包含用户 Pilar Ackerman 的名称和密码。</span><span class="sxs-lookup"><span data-stu-id="daf8e-127">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="daf8e-128"> (由于登录名 litwareinc \\ pilar 作为参数包含，因此 Windows PowerShell 凭据请求对话框仅要求管理员输入 Pilar Ackerman 帐户的密码。 ) 结果凭据对象将存储在名为 $cred 1 的变量中。</span><span class="sxs-lookup"><span data-stu-id="daf8e-128">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="daf8e-129">第二个命令执行相同操作，这一次返回 Ken Myer 帐户的凭据对象。</span><span class="sxs-lookup"><span data-stu-id="daf8e-129">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="daf8e-130">使用这两个凭据对象，示例中的第三个命令确定两个用户是否可以参与 UCWA 会议。</span><span class="sxs-lookup"><span data-stu-id="daf8e-130">With the two credential objects in hand, the third command in the example determines whether the two users can participate in an UCWA conference.</span></span> <span data-ttu-id="daf8e-131">若要运行此任务， **CsUcwaConference** cmdlet 与以下参数一起调用： TargetFqdn (注册机构池的 FQDN) ;OrganizerSipAddress (会议组织者的 SIP 地址) ;OrganizerCredential (包含此同一用户的凭据的 Windows PowerShell 对象) ;ParticipantSipAddress (其他测试用户) 的 SIP 地址;和 ParticipantCredential (包含其他用户) 凭据的 Windows PowerShell 命令行界面对象。</span><span class="sxs-lookup"><span data-stu-id="daf8e-131">To run this task, the **Test-CsUcwaConference** cmdlet is called, together with the following parameters: TargetFqdn (the FQDN of the Registrar pool); OrganizerSipAddress (the SIP address for the meeting organizer); OrganizerCredential (the Windows PowerShell object that contains the credentials for this same user); ParticipantSipAddress (the SIP address for the other test user); and ParticipantCredential (the Windows PowerShell command-line interface object that contains the credentials for the other user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    Test-CsUcwaConference -TargetFqdn atl-cs-001.litwareinc.com -OrganizerSipAddress "sip:pilar@litwareinc.com" -OrganizerCredential $cred1 -ParticipantSipAddress "sip:kenmyer@litwareinc.com" -ParticipantCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="daf8e-132">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="daf8e-132">Determining success or failure</span></span>

<span data-ttu-id="daf8e-133">如果会议配置正确，你将收到类似于此的输出，结果属性标记为 " **成功"：**</span><span class="sxs-lookup"><span data-stu-id="daf8e-133">If conferencing is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="daf8e-134">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="daf8e-134">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="daf8e-135">目标 Uri： https://LyncTest-LyncTest。</span><span class="sxs-lookup"><span data-stu-id="daf8e-135">Target Uri : https:// LyncTest-SE.LyncTest.SelfHost.Corp.</span></span>

<span data-ttu-id="daf8e-136">Microsoft.com:443/CertProv/CertProvisiongService.svc</span><span class="sxs-lookup"><span data-stu-id="daf8e-136">Microsoft.com:443/CertProv/CertProvisiongService.svc</span></span>

<span data-ttu-id="daf8e-137">结果：成功</span><span class="sxs-lookup"><span data-stu-id="daf8e-137">Result : Success</span></span>

<span data-ttu-id="daf8e-138">延迟：00：00：14.9862716</span><span class="sxs-lookup"><span data-stu-id="daf8e-138">Latency : 00:00:14.9862716</span></span>

<span data-ttu-id="daf8e-139">错误消息：</span><span class="sxs-lookup"><span data-stu-id="daf8e-139">Error Message :</span></span>

<span data-ttu-id="daf8e-140">自检</span><span class="sxs-lookup"><span data-stu-id="daf8e-140">Diagnosis :</span></span>

<span data-ttu-id="daf8e-141">如果指定用户无法使用会议，则结果将显示为 " **失败**"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="daf8e-141">If the specified users can't use conferencing, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="daf8e-142">警告：无法读取给定的完全限定的注册机构端口号</span><span class="sxs-lookup"><span data-stu-id="daf8e-142">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="daf8e-143"> (FQDN) 的域名。</span><span class="sxs-lookup"><span data-stu-id="daf8e-143">domain name (FQDN).</span></span> <span data-ttu-id="daf8e-144">使用默认注册器端口号。</span><span class="sxs-lookup"><span data-stu-id="daf8e-144">Using default Registrar port number.</span></span> <span data-ttu-id="daf8e-145">除了</span><span class="sxs-lookup"><span data-stu-id="daf8e-145">Exception:</span></span>

<span data-ttu-id="daf8e-146">InvalidOperationException：在拓扑中找不到匹配的群集。</span><span class="sxs-lookup"><span data-stu-id="daf8e-146">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="daf8e-147">看</span><span class="sxs-lookup"><span data-stu-id="daf8e-147">at</span></span>

<span data-ttu-id="daf8e-148">SipSyntheticTransaction. TryRetri 的 SyntheticTransactions</span><span class="sxs-lookup"><span data-stu-id="daf8e-148">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="daf8e-149">eveRegistrarPortFromTopology (Int32& registrarPortNumber) </span><span class="sxs-lookup"><span data-stu-id="daf8e-149">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="daf8e-150">Test-CsUcwaConference：没有分配测试用户</span><span class="sxs-lookup"><span data-stu-id="daf8e-150">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="daf8e-151">\[LyncTest.SelfHost.Corp.Microsoft.com \] 。</span><span class="sxs-lookup"><span data-stu-id="daf8e-151">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="daf8e-152">验证测试用户配置。</span><span class="sxs-lookup"><span data-stu-id="daf8e-152">Verify test user configuration.</span></span>

<span data-ttu-id="daf8e-153">在第1行：1个字符：1</span><span class="sxs-lookup"><span data-stu-id="daf8e-153">At line:1 char:1</span></span>

<span data-ttu-id="daf8e-154">\+ Test-CsUcwaConference-TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="daf8e-154">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="daf8e-155">\+ CategoryInfo： ResourceUnavailable： (： ) \[ Test-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="daf8e-155">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="daf8e-156">, InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="daf8e-156">, InvalidOperationException</span></span>

<span data-ttu-id="daf8e-157">\+ FullyQualifiedErrorId： NotFoundTestUsers、</span><span class="sxs-lookup"><span data-stu-id="daf8e-157">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="daf8e-158">eticTransactions.TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="daf8e-158">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="daf8e-159">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="daf8e-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="daf8e-160">下面是 **测试 CsUcwaConference** 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="daf8e-160">Here are some common reasons why **Test-CsUcwaConference** might fail:</span></span>

  - <span data-ttu-id="daf8e-161">提供的参数值不正确。</span><span class="sxs-lookup"><span data-stu-id="daf8e-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="daf8e-162">如果使用，则必须正确配置可选参数，否则测试将失败。</span><span class="sxs-lookup"><span data-stu-id="daf8e-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="daf8e-163">重新运行不带可选参数的命令，并查看是否成功。</span><span class="sxs-lookup"><span data-stu-id="daf8e-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="daf8e-164">召开会议的能力取决于已分配给组织会议的用户的会议策略 (**CsUcwaConference** cmdlet 一样，即 "sender" ) 的情况。</span><span class="sxs-lookup"><span data-stu-id="daf8e-164">The ability to conduct a conference depends on the conferencing policy that has been assigned to the user who organized the conference (in the case of the **Test-CsUcwaConference** cmdlet, that is the "sender").</span></span> <span data-ttu-id="daf8e-165">如果不允许组织者在其会议中包含协作活动 (例如，如果其会议策略将 EnableDataCollaboration 属性设置为 False) 则 **CsUcwaConference** cmdlet 将失败。</span><span class="sxs-lookup"><span data-stu-id="daf8e-165">If the organizer is not allowed to include collaborative activities in his or her meeting (for example, if his or her conferencing policy has the EnableDataCollaboration property set to False) then the **Test-CsUcwaConference** cmdlet will fail.</span></span>

  - <span data-ttu-id="daf8e-166">如果边缘服务器配置错误或尚未部署，此命令将失败。</span><span class="sxs-lookup"><span data-stu-id="daf8e-166">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="daf8e-167">另请参阅</span><span class="sxs-lookup"><span data-stu-id="daf8e-167">See Also</span></span>


[<span data-ttu-id="daf8e-168">Test-CsASConference</span><span class="sxs-lookup"><span data-stu-id="daf8e-168">Test-CsASConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsASConference)  
[<span data-ttu-id="daf8e-169">Test-CsDataConference</span><span class="sxs-lookup"><span data-stu-id="daf8e-169">Test-CsDataConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsDataConference)  
[<span data-ttu-id="daf8e-170">Test-CsAVConference</span><span class="sxs-lookup"><span data-stu-id="daf8e-170">Test-CsAVConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference)  
  

<span data-ttu-id="daf8e-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="daf8e-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

