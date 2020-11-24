---
title: Lync Server 2013：规划基于角色的访问控制
description: Lync Server 2013：规划基于角色的访问控制。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for role-based access control (RBAC)
ms:assetid: 41204ba3-ce5b-41a8-a6c3-b444468fa328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425917(v=OCS.15)
ms:contentKeyID: 48183962
ms.date: 01/28/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 971b3353694a1cdd53d88452717e6a9a360c6870
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392496"
---
# <a name="planning-for-role-based-access-control-in-lync-server-2013"></a><span data-ttu-id="2a0bf-103">在 Lync Server 2013 中规划基于角色的访问控制</span><span class="sxs-lookup"><span data-stu-id="2a0bf-103">Planning for role-based access control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a0bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a0bf-104">

<span> </span></span></span>

<span data-ttu-id="2a0bf-105">_**主题上次修改时间：** 2015-01-27_</span><span class="sxs-lookup"><span data-stu-id="2a0bf-105">_**Topic Last Modified:** 2015-01-27_</span></span>

<span data-ttu-id="2a0bf-106">为了使你能够在保持高安全性标准的同时委派管理任务，Lync Server 2013 提供基于角色的访问控制 (RBAC) 。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-106">To enable you to delegate administrative tasks while maintaining high standards for security, Lync Server 2013 offers role-based access control (RBAC).</span></span> <span data-ttu-id="2a0bf-107">通过 RBAC，管理员权限可通过向管理角色分配用户来授予。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-107">With RBAC, administrative privilege is granted by assigning users to administrative roles.</span></span> <span data-ttu-id="2a0bf-108">Lync Server 2013 包含一组丰富的内置管理角色，还使你能够创建新角色并为每个新角色指定一个自定义 cmdlet 列表。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-108">Lync Server 2013 includes a rich set of built-in administrative roles, and also enables you to create new roles and specify a custom list of cmdlets for each new role.</span></span> <span data-ttu-id="2a0bf-109">您还可以将 cmdlet 的脚本添加到所允许的预定义和自定义 RBAC 角色任务中。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-109">You can also add scripts of cmdlets to the allowed tasks of both predefined and custom RBAC roles.</span></span>

<div>

## <a name="better-server-security-and-centralization"></a><span data-ttu-id="2a0bf-110">更好的服务器安全和集中化</span><span class="sxs-lookup"><span data-stu-id="2a0bf-110">Better Server Security and Centralization</span></span>

<span data-ttu-id="2a0bf-111">使用 RBAC、访问和授权完全基于用户的 Lync 服务器角色。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-111">With RBAC, access and authorization is based precisely on a user’s Lync Server role.</span></span> <span data-ttu-id="2a0bf-112">这允许使用 "最低权限" 安全做法，仅授予管理员和用户其作业所需的权限。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-112">This enables use of the security practice of "least privilege," granting administrators and users only the rights that are necessary for their job.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="2a0bf-113">只有在远程工作的管理员使用 Lync Server 控制面板或 Lync Server 命令行管理程序时，RBAC 限制才有效。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-113">RBAC restrictions work only on administrators working remotely, using either the Lync Server Control Panel or Lync Server Management Shell.</span></span> <span data-ttu-id="2a0bf-114">用户坐在运行 Lync Server 的服务器上时，该用户不受 RBAC 限制。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-114">A user sitting at a server running Lync Server is not restricted by RBAC.</span></span> <span data-ttu-id="2a0bf-115">因此，您的 Lync 服务器的物理安全对于保留 RBAC 限制非常重要。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-115">Therefore, physical security of your Lync Server is important to preserve RBAC restrictions.</span></span>



</div>

</div>

<div>

## <a name="roles-and-scope"></a><span data-ttu-id="2a0bf-116">角色和作用域</span><span class="sxs-lookup"><span data-stu-id="2a0bf-116">Roles and Scope</span></span>

<span data-ttu-id="2a0bf-117">在 RBAC 中，启用了 *角色* 以使用 cmdlet 的列表，这些 cmdlet 适用于特定类型的管理员或技术人员。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-117">In RBAC, a *role* is enabled to use a list of cmdlets, designed to be useful for a certain type of administrator or technician.</span></span> <span data-ttu-id="2a0bf-118">*作用域* 是指角色中定义的 cmdlet 可以操作的对象集。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-118">A *scope* is the set of objects which the cmdlets defined in a role can operate on.</span></span> <span data-ttu-id="2a0bf-119">作用域所影响的对象可以是按组织单位) 的用户帐户 (按网站) 分组的 (服务器。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-119">The objects that scope affects can be either user accounts (grouped by organizational unit) or servers (grouped by site).</span></span>

<span data-ttu-id="2a0bf-120">下表列出了 Lync Server 中的预定义角色，并概括介绍了每个角色可以执行的任务类型。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-120">The following table lists the predefined roles in Lync Server, and gives a general overview of the types of tasks each can do.</span></span> <span data-ttu-id="2a0bf-121">第四列显示了每个 Lync 服务器角色的类似 Microsoft Exchange 服务器角色（如果有）。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-121">The fourth column shows the similar Microsoft Exchange Server role for each Lync Server role, if there is one.</span></span>

### <a name="predefined-administrative-roles"></a><span data-ttu-id="2a0bf-122">预定义的管理角色</span><span class="sxs-lookup"><span data-stu-id="2a0bf-122">Predefined Administrative Roles</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a0bf-123">角色</span><span class="sxs-lookup"><span data-stu-id="2a0bf-123">Role</span></span></th>
<th><span data-ttu-id="2a0bf-124">允许的任务</span><span class="sxs-lookup"><span data-stu-id="2a0bf-124">Tasks allowed</span></span></th>
<th><span data-ttu-id="2a0bf-125">基础 Active Directory 组</span><span class="sxs-lookup"><span data-stu-id="2a0bf-125">Underlying Active Directory group</span></span></th>
<th><span data-ttu-id="2a0bf-126">等同于 Exchange</span><span class="sxs-lookup"><span data-stu-id="2a0bf-126">Exchange equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a0bf-127">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-127">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-128">可以执行所有管理任务和修改所有设置，包括创建角色和向角色分配用户。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-128">Can perform all administrative tasks and modify all settings, including creating roles and assigning users to roles.</span></span> <span data-ttu-id="2a0bf-129">可以通过添加新的网站、池和服务来扩展部署。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-129">Can expand a deployment by adding new sites, pools, and services.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-130">CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-130">CSAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-131">组织管理</span><span class="sxs-lookup"><span data-stu-id="2a0bf-131">Organization Management</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a0bf-132">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-132">CsUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-133">可以为 Lync Server 启用和禁用用户、移动用户并向用户分配现有策略。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-133">Can enable and disable users for Lync Server, move users and assign existing policies to users.</span></span> <span data-ttu-id="2a0bf-134">无法修改策略。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-134">Cannot modify policies.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-135">CSUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-135">CSUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-136">邮件收件人</span><span class="sxs-lookup"><span data-stu-id="2a0bf-136">Mail Recipients</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a0bf-137">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-137">CsVoiceAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-138">可以创建、配置和管理与语音相关的设置和策略。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-138">Can create, configure, and manage voice-related settings and policies.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-139">CSVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-139">CSVoiceAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-140">不适用</span><span class="sxs-lookup"><span data-stu-id="2a0bf-140">Not applicable</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a0bf-141">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-141">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-142">可以管理和监视服务器和服务并解决问题。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-142">Can manage, monitor, and troubleshoot servers and services.</span></span> <span data-ttu-id="2a0bf-143">可以阻止与服务器的新连接、停止和启动服务以及应用软件更新。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-143">Can prevent new connections to servers, stop and start services, and apply software updates.</span></span> <span data-ttu-id="2a0bf-144">全局配置影响无法进行更改。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-144">Cannot make changes with global configuration impact.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-145">CSServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-145">CSServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-146">服务器管理</span><span class="sxs-lookup"><span data-stu-id="2a0bf-146">Server Management</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a0bf-147">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-147">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-148">可以查看部署，包括用户和服务器信息，以便监视部署运行状况。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-148">Can view the deployment, including user and server information, in order to monitor deployment health.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-149">CSViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-149">CSViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-150">View-Only 组织管理</span><span class="sxs-lookup"><span data-stu-id="2a0bf-150">View-Only Organization Management</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a0bf-151">CsHelpDesk</span><span class="sxs-lookup"><span data-stu-id="2a0bf-151">CsHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-152">可以查看部署，包括用户的属性和策略。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-152">Can view the deployment, including user's properties and policies.</span></span> <span data-ttu-id="2a0bf-153">可以运行特定的疑难解答任务。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-153">Can run specific troubleshooting tasks.</span></span> <span data-ttu-id="2a0bf-154">无法更改用户属性或策略、服务器配置或服务。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-154">Cannot change user properties or policies, server configuration, or services.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-155">CSHelpDesk</span><span class="sxs-lookup"><span data-stu-id="2a0bf-155">CSHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-156">支持人员</span><span class="sxs-lookup"><span data-stu-id="2a0bf-156">HelpDesk</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a0bf-157">CsArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-157">CsArchivingAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-158">可以修改存档配置和策略。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-158">Can modify archiving configuration and policies.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-159">CSArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-159">CSArchivingAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-160">保留管理，法律封存</span><span class="sxs-lookup"><span data-stu-id="2a0bf-160">Retention Management, Legal Hold</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a0bf-161">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-161">CsResponseGroupAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-162">可以管理网站内响应组应用程序的配置。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-162">Can manage the configuration of the Response Group application within a site.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-163">CSResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-163">CSResponseGroupAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-164">不适用</span><span class="sxs-lookup"><span data-stu-id="2a0bf-164">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a0bf-165">CsLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-165">CsLocationAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-166">增强 9-1-1 (E9-1-1) 管理的最低权限级别，包括创建 E9 位置和网络标识符，以及将它们相互关联。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-166">Lowest level of rights for Enhanced 9-1-1 (E9-1-1) management, including creating E9-1-1 locations and network identifiers, and associating these with each other.</span></span> <span data-ttu-id="2a0bf-167">此角色始终分配有全局范围。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-167">This role is always assigned with a global scope.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-168">CSLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-168">CSLocationAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-169">不适用</span><span class="sxs-lookup"><span data-stu-id="2a0bf-169">Not applicable</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a0bf-170">CsResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="2a0bf-170">CsResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-171">可以管理特定的响应组。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-171">Can manage specific response groups.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-172">CSResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="2a0bf-172">CSResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-173">不适用</span><span class="sxs-lookup"><span data-stu-id="2a0bf-173">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a0bf-174">CsPersistentChatAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-174">CsPersistentChatAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-175">可以管理持久聊天功能和特定的持久聊天聊天室。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-175">Can manage the Persistent Chat feature and specific Persistent Chat rooms.</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-176">CSPersistentChatAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a0bf-176">CSPersistentChatAdministrator</span></span></p></td>
<td><p><span data-ttu-id="2a0bf-177">不适用</span><span class="sxs-lookup"><span data-stu-id="2a0bf-177">Not applicable</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a0bf-178">Lync Server 附带的所有预定义角色都具有全局范围。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-178">All predefined roles shipped in Lync Server have a global scope.</span></span> <span data-ttu-id="2a0bf-179">若要遵循最低权限做法，则不应将用户分配给具有全局范围的角色（如果他们仅管理有限的一组服务器或用户）。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-179">To follow least privilege practices, you should not assign users to roles with global scope if they are going to administer only a limited set of servers or users.</span></span> <span data-ttu-id="2a0bf-180">若要实现此目的，你可以创建基于现有角色的角色，但范围更有限。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-180">To accomplish this, you can create roles which are based on an existing role, but with a more limited scope.</span></span>

<div>

## <a name="creating-a-scoped-role"></a><span data-ttu-id="2a0bf-181">创建作用域角色</span><span class="sxs-lookup"><span data-stu-id="2a0bf-181">Creating a Scoped Role</span></span>

<span data-ttu-id="2a0bf-182">创建具有有限作用域的角色 (作用域角色) 时，你可以指定作用域以及它所基于的现有角色以及要为其分配角色的 Active Directory 组。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-182">When you create a role with limited scope (a scoped role), you specify the scope, along with the existing role it is based on and the Active Directory group to be assigned the role.</span></span> <span data-ttu-id="2a0bf-183">你指定的 Active Directory 组必须已创建。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-183">The Active Directory group you specify must already be created.</span></span> <span data-ttu-id="2a0bf-184">以下 cmdlet 是创建一个角色的示例，该角色具有一个预定义的管理角色的权限，但范围有限。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-184">The following cmdlet is an example of a creating a role which has the privileges of one of the pre-defined administrative roles, but with limited scope.</span></span> <span data-ttu-id="2a0bf-185">它将创建一个名为 `Site01 Server Administrators` 的新角色。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-185">It creates a new role called `Site01 Server Administrators`.</span></span> <span data-ttu-id="2a0bf-186">角色具有预定义的 CsServerAdministrator 角色的功能，但仅适用于位于 Site01 网站中的服务器。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-186">The role has the abilities of the predefined CsServerAdministrator role, but only for the servers located in the Site01 site.</span></span> <span data-ttu-id="2a0bf-187">为使此 cmdlet 正常工作，Site01 网站必须已定义，并且名为的通用安全组 `Site01 Server Administrators` 必须已经存在。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-187">For this cmdlet to work, the Site01 site must already be defined, and a universal security group named `Site01 Server Administrators` must already exist.</span></span>

    New-CsAdminRole -Identity "Site01 Server Administrators" -Template CsServerAdministrator -ConfigScopes "site:Site01"

<span data-ttu-id="2a0bf-188">运行此 cmdlet 后，属于该组成员的所有用户 `Site01 Server Administrators` 将拥有 Site01 中服务器的服务器管理员权限。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-188">After this cmdlet runs, all users who are members of the `Site01 Server Administrators` group will have server administrator privileges for the servers in Site01.</span></span> <span data-ttu-id="2a0bf-189">此外，随后添加到此通用安全组的任何用户也会获得此角色的权限。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-189">Additionally, any users who are later added to this universal security group also gain the privileges of this role.</span></span> <span data-ttu-id="2a0bf-190">请注意，角色本身和分配给它的通用安全组都被称为 `Site01 Server Administrators` 。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-190">Note that both the role itself, and the universal security group it is assigned to are called `Site01 Server Administrators`.</span></span>

<span data-ttu-id="2a0bf-191">以下示例限制用户范围，而不是服务器范围。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-191">The following example limits user scope instead of server scope.</span></span> <span data-ttu-id="2a0bf-192">它将创建一个 `Sales Users Administrator` 角色来管理销售组织单位中的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-192">It creates a `Sales Users Administrator` role to administer the user accounts in the Sales organizational unit.</span></span> <span data-ttu-id="2a0bf-193">必须已创建 SalesUsersAdministrator 通用安全组，此 cmdlet 才能正常工作。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-193">The SalesUsersAdministrator universal security group must already be created for this cmdlet to work.</span></span>

    New-CsAdminRole -Identity "Sales Users Administrator " -Template CsUserAdministrator -UserScopes "OU:OU=Sales, OU=Lync Tenants, DC=Domain, DC=com"

</div>

<div>

## <a name="creating-a-new-role"></a><span data-ttu-id="2a0bf-194">创建新角色</span><span class="sxs-lookup"><span data-stu-id="2a0bf-194">Creating a New Role</span></span>

<span data-ttu-id="2a0bf-195">若要创建可访问一组不在预定义角色或一组脚本或模块中的一组 cmdlet 的角色，请再次使用预定义角色之一作为模板开始。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-195">To create a role that has access to a set of cmdlets not in one of the predefined roles, or to a set of scripts or modules, you again start by using one of the predefined roles as a template.</span></span> <span data-ttu-id="2a0bf-196">请注意，角色可以运行的脚本和模块必须存储在以下位置：</span><span class="sxs-lookup"><span data-stu-id="2a0bf-196">Note that scripts and modules that roles are to be able to run must be stored in the following locations:</span></span>

  - <span data-ttu-id="2a0bf-197">Lync 模块路径，默认情况下为 C： \\ 程序文件 \\ 常见文件 \\ Microsoft Lync Server 2013 \\ 模块 \\ Lync</span><span class="sxs-lookup"><span data-stu-id="2a0bf-197">The Lync module path, which is by default C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\Modules\\Lync</span></span>

  - <span data-ttu-id="2a0bf-198">用户脚本路径，默认情况下为 C： \\ 程序文件 \\ 常见文件 \\ Microsoft Lync Server 2013 \\ AdminScripts</span><span class="sxs-lookup"><span data-stu-id="2a0bf-198">The user script path, which is by default C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\AdminScripts</span></span>

<span data-ttu-id="2a0bf-199">若要创建新角色，请使用 **CsAdminRole** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-199">To make a new role, you use the **New-CsAdminRole** cmdlet.</span></span> <span data-ttu-id="2a0bf-200">在运行 **New-CsAdminRole** 之前，必须首先创建将与此角色关联的基础通用安全组。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-200">Before running **New-CsAdminRole**, you must first create the underlying universal security group that will be associated with this role.</span></span>

<span data-ttu-id="2a0bf-201">以下 cmdlet 用作创建新角色的示例。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-201">The following cmdlets serve as an example of a creating a new role.</span></span> <span data-ttu-id="2a0bf-202">他们创建了一个名为的新角色类型 `MyHelpDeskScriptRole` 。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-202">They create a new role type called `MyHelpDeskScriptRole`.</span></span> <span data-ttu-id="2a0bf-203">新角色具有预定义的 CsHelpDesk 角色的功能，并且还可以在名为 "testscript" 的脚本中运行函数。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-203">The new role has the abilities of the predefined CsHelpDesk role, and can additionally run the functions in a script named “testscript”.</span></span>

    New-CsAdminRole -Identity "MyHelpDeskScriptRole" -Template CsHelpDesk -ScriptModules @{Add="testScript.ps1"}

<span data-ttu-id="2a0bf-204">为使此 cmdlet 正常工作，你必须首先创建通用安全组 MyHelpDeskScriptRole。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-204">For this cmdlet to work, you must have first created the universal security group MyHelpDeskScriptRole.</span></span>

<span data-ttu-id="2a0bf-205">运行此 cmdlet 后，你可以将用户直接分配给此角色 (，在这种情况下，他们具有全局作用域) ，或者基于此角色创建作用域角色，如在本文档中创建作用域角色中所述。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-205">After this cmdlet runs, you can assign users directly to this role (in which case they have global scope), or create a scoped role based on this role, as explained in Creating a Scoped Role, previously in this document.</span></span>

</div>

<div>

## <a name="assigning-roles-to-users"></a><span data-ttu-id="2a0bf-206">向用户分配角色</span><span class="sxs-lookup"><span data-stu-id="2a0bf-206">Assigning Roles to Users</span></span>

<span data-ttu-id="2a0bf-207">每个 Lync 服务器角色都与一个基础 Active Directory 通用安全组相关联。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-207">Each Lync Server role is associated with an underlying Active Directory universal security group.</span></span> <span data-ttu-id="2a0bf-208">你添加到基础组的任何用户都可以获得该角色的能力。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-208">Any users who you add to the underlying group gain the abilities of that role.</span></span>

<span data-ttu-id="2a0bf-209">上述部分中的示例创建了一个新角色并向新角色分配了现有通用安全组。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-209">The examples in the preceding sections both created a new role and assigned an existing universal security group to the new role.</span></span> <span data-ttu-id="2a0bf-210">若要将现有角色分配给一个或多个用户，请将这些用户添加到与该角色关联的组中。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-210">To assign an existing role to one or more users, add those users to the group associated with the role.</span></span> <span data-ttu-id="2a0bf-211">你可以将单个用户和通用安全组添加到这些组。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-211">You can add both individual users and universal security groups to these groups.</span></span>

<span data-ttu-id="2a0bf-212">例如， **CsAdministrator** 角色将自动授予 Active Directory 中的 **CS 管理员** 通用安全组。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-212">For example, the **CsAdministrator** role is automatically granted to the **CS Administrators** universal security group in Active Directory.</span></span> <span data-ttu-id="2a0bf-213">当你部署 Lync Server 时，将在 Active Directory 中创建此通用安全组。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-213">This universal security group is created in Active Directory when you deploy Lync Server.</span></span> <span data-ttu-id="2a0bf-214">若要向用户或组授予此权限，只需将其添加到 **CS 管理员** 组即可。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-214">To grant a user or group this privilege, you can simply add them to the **CS Administrators** group.</span></span>

<span data-ttu-id="2a0bf-215">通过将用户添加到对应于每个角色的基础 Active Directory 组，可向用户提供多个 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-215">A user can be given multiple RBAC roles by being added to the underlying Active Directory groups that correspond to each role.</span></span>

<span data-ttu-id="2a0bf-216">请注意，当你创建一个角色时，后来添加到基础 Active Directory 组的用户将获得该角色的能力。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-216">Note that when you create a role, users who are later added to the underlying Active Directory group gain the abilities of that role.</span></span>

</div>

<div>

## <a name="modifying-the-abilities-of-a-role"></a><span data-ttu-id="2a0bf-217">修改角色的功能</span><span class="sxs-lookup"><span data-stu-id="2a0bf-217">Modifying the Abilities of a Role</span></span>

<span data-ttu-id="2a0bf-218">你可以修改角色可以运行的 cmdlet 和脚本的列表。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-218">You can modify the list of cmdlets and scripts that a role can run.</span></span> <span data-ttu-id="2a0bf-219">你可以修改自定义角色可以运行的 cmdlet 和脚本，但只能修改预定义角色的脚本。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-219">You can modify both the cmdlets and scripts that custom roles can run, but you can modify only the scripts for predefined roles.</span></span> <span data-ttu-id="2a0bf-220">您键入的每个 cmdlet 都可以添加、删除或替换 cmdlet 或脚本。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-220">Each cmdlet you type can add, remove, or replace cmdlets or scripts.</span></span>

<span data-ttu-id="2a0bf-221">若要修改角色，请使用 **CsAdminRole** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-221">To modify a role, use the **Set-CsAdminRole** cmdlet.</span></span> <span data-ttu-id="2a0bf-222">以下 cmdlet 删除角色中的一个脚本。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-222">The following cmdlet removes one script from the role.</span></span>

    Set-CsAdminRole -Identity "MyHelpDeskScriptRole" -ScriptModules @{Remove="testScript.ps1"}

</div>

</div>

<div>

## <a name="planning-for-rbac"></a><span data-ttu-id="2a0bf-223">制定 RBAC 计划</span><span class="sxs-lookup"><span data-stu-id="2a0bf-223">Planning for RBAC</span></span>

<span data-ttu-id="2a0bf-224">对于要针对 Lync Server 部署获得任何类型的管理权限的每个人，请考虑他们需要执行的任务，然后将它们分配给其作业所需的最低权限和作用域角色。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-224">For each person who is to be given any kind of administrative rights for your Lync Server deployment, consider exactly which tasks they need to perform, then assign them to roles with the least privilege and scope necessary for their job.</span></span> <span data-ttu-id="2a0bf-225">如有必要，你可以使用 **CsAdminRole** cmdlet 创建一个新角色，其中仅包含此人员的任务所需的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-225">If necessary, you can use the **Set-CsAdminRole** cmdlet to create a new role with only the cmdlets necessary for this person’s tasks.</span></span>

<span data-ttu-id="2a0bf-226">具有 CsAdministrator 角色的用户可以创建所有类型的角色，包括基于 CsAdministrator 的角色，并为用户分配用户。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-226">Users who have the CsAdministrator role can create all types of roles, including roles based on CsAdministrator, and assign users to them.</span></span> <span data-ttu-id="2a0bf-227">最佳做法是将 CsAdministrator 角色分配给一组非常小的受信任的用户。</span><span class="sxs-lookup"><span data-stu-id="2a0bf-227">The best practice is to assign the CsAdministrator role to a very small set of trusted users.</span></span>

<span data-ttu-id="2a0bf-228"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a0bf-228"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

