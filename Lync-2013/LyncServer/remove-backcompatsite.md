---
title: 删除 BackCompatSite
description: 删除 BackCompatSite。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440299"
---
# <a name="remove-backcompatsite"></a><span data-ttu-id="5c578-103">删除 BackCompatSite</span><span class="sxs-lookup"><span data-stu-id="5c578-103">Remove BackCompatSite</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c578-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c578-104">

<span> </span></span></span>

<span data-ttu-id="5c578-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="5c578-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="5c578-106">在停用所有池并卸载所有边缘服务器之后，请运行拓扑生成器合并向导删除 **BackCompatSite**。</span><span class="sxs-lookup"><span data-stu-id="5c578-106">After all pools are deactivated and all Edge Servers have been uninstalled, run the Topology Builder Merge wizard to remove the **BackCompatSite**.</span></span>

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a><span data-ttu-id="5c578-107">从拓扑生成器删除 BackCompat 网站</span><span class="sxs-lookup"><span data-stu-id="5c578-107">To remove BackCompat site from Topology Builder</span></span>

1.  <span data-ttu-id="5c578-108">从拓扑生成器打开现有部署。</span><span class="sxs-lookup"><span data-stu-id="5c578-108">Open an existing deployment from Topology Builder.</span></span>

2.  <span data-ttu-id="5c578-109">在 " **操作** " 菜单中，单击 " **合并 2007 R2 拓扑**"。</span><span class="sxs-lookup"><span data-stu-id="5c578-109">In the **Action** menu, click **Merge 2007 R2 Topology**.</span></span>

3.  <span data-ttu-id="5c578-110">单击“**下一步**”继续。</span><span class="sxs-lookup"><span data-stu-id="5c578-110">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="5c578-111">在 " **指定旧版 Edge** " 页面上，确保 Edge 服务器列表为空。</span><span class="sxs-lookup"><span data-stu-id="5c578-111">On the **Specify Legacy Edge** page, ensure that list of Edge Servers is empty.</span></span> <span data-ttu-id="5c578-112">如果列表不为空，请使用 " **删除** " 按钮删除所有旧式边缘服务器，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="5c578-112">If the list is not empty, use the **Remove** button to remove all the legacy Edge Servers, and then click **Next**.</span></span>
    
    <span data-ttu-id="5c578-113">![合并拓扑向导，"指定边缘设置" 页面](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "合并拓扑向导，"指定边缘设置" 页面")</span><span class="sxs-lookup"><span data-stu-id="5c578-113">![Merge Topology Wizard, Specify Edge Setup page](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="5c578-114">在 " **指定内部 SIP 端口设置** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="5c578-114">On the **Specify Internal SIP port setting** page, click **Next**.</span></span>

6.  <span data-ttu-id="5c578-115">在 " **摘要** " 页面上，单击 " **下一步** " 以开始合并拓扑以删除旧网站。</span><span class="sxs-lookup"><span data-stu-id="5c578-115">On the **Summary** page, click **Next** to begin merging the topologies to remove the legacy site.</span></span>

7.  <span data-ttu-id="5c578-116">在 " **状态** " 列中，验证值是否 **成功** ，然后单击 " **完成** " 关闭向导。</span><span class="sxs-lookup"><span data-stu-id="5c578-116">In the **Status** column, verify that the value is **Success** and then click **Finish** to close the wizard.</span></span>

8.  <span data-ttu-id="5c578-117">在拓扑生成器的左窗格中，展开 "BackCompatSite" 并确保未列出任何服务器。</span><span class="sxs-lookup"><span data-stu-id="5c578-117">In the left pane of Topology Builder, expand the BackCompatSite and ensure no servers are listed.</span></span>

9.  <span data-ttu-id="5c578-118">右键单击 " **BackCompatSite**"，然后单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="5c578-118">Right-click the **BackCompatSite**, and then click **Delete**.</span></span>

10. <span data-ttu-id="5c578-119">在 **拓扑生成器** 中，选择最前面的节点 **Lync 服务器**。</span><span class="sxs-lookup"><span data-stu-id="5c578-119">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

11. <span data-ttu-id="5c578-120">从 " **操作** " 菜单中，选择 " **发布拓扑** "，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="5c578-120">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

12. <span data-ttu-id="5c578-121">**发布向导** 完成后，单击 "**完成**" 关闭向导。</span><span class="sxs-lookup"><span data-stu-id="5c578-121">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<span data-ttu-id="5c578-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c578-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

