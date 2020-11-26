---
title: 删除前端池或 Standard Edition Server
description: 删除前端池或标准版服务器。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove Front End pool or Standard Edition server
ms:assetid: 83c39a36-49a1-4ac6-9cc5-b0e441b1fdec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688115(v=OCS.15)
ms:contentKeyID: 49733713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c878d56b073558f4f4b50f31b6742fd581c80241
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440274"
---
# <a name="remove-front-end-pool-or-standard-edition-server"></a><span data-ttu-id="452f7-103">删除前端池或 Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="452f7-103">Remove Front End pool or Standard Edition server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="452f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="452f7-104">

<span> </span></span></span>

<span data-ttu-id="452f7-105">_**主题上次修改时间：** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="452f7-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="452f7-106">本主题将指导你完成删除前端池或标准版前端服务器的过程。</span><span class="sxs-lookup"><span data-stu-id="452f7-106">This topic guides you through the process of removing a Front End pool or a Standard Edition Front End Server.</span></span> <span data-ttu-id="452f7-107">删除前端池时，将在池删除过程中删除属于该池的每个前端服务器。</span><span class="sxs-lookup"><span data-stu-id="452f7-107">When you remove a Front End pool, you remove each Front End Server that belongs to the pool as a part of the pool removal process.</span></span> <span data-ttu-id="452f7-108">删除标准版前端服务器时，必须从拓扑生成器中删除 SQL 应用商店定义。</span><span class="sxs-lookup"><span data-stu-id="452f7-108">When you remove a Standard Edition Front End Server, you must remove the SQL Store definition from Topology Builder.</span></span>

<div>

## <a name="to-remove-a-front-end-server-pool"></a><span data-ttu-id="452f7-109">删除前端服务器池</span><span class="sxs-lookup"><span data-stu-id="452f7-109">To remove a Front End Server pool</span></span>

1.  <span data-ttu-id="452f7-110">打开拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="452f7-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="452f7-111">导航到 Lync Server 2010 节点。</span><span class="sxs-lookup"><span data-stu-id="452f7-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="452f7-112">展开 " **企业版前端池**"，展开 "前端池"，右键单击要删除的前端池，然后单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="452f7-112">Expand **Enterprise Edition Front End pools**, expand the Front End pool, right-click the Front End pool that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="452f7-113">发布拓扑，检查复制状态，然后根据需要运行 Lync Server 部署向导。</span><span class="sxs-lookup"><span data-stu-id="452f7-113">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

</div>

<div>

## <a name="to-remove-a-standard-edition-front-end-server"></a><span data-ttu-id="452f7-114">删除标准版前端服务器</span><span class="sxs-lookup"><span data-stu-id="452f7-114">To remove a Standard Edition Front End server</span></span>

1.  <span data-ttu-id="452f7-115">打开拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="452f7-115">Open Topology Builder.</span></span>

2.  <span data-ttu-id="452f7-116">导航到 Lync Server 2010 节点。</span><span class="sxs-lookup"><span data-stu-id="452f7-116">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="452f7-117">展开 **标准版前端服务器**，右键单击要删除的前端服务器，然后单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="452f7-117">Expand **Standard Edition Front End servers**, right-click the Front End Server that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="452f7-118">展开 " **sql 存储**"，右键单击与标准版前端服务器关联的 SQL Server 数据库，然后单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="452f7-118">Expand **SQL stores**, right-click the SQL Server database that is associated with the Standard Edition Front End Server, and then click **Delete**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="452f7-119">必须从标准版前端服务器中删除 collocated SQL Server 数据库的定义。</span><span class="sxs-lookup"><span data-stu-id="452f7-119">You must remove the definition of the collocated SQL Server databases from the Standard Edition Front End Server.</span></span>

    
    </div>

5.  <span data-ttu-id="452f7-120">发布拓扑，检查复制状态，然后根据需要运行 Lync Server 部署向导。</span><span class="sxs-lookup"><span data-stu-id="452f7-120">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="452f7-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="452f7-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

