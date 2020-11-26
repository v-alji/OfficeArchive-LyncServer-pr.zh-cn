---
title: Lync Server 2013：用于通讯簿管理的 Get-CsAddressBookConfiguration
description: Lync Server 2013：用于通讯簿管理的 Get-CsAddressBookConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsAddressBookConfiguration for Address Book management
ms:assetid: bd62f916-caf3-4e10-ada4-631bbb331ef1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429721(v=OCS.15)
ms:contentKeyID: 48185264
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91b96aead7b7038464f3166691a5952b9ff850dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427976"
---
# <a name="get-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a>Lync Server 2013 中的通讯簿管理 Get-CsAddressBookConfiguration

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-11-01_

哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员在本地运行 Get-CsAddressBookConfiguration cmdlet： RTCUniversalServerAdmins。 若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsAddressBookConfiguration"}

Cmdlet Get-CsAddressBookConfiguration 返回有关已存在的配置的信息。

例如：

    Get-CsAddressBookConfiguration -Identity site:Redmond

将 Get-CsAddressBookConfiguration 和 Set-CsAddressBookConfiguration 的功能结合起来，管理员可以定义要修改的配置，然后应用修改。 例如，下面的组合：

    Get-CsAddressBookConfiguration -Filter site:* | Set-CsAddressBookConfiguration -RunTimeOfDay 23:00

返回所有网站中的所有配置，并对配置应用23:00 小时的 RunTimeOfDay。

<div>

## <a name="see-also"></a>另请参阅


[CsAddressBookConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAddressBookConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

