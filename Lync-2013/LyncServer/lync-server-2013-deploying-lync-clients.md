---
title: Lync Server 2013：部署 Lync 客户端
description: Lync Server 2013：部署 Lync 客户端。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync clients
ms:assetid: 3d10abf2-d484-4fa0-8f10-4a5f9dfba4f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204827(v=OCS.15)
ms:contentKeyID: 48183925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09b501fc721ac880c5cf7da0293e3aa9c6443722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429984"
---
# <a name="deploying-lync-clients-in-lync-server-2013"></a><span data-ttu-id="e0190-103">在 Lync Server 2013 中部署 Lync 客户端</span><span class="sxs-lookup"><span data-stu-id="e0190-103">Deploying Lync clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0190-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0190-104">

<span> </span></span></span>

<span data-ttu-id="e0190-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="e0190-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="e0190-106">Lync 2013 引入了一种不同的客户端部署方法。</span><span class="sxs-lookup"><span data-stu-id="e0190-106">Lync 2013 introduces a different approach to client deployment.</span></span> <span data-ttu-id="e0190-107">在以前版本的出发期间，Lync 2013 不再拥有自己的安装程序。</span><span class="sxs-lookup"><span data-stu-id="e0190-107">In a departure from previous releases, Lync 2013 no longer has its own installer.</span></span> <span data-ttu-id="e0190-108">而是在 Office 2013 安装程序中随附 Lync。</span><span class="sxs-lookup"><span data-stu-id="e0190-108">Instead, Lync is included with the Office 2013 setup program.</span></span> <span data-ttu-id="e0190-109">若要将 Lync 2013 部署到你的用户，你可以使用 Office 2013 安装方法和自定义工具。</span><span class="sxs-lookup"><span data-stu-id="e0190-109">To deploy Lync 2013 to your users, you can use Office 2013 installation methods and customization tools.</span></span>

  - <span data-ttu-id="e0190-110">**Office 2013 Windows installer** 是基于 Windows 安装程序包的安装程序包，它包含多个 MSI 文件。</span><span class="sxs-lookup"><span data-stu-id="e0190-110">**Office 2013 Windows Installer** is a Windows Installer-based installation package that consists of multiple MSI files.</span></span> <span data-ttu-id="e0190-111">一个与语言无关的核心 MSI 包与一个或多个特定语言的包组合在一起构成了完整产品。</span><span class="sxs-lookup"><span data-stu-id="e0190-111">A language-neutral core MSI package is combined with one or more language-specific packages to make a complete product.</span></span> <span data-ttu-id="e0190-112">在用户计算机上安装 Office 的过程中以及安装之后，安装程序将组合各个包并执行自定义和维护任务。</span><span class="sxs-lookup"><span data-stu-id="e0190-112">Setup assembles the individual packages and performs customization and maintenance tasks during and after installation of Office on users' computers.</span></span> <span data-ttu-id="e0190-113">本部分中的主题介绍了如何使用和自定义 Office 2013 的 Windows 安装程序来部署 Lync 2013。</span><span class="sxs-lookup"><span data-stu-id="e0190-113">The topics in this section describe how to use and customize the Office 2013 Windows Installer to deploy Lync 2013.</span></span>

  - <span data-ttu-id="e0190-114">**Office 2013 即点** 即用是从 Microsoft 365 管理中心将 Office 安装程序文件流式处理到用户的安装程序。</span><span class="sxs-lookup"><span data-stu-id="e0190-114">**Office 2013 Click-to-Run** is an installation program that streams Office setup files to the user from the Microsoft 365 admin center.</span></span> <span data-ttu-id="e0190-115">通过使用针对即点即用的 Office 部署工具，管理员可以自定义安装。</span><span class="sxs-lookup"><span data-stu-id="e0190-115">Administrators can customize installation by using the Office Deployment Tool for Click-to-Run.</span></span> <span data-ttu-id="e0190-116">由于 Office 2013 的即点即用主要用于 Microsoft 365 环境，本部分中不详细介绍此安装方法。</span><span class="sxs-lookup"><span data-stu-id="e0190-116">Because Office 2013 Click-to-Run is primarily used in the Microsoft 365 environment, this installation method is not described in detail in this section.</span></span> <span data-ttu-id="e0190-117">有关如何使用和自定义即点即用安装的详细信息，请参阅 Office 2013 资源工具包文档。</span><span class="sxs-lookup"><span data-stu-id="e0190-117">Detailed information about using and customizing Click-to-Run installation is available in the Office 2013 Resource Kit documentation.</span></span> <span data-ttu-id="e0190-118">管理员还可以将 Office 2013 的即点即用程序和语言源文件下载到本地位置，这在你希望最大程度地减少对网络的需求或防止用户因公司安全要求而从 Internet 安装软件时非常有用。</span><span class="sxs-lookup"><span data-stu-id="e0190-118">Administrators can also download the Office 2013 Click-to-Run program and language source files to an on-premises location, which is useful when you want to minimize the demand on the network or prevent users from installing software from the Internet because of corporate security requirements.</span></span>

<span data-ttu-id="e0190-119">本部分中的主题重点介绍如何使用基于 Office 2013 的基于 MSI 的安装程序部署客户端。</span><span class="sxs-lookup"><span data-stu-id="e0190-119">The topics in this section focus on how to deploy clients by using the Office 2013 MSI-based installer.</span></span> <span data-ttu-id="e0190-120">您的主参考应是 Office 2013 资源工具包文档，其中详细介绍了如何准备基础结构、自定义安装和部署 Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e0190-120">Your primary reference should be the Office 2013 Resource Kit documentation, which describes in detail how to prepare your infrastructure, customize setup, and deploy Office 2013.</span></span> <span data-ttu-id="e0190-121">但是，你应将 Office 文档与本部分中的主题结合使用，以指出特定于 Lync 2013 的部署注意事项。</span><span class="sxs-lookup"><span data-stu-id="e0190-121">However, you should use the Office documentation in conjunction with topics in this section, which point out deployment considerations that are specific to Lync 2013.</span></span>

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="e0190-122">Lync 2013 的联机会议加载项（支持来自 Outlook 消息和协作客户端的会议管理）将自动与 Lync 2013 一起安装。</span><span class="sxs-lookup"><span data-stu-id="e0190-122">The Online Meeting Add-in for Lync 2013, which supports meeting management from within the Outlook messaging and collaboration client, installs automatically with Lync 2013.</span></span></P>
> <LI>
> <P><span data-ttu-id="e0190-123">Office 2013 安装程序不会卸载以前版本的 Lync 或 Office Communicator。</span><span class="sxs-lookup"><span data-stu-id="e0190-123">The Office 2013 setup program does not uninstall previous versions of Lync or Office Communicator.</span></span> <span data-ttu-id="e0190-124">Lync 2013 客户端与其他 Lync 或 Office Communicator 客户端并行安装</span><span class="sxs-lookup"><span data-stu-id="e0190-124">The Lync 2013 client installs side-by-side with other Lync or Office Communicator clients</span></span></P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e0190-125">本节内容</span><span class="sxs-lookup"><span data-stu-id="e0190-125">In This Section</span></span>

  - [<span data-ttu-id="e0190-126">在 Lync Server 2013 中自定义客户端安装</span><span class="sxs-lookup"><span data-stu-id="e0190-126">Customizing client installation in Lync Server 2013</span></span>](lync-server-2013-customizing-client-installation.md)

  - [<span data-ttu-id="e0190-127">在 Lync Server 2013 中自定义 Lync 行为和用户界面</span><span class="sxs-lookup"><span data-stu-id="e0190-127">Customizing Lync behavior and the user interface in Lync Server 2013</span></span>](lync-server-2013-customizing-lync-behavior-and-the-user-interface.md)

  - [<span data-ttu-id="e0190-128">在 Lync Server 2013 中自定义联机会议加载项</span><span class="sxs-lookup"><span data-stu-id="e0190-128">Customizing the Online Meeting Add-in in Lync Server 2013</span></span>](lync-server-2013-customizing-the-online-meeting-add-in.md)

  - [<span data-ttu-id="e0190-129">在 Lync Server 2013 中配置与会页面</span><span class="sxs-lookup"><span data-stu-id="e0190-129">Configuring the meeting join page in Lync Server 2013</span></span>](lync-server-2013-configuring-the-meeting-join-page.md)

  - [<span data-ttu-id="e0190-130">在 Lync Server 2013 中配置支持的客户端版本</span><span class="sxs-lookup"><span data-stu-id="e0190-130">Configuring supported client versions in Lync Server 2013</span></span>](lync-server-2013-configuring-supported-client-versions.md)

  - [<span data-ttu-id="e0190-131">在 Lync Server 2013 中配置增强的联机状态隐私模式</span><span class="sxs-lookup"><span data-stu-id="e0190-131">Configuring enhanced presence privacy mode in Lync Server 2013</span></span>](lync-server-2013-configuring-enhanced-presence-privacy-mode.md)

<span data-ttu-id="e0190-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0190-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

