---
title: Lync Server 2013：删除未与设备关联的设备更新文件
description: Lync Server 2013：删除未与设备关联的设备更新文件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove Device Update files not associated with a device
ms:assetid: ecebbf73-b456-4990-a91d-308b84d39404
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994084(v=OCS.15)
ms:contentKeyID: 51803996
ms.date: 12/12/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8338f7274d1d27e2290d822324986238f4856fe4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436403"
---
# <a name="remove-device-update-files-not-associated-with-a-device-in-lync-server-2013"></a>删除未与 Lync Server 2013 中的设备关联的设备更新文件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-20_

每次将新设备更新上载到系统时，都会创建相应的设备更新规则。 默认情况下，这些新的设备更新规则将分配给挂起状态。 这意味着可以在测试设备上下载和安装这些规则，但不能在生产设备上下载这些规则，这使你能够在将更新提供给用户之前对其进行测试。 根据测试，你可以接受并部署或拒绝并删除更新。 当您拒绝更新时，设备更新将与它的设备更新规则解除关联。

<div>


可使用 Windows PowerShell 和 **CsDeviceUpdateFile** cmdlet 删除不再与设备关联的设备更新文件。 此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。

<div>


> [!NOTE]  
> 有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> 。



</div>

<div>


  - 例如，以下命令将删除 Web 服务器 atl-cs-001.litwareinc.com 上不再与设备关联的任何设备更新规则：
    
        Clear-CsDeviceUpdateFile -Identity "service:WebServer:atl-cs-001.litwareinc.com"

</div>

有关详细信息，请参阅 [CsDeviceUpdateFile](https://docs.microsoft.com/powershell/module/skype/Clear-CsDeviceUpdateFile) Cmdlet 的帮助主题。

</div>

</div>

<span> </span>

</div>

</div>

</div>

