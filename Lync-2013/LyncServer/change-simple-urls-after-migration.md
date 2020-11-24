---
title: 迁移后更改简单 URL
description: 迁移后更改简单的 Url。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change simple URLs after migration
ms:assetid: addb0dc8-8324-42b1-9a00-f4bd14fdf5c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721844(v=OCS.15)
ms:contentKeyID: 49733777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f9974106d28bcfdc64c2255337baf721a937e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391962"
---
# <a name="change-simple-urls-after-migration"></a><span data-ttu-id="6c4fc-103">迁移后更改简单 URL</span><span class="sxs-lookup"><span data-stu-id="6c4fc-103">Change simple URLs after migration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c4fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c4fc-104">

<span> </span></span></span>

<span data-ttu-id="6c4fc-105">_**主题上次修改时间：** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="6c4fc-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="6c4fc-106">Lync 服务器支持三个简单的 Url：</span><span class="sxs-lookup"><span data-stu-id="6c4fc-106">Lync Server supports three simple URLs:</span></span>

  - <span data-ttu-id="6c4fc-107">"**开会**" 用作网站或组织中的所有会议的基本 URL。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-107">**Meet** is used as the base URL for all conferences in the site or organization.</span></span> <span data-ttu-id="6c4fc-108">通过 "满足简单 URL"，加入会议的链接易于理解，并且易于沟通和分发。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-108">With the Meet simple URL, links to join meetings are easy to comprehend, and easy to communicate and distribute.</span></span>

  - <span data-ttu-id="6c4fc-109">通过 **拨入功能**，可以访问 "电话拨入式会议设置" 网页。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-109">**Dial-in** enables access to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="6c4fc-110">拨入式简单 URL 包含在所有会议邀请中，以便希望拨入会议的用户可以访问必要的电话号码和 PIN 信息。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-110">The Dial-in simple URL is included in all meeting invitations so that users who want to dial in to the meeting can access the necessary phone number and PIN information.</span></span>

  - <span data-ttu-id="6c4fc-111">**管理员** 可快速访问 Lync Server 控制面板。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-111">**Admin** enables quick access to the Lync Server Control Panel.</span></span> <span data-ttu-id="6c4fc-112">管理员简单的 URL 是您的组织内部的。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-112">The Admin simple URL is internal to your organization.</span></span>

<span data-ttu-id="6c4fc-113">迁移到 Lync Server 2013 后，必须知道更改对简单 Url 的 DNS 记录和证书有何影响。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-113">After migrating to Lync Server 2013, you must be aware of how the change impacts your DNS records and certificates for simple URLs.</span></span> <span data-ttu-id="6c4fc-114">如果旧版 Lync Server 2010 控制器在拓扑中保持使用，则不需要对您的简单 Url 进行任何更改。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-114">If the legacy Lync Server 2010 Director remains in use in the topology, no changes to your simple URLs are required.</span></span> <span data-ttu-id="6c4fc-115">如果在迁移后从拓扑中删除了 Lync Server 2010 控制器，则必须更新简单 URL DNS 记录以指向其中一个 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-115">If the Lync Server 2010 Director is removed from the topology after migration, the simple URL DNS records must be updated to point to one of the Lync Server 2013 pools.</span></span> <span data-ttu-id="6c4fc-116">但是，只要更改简单的 URL 名称，就必须在每个 Director 和前端服务器上运行 Enable-CsComputer 以注册更改。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-116">Whenever you change a simple URL name, however, you must run Enable-CsComputer on each Director and Front End Server to register the change.</span></span>

<div>

## <a name="changing-simple-urls-after-migration"></a><span data-ttu-id="6c4fc-117">迁移后更改简单的 Url</span><span class="sxs-lookup"><span data-stu-id="6c4fc-117">Changing Simple URLs after Migration</span></span>

<span data-ttu-id="6c4fc-118">**更新 "满足简单 URL"**</span><span class="sxs-lookup"><span data-stu-id="6c4fc-118">**To update the Meet simple URL**</span></span>

1.  <span data-ttu-id="6c4fc-119">在拓扑生成器中，右键单击顶部节点 **Lync 服务器**，然后单击 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-119">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="6c4fc-120">在左窗格中选择 " **简单 url** "，然后单击 " **会议 url"：** 选择 "满足 url"，然后单击 " **编辑 URL**"。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-120">Select **Simple URLs** in the left pane, then below **Meeting URLs:** select the Meet URL and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="6c4fc-121">将 URL 更新为所需的值，然后单击“**确定**”保存已编辑的 URL。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-121">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span>

<span data-ttu-id="6c4fc-122">**更新管理员简单 URL**</span><span class="sxs-lookup"><span data-stu-id="6c4fc-122">**To update the Admin simple URL**</span></span>

1.  <span data-ttu-id="6c4fc-123">在拓扑生成器中，右键单击顶部节点 **Lync 服务器**，然后单击 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-123">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="6c4fc-124">在左窗格中选择 " **简单 url** "，然后在 " **管理访问 URL** " 框下方输入要用于管理对 Lync Server 2013 控制面板的简单 URL，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-124">Select **Simple URLs** in the left pane, then below **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="6c4fc-125">建议尽可能使用最简单的 URL 作为管理 URL。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-125">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="6c4fc-126">最简单的选项是<STRONG> https://admin 。</STRONG> &lt;域 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="6c4fc-126">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6c4fc-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c4fc-127">See Also</span></span>


[<span data-ttu-id="6c4fc-128">在 Lync Server 2013 中规划简单 URL</span><span class="sxs-lookup"><span data-stu-id="6c4fc-128">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="6c4fc-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c4fc-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

