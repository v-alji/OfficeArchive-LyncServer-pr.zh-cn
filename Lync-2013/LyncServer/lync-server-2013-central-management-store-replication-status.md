---
title: Lync Server 2013：中央管理存储复制状态
description: Lync Server 2013：中央管理存储复制状态。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central management store replication status
ms:assetid: f514f88d-986b-4e45-b79b-e04a7616c1fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720926(v=OCS.15)
ms:contentKeyID: 63969663
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f1f9008a966040cf34ac0499c023f9dbe53a541
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435458"
---
# <a name="central-management-store-replication-status-in-lync-server-2013"></a><span data-ttu-id="ad924-103">Lync Server 2013 中的中央管理存储复制状态</span><span class="sxs-lookup"><span data-stu-id="ad924-103">Central management store replication status in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad924-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad924-104">

<span> </span></span></span>

<span data-ttu-id="ad924-105">_**主题上次修改时间：** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="ad924-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="ad924-106">当管理员对 Lync Server (进行更改时，例如，当管理员创建新的语音策略或更改通讯簿服务器配置设置时) 该更改将记录在中央管理存储中。</span><span class="sxs-lookup"><span data-stu-id="ad924-106">When an administrator makes a change of some kind to Lync Server (for example, when an administrator creates a new voice policy or changes the Address Book Server configuration settings) that change is recorded in the Central Management store.</span></span> <span data-ttu-id="ad924-107">然后，必须将更改复制到运行 Lync Server 服务或服务器角色的所有计算机。</span><span class="sxs-lookup"><span data-stu-id="ad924-107">In turn, the change must then be replicated to all the computers that are running Lync Server services or server roles.</span></span>

<span data-ttu-id="ad924-108">要复制数据，主复制程序（在中央管理服务器上运行）会为所更改的配置数据创建一个快照。</span><span class="sxs-lookup"><span data-stu-id="ad924-108">To replicate data, the Master Replicator (running on the Central Management Server) creates a snapshot of the changed configuration data.</span></span> <span data-ttu-id="ad924-109">然后，将该快照的副本发送到运行 Lync Server 服务或服务器角色的每台计算机。</span><span class="sxs-lookup"><span data-stu-id="ad924-109">A copy of this snapshot is then sent to each computer that is running Lync Server services or server roles.</span></span> <span data-ttu-id="ad924-110">在这些计算机上，复制代理将接收快照并上载所更改的数据。</span><span class="sxs-lookup"><span data-stu-id="ad924-110">On those computers, a replication agent receives the snapshot and uploads the changed data.</span></span> <span data-ttu-id="ad924-111">然后，代理会向主复制程序发送一条消息，报告最新的复制状态。</span><span class="sxs-lookup"><span data-stu-id="ad924-111">The agent then sends the Master Replicator a message reporting the latest replication status.</span></span>

<span data-ttu-id="ad924-112">Get-CsManagementStoreReplicationStatus cmdlet 使你可以验证你的组织中的所有 (或 Lync Server 计算机的所有) 的复制状态。</span><span class="sxs-lookup"><span data-stu-id="ad924-112">The Get-CsManagementStoreReplicationStatus cmdlet enables you to verify the replication status for any (or all) of the Lync Server computers in your organization.</span></span>

<span data-ttu-id="ad924-113">谁可以运行此 cmdlet？</span><span class="sxs-lookup"><span data-stu-id="ad924-113">Who can run this cmdlet?</span></span> <span data-ttu-id="ad924-114">默认情况下，以下各组的成员有权在本地运行 Get-CsManagementStoreReplicationStatus cmdlet：RTCUniversalUserAdmins、RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="ad924-114">By default, members of the following groups are authorized to run the Get-CsManagementStoreReplicationStatus cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span>

<span data-ttu-id="ad924-115">若要返回此 cmdlet 分配给 (的所有 RBAC 角色的列表，包括您自行创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="ad924-115">To return a list of all RBAC roles this cmdlet was assigned to (including any custom RBAC roles that you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsManagementStoreReplicationStatus"}

<div>

## <a name="see-also"></a><span data-ttu-id="ad924-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ad924-116">See Also</span></span>


[<span data-ttu-id="ad924-117">CsManagementStoreReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="ad924-117">Get-CsManagementStoreReplicationStatus</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsManagementStoreReplicationStatus)  
  

<span data-ttu-id="ad924-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad924-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

