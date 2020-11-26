---
title: 将 Lync Server 2010 会议目录移动到 Lync Server 2013
description: 将 Lync Server 2010 会议目录移动到 Lync Server 2013。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move Conference Directories
ms:assetid: 659867e0-ce91-4a95-9787-b1c1566460a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727126(v=OCS.15)
ms:contentKeyID: 62387565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12ac58ac0ab6f1908e7eac3e5824bf2304256632
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440344"
---
# <a name="move-conference-directories"></a>移动会议目录

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-05-28_

在取消池之前，必须针对 Lync Server 2010 池中的每个会议目录执行以下过程。

<div>

## <a name="to-move-a-conference-directory-to-lync-server-2013"></a>将会议目录移动到 Lync Server 2013

1.  打开 Lync Server 命令行管理程序。

2.  若要获取组织中的会议目录的标识，请运行以下命令：
    
        Get-CsConferenceDirectory
    
    上面的命令返回你的组织中的所有会议目录。 因此，你可能希望将结果限制为即将停止的池。 例如，如果你使用完全限定的域名解除池 (FQDN) pool01.contoso.net，请使用此命令将返回的数据限制为来自该池中的会议目录：
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"}
    
    该命令仅返回 ServiceID 属性包含 FQDN pool01.contoso.net 的会议目录。

3.  若要移动会议目录，请对池中的每个会议目录运行以下命令：
    
        Move-CsConferenceDirectory -Identity <Numeric identity of conference directory> -TargetPool <FQDN of pool where ownership is to be transitioned>
    
    例如，若要移动会议目录3，请使用此命令，将 Lync Server 2013 池指定为 TargetPool：
    
        Move-CsConferenceDirectory -Identity 3 -TargetPool "pool02.contoso.net"
    
    如果要移动池中的所有会议目录，请使用类似于以下内容的命令：
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"} | Move-CsConferenceDirectory -TargetPool "pool02.contoso.net"

请参阅文档 "卸载 Microsoft Lync Server 2010 和删除服务器角色" (可从) 下载该文档， [https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227) 以获取有关取消 Lync 2010 池的全面的分步说明。

移动会议目录时，可能会遇到以下错误：

    WARNING: Move operation failed for conference directory with ID "5". Cannot perform a rollback because data migration might have already started. Retry the operation.
    WARNING: Before using the -Force parameter, ensure that you have exported the conference directory data using DBImpExp.exe and imported the data on the target pool. Refer to the DBImpExp-Readme.htm file for more information.
    Move-CsConferenceDirectory : Unable to cast COM object of type 'System._ComObject' to interface type 'Microsoft.Rtc.Interop.User.IRtcConfDirManagement'. 
    This operation failed because the QueryInterface call on the COM component for the interface with SID '{4262B886-503F-4BEA-868C-04E8DF562CEB}' failed due to the following error: The specified module could not be found.

此错误通常在 Lync Server Management Shell 需要更新的 Active Directory 权限集以便完成任务时出现。 若要解决此问题，请关闭该命令行管理程序的当前实例，然后打开一个新的 Shell 实例并重新运行该命令，以便移动会议目录。

</div>

</div>

<span> </span>

</div>

</div>

</div>

