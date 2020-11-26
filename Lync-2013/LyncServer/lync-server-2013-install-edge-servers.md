---
title: Lync Server 2013：安装边缘服务器
description: Lync Server 2013：安装 Edge 服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Edge Servers
ms:assetid: 1655ab69-3899-4ee4-a1cc-8243bc1bfa0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398230(v=OCS.15)
ms:contentKeyID: 48183503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e699a7f41b0ee554bc85fb2d9a72a2d9a42870cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427206"
---
# <a name="install-edge-servers-for-lync-server-2013"></a><span data-ttu-id="500e2-103">安装适用于 Lync Server 2013 的边缘服务器</span><span class="sxs-lookup"><span data-stu-id="500e2-103">Install Edge Servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="500e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="500e2-104">

<span> </span></span></span>

<span data-ttu-id="500e2-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="500e2-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="500e2-106">使用 Lync Server 部署向导在 Edge 服务器上安装 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="500e2-106">You install Lync Server 2013 on Edge Servers by using Lync Server Deployment Wizard.</span></span> <span data-ttu-id="500e2-107">通过在每台边缘服务器上运行部署向导，可以完成设置边缘服务器所需的大部分任务。</span><span class="sxs-lookup"><span data-stu-id="500e2-107">By running the Deployment Wizard on each Edge Server, you can complete most of the tasks required to set up the Edge Server.</span></span> <span data-ttu-id="500e2-108">为了在 Edge 服务器上部署 Lync Server 2013，你必须已运行拓扑生成器才能定义和发布你的 Edge 服务器拓扑，并将其导出到从 Edge 服务器中可用的媒体。</span><span class="sxs-lookup"><span data-stu-id="500e2-108">In order to deploy Lync Server 2013 on an Edge Server, you must have already run Topology Builder to define and publish your Edge Server topology, and exported it to media that is available from the Edge Server.</span></span> <span data-ttu-id="500e2-109">有关详细信息，请参阅 [Lync server 2013 中的外部用户访问应用场景](lync-server-2013-scenarios-for-external-user-access.md) 和 [导出 Lync server 2013 拓扑并将其复制到外部媒体进行边缘安装](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="500e2-109">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) and [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span></span>

<span data-ttu-id="500e2-110">使用部署向导安装每台边缘服务器、安装和分配所需的证书并启动所需的服务后，你可以通过在 [lync server 2013 中配置对外部用户访问的支持](lync-server-2013-configuring-support-for-external-user-access.md) 中的信息来完成设置，以启用和配置外部用户访问以及在 [lync Server 2013 中验证边缘部署](lync-server-2013-verifying-your-edge-deployment.md) 以验证设置（包括服务器和客户端连接）的信息。</span><span class="sxs-lookup"><span data-stu-id="500e2-110">After using the Deployment Wizard to install each Edge Server, install and assign the required certificates, and start the required services, you can complete the setup by using the information in [Configuring support for external user access in Lync Server 2013](lync-server-2013-configuring-support-for-external-user-access.md) to enable and configure external user access and the information in [Verifying your edge deployment in Lync Server 2013](lync-server-2013-verifying-your-edge-deployment.md) to validate the setup, including server and client connectivity.</span></span>

<div>

## <a name="to-install-an-edge-server"></a><span data-ttu-id="500e2-111">安装边缘服务器</span><span class="sxs-lookup"><span data-stu-id="500e2-111">To install an Edge Server</span></span>

1.  <span data-ttu-id="500e2-112">登录到要将边缘服务器安装为本地管理员组的成员的计算机，或者登录到具有等效用户权利和权限的帐户。</span><span class="sxs-lookup"><span data-stu-id="500e2-112">Log on to the computer on which you want to install your Edge Server as a member of the local Administrators group or an account with equivalent user rights and permissions.</span></span>

2.  <span data-ttu-id="500e2-113">请确保使用拓扑生成器创建的拓扑配置文件，然后导出并复制到外部媒体，例如，访问在其 (上复制拓扑配置文件的 USB 驱动器，或验证对将文件复制到的网络共享的访问权限) 。</span><span class="sxs-lookup"><span data-stu-id="500e2-113">Ensure that the topology configuration file you created using Topology Builder, and then exported and copied to external media, is available on the Edge Server (for example, access to the USB drive onto which you copied the topology configuration file, or verify access to the network share where you copied the file).</span></span>

3.  <span data-ttu-id="500e2-114">启动部署向导。</span><span class="sxs-lookup"><span data-stu-id="500e2-114">Start the Deployment Wizard.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="500e2-115">如果收到一条消息，指出需要安装 Microsoft Visual c + + 可再发行组件，请单击 <STRONG>"是"</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="500e2-115">If you get a message saying that you need to install Microsoft Visual C++ Redistributable, click <STRONG>Yes</STRONG>.</span></span> <span data-ttu-id="500e2-116">在下一个对话框中，您可以接受默认 <STRONG>安装位置</STRONG> ，也可以单击 " <STRONG>浏览</STRONG> " 以选择备用位置，然后单击 " <STRONG>安装</STRONG>"。</span><span class="sxs-lookup"><span data-stu-id="500e2-116">In the next dialog box, you can accept the default <STRONG>Installation Location</STRONG> or click the <STRONG>Browse</STRONG> to select an alternate location, and then click <STRONG>Install</STRONG>.</span></span> <span data-ttu-id="500e2-117">在 "下一个" 对话框中，选中 " <STRONG>我接受许可协议中的条款</STRONG> " 复选框，然后单击 <STRONG>"确定"</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="500e2-117">In the next dialog box, select the <STRONG>I accept the terms in the license agreement</STRONG> check box, and then click <STRONG>OK</STRONG>.</span></span>

    
    </div>

4.  <span data-ttu-id="500e2-118">在部署向导中，单击 " **安装或更新 Lync Server 系统**"。</span><span class="sxs-lookup"><span data-stu-id="500e2-118">In the Deployment Wizard, click **Install or Update Lync Server System**.</span></span>

5.  <span data-ttu-id="500e2-119">向导确定部署状态后，针对 **步骤1。安装本地配置存储**，单击 " **运行** "，然后执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="500e2-119">After the wizard determines the deployment state, for **Step 1. Install Local Configuration Store**, click **Run** and then do the following:</span></span>
    
      - <span data-ttu-id="500e2-120">在 " **配置中央管理存储的本地副本** " 对话框中，单击 " **从文件导入 (对于边缘服务器) 推荐的文件**，转到导出的拓扑配置文件的位置，选择 .zip 文件，单击" **打开**"，然后单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="500e2-120">In the **Configure Local Replica of Central Management Store** dialog box, click **Import from a file (Recommended for Edge Servers)**, go to the location of the exported topology configuration file, select the .zip file, click **Open**, and then click **Next**.</span></span>
    
      - <span data-ttu-id="500e2-121">部署向导从配置文件中读取配置信息，并将 XML 配置文件写入本地计算机。</span><span class="sxs-lookup"><span data-stu-id="500e2-121">The Deployment Wizard reads the configuration information from the configuration file and writes the XML configuration file to the local computer.</span></span>
    
      - <span data-ttu-id="500e2-122">“**正在执行命令**”过程完成后，单击“**完成**”。</span><span class="sxs-lookup"><span data-stu-id="500e2-122">After the **Executing Commands** process is finished, click **Finish**.</span></span>

6.  <span data-ttu-id="500e2-123">在 "部署向导" 中，单击 " **步骤2：设置" 或 "删除 Lync Server 组件** " 以安装在存储在本地计算机上的 XML 配置文件中指定的 Lync server 2013 edge 组件。</span><span class="sxs-lookup"><span data-stu-id="500e2-123">In the Deployment Wizard, click **Step 2: SetUp or Remove Lync Server Components** to install the Lync Server 2013 edge components specified in the XML configuration file that is stored on the local computer.</span></span>

7.  <span data-ttu-id="500e2-124">完成安装后，使用 [Lync Server 2013 的边缘证书为 Lync Server 设置边缘证书](lync-server-2013-set-up-edge-certificates.md) ，以便在启动服务之前安装和分配所需的证书。</span><span class="sxs-lookup"><span data-stu-id="500e2-124">After completing the installation, use the information in [Set up Edge certificates for Lync Server 2013](lync-server-2013-set-up-edge-certificates.md) to install and assign the required certificates before you start services.</span></span>

<span data-ttu-id="500e2-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="500e2-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

