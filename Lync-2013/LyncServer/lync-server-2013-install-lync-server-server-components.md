---
title: Lync Server 2013：安装 Lync Server 服务器组件
description: Lync Server 2013：安装 Lync Server server 组件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Lync Server server components
ms:assetid: 186aed6e-7adf-4a92-9f2e-f9a4de5ff202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398239(v=OCS.15)
ms:contentKeyID: 48183528
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1930926f3a46be868d838abf646eb8702c9713a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427164"
---
# <a name="install-server-components-for-lync-server-2013"></a><span data-ttu-id="0b425-103">安装适用于 Lync Server 2013 的服务器组件</span><span class="sxs-lookup"><span data-stu-id="0b425-103">Install server components for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b425-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b425-104">

<span> </span></span></span>

<span data-ttu-id="0b425-105">_**主题上次修改时间：** 2014-05-05_</span><span class="sxs-lookup"><span data-stu-id="0b425-105">_**Topic Last Modified:** 2014-05-05_</span></span>

<span data-ttu-id="0b425-106">在执行以下步骤之前，请确保你使用既是本地管理员又是 Active Directory 中 RTCUniversalReadOnlyAdmins 组成员的域用户帐户登录到服务器。</span><span class="sxs-lookup"><span data-stu-id="0b425-106">Before following these steps, make sure you’re logged onto the server with a domain user account that’s both a local administrator and a member of the RTCUniversalReadOnlyAdmins group in Active Directory.</span></span>

<span data-ttu-id="0b425-107">Lync Server 部署向导用于为每个 Lync 服务器角色安装所需的组件和激活服务器。</span><span class="sxs-lookup"><span data-stu-id="0b425-107">The Lync Server Deployment Wizard is used to install the needed components for each Lync server role and to activate the server.</span></span> <span data-ttu-id="0b425-108">本文将引导你完成在 Lync 基础结构中部署标准版服务器或前端服务器的步骤。</span><span class="sxs-lookup"><span data-stu-id="0b425-108">This article walks you through the steps of deploying a Standard Edition server or a Front End Server in your Lync infrastructure.</span></span>

<div>

## <a name="to-install-lync-server-components"></a><span data-ttu-id="0b425-109">安装 Lync Server 组件</span><span class="sxs-lookup"><span data-stu-id="0b425-109">To install Lync Server components</span></span>

1.  <span data-ttu-id="0b425-110">如果 Lync Server 部署向导未在运行，请在要安装 Lync 的服务器上启动它。</span><span class="sxs-lookup"><span data-stu-id="0b425-110">If the Lync Server Deployment Wizard isn’t running, start it on the server you want to install Lync onto.</span></span>

2.  <span data-ttu-id="0b425-111">单击 " **安装或更新 Lync Server 系统**"。</span><span class="sxs-lookup"><span data-stu-id="0b425-111">Click **Install or Update Lync Server System**.</span></span>

3.  <span data-ttu-id="0b425-112">在部署向导中，确认 **步骤1：安装本地配置存储** 带有绿色复选标记，这意味着该服务器已成功安装应用商店的本地副本。</span><span class="sxs-lookup"><span data-stu-id="0b425-112">In the Deployment Wizard, confirm that **Step 1: Install Local Configuration Store** has a green check mark, which means that this server has a local copy of the store installed successfully.</span></span> <span data-ttu-id="0b425-113">如果未选中，则需要在服务器上安装本地配置存储。</span><span class="sxs-lookup"><span data-stu-id="0b425-113">If it’s not checked, you need to install the Local Configuration store on the server.</span></span> <span data-ttu-id="0b425-114">按照在 [Lync Server 2013 中安装本地配置存储中](lync-server-2013-install-the-local-configuration-store.md) 的步骤操作，然后回到此处。</span><span class="sxs-lookup"><span data-stu-id="0b425-114">Follow the steps at [Install the Local Configuration store in Lync Server 2013](lync-server-2013-install-the-local-configuration-store.md) and then come back here.</span></span>

4.  <span data-ttu-id="0b425-115">准备好在服务器上安装 Lync Server 2013 组件时，请单击 **步骤2：设置或删除 Lync Server 组件** 旁边的 "**运行**"。</span><span class="sxs-lookup"><span data-stu-id="0b425-115">When you’re ready to install the Lync Server 2013 components on your server, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

5.  <span data-ttu-id="0b425-116">在 " **设置 Lync Server 组件** " 页面上，单击 " **下一步** " 以设置在已发布拓扑中定义的组件。</span><span class="sxs-lookup"><span data-stu-id="0b425-116">On the **Set Up Lync Server Components** page, click **Next** to set up components as defined in your published topology.</span></span>

6.  <span data-ttu-id="0b425-117">" **执行命令** " 页面将在设置发生时显示命令和安装信息的摘要。</span><span class="sxs-lookup"><span data-stu-id="0b425-117">The **Executing Commands** page will display a summary of commands and installation information as the set up takes place.</span></span> <span data-ttu-id="0b425-118">完成后，可以使用列表选择要查看的日志，然后单击“**查看日志**”。</span><span class="sxs-lookup"><span data-stu-id="0b425-118">When it’s done, you can use the list to select a log to view, and then click **View Log**.</span></span>

7.  <span data-ttu-id="0b425-119">在 Lync Server 2013 组件设置完成后，如果需要，您已查看日志，请单击 " **完成** " 以在安装中完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="0b425-119">When Lync Server 2013 components setup is done, and you’ve reviewed the logs as needed, click **Finish** to complete this step in the installation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0b425-120">如果系统提示您重新启动服务器 (如果需要安装 Windows 桌面体验) ，则可能会发生此情况。</span><span class="sxs-lookup"><span data-stu-id="0b425-120">If you’re prompted to restart the server (which might happen if Windows Desktop Experience needed to be installed), definitely do that.</span></span> <span data-ttu-id="0b425-121">当计算机恢复正常运行时，你需要再次执行这些步骤，从上面列出的第三个步骤开始 (在 "部署向导" 中再次运行步骤 2) 。</span><span class="sxs-lookup"><span data-stu-id="0b425-121">When the computer is back up and running, you need to do these steps over again, starting from step three listed above (basically run Step 2 in the Deployment Wizard one more time).</span></span>

    
    <span data-ttu-id="0b425-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b425-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

