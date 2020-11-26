---
title: Lync Server 2013：根据语音策略测试电话号码
description: Lync Server 2013：根据语音策略测试电话号码。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test telephone number against a voice policy
ms:assetid: 30c51700-17c6-4c57-891a-8d5ec30b50ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725207(v=OCS.15)
ms:contentKeyID: 63969596
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a6523e7657bd4c30c23909bb02e2569b6067298
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441219"
---
# <a name="test-telephone-number-against-a-voice-policy-in-lync-server-2013"></a><span data-ttu-id="74400-103">根据 Lync Server 2013 中的语音策略测试电话号码</span><span class="sxs-lookup"><span data-stu-id="74400-103">Test telephone number against a voice policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74400-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74400-104">

<span> </span></span></span>

<span data-ttu-id="74400-105">_**主题上次修改时间：** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="74400-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74400-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="74400-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="74400-107">每月</span><span class="sxs-lookup"><span data-stu-id="74400-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74400-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="74400-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="74400-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74400-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74400-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="74400-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="74400-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="74400-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="74400-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsVoicePolicy cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="74400-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoicePolicy cmdlet.</span></span> <span data-ttu-id="74400-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="74400-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoicePolicy&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="74400-114">说明</span><span class="sxs-lookup"><span data-stu-id="74400-114">Description</span></span>

<span data-ttu-id="74400-115">企业语音用户通过公共交换电话网络拨打拨出电话的能力 (PSTN) 转轴，大部分情况下有三种：</span><span class="sxs-lookup"><span data-stu-id="74400-115">The ability of Enterprise Voice users to make outgoing phone calls over the Public Switched Telephone network (PSTN) hinges, in large part, on three things:</span></span>

  - <span data-ttu-id="74400-116">分配给用户的语音策略。</span><span class="sxs-lookup"><span data-stu-id="74400-116">The voice policy assigned to the user.</span></span>

  - <span data-ttu-id="74400-117">用于将来自 Lync 服务器的呼叫路由到 PSTN 网络的语音路由。</span><span class="sxs-lookup"><span data-stu-id="74400-117">The voice routes used to route calls from Lync Server to the PSTN network.</span></span>

  - <span data-ttu-id="74400-118">PSTN 使用，即将语音策略连接到语音路由的 Lync Server 属性。</span><span class="sxs-lookup"><span data-stu-id="74400-118">The PSTN usage, a Lync Server property that connects a voice policy to a voice route.</span></span>

<span data-ttu-id="74400-119">PSTN 用法尤其重要：它是将语音策略连接到语音路由的属性。</span><span class="sxs-lookup"><span data-stu-id="74400-119">The PSTN usage is especially important: it’s the property that connects a voice policy to a voice route.</span></span> <span data-ttu-id="74400-120"> (语音政策和语音路线被称为已连接（如果它们有至少一个 PSTN 使用）。 ) 语音策略可以在不指定 PSTN 使用的情况下进行配置。</span><span class="sxs-lookup"><span data-stu-id="74400-120">(A voice policy and a voice route are said to be connected if they have at least one PSTN usage in common.) Voice policies can be configured without specifying a PSTN usage.</span></span> <span data-ttu-id="74400-121">在这种情况下，已分配该策略的用户将无法通过 PSTN 网络进行传出呼叫。</span><span class="sxs-lookup"><span data-stu-id="74400-121">In that case, users who were assigned that policy won't be able to make outgoing calls over the PSTN network.</span></span> <span data-ttu-id="74400-122">同样，没有指定 PSTN 使用的语音路由也无法将呼叫路由到 PSTN 网络。</span><span class="sxs-lookup"><span data-stu-id="74400-122">Likewise, voice routes that do not have at least one specified PSTN usage will be unable to route calls to the PSTN network.</span></span>

<span data-ttu-id="74400-123">Test-CsVoicePolicy cmdlet 验证给定的语音策略是否具有 PSTN 使用情况，以及该使用情况是否至少由一个语音路由共享。</span><span class="sxs-lookup"><span data-stu-id="74400-123">The Test-CsVoicePolicy cmdlet verifies that a given voice policy has a PSTN usage and that the usage is shared by at least one voice route.</span></span> <span data-ttu-id="74400-124">如果 Test-CsVoicePolicy 成功运行验证，cmdlet 将返回找到的第一个有效语音路由的名称，以及将策略连接到路由的 PSTN 使用的名称。</span><span class="sxs-lookup"><span data-stu-id="74400-124">If the verification run by Test-CsVoicePolicy succeeds, the cmdlet will report back the name of the first valid voice route it finds, and also the name of the PSTN usage that connects the policy to the route.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="74400-125">运行测试</span><span class="sxs-lookup"><span data-stu-id="74400-125">Running the test</span></span>

<span data-ttu-id="74400-126">若要运行 Test-CsVoicePolicy cmdlet，必须首先使用 Get-CsVoicePolicy cmdlet 检索要测试的语音策略实例;然后，必须将该实例管道 CsVoicePolicy。</span><span class="sxs-lookup"><span data-stu-id="74400-126">To run the Test-CsVoicePolicy cmdlet you must first use the Get-CsVoicePolicy cmdlet retrieve an instance of the voice policy to be tested; that instance must then be piped to Test-CsVoicePolicy.</span></span> <span data-ttu-id="74400-127">例如：</span><span class="sxs-lookup"><span data-stu-id="74400-127">For example:</span></span>

`Get-CsVoicePolicy -Identity "Global" | Test-CsVoicePolicy -TargetNumber "+12065551219"`

<span data-ttu-id="74400-128">请注意，此命令不使用 Get-CsVoicePolicy 检索语音策略实例将失败：</span><span class="sxs-lookup"><span data-stu-id="74400-128">Note that this command, which does not use Get-CsVoicePolicy to retrieve a voice policy instance, will fail:</span></span>

`Test-CsVoicePolicy -TargetNumber "+12065551219" -VoicePolicy "Global"`

<span data-ttu-id="74400-129">如果要根据指定的电话号码检查所有语音策略，请使用如下所示的命令：</span><span class="sxs-lookup"><span data-stu-id="74400-129">If you want to check all the voice policies against a specified phone number then use a command similar to this:</span></span>

`Get-CsVoicePolicy | Test-CsVoicePolicy -TargetNumber "+12065551219"`

<span data-ttu-id="74400-130">请注意，TargetNumber 必须使用 E.i 格式进行指定。</span><span class="sxs-lookup"><span data-stu-id="74400-130">Note that the TargetNumber must be specified by using the E.164 format.</span></span> <span data-ttu-id="74400-131">Test-CsVoicePolicy 不会尝试将电话号码正常化或转换为 E-164 格式。</span><span class="sxs-lookup"><span data-stu-id="74400-131">Test-CsVoicePolicy won't attempt to normalize or translate phone numbers into the E.164 format.</span></span>

<span data-ttu-id="74400-132">有关详细信息，请参阅 Test-CsVoicePolicy cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="74400-132">For more information, see the Help documentation for the Test-CsVoicePolicy cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="74400-133">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="74400-133">Determining success or failure</span></span>

<span data-ttu-id="74400-134">如果语音策略可以找到匹配的语音路由和匹配的 PSTN 使用，则将在屏幕上显示路由和使用情况：</span><span class="sxs-lookup"><span data-stu-id="74400-134">If the voice policy can find both a matching voice route and a matching PSTN usage, then both the route and the usage will be displayed on-screen:</span></span>

<span data-ttu-id="74400-135">FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="74400-135">FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="74400-136">\------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="74400-136">\------------------ -------------</span></span>

<span data-ttu-id="74400-137">RedmondVoiceRoute RedmondPstnUsage</span><span class="sxs-lookup"><span data-stu-id="74400-137">RedmondVoiceRoute RedmondPstnUsage</span></span>

<span data-ttu-id="74400-138">如果找不到合适的语音路线或合适的 PSTN 使用，将在屏幕上显示空属性值：</span><span class="sxs-lookup"><span data-stu-id="74400-138">If either an appropriate voice route or an appropriate PSTN usage cannot be found then blank property values will be displayed on-screen:</span></span>

<span data-ttu-id="74400-139">FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="74400-139">FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="74400-140">\------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="74400-140">\------------------ -------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="74400-141">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="74400-141">Reasons why the test might have failed</span></span>

<span data-ttu-id="74400-142">如果 Test-CsVoicePolicy 未返回一个匹配项，这可能意味着语音策略不会与语音路由共享 PSTN 使用。</span><span class="sxs-lookup"><span data-stu-id="74400-142">If Test-CsVoicePolicy does not return a match that could mean that the voice policy does not share a PSTN usage with a voice route.</span></span> <span data-ttu-id="74400-143">若要验证，请使用类似于以下内容的 cmdlet 验证分配给语音策略的 PSTN 用法：</span><span class="sxs-lookup"><span data-stu-id="74400-143">To verify that, use a cmdlet similar to the following to verify that PSTN usages assigned to the voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global" | Select-Object PstnUsages | Format-List`

<span data-ttu-id="74400-144">接下来，运行此命令以确定分配给每个语音路由的 PSTN 使用情况：</span><span class="sxs-lookup"><span data-stu-id="74400-144">Next, run this command to determine the PSTN usages assign to each of your voice routes:</span></span>

`Get-CsVoiceRoute | Select-Object Identity, PstnUsages`

<span data-ttu-id="74400-145">如果你看到任何匹配 (也就是说，如果你看到一个或多个语音路由，其中至少有一个 PSTN 使用与你的语音策略) ，则你应该运行 Test-CsVoiceRoute cmdlet 以验证语音路线是否可以拨出所提供的电话号码。</span><span class="sxs-lookup"><span data-stu-id="74400-145">If you see any matches (that is, if you see one or more voice routes that share at least one PSTN usage with your voice policy), you should then run the Test-CsVoiceRoute cmdlet to verify that the voice route can dial the supplied phone number.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="74400-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="74400-146">See Also</span></span>


[<span data-ttu-id="74400-147">Test-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="74400-147">Test-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoicePolicy)  
  

<span data-ttu-id="74400-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74400-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

