---
title: Lync Server 2013：用于连接到联盟域的测试能力
description: Lync Server 2013：测试连接到联盟域的能力。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to connect to a federated domain
ms:assetid: d8ccfade-ef54-47a4-9f87-36213a635ce5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743840(v=OCS.15)
ms:contentKeyID: 63969653
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf1f5bdef66d34b9ca2e39797df0b4ad32d9afde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441135"
---
# <a name="testing-ability-to-connect-to-a-federated-domain-from-lync-server-2013"></a><span data-ttu-id="fd7fa-103">从 Lync Server 2013 连接到联盟域的测试能力</span><span class="sxs-lookup"><span data-stu-id="fd7fa-103">Testing ability to connect to a federated domain from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd7fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd7fa-104">

<span> </span></span></span>

<span data-ttu-id="fd7fa-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="fd7fa-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd7fa-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="fd7fa-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="fd7fa-107">每天</span><span class="sxs-lookup"><span data-stu-id="fd7fa-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd7fa-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="fd7fa-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="fd7fa-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fd7fa-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd7fa-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="fd7fa-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="fd7fa-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="fd7fa-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsFederatedPartner cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsFederatedPartner cmdlet.</span></span> <span data-ttu-id="fd7fa-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsFederatedPartner&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="fd7fa-114">说明</span><span class="sxs-lookup"><span data-stu-id="fd7fa-114">Description</span></span>

<span data-ttu-id="fd7fa-115">Test-CsFederatedPartner 验证您是否能够连接到联盟伙伴的域。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-115">Test-CsFederatedPartner verifies your ability to connect to the domain of a federated partner.</span></span> <span data-ttu-id="fd7fa-116">若要验证与域的连接，该域必须在允许的 (联盟) 域的集合中列出。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-116">To verify the connectivity to a domain, that domain must be listed in the collection of allowed (federated) domains.</span></span> <span data-ttu-id="fd7fa-117">您可以使用以下命令检索 "允许的域" 列表中的域列表：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-117">You can retrieve a list of the domains on your allowed domains list by using this command:</span></span>

    Get-CsAllowedDomain

<span data-ttu-id="fd7fa-118">有关详细信息，请参阅 [CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-118">For more information, see the Help documentation for the [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="fd7fa-119">运行测试</span><span class="sxs-lookup"><span data-stu-id="fd7fa-119">Running the test</span></span>

<span data-ttu-id="fd7fa-120">Test-FederatedPartner cmdlet 需要两条信息： Edge 服务器的 FQDN 和联盟伙伴的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-120">The Test-FederatedPartner cmdlet requires two pieces of information: the FQDN of your Edge Server and the FQDN of the federated partner.</span></span> <span data-ttu-id="fd7fa-121">例如，此命令测试连接到域 contoso.com 的能力：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-121">For example, this command tests the ability to connect to the domain contoso.com:</span></span>

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"

<span data-ttu-id="fd7fa-122">通过此命令，你可以测试与当前在允许的域列表中的所有域的连接：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-122">This command enables you to test the connections to all the domains currently on your allowed domains list:</span></span>

    Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Identity}

<span data-ttu-id="fd7fa-123">有关详细信息，请参阅 [CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-123">For more information, see the Help documentation for the [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="fd7fa-124">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="fd7fa-124">Determining success or failure</span></span>

<span data-ttu-id="fd7fa-125">如果可以联系指定的域，你将收到与以下内容类似的输出：结果属性标记为 **成功：**</span><span class="sxs-lookup"><span data-stu-id="fd7fa-125">If the specified domain can be contacted, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="fd7fa-126">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="fd7fa-126">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="fd7fa-127">结果：成功</span><span class="sxs-lookup"><span data-stu-id="fd7fa-127">Result : Success</span></span>

<span data-ttu-id="fd7fa-128">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="fd7fa-128">Latency : 00:00:00</span></span>

<span data-ttu-id="fd7fa-129">时发生</span><span class="sxs-lookup"><span data-stu-id="fd7fa-129">Error :</span></span>

<span data-ttu-id="fd7fa-130">自检</span><span class="sxs-lookup"><span data-stu-id="fd7fa-130">Diagnosis :</span></span>

<span data-ttu-id="fd7fa-131">如果无法联系指定域，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-131">If the specified domain cannot be contacted, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="fd7fa-132">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="fd7fa-132">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="fd7fa-133">结果：失败</span><span class="sxs-lookup"><span data-stu-id="fd7fa-133">Result : Failure</span></span>

<span data-ttu-id="fd7fa-134">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="fd7fa-134">Latency : 00:00:00</span></span>

<span data-ttu-id="fd7fa-135">错误：504，服务器超时</span><span class="sxs-lookup"><span data-stu-id="fd7fa-135">Error : 504, Server time-out</span></span>

<span data-ttu-id="fd7fa-136">诊断： ErrorCode = 2，Source = atl-litwareinc，Reason = 请参阅</span><span class="sxs-lookup"><span data-stu-id="fd7fa-136">Diagnosis : ErrorCode=2, Source=atl-cs-001.litwareinc.com,Reason=See</span></span>

<span data-ttu-id="fd7fa-137">响应代码和原因短语。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-137">response code and reason phrase.</span></span>

<span data-ttu-id="fd7fa-138">Microsoft DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="fd7fa-138">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="fd7fa-139">例如，以前的输出表明测试因服务器超时错误而失败。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-139">For example, the previous output states that the test failed because of a server time-out error.</span></span> <span data-ttu-id="fd7fa-140">这通常表示网络连接问题或联系边缘服务器时出现问题。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-140">This typically indicates either network connectivity problems or problems contacting the Edge Server.</span></span>

<span data-ttu-id="fd7fa-141">如果 Test-CsFederatedPartner 失败，则可能需要重新运行测试，这一次包括 Verbose 参数：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-141">If Test-CsFederatedPartner fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com" -Verbose

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="fd7fa-142">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="fd7fa-142">Reasons why the test might have failed</span></span>

<span data-ttu-id="fd7fa-143">下面是 Test-CsFederatedPartner 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-143">Here are some common reasons why Test-CsFederatedPartner might fail:</span></span>

  - <span data-ttu-id="fd7fa-144">边缘服务器可能不可用。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-144">The Edge Server might not be available.</span></span> <span data-ttu-id="fd7fa-145">你可以使用以下命令来使用 Edge 服务器的 Fqdn：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-145">You can the FQDNs of your Edge Servers by using this command:</span></span>
    
        Get-CsService -EdgeServer | Select-Object PoolFqdn
    
    <span data-ttu-id="fd7fa-146">然后，你可以 ping 每台边缘服务器以验证是否可以通过网络访问它。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-146">You can then ping each Edge Server to verify that it can be accessed over the network.</span></span> <span data-ttu-id="fd7fa-147">例如：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-147">For example:</span></span>
    
        ping atl-edge-001.litwareinc.com

  - <span data-ttu-id="fd7fa-148">指定域可能未在 "允许的域" 列表中列出。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-148">The specified domain might not be listed on the allowed domains list.</span></span> <span data-ttu-id="fd7fa-149">若要验证已添加到 "允许的域" 列表中的域，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-149">To verify the domains that were added to the allowed domains list, use this command:</span></span>
    
        Get-CsAllowedDomain
    
    <span data-ttu-id="fd7fa-150">如果你想要查看阻止用户与之通信的域的列表，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="fd7fa-150">If you’d like to see a list of domains that users were blocked from communicating with, then use this command:</span></span>
    
        Get-CsBlockedDomain

<span data-ttu-id="fd7fa-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd7fa-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

