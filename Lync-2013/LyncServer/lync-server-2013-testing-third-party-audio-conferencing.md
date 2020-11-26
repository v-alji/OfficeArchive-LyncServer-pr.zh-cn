---
title: Lync Server 2013：测试第三方音频会议
description: Lync Server 2013：测试第三方音频会议。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing third-party audio conferencing
ms:assetid: 0428eb2f-a5ce-47e5-9ea4-383965dfc1e4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727299(v=OCS.15)
ms:contentKeyID: 63969576
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f009d95834768d8a4e6619a79ff1f3be0a2b92bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440953"
---
# <a name="testing-third-party-audio-conferencing-in-lync-server-2013"></a><span data-ttu-id="27b11-103">在 Lync Server 2013 中测试第三方音频会议</span><span class="sxs-lookup"><span data-stu-id="27b11-103">Testing third-party audio conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27b11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27b11-104">

<span> </span></span></span>

<span data-ttu-id="27b11-105">_**主题上次修改时间：** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="27b11-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27b11-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="27b11-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="27b11-107">每天</span><span class="sxs-lookup"><span data-stu-id="27b11-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27b11-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="27b11-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="27b11-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="27b11-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27b11-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="27b11-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="27b11-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="27b11-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="27b11-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsAudioConferencingProvider cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="27b11-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAudioConferencingProvider cmdlet.</span></span> <span data-ttu-id="27b11-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="27b11-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAudioConferencingProvider&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="27b11-114">说明</span><span class="sxs-lookup"><span data-stu-id="27b11-114">Description</span></span>

<span data-ttu-id="27b11-115">音频会议提供商是为组织提供会议服务的第三方公司。</span><span class="sxs-lookup"><span data-stu-id="27b11-115">An audio conferencing provider is a third-party company that provides organizations with conferencing services.</span></span> <span data-ttu-id="27b11-116">此外，音频会议提供商使外出且未连接到企业网络或 Internet 的用户可以通过音频参加会议。</span><span class="sxs-lookup"><span data-stu-id="27b11-116">Among other things, audio conferencing providers enable users located off site, and not connected to the corporate network or the Internet, to participate in the audio portion of a conference or meeting.</span></span> <span data-ttu-id="27b11-117">音频会议提供商通常提供高端服务，例如实时翻译、脚本和实时的每个会议运营商帮助。</span><span class="sxs-lookup"><span data-stu-id="27b11-117">Audio conferencing providers often provide high-end services such as live translation, transcription, and live per-conference operator assistance.</span></span>

<span data-ttu-id="27b11-118">**CsAudioConferencingProvider** cmdlet 用于验证用户是否能够与他/她的音频会议提供商建立连接。</span><span class="sxs-lookup"><span data-stu-id="27b11-118">The **Test-CsAudioConferencingProvider** cmdlet is used to verify that a user is able to make a connection to his or her audio conferencing provider.</span></span> <span data-ttu-id="27b11-119">请注意，此 cmdlet 可以通过两种方式之一运行。</span><span class="sxs-lookup"><span data-stu-id="27b11-119">Note that this cmdlet can be run in one of two ways.</span></span> <span data-ttu-id="27b11-120">许多管理员将使用 CsHealthMonitoringConfiguration cmdlet 为其每个注册机构池设置测试用户。</span><span class="sxs-lookup"><span data-stu-id="27b11-120">Many administrators will use the CsHealthMonitoringConfiguration cmdlets to set up test users for each of their Registrar pools.</span></span> <span data-ttu-id="27b11-121">这些测试用户表示一对已预配置用于综合事务的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="27b11-121">These test users represent a pair of user accounts that have been preconfigured for use with synthetic transactions.</span></span> <span data-ttu-id="27b11-122"> (通常是测试帐户，而不是属于实际用户的帐户。 ) 如果为池配置了测试用户，管理员可以对该池运行 **CsAudioConferencingProvider** cmdlet，而无需指定 (的标识并提供用于) 测试所涉及的用户帐户的凭据。</span><span class="sxs-lookup"><span data-stu-id="27b11-122">(Typically these are test accounts and not accounts that belong to actual users.) If test users are configured for a pool, administrators can run the **Test-CsAudioConferencingProvider** cmdlet against that pool without having to specify the identity of (and supply the credentials for) the user account involved in the test.</span></span>

<span data-ttu-id="27b11-123">或者，管理员可以使用实际 **的** 用户帐户运行 CsAudioConferencingProvider cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27b11-123">Alternatively, administrators can run the **Test-CsAudioConferencingProvider** cmdlet using an actual user account.</span></span> <span data-ttu-id="27b11-124">如果你决定使用实际的用户帐户执行测试，你将需要为该帐户提供登录名和密码。</span><span class="sxs-lookup"><span data-stu-id="27b11-124">If you decide to conduct the test using an actual user account you will need to supply the logon name and password for that account.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="27b11-125">运行测试</span><span class="sxs-lookup"><span data-stu-id="27b11-125">Running the test</span></span>

<span data-ttu-id="27b11-126">示例1检查是否已为 pool atl-cs-001.litwareinc.com 定义的测试用户能够连接到他/她的音频会议提供商。</span><span class="sxs-lookup"><span data-stu-id="27b11-126">Example 1 checks to see if a test user defined for the pool atl-cs-001.litwareinc.com is able to connect to his or her audio conferencing provider.</span></span> <span data-ttu-id="27b11-127">此命令要求为池至少定义一个测试用户。</span><span class="sxs-lookup"><span data-stu-id="27b11-127">This command requires that at least one test user be defined for the pool.</span></span> <span data-ttu-id="27b11-128">如果没有为 atl-cs-001.litwareinc.com 定义测试用户，则该命令将失败;这是因为 **CsAudioConferencingProvider** cmdlet 不会知道在测试中使用哪个用户。</span><span class="sxs-lookup"><span data-stu-id="27b11-128">If no test users have been defined for atl-cs-001.litwareinc.com, then the command will fail; that's because the **Test-CsAudioConferencingProvider** cmdlet will not know which user to employ in the test.</span></span> <span data-ttu-id="27b11-129">如果尚未为池定义测试用户，则必须在验证与音频会议提供商的连接时，包含该命令应使用的用户帐户的 UserSipAddress 参数和凭据。</span><span class="sxs-lookup"><span data-stu-id="27b11-129">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user account that the command should employ when verifying the connection with an audio conferencing provider.</span></span>

    Test-CsAudioConferencingProvider -TargetFqdn atl-cs-001.litwareinc.com 

<span data-ttu-id="27b11-130">示例2中所示的命令测试特定用户 (litwareinc \\ kenmyer) 的功能以连接到他的音频会议提供商。</span><span class="sxs-lookup"><span data-stu-id="27b11-130">The commands shown in Example 2 test the ability of a specific user (litwareinc\\kenmyer) to connect to his audio conferencing provider.</span></span> <span data-ttu-id="27b11-131">为此，示例中的第一个命令使用 Get-Credential cmdlet 创建 Windows PowerShell 命令行界面凭据对象，该对象包含用户 Ken Myer 的名称和密码。</span><span class="sxs-lookup"><span data-stu-id="27b11-131">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credentials object containing the name and password of the user Ken Myer.</span></span> <span data-ttu-id="27b11-132"> (由于登录名 litwareinc \\ kenmyer 已作为参数包含，因此 "Windows PowerShell 凭据请求" 对话框仅要求管理员输入 Ken Myer 帐户的密码。 ) 生成的凭据对象存储在名为 $credential 的变量中。</span><span class="sxs-lookup"><span data-stu-id="27b11-132">(Because the logon name litwareinc\\kenmyer has been included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Ken Myer account.) The resulting credentials object is stored in a variable named $credential.</span></span>

<span data-ttu-id="27b11-133">然后，第二个命令检查该用户是否可以连接到他的音频会议提供商。</span><span class="sxs-lookup"><span data-stu-id="27b11-133">The second command then checks to see if this user can connect to his audio conferencing provider.</span></span> <span data-ttu-id="27b11-134">若要执行此任务，将调用 Test-CsAudioConferencingProvider cmdlet 以及三个参数： TargetFqdn (注册池的 FQDN) ;UserCredential (包含 Ken Myer 的用户凭据的 Windows PowerShell 对象) ;和 UserSipAddress (与提供的用户凭据) 对应的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="27b11-134">To carry out this task, the Test-CsAudioConferencingProvider cmdlet is called, along with three parameters: TargetFqdn (the FQDN of the Registrar pool); UserCredential (the Windows PowerShell object containing Ken Myer's user credentials); and UserSipAddress (the SIP address corresponding to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer" 
    Test-CsAudioConferencingProvider -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="27b11-135">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="27b11-135">Determining success or failure</span></span>

<span data-ttu-id="27b11-136">如果音频会议提供商配置正确，则会收到与此类似的输出，结果属性标记为 **成功：**</span><span class="sxs-lookup"><span data-stu-id="27b11-136">If the audio conferencing provider is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="27b11-137">目标 Fqdn： atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="27b11-137">Target Fqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="27b11-138">结果：成功</span><span class="sxs-lookup"><span data-stu-id="27b11-138">Result : Success</span></span>

<span data-ttu-id="27b11-139">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="27b11-139">Latency : 00:00:00</span></span>

<span data-ttu-id="27b11-140">错误消息：</span><span class="sxs-lookup"><span data-stu-id="27b11-140">Error Message :</span></span>

<span data-ttu-id="27b11-141">自检</span><span class="sxs-lookup"><span data-stu-id="27b11-141">Diagnosis :</span></span>

<span data-ttu-id="27b11-142">如果指定的用户无法登录或注销，则结果将显示为 **失败**，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="27b11-142">If the specified user can't log on or log off, the Result will be shown as a **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="27b11-143">目标 Fqdn： atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="27b11-143">Target Fqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="27b11-144">结果：失败</span><span class="sxs-lookup"><span data-stu-id="27b11-144">Result : Failure</span></span>

<span data-ttu-id="27b11-145">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="27b11-145">Latency : 00:00:00</span></span>

<span data-ttu-id="27b11-146">错误消息：10060，连接尝试失败，因为已连接的参与方</span><span class="sxs-lookup"><span data-stu-id="27b11-146">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="27b11-147">在一段时间后未正确响应，或者</span><span class="sxs-lookup"><span data-stu-id="27b11-147">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="27b11-148">已建立连接失败，因为连接的主机已</span><span class="sxs-lookup"><span data-stu-id="27b11-148">established connection failed because connected host has</span></span>

<span data-ttu-id="27b11-149">无法响应 \[ 2001：4898： e8： f39e：5c9a： ad83：81b3： 9944 \] ：5061</span><span class="sxs-lookup"><span data-stu-id="27b11-149">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="27b11-150">内部异常：连接尝试失败，因为</span><span class="sxs-lookup"><span data-stu-id="27b11-150">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="27b11-151">已连接方在一段时间后未正确响应</span><span class="sxs-lookup"><span data-stu-id="27b11-151">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="27b11-152">时间，或已建立的连接失败，因为已连接的主机</span><span class="sxs-lookup"><span data-stu-id="27b11-152">time, or established connection failed because connected host</span></span>

<span data-ttu-id="27b11-153">无法响应</span><span class="sxs-lookup"><span data-stu-id="27b11-153">has failed to respond</span></span>

<span data-ttu-id="27b11-154">\[2001：4898： e8： f39e：5c9a： ad83：81b3： 9944 \] ：5061</span><span class="sxs-lookup"><span data-stu-id="27b11-154">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="27b11-155">自检</span><span class="sxs-lookup"><span data-stu-id="27b11-155">Diagnosis :</span></span>

<span data-ttu-id="27b11-156">例如，以前的输出包含 "已连接方" 未正确响应的注释，这通常表示边缘服务器有问题。</span><span class="sxs-lookup"><span data-stu-id="27b11-156">For example, the previous output includes the note “the connected party did not properly respond” That typically indicates a problem with the Edge Server.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="27b11-157">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="27b11-157">Reasons why the test might have failed</span></span>

<span data-ttu-id="27b11-158">下面是 **测试 CsAudioConferencingProvider** 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="27b11-158">Here are some common reasons why **Test-CsAudioConferencingProvider** might fail:</span></span>

  - <span data-ttu-id="27b11-159">提供的参数值不正确。</span><span class="sxs-lookup"><span data-stu-id="27b11-159">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="27b11-160">如前面的示例所示，必须正确配置可选参数，否则测试将失败。</span><span class="sxs-lookup"><span data-stu-id="27b11-160">As shown in the previous example, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="27b11-161">重新运行不带可选参数的命令，并查看是否成功。</span><span class="sxs-lookup"><span data-stu-id="27b11-161">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="27b11-162">请注意，如果 **CsAudioConferencingProvider** cmdlet 使用的用户尚未分配音频会议提供商，则测试将失败。</span><span class="sxs-lookup"><span data-stu-id="27b11-162">Note that the test will fail if the user employed by the **Test-CsAudioConferencingProvider** cmdlet has not been assigned an audio conferencing provider.</span></span>

  - <span data-ttu-id="27b11-163">如果边缘服务器配置错误或尚未部署，此命令将失败。</span><span class="sxs-lookup"><span data-stu-id="27b11-163">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

<span data-ttu-id="27b11-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27b11-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

