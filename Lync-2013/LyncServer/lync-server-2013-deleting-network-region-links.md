---
title: Lync Server 2013：删除网络区域链接
description: Lync Server 2013：删除网络区域链接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network region links
ms:assetid: 839273cd-d23f-4b38-84e6-d2dc972f49cd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688114(v=OCS.15)
ms:contentKeyID: 49733712
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a17c1ec64460e0f7cb447597f94aadd7fd2a9ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430285"
---
# <a name="deleting-network-region-links-in-lync-server-2013"></a><span data-ttu-id="645da-103">删除 Lync Server 2013 中的网络区域链接</span><span class="sxs-lookup"><span data-stu-id="645da-103">Deleting network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="645da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="645da-104">

<span> </span></span></span>

<span data-ttu-id="645da-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="645da-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="645da-106">你可以将两个网络区域之间的链接配置为 "呼叫许可控制" (CAC) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="645da-106">You can configure links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="645da-107">网络中的区域通过 (WAN) 连接的物理广域网络进行链接。</span><span class="sxs-lookup"><span data-stu-id="645da-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="645da-108">可以使用 Lync Server "控制面板" 删除两个网络区域之间的现有链接。</span><span class="sxs-lookup"><span data-stu-id="645da-108">You can use the Lync Server Control Panel to delete an existing link between two network regions.</span></span> <span data-ttu-id="645da-109">有关创建或修改网络区域链接的详细信息，请参阅 [在 Lync Server 2013 中配置网络区域链接](lync-server-2013-configuring-network-region-links.md)</span><span class="sxs-lookup"><span data-stu-id="645da-109">For details about creating or modifying network region link, see [Configuring network region links in Lync Server 2013](lync-server-2013-configuring-network-region-links.md)</span></span>

<div>

## <a name="to-delete-a-network-region-link"></a><span data-ttu-id="645da-110">删除网络区域链接</span><span class="sxs-lookup"><span data-stu-id="645da-110">To delete a network region link</span></span>

1.  <span data-ttu-id="645da-111">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="645da-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="645da-112">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="645da-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="645da-113">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="645da-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="645da-114">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **区域链接**"。</span><span class="sxs-lookup"><span data-stu-id="645da-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="645da-115">在 " **区域链接** " 页面上，单击要删除的区域链接。</span><span class="sxs-lookup"><span data-stu-id="645da-115">On the **Region Link** page, click the region link that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="645da-116">您可以一次删除多个区域链接。</span><span class="sxs-lookup"><span data-stu-id="645da-116">You can delete more than one region link at a time.</span></span> <span data-ttu-id="645da-117">若要执行此操作，请在按住 CTRL 键的同时按 CTRL 并选择多个区域链接。</span><span class="sxs-lookup"><span data-stu-id="645da-117">To do this, press CTRL and select multiple region links while holding down the CTRL key.</span></span> <span data-ttu-id="645da-118">或者，若要选择所有区域链接，请单击 "<STRONG>编辑</STRONG>" 菜单上的 "<STRONG>全选</STRONG>"。</span><span class="sxs-lookup"><span data-stu-id="645da-118">Or, to select all region links, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="645da-119">从 " **编辑** " 菜单中，选择 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="645da-119">From the **Edit** menu, select **Delete**.</span></span>

6.  <span data-ttu-id="645da-120">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="645da-120">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="645da-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="645da-121">See Also</span></span>


[<span data-ttu-id="645da-122">在 Lync Server 2013 中配置网络区域链接</span><span class="sxs-lookup"><span data-stu-id="645da-122">Configuring network region links in Lync Server 2013</span></span>](lync-server-2013-configuring-network-region-links.md)  
  

<span data-ttu-id="645da-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="645da-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

