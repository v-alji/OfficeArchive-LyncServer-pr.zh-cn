---
title: Lync Server 2013：还原企业版成员服务器
description: Lync Server 2013：还原企业版成员服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring an Enterprise Edition member server
ms:assetid: d960b19c-2104-4719-b736-0d940f254d42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202191(v=OCS.15)
ms:contentKeyID: 51541523
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f9838f030205d92988e185798d982f835122c9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436207"
---
# <a name="restoring-an-enterprise-edition-member-server-in-lync-server-2013"></a><span data-ttu-id="c5de4-103">在 Lync Server 2013 中还原企业版成员服务器</span><span class="sxs-lookup"><span data-stu-id="c5de4-103">Restoring an Enterprise Edition member server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c5de4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c5de4-104">

<span> </span></span></span>

<span data-ttu-id="c5de4-105">_**主题上次修改时间：** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="c5de4-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="c5de4-106">如果运行下列服务器角色之一的服务器失败，请按照本主题中的过程还原服务器。</span><span class="sxs-lookup"><span data-stu-id="c5de4-106">If a server running one of the following server roles fails, follow the procedure in this topic to restore the server.</span></span> <span data-ttu-id="c5de4-107">如果多台服务器独立失败，请按照每台服务器的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="c5de4-107">If multiple servers fail independently, follow the procedure for each server.</span></span>

  - <span data-ttu-id="c5de4-108">前端服务器</span><span class="sxs-lookup"><span data-stu-id="c5de4-108">Front End Server</span></span>

  - <span data-ttu-id="c5de4-109">中介服务器</span><span class="sxs-lookup"><span data-stu-id="c5de4-109">Mediation Server</span></span>

  - <span data-ttu-id="c5de4-110">控制器</span><span class="sxs-lookup"><span data-stu-id="c5de4-110">Director</span></span>

  - <span data-ttu-id="c5de4-111">持久聊天服务器</span><span class="sxs-lookup"><span data-stu-id="c5de4-111">Persistent Chat Server</span></span>

  - <span data-ttu-id="c5de4-112">边缘服务器</span><span class="sxs-lookup"><span data-stu-id="c5de4-112">Edge Server</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="c5de4-113">我们建议你先拍摄系统的映像副本，然后再开始还原。</span><span class="sxs-lookup"><span data-stu-id="c5de4-113">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="c5de4-114">你可以将此映像用作回退点，以防在还原过程中出现问题。</span><span class="sxs-lookup"><span data-stu-id="c5de4-114">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="c5de4-115">您可能希望在安装操作系统和 SQL Server 后获取图像副本，并还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="c5de4-115">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-a-member-server"></a><span data-ttu-id="c5de4-116">还原成员服务器</span><span class="sxs-lookup"><span data-stu-id="c5de4-116">To restore a member server</span></span>

1.  <span data-ttu-id="c5de4-117">从具有相同的完全限定的域名（ (FQDN) 为失败的服务器）开始，安装操作系统，然后还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="c5de4-117">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed server, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5de4-118">按照组织的服务器部署过程执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="c5de4-118">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="c5de4-119">从作为 RTCUniversalServerAdmins 组成员的用户帐户，登录到要还原的服务器。</span><span class="sxs-lookup"><span data-stu-id="c5de4-119">From a user account that is a member of the RTCUniversalServerAdmins group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="c5de4-120">浏览到 Lync Server 安装文件夹或媒体，然后启动位于 \\ 安装 amd64Setup.exe 的 Lync Server 部署向导 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="c5de4-120">Browse to the Lync Server installation folder or media, and start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span>

4.  <span data-ttu-id="c5de4-121">按照部署向导执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="c5de4-121">Follow the Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="c5de4-122">运行 **步骤1：安装本地配置存储** 以安装本地配置文件。</span><span class="sxs-lookup"><span data-stu-id="c5de4-122">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="c5de4-123">运行 **步骤2：设置或删除 Lync Server 组件** 以安装 lync server 服务器角色。</span><span class="sxs-lookup"><span data-stu-id="c5de4-123">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server role.</span></span>
    
    3.  <span data-ttu-id="c5de4-124">运行 **步骤3：请求、安装或分配证书** 以分配证书。</span><span class="sxs-lookup"><span data-stu-id="c5de4-124">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="c5de4-125">运行 **步骤4：启动服务** 以启动服务器上的服务。</span><span class="sxs-lookup"><span data-stu-id="c5de4-125">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="c5de4-126">有关运行部署向导的详细信息，请参阅要还原的服务器角色的部署文档。</span><span class="sxs-lookup"><span data-stu-id="c5de4-126">For details about running the Deployment Wizard, see the Deployment documentation for the server role that you are restoring.</span></span>

<span data-ttu-id="c5de4-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5de4-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

