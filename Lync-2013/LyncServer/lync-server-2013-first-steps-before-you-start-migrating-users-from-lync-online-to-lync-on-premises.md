---
title: Lync Server 2013：开始将用户从 Lync Online 迁移到本地 Lync 之前的第一步
description: Lync Server 2013：开始将用户从 Lync Online 迁移到本地 Lync 之前的第一步。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: First steps before you start migrating users from Lync Online to Lync on-premises
ms:assetid: 98245b04-ded4-4186-8da3-ba1c554b5c39
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689118(v=OCS.15)
ms:contentKeyID: 62258123
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 408820e461c0a9f7c0beaaaae3a502802048d3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428116"
---
# <a name="first-steps-before-you-start-migrating-users-from-lync-online-to-lync-on-premises-in-lync-server-2013"></a><span data-ttu-id="d1e29-103">在 Lync Server 2013 中开始将用户从 Lync Online 迁移到本地 Lync 之前的第一步</span><span class="sxs-lookup"><span data-stu-id="d1e29-103">First steps before you start migrating users from Lync Online to Lync on-premises in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1e29-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1e29-104">

<span> </span></span></span>

<span data-ttu-id="d1e29-105">_**主题上次修改时间：** 2014-05-08_</span><span class="sxs-lookup"><span data-stu-id="d1e29-105">_**Topic Last Modified:** 2014-05-08_</span></span>

<span data-ttu-id="d1e29-106">在开始将 Lync Online 用户移动到本地环境之前，请检查以下所有条件是否为 true：</span><span class="sxs-lookup"><span data-stu-id="d1e29-106">Before you start moving Lync Online users to your on-premises environment, check that all of the following are true:</span></span>

  - <span data-ttu-id="d1e29-107">您的 Lync Server 本地环境必须完全部署和验证。</span><span class="sxs-lookup"><span data-stu-id="d1e29-107">Your Lync Server on-premises environment must be fully deployed and validated.</span></span> <span data-ttu-id="d1e29-108">有关详细信息，请参阅 [部署 Lync Server 2013](lync-server-2013-deploying-lync-server.md)。</span><span class="sxs-lookup"><span data-stu-id="d1e29-108">For more information, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md).</span></span>

  - <span data-ttu-id="d1e29-109">必须为远程 PowerShell 访问配置 Lync Online 租户。</span><span class="sxs-lookup"><span data-stu-id="d1e29-109">Your Lync Online tenant must be configured for remote PowerShell Access.</span></span>
    
    <span data-ttu-id="d1e29-110">若要执行此操作，请首先安装适用于 Windows PowerShell 的 Lync Online 模块，可在此处获取： [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911) 。</span><span class="sxs-lookup"><span data-stu-id="d1e29-110">To do this, first install the Lync Online module for Windows PowerShell, which you can get here: [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911).</span></span>
    
    <span data-ttu-id="d1e29-111">安装该模块后，您可以通过在 Lync Server Management Shell 中键入以下 cmdlet 来建立远程会话：</span><span class="sxs-lookup"><span data-stu-id="d1e29-111">After you install the module, you can establish a remote session by typing the following cmdlets in the Lync Server Management Shell:</span></span>
    
       ```PowerShell
        Import-Module LyncOnlineConnector
       ```  
    
       ```PowerShell
        $cred = Get-Credential
       ``` 
    
       ```PowerShell
        $CSSession = New-CsOnlineSession -Credential $cred
       ```
    
       ```PowerShell
        Import-PSSession $CSSession -AllowClobber
       ```
    
    <span data-ttu-id="d1e29-112">有关如何建立与 Lync Online 的远程 PowerShell 会话的详细信息，请参阅 [使用 Windows PowerShell 连接到 Lync online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="d1e29-112">For more information about how to establish a remote PowerShell session with Lync Online, see [Connecting to Lync Online by using Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>
  
    <span data-ttu-id="d1e29-113">有关使用 Lync Online PowerShell 模块的详细信息，请参阅 [使用 Windows PowerShell 管理 Lync online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="d1e29-113">For more information about using the Lync Online PowerShell module, see [Using Windows PowerShell to manage Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

  - <span data-ttu-id="d1e29-114">必须为共享 SIP 地址空间配置您的 Lync Online。</span><span class="sxs-lookup"><span data-stu-id="d1e29-114">Your Lync Online must be configured for Shared SIP Address Space.</span></span> <span data-ttu-id="d1e29-115">若要执行此操作，请首先启动与 Lync Online 的远程 Powershell 会话。</span><span class="sxs-lookup"><span data-stu-id="d1e29-115">To do this, first start a remote Powershell session with Lync Online.</span></span> <span data-ttu-id="d1e29-116">然后运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d1e29-116">Then run the following cmdlet:</span></span>
    
        Set-CsTenantFederationConfiguration -SharedSipAddressSpace $True

<span data-ttu-id="d1e29-117">完成这些步骤后，您可以继续在 [Lync Server 2013 中将 Lync Online 用户迁移到本地 lync](lync-server-2013-migrating-lync-online-users-to-lync-on-premises.md)。</span><span class="sxs-lookup"><span data-stu-id="d1e29-117">After you’ve finished these steps, you can move on to [Migrating Lync Online users to Lync on-premises in Lync Server 2013](lync-server-2013-migrating-lync-online-users-to-lync-on-premises.md).</span></span>

<span data-ttu-id="d1e29-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1e29-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

