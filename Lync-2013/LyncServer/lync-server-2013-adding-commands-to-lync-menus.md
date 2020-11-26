---
title: Lync Server 2013：将命令添加到 Lync 菜单
description: Lync Server 2013：将命令添加到 Lync 菜单。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding commands to Lync menus
ms:assetid: a8443bc2-e234-4022-870a-00700f38b1ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412788(v=OCS.15)
ms:contentKeyID: 48185091
ms.date: 04/11/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ed4d62d085eaf115d107244ae50a7cc69e0aacd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439238"
---
# <a name="adding-commands-to-lync-menus-in-lync-server-2013"></a><span data-ttu-id="93966-103">在 Lync Server 2013 中将命令添加到 Lync 菜单</span><span class="sxs-lookup"><span data-stu-id="93966-103">Adding commands to Lync menus in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93966-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93966-104">

<span> </span></span></span>

<span data-ttu-id="93966-105">_**主题上次修改时间：** 2016-04-11_</span><span class="sxs-lookup"><span data-stu-id="93966-105">_**Topic Last Modified:** 2016-04-11_</span></span>

<span data-ttu-id="93966-106">你可以将自定义命令添加到 Lync 2013 菜单，并将 SIP 统一资源标识符 (URI) 当前用户和所选联系人添加到自定义命令启动的应用程序。</span><span class="sxs-lookup"><span data-stu-id="93966-106">You can add custom commands to Lync 2013 menus and pass the SIP Uniform Resource Identifier (URI) of the current user and selected contacts to the application that the custom command starts.</span></span>

<span data-ttu-id="93966-107">你添加的自定义命令可以显示在以下一个或多个菜单中：</span><span class="sxs-lookup"><span data-stu-id="93966-107">The custom commands that you add can appear on one or more of the following menus:</span></span>

  - <span data-ttu-id="93966-108">Lync 主窗口中的菜单栏上的 "工具" 菜单</span><span class="sxs-lookup"><span data-stu-id="93966-108">The Tools menu, on the menu bar in the Lync main window</span></span>

  - <span data-ttu-id="93966-109">联系人列表中联系人的快捷菜单</span><span class="sxs-lookup"><span data-stu-id="93966-109">The shortcut menu for contacts in the Contacts list</span></span>

  - <span data-ttu-id="93966-110">对话窗口中的 "更多选项" 菜单</span><span class="sxs-lookup"><span data-stu-id="93966-110">The More Options menu, in the Conversation window</span></span>

  - <span data-ttu-id="93966-111">对话窗口参与者列表中列出的人员的快捷菜单</span><span class="sxs-lookup"><span data-stu-id="93966-111">The shortcut menu for people listed in the Conversation window participant list</span></span>

  - <span data-ttu-id="93966-112">联系人卡片中的 "选项" 菜单</span><span class="sxs-lookup"><span data-stu-id="93966-112">The options menu in a contact card</span></span>

<span data-ttu-id="93966-113">你可以为两种类型的应用程序定义自定义命令，即执行以下任一操作的应用程序：</span><span class="sxs-lookup"><span data-stu-id="93966-113">You can define custom commands for two types of applications—applications that do either of the following:</span></span>

  - <span data-ttu-id="93966-114">仅应用于当前用户并在本地计算机上启动。</span><span class="sxs-lookup"><span data-stu-id="93966-114">Apply only to the current user and are started on the local computer.</span></span>

  - <span data-ttu-id="93966-115">涉及其他用户（如联机协作程序），并且必须在每个用户的计算机上启动。</span><span class="sxs-lookup"><span data-stu-id="93966-115">Involve additional users, such as an online collaboration program, and must be started on each user's computer.</span></span>

<span data-ttu-id="93966-116">可通过以下方式调用自定义命令：</span><span class="sxs-lookup"><span data-stu-id="93966-116">The custom command can be invoked in the following ways:</span></span>

  - <span data-ttu-id="93966-117">选择一个或多个用户，然后选择 "自定义" 命令。</span><span class="sxs-lookup"><span data-stu-id="93966-117">Select one or more users, and then choose the custom command.</span></span>

  - <span data-ttu-id="93966-118">启动两方或多方对话，然后选择 "自定义" 命令。</span><span class="sxs-lookup"><span data-stu-id="93966-118">Start a two-party or multiparty conversation, and then choose the custom command.</span></span>

<div>

## <a name="to-add-a-custom-command"></a><span data-ttu-id="93966-119">添加自定义命令</span><span class="sxs-lookup"><span data-stu-id="93966-119">To add a custom command</span></span>

<span data-ttu-id="93966-120">使用下表中的注册表设置将命令添加到菜单。</span><span class="sxs-lookup"><span data-stu-id="93966-120">Use the registry settings in the following table to add a command to the menus.</span></span> <span data-ttu-id="93966-121">这些条目放置在注册表中的以下位置之一：</span><span class="sxs-lookup"><span data-stu-id="93966-121">These entries are placed in the registry at one of the following locations:</span></span>

  - <span data-ttu-id="93966-122">对于32位操作系统： HKEY \_ 本地 \_ 计算机 \\ 软件 \\ Microsoft \\ Office \\ 15.0 \\ Lync \\ SessionManager \\ 应用</span><span class="sxs-lookup"><span data-stu-id="93966-122">For 32bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

  - <span data-ttu-id="93966-123">对于64位操作系统： HKEY \_ LOCAL \_ MACHINE \\ 软件 \\ Wow6432Node \\ Microsoft \\ Office \\ 15.0 \\ Lync \\ SessionManager \\ 应用</span><span class="sxs-lookup"><span data-stu-id="93966-123">For 64bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

### <a name="custom-command-registry-entries"></a><span data-ttu-id="93966-124">自定义命令注册表项</span><span class="sxs-lookup"><span data-stu-id="93966-124">Custom Command Registry Entries</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93966-125">名称</span><span class="sxs-lookup"><span data-stu-id="93966-125">Name</span></span></th>
<th><span data-ttu-id="93966-126">类型</span><span class="sxs-lookup"><span data-stu-id="93966-126">Type</span></span></th>
<th><span data-ttu-id="93966-127">数据</span><span class="sxs-lookup"><span data-stu-id="93966-127">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93966-128">名称</span><span class="sxs-lookup"><span data-stu-id="93966-128">Name</span></span></p></td>
<td><p><span data-ttu-id="93966-129">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="93966-129">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="93966-130">显示在菜单上的应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="93966-130">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93966-131">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="93966-131">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="93966-132">长</span><span class="sxs-lookup"><span data-stu-id="93966-132">DWORD</span></span></p></td>
<td><p><span data-ttu-id="93966-133">0 = 默认的可执行 () </span><span class="sxs-lookup"><span data-stu-id="93966-133">0 = Executable (default)</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="93966-134">需要 ApplicationInstallPath。</span><span class="sxs-lookup"><span data-stu-id="93966-134">Requires ApplicationInstallPath.</span></span>


</div>
<p><span data-ttu-id="93966-135">1 = 协议</span><span class="sxs-lookup"><span data-stu-id="93966-135">1 = Protocol</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93966-136">ApplicationInstallPath</span><span class="sxs-lookup"><span data-stu-id="93966-136">ApplicationInstallPath</span></span></p></td>
<td><p><span data-ttu-id="93966-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="93966-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="93966-138">可执行文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="93966-138">Full path of the executable.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="93966-139">如果 ApplicationType 为 0 (可执行文件) ，则必须指定。</span><span class="sxs-lookup"><span data-stu-id="93966-139">Must be specified if ApplicationType is 0 (Executable).</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93966-140">路径</span><span class="sxs-lookup"><span data-stu-id="93966-140">Path</span></span></p></td>
<td><p><span data-ttu-id="93966-141">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="93966-141">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="93966-142">要与任何参数一起启动的完整路径，包括默认参数 <em>% user id%</em> 和 <em>% contact id%</em>。</span><span class="sxs-lookup"><span data-stu-id="93966-142">Full path to be started along with any parameters, including the default parameters <em>%user-id%</em> and <em>%contact-id%</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93966-143">SessionType</span><span class="sxs-lookup"><span data-stu-id="93966-143">SessionType</span></span></p></td>
<td><p><span data-ttu-id="93966-144">长</span><span class="sxs-lookup"><span data-stu-id="93966-144">DWORD</span></span></p></td>
<td><p><span data-ttu-id="93966-145">0 = 本地会话。</span><span class="sxs-lookup"><span data-stu-id="93966-145">0 = Local session.</span></span> <span data-ttu-id="93966-146">在本地计算机上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="93966-146">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="93966-147">1 = 两方会话 (默认) 。</span><span class="sxs-lookup"><span data-stu-id="93966-147">1 = Two-party session (default).</span></span> <span data-ttu-id="93966-148">Lync 2013 在本地启动应用程序，然后将桌面通知发送给另一个用户。</span><span class="sxs-lookup"><span data-stu-id="93966-148">Lync 2013 starts the application locally and then sends a desktop notification to the other user.</span></span> <span data-ttu-id="93966-149">其他用户单击通知以在其计算机上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="93966-149">The other user clicks the notification to start the application on their computer.</span></span></p>
<p><span data-ttu-id="93966-150">2 = 多方会话。</span><span class="sxs-lookup"><span data-stu-id="93966-150">2 = Multiparty session.</span></span> <span data-ttu-id="93966-151">Lync 2013 在本地启动应用程序，然后向其他用户发送桌面通知。</span><span class="sxs-lookup"><span data-stu-id="93966-151">Lync 2013 starts the application locally and then sends desktop notifications to the other users.</span></span> <span data-ttu-id="93966-152">其他用户单击通知以在其计算机上启动指定的应用程序。</span><span class="sxs-lookup"><span data-stu-id="93966-152">The other user clicks the notification to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93966-153">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="93966-153">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="93966-154">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="93966-154">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="93966-155">将显示此命令的菜单的列表，用分号分隔。</span><span class="sxs-lookup"><span data-stu-id="93966-155">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="93966-156">可能的值：</span><span class="sxs-lookup"><span data-stu-id="93966-156">Possible values are:</span></span></p>
<p><span data-ttu-id="93966-157">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="93966-157">MainWindowActions</span></span></p>
<p><span data-ttu-id="93966-158">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="93966-158">MainWindowRightClick</span></span></p>
<p><span data-ttu-id="93966-159">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="93966-159">ConversationWindowActions</span></span></p>
<p><span data-ttu-id="93966-160">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="93966-160">ConversationWindowRightClick</span></span></p>
<p><span data-ttu-id="93966-161">ContactCardMenu</span><span class="sxs-lookup"><span data-stu-id="93966-161">ContactCardMenu</span></span></p>
<p><span data-ttu-id="93966-162">如果未定义 ExtensibleMenu，则使用 MainWindowRightClick 和 ConversationWindowActions 的默认值。</span><span class="sxs-lookup"><span data-stu-id="93966-162">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93966-163">例如，下面的注册表编辑器 (。REG) 文件显示将 Contoso Sales Contact Manager 菜单项添加到对话窗口中的 "操作" 菜单的结果：</span><span class="sxs-lookup"><span data-stu-id="93966-163">For example, the following Registry Editor (.REG) file shows the results of adding a Contoso Sales Contact Manager menu item to Actions menu in the Conversation window:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Lync\SessionManager\Apps\{1F9F07C6-7E0B-462B-AAD7-98C6DBEA8F69}]
    "Name"="Contoso Sales Contact Manager"
    "HelpMessage"="The Contoso Sales Contact Manager is not installed. Contact the Help Desk for more information."
    "ApplicationType"=dword:00000000
    "ApplicationInstallPath"="C:\\cscm.exe"
    "Path"="C:\\cscm.exe %user-id% %contact-id%"
    "SessionType"=dword:00000001
    "ExtensibleMenu"="ConversationWindowActions;MainWindowRightClick"

</div>

<div>

## <a name="to-access-a-custom-command"></a><span data-ttu-id="93966-164">访问自定义命令</span><span class="sxs-lookup"><span data-stu-id="93966-164">To access a custom command</span></span>

<span data-ttu-id="93966-165">若要在添加自定义命令后访问它，请根据你定义的 ExtensibleMenu 值执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="93966-165">To access a custom command after it is added, do one of the following, depending on the ExtensibleMenu values that you define:</span></span>

  - <span data-ttu-id="93966-166">**MainWindowActions**   在 Lync 主窗口中，单击 " **工具**"，然后单击您的自定义命令。</span><span class="sxs-lookup"><span data-stu-id="93966-166">**MainWindowActions**   In the Lync main window, click **Tools**, and then click your custom command.</span></span>

  - <span data-ttu-id="93966-167">**MainWindowRightClick**   在 Lync 主窗口中，右键单击某个联系人，然后单击您的自定义命令。</span><span class="sxs-lookup"><span data-stu-id="93966-167">**MainWindowRightClick**   In the Lync main window, right-click a contact, and then click your custom command.</span></span>

  - <span data-ttu-id="93966-168">**ConversationWindowActions**   在对话窗口中，单击 " **更多选项** " 图标，然后单击您的自定义命令。</span><span class="sxs-lookup"><span data-stu-id="93966-168">**ConversationWindowActions**   In the Conversation window, click the **More Options** icon, and then click your custom command.</span></span>

  - <span data-ttu-id="93966-169">**ConversationWindowRightClick**   在对话窗口中，右键单击联系人姓名，然后单击您的自定义命令。</span><span class="sxs-lookup"><span data-stu-id="93966-169">**ConversationWindowRightClick**   In the Conversation window, right-click a contact name, and then click your custom command.</span></span>

<span data-ttu-id="93966-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93966-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

