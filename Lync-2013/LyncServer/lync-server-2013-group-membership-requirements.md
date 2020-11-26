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
# <a name="group-membership-requirements-for-lync-server-2013"></a><span data-ttu-id="a93bd-103">Lync Server 2013 的组成员身份要求</span><span class="sxs-lookup"><span data-stu-id="a93bd-103">Group membership requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a93bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a93bd-104">

<span> </span></span></span>

<span data-ttu-id="a93bd-105">_**主题上次修改时间：** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="a93bd-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="a93bd-106">下表总结了人员应属于的组或组，以便成功安装、管理 Lync Server 2013 并对其进行故障排除。</span><span class="sxs-lookup"><span data-stu-id="a93bd-106">The following table summarizes the group or groups that a person should belong to in order to successfully install, manage, and troubleshoot Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a93bd-107">Lync Server 2013 可执行文件</span><span class="sxs-lookup"><span data-stu-id="a93bd-107">Lync Server 2013 Executable</span></span></th>
<th><span data-ttu-id="a93bd-108">需要组成员身份</span><span class="sxs-lookup"><span data-stu-id="a93bd-108">Group Membership Required</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a93bd-109"><strong>Setup.exe</strong> –开始安装 Lync Server 2013 管理工具的可执行文件。</span><span class="sxs-lookup"><span data-stu-id="a93bd-109"><strong>Setup.exe</strong> – Executable that starts the installation of the Lync Server 2013 administrative tools.</span></span></p></td>
<td><p><span data-ttu-id="a93bd-110">运行可执行文件的计算机上本地管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="a93bd-110">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="a93bd-111">"域用户" 组的成员以读取 Active Directory 域服务中的信息。</span><span class="sxs-lookup"><span data-stu-id="a93bd-111">Member of Domain Users group to read information in Active Directory Domain Services.</span></span> <span data-ttu-id="a93bd-112">此权限级别是必需的，因为在本地计算机上自动安装所需的 MSI 程序包需要允许读取和写入受保护的本地计算机资源（如程序文件目录）和受保护的注册表（如本地计算机配置单元）的权限。</span><span class="sxs-lookup"><span data-stu-id="a93bd-112">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="a93bd-113">你还可以将设置权限委派给你不希望向其授予域管理员组成员身份的用户或组。</span><span class="sxs-lookup"><span data-stu-id="a93bd-113">You can also delegate setup permissions to users or groups to whom you do not want to grant membership in the Domain Admins group.</span></span> <span data-ttu-id="a93bd-114">有关详细信息，请参阅部署文档中的 <A href="lync-server-2013-granting-setup-permissions.md">在 Lync Server 2013 中授予设置权限</A> 。</span><span class="sxs-lookup"><span data-stu-id="a93bd-114">For details, see <A href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</A> in the Deployment documentation.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93bd-115"><strong>Deploy.exe</strong> –由 setup.exe 调用，deploy.exe 负责为服务器角色部署软件组件。</span><span class="sxs-lookup"><span data-stu-id="a93bd-115"><strong>Deploy.exe</strong> – Called by setup.exe, deploy.exe is responsible for the deployment of the software components for the server roles.</span></span></p></td>
<td><p><span data-ttu-id="a93bd-116">运行可执行文件的计算机上本地管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="a93bd-116">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="a93bd-117">"域用户" 组的成员以读取 AD DS 中的信息。</span><span class="sxs-lookup"><span data-stu-id="a93bd-117">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="a93bd-118">此权限级别是必需的，因为在本地计算机上自动安装所需的 MSI 程序包需要允许读取和写入受保护的本地计算机资源（如程序文件目录）和受保护的注册表（如本地计算机配置单元）的权限。</span><span class="sxs-lookup"><span data-stu-id="a93bd-118">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span> <span data-ttu-id="a93bd-119">若要阅读中央管理存储，RtcUniversalReadOnlyAdmins 组中的成员身份是必需的。</span><span class="sxs-lookup"><span data-stu-id="a93bd-119">Membership in RtcUniversalReadOnlyAdmins group is necessary to read the Central Management store.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="a93bd-120">如果您运行的是 Windows Vista 操作系统或 Windows 7 操作系统，则系统会提示用户帐户控制 (UAC) 继续安装。</span><span class="sxs-lookup"><span data-stu-id="a93bd-120">If you are running the Windows Vista operating system or Windows 7 operating system, you will be prompted by User Account Control (UAC) to proceed with installation.</span></span> <span data-ttu-id="a93bd-121">如果您使用标准用户帐户登录，则当系统提示您有权安装软件的帐户时，您将需要属于本地管理员组成员的人员才能提供凭据。</span><span class="sxs-lookup"><span data-stu-id="a93bd-121">If you are logged on with a standard user account, you will need someone who is a member of the Local Administrators group to provide credentials when prompted for an account with permissions to install the software.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93bd-122"><strong>Bootstrapper.exe</strong> –由 setup.exe 调用，bootstrapper.exe 负责部署和配置服务器角色。</span><span class="sxs-lookup"><span data-stu-id="a93bd-122"><strong>Bootstrapper.exe</strong> – Called by setup.exe, bootstrapper.exe is responsible for deployment and configuration of server roles.</span></span></p></td>
<td><p><span data-ttu-id="a93bd-123">运行可执行文件的计算机上本地管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="a93bd-123">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="a93bd-124">RTCUniversalServerAdmins 组的成员以运行 Bootstrapper.exe。</span><span class="sxs-lookup"><span data-stu-id="a93bd-124">Member of the RTCUniversalServerAdmins group to run Bootstrapper.exe.</span></span> <span data-ttu-id="a93bd-125">"域用户" 组的成员以读取 AD DS 中的信息。</span><span class="sxs-lookup"><span data-stu-id="a93bd-125">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="a93bd-126">此权限级别是必需的，因为在本地计算机上自动安装所需的 MSI 程序包需要允许读取和写入受保护的本地计算机资源（如程序文件目录）和受保护的注册表（如本地计算机配置单元）的权限。</span><span class="sxs-lookup"><span data-stu-id="a93bd-126">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93bd-127"><strong>TopologyBuilder</strong> -由向导驱动的用户界面，用于创建、查看、调整和验证 Lync Server 2013 拓扑。</span><span class="sxs-lookup"><span data-stu-id="a93bd-127"><strong>TopologyBuilder</strong> – Wizard-driven user interface to create, view, adjust, and validate Lync Server 2013 topologies.</span></span></p></td>
<td><p><span data-ttu-id="a93bd-128">运行可执行文件的计算机上本地管理员组的成员，以查看拓扑。</span><span class="sxs-lookup"><span data-stu-id="a93bd-128">Member of the Local Administrators group on the computer from which the executable is run to view the topology.</span></span> <span data-ttu-id="a93bd-129">RTCUniversalServerAdmins 组的成员以更改配置设置。</span><span class="sxs-lookup"><span data-stu-id="a93bd-129">Member of the RTCUniversalServerAdmins group to change configuration settings.</span></span> <span data-ttu-id="a93bd-130">RTCUniversalServerAdmins 组和域管理员组的成员或 RTCUniversalServerAdmins 组的成员 (仅当该组已被授予委派设置权限) 时，才能发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="a93bd-130">Member of the RTCUniversalServerAdmins group and Domain Admins group, or member of the RTCUniversalServerAdmins group (only if the group has been granted delegate setup permissions), to publish the topology.</span></span> <span data-ttu-id="a93bd-131">有关委派设置权限以允许 RTCUniversalServerAdmins 组的成员发布拓扑的详细信息，而不是域管理员组的成员，请参阅部署文档中 <a href="lync-server-2013-granting-setup-permissions.md">Lync Server 2013 中的 "授予设置权限</a> "。</span><span class="sxs-lookup"><span data-stu-id="a93bd-131">For details about delegating setup permissions to allow members of the RTCUniversalServerAdmins group to publish the topology without being members of the Domain Admins group, see <a href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93bd-132"><strong>AdminUIHost</strong> –用于管理 Lync Server 2013 的基于 Web 的图形用户界面。</span><span class="sxs-lookup"><span data-stu-id="a93bd-132"><strong>AdminUIHost</strong> – Web-based graphical user interface for managing Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="a93bd-133">CsAdministrator 组的成员或其他基于角色的访问控制的成员 (为其分配特定管理任务的 RBAC) 角色。</span><span class="sxs-lookup"><span data-stu-id="a93bd-133">Member of CsAdministrator group or member of another role-based access control (RBAC) role to which the specific administrative task is assigned.</span></span> <span data-ttu-id="a93bd-134">Lync Server 2013 控制面板通过运行 Lync Server 2013 管理外壳 cmdlet 实现配置更改。</span><span class="sxs-lookup"><span data-stu-id="a93bd-134">Lync Server 2013 Control Panel implements configuration changes by running Lync Server 2013 Management Shell cmdlets.</span></span> <span data-ttu-id="a93bd-135">有关预定义角色和 cmdlet 成员的列表，请参阅规划文档中的在 <a href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 中规划基于角色的访问控制</a> 。</span><span class="sxs-lookup"><span data-stu-id="a93bd-135">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93bd-136">已<strong>加载 Lync server 2013 模块的PowerShell.exe</strong> -具有特定于 lync server 2013 管理的 cmdlet 的命令行管理工具。</span><span class="sxs-lookup"><span data-stu-id="a93bd-136"><strong>PowerShell.exe with the Lync Server 2013 module loaded</strong> – Command-line administrative tool with cmdlets specific to management of Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="a93bd-137">已分配特定 cmdlet 的其他 RBAC 角色的 CsAdministrator 组成员或成员。</span><span class="sxs-lookup"><span data-stu-id="a93bd-137">Member of CsAdministrator group or member of another RBAC role to which the specific cmdlet has been assigned.</span></span> <span data-ttu-id="a93bd-138">有关预定义角色和 cmdlet 成员的列表，请参阅规划文档中的在 <a href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 中规划基于角色的访问控制</a> 。</span><span class="sxs-lookup"><span data-stu-id="a93bd-138">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="a93bd-139">或者是以下一个或多个组的成员，具体取决于 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="a93bd-139">Or, member of one or more of the following groups, depending on the cmdlet:</span></span></p>
<ul>
<li><p><span data-ttu-id="a93bd-140">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="a93bd-140">RTCUniversalServerAdmins</span></span></p></li>
<li><p><span data-ttu-id="a93bd-141">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="a93bd-141">RTCUniversalUserAdmins</span></span></p></li>
<li><p><span data-ttu-id="a93bd-142">RTCUniversalReadOnlyAdmins</span><span class="sxs-lookup"><span data-stu-id="a93bd-142">RTCUniversalReadOnlyAdmins</span></span></p></li>
</ul></td>
</tr><span data-ttu-id="a93bd-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a93bd-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

