---
title: 创建新的 URL 筛选器以处理即时消息对话中的超链接
description: 创建新的 URL 筛选器以处理即时消息对话中的超链接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new URL filter to handle hyperlinks in IM conversations
ms:assetid: d0ee01e5-f039-4a34-ac9d-659fe4e9e879
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182590(v=OCS.15)
ms:contentKeyID: 48185426
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e583b3e8cbd04279ab7f54b4138a349fa0d1e85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432119"
---
# <a name="create-a-new-url-filter-in-lync-server-2013-to-handle-hyperlinks-in-im-conversations"></a><span data-ttu-id="9a5af-103">在 Lync Server 2013 中创建新的 URL 筛选器以处理即时消息对话中的超链接</span><span class="sxs-lookup"><span data-stu-id="9a5af-103">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a5af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a5af-104">

<span> </span></span></span>

<span data-ttu-id="9a5af-105">_**主题上次修改时间：** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="9a5af-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="9a5af-106">除了修改全局 URL 筛选器之外，还可以为 Lync Server 2013 部署中的各个网站配置自定义 URL 筛选器。</span><span class="sxs-lookup"><span data-stu-id="9a5af-106">In addition to modifying the global URL filter, you can configure custom URL filters for individual sites within your Lync Server 2013 deployment.</span></span> <span data-ttu-id="9a5af-107">有关 URL 筛选的详细信息，请参阅 [在 Lync Server 2013 中配置即时消息 (IM) 的文件传输和 URL 筛选](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)。</span><span class="sxs-lookup"><span data-stu-id="9a5af-107">For details about URL filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-create-a-new-url-filter"></a><span data-ttu-id="9a5af-108">创建新的 URL 筛选器</span><span class="sxs-lookup"><span data-stu-id="9a5af-108">To create a new URL filter</span></span>

1.  <span data-ttu-id="9a5af-109">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="9a5af-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9a5af-110">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="9a5af-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9a5af-111">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="9a5af-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9a5af-112">在左侧导航栏中，单击 " **IM 和状态**"，然后单击 " **URL 筛选器**"。</span><span class="sxs-lookup"><span data-stu-id="9a5af-112">In the left navigation bar, click **IM and Presence**, and then click **URL Filter**.</span></span>

4.  <span data-ttu-id="9a5af-113">在 " **URL 筛选** " 页面上，单击 " **新建**"。</span><span class="sxs-lookup"><span data-stu-id="9a5af-113">On the **URL Filter** page, click **New**.</span></span>

5.  <span data-ttu-id="9a5af-114">在 " **选择网站**" 中，单击要为其创建 URL 筛选器的网站，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="9a5af-114">In **Select a Site**, click the site for which you want to create the URL filter, and then click **OK**.</span></span>

6.  <span data-ttu-id="9a5af-115">在 " **新建 URL 筛选器** " 对话框中，选中 " **启用 url 筛选** " 复选框以启用网站的 URL 筛选。</span><span class="sxs-lookup"><span data-stu-id="9a5af-115">In the **New URL Filter** dialog box, select the **Enable URL Filter** check box to enable URL filtering for the site.</span></span>

7.  <span data-ttu-id="9a5af-116">若要阻止包含扩展名在 " **文件类型扩展** " 下列出的文件的任何活动 URL 位于 " **编辑文件筛选器**" 中，请选中 " **使用文件扩展名阻止 url** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="9a5af-116">To block any active URL that contains a file with an extension listed under **File type extensions to block** in **Edit File Filter**, select the **Block URLs with file extension** check box.</span></span>

8.  <span data-ttu-id="9a5af-117">在 " **超链接前缀** " 下拉列表框中，单击与您希望在即时消息对话中处理 url 的方式相对应的选项。</span><span class="sxs-lookup"><span data-stu-id="9a5af-117">In the **Hyperlink prefix** drop-down list box, click the option that corresponds to how you want to handle URLs in instant message conversations.</span></span>
    
    <span data-ttu-id="9a5af-118">" **允许消息** " 框可在发送允许发送的超链接时向用户发送警告消息。</span><span class="sxs-lookup"><span data-stu-id="9a5af-118">The **Allow message** box enables a warning message to be sent to the user when sending hyperlinks that are allowed to be sent.</span></span>

9.  <span data-ttu-id="9a5af-119">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="9a5af-119">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9a5af-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9a5af-120">See Also</span></span>


[<span data-ttu-id="9a5af-121">在 Lync Server 2013 中为即时消息 (IM) 配置文件传输和 URL 筛选</span><span class="sxs-lookup"><span data-stu-id="9a5af-121">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="9a5af-122">在 Lync Server 2013 中为特定网站创建新的文件传输筛选器</span><span class="sxs-lookup"><span data-stu-id="9a5af-122">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="9a5af-123">在 Lync Server 2013 中修改默认文件传输筛选器</span><span class="sxs-lookup"><span data-stu-id="9a5af-123">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  


[<span data-ttu-id="9a5af-124">在 Lync Server 2013 中修改默认 URL 筛选器</span><span class="sxs-lookup"><span data-stu-id="9a5af-124">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="9a5af-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a5af-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

