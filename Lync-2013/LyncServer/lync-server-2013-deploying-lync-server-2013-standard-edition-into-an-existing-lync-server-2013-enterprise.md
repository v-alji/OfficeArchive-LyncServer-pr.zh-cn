---
title: Lync Server 2013：将 Lync Server 2013 Standard Edition 部署到现有 Lync Server 2013 Enterprise 中
description: Lync Server 2013：将 Lync Server 2013 标准版部署到现有 Lync Server 2013 企业版。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Server 2013 Standard Edition into an existing Lync Server 2013 Enterprise
ms:assetid: 05ea128d-6c94-49b3-b28b-477367196425
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398112(v=OCS.15)
ms:contentKeyID: 48183297
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b233d4e782e716904fca0a2a146b2459e906aa57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429949"
---
# <a name="deploying-lync-server-2013-standard-edition-into-an-existing-lync-server-2013-enterprise"></a><span data-ttu-id="37087-103">将 Lync Server 2013 Standard Edition 部署到现有 Lync Server 2013 Enterprise 中</span><span class="sxs-lookup"><span data-stu-id="37087-103">Deploying Lync Server 2013 Standard Edition into an existing Lync Server 2013 Enterprise</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37087-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37087-104">

<span> </span></span></span>

<span data-ttu-id="37087-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="37087-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="37087-106">将标准版服务器部署到现有企业版部署类似于部署其他服务器角色。</span><span class="sxs-lookup"><span data-stu-id="37087-106">Deploying a Standard Edition server into an existing Enterprise Edition deployment is similar to deploying additional server roles.</span></span> <span data-ttu-id="37087-107">标准版服务器可能会部署到另一个网站，允许该网站中的用户驻留在标准版的服务器上，而不是通过广域网)  (的前端池。</span><span class="sxs-lookup"><span data-stu-id="37087-107">A Standard Edition server might be deployed to another site, allowing for users in that site to be homed on the Standard Edition server rather than the Front End pool across a wide area network (WAN).</span></span> <span data-ttu-id="37087-108">在 [部署 Lync Server 2013](lync-server-2013-deploying-lync-server.md) 文档的其他部分中已定义了在该网站中安装新网站和服务器的过程。</span><span class="sxs-lookup"><span data-stu-id="37087-108">The procedures for installing the new site and servers in that site are already defined in other sections of the [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) documentation.</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="37087-109">**定义新网站**</span><span class="sxs-lookup"><span data-stu-id="37087-109">**To define a new site**</span></span>

1.  <span data-ttu-id="37087-110">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="37087-110">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="37087-111">在控制台树中，右键单击 " **Lync Server 2013**"，然后单击 " **新建中心网站**"。</span><span class="sxs-lookup"><span data-stu-id="37087-111">In the console tree, right-click **Lync Server 2013**, and then click **New Central Site**.</span></span>

3.  <span data-ttu-id="37087-112">在 " **标识网站** " 页面上，为网站提供一个名称，并选择 "输入说明"。</span><span class="sxs-lookup"><span data-stu-id="37087-112">On the **Identify the site** page, give a name to the site and optionally enter a description.</span></span>

4.  <span data-ttu-id="37087-113">按照定义网站拓扑的其余部分中的过程操作。</span><span class="sxs-lookup"><span data-stu-id="37087-113">Follow the procedures for defining the rest of the site topology.</span></span> <span data-ttu-id="37087-114">有关详细信息，请参阅 [在 Lync Server 2013 中定义和配置拓扑](lync-server-2013-defining-and-configuring-the-topology.md)。</span><span class="sxs-lookup"><span data-stu-id="37087-114">For details, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span>

5.  <span data-ttu-id="37087-115">发布更新后的拓扑。</span><span class="sxs-lookup"><span data-stu-id="37087-115">Publish the updated topology.</span></span> <span data-ttu-id="37087-116">有关详细信息，请参阅 [在 Lync Server 2013 中发布拓扑](lync-server-2013-publish-the-topology.md)。</span><span class="sxs-lookup"><span data-stu-id="37087-116">For details, see [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md).</span></span>

6.  <span data-ttu-id="37087-117">设置和安装标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="37087-117">Set up and install a Standard Edition server.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="37087-118">如果你已使用标准版服务器部署了环境，你将从 Lync Server 部署向导开始安装过程，方法是使用 " <STRONG>准备第一个标准版服务器</STRONG> " 链接将初始数据库文件安装到新的标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="37087-118">If you have deployed an environment with only a Standard Edition server, you would have begun the setup process from the Lync Server Deployment Wizard by using the <STRONG>Prepare first Standard Edition server</STRONG> link to install the initial database files to the new Standard Edition server.</span></span> <span data-ttu-id="37087-119">在将标准版服务器安装到现有 Lync Server 2013 部署中时<STRONG>，请不要执行此</STRONG>过程。</span><span class="sxs-lookup"><span data-stu-id="37087-119"><STRONG>Do not</STRONG> follow that process when installing a Standard Edition server into an existing Lync Server 2013 deployment.</span></span>

    
    <span data-ttu-id="37087-120"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37087-120"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

