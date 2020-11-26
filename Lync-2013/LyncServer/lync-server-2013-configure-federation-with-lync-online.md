---
title: Lync Server 2013：配置与 Lync Online 的联盟
description: Lync Server 2013：配置与 Lync Online 的联盟。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure federation with Lync Online
ms:assetid: a10bd1d5-c003-46db-9f57-7d55d3fa08da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205126(v=OCS.15)
ms:contentKeyID: 48184946
ms.date: 08/15/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f3372a76b5ff7ad9dde5a00fd562b74877bd679a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434030"
---
# <a name="configure-federation-of-lync-server-2013-with-lync-online"></a><span data-ttu-id="10dc7-103">配置 Lync Server 2013 与 Lync Online 的联合</span><span class="sxs-lookup"><span data-stu-id="10dc7-103">Configure federation of Lync Server 2013 with Lync Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10dc7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10dc7-104">

<span> </span></span></span>

<span data-ttu-id="10dc7-105">_**主题上次修改时间：** 2016-08-15_</span><span class="sxs-lookup"><span data-stu-id="10dc7-105">_**Topic Last Modified:** 2016-08-15_</span></span>

<span data-ttu-id="10dc7-106">按照本部分中的步骤配置本地部署和 Skype for Business Online 之间的互操作性。</span><span class="sxs-lookup"><span data-stu-id="10dc7-106">Follow the steps in this section to configure interoperability between your on-premises deployment and Skype for Business Online.</span></span>

<span id="a"></span>

<div>

## <a name="configure-your-on-premises-edge-service-for-federation-with-skype-for-business-online"></a><span data-ttu-id="10dc7-107">为具有 Skype for business Online 的联盟配置本地边缘服务</span><span class="sxs-lookup"><span data-stu-id="10dc7-107">Configure Your On-Premises Edge Service for Federation with Skype for Business Online</span></span>

<span data-ttu-id="10dc7-108">联合身份验证允许本地部署中的用户与你的组织中的 Microsoft 365 或 Office 365 用户进行通信。</span><span class="sxs-lookup"><span data-stu-id="10dc7-108">Federation allows users in your on-premises deployment to communicate with Microsoft 365 or Office 365 users in your organization.</span></span> <span data-ttu-id="10dc7-109">若要配置联盟，请运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="10dc7-109">To configure federation, run the following cmdlets:</span></span>

   ```powershell
    Set-CSAccessEdgeConfiguration -AllowOutsideUsers 1 -AllowFederatedUsers 1 -UseDnsSrvRouting -EnablePartnerDiscovery $True
   ```

   ```powershell
    New-CSHostingProvider -Identity LyncOnline -ProxyFqdn "sipfed.online.lync.com" -Enabled $true -EnabledSharedAddressSpace $true -HostsOCSUsers $true -VerificationLevel UseSourceVerification -IsLocal $false -AutodiscoverUrl https://webdir.online.lync.com/Autodiscover/AutodiscoverService.svc/root
   ```

</div>

<span id="b"></span>

<div>

## <a name="configure-your-skype-for-business-online-tenant-for-a-shared-sip-address-space"></a><span data-ttu-id="10dc7-110">为共享 SIP 地址空间配置 Skype for Business Online 租户</span><span class="sxs-lookup"><span data-stu-id="10dc7-110">Configure Your Skype for Business Online Tenant for a Shared SIP Address Space</span></span>

<span data-ttu-id="10dc7-111">会话初始协议 (SIP) 地址是网络上每个用户的唯一标识符，类似于电话号码或电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="10dc7-111">A Session Initiation Protocol (SIP) address is a unique identifier for each user on a network, similar to a phone number or an email address.</span></span> <span data-ttu-id="10dc7-112">在尝试将 Lync 用户从本地移动到 Skype for business Online 之前，你需要将 Microsoft 365 或 Office 365 组织配置为与本地部署 (SIP) 地址空间共享共享会话初始协议。</span><span class="sxs-lookup"><span data-stu-id="10dc7-112">Before you try to move Lync users from on-premises to Skype for Business Online, you’ll need to configure your Microsoft 365 or Office 365 organization to share the Shared Session Initiation Protocol (SIP) address space with your on-premises deployment.</span></span> <span data-ttu-id="10dc7-113">如果未进行此配置，您可能会看到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="10dc7-113">If this is not configured, you may see the following error message:</span></span>

<span data-ttu-id="10dc7-114">Move-CsUser : HostedMigration 错误: Error=(510), 描述=(没有为此用户的租户启用共享 sip 地址空间。)</span><span class="sxs-lookup"><span data-stu-id="10dc7-114">Move-CsUser : HostedMigration fault: Error=(510), Description=(This user’s tenant is not enabled for shared sip address space.)</span></span>

<span data-ttu-id="10dc7-115">若要配置共享 SIP 地址空间，请建立与 Skype for Business Online 的远程 PowerShell 会话，然后运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="10dc7-115">To configure a shared SIP address space, establish a remote PowerShell session with Skype for Business Online, and then run the following cmdlet:</span></span>
```powershell
Set-CsTenantFederationConfiguration -SharedSipAddressSpace $true
```
<span data-ttu-id="10dc7-116">若要建立与 Skype for Business Online 的远程 PowerShell 会话，首先需要安装适用于 Windows PowerShell 的 Skype for Business Online 模块，可在此处下载： [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911) 。</span><span class="sxs-lookup"><span data-stu-id="10dc7-116">To establish a remote PowerShell session with Skype for Business Online, you first need to install the Skype for Business Online module for Windows PowerShell, which you can get here: [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911).</span></span>

<span data-ttu-id="10dc7-117">安装该模块后，您可以使用下列 cmdlet 建立远程会话：</span><span class="sxs-lookup"><span data-stu-id="10dc7-117">After you install the module, you can establish a remote session with the following cmdlets:</span></span>

   ```powershell
    Import-Module LyncOnlineConnector
   ```

   ```powershell
    $cred = Get-Credential
   ``` 

   ```powershell
    $CSSession = New-CsOnlineSession -Credential $cred
   ```

   ```powershell
    Import-PSSession $CSSession -AllowClobber
   ```

<span data-ttu-id="10dc7-118">有关如何建立与 Skype for Business Online 的远程 PowerShell 会话的详细信息，请参阅 [使用 Windows PowerShell 连接到 skype for Business online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="10dc7-118">For more information about how to establish a remote PowerShell session with Skype for Business Online, see [Connecting to Skype for Business Online by using Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

<span data-ttu-id="10dc7-119">有关使用 Skype for Business Online PowerShell 模块的详细信息，请参阅 [使用 Windows PowerShell 管理 skype For Business online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="10dc7-119">For more information about using the Skype for Business Online PowerShell module, see [Using Windows PowerShell to manage Skype for Business Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="10dc7-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="10dc7-120">See Also</span></span>


[<span data-ttu-id="10dc7-121">新-CsHostingProvider</span><span class="sxs-lookup"><span data-stu-id="10dc7-121">New-CsHostingProvider</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostingProvider)  
  

<span data-ttu-id="10dc7-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10dc7-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
