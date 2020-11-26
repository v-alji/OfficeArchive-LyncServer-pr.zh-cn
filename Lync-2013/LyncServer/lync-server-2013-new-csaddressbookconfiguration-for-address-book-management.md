---
title: Lync Server 2013：用于通讯簿管理的 New-CsAddressBookConfiguration
description: Lync Server 2013：用于通讯簿管理的 New-CsAddressBookConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsAddressBookConfiguration for Address Book management
ms:assetid: a58ddc8c-ae04-4141-b69e-e45374a67d72
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429718(v=OCS.15)
ms:contentKeyID: 48184985
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c85d85fefe701456ad253f1afc69b73093b30996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445447"
---
# <a name="new-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a>Lync Server 2013 中的通讯簿管理 New-CsAddressBookConfiguration

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-11-01_

哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员在本地运行 New-CsAddressBookConfiguration cmdlet： RTCUniversalServerAdmins。 若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsAddressBookConfiguration"}

New-CsAddressBookConfiguration cmdlet 创建新配置以管理通讯簿的行为。 特定于此 cmdlet 的功能是定义通讯簿服务是否创建客户端下载文件，以及如何使用规范化规则，在合并新的完整文件之前保留增量和精简的增量文件的时间、增量文件大小、创建完整的文件通讯簿所需的时间以及内部应用于同步用户数据库中的信息。

例如：

    New-CsAddressBookConfiguration -Identity site:Redmond -KeepDuration 15 -SynchronizePollingInterval 00:10:00

<div>

## <a name="see-also"></a>另请参阅


[新-CsAddressBookConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsAddressBookConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

