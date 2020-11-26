---
title: Lync Server 2013：将响应组移动到新池
description: Lync Server 2013：将响应组移动到新池。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Moving response groups to a new pool
ms:assetid: da0db765-41e5-430b-b5a7-5418ec5ff2a7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205298(v=OCS.15)
ms:contentKeyID: 48185538
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b696963a28abbcd258f53fae12c3e281efa6ae4d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425260"
---
# <a name="moving-response-groups-to-a-new-pool-in-lync-server-2013"></a><span data-ttu-id="a128c-103">将响应组移动到 Lync Server 2013 中的新池</span><span class="sxs-lookup"><span data-stu-id="a128c-103">Moving response groups to a new pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a128c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a128c-104">

<span> </span></span></span>

<span data-ttu-id="a128c-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a128c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a128c-106">Lync Server 2013 引入了新 cmdlet 支持，用于将响应组从一个池移动到另一个池，即使完全限定的域名 (FQDN) 不同。</span><span class="sxs-lookup"><span data-stu-id="a128c-106">Lync Server 2013 introduces new cmdlet support for moving response groups from one pool to another pool, even when the fully qualified domain name (FQDN) is different.</span></span>

<span data-ttu-id="a128c-107">使用以下过程中的步骤将响应组从一个前端池移动到另一个具有不同 FQDN 的前端池。</span><span class="sxs-lookup"><span data-stu-id="a128c-107">Use the steps in the following procedure to move response groups from one Front End pool to another Front End pool with a different FQDN.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a128c-108">在共存环境中，只能在 Lync Server 2013 前端池之间移动响应组 &nbsp; 。</span><span class="sxs-lookup"><span data-stu-id="a128c-108">In a coexistence environment, you can move response groups only between Lync Server 2013&nbsp;Front End pools.</span></span>



</div>

<div>

## <a name="to-move-response-groups-to-a-pool-with-a-different-fqdn"></a><span data-ttu-id="a128c-109">将响应组移动到具有不同 FQDN 的池</span><span class="sxs-lookup"><span data-stu-id="a128c-109">To move response groups to a pool with a different FQDN</span></span>

1.  <span data-ttu-id="a128c-110">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="a128c-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a128c-111">导出源池中的响应组。</span><span class="sxs-lookup"><span data-stu-id="a128c-111">Export the response groups in the source pool.</span></span> <span data-ttu-id="a128c-112">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="a128c-112">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<source FQDN>" -FileName "<export file name>"
    
    <span data-ttu-id="a128c-113">例如：</span><span class="sxs-lookup"><span data-stu-id="a128c-113">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:source.contoso.com" -FileName "C:\RgsExportSource.zip"
    
    <span data-ttu-id="a128c-114">若要在导出期间从源池中删除响应组，请包括-RemoveExportedConfiguration 参数。</span><span class="sxs-lookup"><span data-stu-id="a128c-114">To remove the response groups from the source pool during the export, include the –RemoveExportedConfiguration parameter.</span></span> <span data-ttu-id="a128c-115">例如：</span><span class="sxs-lookup"><span data-stu-id="a128c-115">For example:</span></span>
    
        Export-CsRgsConfiguration -Source ApplicationServer:source.contoso.com -FileName "C:\RgsExportSource.zip" -RemoveExportedConfiguration

3.  <span data-ttu-id="a128c-116">将响应组导入目标池，并将目标池分配为新所有者。</span><span class="sxs-lookup"><span data-stu-id="a128c-116">Import the response groups to the destination pool and assign the destination pool as the new owner.</span></span> <span data-ttu-id="a128c-117">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="a128c-117">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<destination pool>" -FileName "<export file name>" -OverwriteOwner
    
    <span data-ttu-id="a128c-118">如果你还希望将 "响应组" 应用程序级别的设置从源池中复制到目标池，请包括-ReplaceExistingRgsSettings 参数。</span><span class="sxs-lookup"><span data-stu-id="a128c-118">If you also want to copy the Response Group application-level settings from the source pool to the destination pool, include the –ReplaceExistingRgsSettings parameter.</span></span> <span data-ttu-id="a128c-119">你只能针对每个池定义一组应用程序级别设置。</span><span class="sxs-lookup"><span data-stu-id="a128c-119">You can define only one set of application-level settings per pool.</span></span> <span data-ttu-id="a128c-120">如果将应用程序级别的设置从源池复制到目标池，源池中的设置将替换目标池的设置。</span><span class="sxs-lookup"><span data-stu-id="a128c-120">If you copy the application-level settings from the source pool to the destination pool, the settings from the source pool replace the settings for the destination pool.</span></span> <span data-ttu-id="a128c-121">如果不从源池中复制应用程序级别的设置，则目标池中的现有设置将应用于导入的响应组。</span><span class="sxs-lookup"><span data-stu-id="a128c-121">If you do not copy the application-level settings from the source pool, the existing settings from the destination pool apply to the imported response groups.</span></span>
    
    <span data-ttu-id="a128c-122">例如：</span><span class="sxs-lookup"><span data-stu-id="a128c-122">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:destination.contoso.com" -FileName "C:\RgsExportSource.zip" -OverwriteOwner -ReplaceExistingRgsSettings
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a128c-123">应用程序级设置包括默认的音乐保留配置、默认的音乐保留音频文件、代理 ringback 宽限期和调用上下文配置。</span><span class="sxs-lookup"><span data-stu-id="a128c-123">Application-level settings include the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span> <span data-ttu-id="a128c-124">若要查看这些配置设置，请运行 <STRONG>CsRgsConfiguration</STRONG> cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a128c-124">To view these configuration settings, run the <STRONG>Get-CsRgsConfiguration</STRONG> cmdlet.</span></span> <span data-ttu-id="a128c-125">有关此 cmdlet 的详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration">CsRgsConfiguration</A>。</span><span class="sxs-lookup"><span data-stu-id="a128c-125">For details about this cmdlet, see <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration">Get-CsRgsConfiguration</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="a128c-126">通过执行以下操作来验证导入是否成功：显示导入的响应组配置：</span><span class="sxs-lookup"><span data-stu-id="a128c-126">Verify that the import was successful by displaying the imported response group configuration by doing the following:</span></span>
    
      - <span data-ttu-id="a128c-127">验证导入了所有工作流。</span><span class="sxs-lookup"><span data-stu-id="a128c-127">Verify that all the workflows were imported.</span></span> <span data-ttu-id="a128c-128">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="a128c-128">At the command line, type the following:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="a128c-129">验证是否已导入所有队列。</span><span class="sxs-lookup"><span data-stu-id="a128c-129">Verify that all the queues were imported.</span></span> <span data-ttu-id="a128c-130">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="a128c-130">At the command line, type the following:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="a128c-131">验证是否已导入所有代理组。</span><span class="sxs-lookup"><span data-stu-id="a128c-131">Verify that all the agent groups were imported.</span></span> <span data-ttu-id="a128c-132">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="a128c-132">At the command line, type the following:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="a128c-133">验证是否已导入所有营业时间。</span><span class="sxs-lookup"><span data-stu-id="a128c-133">Verify that all the hours of business were imported.</span></span> <span data-ttu-id="a128c-134">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="a128c-134">At the command line, type the following:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<destination pool FQDN>" 
    
      - <span data-ttu-id="a128c-135">验证是否已导入所有假日集。</span><span class="sxs-lookup"><span data-stu-id="a128c-135">Verify that all the holiday sets were imported.</span></span> <span data-ttu-id="a128c-136">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="a128c-136">At the command line, type the following:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<destination pool FQDN>" 

5.  <span data-ttu-id="a128c-137">通过将呼叫放到其中一个响应组并验证是否正确处理了呼叫，验证导入是否成功。</span><span class="sxs-lookup"><span data-stu-id="a128c-137">Verify that the import was successful by placing a call to one of the response groups and verifying that the call is handled correctly.</span></span>

6.  <span data-ttu-id="a128c-138">请求代理是正式代理组的成员，以便登录到目标池中的代理组。</span><span class="sxs-lookup"><span data-stu-id="a128c-138">Request agents who are members of formal agent groups to sign in to their agent groups in the destination pool.</span></span>

7.  <span data-ttu-id="a128c-139">如果以前没有从源池中删除响应组，请从源池中删除响应组。</span><span class="sxs-lookup"><span data-stu-id="a128c-139">If you did not previously remove response groups from the source pool, remove the response groups from the source pool.</span></span> <span data-ttu-id="a128c-140">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="a128c-140">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<source pool FQDN> -RemoveExportedConfiguration -FileName "<temporary export file name>"
    
    <span data-ttu-id="a128c-141">例如：</span><span class="sxs-lookup"><span data-stu-id="a128c-141">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:source.contoso.com" -RemoveExportedConfiguration -FileName "C:\TempRGsConfiguration.zip"

<span data-ttu-id="a128c-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a128c-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

