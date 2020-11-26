---
title: Lync Server 2013：为特定网站创建新的文件传输筛选器
description: Lync Server 2013：为特定网站创建新的文件传输筛选器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new file transfer filter for a specific site
ms:assetid: d0006487-5217-491c-b730-e6c551cd9825
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182589(v=OCS.15)
ms:contentKeyID: 48185577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d3b5003711c2f2e74b726809fba5da6d9fd0aa57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432168"
---
# <a name="create-a-new-file-transfer-filter-in-lync-server-2013-for-a-specific-site"></a><span data-ttu-id="e1311-103">在 Lync Server 2013 中为特定网站创建新的文件传输筛选器</span><span class="sxs-lookup"><span data-stu-id="e1311-103">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1311-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1311-104">

<span> </span></span></span>

<span data-ttu-id="e1311-105">_**主题上次修改时间：** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="e1311-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="e1311-106">除了修改全局文件传输筛选器，还可以为 Lync Server 2013 部署中的特定网站配置自定义文件传输筛选器。</span><span class="sxs-lookup"><span data-stu-id="e1311-106">In addition to modifying the global file transfer filter, you can configure custom file transfer filters for specific sites within your Lync Server 2013 deployment.</span></span> <span data-ttu-id="e1311-107">有关文件传输筛选的详细信息，请参阅 [在 Lync Server 2013 中为即时消息 (IM) 配置文件传输和 URL 筛选](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)。</span><span class="sxs-lookup"><span data-stu-id="e1311-107">For details about file transfer filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-create-a-file-transfer-filter-for-a-specific-site"></a><span data-ttu-id="e1311-108">为特定网站创建文件传输筛选器</span><span class="sxs-lookup"><span data-stu-id="e1311-108">To create a file transfer filter for a specific site</span></span>

1.  <span data-ttu-id="e1311-109">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="e1311-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e1311-110">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="e1311-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e1311-111">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="e1311-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e1311-112">在左侧导航栏中，单击 " **IM 和状态** "，然后单击 " **文件筛选器**"。</span><span class="sxs-lookup"><span data-stu-id="e1311-112">In the left navigation bar, click **IM and Presence** and then click **File Filter**.</span></span>

4.  <span data-ttu-id="e1311-113">在 " **文件筛选器** " 页面上，单击 " **新建**"。</span><span class="sxs-lookup"><span data-stu-id="e1311-113">On the **File Filter** page, click **New**.</span></span>

5.  <span data-ttu-id="e1311-114">在 " **选择网站** " 对话框中，单击要为其创建文件传输筛选器的网站，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="e1311-114">In the **Select a Site** dialog box, click the site for which you want to create the file transfer filter, and then click **OK**.</span></span>

6.  <span data-ttu-id="e1311-115">在 " **新建文件筛选器**" 中，单击 " **启用文件筛选器** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="e1311-115">In **New File Filter**, click the **Enable file filter** check box.</span></span>

7.  <span data-ttu-id="e1311-116">在 " **文件传输** " 下拉列表框中，单击 " **阻止全部** " 或 " **阻止特定文件类型**"。</span><span class="sxs-lookup"><span data-stu-id="e1311-116">In **File transfer** drop-down list box, click **Block All** or **Block specific file types**.</span></span>

8.  <span data-ttu-id="e1311-117">如果单击 " **全部阻止**"，请跳到步骤10。</span><span class="sxs-lookup"><span data-stu-id="e1311-117">If you clicked **Block All**, skip to step 10.</span></span>

9.  <span data-ttu-id="e1311-118">如果单击了 " **阻止特定文件类型**"，请执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="e1311-118">If you clicked **Block specific file types**, do the following:</span></span>
    
    1.  <span data-ttu-id="e1311-119">单击 " **选择** " 以修改要阻止的文件类型扩展名的默认列表。</span><span class="sxs-lookup"><span data-stu-id="e1311-119">Click **Select** to modify the default list of file type extensions that you want to block.</span></span>
    
    2.  <span data-ttu-id="e1311-120">在 " **选择文件类型** " 对话框中，从 " **文件类型扩展**" 下的类别中添加或删除扩展名，选择要阻止或允许的文件类型。</span><span class="sxs-lookup"><span data-stu-id="e1311-120">In the **Select File Type** dialog box, select the file types that you want to block or allow by adding or removing their extensions from the categories under **File type extensions**.</span></span>
    
    3.  <span data-ttu-id="e1311-121">如果看不到要阻止的文件类型的扩展名，请在文本框中的 " **向列表添加文件类型扩展名**" 下键入扩展名，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="e1311-121">If you do not see the extension for a file type that you want to block, type the extension in the text box under **Add file type extensions to the list**, and then click **Add**.</span></span>
    
    4.  <span data-ttu-id="e1311-122">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="e1311-122">Click **OK**.</span></span>

10. <span data-ttu-id="e1311-123">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="e1311-123">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e1311-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e1311-124">See Also</span></span>


[<span data-ttu-id="e1311-125">在 Lync Server 2013 中为即时消息 (IM) 配置文件传输和 URL 筛选</span><span class="sxs-lookup"><span data-stu-id="e1311-125">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="e1311-126">在 Lync Server 2013 中创建新的 URL 筛选器以处理即时消息对话中的超链接</span><span class="sxs-lookup"><span data-stu-id="e1311-126">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  
[<span data-ttu-id="e1311-127">在 Lync Server 2013 中修改默认文件传输筛选器</span><span class="sxs-lookup"><span data-stu-id="e1311-127">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  


[<span data-ttu-id="e1311-128">在 Lync Server 2013 中修改默认 URL 筛选器</span><span class="sxs-lookup"><span data-stu-id="e1311-128">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="e1311-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1311-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

