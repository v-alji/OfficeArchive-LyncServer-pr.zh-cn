---
title: 测试并报告 Kerberos 身份验证的功能准备工作
description: 测试和报告 Kerberos 身份验证的功能准备情况。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test and report functional readiness for Kerberos authentication
ms:assetid: d52c39e5-747d-4f29-88aa-30fd6f26b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398925(v=OCS.15)
ms:contentKeyID: 48185519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d32591a8cced7dce2e0bb78cc26189dce1900a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444299"
---
# <a name="test-and-report-functional-readiness-for-kerberos-authentication-in-lync-server-2013"></a>在 Lync Server 2013 中测试并报告 Kerberos 身份验证的功能准备工作

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-01-16_

若要成功完成此过程，你应以 RTCUniversalServerAdmins 组成员的用户身份登录。

你可以使用 **CsKerberosAccountAssignment** Windows PowerShell cmdlet 测试和报告用于 Kerberos 身份验证的网站分配的功能准备情况。 此命令将查询在必需的 Identity 参数中指定的网站。 可选报表参数使 cmdlet 在运行该命令的计算机上将 HTML 报表写入 C： \\ 日志。 可选的详细参数将活动信息报告到屏幕。

<div>

## <a name="to-test-and-report-functional-readiness-for-kerberos-authentication-for-a-site"></a>测试和报告适用于网站的 Kerberos 身份验证的功能准备情况

1.  作为 RTCUniversalServerAdmins 组的成员，登录到运行 Lync Server 2013 的域或安装了管理工具的计算机上的计算机。

2.  启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。

3.  从命令行运行以下命令：
    
        Test-CsKerberosAccountAssignment -Identity "site:SiteName" -Report "c:\logs\FileName.htm" -Verbose
    
    例如：
    
        Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "c:\logs\KerberosReport.htm" -Verbose

</div>

</div>

<span> </span>

</div>

</div>

</div>

