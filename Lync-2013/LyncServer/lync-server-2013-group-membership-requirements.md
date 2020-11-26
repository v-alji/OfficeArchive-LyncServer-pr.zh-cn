---
title: Lync Server 2013：组成员身份要求
description: Lync Server 2013：组成员身份要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group membership requirements
ms:assetid: 01876843-8717-4e72-baf5-866ac8cceee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204623(v=OCS.15)
ms:contentKeyID: 48183239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f18fb6fbc782ecd41b7a782965f2cd6a82f6fd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427836"
---
# <a name="group-membership-requirements-for-lync-server-2013"></a>Lync Server 2013 的组成员身份要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-05_

下表总结了人员应属于的组或组，以便成功安装、管理 Lync Server 2013 并对其进行故障排除。


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lync Server 2013 可执行文件</th>
<th>需要组成员身份</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Setup.exe</strong> –开始安装 Lync Server 2013 管理工具的可执行文件。</p></td>
<td><p>运行可执行文件的计算机上本地管理员组的成员。 "域用户" 组的成员以读取 Active Directory 域服务中的信息。 此权限级别是必需的，因为在本地计算机上自动安装所需的 MSI 程序包需要允许读取和写入受保护的本地计算机资源（如程序文件目录）和受保护的注册表（如本地计算机配置单元）的权限。</p>
<div>

> [!TIP]  
> 你还可以将设置权限委派给你不希望向其授予域管理员组成员身份的用户或组。 有关详细信息，请参阅部署文档中的 <A href="lync-server-2013-granting-setup-permissions.md">在 Lync Server 2013 中授予设置权限</A> 。


</div></td>
</tr>
<tr class="even">
<td><p><strong>Deploy.exe</strong> –由 setup.exe 调用，deploy.exe 负责为服务器角色部署软件组件。</p></td>
<td><p>运行可执行文件的计算机上本地管理员组的成员。 "域用户" 组的成员以读取 AD DS 中的信息。 此权限级别是必需的，因为在本地计算机上自动安装所需的 MSI 程序包需要允许读取和写入受保护的本地计算机资源（如程序文件目录）和受保护的注册表（如本地计算机配置单元）的权限。 若要阅读中央管理存储，RtcUniversalReadOnlyAdmins 组中的成员身份是必需的。</p>
<div>

> [!NOTE]  
> 如果您运行的是 Windows Vista 操作系统或 Windows 7 操作系统，则系统会提示用户帐户控制 (UAC) 继续安装。 如果您使用标准用户帐户登录，则当系统提示您有权安装软件的帐户时，您将需要属于本地管理员组成员的人员才能提供凭据。


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Bootstrapper.exe</strong> –由 setup.exe 调用，bootstrapper.exe 负责部署和配置服务器角色。</p></td>
<td><p>运行可执行文件的计算机上本地管理员组的成员。 RTCUniversalServerAdmins 组的成员以运行 Bootstrapper.exe。 "域用户" 组的成员以读取 AD DS 中的信息。 此权限级别是必需的，因为在本地计算机上自动安装所需的 MSI 程序包需要允许读取和写入受保护的本地计算机资源（如程序文件目录）和受保护的注册表（如本地计算机配置单元）的权限。</p></td>
</tr>
<tr class="even">
<td><p><strong>TopologyBuilder</strong> -由向导驱动的用户界面，用于创建、查看、调整和验证 Lync Server 2013 拓扑。</p></td>
<td><p>运行可执行文件的计算机上本地管理员组的成员，以查看拓扑。 RTCUniversalServerAdmins 组的成员以更改配置设置。 RTCUniversalServerAdmins 组和域管理员组的成员或 RTCUniversalServerAdmins 组的成员 (仅当该组已被授予委派设置权限) 时，才能发布拓扑。 有关委派设置权限以允许 RTCUniversalServerAdmins 组的成员发布拓扑的详细信息，而不是域管理员组的成员，请参阅部署文档中 <a href="lync-server-2013-granting-setup-permissions.md">Lync Server 2013 中的 "授予设置权限</a> "。</p></td>
</tr>
<tr class="odd">
<td><p><strong>AdminUIHost</strong> –用于管理 Lync Server 2013 的基于 Web 的图形用户界面。</p></td>
<td><p>CsAdministrator 组的成员或其他基于角色的访问控制的成员 (为其分配特定管理任务的 RBAC) 角色。 Lync Server 2013 控制面板通过运行 Lync Server 2013 管理外壳 cmdlet 实现配置更改。 有关预定义角色和 cmdlet 成员的列表，请参阅规划文档中的在 <a href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 中规划基于角色的访问控制</a> 。</p></td>
</tr>
<tr class="even">
<td><p>已<strong>加载 Lync server 2013 模块的PowerShell.exe</strong> -具有特定于 lync server 2013 管理的 cmdlet 的命令行管理工具。</p></td>
<td><p>已分配特定 cmdlet 的其他 RBAC 角色的 CsAdministrator 组成员或成员。 有关预定义角色和 cmdlet 成员的列表，请参阅规划文档中的在 <a href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 中规划基于角色的访问控制</a> 。</p>
<p>或者是以下一个或多个组的成员，具体取决于 cmdlet：</p>
<ul>
<li><p>RTCUniversalServerAdmins</p></li>
<li><p>RTCUniversalUserAdmins</p></li>
<li><p>RTCUniversalReadOnlyAdmins</p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

