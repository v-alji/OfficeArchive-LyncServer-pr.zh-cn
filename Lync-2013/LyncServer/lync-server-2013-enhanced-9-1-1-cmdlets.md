---
title: Lync Server 2013：增强的 9-1-1 cmdlet
description: Lync Server 2013：增强的 9-1-1 cmdlet。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enhanced 9-1-1 cmdlets
ms:assetid: e560c688-7b34-4bd7-8104-24f390644105
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415678(v=OCS.15)
ms:contentKeyID: 48185650
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 381489f214e58542b7bd4e13e6e56d2bdef10d12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428641"
---
# <a name="enhanced-9-1-1-cmdlets-in-lync-server-2013"></a>Lync Server 2013 中的增强 9-1-1 cmdlet

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-06-20_

Microsoft Lync Server 2013 附带了一些 cmdlet，使你可以实施和管理增强的 9-1-1 (E9 企业语音解决方案的) 实施。 使用这些 cmdlet 将连接点映射到物理地址，并将企业语音用户所需的设置配置为成功完成紧急呼叫，并自动将位置发送给紧急服务提供商。 不能从 Lync Server 控制面板配置 E9-1-1，必须使用 cmdlet。

<div>

## <a name="enhanced-9-1-1-cmdlets"></a>增强的 9-1-1 Cmdlet

使用以下 cmdlet 配置 E9-1-1。

**增强型 9-1-1**

  - <span></span>  
    [CsEnhancedEmergencyServiceDisclaimer](https://technet.microsoft.com/library/Gg412877(v=OCS.15))

  - <span></span>  
    [Remove-CsEnhancedEmergencyServiceDisclaimer](https://technet.microsoft.com/library/Gg425810(v=OCS.15))

  - <span></span>  
    [Set-CsEnhancedEmergencyServiceDisclaimer](https://technet.microsoft.com/library/Gg398620(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsLisCivicAddress](https://technet.microsoft.com/library/Gg398459(v=OCS.15))

  - <span></span>  
    [Test-CsLisCivicAddress](https://technet.microsoft.com/library/Gg425914(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Export-CsLisConfiguration](https://technet.microsoft.com/library/Gg398539(v=OCS.15))

  - <span></span>  
    [Import-CsLisConfiguration](https://technet.microsoft.com/library/Gg398380(v=OCS.15))

  - <span></span>  
    [Debug-CsLisConfiguration](https://technet.microsoft.com/library/Gg398710(v=OCS.15))

  - <span></span>  
    [Test-CsLisConfiguration](https://technet.microsoft.com/library/Gg398497(v=OCS.15))

  - <span></span>  
    [Publish-CsLisConfiguration](https://technet.microsoft.com/library/Gg398364(v=OCS.15))

  - <span></span>  
    [Unpublish-CsLisConfiguration](unhttps://technet.microsoft.com/library/Gg398364(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsLisLocation](https://technet.microsoft.com/library/Gg412834(v=OCS.15))

  - <span></span>  
    [Remove-CsLisLocation](https://technet.microsoft.com/library/Gg425722(v=OCS.15))

  - <span></span>  
    [Set-CsLisLocation](https://technet.microsoft.com/library/Gg398757(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsLisPort](https://technet.microsoft.com/library/Gg398820(v=OCS.15))

  - <span></span>  
    [Remove-CsLisPort](https://technet.microsoft.com/library/Gg412899(v=OCS.15))

  - <span></span>  
    [Set-CsLisPort](https://technet.microsoft.com/library/Gg398700(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsLisServiceProvider](https://technet.microsoft.com/library/Gg398116(v=OCS.15))

  - <span></span>  
    [Remove-CsLisServiceProvider](https://technet.microsoft.com/library/Gg398904(v=OCS.15))

  - <span></span>  
    [Set-CsLisServiceProvider](https://technet.microsoft.com/library/Gg425911(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsLisSubnet](https://technet.microsoft.com/library/Gg398473(v=OCS.15))

  - <span></span>  
    [Remove-CsLisSubnet](https://technet.microsoft.com/library/Gg413053(v=OCS.15))

  - <span></span>  
    [Set-CsLisSubnet](https://technet.microsoft.com/library/Gg399016(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsLisSwitch](https://technet.microsoft.com/library/Gg425769(v=OCS.15))

  - <span></span>  
    [Remove-CsLisSwitch](https://technet.microsoft.com/library/Gg398352(v=OCS.15))

  - <span></span>  
    [Set-CsLisSwitch](https://technet.microsoft.com/library/Gg412823(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsLisWirelessAccessPoint](https://technet.microsoft.com/library/Gg398117(v=OCS.15))

  - <span></span>  
    [Remove-CsLisWirelessAccessPoint](https://technet.microsoft.com/library/Gg398461(v=OCS.15))

  - <span></span>  
    [Set-CsLisWirelessAccessPoint](https://technet.microsoft.com/library/Gg412723(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsLocationPolicy](https://technet.microsoft.com/library/Gg398911(v=OCS.15))

  - <span></span>  
    [授权-CsLocationPolicy](https://technet.microsoft.com/library/Gg413049(v=OCS.15))

  - <span></span>  
    [新-CsLocationPolicy](https://technet.microsoft.com/library/Gg398231(v=OCS.15))

  - <span></span>  
    [Remove-CsLocationPolicy](https://technet.microsoft.com/library/Gg398727(v=OCS.15))

  - <span></span>  
    [Set-CsLocationPolicy](https://technet.microsoft.com/library/Gg412987(v=OCS.15))

  - <span></span>  
    [Test-CsLocationPolicy](https://technet.microsoft.com/library/Gg425962(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsNetworkSite](https://technet.microsoft.com/library/Gg398766(v=OCS.15))

  - <span></span>  
    [New-CsNetworkSite](https://technet.microsoft.com/library/Gg398365(v=OCS.15))

  - <span></span>  
    [Remove-CsNetworkSite](https://technet.microsoft.com/library/Gg398135(v=OCS.15))

  - <span></span>  
    [Set-CsNetworkSite](https://technet.microsoft.com/library/Gg398295(v=OCS.15))

</div>

<div>

## <a name="see-also"></a>另请参阅


[Lync Server PowerShell 博客](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

