---
title: Lync Server 2013：配置类别
description: Lync Server 2013：配置类别。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure categories
ms:assetid: 4547f514-f0c0-404d-890f-092ddeeac852
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204859(v=OCS.15)
ms:contentKeyID: 48184033
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1342ea0f5ee32284a32ac0dcc8ab3d370bb1dd91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434016"
---
# <a name="configure-categories-in-lync-server-2013"></a><span data-ttu-id="314cc-103">在 Lync Server 2013 中配置类别</span><span class="sxs-lookup"><span data-stu-id="314cc-103">Configure categories in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="314cc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="314cc-104">

<span> </span></span></span>

<span data-ttu-id="314cc-105">_**主题上次修改时间：** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="314cc-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="314cc-106">在 Lync Server 2013 控制面板中，你可以使用 **持久聊天** 页面的 "**类别**" 部分配置类别。</span><span class="sxs-lookup"><span data-stu-id="314cc-106">In Lync Server 2013 Control Panel, you can use the **Category** section of the **Persistent Chat** page to configure categories.</span></span> <span data-ttu-id="314cc-107">持久的聊天室类别是用于组织聊天室的逻辑结构。</span><span class="sxs-lookup"><span data-stu-id="314cc-107">A Persistent Chat room category is a logical structure for organizing chat rooms.</span></span> <span data-ttu-id="314cc-108">类别定义一组默认的访问控制列表 (ACL)，以便控制可以创建或加入聊天室的用户和用户组。</span><span class="sxs-lookup"><span data-stu-id="314cc-108">A category defines a default set of access control lists (ACLs) for controlling the users and user groups who may create or join the chat rooms.</span></span> <span data-ttu-id="314cc-109">您还可以使用类别强制在组织中不同部门之间使用信息隔离墙。</span><span class="sxs-lookup"><span data-stu-id="314cc-109">You can use categories enforce ethical walls between different subdivisions within their organizations.</span></span>

<span data-ttu-id="314cc-110">聊天室类别可以包含聊天室，但不包含其他类别。</span><span class="sxs-lookup"><span data-stu-id="314cc-110">Chat room categories may contain chat rooms, but not other categories.</span></span> <span data-ttu-id="314cc-111">每个类别说明了其内容及元数据，比如名称和说明。</span><span class="sxs-lookup"><span data-stu-id="314cc-111">Each category describes its contents with metadata, such as Name and Description.</span></span> <span data-ttu-id="314cc-112">此外，类别还具有可以设置以控制其所拥有聊天室的行为的属性，例如聊天室是否允许执行Invitations或File Uploads操作，或者包含Chat History。</span><span class="sxs-lookup"><span data-stu-id="314cc-112">In addition, the category has properties which can be set to control the behavior of the chat rooms belonging to it, such as if the chat rooms allow Invitations or File Uploads, or contain Chat History.</span></span>

<div>

## <a name="to-configure-categories-for-chat-rooms"></a><span data-ttu-id="314cc-113">配置聊天室的类别</span><span class="sxs-lookup"><span data-stu-id="314cc-113">To configure categories for chat rooms</span></span>

1.  <span data-ttu-id="314cc-114">使用分配给 CsPersistentChatAdministrator 或 CsAdministrator 角色的用户帐户登录您的本地部署中的任一计算机。</span><span class="sxs-lookup"><span data-stu-id="314cc-114">From a user account that is assigned to the CsPersistentChatAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="314cc-115">从 " **开始** " 菜单中，选择 "Lync Server 控制面板" 或打开一个浏览器窗口，然后输入管理员 URL。</span><span class="sxs-lookup"><span data-stu-id="314cc-115">From the **Start** menu, select the Lync Server Control Panel or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="314cc-116">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="314cc-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="314cc-117">你还可以使用 Windows PowerShell cmdlet。</span><span class="sxs-lookup"><span data-stu-id="314cc-117">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="314cc-118">有关详细信息，请参阅在部署文档中 <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">使用 Windows PowerShell Cmdlet 配置持久聊天服务器</A> 。</span><span class="sxs-lookup"><span data-stu-id="314cc-118">For details, see <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

3.  <span data-ttu-id="314cc-119">在左侧导航栏中，单击“**持久聊天**”，然后单击“**类别**”。</span><span class="sxs-lookup"><span data-stu-id="314cc-119">In the left navigation bar, click **Persistent Chat**, and then click **Category**.</span></span>
    
    <span data-ttu-id="314cc-120">对于多个持久聊天服务器池部署，从下拉列表中选择相应的池。</span><span class="sxs-lookup"><span data-stu-id="314cc-120">For multiple Persistent Chat Server pool deployments, select the appropriate pool from the drop-down list.</span></span>

4.  <span data-ttu-id="314cc-121">在“**类别**”页上，单击“**新建**”或“**编辑**”。</span><span class="sxs-lookup"><span data-stu-id="314cc-121">On the **Category** page, click **New** or **Edit**.</span></span>

5.  <span data-ttu-id="314cc-122">在 " **选择服务**" 中，选择与需要在其中创建类别的持久聊天服务器池对应的服务。</span><span class="sxs-lookup"><span data-stu-id="314cc-122">In **Select a Service**, select the service corresponding to the Persistent Chat Server pool on which the category needs to be created.</span></span> <span data-ttu-id="314cc-123">该服务是持久聊天服务器池，持久聊天 (客户端) 用于标识该类别所属的池。</span><span class="sxs-lookup"><span data-stu-id="314cc-123">The service is the Persistent Chat Server pool that the Persistent Chat (client) uses to identify which pool the category belongs to.</span></span> <span data-ttu-id="314cc-124">一个类别只能属于一个持久聊天服务器池，不能移到另一个，或与另一个池共享。</span><span class="sxs-lookup"><span data-stu-id="314cc-124">A category can belong to only one Persistent Chat Server pool, and cannot be moved to another one, or shared with another pool.</span></span>

6.  <span data-ttu-id="314cc-125">在“**新建类别**”中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="314cc-125">In **New Category**, do the following:</span></span>
    
    1.  <span data-ttu-id="314cc-126">在“**名称**”中，指定新聊天室类别的名称。</span><span class="sxs-lookup"><span data-stu-id="314cc-126">In **Name**, specify a name for the new room category.</span></span>
    
    2.  <span data-ttu-id="314cc-127">在“**描述**”中，提供有关聊天室类别（例如 Contoso 聊天室类别）的详细描述。</span><span class="sxs-lookup"><span data-stu-id="314cc-127">In **Description**, provide a detailed description for the room category (for example, a room category for Contoso).</span></span>
    
    3.  <span data-ttu-id="314cc-128">要控制是否为属于此类别的聊天室启用邀请，请选中或清除“**启用邀请**”复选框。</span><span class="sxs-lookup"><span data-stu-id="314cc-128">To control whether invitations can be enabled for chat rooms that belong to this category, select or clear the **Enable invitations** check box.</span></span> <span data-ttu-id="314cc-129">如果选中，则此类别的聊天室将打开或关闭邀请；如果清除，则不允许此类别的聊天室具有邀请。</span><span class="sxs-lookup"><span data-stu-id="314cc-129">If selected, rooms in this category may have invitations on or off; if cleared, the rooms in this category are not allowed to have invitations.</span></span> <span data-ttu-id="314cc-130">如果会议室有邀请，则在将新成员添加到聊天室时，他或她将收到新聊天室在其持久聊天客户端中的通知。</span><span class="sxs-lookup"><span data-stu-id="314cc-130">If a room has invitations on, when a new member is added to a room, he or she gets a notification of the new room in their Persistent Chat client.</span></span>
    
    4.  <span data-ttu-id="314cc-p107">要控制属于此类别的聊天室中的文件上载，请选中或清除“**启用文件上载**”复选框。如果选中，该类别的聊天室可以启用或禁用文件上载；如果清除，则不允许该类别的聊天室执行文件上载操作。</span><span class="sxs-lookup"><span data-stu-id="314cc-p107">To control file uploads in chat rooms belonging to this category, select or clear the **Enable file upload** check box. If selected, the rooms of this category can enable or disable file uploads; if cleared, the rooms of this category are not allowed to have file uploads.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="314cc-133">由于自定义应用程序或以前的群组聊天客户端使用 Office 通信服务器 2007 R2 &nbsp; 组聊天服务器或 Lync server 2010，组聊天可将文件发布到聊天室，因此在服务器上强制使用此设置。</span><span class="sxs-lookup"><span data-stu-id="314cc-133">This setting is enforced on the server because custom applications or previous Group Chat clients that use Office Communications Server 2007 R2&nbsp;Group Chat Server or Lync Server 2010, Group Chat can post files to a room.</span></span> <span data-ttu-id="314cc-134">Lync 2013 客户端没有文件上传/下载功能，因此，如果你有纯 Lync 2013 部署或 Lync 2013 客户端，则无法在持久聊天服务器聊天室中发布文件。</span><span class="sxs-lookup"><span data-stu-id="314cc-134">The Lync 2013 client does not have file upload/download capability, so if you have a pure Lync 2013 deployment or Lync 2013 client, it is not possible to post files in a Persistent Chat Server chat room.</span></span>

        
        </div>
    
    5.  <span data-ttu-id="314cc-135">若要控制聊天历史记录，请选中或清除 " **启用聊天历史记录** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="314cc-135">To control chat history, select or clear the **Enable chat history** check box.</span></span> <span data-ttu-id="314cc-136">如果选中，则聊天室聊天内容将变成持久的；否则，将不会保留聊天消息。</span><span class="sxs-lookup"><span data-stu-id="314cc-136">If selected, room chats become persistent; otherwise, chat messages are not persisted.</span></span> <span data-ttu-id="314cc-137">如果启用了合规性，则将按合规性保存聊天室聊天内容，但用户无法访问较早的消息。</span><span class="sxs-lookup"><span data-stu-id="314cc-137">If compliance is enabled, room chats will be saved in compliance, but users will not be able to access older messages.</span></span> <span data-ttu-id="314cc-138">此选项可用于指定为无需保留聊天历史记录的实时、临时协作的聊天室。</span><span class="sxs-lookup"><span data-stu-id="314cc-138">This option can be used for rooms designated for real-time, ad hoc collaborations that don’t need chat history to be persisted.</span></span>

7.  <span data-ttu-id="314cc-139">在“**编辑类别**”中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="314cc-139">In **Edit Category**, do the following:</span></span>
    
      - <span data-ttu-id="314cc-140">在 "允许的成员" 部分 **中，在**" **允许的成员** " 部分中，添加或删除用户和其他 Active Directory 域服务主体 (用户、通讯组、组织单位等) ，允许将这些成员添加为属于该类别的聊天室的成员。</span><span class="sxs-lookup"><span data-stu-id="314cc-140">In **Membership**, in the **Allowed members** section, add or remove users and other Active Directory Domain Services principals (users, distribution groups, organizational units, and so on) that are permitted to be added as members of chat rooms belonging to the category.</span></span> <span data-ttu-id="314cc-141">类别允许的主体可搜索此类别的聊天室（除非隐藏了聊天室，在这种情况下，仅聊天室的成员可在此目录中搜索聊天室）。</span><span class="sxs-lookup"><span data-stu-id="314cc-141">Principals permitted by a category can search for the rooms in the category (unless the room is hidden, in which case only members of the room can search for it in the directory).</span></span>
    
      - <span data-ttu-id="314cc-142">在 "**拒绝成员**" 部分 **中，在**"拒绝的成员" 部分中，添加或删除与从聊天室拒绝的成员关联的用户和其他 Active Directory 主体。</span><span class="sxs-lookup"><span data-stu-id="314cc-142">In **Membership**, in the **Denied members** section, add or remove users and other Active Directory principals associated with members being denied from the room.</span></span>
    
      - <span data-ttu-id="314cc-143">在 " **成员资格**" 部分中，在 " **创建者** " 部分中，添加或删除与类别的 "创建者" 关联的用户和其他 Active Directory 主体。</span><span class="sxs-lookup"><span data-stu-id="314cc-143">In **Membership**, in the **Creators** section, add or remove users and other Active Directory principals associated with creators for the category.</span></span> <span data-ttu-id="314cc-144">创建者是有权创建聊天室并指定聊天室管理员和成员的用户。</span><span class="sxs-lookup"><span data-stu-id="314cc-144">A creator is a user who has permissions to create chat rooms and assign chat room managers and members.</span></span>

8.  <span data-ttu-id="314cc-145">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="314cc-145">Click **Commit**.</span></span>

<span data-ttu-id="314cc-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="314cc-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

