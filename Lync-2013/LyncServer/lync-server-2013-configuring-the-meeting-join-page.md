---
title: Lync Server 2013：配置与会页面
description: Lync Server 2013：配置会议加入页面。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the meeting join page
ms:assetid: 45880423-47f4-49af-b825-cbd8e3fc1046
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204861(v=OCS.15)
ms:contentKeyID: 48184037
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e7c9dde0fdb6829da7bd11e16261a4bd76b7554
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432532"
---
# <a name="configuring-the-meeting-join-page-in-lync-server-2013"></a>在 Lync Server 2013 中配置与会页面

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-12-14_

当用户单击会议请求中的会议链接时，会议加入页面检测是否已在用户的计算机上安装了 Lync 2013 客户端。 如果已安装客户端，客户端将打开并加入会议。 如果未安装客户端，则默认情况下将打开2013版本的 Lync Web App。

如果您希望允许用户通过 Office Communicator 2007 R2 或 Lync 2010 助理加入会议，则可以修改会议加入页面的行为。 这些配置选项已从 Lync Server 2013 控制面板中删除，但你可以使用 Set-CsWebServiceConfiguration cmdlet 对其进行配置。

### <a name="meeting-join-page-set-cswebserviceconfiguration-parameters"></a>会议联接页 Set-CsWebServiceConfiguration 参数

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Set-CsWebServiceConfiguration 参数</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ShowJoinUsingLegacyClientLink</p></td>
<td><p>如果设置为 True，则通过使用 Lync 之外的客户端应用程序加入会议的用户将有机会通过使用 Office Communicator 2007 R2 加入会议。 默认值为 False。</p></td>
</tr>
<tr class="even">
<td><p>ShowAlternateJoinOptionsExpanded</p></td>
<td><p>如果设置为 True，则用于加入联机会议 (（如 Office Communicator 2007 R2) ）的替代选项将自动展开并向用户显示。 在设置为 False 时 (默认值) 这些选项将可用，但用户将必须显示其自身的选项列表。</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-the-meeting-join-page-by-using-lync-server-2013-management-shell"></a>使用 Lync Server 2013 命令行管理程序配置会议加入页面

1.  启动 Lync Server 2013 命令行管理程序：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server Management Shell**"。

2.  若要查看 web 服务配置设置，请运行以下 cmdlet：
    
        Get-CsWebServiceConfiguration

3.  运行以下命令，将参数设置为 True 或 False，具体取决于你的首选项 (有关此 cmdlet 的参数的详细信息，请参阅 Lync Server 2013 管理外壳文档) 中的 [CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration) ：
    
        Set-CsWebServiceConfiguration -Identity global -ShowJoinUsingLegacyClientLink $True

</div>

<div>

## <a name="see-also"></a>另请参阅


[Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

