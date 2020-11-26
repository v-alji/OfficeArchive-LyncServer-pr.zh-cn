---
title: 测试分配给网站的 Kerberos 帐户的配置
description: 测试分配给网站的 Kerberos 帐户的配置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing configuration of the Kerberos account assigned to a site
ms:assetid: a087d77e-c59e-44f5-9caa-ccfd41be7276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743837(v=OCS.15)
ms:contentKeyID: 63969637
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0eab1618474a19753a4c6064d59aa4f8a856fceb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441065"
---
# <a name="testing-configuration-of-the-kerberos-account-assigned-to-a-site-in-lync-server-2013"></a><span data-ttu-id="a77c4-103">在 Lync Server 2013 中测试分配给网站的 Kerberos 帐户的配置</span><span class="sxs-lookup"><span data-stu-id="a77c4-103">Testing configuration of the Kerberos account assigned to a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a77c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a77c4-104">

<span> </span></span></span>

<span data-ttu-id="a77c4-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="a77c4-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a77c4-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="a77c4-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="a77c4-107">每天</span><span class="sxs-lookup"><span data-stu-id="a77c4-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a77c4-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="a77c4-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="a77c4-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a77c4-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a77c4-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="a77c4-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="a77c4-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="a77c4-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="a77c4-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsKerberosAccountAssignment cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="a77c4-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsKerberosAccountAssignment cmdlet.</span></span> <span data-ttu-id="a77c4-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="a77c4-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsKerberosAccountAssignment&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="a77c4-114">说明</span><span class="sxs-lookup"><span data-stu-id="a77c4-114">Description</span></span>

<span data-ttu-id="a77c4-115">通过 Test-CsKerberosAccountAssignment cmdlet，你可以验证 Kerberos 帐户是否与给定网站相关联、此帐户是否已正确配置以及帐户是否按预期工作。</span><span class="sxs-lookup"><span data-stu-id="a77c4-115">The Test-CsKerberosAccountAssignment cmdlet enables you to verify that a Kerberos account is associated with a given site, that this account is configured correctly, and that the account is working as expected.</span></span> <span data-ttu-id="a77c4-116">Kerberos 帐户是计算机帐户，可用作运行 Internet 信息服务器的网站中的所有计算机的身份验证主体 (IIS) 。</span><span class="sxs-lookup"><span data-stu-id="a77c4-116">Kerberos accounts are computer accounts that can serve as the authentication principal for all the computers in a site that are running Internet Information Server (IIS).</span></span> <span data-ttu-id="a77c4-117">由于这些帐户使用 Kerberos 身份验证协议，因此帐户称为 Kerberos 帐户，新的身份验证过程称为 Kerberos web 身份验证。</span><span class="sxs-lookup"><span data-stu-id="a77c4-117">Because these accounts use the Kerberos authentication protocol, the accounts are known as Kerberos accounts, and the new authentication process is known as Kerberos web authentication.</span></span> <span data-ttu-id="a77c4-118">这使你可以使用单个帐户管理所有 IIS 服务器。</span><span class="sxs-lookup"><span data-stu-id="a77c4-118">This enables you to manage all IIS servers by using a single account.</span></span>

<span data-ttu-id="a77c4-119">有关详细信息，请参阅 [CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="a77c4-119">For more information, see the Help documentation for the [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="a77c4-120">运行测试</span><span class="sxs-lookup"><span data-stu-id="a77c4-120">Running the Test</span></span>

<span data-ttu-id="a77c4-121">默认情况下，Test-CsKerberosAccountAssignment 在屏幕上显示非常少的输出。</span><span class="sxs-lookup"><span data-stu-id="a77c4-121">By default, Test-CsKerberosAccountAssignment displays very little output on-screen.</span></span> <span data-ttu-id="a77c4-122">而是将 cmdlet 返回的信息写入 HTML 文件。</span><span class="sxs-lookup"><span data-stu-id="a77c4-122">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="a77c4-123">因此，我们建议你在运行 Test CsKerberosAccountAssignment 时随时包括 Verbose 参数和 Report 参数。</span><span class="sxs-lookup"><span data-stu-id="a77c4-123">Because of that, we recommend that you include the Verbose parameter and the Report parameter any time that you run Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="a77c4-124">在运行 cmdlet 时，Verbose 参数将在屏幕上提供稍有更详细的输出。</span><span class="sxs-lookup"><span data-stu-id="a77c4-124">The Verbose parameter will provide slightly more detailed output on-screen while the cmdlet runs.</span></span> <span data-ttu-id="a77c4-125">Report 参数允许你为由 Test CsKerberosAccountAssignment 生成的 HTML 文件指定文件路径和文件名。</span><span class="sxs-lookup"><span data-stu-id="a77c4-125">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="a77c4-126">如果不包含报表参数，则 HTML 文件将自动保存到 "用户" 文件夹中，并指定如下名称： ce84964a-c4da-4622-ad34-c54ff3ed361f.html。</span><span class="sxs-lookup"><span data-stu-id="a77c4-126">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="a77c4-127">在运行 Test CsKerberosAccountAssignment 时，还必须指定网站标识。</span><span class="sxs-lookup"><span data-stu-id="a77c4-127">You must also specify a site Identity when you run Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="a77c4-128">在网站范围内分配 Kerberos 帐户。</span><span class="sxs-lookup"><span data-stu-id="a77c4-128">Kerberos accounts are assigned at the site scope.</span></span>

<span data-ttu-id="a77c4-129">以下命令将运行 Test-CsKerberosAccountAssignment 并将输出保存到名为 C： \\ LogsKerberosTest.html 的文件中 \\ ：</span><span class="sxs-lookup"><span data-stu-id="a77c4-129">The following command runs Test-CsKerberosAccountAssignment and saves the output to a file that is named C:\\Logs\\KerberosTest.html:</span></span>

    Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "C:\Logs\KerberosTest.html" -Verbose

<span data-ttu-id="a77c4-130">有关详细信息，请参阅 [CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="a77c4-130">For more information, see the Help documentation for the [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="a77c4-131">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="a77c4-131">Determining Success or Failure</span></span>

<span data-ttu-id="a77c4-132">Test-CsKerberosAccountAssignment cmdlet 不会返回对成功或失败的简单指示。</span><span class="sxs-lookup"><span data-stu-id="a77c4-132">The Test-CsKerberosAccountAssignment cmdlet does not return a simple indication of success or failure.</span></span> <span data-ttu-id="a77c4-133">而是必须使用 Internet Explorer 查看生成的 HTML 文件。</span><span class="sxs-lookup"><span data-stu-id="a77c4-133">Instead, you must view the generated HTML file by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="a77c4-134">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="a77c4-134">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="a77c4-135">下面是 Test-CsKerberosAccountAssignment 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="a77c4-135">Here are some common reasons why Test-CsKerberosAccountAssignment might fail:</span></span>

  - <span data-ttu-id="a77c4-136">您可能指定了一个不正确的站点标识。</span><span class="sxs-lookup"><span data-stu-id="a77c4-136">You might have specified an incorrect site Identity.</span></span> <span data-ttu-id="a77c4-137">若要返回有效网站标识的列表，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="a77c4-137">To return a list of valid site Identity, use this command:</span></span>
    
        Get-CsSite | Select-Identity Identity
    
    <span data-ttu-id="a77c4-138">网站标识通常如下所示：</span><span class="sxs-lookup"><span data-stu-id="a77c4-138">A site Identity typically looks as follows:</span></span>
    
    <span data-ttu-id="a77c4-139">网站：雷德蒙</span><span class="sxs-lookup"><span data-stu-id="a77c4-139">site:Redmond</span></span>

  - <span data-ttu-id="a77c4-140">指定网站可能未分配 Kerberos 帐户。</span><span class="sxs-lookup"><span data-stu-id="a77c4-140">The specified site might not have a Kerberos account assigned to it.</span></span> <span data-ttu-id="a77c4-141">你可以通过运行如下命令确定是否将 Kerberos 帐户分配给网站：</span><span class="sxs-lookup"><span data-stu-id="a77c4-141">You can determine whether or not a Kerberos account is assigned to a site by running a command similar to this:</span></span>
    
        Get-CsKerberosAccountAssignment -Identity "site:Redmond"

  - <span data-ttu-id="a77c4-142">您的 Kerberos 帐户可能有一个无效密码。</span><span class="sxs-lookup"><span data-stu-id="a77c4-142">Your Kerberos account might have a password that isn't valid.</span></span> <span data-ttu-id="a77c4-143">如果在报告中收到以下错误消息，您可能需要重置 Kerberos 帐户密码：</span><span class="sxs-lookup"><span data-stu-id="a77c4-143">If you receive the following error message in report, you'll probably have to reset the Kerberos account password:</span></span>
    
    <span data-ttu-id="a77c4-144">InvalidKerberosConfiguration： Kerberos 配置无效。</span><span class="sxs-lookup"><span data-stu-id="a77c4-144">InvalidKerberosConfiguration: The Kerberos configuration is invalid.</span></span>
    
    <span data-ttu-id="a77c4-145">InvalidKerberosConfiguration： atl-cs001.litwareinc.com 上的 Kerberos 配置无效。</span><span class="sxs-lookup"><span data-stu-id="a77c4-145">InvalidKerberosConfiguration: The Kerberos configuration on atl-cs001.litwareinc.com is invalid.</span></span> <span data-ttu-id="a77c4-146">所需的指定帐户为 litwareinc \\ kerberostest。</span><span class="sxs-lookup"><span data-stu-id="a77c4-146">The expected assigned account is litwareinc\\kerberostest.</span></span> <span data-ttu-id="a77c4-147">确保帐户未过期，并且计算机上配置的密码与帐户的 Active Directory 密码相匹配。</span><span class="sxs-lookup"><span data-stu-id="a77c4-147">Ensure that the account has not expired, and the configured password on the machine matches the Active Directory password of the account.</span></span>
    
    <span data-ttu-id="a77c4-148">你可以使用 [CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) cmdlet 设置密码。</span><span class="sxs-lookup"><span data-stu-id="a77c4-148">You can set the password using the [Set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="a77c4-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a77c4-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

