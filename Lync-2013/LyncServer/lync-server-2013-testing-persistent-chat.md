---
title: Lync Server 2013：测试持久聊天
description: Lync Server 2013：测试持久聊天。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing persistent chat
ms:assetid: d351b6f2-bc31-42e0-9e8d-c347713d6b4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727313(v=OCS.15)
ms:contentKeyID: 63969651
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8b1dc4eef1870f1287dacdc1852ab1e24edd169
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440995"
---
# <a name="testing-persistent-chat-in-lync-server-2013"></a><span data-ttu-id="609b1-103">在 Lync Server 2013 中测试持久聊天</span><span class="sxs-lookup"><span data-stu-id="609b1-103">Testing persistent chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="609b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="609b1-104">

<span> </span></span></span>

<span data-ttu-id="609b1-105">_**主题上次修改时间：** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="609b1-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="609b1-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="609b1-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="609b1-107">每天</span><span class="sxs-lookup"><span data-stu-id="609b1-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="609b1-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="609b1-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="609b1-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="609b1-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="609b1-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="609b1-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="609b1-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="609b1-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="609b1-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 <strong>CsPersistentChatMessage</strong> cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="609b1-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsPersistentChatMessage</strong> cmdlet.</span></span> <span data-ttu-id="609b1-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="609b1-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPersistentChatMessage&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="609b1-114">说明</span><span class="sxs-lookup"><span data-stu-id="609b1-114">Description</span></span>

<span data-ttu-id="609b1-115">**CsPersistentChatMessage** cmdlet 验证一对测试用户是否可以使用持久聊天服务交换消息。</span><span class="sxs-lookup"><span data-stu-id="609b1-115">The **Test-CsPersistentChatMessage** cmdlet verifies that a pair of test users can exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="609b1-116">为此，该 cmdlet 将两个用户记录到 Lync Server 2013，将用户连接到持久聊天室，交换一对消息，然后退出聊天室并注销两个用户。</span><span class="sxs-lookup"><span data-stu-id="609b1-116">To do this, the cmdlet logs the two users on to Lync Server 2013, connects the users to a persistent Chat room, exchanges a pair of messages, then exits the chat room and logs off the two users.</span></span> <span data-ttu-id="609b1-117">请注意，如果你没有创建任何聊天室，或者没有为两个测试用户帐户分配可访问永久聊天服务的持久聊天策略，则对此 cmdlet 的调用将失败。</span><span class="sxs-lookup"><span data-stu-id="609b1-117">Note that calls to this cmdlet will fail if you have not created any chat rooms or if the two test user accounts are not assigned a Persistent Chat policy that gives them access to the Persistent Chat service.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="609b1-118">运行测试</span><span class="sxs-lookup"><span data-stu-id="609b1-118">Running the test</span></span>

<span data-ttu-id="609b1-119">以下示例中所示的命令将测试一对用户 (litwareinc \\ pilar 和 litwareinc \\ kenmyer) 登录 Lync Server 2013，然后使用持久聊天服务交换邮件。</span><span class="sxs-lookup"><span data-stu-id="609b1-119">The commands shown in the following example test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to log on to Lync Server 2013 and then exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="609b1-120">为此，示例中的第一个命令使用 **Get 凭据** Cmdlet 创建 Windows PowerShell 命令行界面凭据对象，该对象包含用户 Pilar Ackerman 的名称和密码。</span><span class="sxs-lookup"><span data-stu-id="609b1-120">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="609b1-121"> (由于登录名 litwareinc \\ pilar 作为参数包含，因此 Windows PowerShell 凭据请求对话框仅要求管理员输入 Pilar Ackerman 帐户的密码。 ) 结果凭据对象将存储在名为 $cred 1 的变量中。</span><span class="sxs-lookup"><span data-stu-id="609b1-121">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="609b1-122">第二个命令执行相同操作，这一次返回 Ken Myer 帐户的凭据对象。</span><span class="sxs-lookup"><span data-stu-id="609b1-122">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="609b1-123">使用凭据对象，第三个命令确定这两个用户是否可以使用持久聊天来登录 Lync Server 2013 和 exchange 邮件。</span><span class="sxs-lookup"><span data-stu-id="609b1-123">With the credential objects in hand, the third command determines whether these two users can log on to Lync Server 2013 and exchange messages using Persistent Chat.</span></span> <span data-ttu-id="609b1-124">若要执行此任务，请使用以下参数调用 **CsPersistentChatMessage** Cmdlet： TargetFqdn (注册机构池的 FQDN) ;SenderSipAddress (第一个测试用户) 的 SIP 地址;SenderCredential (包含此同一用户的凭据的 Windows PowerShell 对象) ;ReceiverSipAddress (其他测试用户) 的 SIP 地址;和 ReceiverCredential (包含其他测试用户) 凭据的 Windows PowerShell 对象。</span><span class="sxs-lookup"><span data-stu-id="609b1-124">To perform this task, the **Test-CsPersistentChatMessage** cmdlet is called using the following parameters: TargetFqdn (the FQDN of the Registrar pool); SenderSipAddress (the SIP address for the first test user); SenderCredential (the Windows PowerShell object that contains the credentials for this same user); ReceiverSipAddress (the SIP address for the other test user); and ReceiverCredential (the Windows PowerShell object that contains the credentials for the other test user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsPersistentChatMessage -TargetFqdn atl-persistentchat-001.litwareinc.com -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $cred1 -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -ReceiverCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="609b1-125">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="609b1-125">Determining success or failure</span></span>

<span data-ttu-id="609b1-126">如果指定用户具有有效的位置策略，则会收到与此类似的输出，结果属性标记为 **成功**：</span><span class="sxs-lookup"><span data-stu-id="609b1-126">If the specified user has a valid location policy, then you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="609b1-127">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="609b1-127">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="609b1-128">结果：成功</span><span class="sxs-lookup"><span data-stu-id="609b1-128">Result : Success</span></span>

<span data-ttu-id="609b1-129">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="609b1-129">Latency : 00:00:00</span></span>

<span data-ttu-id="609b1-130">错误消息：</span><span class="sxs-lookup"><span data-stu-id="609b1-130">Error Message :</span></span>

<span data-ttu-id="609b1-131">自检</span><span class="sxs-lookup"><span data-stu-id="609b1-131">Diagnosis :</span></span>

<span data-ttu-id="609b1-132">如果指定用户无法使用持久聊天服务交换邮件，则结果将显示为 " **失败**"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="609b1-132">If the specified users can't exchange messages using the Persistent Chat service, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="609b1-133">警告：无法读取给定的完全限定的注册机构端口号</span><span class="sxs-lookup"><span data-stu-id="609b1-133">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="609b1-134"> (FQDN) 的域名。</span><span class="sxs-lookup"><span data-stu-id="609b1-134">domain name (FQDN).</span></span> <span data-ttu-id="609b1-135">使用默认注册器端口号。</span><span class="sxs-lookup"><span data-stu-id="609b1-135">Using default Registrar port number.</span></span> <span data-ttu-id="609b1-136">除了</span><span class="sxs-lookup"><span data-stu-id="609b1-136">Exception:</span></span>

<span data-ttu-id="609b1-137">InvalidOperationException：在拓扑中找不到匹配的群集。</span><span class="sxs-lookup"><span data-stu-id="609b1-137">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="609b1-138">看</span><span class="sxs-lookup"><span data-stu-id="609b1-138">at</span></span>

<span data-ttu-id="609b1-139">SipSyntheticTransaction. TryRetri 的 SyntheticTransactions</span><span class="sxs-lookup"><span data-stu-id="609b1-139">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="609b1-140">eveRegistrarPortFromTopology (Int32& registrarPortNumber) </span><span class="sxs-lookup"><span data-stu-id="609b1-140">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="609b1-141">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="609b1-141">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="609b1-142">结果：失败</span><span class="sxs-lookup"><span data-stu-id="609b1-142">Result : Failure</span></span>

<span data-ttu-id="609b1-143">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="609b1-143">Latency : 00:00:00</span></span>

<span data-ttu-id="609b1-144">错误消息：10060，连接尝试失败，因为已连接的参与方</span><span class="sxs-lookup"><span data-stu-id="609b1-144">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="609b1-145">在一段时间后未正确响应，或者</span><span class="sxs-lookup"><span data-stu-id="609b1-145">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="609b1-146">已建立连接失败，因为连接的主机已</span><span class="sxs-lookup"><span data-stu-id="609b1-146">established connection failed because connected host has</span></span>

<span data-ttu-id="609b1-147">无法响应 \[ 2001：4898： e8： f39e：5c9a： ad83：81b3： 9944 \] ：5061</span><span class="sxs-lookup"><span data-stu-id="609b1-147">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="609b1-148">内部异常：连接尝试失败，因为</span><span class="sxs-lookup"><span data-stu-id="609b1-148">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="609b1-149">已连接方在一段时间后未正确响应</span><span class="sxs-lookup"><span data-stu-id="609b1-149">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="609b1-150">时间，或已建立的连接失败，因为已连接的主机</span><span class="sxs-lookup"><span data-stu-id="609b1-150">time, or established connection failed because connected host</span></span>

<span data-ttu-id="609b1-151">无法响应</span><span class="sxs-lookup"><span data-stu-id="609b1-151">has failed to respond</span></span>

<span data-ttu-id="609b1-152">\[2001：4898： e8： f39e：5c9a： ad83：81b3： 9944 \] ：5061</span><span class="sxs-lookup"><span data-stu-id="609b1-152">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="609b1-153">自检</span><span class="sxs-lookup"><span data-stu-id="609b1-153">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="609b1-154">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="609b1-154">Reasons why the test might have failed</span></span>

<span data-ttu-id="609b1-155">下面是 **测试 CsPersistentChatMessage** 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="609b1-155">Here are some common reasons why **Test-CsPersistentChatMessage** might fail:</span></span>

  - <span data-ttu-id="609b1-156">提供的参数值不正确。</span><span class="sxs-lookup"><span data-stu-id="609b1-156">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="609b1-157">所需的测试帐户可能不存在或已正确创建。</span><span class="sxs-lookup"><span data-stu-id="609b1-157">The required test accounts may not exist or have been correctly created.</span></span>

  - <span data-ttu-id="609b1-158">可能存在导致测试超时的意外延迟的网络问题。</span><span class="sxs-lookup"><span data-stu-id="609b1-158">There may have been a network issue causing an unexpected delay which timed out the test.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="609b1-159">另请参阅</span><span class="sxs-lookup"><span data-stu-id="609b1-159">See Also</span></span>


[<span data-ttu-id="609b1-160">Grant-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="609b1-160">Grant-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsPersistentChatPolicy)  
[<span data-ttu-id="609b1-161">New-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="609b1-161">New-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsPersistentChatPolicy)  
[<span data-ttu-id="609b1-162">Set-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="609b1-162">Set-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatPolicy)  
  

<span data-ttu-id="609b1-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="609b1-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

