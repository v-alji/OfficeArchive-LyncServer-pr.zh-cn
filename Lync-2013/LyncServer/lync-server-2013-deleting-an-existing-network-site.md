---
title: Lync Server 2013：删除现有网络网站
description: Lync Server 2013：删除现有网络网站。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an existing network site
ms:assetid: 2762149b-3572-4513-b838-beda7fa9e81e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688001(v=OCS.15)
ms:contentKeyID: 49733589
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7cef4774ee71aaf6851757d5b88d30138fc34997
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430355"
---
# <a name="deleting-an-existing-network-site-in-lync-server-2013"></a><span data-ttu-id="79a13-103">在 Lync Server 2013 中删除现有网络网站</span><span class="sxs-lookup"><span data-stu-id="79a13-103">Deleting an existing network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79a13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79a13-104">

<span> </span></span></span>

<span data-ttu-id="79a13-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="79a13-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="79a13-106">网络站点是在呼叫许可控制的每个区域内配置的办公室或位置 (CAC) 或增强的9-1-1 部署。</span><span class="sxs-lookup"><span data-stu-id="79a13-106">Network sites are the offices or locations configured within each region of a call admission control (CAC) or Enhanced 9-1-1 deployment.</span></span> <span data-ttu-id="79a13-107">你可以使用 Lync Server 2013 控制面板配置网站并将其与区域相关联。</span><span class="sxs-lookup"><span data-stu-id="79a13-107">You can use the Lync Server 2013 Control Panel to configure sites and associate them with regions.</span></span> <span data-ttu-id="79a13-108">例如，北美洲的网络区域可能与诸如芝加哥、雷德蒙和范区的网络站点相关联。</span><span class="sxs-lookup"><span data-stu-id="79a13-108">For example, a network region for North America might be associated with networks sites such as Chicago, Redmond, and Vancouver.</span></span> <span data-ttu-id="79a13-109">必须为组织内的每个网站创建 CAC 网络网站，即使该网站没有带宽限制也是如此。</span><span class="sxs-lookup"><span data-stu-id="79a13-109">A CAC network site must be created for every site within an organization, even if that site has no bandwidth limitations.</span></span> <span data-ttu-id="79a13-110">在 Lync Server 控制面板中，您可以创建、修改和删除网络站点。</span><span class="sxs-lookup"><span data-stu-id="79a13-110">From the Lync Server Control Panel you can create, modify, and delete network sites.</span></span> <span data-ttu-id="79a13-111">使用以下过程删除现有网络网站。</span><span class="sxs-lookup"><span data-stu-id="79a13-111">Use the following procedure to delete an existing network site.</span></span> <span data-ttu-id="79a13-112">有关创建或修改网络站点的详细信息，请参阅 [在 Lync Server 2013 中创建或修改网络站点](lync-server-2013-creating-or-modifying-network-sites.md)</span><span class="sxs-lookup"><span data-stu-id="79a13-112">For details about creating or modifying network sites, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md)</span></span>

<div>

## <a name="to-delete-a-network-site"></a><span data-ttu-id="79a13-113">删除网络网站</span><span class="sxs-lookup"><span data-stu-id="79a13-113">To delete a network site</span></span>

1.  <span data-ttu-id="79a13-114">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="79a13-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="79a13-115">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="79a13-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="79a13-116">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="79a13-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="79a13-117">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **网站**"。</span><span class="sxs-lookup"><span data-stu-id="79a13-117">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="79a13-118">在 " **网站** " 页面上，单击要删除的网站。</span><span class="sxs-lookup"><span data-stu-id="79a13-118">On the **Site** page, click the site that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79a13-119">您可以一次删除多个网站。</span><span class="sxs-lookup"><span data-stu-id="79a13-119">You can delete more than one site at a time.</span></span> <span data-ttu-id="79a13-120">若要执行此操作，请在按住 CTRL 键的同时按 CTRL 并选择多个网站。</span><span class="sxs-lookup"><span data-stu-id="79a13-120">To do this, press CTRL and select multiple sites while holding down the CTRL key.</span></span> <span data-ttu-id="79a13-121">或者，若要选择 "所有网站"，请单击 "<STRONG>编辑</STRONG>" 菜单上的 "<STRONG>全选</STRONG>"。</span><span class="sxs-lookup"><span data-stu-id="79a13-121">Or, to select all sites, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="79a13-122">在 " **编辑** " 菜单上，单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="79a13-122">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="79a13-123">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="79a13-123">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="79a13-124">如果网络站点与网络子网相关联，则不能将其删除。</span><span class="sxs-lookup"><span data-stu-id="79a13-124">You cannot remove a network site if it is associated with a network subnet.</span></span> <span data-ttu-id="79a13-125">如果您尝试删除与子网相关联的网站，您将收到一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="79a13-125">If you attempt to remove a site associated with a subnet you will receive an error message.</span></span> <span data-ttu-id="79a13-126">若要查看某个网站是否与任何子网相关联，请单击该网站，然后单击 "<STRONG>编辑</STRONG>" 菜单上的 "<STRONG>显示详细信息</STRONG>"。</span><span class="sxs-lookup"><span data-stu-id="79a13-126">To see if a site is associated with any subnets, click the site and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    <span data-ttu-id="79a13-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79a13-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

