---
title: Lync Server 2013：查看组织中设备的软件更新
description: Lync Server 2013：查看组织中的设备的软件更新。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View software updates for devices in your organization
ms:assetid: d2cca12b-ed43-4e1f-90ab-d14bca8b482c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182592(v=OCS.15)
ms:contentKeyID: 48185418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 833ab25315847b760271c63bbfca3ba8357e41c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392172"
---
# <a name="view-software-updates-for-devices-in-lync-server-2013"></a><span data-ttu-id="18add-103">在 Lync Server 2013 中查看设备的软件更新</span><span class="sxs-lookup"><span data-stu-id="18add-103">View software updates for devices in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18add-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18add-104">

<span> </span></span></span>

<span data-ttu-id="18add-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="18add-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="18add-106">使用 Lync Server 2013，您可以使用 "设备更新" Web 服务查看和管理您的组织的设备的软件更新。</span><span class="sxs-lookup"><span data-stu-id="18add-106">With Lync Server 2013, you use Device Update Web service to view and manage software updates for your organization’s devices.</span></span> <span data-ttu-id="18add-107">从 Microsoft 支持网站的 .cab (cabinet) 文件中提供了这些更新 [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) 。</span><span class="sxs-lookup"><span data-stu-id="18add-107">These updates are available in .cab (cabinet) files from the Microsoft Support website at [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091).</span></span> <span data-ttu-id="18add-108">下载 .cab 文件后，运行 **CSDeviceUpdate** cmdlet 以从 .cab 文件中导入设备更新规则。</span><span class="sxs-lookup"><span data-stu-id="18add-108">After you download the .cab file, run the **Import-CSDeviceUpdate** cmdlet to import the device update rules from the .cab file.</span></span> <span data-ttu-id="18add-109">有关 **CSDeviceUpdate** cmdlet 的详细信息，请参阅 Lync Server Management Shell 文档中的 [Import-CSDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) 。</span><span class="sxs-lookup"><span data-stu-id="18add-109">For details about the **Import-CSDeviceUpdate** cmdlet, see [Import-CsDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) in the Lync Server Management Shell documentation.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="18add-110">在为你的组织部署新的更新之前，请验证它在测试设备上是否正常工作。</span><span class="sxs-lookup"><span data-stu-id="18add-110">Before deploying a new update to your organization, verify that it functions correctly on a test device.</span></span>



</div>

<div>

## <a name="to-view-software-updates-for-uc-devices"></a><span data-ttu-id="18add-111">查看 UC 设备的软件更新</span><span class="sxs-lookup"><span data-stu-id="18add-111">To view software updates for UC devices</span></span>

1.  <span data-ttu-id="18add-112">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="18add-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="18add-113">从 Microsoft 支持网站中 [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) ，将 .cab 文件下载到 Lync Server 2013 计算机上的某个位置 (例如，C： \\UCUpdates.cab) 的更新 \\ 。</span><span class="sxs-lookup"><span data-stu-id="18add-113">From the Microsoft Support website at [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091), download the .cab file to a location on a Lync Server 2013 computer (for example, C:\\Updates\\UCUpdates.cab).</span></span>

3.  <span data-ttu-id="18add-114">\\通过运行以下 cmdlet 之一从 C： UpdatesUCUpdates.cab 文件中导入设备更新规则 \\ ：</span><span class="sxs-lookup"><span data-stu-id="18add-114">Import the device update rules from the C:\\Updates\\UCUpdates.cab file by running one of the following cmdlets:</span></span>
    
      - <span data-ttu-id="18add-115">如果 .cab 文件位于运行要更新的服务的同一台计算机上 (服务： Redmond-websvc) ，请运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="18add-115">If the .cab file is located on the same computer as the one running the service to be updated (service:Redmond-websvc-2), run the following cmdlet:</span></span>
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-2 -FileName C:\Updates\UCUpdates.cab
    
      - <span data-ttu-id="18add-116">如果 .cab 文件所在的计算机不同于运行要更新的服务的计算机 (服务： Redmond-websvc) ，请运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="18add-116">If the .cab file is located on a different computer than the one running the service to be updated (service:Redmond-websvc-3), run the following cmdlet:</span></span>
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-3 -ByteInput C:\Updates\UCUpdates.cab

4.  <span data-ttu-id="18add-117">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="18add-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="18add-118">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="18add-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

5.  <span data-ttu-id="18add-119">在左侧导航栏中，单击 " **客户端**"，然后单击 " **设备更新**"。</span><span class="sxs-lookup"><span data-stu-id="18add-119">In the left navigation bar, click **Clients**, and then click **Device Update**.</span></span>

6.  <span data-ttu-id="18add-120">在 " **设备更新** " 页面上，单击列表中的更新，然后执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="18add-120">On the **Device Update** page, click an update in the list, and then do one of the following:</span></span>
    
      - <span data-ttu-id="18add-121">**取消待处理的更新。**</span><span class="sxs-lookup"><span data-stu-id="18add-121">**Cancel a pending update.**</span></span> <span data-ttu-id="18add-122">若要阻止所选更新部署到你的组织的设备，请单击 " **操作** " 菜单，然后单击 " **取消挂起的更新**"。</span><span class="sxs-lookup"><span data-stu-id="18add-122">To prevent the selected update from being deployed to your organization’s devices, click the **Action** menu, and then click **Cancel pending updates**.</span></span>
    
      - <span data-ttu-id="18add-123">**批准更新。**</span><span class="sxs-lookup"><span data-stu-id="18add-123">**Approve an update.**</span></span> <span data-ttu-id="18add-124">若要允许将所选更新部署到你的组织的设备，请单击 " **操作** " 菜单，然后单击 " **批准**"。</span><span class="sxs-lookup"><span data-stu-id="18add-124">To allow the selected update to be deployed to your organization’s devices, click the **Action** menu, and then click **Approve**.</span></span>
    
      - <span data-ttu-id="18add-125">**还原更新。**</span><span class="sxs-lookup"><span data-stu-id="18add-125">**Restore an update.**</span></span> <span data-ttu-id="18add-126">若要允许将以前批准的更新部署到你的组织的设备，请单击 " **操作** " 菜单，然后单击 " **还原**"。</span><span class="sxs-lookup"><span data-stu-id="18add-126">To allow a previously approved update to be deployed to your organization’s devices, click the **Action** menu, and then click **Restore**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="18add-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18add-127">See Also</span></span>


[<span data-ttu-id="18add-128">在 Lync Server 2013 中管理设备、电话和客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="18add-128">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="18add-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18add-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

