---
title: Lync Server 2013：删除网络带宽策略配置文件
description: Lync Server 2013：删除网络带宽策略配置文件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network bandwidth policy profiles
ms:assetid: 4d6beda8-6aa5-4d5e-8a07-363598f0e0c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688050(v=OCS.15)
ms:contentKeyID: 49733643
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69f460d9620158d1857dae41e0033f6d36078868
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430299"
---
# <a name="deleting-network-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="70632-103">删除 Lync Server 2013 中的网络带宽策略配置文件</span><span class="sxs-lookup"><span data-stu-id="70632-103">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70632-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70632-104">

<span> </span></span></span>

<span data-ttu-id="70632-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="70632-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="70632-106">作为 "呼叫许可控制" (CAC) 的一部分，带宽策略用于定义某些形式的带宽限制。</span><span class="sxs-lookup"><span data-stu-id="70632-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="70632-107">在 Microsoft Lync Server 2013 中，只有音频和视频形式可以分配带宽限制。</span><span class="sxs-lookup"><span data-stu-id="70632-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="70632-108">你可以设置整体带宽限制和会话限制。</span><span class="sxs-lookup"><span data-stu-id="70632-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="70632-109">你可以使用 Lync Server 控制面板为这些策略创建、修改或删除容器配置文件。</span><span class="sxs-lookup"><span data-stu-id="70632-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="70632-110">使用以下过程删除网络带宽策略配置文件。</span><span class="sxs-lookup"><span data-stu-id="70632-110">Use the following procedures to delete a network bandwidth policy profiles.</span></span> <span data-ttu-id="70632-111">有关创建或修改网络带宽策略配置文件的详细信息，请参阅 [在 Lync Server 2013 中创建或修改带宽策略配置文件](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="70632-111">For details on creating or modifying a network bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-delete-a-bandwidth-policy-profile"></a><span data-ttu-id="70632-112">删除带宽策略配置文件</span><span class="sxs-lookup"><span data-stu-id="70632-112">To delete a bandwidth policy profile</span></span>

1.  <span data-ttu-id="70632-113">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="70632-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="70632-114">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="70632-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="70632-115">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="70632-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="70632-116">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **带宽策略**"。</span><span class="sxs-lookup"><span data-stu-id="70632-116">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="70632-117">在 " **带宽策略** " 页面上，单击要删除的带宽策略配置文件。</span><span class="sxs-lookup"><span data-stu-id="70632-117">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="70632-118">您可以一次删除多个配置文件。</span><span class="sxs-lookup"><span data-stu-id="70632-118">You can delete more than one profile at a time.</span></span> <span data-ttu-id="70632-119">若要执行此操作，请在按住 CTRL 键的同时按 CTRL 并选择多个配置文件。</span><span class="sxs-lookup"><span data-stu-id="70632-119">To do this, press CTRL and select multiple profiles while holding down the CTRL key.</span></span> <span data-ttu-id="70632-120">或者，若要选择所有配置文件，请单击 "<STRONG>编辑</STRONG>" 菜单上的 "<STRONG>全选</STRONG>"。</span><span class="sxs-lookup"><span data-stu-id="70632-120">Or, to select all profiles, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="70632-121">在 " **编辑** " 菜单上，单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="70632-121">On the **Edit** menu, click **Delete**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="70632-122">您不能删除与网络站点相关联的带宽策略配置文件。</span><span class="sxs-lookup"><span data-stu-id="70632-122">You cannot delete a bandwidth policy profile that is associated with a network site.</span></span> <span data-ttu-id="70632-123">您必须先删除与网络站点的关联，然后才能删除配置文件。</span><span class="sxs-lookup"><span data-stu-id="70632-123">You must first remove the association with the network site before you can delete the profile.</span></span> <span data-ttu-id="70632-124">有关如何修改网络站点的详细信息，请参阅 <A href="lync-server-2013-creating-or-modifying-network-sites.md">在 Lync Server 2013 中创建或修改网络站点</A>。</span><span class="sxs-lookup"><span data-stu-id="70632-124">For details about how to modify the network site, see <A href="lync-server-2013-creating-or-modifying-network-sites.md">Creating or modifying network sites in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="70632-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70632-125">See Also</span></span>


[<span data-ttu-id="70632-126">在 Lync Server 2013 中创建或修改带宽策略配置文件</span><span class="sxs-lookup"><span data-stu-id="70632-126">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="70632-127">在 Lync Server 2013 中查看网络带宽策略配置文件信息</span><span class="sxs-lookup"><span data-stu-id="70632-127">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-bandwidth-policy-profile-information.md)  


[<span data-ttu-id="70632-128">在 Lync Server 2013 中配置呼叫许可控制</span><span class="sxs-lookup"><span data-stu-id="70632-128">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="70632-129">Remove-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="70632-129">Remove-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="70632-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70632-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

