---
title: Lync Server 2013：验证地址
description: Lync Server 2013：验证地址。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validate addresses
ms:assetid: aae557c9-e6f5-4d23-8af1-1d4cd7968c54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412808(v=OCS.15)
ms:contentKeyID: 48185108
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcbb8789912b3bcbcfb60dd79807f06c2957c1f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446316"
---
# <a name="validate-addresses-in-lync-server-2013"></a>在 Lync Server 2013 中验证地址

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-17_

在发布位置数据库之前，必须根据您的 SIP 主干或公共交换电话网络 (PSTN) E9 服务提供商维护的主要街道地址指南 () MSAG "验证新位置。

有关 SIP 中继 E9 服务提供商的详细信息，请参阅 [为 Lync Server 2013 选择 E9 服务提供商](lync-server-2013-choosing-an-e9-1-1-service-provider.md)。

有关验证地址的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：

  - **CsLisServiceProvider**

  - **Set-CsLisServiceProvider**

  - **Remove-CsLisServiceProvider**

  - **CsLisCivicAddress**

  - **Test-CsLisCivicAddress**

<div>

## <a name="to-validate-addresses-located-in-the-location-database"></a>验证位于位置数据库中的地址

1.  启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。

2.  运行以下 cmdlet 配置紧急服务提供商连接。
    
        $pwd = Read-Host -AsSecureString <password>
        Set-CsLisServiceProvider -ServiceProviderName Provider1 -ValidationServiceUrl <URL provided by provider> -CertFileName <location of certificate provided by provider> -Password $pwd

3.  运行以下 cmdlet 验证位置数据库中的地址。
    
        Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus
    
    还可以使用 **Test-CsLisCivicAddress** cmdlet 验证单个地址。

</div>

</div>

<span> </span>

</div>

</div>

</div>

