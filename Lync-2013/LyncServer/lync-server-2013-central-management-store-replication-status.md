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
# <a name="central-management-store-replication-status-in-lync-server-2013"></a>Lync Server 2013 中的中央管理存储复制状态

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2015-01-26_

当管理员对 Lync Server (进行更改时，例如，当管理员创建新的语音策略或更改通讯簿服务器配置设置时) 该更改将记录在中央管理存储中。 然后，必须将更改复制到运行 Lync Server 服务或服务器角色的所有计算机。

要复制数据，主复制程序（在中央管理服务器上运行）会为所更改的配置数据创建一个快照。 然后，将该快照的副本发送到运行 Lync Server 服务或服务器角色的每台计算机。 在这些计算机上，复制代理将接收快照并上载所更改的数据。 然后，代理会向主复制程序发送一条消息，报告最新的复制状态。

Get-CsManagementStoreReplicationStatus cmdlet 使你可以验证你的组织中的所有 (或 Lync Server 计算机的所有) 的复制状态。

谁可以运行此 cmdlet？ 默认情况下，以下各组的成员有权在本地运行 Get-CsManagementStoreReplicationStatus cmdlet：RTCUniversalUserAdmins、RTCUniversalServerAdmins。

若要返回此 cmdlet 分配给 (的所有 RBAC 角色的列表，包括您自行创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsManagementStoreReplicationStatus"}

<div>

## <a name="see-also"></a>另请参阅


[CsManagementStoreReplicationStatus](https://docs.microsoft.com/powershell/module/skype/Get-CsManagementStoreReplicationStatus)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

