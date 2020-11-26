---
title: Lync Server 2013：测试 PSTN 电话呼叫路由
description: Lync Server 2013：测试 PSTN 电话呼叫路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call routing
ms:assetid: 301dd44d-03e9-41cd-9722-54e00365aa45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727302(v=OCS.15)
ms:contentKeyID: 63969598
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da931b43176932a9b6781fa27318e83e6994548c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440988"
---
# <a name="testing-pstn-phone-call-routing-in-lync-server-2013"></a>在 Lync Server 2013 中测试 PSTN 电话呼叫路由

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-11-01_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>验证计划</p></td>
<td><p>每天</p></td>
</tr>
<tr class="even">
<td><p>测试工具</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>需要权限</p></td>
<td><p>当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</p>
<p>使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 <strong>CsInterTrunkRouting</strong> cmdlet 权限的 RBAC 角色。 若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsInterTrunkRouting&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>说明

**CsInterTrunkRouting** cmdlet 验证呼叫是否可以从一个 SIP 路由到另一个 SIP。 为此，将为 cmdlet 提供一个电话号码和一个中继配置。 然后， **CsInterTrunkRouting** 将为指定的号码报告返回匹配的路由和匹配的 PSTN 用法。 请注意，仅当中继具有匹配指定电话号码的号码模式并且中继至少共享一个 PSTN 用法时，才能在中继之间进行路由。

</div>

<div>

## <a name="running-the-test"></a>运行测试

下面显示的命令返回匹配的路由和匹配的手机用法，使用户能够使用 Redmond 网站的干线配置设置呼叫电话号码1-206-555-1219。

    $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
    
    Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219" -TrunkConfiguration $trunk

</div>

<div>

## <a name="determining-success-or-failure"></a>确定成功还是失败

如果可以将呼叫从一个 SIP 路由到另一个 SIP，您将收到如下输出：

FirstMatchingRoute MatchingUsage MatchingRoutes

\------------------ ------------- --------------

RedmondRoute LocalUsage {RedmondRoute}

如果测试不成功，你将收到类似以下内容的输出：

Test-CsInterTrunkRouting：无法处理参数 Test-CsInterTrunkRouting 上的参数转换

'TrunkConfiguration'. TrunkConfigurationsetting (参数) 无效。 指定一个

有效设置 (参数) 然后再试。

位于第一行：1个字符：79

\+ Test-CsInterTrunkRouting-TargetNumber "电话： + 12065551219"

\-TrunkConfiguration $t .。。

\+

~~

\+ CategoryInfo： InvalidData： (： ) \[ Test-CsInterTrunkRouting \] ，Par

ameterBindingArgumentTransformationException

\+ FullyQualifiedErrorId： ParameterArgumentTransformationError，Microsoft。

tc。TestOcsInterTrunkRoutingCmdlet 的管理

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>测试可能失败的原因

下面是 **测试 CsInterTrunkRouting** 可能失败的一些常见原因：

  - 您指定的参数无效。 主干可能尚未正确配置，并且指定的目标号码可能不正确或无效。

</div>

<div>

## <a name="see-also"></a>另请参阅


[Get-CsTrunk](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunk)  
[New-cstrunkconfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

