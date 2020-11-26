---
title: Lync Server 2013：用于通讯簿管理的 New-CsWebServiceConfiguration
description: Lync Server 2013：用于通讯簿管理的 New-CsWebServiceConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsWebServiceConfiguration for Address Book management
ms:assetid: 49e4ecc5-aa3e-4dd4-a32c-b0dea3758fab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429703(v=OCS.15)
ms:contentKeyID: 48184067
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8972f1b4fe71554e6a8925ddebea6303e2f074a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445433"
---
# <a name="new-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a>Lync Server 2013 中的通讯簿管理 New-CsWebServiceConfiguration

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-11-01_

哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员在本地运行 New-CsWebServiceConfiguration cmdlet： RTCUniversalServerAdmins。 若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsWebServiceConfiguration"}

此 cmdlet New-CsWebServiceConfiguration 为你的组织中的 Web 服务定义新配置。 Web 服务配置的范围只能在网站或服务级别。 它无法在全局级别创建新的 Web 服务配置。 "通讯簿" 的特别兴趣是 "EnableGroupExansion" 属性。 如果设置为 True，则 Web 服务可以响应组展开请求。

例如：

    New-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $False -UseCertificateAuth $True

<div>

## <a name="see-also"></a>另请参阅


[新-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsWebServiceConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

