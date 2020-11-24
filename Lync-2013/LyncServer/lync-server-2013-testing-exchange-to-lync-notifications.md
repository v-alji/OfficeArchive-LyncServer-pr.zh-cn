---
title: Lync Server 2013：测试与 Lync 通知的 Exchange
description: Lync Server 2013：测试与 Lync 通知的 Exchange。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Exchange to Lync notifications
ms:assetid: ed2d6325-3cf5-4450-9951-03092bcb0a7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727315(v=OCS.15)
ms:contentKeyID: 63969665
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bdf453bfdaab7e7b6bdaae8b67ac7759c0d55af4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392092"
---
# <a name="testing-exchange-to-lync-notifications-in-lync-server-2013"></a><span data-ttu-id="238f0-103">在 Lync Server 2013 中测试与 Lync 通知的 Exchange</span><span class="sxs-lookup"><span data-stu-id="238f0-103">Testing Exchange to Lync notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="238f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="238f0-104">

<span> </span></span></span>

<span data-ttu-id="238f0-105">_**主题上次修改时间：** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="238f0-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="238f0-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="238f0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="238f0-107">每天</span><span class="sxs-lookup"><span data-stu-id="238f0-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="238f0-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="238f0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="238f0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="238f0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="238f0-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="238f0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="238f0-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="238f0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="238f0-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 <strong>CsExStorageNotification</strong> cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="238f0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExStorageNotification</strong> cmdlet.</span></span> <span data-ttu-id="238f0-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="238f0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExStorageNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="238f0-114">说明</span><span class="sxs-lookup"><span data-stu-id="238f0-114">Description</span></span>

<span data-ttu-id="238f0-115">**CsExStorageNotification** cmdlet 用于验证 Microsoft Exchange Server 2013 通知服务是否可以在每次更新用户的联系人列表时通知 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="238f0-115">The **Test-CsExStorageNotification** cmdlet is used to verify that the Microsoft Exchange Server 2013 notification service can notify Lync Server 2013 any time updates are made to a user's Contact List.</span></span> <span data-ttu-id="238f0-116">仅当使用统一联系人存储时，此 cmdlet 才有效。</span><span class="sxs-lookup"><span data-stu-id="238f0-116">This cmdlet is valid only if you are using the unified contact store.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="238f0-117">运行测试</span><span class="sxs-lookup"><span data-stu-id="238f0-117">Running the test</span></span>

<span data-ttu-id="238f0-118">示例1测试中显示的命令可查看 Lync Server 存储服务是否可以连接到用户 sip:kenmyer@litwareinc.com 的 Microsoft Exchange Server 邮箱通知服务。</span><span class="sxs-lookup"><span data-stu-id="238f0-118">The command shown in Example 1 tests to see whether the Lync Server Storage Service can connect to the Microsoft Exchange Server mailbox notification service for the user sip:kenmyer@litwareinc.com.</span></span> <span data-ttu-id="238f0-119">在此示例中，NetNamedPipe 用作 WCF 绑定。</span><span class="sxs-lookup"><span data-stu-id="238f0-119">In this example, NetNamedPipe is used as the WCF binding.</span></span>

    Test-CsExStorageNotification -SipUri "sip:kenmyer@litwareinc.com" -Binding "NetNamedPipe"

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="238f0-120">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="238f0-120">Determining success or failure</span></span>

<span data-ttu-id="238f0-121">如果 Exchange 集成配置正确，则会收到与此类似的输出，结果属性标记为 **成功**：</span><span class="sxs-lookup"><span data-stu-id="238f0-121">If Exchange integration is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="238f0-122">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="238f0-122">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="238f0-123">结果：成功</span><span class="sxs-lookup"><span data-stu-id="238f0-123">Result : Success</span></span>

<span data-ttu-id="238f0-124">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="238f0-124">Latency : 00:00:00</span></span>

<span data-ttu-id="238f0-125">错误消息：</span><span class="sxs-lookup"><span data-stu-id="238f0-125">Error Message :</span></span>

<span data-ttu-id="238f0-126">自检</span><span class="sxs-lookup"><span data-stu-id="238f0-126">Diagnosis :</span></span>

<span data-ttu-id="238f0-127">如果指定的用户无法接收通知，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="238f0-127">If the specified user can't receive notifications, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="238f0-128">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="238f0-128">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="238f0-129">结果：失败</span><span class="sxs-lookup"><span data-stu-id="238f0-129">Result : Failure</span></span>

<span data-ttu-id="238f0-130">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="238f0-130">Latency : 00:00:00</span></span>

<span data-ttu-id="238f0-131">错误消息：10060，连接尝试失败，因为已连接的参与方</span><span class="sxs-lookup"><span data-stu-id="238f0-131">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="238f0-132">在一段时间后未正确响应，或者</span><span class="sxs-lookup"><span data-stu-id="238f0-132">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="238f0-133">已建立连接失败，因为连接的主机已</span><span class="sxs-lookup"><span data-stu-id="238f0-133">established connection failed because connected host has</span></span>

<span data-ttu-id="238f0-134">无法响应10.188.116.96：5061</span><span class="sxs-lookup"><span data-stu-id="238f0-134">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="238f0-135">内部异常：连接尝试失败，因为</span><span class="sxs-lookup"><span data-stu-id="238f0-135">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="238f0-136">已连接方在一段时间后未正确响应</span><span class="sxs-lookup"><span data-stu-id="238f0-136">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="238f0-137">时间，或已建立的连接失败，因为已连接的主机</span><span class="sxs-lookup"><span data-stu-id="238f0-137">time, or established connection failed because connected host</span></span>

<span data-ttu-id="238f0-138">无法响应10.188.116.96：5061</span><span class="sxs-lookup"><span data-stu-id="238f0-138">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="238f0-139">自检</span><span class="sxs-lookup"><span data-stu-id="238f0-139">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="238f0-140">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="238f0-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="238f0-141">下面是 **测试 CsExStorageNotification** 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="238f0-141">Here are some common reasons why **Test-CsExStorageNotification** might fail:</span></span>

  - <span data-ttu-id="238f0-142">提供的参数值不正确。</span><span class="sxs-lookup"><span data-stu-id="238f0-142">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="238f0-143">如果使用，则必须正确配置可选参数，否则测试将失败。</span><span class="sxs-lookup"><span data-stu-id="238f0-143">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="238f0-144">重新运行不带可选参数的命令，并查看是否成功。</span><span class="sxs-lookup"><span data-stu-id="238f0-144">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="238f0-145">如果 Microsoft Exchange Server 配置错误或尚未部署，此命令将失败。</span><span class="sxs-lookup"><span data-stu-id="238f0-145">This command will fail if the Microsoft Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="238f0-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="238f0-146">See Also</span></span>


[<span data-ttu-id="238f0-147">Test-CsExStorageConnectivity</span><span class="sxs-lookup"><span data-stu-id="238f0-147">Test-CsExStorageConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExStorageConnectivity)  
  

<span data-ttu-id="238f0-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="238f0-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

