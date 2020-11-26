---
title: Lync Server 2013：还原文件存储
description: Lync Server 2013：还原文件存储。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a file store
ms:assetid: 89916fc6-31d3-4c7f-9eaf-c02584761ef4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202180(v=OCS.15)
ms:contentKeyID: 51541491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201c4b20f224fa3a25e931689e564410c60143e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436249"
---
# <a name="restoring-a-file-store-in-lync-server-2013"></a><span data-ttu-id="41d28-103">在 Lync Server 2013 中还原文件存储</span><span class="sxs-lookup"><span data-stu-id="41d28-103">Restoring a file store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41d28-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41d28-104">

<span> </span></span></span>

<span data-ttu-id="41d28-105">_**主题上次修改时间：** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="41d28-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="41d28-106">标准版的文件存储通常位于标准版服务器上。</span><span class="sxs-lookup"><span data-stu-id="41d28-106">File Stores for Standard Edition are typically located on the Standard Edition server.</span></span> <span data-ttu-id="41d28-107">企业版的文件存储通常位于文件服务器或群集上。</span><span class="sxs-lookup"><span data-stu-id="41d28-107">File Stores for Enterprise Edition are typically located on a file server or cluster.</span></span> <span data-ttu-id="41d28-108">以下过程介绍了如何还原文件存储。</span><span class="sxs-lookup"><span data-stu-id="41d28-108">The following procedure describes how to restore a File Store.</span></span>

<div>

## <a name="to-restore-a-file-store"></a><span data-ttu-id="41d28-109">还原文件存储</span><span class="sxs-lookup"><span data-stu-id="41d28-109">To restore a File Store</span></span>

1.  <span data-ttu-id="41d28-110">如果文件存储失败，请将相应的文件存储区从 $Backup 复制 \\ 到文件服务器或标准版服务器上的文件存储位置，然后共享该文件夹。</span><span class="sxs-lookup"><span data-stu-id="41d28-110">If a File Store fails, copy the appropriate File Store from $Backup\\ to the File Store location on the file server or Standard Edition server, and then share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="41d28-111">已还原文件存储的路径和文件名应与备份的文件存储完全相同，以便使用这些文件的组件可以访问它们。</span><span class="sxs-lookup"><span data-stu-id="41d28-111">The path and file name for the restored File Store should be exactly the same as the backed up File Store, so that components that use the files can access them.</span></span>

    
    </div>

2.  <span data-ttu-id="41d28-112">如有必要，请设置文件存储 (Acl) 的访问控制列表。</span><span class="sxs-lookup"><span data-stu-id="41d28-112">If necessary, set the access control lists (ACLs) for the File Store.</span></span> <span data-ttu-id="41d28-113">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="41d28-113">At the command line, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="41d28-114">只有在还原过程中没有其他方法运行拓扑生成器时，才需要执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="41d28-114">You need to perform this step only if you have not otherwise run Topology Builder during your restoration process.</span></span>

    
    <span data-ttu-id="41d28-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41d28-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

