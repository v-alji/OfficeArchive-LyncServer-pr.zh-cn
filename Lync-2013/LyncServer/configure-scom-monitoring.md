---
title: 配置 SCOM 监控
description: 配置 SCOM 监视。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure SCOM monitoring
ms:assetid: 4003d225-2a33-448c-abd9-571750661140
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688033(v=OCS.15)
ms:contentKeyID: 49733624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c93e10c705a1a1e08972d7534e00a33c472d23a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391892"
---
# <a name="configure-scom-monitoring"></a><span data-ttu-id="2b454-103">配置 SCOM 监控</span><span class="sxs-lookup"><span data-stu-id="2b454-103">Configure SCOM monitoring</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b454-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b454-104">

<span> </span></span></span>

<span data-ttu-id="2b454-105">_**主题上次修改时间：** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="2b454-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="2b454-106">迁移到 Microsoft Lync Server 2013 后，必须完成一些任务，才能将 Lync Server 2013 配置为使用 System Center Operations Manager。</span><span class="sxs-lookup"><span data-stu-id="2b454-106">After migrating to Microsoft Lync Server 2013, you must complete a few tasks to configure Lync Server 2013 to work with System Center Operations Manager.</span></span>

  - <span data-ttu-id="2b454-107">将 Lync Server 2010 更新应用到选择的服务器以管理集中发现逻辑。</span><span class="sxs-lookup"><span data-stu-id="2b454-107">Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.</span></span>

  - <span data-ttu-id="2b454-108">更新中央发现候选服务器注册表项。</span><span class="sxs-lookup"><span data-stu-id="2b454-108">Update the central discovery candidate server registry key.</span></span>

  - <span data-ttu-id="2b454-109">将您的主 System Center Operations Manager 管理服务器配置为替代候选中央发现节点。</span><span class="sxs-lookup"><span data-stu-id="2b454-109">Configure your primary System Center Operations Manager management server to override the candidate central discovery node.</span></span>

<span data-ttu-id="2b454-110">下面提供了有关执行其中每项任务的说明。</span><span class="sxs-lookup"><span data-stu-id="2b454-110">Instructions for carrying out each of these tasks are provided below.</span></span>

<span data-ttu-id="2b454-111">**将 Lync Server 2010 更新应用到选择的服务器以管理集中发现逻辑。**</span><span class="sxs-lookup"><span data-stu-id="2b454-111">**Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.**</span></span>

1.  <span data-ttu-id="2b454-112">选择安装了 System Center Operations Manager 代理文件的服务器，并将其配置为候选发现节点。</span><span class="sxs-lookup"><span data-stu-id="2b454-112">Elect a server that has the System Center Operations Manager agent files installed and is configured as a candidate discovery node.</span></span>

2.  <span data-ttu-id="2b454-113">将 Lync Server 2010 更新应用于此服务器。</span><span class="sxs-lookup"><span data-stu-id="2b454-113">Apply Lync Server 2010 updates to this server.</span></span> <span data-ttu-id="2b454-114">请参阅 [应用 Lync Server 2010 更新](apply-lync-server-2010-updates.md)主题。</span><span class="sxs-lookup"><span data-stu-id="2b454-114">See the topic [Apply Lync Server 2010 updates](apply-lync-server-2010-updates.md).</span></span>

<span data-ttu-id="2b454-115">**更新中央发现候选服务器注册表项。**</span><span class="sxs-lookup"><span data-stu-id="2b454-115">**Update the central discovery candidate server registry key.**</span></span>

1.  <span data-ttu-id="2b454-116">在选择了管理中心发现逻辑的服务器上，打开 Windows PowerShell 命令窗口。</span><span class="sxs-lookup"><span data-stu-id="2b454-116">On the server elected to manage the central discovery logic, open a Windows PowerShell command window.</span></span>

2.  <span data-ttu-id="2b454-117">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="2b454-117">At the command line, type the following:</span></span>
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health"
       ```
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health\CentralDiscoveryCandidate"
       ```
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="2b454-118">编辑注册表时，如果注册表项已存在，则可能会遇到错误：命令失败。</span><span class="sxs-lookup"><span data-stu-id="2b454-118">Whenever you edit the registry, you may experience an error that the command failed if the registry key already exists.</span></span> <span data-ttu-id="2b454-119">如果遇到这种情况，您可以安全地忽略该错误。</span><span class="sxs-lookup"><span data-stu-id="2b454-119">If you experience this, you can safely ignore the error.</span></span>

    
    </div>

<span data-ttu-id="2b454-120">**将您的主 System Center Operations Manager 管理服务器配置为替代候选中央发现观察程序节点。**</span><span class="sxs-lookup"><span data-stu-id="2b454-120">**Configure your primary System Center Operations Manager management server to override the candidate central discovery watcher node.**</span></span>

1.  <span data-ttu-id="2b454-121">在已安装 System Center Operations Manager 控制台的计算机上，展开 " **管理包对象** "，然后选择 " **对象发现**"。</span><span class="sxs-lookup"><span data-stu-id="2b454-121">On a computer where the System Center Operations Manager console has been installed, expand **Management Pack Objects** and then select **Object Discoveries**.</span></span>

2.  <span data-ttu-id="2b454-122">单击 "**更改范围 ...** "</span><span class="sxs-lookup"><span data-stu-id="2b454-122">Click **Change Scope...**</span></span>

3.  <span data-ttu-id="2b454-123">从 " **作用域管理包对象** " 页面中，选择 " **搜索候选** 项"。</span><span class="sxs-lookup"><span data-stu-id="2b454-123">From the **Scope Management Pack Objects** page, select **LS Discovery Candidate**.</span></span>

4.  <span data-ttu-id="2b454-124">将 " **发现候选** 项" 的有效值替换为前面过程中所选择的候选服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="2b454-124">Override the **LS Discovery Candidate Effective Value** to the name of the candidate server elected in the earlier procedure.</span></span>

<span data-ttu-id="2b454-125">最后，若要完成更改，请重新启动 System Center Operations Manager 根管理服务器上的运行状况服务。</span><span class="sxs-lookup"><span data-stu-id="2b454-125">Lastly, to finalize your changes, restart the health service on the System Center Operations Manager Root Management Server.</span></span>

<span data-ttu-id="2b454-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b454-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

