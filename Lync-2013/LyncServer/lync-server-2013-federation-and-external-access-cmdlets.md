---
title: Lync Server 2013：联盟和外部访问 cmdlet
description: Lync Server 2013：联盟和外部访问 cmdlet。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Federation and external access cmdlets
ms:assetid: 4a384a57-257f-47a6-98d9-54cea2c647b7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415651(v=OCS.15)
ms:contentKeyID: 48184018
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 930de66a54d3f8db07394baf2d8470affe5090e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428193"
---
# <a name="federation-and-external-access-cmdlets-in-lync-server-2013"></a><span data-ttu-id="8ad57-103">Lync Server 2013 中的联盟和外部访问 cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ad57-103">Federation and external access cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ad57-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ad57-104">

<span> </span></span></span>

<span data-ttu-id="8ad57-105">_**主题上次修改时间：** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="8ad57-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="8ad57-106">联盟和外部访问提供两个重要功能：联盟使用户能够与组织外部的人员进行通信，而外部访问使用户能够从内部网络外部连接到 Microsoft Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="8ad57-106">Federation and external access provide two important capabilities: federation enables users to communicate with people outside your organization, while external access enables users to connect to Microsoft Lync Server 2013 from outside the internal network.</span></span> <span data-ttu-id="8ad57-107">在 Lync Server 2013 中可用于管理联盟和外部访问的 cmdlet 使你可以确定你的用户可以 (和无法) 通信的用户，并确定这些用户是否可以连接到 Lync 服务器，而无需登录到内部网络。</span><span class="sxs-lookup"><span data-stu-id="8ad57-107">The cmdlets available for managing federation and external access in Lync Server 2013 let you determine who your users can (and cannot) communicate with, and determine whether or not those users can connect to Lync Server without having to log on to the internal network.</span></span>

<div>

## <a name="federation-and-external-access-cmdlets"></a><span data-ttu-id="8ad57-108">联盟和外部访问 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ad57-108">Federation and External Access Cmdlets</span></span>

<span data-ttu-id="8ad57-109">可从 Lync Server 控制面板执行大多数适用于联盟和外部访问的管理任务。</span><span class="sxs-lookup"><span data-stu-id="8ad57-109">Most management tasks that apply to federation and external access can be performed from the Lync Server Control Panel.</span></span> <span data-ttu-id="8ad57-110">可以使用 Lync Server 命令行管理程序或脚本中的 cmdlet 执行这些相同的任务;使用脚本可以自动执行某些任务。</span><span class="sxs-lookup"><span data-stu-id="8ad57-110">These same tasks can be performed using cmdlets from the Lync Server Management Shell or from within a script; using a script enables you to automate certain tasks.</span></span> <span data-ttu-id="8ad57-111">下面是与管理联盟和外部访问权限直接相关的 cmdlet 的列表：</span><span class="sxs-lookup"><span data-stu-id="8ad57-111">The following is a list of cmdlets that relate directly to managing federation and external access:</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-112">[CsAllowedDomain](https://technet.microsoft.com/library/Gg398164(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-112">[Get-CsAllowedDomain](https://technet.microsoft.com/library/Gg398164(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-113">[新-CsAllowedDomain](https://technet.microsoft.com/library/Gg398628(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-113">[New-CsAllowedDomain](https://technet.microsoft.com/library/Gg398628(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-114">[Remove-CsAllowedDomain](https://technet.microsoft.com/library/Gg398913(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-114">[Remove-CsAllowedDomain](https://technet.microsoft.com/library/Gg398913(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-115">[Set-CsAllowedDomain](https://technet.microsoft.com/library/Gg398931(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-115">[Set-CsAllowedDomain](https://technet.microsoft.com/library/Gg398931(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="8ad57-116">[CsBlockedDomain](https://technet.microsoft.com/library/Gg398424(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-116">[Get-CsBlockedDomain](https://technet.microsoft.com/library/Gg398424(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-117">[新-CsBlockedDomain](https://technet.microsoft.com/library/Gg398822(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-117">[New-CsBlockedDomain](https://technet.microsoft.com/library/Gg398822(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-118">[Remove-CsBlockedDomain](https://technet.microsoft.com/library/Gg425832(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-118">[Remove-CsBlockedDomain](https://technet.microsoft.com/library/Gg425832(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-119">[Set-CsBlockedDomain](https://technet.microsoft.com/library/Gg398090(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-119">[Set-CsBlockedDomain](https://technet.microsoft.com/library/Gg398090(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="8ad57-120">[CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg425805(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-120">[Get-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg425805(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-121">[授权-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg425942(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-121">[Grant-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg425942(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-122">[新-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg398441(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-122">[New-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg398441(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-123">[Remove-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg399057(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-123">[Remove-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg399057(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-124">[Set-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg398916(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-124">[Set-CsExternalAccessPolicy](https://technet.microsoft.com/library/Gg398916(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="8ad57-125">[Get-CsFIPSConfiguration](https://technet.microsoft.com/library/JJ204904(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-125">[Get-CsFIPSConfiguration](https://technet.microsoft.com/library/JJ204904(v=OCS.15))</span></span>

  - <span data-ttu-id="8ad57-126">[New-CsFIPSConfiguration](https://technet.microsoft.com/library/JJ205114(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-126">[New-CsFIPSConfiguration](https://technet.microsoft.com/library/JJ205114(v=OCS.15))</span></span>

  - <span data-ttu-id="8ad57-127">[Remove-CsFIPSConfiguration](https://technet.microsoft.com/library/JJ205201(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-127">[Remove-CsFIPSConfiguration](https://technet.microsoft.com/library/JJ205201(v=OCS.15))</span></span>

  - <span data-ttu-id="8ad57-128">[Set-CsFIPSConfiguration](https://technet.microsoft.com/library/JJ205084(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-128">[Set-CsFIPSConfiguration](https://technet.microsoft.com/library/JJ205084(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="8ad57-129">[Disable-CsHostingProvider](https://technet.microsoft.com/library/Gg398481(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-129">[Disable-CsHostingProvider](https://technet.microsoft.com/library/Gg398481(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-130">[Enable-CsHostingProvider](https://technet.microsoft.com/library/Gg398166(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-130">[Enable-CsHostingProvider](https://technet.microsoft.com/library/Gg398166(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-131">[CsHostingProvider](https://technet.microsoft.com/library/Gg413078(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-131">[Get-CsHostingProvider](https://technet.microsoft.com/library/Gg413078(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-132">[新-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-132">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-133">[Remove-CsHostingProvider](https://technet.microsoft.com/library/Gg425809(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-133">[Remove-CsHostingProvider](https://technet.microsoft.com/library/Gg425809(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-134">[Set-CsHostingProvider](https://technet.microsoft.com/library/Gg398532(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-134">[Set-CsHostingProvider](https://technet.microsoft.com/library/Gg398532(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="8ad57-135">[Disable-CsPublicProvider](https://technet.microsoft.com/library/Gg398984(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-135">[Disable-CsPublicProvider](https://technet.microsoft.com/library/Gg398984(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-136">[Enable-CsPublicProvider](https://technet.microsoft.com/library/Gg398780(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-136">[Enable-CsPublicProvider](https://technet.microsoft.com/library/Gg398780(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-137">[CsPublicProvider](https://technet.microsoft.com/library/Gg412945(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-137">[Get-CsPublicProvider](https://technet.microsoft.com/library/Gg412945(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-138">[新-CsPublicProvider](https://technet.microsoft.com/library/Gg398161(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-138">[New-CsPublicProvider](https://technet.microsoft.com/library/Gg398161(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-139">[Remove-CsPublicProvider](https://technet.microsoft.com/library/Gg412906(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-139">[Remove-CsPublicProvider](https://technet.microsoft.com/library/Gg412906(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="8ad57-140">[Set-CsPublicProvider](https://technet.microsoft.com/library/Gg413087(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-140">[Set-CsPublicProvider](https://technet.microsoft.com/library/Gg413087(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="8ad57-141">[Test-CsFederatedPartner](https://technet.microsoft.com/library/Gg398281(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-141">[Test-CsFederatedPartner](https://technet.microsoft.com/library/Gg398281(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="8ad57-142">[Get-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ204981(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-142">[Get-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ204981(v=OCS.15))</span></span>

  - <span data-ttu-id="8ad57-143">[New-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ204631(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-143">[New-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ204631(v=OCS.15))</span></span>

  - <span data-ttu-id="8ad57-144">[Remove-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ205055(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-144">[Remove-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ205055(v=OCS.15))</span></span>

  - <span data-ttu-id="8ad57-145">[Set-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ204686(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-145">[Set-CsXmppAllowedPartner](https://technet.microsoft.com/library/JJ204686(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="8ad57-146">[Get-CsXmppGatewayConfiguration](https://technet.microsoft.com/library/JJ204869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-146">[Get-CsXmppGatewayConfiguration](https://technet.microsoft.com/library/JJ204869(v=OCS.15))</span></span>

  - <span data-ttu-id="8ad57-147">[Set-CsXmppGatewayConfiguration](https://technet.microsoft.com/library/JJ204769(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-147">[Set-CsXmppGatewayConfiguration](https://technet.microsoft.com/library/JJ204769(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="8ad57-148">[Test-CsXmppIM](https://technet.microsoft.com/library/JJ205423(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="8ad57-148">[Test-CsXmppIM](https://technet.microsoft.com/library/JJ205423(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8ad57-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8ad57-149">See Also</span></span>


[<span data-ttu-id="8ad57-150">Lync Server PowerShell 博客</span><span class="sxs-lookup"><span data-stu-id="8ad57-150">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="8ad57-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ad57-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

