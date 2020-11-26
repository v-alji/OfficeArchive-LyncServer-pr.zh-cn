---
title: Lync Server 2013：安装 Standard Edition 服务器数据库
description: Lync Server 2013：安装标准版服务器数据库。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Standard Edition server database
ms:assetid: 0bd3a804-aad6-48cb-981b-54725af032db
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398167(v=OCS.15)
ms:contentKeyID: 48183385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a20d2c01de94ad88960555db78c57c6b79d92f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427150"
---
# <a name="install-standard-edition-server-database-for-lync-server-2013"></a><span data-ttu-id="2d9ea-103">安装适用于 Lync Server 2013 的 Standard Edition 服务器数据库</span><span class="sxs-lookup"><span data-stu-id="2d9ea-103">Install Standard Edition server database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d9ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d9ea-104">

<span> </span></span></span>

<span data-ttu-id="2d9ea-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="2d9ea-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="2d9ea-106">将标准版服务器设置为基础结构中的唯一服务器，以使家庭用户与其他服务器安装不同，因为 **部署向导** 中有专门用于设置初始服务器的选择。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-106">Setting up a Standard Edition server as the only server in your infrastructure that homes users differs from other server installations in that there is a selection in the **Deployment Wizard** specifically for setting up the initial server.</span></span>

<div>

## <a name="to-install-a-standard-edition-server"></a><span data-ttu-id="2d9ea-107">安装标准版服务器</span><span class="sxs-lookup"><span data-stu-id="2d9ea-107">To install a Standard Edition server</span></span>

1.  <span data-ttu-id="2d9ea-108">登录到要将标准版服务器安装为本地管理员或等效域的服务器。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-108">Log on to the server where you are going to install Standard Edition server as a local administrator or a domain equivalent.</span></span>

2.  <span data-ttu-id="2d9ea-109">如果尚未准备好 Active Directory 域服务，则首先执行这些过程。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-109">If you have not prepared Active Directory Domain Services, then first perform those procedures.</span></span> <span data-ttu-id="2d9ea-110">有关详细信息，请参阅 [准备适用于 Lync Server 2013 的 Active Directory 域服务](lync-server-2013-preparing-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-110">For details, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

3.  <span data-ttu-id="2d9ea-111">在 Lync Server 部署向导中，单击 " **准备第一个标准版服务器**"。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-111">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="2d9ea-112">在 " **准备单个标准版服务器** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-112">On the **Prepare single Standard Edition Server** page, click **Next**.</span></span>

5.  <span data-ttu-id="2d9ea-113">在 " **执行命令** " 页面上，SQL Server 2012 Express 作为中央管理存储进行安装。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-113">On the **Executing Commands** page, the SQL Server 2012 Express is installed as the Central Management store.</span></span> <span data-ttu-id="2d9ea-114">已创建必要的防火墙规则。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-114">Necessary firewall rules are created.</span></span> <span data-ttu-id="2d9ea-115">当数据库和必备软件的安装完成后，单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-115">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2d9ea-116">初始安装可能需要一些时间，但不显示命令输出摘要屏幕的更新。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-116">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="2d9ea-117">这是由于 SQL Server Express 的安装所致。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-117">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="2d9ea-118">如果需要监视数据库的安装，请使用 "任务管理器" 监视设置。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-118">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

6.  <span data-ttu-id="2d9ea-119">在 "Lync Server 部署向导" 页面上，如果之前尚未安装 "管理工具"，请单击 " **安装拓扑生成器** "。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-119">On the Lync Server Deployment Wizard page, click **Install Topology Builder** if you have not previously installed the administrative tools.</span></span> <span data-ttu-id="2d9ea-120">有关详细信息，请参阅 [安装 Lync Server 2013 管理工具](lync-server-2013-install-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-120">For details, see [Install Lync Server 2013 administrative tools](lync-server-2013-install-lync-server-administrative-tools.md).</span></span>

7.  <span data-ttu-id="2d9ea-121">确认 "准备 Active Directory"、"准备第一个标准版服务器" 和 "安装拓扑生成器" 旁边有绿色复选标记。</span><span class="sxs-lookup"><span data-stu-id="2d9ea-121">Confirm that there are green check marks next to “Prepare Active Directory,” “Prepare first Standard Edition server,” and “Install Topology Builder.”</span></span>

<span data-ttu-id="2d9ea-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d9ea-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

