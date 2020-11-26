---
title: Lync Server 2013：服务器角色和服务 cmdlet
description: Lync Server 2013：服务器角色和服务 cmdlet。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server roles and services cmdlets
ms:assetid: ff3561de-043e-4071-88f7-8de3cded52f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415683(v=OCS.15)
ms:contentKeyID: 48185971
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e88d41653c6ec429809c56a3de0a35ef08450a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444880"
---
# <a name="server-roles-and-services-cmdlets-in-lync-server-2013"></a>Lync Server 2013 中的服务器角色和服务 cmdlet

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-07-29_

许多 Microsoft Lync Server 2013 组件作为服务器角色或服务运行。 Lync Server 2013 附带了许多 cmdlet，可让你管理这些服务器角色和服务。

<div>

## <a name="server-roles-and-services-cmdlets"></a>服务器角色和服务 Cmdlet

许多 (，但并非所有适用于服务器和服务角色的管理任务) 都可以从 Lync Server 控制面板执行。 例如，您可以使用 Lync Server "控制面板" 管理存档服务器设置，但不能管理通讯簿服务器设置。 但是，所有这些任务都可以使用 Lync Server 命令行管理程序或脚本中的 cmdlet 执行;使用脚本可以自动执行某些任务。 以下是与管理服务器角色和服务直接相关的 cmdlet 的列表：

**[Lync Server 2013 中的通讯簿服务器 cmdlet](lync-server-2013-address-book-server-cmdlets.md)**

  - <span></span>  
    [CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))

  - <span></span>  
    [新-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))

  - <span></span>  
    [Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))

  - <span></span>  
    [Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))

**[Lync Server 2013 中的存档和监视 cmdlet](lync-server-2013-archiving-and-monitoring-cmdlets.md)**

  - <span></span>  
    [CsArchivingConfiguration](https://technet.microsoft.com/library/Gg399012(v=OCS.15))

  - <span></span>  
    [新-CsArchivingConfiguration](https://technet.microsoft.com/library/Gg398471(v=OCS.15))

  - <span></span>  
    [Remove-CsArchivingConfiguration](https://technet.microsoft.com/library/Gg398951(v=OCS.15))

  - <span></span>  
    [Set-CsArchivingConfiguration](https://technet.microsoft.com/library/Gg413030(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Export-CsArchivingData](https://technet.microsoft.com/library/Gg398452(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Invoke-CsArchivingDatabasePurge](https://technet.microsoft.com/library/JJ204627(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsArchivingPolicy](https://technet.microsoft.com/library/Gg425731(v=OCS.15))

  - <span></span>  
    [授权-CsArchivingPolicy](https://technet.microsoft.com/library/Gg398475(v=OCS.15))

  - <span></span>  
    [新-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15))

  - <span></span>  
    [Remove-CsArchivingPolicy](https://technet.microsoft.com/library/Gg425924(v=OCS.15))

  - <span></span>  
    [Set-CsArchivingPolicy](https://technet.microsoft.com/library/Gg398294(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Set-CsArchivingServer](https://technet.microsoft.com/library/Gg398923(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsCdrConfiguration](https://technet.microsoft.com/library/Gg398298(v=OCS.15))

  - <span></span>  
    [新-CsCdrConfiguration](https://technet.microsoft.com/library/Gg399018(v=OCS.15))

  - <span></span>  
    [Remove-CsCdrConfiguration](https://technet.microsoft.com/library/Gg398451(v=OCS.15))

  - <span></span>  
    [Set-CsCdrConfiguration](https://technet.microsoft.com/library/Gg398774(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Set-CsMonitoringServer](https://technet.microsoft.com/library/Gg425776(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsQoEConfiguration](https://technet.microsoft.com/library/Gg399004(v=OCS.15))

  - <span></span>  
    [新-CsQoEConfiguration](https://technet.microsoft.com/library/Gg398325(v=OCS.15))

  - <span></span>  
    [Remove-CsQoEConfiguration](https://technet.microsoft.com/library/Gg425879(v=OCS.15))

  - <span></span>  
    [Set-CsQoEConfiguration](https://technet.microsoft.com/library/Gg398245(v=OCS.15))

[Invoke-CsCdrDatabasePurge](https://technet.microsoft.com/library/JJ205113(v=OCS.15))

  - <span></span>  
    [Export-CsArchivingData](https://technet.microsoft.com/library/Gg398452(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Invoke-CsQoEDatabasePurge](https://technet.microsoft.com/library/JJ205247(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsReportingConfiguration](https://technet.microsoft.com/library/JJ205356(v=OCS.15))

  - <span></span>  
    [New-CsReportingConfiguration](https://technet.microsoft.com/library/JJ204787(v=OCS.15))

  - <span></span>  
    [Remove-CsReportingConfiguration](https://technet.microsoft.com/library/JJ204711(v=OCS.15))

  - <span></span>  
    [Set-CsReportingConfiguration](https://technet.microsoft.com/library/JJ205075(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsTestUserCredential](https://technet.microsoft.com/library/JJ204759(v=OCS.15))

  - <span></span>  
    [Remove-CsTestUserCredential](https://technet.microsoft.com/library/JJ204870(v=OCS.15))

  - <span></span>  
    [Set-CsTestUserCredential](https://technet.microsoft.com/library/JJ205341(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsWatcherNodeConfiguration](https://technet.microsoft.com/library/JJ204739(v=OCS.15))

  - <span></span>  
    [New-CsWatcherNodeConfiguration](https://technet.microsoft.com/library/JJ205254(v=OCS.15))

  - <span></span>  
    [Remove-CsWatcherNodeConfiguration](https://technet.microsoft.com/library/JJ204926(v=OCS.15))

  - <span></span>  
    [Set-CsWatcherNodeConfiguration](https://technet.microsoft.com/library/JJ204620(v=OCS.15))

  - <span></span>  
    [Test-CsWatcherNodeConfiguration](https://technet.microsoft.com/library/JJ204652(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [New-CsExtendedTest](https://technet.microsoft.com/library/JJ205275(v=OCS.15))

**[Lync Server 2013 中的数据库和管理服务器 cmdlet](lync-server-2013-database-and-management-server-cmdlets.md)**

  - <span></span>  
    [Get-CsConfigurationStoreLocation](https://technet.microsoft.com/library/Gg412814(v=OCS.15))

  - <span></span>  
    [Remove-CsConfigurationStoreLocation](https://technet.microsoft.com/library/Gg398214(v=OCS.15))

  - <span></span>  
    [Set-CsConfigurationStoreLocation](https://technet.microsoft.com/library/Gg398258(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [安装-CsDatabase](https://technet.microsoft.com/library/Gg399044(v=OCS.15))

  - <span></span>  
    [Test-CsDatabase](https://technet.microsoft.com/library/JJ204839(v=OCS.15))

  - <span></span>  
    [Uninstall-CsDatabase](unhttps://technet.microsoft.com/library/Gg399044(v=OCS.15))

<!-- end list -->

  - [Invoke-CsDatabaseFailover](https://technet.microsoft.com/library/JJ204744(v=OCS.15))

<!-- end list -->

  - [Get-CsDatabaseMirrorState](https://technet.microsoft.com/library/JJ204845(v=OCS.15))

<!-- end list -->

  - [Install-CsMirrorDatabase](https://technet.microsoft.com/library/JJ204986(v=OCS.15))

  - [Uninstall-CsMirrorDatabase](unhttps://technet.microsoft.com/library/JJ204986(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsUserDatabaseState](https://technet.microsoft.com/library/Gg398831(v=OCS.15))

  - <span></span>  
    [Set-CsUserDatabaseState](https://technet.microsoft.com/library/Gg412973(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Update-CsUserDatabase](https://technet.microsoft.com/library/Gg398682(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Move-CsManagementServer](https://technet.microsoft.com/library/Gg412921(v=OCS.15))

  - <span></span>  
    [Set-CsManagementServer](https://technet.microsoft.com/library/Gg398465(v=OCS.15))

<!-- end list -->

  - [Invoke-CsManagementServerFailover](https://technet.microsoft.com/library/JJ204647(v=OCS.15))

**[Lync Server 2013 中的 Edge 服务器 cmdlet](lync-server-2013-edge-server-cmdlets.md)**

  - <span></span>  
    [CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))

  - <span></span>  
    [Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))

  - <span></span>  
    [新-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))

  - <span></span>  
    [Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))

  - <span></span>  
    [Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))

**[Lync Server 2013 中的其他服务器角色 cmdlet](lync-server-2013-other-server-role-cmdlets.md)**

  - <span></span>  
    [Set-CsConferenceServer](https://technet.microsoft.com/library/Gg398738(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Set-CsUserServer](https://technet.microsoft.com/library/Gg413026(v=OCS.15))

**[Lync Server 2013 中的注册机构和主管 cmdlet](lync-server-2013-registrar-and-director-cmdlets.md)**

  - <span></span>  
    [Set-CsDirector](https://technet.microsoft.com/library/Gg398565(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Reset-CsPoolRegistrarState](https://technet.microsoft.com/library/JJ619172(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Set-CsRegistrar](https://technet.microsoft.com/library/Gg398993(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398483(v=OCS.15))

  - <span></span>  
    [新-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg425893(v=OCS.15))

  - <span></span>  
    [Remove-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398482(v=OCS.15))

  - <span></span>  
    [Set-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398764(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15))

**[Lync Server 2013 中的服务 cmdlet](lync-server-2013-services-cmdlets.md)**

  - <span></span>  
    [CsService](https://technet.microsoft.com/library/Gg413038(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsWindowsService](https://technet.microsoft.com/library/Gg398803(v=OCS.15))

  - <span></span>  
    [开始-CsWindowsService](https://technet.microsoft.com/library/Gg398561(v=OCS.15))

  - <span></span>  
    [停止-CsWindowsService](https://technet.microsoft.com/library/Gg398426(v=OCS.15))

**[Lync Server 2013 中的服务器角色和服务 cmdlet 疑难解答](lync-server-2013-troubleshooting-server-roles-and-services-cmdlets.md)**

  - <span></span>  
    [Get-CsAudioTestServiceApplication](https://technet.microsoft.com/library/Gg412984(v=OCS.15))

  - <span></span>  
    [Set-CsAudioTestServiceApplication](https://technet.microsoft.com/library/Gg398907(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg398667(v=OCS.15))

  - <span></span>  
    [新-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg398718(v=OCS.15))

  - <span></span>  
    [Remove-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg425794(v=OCS.15))

  - <span></span>  
    [Set-CsHealthMonitoringConfiguration](https://technet.microsoft.com/library/Gg425847(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg413034(v=OCS.15))

  - <span></span>  
    [New-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg398733(v=OCS.15))

  - <span></span>  
    [Remove-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg412853(v=OCS.15))

  - <span></span>  
    [Set-CsDiagnosticConfiguration](https://technet.microsoft.com/library/Gg425734(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [新-CsDiagnosticsFilter](https://technet.microsoft.com/library/Gg413009(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg412774(v=OCS.15))

  - <span></span>  
    [新-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg398350(v=OCS.15))

  - <span></span>  
    [Remove-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg398941(v=OCS.15))

  - <span></span>  
    [Set-CsDiagnosticHeaderConfiguration](https://technet.microsoft.com/library/Gg399045(v=OCS.15))

**[Lync Server 2013 中的 Web 服务器和服务 cmdlet](lync-server-2013-web-server-and-services-cmdlets.md)**

  - <span></span>  
    [新-CsSimpleUrl](https://technet.microsoft.com/library/Gg398180(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg398392(v=OCS.15))

  - <span></span>  
    [新-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg425813(v=OCS.15))

  - <span></span>  
    [Remove-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg398515(v=OCS.15))

  - <span></span>  
    [Set-CsSimpleUrlConfiguration](https://technet.microsoft.com/library/Gg412991(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [新-CsSimpleUrlEntry](https://technet.microsoft.com/library/Gg425902(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Set-CsWebServer](https://technet.microsoft.com/library/Gg398759(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg425751(v=OCS.15))

  - <span></span>  
    [新-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398440(v=OCS.15))

  - <span></span>  
    [Remove-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398266(v=OCS.15))

  - <span></span>  
    [Set-CsWebServiceConfiguration](https://technet.microsoft.com/library/Gg398396(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [New-CsWebTrustedCACertificate](https://technet.microsoft.com/library/Gg412746(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [New-CsKerberosAccount](https://technet.microsoft.com/library/Gg398485(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398526(v=OCS.15))

  - <span></span>  
    [New-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398074(v=OCS.15))

  - <span></span>  
    [Remove-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg413052(v=OCS.15))

  - <span></span>  
    [Set-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg398232(v=OCS.15))

  - <span></span>  
    [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15))

<!-- end list -->

  - [Test-CsWebApp](https://technet.microsoft.com/library/Hh689989(v=OCS.15))

  - [Test-CsWebAppAnonymous](https://technet.microsoft.com/library/Hh690041(v=OCS.15))

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

