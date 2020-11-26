---
title: Lync Server 2013：运行架构准备
description: Lync Server 2013：运行架构准备。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running schema preparation
ms:assetid: 9d02bdb1-ff29-417a-bcce-b068b31207d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412729(v=OCS.15)
ms:contentKeyID: 48184911
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0991bbff7f54f8b8b9eb01fc87f752e00f3dcbfd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442192"
---
# <a name="running-active-directory-schema-preparation-in-lync-server-2013"></a><span data-ttu-id="92cf1-103">在 Lync Server 2013 中运行 Active Directory 架构准备</span><span class="sxs-lookup"><span data-stu-id="92cf1-103">Running Active Directory schema preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="92cf1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="92cf1-104">

<span> </span></span></span>

<span data-ttu-id="92cf1-105">_**主题上次修改时间：** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="92cf1-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="92cf1-106">你可以使用安装程序或 Lync Server Management Shell cmdlet 来准备 Active Directory 架构。</span><span class="sxs-lookup"><span data-stu-id="92cf1-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the Active Directory schema.</span></span> <span data-ttu-id="92cf1-107">扩展 Active Directory 架构的 cmdlet 为 **Install-CsAdServerSchema**。</span><span class="sxs-lookup"><span data-stu-id="92cf1-107">The cmdlet that extends the Active Directory schema is **Install-CsAdServerSchema**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="92cf1-108"> (<STRONG>安装</STRONG> 的架构准备 cmdlet) 必须访问架构主机，这要求远程注册表服务正在运行且远程注册表项已启用。</span><span class="sxs-lookup"><span data-stu-id="92cf1-108">The schema preparation cmdlet (<STRONG>Install-CsAdServerSchema</STRONG>) must access the schema master, which requires that the remote registry service is running and that the remote registry key is enabled.</span></span> <span data-ttu-id="92cf1-109">如果无法在架构主机上启用远程注册表服务，则可以在架构主机上本地运行 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92cf1-109">If the remote registry service cannot be enabled on the schema master, you can run the cmdlet locally on the schema master.</span></span> <span data-ttu-id="92cf1-110">有关注册表远程访问的详细信息，请参阅 Microsoft 知识库文章 314837 "如何管理对注册表的远程访问" <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A> 。</span><span class="sxs-lookup"><span data-stu-id="92cf1-110">For details about registry remote access, see Microsoft Knowledge Base article 314837, "How to Manage Remote Access to the Registry," at <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A>.</span></span>



</div>

<span data-ttu-id="92cf1-111">完成架构准备后，手动验证架构分区是否已复制，然后再继续执行林准备。</span><span class="sxs-lookup"><span data-stu-id="92cf1-111">After you complete schema preparation, manually verify that the schema partition has been replicated before proceeding to forest preparation.</span></span> <span data-ttu-id="92cf1-112">有关详细信息，请参阅 [在 Lync Server 2013 中验证 Active Directory 架构复制](lync-server-2013-verifying-schema-replication.md)。</span><span class="sxs-lookup"><span data-stu-id="92cf1-112">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="92cf1-113">使用安装程序准备当前林的架构</span><span class="sxs-lookup"><span data-stu-id="92cf1-113">To use Setup to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="92cf1-114">以架构管理员组的成员身份登录到林中的服务器，并使用架构主机上的管理员权限登录。</span><span class="sxs-lookup"><span data-stu-id="92cf1-114">Log on to a server in your forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="92cf1-115">在 Lync Server 2013 安装文件夹或媒体中，运行 Setup.exe 以启动部署向导。</span><span class="sxs-lookup"><span data-stu-id="92cf1-115">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="92cf1-116">如果系统提示您安装 Microsoft Visual c + + 可再发行组件，请单击 **"是"**。</span><span class="sxs-lookup"><span data-stu-id="92cf1-116">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>

4.  <span data-ttu-id="92cf1-117">"Lync Server 2013 设置" 对话框提示你输入安装 Lync Server 文件的位置。</span><span class="sxs-lookup"><span data-stu-id="92cf1-117">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="92cf1-118">选择默认位置或 **浏览** 到您选择的位置，然后单击 " **安装**"。</span><span class="sxs-lookup"><span data-stu-id="92cf1-118">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>

5.  <span data-ttu-id="92cf1-119">在 "许可协议" 页面上，选中 " **我接受许可协议中的条款**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="92cf1-119">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span>

6.  <span data-ttu-id="92cf1-120">安装程序安装 Lync Server 核心组件。</span><span class="sxs-lookup"><span data-stu-id="92cf1-120">The installer installs the Lync Server Core Components.</span></span>

7.  <span data-ttu-id="92cf1-121">当部署向导准备就绪时，单击 " **准备 Active Directory**"，然后等待确定部署状态。</span><span class="sxs-lookup"><span data-stu-id="92cf1-121">When the Deployment Wizard is ready, click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

8.  <span data-ttu-id="92cf1-122">在 **步骤1：准备架构** 中，单击 " **运行**"。</span><span class="sxs-lookup"><span data-stu-id="92cf1-122">At **Step 1: Prepare Schema**, click **Run**.</span></span>

9.  <span data-ttu-id="92cf1-123">在 " **准备架构** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="92cf1-123">On the **Prepare Schema** page, click **Next**.</span></span>

10. <span data-ttu-id="92cf1-124">在“**正在执行命令**”页上，查找“**任务状态：已完成**”，然后单击“**查看日志**”。</span><span class="sxs-lookup"><span data-stu-id="92cf1-124">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

11. <span data-ttu-id="92cf1-125">在 " **操作** " 列下，展开 " **架构准备**"， **\<Success\>** 在每个任务的末尾查找执行结果，验证架构准备是否成功完成，关闭日志，然后单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="92cf1-125">Under the **Action** column, expand **Schema Prep**, look for the **\<Success\>** Execution Result at the end of each task to verify that schema preparation completed successfully, close the log, and then click **Finish**.</span></span>

12. <span data-ttu-id="92cf1-126">等待 Active Directory 复制完成或强制执行复制。</span><span class="sxs-lookup"><span data-stu-id="92cf1-126">Wait for Active Directory replication to complete or force replication.</span></span>

13. <span data-ttu-id="92cf1-127">手动验证架构更改是否已复制到所有其他域控制器。</span><span class="sxs-lookup"><span data-stu-id="92cf1-127">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="92cf1-128">有关详细信息，请参阅 [在 Lync Server 2013 中验证 Active Directory 架构复制](lync-server-2013-verifying-schema-replication.md)。</span><span class="sxs-lookup"><span data-stu-id="92cf1-128">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="92cf1-129">使用 cmdlet 准备当前林的架构</span><span class="sxs-lookup"><span data-stu-id="92cf1-129">To use cmdlets to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="92cf1-130">以架构管理员组的成员身份登录到林中的计算机，并使用架构主机上的管理员权限登录。</span><span class="sxs-lookup"><span data-stu-id="92cf1-130">Log on to a computer in the forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="92cf1-131">安装 Lync Server Core 组件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="92cf1-131">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="92cf1-132">在 Lync Server 2013 安装文件夹或媒体中，运行 Setup.exe 以启动 Lync Server 部署向导。</span><span class="sxs-lookup"><span data-stu-id="92cf1-132">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="92cf1-133">如果系统提示您安装 Microsoft Visual c + + 可再发行组件，请单击 **"是"**。</span><span class="sxs-lookup"><span data-stu-id="92cf1-133">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="92cf1-134">"Lync Server 2013 设置" 对话框提示你输入安装 Lync Server 文件的位置。</span><span class="sxs-lookup"><span data-stu-id="92cf1-134">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="92cf1-135">选择默认位置或 **浏览** 到您选择的位置，然后单击 " **安装**"。</span><span class="sxs-lookup"><span data-stu-id="92cf1-135">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="92cf1-136">在 "许可协议" 页面上，选中 " **我接受许可协议中的条款**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="92cf1-136">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="92cf1-137">安装程序安装 Lync Server 2013 核心组件。</span><span class="sxs-lookup"><span data-stu-id="92cf1-137">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="92cf1-138">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="92cf1-138">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="92cf1-139">运行：</span><span class="sxs-lookup"><span data-stu-id="92cf1-139">Run:</span></span>
    
        Install-CsAdServerSchema [-Ldf <directory where the .ldf file is located>] 
    
    <span data-ttu-id="92cf1-140">如果不指定 Ldf 参数，则默认值为从注册表中读取的 Lync Server 2013 安装路径。</span><span class="sxs-lookup"><span data-stu-id="92cf1-140">If you do not specify the Ldf parameter, the default value is the Lync Server 2013 installation path that is read from the registry.</span></span>
    
    <span data-ttu-id="92cf1-141">例如：</span><span class="sxs-lookup"><span data-stu-id="92cf1-141">For example:</span></span>
    
        Install-CsAdServerSchema -Ldf "C:\Program Files\Microsoft Lync Server 2013\Deployment\Setup"

5.  <span data-ttu-id="92cf1-142">使用以下 cmdlet 验证架构准备是否已完成运行。</span><span class="sxs-lookup"><span data-stu-id="92cf1-142">Use the following cmdlet to verify that schema preparation ran to completion.</span></span>
    
        Get-CsAdServerSchema 
    
    <span data-ttu-id="92cf1-143">如果架构准备成功，此 cmdlet 将返回 **架构 \_ 版本 \_ 状态的 \_ 当前** 值。</span><span class="sxs-lookup"><span data-stu-id="92cf1-143">This cmdlet returns a value of **SCHEMA\_VERSION\_STATE\_CURRENT** if schema preparation was successful.</span></span>

6.  <span data-ttu-id="92cf1-144">等待 Active Directory 复制完成或强制执行复制。</span><span class="sxs-lookup"><span data-stu-id="92cf1-144">Wait for Active Directory replication to complete or force replication.</span></span>

7.  <span data-ttu-id="92cf1-145">手动验证架构更改是否已复制到所有其他域控制器。</span><span class="sxs-lookup"><span data-stu-id="92cf1-145">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="92cf1-146">有关详细信息，请参阅 [在 Lync Server 2013 中验证 Active Directory 架构复制](lync-server-2013-verifying-schema-replication.md)。</span><span class="sxs-lookup"><span data-stu-id="92cf1-146">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="92cf1-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="92cf1-147">See Also</span></span>


[<span data-ttu-id="92cf1-148">在 Lync Server 2013 中验证 Active Directory 架构复制</span><span class="sxs-lookup"><span data-stu-id="92cf1-148">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)  


[<span data-ttu-id="92cf1-149">在 Lync Server 2013 中准备 Active Directory 架构</span><span class="sxs-lookup"><span data-stu-id="92cf1-149">Preparing the Active Directory schema in Lync Server 2013</span></span>](lync-server-2013-preparing-the-active-directory-schema.md)  
  

<span data-ttu-id="92cf1-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="92cf1-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

