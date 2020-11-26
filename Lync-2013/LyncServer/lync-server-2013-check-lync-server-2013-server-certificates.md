---
title: Lync Server 2013：检查 Lync Server 2013 服务器证书
description: Lync Server 2013：检查 Lync Server 2013 服务器证书。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check server certificates
ms:assetid: 7b0474e8-0efe-47f0-84eb-a1ba575dabfd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725210(v=OCS.15)
ms:contentKeyID: 63969620
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 641651cb425b4fe8bd820bcebfa277084233bb1d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435017"
---
# <a name="check-lync-server-2013-server-certificates"></a><span data-ttu-id="fcc60-103">检查 Lync Server 2013 服务器证书</span><span class="sxs-lookup"><span data-stu-id="fcc60-103">Check Lync Server 2013 server certificates</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fcc60-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fcc60-104">

<span> </span></span></span>

<span data-ttu-id="fcc60-105">_**主题上次修改时间：** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="fcc60-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcc60-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="fcc60-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="fcc60-107">每月</span><span class="sxs-lookup"><span data-stu-id="fcc60-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcc60-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="fcc60-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="fcc60-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fcc60-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcc60-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="fcc60-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="fcc60-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="fcc60-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="fcc60-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Get-CsCertificate cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="fcc60-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Get-CsCertificate cmdlet.</span></span> <span data-ttu-id="fcc60-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="fcc60-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Get-CsCertificate&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="fcc60-114">说明</span><span class="sxs-lookup"><span data-stu-id="fcc60-114">Description</span></span>

<span data-ttu-id="fcc60-115">Get-CsCertificate cmdlet 使你能够检索有关每个 Lync 服务器证书的信息。</span><span class="sxs-lookup"><span data-stu-id="fcc60-115">The Get-CsCertificate cmdlet enables you to retrieve information about each of your Lync Server certificates.</span></span> <span data-ttu-id="fcc60-116">这一点尤其重要，因为证书具有内置的到期日期。</span><span class="sxs-lookup"><span data-stu-id="fcc60-116">That’s especially important because certificates have a built-in expiration date.</span></span> <span data-ttu-id="fcc60-117">例如，私下颁发的证书通常会在12个月后过期。</span><span class="sxs-lookup"><span data-stu-id="fcc60-117">For example,, privately-issued certificates typically expire after 12 months.</span></span> <span data-ttu-id="fcc60-118">如果任何 Lync 服务器证书过期，则将丢失随附的功能，直到续订或替换该证书。</span><span class="sxs-lookup"><span data-stu-id="fcc60-118">If any of your Lync Server certificates expire then you'll lose the accompanying functionality until that certificate is renewed or replaced.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="fcc60-119">运行测试</span><span class="sxs-lookup"><span data-stu-id="fcc60-119">Running the test</span></span>

<span data-ttu-id="fcc60-120">若要返回每个 Lync 服务器证书的信息，只需运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="fcc60-120">To return information about each of your Lync Server certificates just run the following command:</span></span>

`Get-CsCertificate`

<span data-ttu-id="fcc60-121">或者，你可以根据到期日期筛选返回的证书信息。</span><span class="sxs-lookup"><span data-stu-id="fcc60-121">Or, you can filter the return certificate information based on expiration date.</span></span> <span data-ttu-id="fcc60-122">例如，此命令将返回的数据限制为过期 (在 2014 6 月1日之后无法使用的证书) ：</span><span class="sxs-lookup"><span data-stu-id="fcc60-122">For example, this command limits the returned data to certificates that expire (cannot be used after) June 1, 2014:</span></span>

`Get-CsCertificate | Where-Object {$_.NotAfter -lt "6/1/2014"}`

<span data-ttu-id="fcc60-123">有关详细信息，请参阅 Get-CsCertificate cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="fcc60-123">For more information, see the Help documentation for the Get-CsCertificate cmdlet.</span></span>

<span data-ttu-id="fcc60-124">请注意，虽然 Test-CsCertificateConfiguration cmdlet 存在，但对管理员而言不太有用。</span><span class="sxs-lookup"><span data-stu-id="fcc60-124">Note that, although the Test-CsCertificateConfiguration cmdlet exists, it is not very useful to administrators.</span></span> <span data-ttu-id="fcc60-125"> (相反，该 cmdlet 主要由证书向导使用。 ) 尽管此 cmdlet 有效，但它返回的信息是最小值，如以下输出示例中所示：</span><span class="sxs-lookup"><span data-stu-id="fcc60-125">(Instead, that cmdlet is primarily used by the Certificate wizard.) Although the cmdlet works, the information that it returns is of minimal value as shown in the following output example:</span></span>

<span data-ttu-id="fcc60-126">指纹使用</span><span class="sxs-lookup"><span data-stu-id="fcc60-126">Thumbprint Use</span></span>

<span data-ttu-id="fcc60-127">\---------- ---</span><span class="sxs-lookup"><span data-stu-id="fcc60-127">\---------- ---</span></span>

<span data-ttu-id="fcc60-128">A9D51A2911C74FABFF7F2A8A994B20857D399107 默认值</span><span class="sxs-lookup"><span data-stu-id="fcc60-128">A9D51A2911C74FABFF7F2A8A994B20857D399107 Default</span></span>

</div>

<div>

## <a name="reviewing-the-output"></a><span data-ttu-id="fcc60-129">查看输出</span><span class="sxs-lookup"><span data-stu-id="fcc60-129">Reviewing the output</span></span>

<span data-ttu-id="fcc60-130">对于您的每个 Lync 服务器证书，Get-CsCertificate cmdlet 都将返回类似于以下内容的信息：</span><span class="sxs-lookup"><span data-stu-id="fcc60-130">The Get-CsCertificate cmdlet returns information similar to the following for each of your Lync Server certificates:</span></span>

<span data-ttu-id="fcc60-131">颁发者： CN = FabrikamCA</span><span class="sxs-lookup"><span data-stu-id="fcc60-131">Issuer : CN=FabrikamCA</span></span>

<span data-ttu-id="fcc60-132">NotAfter： 12/28/2015 3:35:41 PM</span><span class="sxs-lookup"><span data-stu-id="fcc60-132">NotAfter : 12/28/2015 3:35:41 PM</span></span>

<span data-ttu-id="fcc60-133">NotBefore： 1/2/2014 12:49:37 PM</span><span class="sxs-lookup"><span data-stu-id="fcc60-133">NotBefore : 1/2/2014 12:49:37 PM</span></span>

<span data-ttu-id="fcc60-134">SerialNumber：611BB01200000000000C</span><span class="sxs-lookup"><span data-stu-id="fcc60-134">SerialNumber : 611BB01200000000000C</span></span>

<span data-ttu-id="fcc60-135">主题： CN = LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fcc60-135">Subject : CN=LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="fcc60-136">AlternativeNames： {sip.fabrikam.com，LYNC-SE.fabrikam.com，</span><span class="sxs-lookup"><span data-stu-id="fcc60-136">AlternativeNames : {sip.fabrikam.com, LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="fcc60-137">meet.fabrikam.com、admin.fabrikam.com ...}</span><span class="sxs-lookup"><span data-stu-id="fcc60-137">meet.fabrikam.com, admin.fabrikam.com...}</span></span>

<span data-ttu-id="fcc60-138">指纹： A9D51A2911C74FABFF7F2A8A994B20857D399107</span><span class="sxs-lookup"><span data-stu-id="fcc60-138">Thumbprint : A9D51A2911C74FABFF7F2A8A994B20857D399107</span></span>

<span data-ttu-id="fcc60-139">使用：默认</span><span class="sxs-lookup"><span data-stu-id="fcc60-139">Use : Default</span></span>

<span data-ttu-id="fcc60-140">通常，与 Lync Server 证书有关的首要问题涉及日期和时间，例如当证书在 NotBefore) 或过期时 (NotAfter) 时 (生效。</span><span class="sxs-lookup"><span data-stu-id="fcc60-140">As a rule, the top issues involving Lync Server certificates involve dates and times, such as when certificates take effect (NotBefore) or when they expire (NotAfter).</span></span> <span data-ttu-id="fcc60-141">由于这些日期和时间非常重要，因此你可能希望将返回的数据限制为 "证书使用"、"证书序列号" 和 "证书到期日期" 等信息。然后，你可以快速查看所有证书以及它们何时过期。</span><span class="sxs-lookup"><span data-stu-id="fcc60-141">Because these dates and times are so important, you might want to limit the returned data to information such as the certificate use, the certificate serial number, and the certificate expiration date; then you can quickly review all the certificates and when they will expire.</span></span> <span data-ttu-id="fcc60-142">若要仅返回该信息，请使用该命令以及选项，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fcc60-142">To return just that information, use the command together with the options as shown:</span></span>

`Get-CsCertificate | Select-Object Use, SerialNumber, NotAfter | Sort-Object NotAfter`

<span data-ttu-id="fcc60-143">该命令返回与以下内容类似的数据，其中的证书按其到期日期顺序排序：</span><span class="sxs-lookup"><span data-stu-id="fcc60-143">That command returns data similar to the following, with the certificates sorted in order of their expiration date:</span></span>

<span data-ttu-id="fcc60-144">使用 SerialNumber NotAfter</span><span class="sxs-lookup"><span data-stu-id="fcc60-144">Use SerialNumber NotAfter</span></span>

<span data-ttu-id="fcc60-145">\--- ------------ --------</span><span class="sxs-lookup"><span data-stu-id="fcc60-145">\--- ------------ --------</span></span>

<span data-ttu-id="fcc60-146">默认 611BB01200000000000C 12/28/2015 3:35:41 PM</span><span class="sxs-lookup"><span data-stu-id="fcc60-146">Default 611BB01200000000000C 12/28/2015 3:35:41 PM</span></span>

<span data-ttu-id="fcc60-147">WebServicesInteral 32980AA20BBB20000191 02/15/2016 2:16:12 PM</span><span class="sxs-lookup"><span data-stu-id="fcc60-147">WebServicesInteral 32980AA20BBB20000191 02/15/2016 2:16:12 PM</span></span>

<span data-ttu-id="fcc60-148">WebServicesExternal 0451B012003872651A0C 02/20/2016 7:11:58 AM</span><span class="sxs-lookup"><span data-stu-id="fcc60-148">WebServicesExternal 0451B012003872651A0C 02/20/2016 7:11:58 AM</span></span>

<span data-ttu-id="fcc60-149">如果存在证书问题，可能需要查看为证书配置的 AlternativeNames。</span><span class="sxs-lookup"><span data-stu-id="fcc60-149">If you have certificate problems, you might want to review the AlternativeNames configured for a certificate.</span></span> <span data-ttu-id="fcc60-150">乍一看，这似乎是一个问题。</span><span class="sxs-lookup"><span data-stu-id="fcc60-150">At first glance, that seems to be a problem.</span></span> <span data-ttu-id="fcc60-151">默认情况下，根据控制台窗口的大小，Get-CsCertificate 可能无法显示所有名称：</span><span class="sxs-lookup"><span data-stu-id="fcc60-151">By default, and depending on the size of your console window, Get-CsCertificate might not be able to display all the names:</span></span>

<span data-ttu-id="fcc60-152">AlternativeNames： {sip.fabrikam.com，LYNC.fabrikam.com，</span><span class="sxs-lookup"><span data-stu-id="fcc60-152">AlternativeNames : {sip.fabrikam.com, LYNC.fabrikam.com,</span></span>

<span data-ttu-id="fcc60-153">meet.fabrikam.com、fabrika ...}</span><span class="sxs-lookup"><span data-stu-id="fcc60-153">meet.fabrikam.com, admin.fabrika...}</span></span>

<span data-ttu-id="fcc60-154">若要查看分配给证书的所有替代名称，请使用类似于下面的命令：</span><span class="sxs-lookup"><span data-stu-id="fcc60-154">To see all the alternative names assigned to a certificate use a command similar to this one:</span></span>

`Get-CsCertificate | Where-Object {$_.SerialNumber -eq "611BB01200000000000C"} | Select-Object -ExpandProperty AlternativeNames`

<span data-ttu-id="fcc60-155">这应显示证书上的所有备用名称：</span><span class="sxs-lookup"><span data-stu-id="fcc60-155">That should show you all of the alternative names on the certificate:</span></span>

<span data-ttu-id="fcc60-156">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fcc60-156">sip.fabrikam.com</span></span>

<span data-ttu-id="fcc60-157">LYNC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fcc60-157">LYNC.fabrikam.com</span></span>

<span data-ttu-id="fcc60-158">meet.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fcc60-158">meet.fabrikam.com</span></span>

<span data-ttu-id="fcc60-159">admin.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fcc60-159">admin.fabrikam.com</span></span>

<span data-ttu-id="fcc60-160">LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fcc60-160">LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="fcc60-161">Dialin.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fcc60-161">Dialin.fabrikam.com</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fcc60-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fcc60-162">See Also</span></span>


[<span data-ttu-id="fcc60-163">Get-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="fcc60-163">Get-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCertificate)  
  

<span data-ttu-id="fcc60-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fcc60-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

