---
title: 授权到 Office 通信服务器 2007 R2 Edge 服务器的连接
description: 授权到 Office 通信服务器 2007 R2 Edge 服务器的连接。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Authorize connection to Office Communications Server 2007 R2 Edge Server
ms:assetid: 14f6798a-28d6-4b3d-8734-942192e1bbf5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204702(v=OCS.15)
ms:contentKeyID: 48183493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de8dadb2c476c892f4ffd548ce176d12d3b1a1cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391968"
---
# <a name="authorize-connection-to-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="64617-103">授权到 Office 通信服务器 2007 R2 Edge 服务器的连接</span><span class="sxs-lookup"><span data-stu-id="64617-103">Authorize connection to Office Communications Server 2007 R2 Edge Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64617-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64617-104">

<span> </span></span></span>

<span data-ttu-id="64617-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="64617-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="64617-106">对于你的试点池中的每个 Lync Server 2013 前端服务器或标准版服务器，你必须更新授权连接到 Office 通信服务器 2007 R2 Edge 服务器的内部服务器的列表。</span><span class="sxs-lookup"><span data-stu-id="64617-106">For each Lync Server 2013 Front End Server or Standard Edition server in your pilot pool, you must update the list of internal servers that are authorized to connect to the Office Communications Server 2007 R2 Edge Server.</span></span> <span data-ttu-id="64617-107">如果没有这些更新，外部音频/视频 (A/V) 通过使用旧版 Edge 服务器加入的用户的会议将不起作用。</span><span class="sxs-lookup"><span data-stu-id="64617-107">Without these updates, external audio/visual (A/V) conferencing for users joining by using the legacy Edge Server will not work.</span></span>

<div>

## <a name="to-authorize-connection-to-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="64617-108">授权到 Office 通信服务器 2007 R2 Edge 服务器的连接</span><span class="sxs-lookup"><span data-stu-id="64617-108">To Authorize Connection to Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="64617-109">从 Office 通信服务器 2007 R2 Edge 服务器的 " **管理工具** " 组中，打开 " **计算机管理** " 管理单元。</span><span class="sxs-lookup"><span data-stu-id="64617-109">From the Office Communications Server 2007 R2 Edge Server, from the **Administrative Tools** group, open the **Computer Management** snap-in.</span></span>

2.  <span data-ttu-id="64617-110">在控制台树中，展开 " **服务和应用程序**"。</span><span class="sxs-lookup"><span data-stu-id="64617-110">In the console tree, expand **Services and Applications**.</span></span>

3.  <span data-ttu-id="64617-111">右键单击 " **Office 通信服务器 2007 R2**"，然后单击 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="64617-111">Right-click **Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="64617-112">单击 " **内部** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="64617-112">Click the **Internal** tab.</span></span>

5.  <span data-ttu-id="64617-113">在 " **添加服务器**" 下，单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="64617-113">Under **Add Server**, click **Add**.</span></span>

6.  <span data-ttu-id="64617-114">在 " **添加 Office 通信服务器** " 对话框中，输入相应的信息：</span><span class="sxs-lookup"><span data-stu-id="64617-114">In the **Add Office Communications Server** dialog box, enter the appropriate information:</span></span>
    
      - <span data-ttu-id="64617-115">指定每个 Lync Server 2013 的完全限定的域名 (FQDN) 每个 Lync Server 前端服务器或标准版服务器以及 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="64617-115">Specify the fully qualified domain name (FQDN) of each Lync Server 2013 Front End Server or Standard Edition server, and Lync Server 2013 pool.</span></span>
    
      - <span data-ttu-id="64617-116">如果在通过其 FQDN 指定下一跃点计算机的池中配置了静态路由，请指定 Lync Server 2013 控制器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="64617-116">Specify the FQDN of the Lync Server 2013 Director if you configured a static route on the pool that specifies the next hop computer by its FQDN.</span></span>

7.  <span data-ttu-id="64617-117">为每个 Lync Server 2013、前端服务器、标准版服务器、池和控制器添加条目后，单击 " **应用** "，然后单击 **"确定"** 以关闭 "属性" 页面。</span><span class="sxs-lookup"><span data-stu-id="64617-117">After you have added an entry for each Lync Server 2013, Front End Server, Standard Edition server, pool, and Director, click **Apply** and then click **OK** to close the Properties page.</span></span>

<span data-ttu-id="64617-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64617-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

