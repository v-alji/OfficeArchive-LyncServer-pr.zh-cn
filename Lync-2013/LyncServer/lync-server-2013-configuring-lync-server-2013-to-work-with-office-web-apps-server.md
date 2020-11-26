---
title: 将 Lync Server 2013 配置为使用 Office Web Apps 服务器
description: 将 Lync Server 2013 配置为使用 Office Web Apps 服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Lync Server 2013 to work with Office Web Apps Server
ms:assetid: 6231e519-9010-4ff9-b5a6-b5859c2b3e11
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204944(v=OCS.15)
ms:contentKeyID: 48184288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e53500e0ad272c81340c25946f5b7f8e72a121
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433009"
---
# <a name="configuring-lync-server-2013-to-work-with-office-web-apps-server"></a><span data-ttu-id="81a0a-103">将 Lync Server 2013 配置为使用 Office Web Apps 服务器</span><span class="sxs-lookup"><span data-stu-id="81a0a-103">Configuring Lync Server 2013 to work with Office Web Apps Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81a0a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81a0a-104">

<span> </span></span></span>

<span data-ttu-id="81a0a-105">_**主题上次修改时间：** 2013-04-22_</span><span class="sxs-lookup"><span data-stu-id="81a0a-105">_**Topic Last Modified:** 2013-04-22_</span></span>

<span data-ttu-id="81a0a-106">必须先部署和配置 Office Web Apps 服务器，然后才能将 Lync Server 2013 配置为使用 Office Web Apps 服务器。</span><span class="sxs-lookup"><span data-stu-id="81a0a-106">Before you can configure Lync Server 2013 to use Office Web Apps Server, Office Web Apps Server must be deployed and configured.</span></span> <span data-ttu-id="81a0a-107">有关如何安装和配置单个 Office Web Apps 服务器的详细信息，请参阅文档指南，有关如何安装和配置 Office Web Apps 服务器场以获得高可用性的详细信息，请参阅文档 **指南** 。</span><span class="sxs-lookup"><span data-stu-id="81a0a-107">See the document **Guide to Deploying Office Web Apps Server and Office Web Apps** for detail information on how to install and configure a single Office Web Apps Server, or for information on how to install and configure an Office Web Apps Server Farm for high availability.</span></span>

<span data-ttu-id="81a0a-108">成功安装 Office Web Apps 服务器并正确配置 Web 场后，必须配置 Lync 服务器才能与新服务器通信;可通过将 Office Web Apps 服务器发现 URL 添加到 Lync Server 拓扑来完成此操作。</span><span class="sxs-lookup"><span data-stu-id="81a0a-108">After Office Web Apps Server has been successfully installed and your Web farm correctly configured, you must then configure Lync Server to communicate with the new server; this is done by adding the Office Web Apps Server discovery URL to your Lync Server topology.</span></span> <span data-ttu-id="81a0a-109">若要向拓扑中添加 Office Web Apps 服务器，请完成下列步骤：</span><span class="sxs-lookup"><span data-stu-id="81a0a-109">To add Office Web Apps Server to your topology, complete the following steps:</span></span>

1.  <span data-ttu-id="81a0a-110">单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="81a0a-110">Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="81a0a-111">在“**拓扑生成器**”对话框中，选择“**从现有部署下载拓扑**”，然后单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="81a0a-111">In the **Topology Builder** dialog box, select **Download Topology from existing deployment** and then click **OK**.</span></span>

3.  <span data-ttu-id="81a0a-p103">在“**将拓扑另存为**”对话框的“**文件名**”框中为拓扑文档键入一个名称（例如“**PreWebAppsServerTopology**”），然后单击“**保存**”。如果之后你的新拓扑遇到问题，则可检索和重新发布此拓扑。</span><span class="sxs-lookup"><span data-stu-id="81a0a-p103">In the **Save Topology As** dialog box, type a name for your topology document (for example, **PreWebAppsServerTopology**) in the **File name** box and then click **Save**. This topology can later be retrieved and republished if you encounter problems with your new topology.</span></span>

4.  <span data-ttu-id="81a0a-114">在拓扑生成器中，展开 " **Lync Server 2013**"，展开您的网站的名称，展开 " **企业版前端池**"，右键单击其中一个池的名称，然后单击 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="81a0a-114">In Topology Builder, expand **Lync Server 2013**, expand the name of your site, expand **Enterprise Edition Front End pools**, right-click the name of one of your pools, and then click **Edit Properties**.</span></span>

5.  <span data-ttu-id="81a0a-115">在“**编辑属性**”对话框的“**常规**”选项卡上，查找标题“**关联 Office Web Apps 服务器**”，然后单击“**新建**”（或从下拉列表中选择现有 Office Web Apps 服务器）。</span><span class="sxs-lookup"><span data-stu-id="81a0a-115">In the **Edit Properties** dialog box, on the **General** tab, find the heading **Associate Office Web Apps Server** and then click **New** (or select an existing Office Web Apps Server from the drop-down list).</span></span>

6.  <span data-ttu-id="81a0a-116">在“**定义新的 Office Web Apps 服务器**”对话框的“**Office Web Apps 服务器 FQDN**”框中，键入你的 Office Web Apps 服务器计算机的完全限定域名 (FQDN)；执行此操作时，你的 Office Web Apps 服务器搜索 URL 应自动输入到“**Office Web Apps 服务器搜索 URL**”框中。</span><span class="sxs-lookup"><span data-stu-id="81a0a-116">In the **Define New Office Web Apps Server** dialog box, type the fully qualified domain name (FQDN) of your Office Web Apps Server computer in the **Office Web Apps Server FQDN** box; when you do this, your Office Web Apps Server discovery URL should automatically be entered into the **Office Web Apps Server discovery URL** box.</span></span>
    
    <span data-ttu-id="81a0a-117">如果 Office Web Apps 服务器在本地安装，并且在与 Lync Server 2013 相同的网络区域中安装，则会在 **外部网络中部署 "Office Web apps" 服务器 (也就是说，不应选择 "外围/Internet) "** 。</span><span class="sxs-lookup"><span data-stu-id="81a0a-117">If the Office Web Apps Server is installed on-premises and in the same network zone as Lync Server 2013 then the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)** should not be selected.</span></span>
    
    <span data-ttu-id="81a0a-118">如果 Office Web Apps 服务器部署在内部防火墙之外，则请选择选项“**在外部网络(即，外围/Internet)中部署 Office Web Apps 服务器**”。</span><span class="sxs-lookup"><span data-stu-id="81a0a-118">If the Office Web Apps Server is deployed outside your internal firewall, then select the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)**.</span></span>

7.  <span data-ttu-id="81a0a-119">在“**定义新的 Office Web Apps Server**”对话框中，单击“**确定**”，然后在“**编辑属性**”对话框中单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="81a0a-119">In the **Define New Office Web Apps Server** dialog box, click **OK**, and then click **OK** in the **Edit Properties** dialog box.</span></span> <span data-ttu-id="81a0a-120">Office Web Apps 发现 URL 随后将作为该池的关联之一列出。</span><span class="sxs-lookup"><span data-stu-id="81a0a-120">The Office Web Apps discovery URL will then be listed as one of the pool's Associations.</span></span>

<span data-ttu-id="81a0a-121">您必须对需要与您的 Office Web Apps 服务器关联的每个池重复此过程。</span><span class="sxs-lookup"><span data-stu-id="81a0a-121">You will have to repeat this process for each pool that needs to be associated with your Office Web Apps Server.</span></span>

<span data-ttu-id="81a0a-122">将发现 URL 添加到拓扑后，必须随后发布此更新后的拓扑。</span><span class="sxs-lookup"><span data-stu-id="81a0a-122">After you have added the discovery URL to the topology you must then publish this updated topology.</span></span> <span data-ttu-id="81a0a-123">若要在拓扑生成器中执行此操作：</span><span class="sxs-lookup"><span data-stu-id="81a0a-123">To do that in Topology Builder:</span></span>

1.  <span data-ttu-id="81a0a-124">单击“**操作**”，然后单击“**发布拓扑**”。</span><span class="sxs-lookup"><span data-stu-id="81a0a-124">Click **Action** and then click **Publish Topology**.</span></span>

2.  <span data-ttu-id="81a0a-125">在发布拓扑向导的“**发布拓扑**”页上，单击“**下一步**”。</span><span class="sxs-lookup"><span data-stu-id="81a0a-125">In the Publish Topology wizard, on the **Publish the Topology** page, click **Next**.</span></span>

3.  <span data-ttu-id="81a0a-126">在“**发布向导完成**”页上，单击“**完成**”。</span><span class="sxs-lookup"><span data-stu-id="81a0a-126">On the **Publishing wizard complete** page, click **Finish**.</span></span>

4.  <span data-ttu-id="81a0a-127">关闭拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="81a0a-127">Close Topology Builder.</span></span>

<span data-ttu-id="81a0a-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81a0a-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

