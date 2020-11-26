---
title: Lync Server 2013：安装 Lync Server 管理工具
description: Lync Server 2013：安装 Lync Server 管理工具。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Lync Server administrative tools
ms:assetid: 842b85e4-2eeb-464f-b1c1-ceb8cc04f8d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398665(v=OCS.15)
ms:contentKeyID: 48184695
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca1ad96299197c3339d06c4f094784edc632e6b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427192"
---
# <a name="install-lync-server-2013-administrative-tools"></a><span data-ttu-id="27a14-103">安装 Lync Server 2013 管理工具</span><span class="sxs-lookup"><span data-stu-id="27a14-103">Install Lync Server 2013 administrative tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27a14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27a14-104">

<span> </span></span></span>

<span data-ttu-id="27a14-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="27a14-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="27a14-106">本主题介绍了如何安装您需要用于部署和管理 Lync Server 2013 的管理工具。</span><span class="sxs-lookup"><span data-stu-id="27a14-106">This topic describes how to install the administrative tools you need to use to deploy and manage Lync Server 2013.</span></span> <span data-ttu-id="27a14-107">默认情况下，在运行 Lync Server 2013 的每台服务器上安装 "管理工具"。</span><span class="sxs-lookup"><span data-stu-id="27a14-107">The administrative tools are installed by default on each server running Lync Server 2013.</span></span> <span data-ttu-id="27a14-108">此外，还可以在其他计算机上安装管理工具，如专用管理控制台。</span><span class="sxs-lookup"><span data-stu-id="27a14-108">Additionally, you can install the administrative tools on other computers, such as dedicated administrative consoles.</span></span> <span data-ttu-id="27a14-109">强烈建议在你正在创建的 Lync Server 2013 部署所在的计算机上安装管理工具，因为这样做是为了确保已完成 Active Directory 域服务准备步骤，从而使你可以在以后使用该计算机上的管理工具发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="27a14-109">We strongly recommend that you install the administrative tools on a computer that is in the same domain or forest as the Lync Server 2013 deployment you are creating because by doing so you make sure that Active Directory Domain Services preparation steps are already complete, which enables you to use the administrative tools on that computer later to publish your topology.</span></span>

<span data-ttu-id="27a14-110">在安装或使用 Lync Server 2013 管理工具之前，请确保查看基础结构、操作系统、软件和管理员权限要求。</span><span class="sxs-lookup"><span data-stu-id="27a14-110">Make sure that you review infrastructure, operating system, software, and administrator rights requirements before you install or use the Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="27a14-111">有关基础结构要求的详细信息，请参阅 [Lync Server 2013 中的管理工具基础结构要求](lync-server-2013-administrative-tools-infrastructure-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="27a14-111">For details about infrastructure requirements, see [Administrative tools infrastructure requirements in Lync Server 2013](lync-server-2013-administrative-tools-infrastructure-requirements.md).</span></span> <span data-ttu-id="27a14-112">有关操作系统和软件要求的详细信息安装 Lync Server 2013 管理工具，请参阅 lync [server 2013 中的 "服务器和工具" 操作系统支持](lync-server-2013-server-and-tools-operating-system-support.md)、lync [server 2013 的其他软件要求](lync-server-2013-additional-software-requirements.md)以及 [Lync server 2013 中的其他服务器支持和要求](lync-server-2013-additional-server-support-and-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="27a14-112">For details about operating system and software requirements to install the Lync Server 2013 administrative tools, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md), [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md), and [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md).</span></span> <span data-ttu-id="27a14-113">有关安装和使用工具所需的用户权利和权限的详细信息，请参阅 [安装和管理 Lync Server 2013 所需的管理员权利和权限](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="27a14-113">For details about the user rights and permissions required to install and use the tools, see [Administrator rights and permissions required for setup and administration of Lync Server 2013](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="27a14-114">如果你的组织需要在除系统驱动器之外的驱动器上查找 Internet 信息服务 (IIS) 和所有 Web 服务，则可以在 "设置" 对话框中更改 Lync Server 文件的安装位置路径。</span><span class="sxs-lookup"><span data-stu-id="27a14-114">If your organization requires that you locate Internet Information Services (IIS) and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server files in the Setup dialog box.</span></span> <span data-ttu-id="27a14-115">如果将安装文件安装到此路径（包括 OCSCore.msi），则会将其他 Lync Server 2013 文件也部署到此驱动器。</span><span class="sxs-lookup"><span data-stu-id="27a14-115">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span>



</div>

<div>

## <a name="to-install-the-lync-server-2013-administrative-tools"></a><span data-ttu-id="27a14-116">安装 Lync Server 2013 管理工具</span><span class="sxs-lookup"><span data-stu-id="27a14-116">To install the Lync Server 2013 administrative tools</span></span>

1.  <span data-ttu-id="27a14-117">以本地管理员身份登录 (最低要求) 要安装管理工具的计算机。</span><span class="sxs-lookup"><span data-stu-id="27a14-117">Log on as a local administrator (minimum requirement) to the computer where you want to install the administrative tools.</span></span> <span data-ttu-id="27a14-118">如果您在 Windows Vista 或 Windows 7 操作系统上以标准用户身份登录，并且用户帐户控制 (UAC) 处于启用状态，系统将提示您输入本地管理员或域等效的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="27a14-118">If you are logged on as an a standard user on the Windows Vista or Windows 7 operating systems, and User Account Control (UAC) is enabled, you will be prompted for the local administrator or a domain equivalent user name and password.</span></span>

2.  <span data-ttu-id="27a14-119">在计算机上找到安装媒体，然后双击 " \\ 设置 \\ amd64 \\Setup.exe"。</span><span class="sxs-lookup"><span data-stu-id="27a14-119">Locate the installation media on your computer, and then double-click \\Setup\\amd64\\Setup.exe.</span></span>

3.  <span data-ttu-id="27a14-120">如果系统提示您安装 Microsoft Visual c + + 2008 可分发，请单击 **"是"**。</span><span class="sxs-lookup"><span data-stu-id="27a14-120">If you are prompted to install the Microsoft Visual C++ 2008 distributable, click **Yes**.</span></span>

4.  <span data-ttu-id="27a14-121">在 " **Microsoft Lync Server 2013 安装位置** " 页面上，单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="27a14-121">On the **Microsoft Lync Server 2013 Installation Location** page, click **OK**.</span></span> <span data-ttu-id="27a14-122">如果需要将文件安装到其他位置，请将此路径更改为其他位置或驱动器。</span><span class="sxs-lookup"><span data-stu-id="27a14-122">Change this path to another location or drive if you need to have the files installed to another location.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="27a14-123">如果你的组织需要在除系统驱动器之外的驱动器上查找 Internet 信息服务 (IIS) 和所有 Web 服务，则可以在 "设置" 对话框中更改 Lync Server 2013 文件的安装位置路径。</span><span class="sxs-lookup"><span data-stu-id="27a14-123">If your organization requires that you locate Internet Information Services (IIS) and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box.</span></span> <span data-ttu-id="27a14-124">如果将安装文件安装到此路径（包括 OCSCore.msi），则将同时向此驱动器部署 Lync Server 2013 文件的其余部分。</span><span class="sxs-lookup"><span data-stu-id="27a14-124">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive too.</span></span>

    
    </div>

5.  <span data-ttu-id="27a14-125">在 " **最终用户许可协议** " 页面上，查看许可条款，单击 " **我接受**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="27a14-125">On the **End User License Agreement** page, review the license terms, click **I accept**, and then click **OK**.</span></span> <span data-ttu-id="27a14-126">必须先执行此步骤，然后才能继续。</span><span class="sxs-lookup"><span data-stu-id="27a14-126">This step is required before you can continue.</span></span>

6.  <span data-ttu-id="27a14-127">在 " **Microsoft Lync Server 2013-部署向导** " 页面上，单击 " **安装管理员工具**"。</span><span class="sxs-lookup"><span data-stu-id="27a14-127">On the **Microsoft Lync Server 2013 – Deployment Wizard** page, click **Install Administrator Tools**.</span></span>

7.  <span data-ttu-id="27a14-128">安装成功完成后，单击 " **退出**"。</span><span class="sxs-lookup"><span data-stu-id="27a14-128">When the installation successfully completes, click **Exit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="27a14-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27a14-129">See Also</span></span>


[<span data-ttu-id="27a14-130">打开 Lync Server 2013 管理工具</span><span class="sxs-lookup"><span data-stu-id="27a14-130">Open Lync Server 2013 administrative tools</span></span>](lync-server-2013-open-lync-server-administrative-tools.md)  


[<span data-ttu-id="27a14-131">Lync Server 2013 管理工具</span><span class="sxs-lookup"><span data-stu-id="27a14-131">Lync Server 2013 administrative tools</span></span>](lync-server-2013-lync-server-administrative-tools.md)  
  

<span data-ttu-id="27a14-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27a14-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

