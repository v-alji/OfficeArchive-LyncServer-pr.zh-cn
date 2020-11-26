---
title: 迁移过程 - 详细信息
description: 迁移流程-详细信息。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration process - details
ms:assetid: ca7e352c-9bde-47d9-8273-5cf2fdfdfe7e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205264(v=OCS.15)
ms:contentKeyID: 48185412
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8ecc5f23a328aef7cc65ad84e28dbb629d44b91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438601"
---
# <a name="migration-process---details"></a><span data-ttu-id="8d3e3-103">迁移过程 - 详细信息</span><span class="sxs-lookup"><span data-stu-id="8d3e3-103">Migration process - details</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d3e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d3e3-104">

<span> </span></span></span>

<span data-ttu-id="8d3e3-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="8d3e3-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="8d3e3-106">使用以下先决条件和详细步骤将 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天迁移到 Lync Server 2013、持久聊天服务器。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-106">Use the following prerequisites and detailed steps to migrate either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span>

<div>

## <a name="prerequisites-for-migration"></a><span data-ttu-id="8d3e3-107">迁移的先决条件</span><span class="sxs-lookup"><span data-stu-id="8d3e3-107">Prerequisites for Migration</span></span>

<span data-ttu-id="8d3e3-108">在将 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天迁移到 Lync Server 2013、持久聊天服务器之前，请确保您已满足以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-108">Be sure that you’ve met the following prerequisites before migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span>

1.  <span data-ttu-id="8d3e3-109">至少部署一个 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-109">Deploy at least one Lync Server 2013 pool.</span></span> <span data-ttu-id="8d3e3-110">如果你有多个 Lync Server 2013 池，请确定哪个 Lync Server 2013 池将成为新 Lync Server 2013 持久聊天服务器池的主池。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-110">If you have multiple Lync Server 2013 pools, decide which Lync Server 2013 pool will be the home pool for the new Lync Server 2013 Persistent Chat Server pool.</span></span>

2.  <span data-ttu-id="8d3e3-111">安装 Lync Server 2013 持久聊天服务器池。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-111">Install the Lync Server 2013, Persistent Chat Server pool.</span></span> <span data-ttu-id="8d3e3-112">它将为空 (没有类别、会议室或外接) 。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-112">It will be empty (no categories, rooms, or add-ins).</span></span> <span data-ttu-id="8d3e3-113">在迁移旧版类别、会议室或外接程序之前，可以在 Lync Server 2013 的持久聊天服务器部署中创建会议室、类别或加载项。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-113">Before you migrate your legacy categories, rooms, or add-ins, you can create rooms, categories, or add-ins in your Lync Server 2013, Persistent Chat Server deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8d3e3-114">请注意，这些新创建的项目可能会与你迁移的旧版项目发生冲突。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-114">Be aware that these newly created items may conflict with legacy items that you migrate.</span></span> <span data-ttu-id="8d3e3-115">避免任何命名冲突;否则，在迁移旧数据时，它们将被覆盖。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-115">Avoid any naming conflicts; otherwise, they will be overwritten when the legacy data is migrated.</span></span>

    
    </div>

</div>

<div>

## <a name="preparing-the-source-data-for-migration"></a><span data-ttu-id="8d3e3-116">为迁移准备源数据</span><span class="sxs-lookup"><span data-stu-id="8d3e3-116">Preparing the Source Data for Migration</span></span>

<span data-ttu-id="8d3e3-117">执行以下步骤来正确准备要迁移的源数据。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-117">Perform the following steps to properly prepare your source data for migration.</span></span>

1.  <span data-ttu-id="8d3e3-118">备份 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 群组聊天的源数据库。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-118">Back up the source databases for either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat.</span></span> <span data-ttu-id="8d3e3-119">有关备份 SQL Server 的详细信息，请参阅 "备份概述 (SQL Server) " <https://go.microsoft.com/fwlink/p/?linkid=254851> 。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-119">For details about backing up SQL Server, see "Backup Overview (SQL Server)" at <https://go.microsoft.com/fwlink/p/?linkid=254851>.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8d3e3-120">Active Directory 域服务应该是相同的。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-120">Active Directory Domain Services should be the same.</span></span> <span data-ttu-id="8d3e3-121">作为迁移的一个条件，在不同的 Active Directory 林中) 中，不能迁移到不同部署 (中的池。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-121">As a condition for migration, you cannot migrate to a pool in a different deployment (specifically, in a different Active Directory forest).</span></span>

    
    </div>

2.  <span data-ttu-id="8d3e3-122">检查 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天聊天室和类别配置。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-122">Inspect your Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat chat rooms and category configuration.</span></span> <span data-ttu-id="8d3e3-123">在现有旧版部署中对类别、会议室或外接程序所做的任何更改都将由群组聊天管理员工具完成。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-123">Any changes to categories, rooms, or add-ins in your existing legacy deployment will be done by the Group Chat Admin Tool.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="8d3e3-124">Lync server 2013 中的类别、会议室或加载项的任何更改都是由 Lync Server 控制面板或 Windows PowerShell cmdlet 执行的，持久聊天服务器部署。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-124">Any changes to categories, rooms, or add-ins in your Lync Server 2013, Persistent Chat Server deployment are performed by the Lync Server Control Panel or Windows PowerShell cmdlets.</span></span>

    
    </div>
    
    <span data-ttu-id="8d3e3-125">请按照以下步骤准备旧版系统进行迁移。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-125">Follow these steps to prepare your legacy system for migration.</span></span>
    
    1.  <span data-ttu-id="8d3e3-126">持久性聊天服务器支持单个级别的类别，不同类别的深度分层集。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-126">Persistent Chat Server supports a single level of categories, unlike a deep hierarchical set of categories.</span></span> <span data-ttu-id="8d3e3-127">迁移后，子类别将以完整的父类别名称作为前缀。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-127">After migration, the subcategories are prefixed with full parent category names.</span></span> <span data-ttu-id="8d3e3-128">你可能希望简化和平展你的现有类别结构，以便生成的结构满足你的要求。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-128">You might want to simplify and flatten your existing category structure so that the resulting structure meets your requirements.</span></span>
    
    2.  <span data-ttu-id="8d3e3-129">验证根类别的 **经理** 。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-129">Verify the **Managers** at the root Category.</span></span> <span data-ttu-id="8d3e3-130">如果此级别上存在任何经理，则将在迁移后将这些用户添加为 **所有会议室的管理员** 。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-130">If any Managers exist at this level, these users will be added as **Managers to all rooms** after migration.</span></span> <span data-ttu-id="8d3e3-131">如果这不是您的组织的要求，您需要从根类别中删除这些经理。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-131">If this is not a requirement for your organization, you need to remove these Managers from the root Category.</span></span>
    
    3.  <span data-ttu-id="8d3e3-132">验证房间名称的长度。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-132">Verify the length of room names.</span></span> <span data-ttu-id="8d3e3-133">迁移后，由于 "简化类别" 结构，如果子类别中存在会议室，则它们的前缀为完整的父类别名称。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-133">After migration, due to simplified category structures, if the rooms exist under a child category, they are prefixed with full parent category names.</span></span> <span data-ttu-id="8d3e3-134">命名限制为256个字符，包括父类别名称。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-134">The naming limit is 256 characters, including parent category names.</span></span> <span data-ttu-id="8d3e3-135">必须验证房间名称的长度，如果这些名称太长，可能会缩短长度。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-135">You must verify the length of the room names and possibly shorten the length, if they are too long.</span></span>
    
    4.  <span data-ttu-id="8d3e3-136">在 Lync Server 2013 中，如果 "类别 **邀请** 设置" 设置为 "true"，则可以选择 "真" 或 "假"，以在该类别下对聊天室的邀请进行选择。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-136">In Lync Server 2013, if the category **invitations** settings are set to true, you can choose true or false for invitations to rooms under that category.</span></span> <span data-ttu-id="8d3e3-137">但是，如果 "类别邀请" 设置设置为 "false"，则该类别下的会议室将会关闭邀请。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-137">However if the category invitations settings are set to false, rooms under that category have invitations turned off.</span></span> <span data-ttu-id="8d3e3-138">在迁移之前，如果您希望在特定类别下) 存在会议室 (s，则必须重置您的旧版 Lync 服务器组聊天服务器版本中的邀请设置。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-138">Before migration, you must reset the invitation settings in your legacy Lync Server Group Chat Server version, if you want room(s) to exist under a specific category.</span></span> <span data-ttu-id="8d3e3-139">否则，在迁移期间，Lync Server 2013 将显示警告，并将聊天室设置为默认值 false。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-139">Otherwise, during migration, Lync Server 2013 displays warnings and sets rooms to the default value of false.</span></span>
    
    5.  <span data-ttu-id="8d3e3-140">如果你在聊天室中使用了文件，则必须在迁移后手动将文件保存到新的持久聊天文件存储。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-140">If you used files in chat rooms, you must XCOPY the files manually to the new Persistent Chat file store after migration.</span></span> <span data-ttu-id="8d3e3-141">这些工具不会执行此操作。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-141">The tools don’t do this.</span></span>
    
    6.  <span data-ttu-id="8d3e3-142">如果您有联盟用户和带联盟用户的聊天室，请注意持久聊天服务器不支持联盟。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-142">If you had federated users and rooms with federated users, be aware that Persistent Chat Server does not support federation.</span></span> <span data-ttu-id="8d3e3-143">将迁移带联盟用户的聊天室;但是，用户本身将无法访问内容，因为不支持联盟访问。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-143">Rooms with federated users will be migrated; however, the users themselves won’t be able to access the content, because federated access is not supported.</span></span>
    
    7.  <span data-ttu-id="8d3e3-144">标识不想迁移的聊天室，并将其标记为 "已禁用"。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-144">Identify those rooms that you do not want to migrate, and mark them as disabled.</span></span>
    
    8.  <span data-ttu-id="8d3e3-145">标识要迁移聊天室内容的截止日期。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-145">Identify the date beyond which you want to migrate the chat room content.</span></span> <span data-ttu-id="8d3e3-146">例如，你可能不希望迁移早于2010年1月1日的消息，因为这些消息可能已过时或与迁移无关。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-146">For example, you may not want to migrate messages earlier than January 1, 2010, because these messages may be obsolete or not relevant for migration.</span></span>

</div>

<div>

## <a name="performing-the-migration"></a><span data-ttu-id="8d3e3-147">执行迁移</span><span class="sxs-lookup"><span data-stu-id="8d3e3-147">Performing the Migration</span></span>

<span data-ttu-id="8d3e3-148">执行以下步骤迁移旧式群组聊天服务器。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-148">Perform the following steps to migrate your legacy Group Chat Server.</span></span>

1.  <span data-ttu-id="8d3e3-149">关闭 Lync Server 2010、群组聊天、Office 通信服务器 2007 R2 群组聊天或 Lync Server 2013、持久聊天服务器服务。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-149">Shut down the Lync Server 2010, Group Chat, Office Communications Server 2007 R2 Group Chat or Lync Server 2013, Persistent Chat Server services.</span></span> <span data-ttu-id="8d3e3-150">必须停止所有服务，因此计划在有足够的停机时间时执行此操作。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-150">All services must be stopped, so plan to do this at a time when there is enough downtime.</span></span> <span data-ttu-id="8d3e3-151">如前面所述，请确保备份当前的群组聊天数据库。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-151">As previously described, make sure to back up your current Group Chat database.</span></span>

2.  <span data-ttu-id="8d3e3-152">以永久聊天管理员 RBAC 角色的成员身份运行 Windows PowerShell **Export CsPersistentChatData** Cmdlet (CsPersistentChatAdministrator) 。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-152">Run the Windows PowerShell **Export-CsPersistentChatData** cmdlet as a member of the Persistent Chat administrator RBAC role (CsPersistentChatAdministrator).</span></span> <span data-ttu-id="8d3e3-153">有关导出/导入 cmdlet 的详细信息，请参阅 [在 Lync server 2013 中使用 Windows PowerShell cmdlet 对持久聊天服务器配置进行故障排除](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md)。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-153">For details about the export/import cmdlets, see [Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md).</span></span>
    
    <span data-ttu-id="8d3e3-154">检查导出的内容。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-154">Inspect the exported contents.</span></span>

3.  <span data-ttu-id="8d3e3-155">准备导入之前，请关闭 Lync Server 2013、持久聊天服务器服务。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-155">Before you’re ready to import, shut down Lync Server 2013, Persistent Chat Server services.</span></span> <span data-ttu-id="8d3e3-156">需要停止所有服务，因此计划在有足够的停机时间时执行此操作。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-156">All services need to be stopped, so plan to do this at a time when there is enough downtime.</span></span>

4.  <span data-ttu-id="8d3e3-157">如果在迁移之前在 Lync Server 2013 部署中创建了任何类别、会议室或加载项，请执行持久聊天数据库的备份。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-157">Perform a backup of the Persistent Chat database if you had created any categories, rooms, or add-ins in your Lync Server 2013 deployment before the migration.</span></span> <span data-ttu-id="8d3e3-158">导出/导入过程将能够将旧数据合并到 Lync Server 2013 部署中，但你需要备份数据库以防意外覆盖内容 (例如，如果仍然存在命名冲突) 。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-158">The export/import process will be able to merge the legacy data into the Lync Server 2013 deployment, but you’ll want to back up the database in case that content is inadvertently overwritten (for example, if naming conflicts still exist).</span></span>

5.  <span data-ttu-id="8d3e3-159">运行 Windows PowerShell **Import-CsPersistentChatData** cmdlet (导入工具) ，使用 **WhatIf** 命令使用已迁移的数据填充持久聊天服务器池的后端服务器。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-159">Run the Windows PowerShell **Import-CsPersistentChatData** cmdlet (import tool), with a **WhatIf** command to populate the Back End Server of the Persistent Chat Server pool with migrated data.</span></span> <span data-ttu-id="8d3e3-160">过程中会发生某些转换，以适应简化的管理模型。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-160">Some conversions happen in the process to accommodate the simplified administration model.</span></span> <span data-ttu-id="8d3e3-161">修复出现的任何错误或警告。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-161">Fix any errors or warnings that appear.</span></span>

6.  <span data-ttu-id="8d3e3-162">作为持久聊天管理员 RBAC 角色的成员 (CsPersistentChatAdministrator) 运行持久聊天服务器 Windows PowerShell **Import CsPersistentChatData** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-162">Run the Persistent Chat Server Windows PowerShell **Import-CsPersistentChatData** cmdlet as a member of the Persistent Chat administrator RBAC role (CsPersistentChatAdministrator).</span></span> <span data-ttu-id="8d3e3-163">有关导出/导入 cmdlet 的详细信息，请参阅 [在 Lync server 2013 中使用 Windows PowerShell cmdlet 对持久聊天服务器配置进行故障排除](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md)。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-163">For details about the export/import cmdlets, see [Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md).</span></span>

7.  <span data-ttu-id="8d3e3-164">必须将所有上载的文件作为 (整个文件夹的所有上载文件) 到新的 Lync Server 2013、持久聊天文件存储。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-164">You must XCOPY all uploaded files (the entire folder) to the new Lync Server 2013, Persistent Chat file store.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8d3e3-165">Lync 2013 (客户端) 不支持上载或查看聊天室中的文件。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-165">The Lync 2013 (client) does not support uploading or viewing files in chat rooms.</span></span> <span data-ttu-id="8d3e3-166">您仍然可以使用旧客户端来发布和查看聊天室中的文件。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-166">You can still use the legacy client to post and view files in the room.</span></span>

    
    </div>

8.  <span data-ttu-id="8d3e3-167">将 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 群组聊天查找服务器 URI 移植到 Lync Server 2013、持久聊天服务器联系人对象。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-167">Port the Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat Lookup Server URI to the Lync Server 2013, Persistent Chat Server contact object.</span></span> <span data-ttu-id="8d3e3-168">如果您的 Lync 2010 群组聊天或 Office Communicator 2007 R2 组聊天客户端需要连接到最新的 Lync 2013、持久聊天 (客户端) 在没有任何客户端配置更改的情况下进行迁移，则需要执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="8d3e3-168">The following steps are required if either your Lync 2010 Group Chat or Office Communicator 2007 R2 Group Chat clients need to connect to the latest Lync 2013, Persistent Chat (client) after migration without any client-side configuration changes:</span></span>
    
      - <span data-ttu-id="8d3e3-169">删除 "ocschat@ \<domainName\> .Com 查找服务器" 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-169">Delete the ocschat@\<domainName\>.com Lookup Server user account.</span></span> <span data-ttu-id="8d3e3-170">这用于指向 Lync Server 2010 中的查找服务，群组聊天。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-170">This was used to point to the Lookup Service in Lync Server 2010, Group Chat.</span></span> <span data-ttu-id="8d3e3-171">你可以在以后卸载该池并删除受信任的条目。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-171">You can uninstall the pool and remove trusted entries later.</span></span>
    
      - <span data-ttu-id="8d3e3-172">通过运行具有相同 SIP URI 的 Windows PowerShell cmdlet **CsPersistentChatEndpoint**，创建旧终结点 (持久聊天服务器联系人对象) ，以便在重新启动服务时，旧客户端将有效工作。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-172">Create a legacy endpoint (Persistent Chat Server contact object) by running the Windows PowerShell cmdlet, **New-CsPersistentChatEndpoint**, with the identical SIP URI so that the legacy client will work effectively when the service is restarted.</span></span>
    
    <span data-ttu-id="8d3e3-173">强制执行的迁移过程已完成。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-173">The mandatory migration process is complete at this point.</span></span> <span data-ttu-id="8d3e3-174">Lync 2010 群组聊天 (客户) 或 Office Communicator 2007 R2 群组聊天 (客户) 端现在可以透明地连接到新的持久聊天服务器池。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-174">Lync 2010 Group Chat (clients) or Office Communicator 2007 R2 Group Chat (clients) can connect to the new Persistent Chat Server pool now, transparently.</span></span>
    
    <span data-ttu-id="8d3e3-175">对于 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 群组聊天，请按照以下附加解除授权步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-175">Follow these additional decommissioning steps for Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat.</span></span>

9.  <span data-ttu-id="8d3e3-176">通过打开新的持久聊天服务器池中的所有计算机启动持久聊天服务器服务。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-176">Start the Persistent Chat Server services by turning on all computers in the new Persistent Chat Server pool.</span></span>

10. <span data-ttu-id="8d3e3-177">使用 Lync Server "控制面板" 和 "Windows PowerShell" cmdlet 验证数据是否已成功迁移。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-177">Use the Lync Server Control Panel and Windows PowerShell cmdlets to verify that the data has migrated successfully.</span></span>

11. <span data-ttu-id="8d3e3-178">从群组聊天服务器池中的计算机卸载 Lync 2010 组聊天或 Office Communicator 2007 R2 组聊天。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-178">Uninstall Lync 2010 Group Chat or Office Communicator 2007 R2 Group Chat from the computers in the Group Chat Server pool.</span></span>

12. <span data-ttu-id="8d3e3-179">使用 Windows PowerShell cmdlet 删除受信任的应用程序和受信任的应用程序池。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-179">Delete the trusted application and trusted application pool using Windows PowerShell cmdlets.</span></span> <span data-ttu-id="8d3e3-180">此操作将从中央管理存储以及关联的受信任服务条目 (TSEs) 从 Active Directory 中删除这些项目。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-180">This deletes these items from the Central Management store and the associated Trusted Service Entries (TSEs) from the Active Directory.</span></span> <span data-ttu-id="8d3e3-181">或者，此步骤的工作原理是使用拓扑生成器 (受信任的应用程序/池有一个专用节点，也) 。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-181">Alternatively, this step works by using the Topology Builder (the trusted applications/pools have a dedicated node there, also).</span></span>

13. <span data-ttu-id="8d3e3-182">现在，您可以通过新客户端开始启用持久聊天服务器功能。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-182">You can now begin to enable Persistent Chat Server functionality through the new clients.</span></span> <span data-ttu-id="8d3e3-183">有关启用持久聊天服务器的详细信息，请参阅 [在 Lync server 2013 中部署持久聊天服务器](lync-server-2013-deploying-persistent-chat-server.md)。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-183">For details about enabling Persistent Chat Server, see [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8d3e3-184">Lync Server 2013 支持多个持久聊天服务器池。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-184">Lync Server 2013 supports multiple Persistent Chat Server pools.</span></span> <span data-ttu-id="8d3e3-185">但是，我们支持将 Lync 2010 组聊天或 Office 通信服务器 2007 R2 &nbsp; 组聊天池迁移到单个 Lync server 2013、持久聊天服务器池。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-185">However, we support migrating a Lync 2010 Group Chat or Office Communications Server 2007 R2&nbsp;Group Chat pool to a single Lync Server 2013, Persistent Chat Server pool.</span></span> <span data-ttu-id="8d3e3-186">你可以在你的部署中添加其他新持久聊天服务器池以满足法规需求 (例如，将数据保留在给定地理区域内) 。</span><span class="sxs-lookup"><span data-stu-id="8d3e3-186">You can add additional new Persistent Chat Server pools in your deployment to meet the regulatory needs (for example, keeping data within a given geography).</span></span>

    
    <span data-ttu-id="8d3e3-187"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d3e3-187"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

