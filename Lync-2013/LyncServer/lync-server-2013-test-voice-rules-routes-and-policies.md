---
title: Lync Server 2013：测试语音规则、路由和策略
description: Lync Server 2013：测试语音规则、路由和策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice rules, routes, and policies
ms:assetid: ebb9c3fa-6950-4311-87ca-e1ecd9280a43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725213(v=OCS.15)
ms:contentKeyID: 63969661
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf205ac2585298dfc5347d93e382e8bbda9f3ff4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391789"
---
# <a name="test-voice-rules-routes-and-policies-in-lync-server-2013"></a><span data-ttu-id="473c1-103">在 Lync Server 2013 中测试语音规则、路由和策略</span><span class="sxs-lookup"><span data-stu-id="473c1-103">Test voice rules, routes, and policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="473c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="473c1-104">

<span> </span></span></span>

<span data-ttu-id="473c1-105">_**主题上次修改时间：** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="473c1-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="473c1-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="473c1-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="473c1-107">每月</span><span class="sxs-lookup"><span data-stu-id="473c1-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473c1-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="473c1-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="473c1-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="473c1-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473c1-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="473c1-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="473c1-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="473c1-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="473c1-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsVoiceUser cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="473c1-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceUser cmdlet.</span></span> <span data-ttu-id="473c1-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="473c1-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceUser&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="473c1-114">说明</span><span class="sxs-lookup"><span data-stu-id="473c1-114">Description</span></span>

<span data-ttu-id="473c1-115">当用户进行电话呼叫时，呼叫到达其目标所需的路线取决于分配给该用户的策略和拨号计划。</span><span class="sxs-lookup"><span data-stu-id="473c1-115">When a user makes a phone call, the route the call takes to reach its destination depends on both the policies and dial plans assigned to that user.</span></span> <span data-ttu-id="473c1-116">如果用户的 SIP 地址和电话号码，Test-CsVoiceUser cmdlet 将验证问题用户是否可以完成对该号码的呼叫。</span><span class="sxs-lookup"><span data-stu-id="473c1-116">Given a user’s SIP address and a phone number, the Test-CsVoiceUser cmdlet verifies whether the user in question can complete a call to that number.</span></span> <span data-ttu-id="473c1-117">如果测试成功，Test-CsVoiceUser 返回以下内容：</span><span class="sxs-lookup"><span data-stu-id="473c1-117">If the test succeeds, Test-CsVoiceUser returns the following:</span></span>

  - <span data-ttu-id="473c1-118">根据用户的拨号计划，已转换为 (164 格式的数字) </span><span class="sxs-lookup"><span data-stu-id="473c1-118">The number translated to E.164 format (based on the user’s dial plan)</span></span>

  - <span data-ttu-id="473c1-119">提供该翻译的规范化规则</span><span class="sxs-lookup"><span data-stu-id="473c1-119">The normalization rule that supplied that translation</span></span>

  - <span data-ttu-id="473c1-120"> (根据路线优先级) 使用的语音路线;</span><span class="sxs-lookup"><span data-stu-id="473c1-120">The voice route used (based on route priority);</span></span>

  - <span data-ttu-id="473c1-121">将用户语音策略链接到语音路由的电话使用。</span><span class="sxs-lookup"><span data-stu-id="473c1-121">The phone usage that linked the user’s voice policy to the voice route.</span></span>

<span data-ttu-id="473c1-122">Test-CsVoiceUser 使你能够确定特定的电话号码是否按预期进行路由和翻译，并帮助解决单个用户遇到的与呼叫相关的问题。</span><span class="sxs-lookup"><span data-stu-id="473c1-122">Test-CsVoiceUser enables you to determine whether a specific phone number will route and translate as expected, and can help troubleshoot call-related problems that are experienced by individual users.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="473c1-123">运行测试</span><span class="sxs-lookup"><span data-stu-id="473c1-123">Running the test</span></span>

<span data-ttu-id="473c1-124">在运行 Test-CsVoiceUser cmdlet 时，你必须提供以下两条信息： (DialedNumber) 拨打的号码和正在测试的用户帐户的标识。</span><span class="sxs-lookup"><span data-stu-id="473c1-124">When running the Test-CsVoiceUser cmdlet you must supply two pieces of information: the number being dialed (DialedNumber) and the Identity of the user account being tested.</span></span> <span data-ttu-id="473c1-125">例如，此命令将测试具有 SIP 地址 sip:kenmyer@litwareinc.com 的用户的功能，以便拨打电话号码 + 1206555-1219：</span><span class="sxs-lookup"><span data-stu-id="473c1-125">For example, this command tests the ability of the user who has the SIP address sip:kenmyer@litwareinc.com to make a call to the phone number +1206555-1219:</span></span>

`Test-CsVoiceUser -DialedNumber "12065551219" -SipUri "sip:kenmyer@litwareinc.com"`

<span data-ttu-id="473c1-126">电话号码应按您希望的拨号方式进行格式设置。</span><span class="sxs-lookup"><span data-stu-id="473c1-126">The phone number should be formatted in the way that you expect it to be dialed.</span></span> <span data-ttu-id="473c1-127">例如，如果在拨长途电话之前，用户通常不先拨1，则应使用以下格式：</span><span class="sxs-lookup"><span data-stu-id="473c1-127">For example, if users typically do not dial the 1 before placing a long distance call then you should use this format:</span></span>

`-DialedNumber "2065551219"`

<span data-ttu-id="473c1-128">当然，在这种情况下，如果你没有可以将数字2065551219正确转换为 Lync Server 使用的 E：164电话格式的规范化规则，测试将失败。</span><span class="sxs-lookup"><span data-stu-id="473c1-128">Of course, in that case, the test will fail if you do not have a normalization rule that can correctly translate the number 2065551219 into the E.164 telephone format that is used by Lync Server.</span></span> <span data-ttu-id="473c1-129">有关详细信息，请参阅帮助主题 New-CsVoiceNormalizationRule cmdlet。</span><span class="sxs-lookup"><span data-stu-id="473c1-129">For more information, see the help topic New-CsVoiceNormalizationRule cmdlet.</span></span>

<span data-ttu-id="473c1-130">如果你想要对每个用户帐户运行此相同的测试，你可以使用类似于以下的命令：</span><span class="sxs-lookup"><span data-stu-id="473c1-130">If you want to run this same test against each of your user accounts, you can use a command similar to the following:</span></span>

`Get-CsUser | ForEach-Object {$_.DisplayName; Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri $_.SipAddress} | Format-List`

<span data-ttu-id="473c1-131">有关详细信息，请参阅 Test-CsVoiceUser cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="473c1-131">For more information, see the Help documentation for the Test-CsVoiceUser cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="473c1-132">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="473c1-132">Determining success or failure</span></span>

<span data-ttu-id="473c1-133">如果测试成功完成 (也就是说，如果用户可以拨打指定号码的电话) ，则输出将显示诸如已翻译电话号码和匹配规范化规则和语音路线之类的信息：</span><span class="sxs-lookup"><span data-stu-id="473c1-133">If the test is completed successfully (that is, if the user can make a phone call to the specified number), the output will show information like the translated phone number and the matching normalization rule and voice route:</span></span>

<span data-ttu-id="473c1-134">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="473c1-134">TranslatedNumber    MatchingRule    FirstMatchingRoute    MatchingUsage</span></span>

<span data-ttu-id="473c1-135">\----------------    ------------    ------------------    -------------</span><span class="sxs-lookup"><span data-stu-id="473c1-135">\----------------    ------------    ------------------    -------------</span></span>

<span data-ttu-id="473c1-136">\+12065551219 Descripti   LocalRoute Local</span><span class="sxs-lookup"><span data-stu-id="473c1-136">\+12065551219        Descripti...    LocalRoute            Local</span></span>

<span data-ttu-id="473c1-137">由于 Windows PowerShell 屏幕的限制，至少一些返回的信息 (最值得注意的是匹配规范化规则的完整描述) 可能不会显示在屏幕上。</span><span class="sxs-lookup"><span data-stu-id="473c1-137">Because of the limitations of the Windows PowerShell screen, at least some returned information (most notably the full description of the matching normalization rule) might not appear on-screen.</span></span> <span data-ttu-id="473c1-138">如果你仅对测试的成功或失败感兴趣，则可能不重要。</span><span class="sxs-lookup"><span data-stu-id="473c1-138">If you are only interested in the success or failure of the test, then this might not matter.</span></span> <span data-ttu-id="473c1-139">如果你希望查看返回数据的完整详细信息，请在运行测试时将输出管道到 Format-List cmdlet：</span><span class="sxs-lookup"><span data-stu-id="473c1-139">If you would prefer to see the full details of the returned data then pipe the output to the Format-List cmdlet when running the test:</span></span>

`Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri "sip:kenmyer@litwareinc.com" -Verbose | Format-List`

<span data-ttu-id="473c1-140">这将以更易于读取器的格式显示输出：</span><span class="sxs-lookup"><span data-stu-id="473c1-140">That will display the output in a more reader-friendly format:</span></span>

<span data-ttu-id="473c1-141">TranslatedNumber： + 12065551219</span><span class="sxs-lookup"><span data-stu-id="473c1-141">TranslatedNumber : +12065551219</span></span>

<span data-ttu-id="473c1-142">MatchingRule： Description =;模式 = ^ (\\ d {11}) $;转换 = + $ 1;</span><span class="sxs-lookup"><span data-stu-id="473c1-142">MatchingRule : Description=;Pattern=^(\\d{11})$;Translation=+$1;</span></span>

<span data-ttu-id="473c1-143">Name = Prefix All; IsInternalExtension = False</span><span class="sxs-lookup"><span data-stu-id="473c1-143">Name=Prefix All;IsInternalExtension=False</span></span>

<span data-ttu-id="473c1-144">FirsMatchingRoute : LocalRoute</span><span class="sxs-lookup"><span data-stu-id="473c1-144">FirsMatchingRoute : LocalRoute</span></span>

<span data-ttu-id="473c1-145">MatchingUsage： Local</span><span class="sxs-lookup"><span data-stu-id="473c1-145">MatchingUsage : Local</span></span>

<span data-ttu-id="473c1-146">如果测试失败，Test-CsVoiceUser 将返回一组空的属性值：</span><span class="sxs-lookup"><span data-stu-id="473c1-146">If the test fails, Test-CsVoiceUser will return an empty set of property values:</span></span>

<span data-ttu-id="473c1-147">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="473c1-147">TranslatedNumber MatchingRule FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="473c1-148">\---------------- ------------ ------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="473c1-148">\---------------- ------------ ------------------ -------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="473c1-149">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="473c1-149">Reasons why the test might have failed</span></span>

<span data-ttu-id="473c1-150">Test-CsVoiceUser cmdlet 可能失败的原因有多种：可能没有可以转换所提供的电话号码的规范化规则。</span><span class="sxs-lookup"><span data-stu-id="473c1-150">There are any number of reasons why the Test-CsVoiceUser cmdlet might fail: there might not be a normalization rule that can translate the provided phone number.</span></span> <span data-ttu-id="473c1-151">语音路线可能出现问题。</span><span class="sxs-lookup"><span data-stu-id="473c1-151">There could be problems with the voice route.</span></span> <span data-ttu-id="473c1-152">分配给有问题的用户的拨号计划可能存在配置问题。</span><span class="sxs-lookup"><span data-stu-id="473c1-152">There could be a configuration issue with the dial plan assigned to the user in question.</span></span> <span data-ttu-id="473c1-153">因此，你可能希望在运行 Test-CsVoiceUser cmdlet 时包含详细参数：</span><span class="sxs-lookup"><span data-stu-id="473c1-153">Because of that, you might want to include the Verbose parameter when you are running the Test-CsVoiceUser cmdlet:</span></span>

`Test-CsVoiceUser -DialedNumber "+12065551219" -SipUri "sip:kenmyer@litwareinc.com" -Verbose`

<span data-ttu-id="473c1-154">包括详细 cmdlet 时，Test-CsVoiceUser 将颁发执行检查时采取的所有步骤的详细帐户。</span><span class="sxs-lookup"><span data-stu-id="473c1-154">When the Verbose cmdlet is included, Test-CsVoiceUser will issue a detailed account of all the steps in takes when conducting its checks.</span></span> <span data-ttu-id="473c1-155">例如，你可能会看到类似以下的步骤：</span><span class="sxs-lookup"><span data-stu-id="473c1-155">For example, you might see steps similar to these:</span></span> 

<span data-ttu-id="473c1-156">详细：查找标识为 "sip:kenmyer@litwareinc.com" 的用户</span><span class="sxs-lookup"><span data-stu-id="473c1-156">VERBOSE: Locating user with identity "sip:kenmyer@litwareinc.com"</span></span>

<span data-ttu-id="473c1-157">详细：正在加载拨号计划： "RedmondDialPlan"</span><span class="sxs-lookup"><span data-stu-id="473c1-157">VERBOSE: Loading dial plan: "RedmondDialPlan"</span></span>

<span data-ttu-id="473c1-158">这些附加信息可提供有关可用于查明失败原因的步骤的提示。</span><span class="sxs-lookup"><span data-stu-id="473c1-158">This additional information can provide hints as to the steps that you can take to pinpoint the cause of the failure.</span></span> <span data-ttu-id="473c1-159">例如，此处显示的详细输出告诉我们，正在测试的用户是否已分配了拨号计划 RedmondDialPlan。</span><span class="sxs-lookup"><span data-stu-id="473c1-159">For example, the verbose output shown here tells us that the user being tested was assigned the dial plan RedmondDialPlan.</span></span> <span data-ttu-id="473c1-160">如果测试失败，下一个逻辑下一步是验证 RedmondDialPlan 是否可以转换提供的电话号码。</span><span class="sxs-lookup"><span data-stu-id="473c1-160">If the test has failed, one logical next step would be to verify that RedmondDialPlan can translate the supplied phone number.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="473c1-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="473c1-161">See Also</span></span>


[<span data-ttu-id="473c1-162">Test-CsVoiceUser</span><span class="sxs-lookup"><span data-stu-id="473c1-162">Test-CsVoiceUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceUser)  
  

<span data-ttu-id="473c1-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="473c1-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

