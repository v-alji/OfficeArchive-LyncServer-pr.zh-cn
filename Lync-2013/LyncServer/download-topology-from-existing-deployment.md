---
title: 从现有部署下载拓扑
description: 从现有部署下载拓扑。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Download topology from existing deployment
ms:assetid: e39065a2-d4b0-4f27-8c49-f56be78fa55b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721913(v=OCS.15)
ms:contentKeyID: 49733847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c22d746f8faf3fdf14a44e751eeb3c88bf3eef4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392032"
---
# <a name="download-topology-from-existing-deployment"></a><span data-ttu-id="06afb-103">从现有部署下载拓扑</span><span class="sxs-lookup"><span data-stu-id="06afb-103">Download topology from existing deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06afb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06afb-104">

<span> </span></span></span>

<span data-ttu-id="06afb-105">_**主题上次修改时间：** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="06afb-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="06afb-106">创建 Lync Server 2013 池时，将使用与 Lync Server 2010 相关联的中央管理存储。</span><span class="sxs-lookup"><span data-stu-id="06afb-106">When creating a Lync Server 2013 pool, you will use the Central Management Store that is associated with Lync Server 2010.</span></span> <span data-ttu-id="06afb-107">在首次使用时启动拓扑生成器和后续编辑会话时，系统会提示你输入希望拓扑生成器加载当前配置文档的位置。</span><span class="sxs-lookup"><span data-stu-id="06afb-107">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="06afb-108">因为你已定义了 Lync Server 2010 拓扑，并且已建立中央管理存储，因此你应该选择从现有部署下载拓扑。</span><span class="sxs-lookup"><span data-stu-id="06afb-108">Because you already have a Lync Server 2010 topology defined and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="06afb-109">拓扑生成器将读取数据库并检索当前定义。</span><span class="sxs-lookup"><span data-stu-id="06afb-109">Topology Builder will read the database and retrieve the current definition.</span></span>

<span data-ttu-id="06afb-110">**从现有部署下载拓扑**</span><span class="sxs-lookup"><span data-stu-id="06afb-110">**To download a topology from an existing deployment**</span></span>

1.  <span data-ttu-id="06afb-111">打开 **Lync Server 部署向导**。</span><span class="sxs-lookup"><span data-stu-id="06afb-111">Open the **Lync Server Deployment Wizard**.</span></span>

2.  <span data-ttu-id="06afb-112">在 " **Lync Server 2013-部署向导** " 页面上，单击 " **安装管理工具**"。</span><span class="sxs-lookup"><span data-stu-id="06afb-112">From the **Lync Server 2013 – Deployment Wizard** page, click **Install Administrative Tools**.</span></span>

3.  <span data-ttu-id="06afb-113">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013** "，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="06afb-113">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013** , and then click **Lync Server Topology Builder**.</span></span>

4.  <span data-ttu-id="06afb-114">**从现有部署中选择 "下载拓扑**"。</span><span class="sxs-lookup"><span data-stu-id="06afb-114">Select **Download Topology from existing deployment**.</span></span>
    
    <span data-ttu-id="06afb-115">![部署向导拓扑生成器设置](images/JJ721913.d5b39fd9-3c13-422e-a06c-25d2568fe781(OCS.15).jpg "部署向导拓扑生成器设置")</span><span class="sxs-lookup"><span data-stu-id="06afb-115">![Deployment Wizard Topology Builder settings](images/JJ721913.d5b39fd9-3c13-422e-a06c-25d2568fe781(OCS.15).jpg "Deployment Wizard Topology Builder settings")</span></span>

5.  <span data-ttu-id="06afb-116">选择文件名，并使用默认的 tbxml 文件类型保存拓扑。</span><span class="sxs-lookup"><span data-stu-id="06afb-116">Choose a file name and save the topology with the default .tbxml file type.</span></span>

6.  <span data-ttu-id="06afb-117">如图所示展开 Lync 服务器节点，以显示部署中的各种服务器角色。</span><span class="sxs-lookup"><span data-stu-id="06afb-117">Expand the Lync Server node, as shown, to reveal the various server roles in the deployment.</span></span>
    
    <span data-ttu-id="06afb-118">![拓扑生成器服务器角色常规属性](images/JJ721913.af99ead3-676b-47fd-8369-5a5f9717383f(OCS.15).jpg "拓扑生成器服务器角色常规属性")</span><span class="sxs-lookup"><span data-stu-id="06afb-118">![Topology Builder server role general properties](images/JJ721913.af99ead3-676b-47fd-8369-5a5f9717383f(OCS.15).jpg "Topology Builder server role general properties")</span></span>

<span data-ttu-id="06afb-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06afb-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

