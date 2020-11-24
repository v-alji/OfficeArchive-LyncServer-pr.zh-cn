---
title: 将第三方协作应用程序与 Lync 集成
description: 将第三方协作应用程序与 Lync 集成。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating a third-party collaboration application with Lync
ms:assetid: 00b9312c-b0c8-4f79-8b76-05b2d820e197
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398068(v=OCS.15)
ms:contentKeyID: 48183224
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adbe1abab83a569f581af034fc46abfef4cf819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392385"
---
# <a name="integrating-a-third-party-collaboration-application-with-lync-server-2013"></a><span data-ttu-id="b2392-103">将第三方协作应用程序与 Lync Server 2013 集成</span><span class="sxs-lookup"><span data-stu-id="b2392-103">Integrating a third-party collaboration application with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2392-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2392-104">

<span> </span></span></span>

<span data-ttu-id="b2392-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="b2392-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="b2392-106">你可以通过向注册表添加有关应用程序的信息，将 Lync 2013 与任何第三方联机协作应用程序集成。</span><span class="sxs-lookup"><span data-stu-id="b2392-106">You can integrate Lync 2013 with any third-party online collaboration application by adding information about the application to the registry.</span></span> <span data-ttu-id="b2392-107">您可以使用 Lync 2013 启动在内部服务器、基于 Internet 的服务或两者之间托管的数据会议会话。</span><span class="sxs-lookup"><span data-stu-id="b2392-107">You can use Lync 2013 to start data conferencing sessions hosted on an in-house server, an Internet-based service, or both.</span></span> <span data-ttu-id="b2392-108">可以从 "联系人" 列表或从现有即时消息、语音或视频会话启动协作或数据会议会话。</span><span class="sxs-lookup"><span data-stu-id="b2392-108">The collaboration or data conferencing session can be started from the Contacts list or from an existing instant messaging, voice, or video session.</span></span> <span data-ttu-id="b2392-109">Lync 2013 仅用作启动应用程序的工具。</span><span class="sxs-lookup"><span data-stu-id="b2392-109">Lync 2013 acts only as the vehicle for starting the application.</span></span> <span data-ttu-id="b2392-110">联机协作会话开始后，任何现有 Lync 2013 对话都将保持活动状态。</span><span class="sxs-lookup"><span data-stu-id="b2392-110">Any existing Lync 2013 conversations remain active after the online collaboration session has begun.</span></span>

<span data-ttu-id="b2392-111">以下各部分介绍了如何将 Lync 2013 与基于 Internet 和基于服务器的协作应用程序集成。</span><span class="sxs-lookup"><span data-stu-id="b2392-111">The following sections describe how to integrate Lync 2013 with Internet-based and server-based collaboration applications.</span></span>

<div>

## <a name="integrating-an-internet-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="b2392-112">将 Internet-Based 协作应用程序与 Lync 2013 集成</span><span class="sxs-lookup"><span data-stu-id="b2392-112">Integrating an Internet-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="b2392-113">通常情况下，集成第三方协作应用程序涉及的步骤如下所示：</span><span class="sxs-lookup"><span data-stu-id="b2392-113">Generally, the steps involved in integrating a third-party collaboration application are as follows:</span></span>

1.  <span data-ttu-id="b2392-114">有关应用程序的信息将添加到注册表中。</span><span class="sxs-lookup"><span data-stu-id="b2392-114">Information about the application is added to the registry.</span></span>

2.  <span data-ttu-id="b2392-115">组织者登录 Lync 2013 并选择联系人进行数据共享和协作。</span><span class="sxs-lookup"><span data-stu-id="b2392-115">The organizer signs in to Lync 2013 and selects contacts for data sharing and collaboration.</span></span> <span data-ttu-id="b2392-116">或者，组织者可能已经在对话中，并且决定添加数据会议。</span><span class="sxs-lookup"><span data-stu-id="b2392-116">Or, the organizer may already be in a conversation and decide to add data conferencing.</span></span>

3.  <span data-ttu-id="b2392-117">Lync 2013 读取注册表，启动协作应用程序，然后将自定义 SIP 消息（appINVITE）发送给所选参与者。</span><span class="sxs-lookup"><span data-stu-id="b2392-117">Lync 2013 reads the registry, starts the collaboration application, and then sends a custom SIP message—an appINVITE—to the selected participants.</span></span>

4.  <span data-ttu-id="b2392-118">参与者接受邀请，并在每个人的计算机上启动协作应用程序。</span><span class="sxs-lookup"><span data-stu-id="b2392-118">Participants accept the invitation, and the collaboration application is started on each person’s computer.</span></span> <span data-ttu-id="b2392-119">Lync 2013 使用注册表确定要使用的协作应用程序，然后使用 appINVITE 消息中包含的参数启动该应用程序。</span><span class="sxs-lookup"><span data-stu-id="b2392-119">Lync 2013 uses the registry to determine which collaboration application to use, and then starts that application by using the parameters included in the appINVITE message.</span></span>

<span data-ttu-id="b2392-120">下表介绍了将基于 Internet 的协作应用程序与 Lync 2013 集成所需的注册表项。</span><span class="sxs-lookup"><span data-stu-id="b2392-120">The following table describes the registry entries required to integrate an Internet-based collaboration application with Lync 2013.</span></span> <span data-ttu-id="b2392-121">这些条目放置在注册表中的以下位置：</span><span class="sxs-lookup"><span data-stu-id="b2392-121">These entries are placed in the registry in the following location:</span></span>

  - <span data-ttu-id="b2392-122">HKEY \_ LOCAL \_ MACHINE \\ 软件 \\ Microsoft \\ Office \\ 15.0 \\ Lync \\ SessionManager \\ Apps \\ 参数</span><span class="sxs-lookup"><span data-stu-id="b2392-122">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="b2392-123">基于 Internet 的协作应用程序的注册表项</span><span class="sxs-lookup"><span data-stu-id="b2392-123">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2392-124">名称</span><span class="sxs-lookup"><span data-stu-id="b2392-124">Name</span></span></th>
<th><span data-ttu-id="b2392-125">类型</span><span class="sxs-lookup"><span data-stu-id="b2392-125">Type</span></span></th>
<th><span data-ttu-id="b2392-126">数据</span><span class="sxs-lookup"><span data-stu-id="b2392-126">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2392-127">名称</span><span class="sxs-lookup"><span data-stu-id="b2392-127">Name</span></span></p></td>
<td><p><span data-ttu-id="b2392-128">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-128">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-129">Lync 2013 菜单的应用程序名称。</span><span class="sxs-lookup"><span data-stu-id="b2392-129">The application name for Lync 2013 menus.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2392-130">SmallIcon</span><span class="sxs-lookup"><span data-stu-id="b2392-130">SmallIcon</span></span></p></td>
<td><p><span data-ttu-id="b2392-131">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-131">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-132">指向16像素 x 16 像素图标、BMP 或 PNG 的路径。</span><span class="sxs-lookup"><span data-stu-id="b2392-132">Path to 16-pixel x 16-pixel icon, BMP or PNG.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2392-133">路径</span><span class="sxs-lookup"><span data-stu-id="b2392-133">Path</span></span></p></td>
<td><p><span data-ttu-id="b2392-134">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-134">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-135">用于启动联机协作应用程序的参与者路径。</span><span class="sxs-lookup"><span data-stu-id="b2392-135">Participant path for starting the online collaboration application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2392-136">OriginatorPath</span><span class="sxs-lookup"><span data-stu-id="b2392-136">OriginatorPath</span></span></p></td>
<td><p><span data-ttu-id="b2392-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-138">用于启动联机协作应用程序的组织者路径。</span><span class="sxs-lookup"><span data-stu-id="b2392-138">Organizer path for starting the online collaboration application.</span></span> <span data-ttu-id="b2392-139">此路径可以包含 "参数" 子项中定义的一个或多个自定义参数。</span><span class="sxs-lookup"><span data-stu-id="b2392-139">This path can contain one or more custom parameters as defined in the Parameters subkey.</span></span> <span data-ttu-id="b2392-140">例如， <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span><span class="sxs-lookup"><span data-stu-id="b2392-140">For example, <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2392-141">SessionType</span><span class="sxs-lookup"><span data-stu-id="b2392-141">SessionType</span></span></p></td>
<td><p><span data-ttu-id="b2392-142">长</span><span class="sxs-lookup"><span data-stu-id="b2392-142">DWORD</span></span></p></td>
<td><p><span data-ttu-id="b2392-143">0 = 本地会话。</span><span class="sxs-lookup"><span data-stu-id="b2392-143">0 = Local session.</span></span> <span data-ttu-id="b2392-144">在本地计算机上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="b2392-144">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="b2392-145">1 = 两方会话 (默认) 。</span><span class="sxs-lookup"><span data-stu-id="b2392-145">1 = Two-party session (default).</span></span> <span data-ttu-id="b2392-146">Lync 2013 在本地启动应用程序，然后将系统通知发送给另一个用户。</span><span class="sxs-lookup"><span data-stu-id="b2392-146">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="b2392-147">其他用户单击通知并在其计算机上启动指定的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b2392-147">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="b2392-148">2 = 多方会话。</span><span class="sxs-lookup"><span data-stu-id="b2392-148">2 = Multiparty session.</span></span> <span data-ttu-id="b2392-149">Lync 2013 在本地启动应用程序，然后向其他用户发送系统通知，提示用户在其自己的计算机上启动指定的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b2392-149">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their own computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2392-150">ExensibleMenu</span><span class="sxs-lookup"><span data-stu-id="b2392-150">ExensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="b2392-151">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-151">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-152">将显示此命令的菜单的列表，用分号分隔。</span><span class="sxs-lookup"><span data-stu-id="b2392-152">A list of the menus where this command will appear, separated by semi-colons.</span></span> <span data-ttu-id="b2392-153">可能的值：</span><span class="sxs-lookup"><span data-stu-id="b2392-153">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2392-154">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="b2392-154">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="b2392-155">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="b2392-155">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="b2392-156">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="b2392-156">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="b2392-157">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="b2392-157">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="b2392-158">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="b2392-158">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="b2392-159">如果未定义 ExtensibleMenu，则使用 MainWindowRightClick 和 ConversationWindowActions 的默认值。</span><span class="sxs-lookup"><span data-stu-id="b2392-159">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b2392-160">下表描述了参数的注册表项。</span><span class="sxs-lookup"><span data-stu-id="b2392-160">The following table describes the registry entries for parameters.</span></span> <span data-ttu-id="b2392-161">这些条目位于 HKEY \_ 当前 \_ 用户 \\ 软件 \\ Microsoft \\ Office \\ 15.0 \\ Lync \\ SessionManager \\ 应用 \\ 参数中。</span><span class="sxs-lookup"><span data-stu-id="b2392-161">These entries are place at HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters.</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="b2392-162">基于 Internet 的协作应用程序的注册表项</span><span class="sxs-lookup"><span data-stu-id="b2392-162">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2392-163">名称</span><span class="sxs-lookup"><span data-stu-id="b2392-163">Name</span></span></th>
<th><span data-ttu-id="b2392-164">类型</span><span class="sxs-lookup"><span data-stu-id="b2392-164">Type</span></span></th>
<th><span data-ttu-id="b2392-165">数据</span><span class="sxs-lookup"><span data-stu-id="b2392-165">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2392-166">Param1</span><span class="sxs-lookup"><span data-stu-id="b2392-166">Param1</span></span></p></td>
<td><p><span data-ttu-id="b2392-167">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-167">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-168">在 "标记化格式" 中使用 (<code>%Parm1%</code>) 将特定于用户的值添加到 OriginatorPath 注册表项。</span><span class="sxs-lookup"><span data-stu-id="b2392-168">Used in tokenized format (<code>%Parm1%</code>) to add user-specific values to the OriginatorPath registry key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2392-169">Param2</span><span class="sxs-lookup"><span data-stu-id="b2392-169">Param2</span></span></p></td>
<td><p><span data-ttu-id="b2392-170">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-170">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-171">请参阅 Param1。</span><span class="sxs-lookup"><span data-stu-id="b2392-171">See Param1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2392-172">Param3</span><span class="sxs-lookup"><span data-stu-id="b2392-172">Param3</span></span></p></td>
<td><p><span data-ttu-id="b2392-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-174">请参阅 Param1。</span><span class="sxs-lookup"><span data-stu-id="b2392-174">See Param1.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b2392-175">以下示例注册表设置将 ADatum 协作客户端与 Lync 2013 集成：</span><span class="sxs-lookup"><span data-stu-id="b2392-175">The following example registry settings integrate ADatum Collaboration Client with Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Path"="https://meetingservice.adatum.com/cc/%param1%/meet/%param2%"
    "OriginatorPath"="https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&role=present&pw=%param3%"
    "SessionType"=dword:00000002
    "ApplicationType"=dword:00000001
    "LiveServerIntegration"=dword:00000000
    "Name"="ADatum Online Collaboration Service"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"
    
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Param1"="meetserv"
    "Param2"="admin"
    "Param3"="abcdefg123"

</div>

<div>

## <a name="integrating-a-server-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="b2392-176">将 Server-Based 协作应用程序与 Lync 2013 集成</span><span class="sxs-lookup"><span data-stu-id="b2392-176">Integrating a Server-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="b2392-177">用于从 Lync 2013 中添加用于启动基于服务器的协作应用程序命令的设置与上一节中所述，将 Internet-Based 协作应用程序集成到 Lync 2013。</span><span class="sxs-lookup"><span data-stu-id="b2392-177">The settings to add commands for starting a server-based collaboration application from within Lync 2013 are similar to those described in the previous section, Integrating an Internet-Based Collaboration Application with Lync 2013.</span></span> <span data-ttu-id="b2392-178">但是，OriginatorPath 不是必需的，并且某些值已更改。</span><span class="sxs-lookup"><span data-stu-id="b2392-178">However, the OriginatorPath is not required, and some values are changed.</span></span> <span data-ttu-id="b2392-179">注册表项放置在以下位置：</span><span class="sxs-lookup"><span data-stu-id="b2392-179">Registry entries are placed in the following location:</span></span>

  - <span data-ttu-id="b2392-180">HKEY \_ LOCAL \_ MACHINE \\ 软件 \\ Microsoft \\ Office \\ 15.0 \\ Lync \\ SessionManager \\ Apps \\ 参数</span><span class="sxs-lookup"><span data-stu-id="b2392-180">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-a-server-based-collaboration-application"></a><span data-ttu-id="b2392-181">基于服务器的协作应用程序的注册表项</span><span class="sxs-lookup"><span data-stu-id="b2392-181">Registry Entries for a Server-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2392-182">名称</span><span class="sxs-lookup"><span data-stu-id="b2392-182">Name</span></span></th>
<th><span data-ttu-id="b2392-183">类型</span><span class="sxs-lookup"><span data-stu-id="b2392-183">Type</span></span></th>
<th><span data-ttu-id="b2392-184">数据</span><span class="sxs-lookup"><span data-stu-id="b2392-184">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2392-185">名称</span><span class="sxs-lookup"><span data-stu-id="b2392-185">Name</span></span></p></td>
<td><p><span data-ttu-id="b2392-186">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-186">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-187">显示在菜单上的应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="b2392-187">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2392-188">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="b2392-188">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="b2392-189">长</span><span class="sxs-lookup"><span data-stu-id="b2392-189">DWORD</span></span></p></td>
<td><p><span data-ttu-id="b2392-190">值 = 1。</span><span class="sxs-lookup"><span data-stu-id="b2392-190">Value = 1.</span></span> <span data-ttu-id="b2392-191">将应用程序类型设置为 "协议"。</span><span class="sxs-lookup"><span data-stu-id="b2392-191">Sets the application type to protocol.</span></span> <span data-ttu-id="b2392-192">在此情况下，其他可能的值不适用。</span><span class="sxs-lookup"><span data-stu-id="b2392-192">The other possible values do not apply in this case.</span></span> <span data-ttu-id="b2392-193">如果不存在，则将 ApplicationType 设置为 0 (可执行文件) 。</span><span class="sxs-lookup"><span data-stu-id="b2392-193">If not present, ApplicationType is set to 0 (executable).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2392-194">路径</span><span class="sxs-lookup"><span data-stu-id="b2392-194">Path</span></span></p></td>
<td><p><span data-ttu-id="b2392-195">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-195">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-196">用于启动协作应用程序的协议。</span><span class="sxs-lookup"><span data-stu-id="b2392-196">Protocol used to start the collaboration application.</span></span> <span data-ttu-id="b2392-197">对于 Live Meeting 2007，Path 的值设置为 <code>meet:%conf-uri%</code> 。</span><span class="sxs-lookup"><span data-stu-id="b2392-197">For Live Meeting 2007, the value of Path is set to <code>meet:%conf-uri%</code>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2392-198">SessionType</span><span class="sxs-lookup"><span data-stu-id="b2392-198">SessionType</span></span></p></td>
<td><p><span data-ttu-id="b2392-199">长</span><span class="sxs-lookup"><span data-stu-id="b2392-199">DWORD</span></span></p></td>
<td><p><span data-ttu-id="b2392-200">0 = 本地会话。</span><span class="sxs-lookup"><span data-stu-id="b2392-200">0 = Local session.</span></span> <span data-ttu-id="b2392-201">在本地计算机上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="b2392-201">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="b2392-202">1 = 两方会话 (默认) 。</span><span class="sxs-lookup"><span data-stu-id="b2392-202">1 = Two-party session (default).</span></span> <span data-ttu-id="b2392-203">Lync 2013 在本地启动应用程序，然后将系统通知发送给另一个用户。</span><span class="sxs-lookup"><span data-stu-id="b2392-203">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="b2392-204">其他用户单击通知并在其计算机上启动指定的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b2392-204">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="b2392-205">2 = 多方会话。</span><span class="sxs-lookup"><span data-stu-id="b2392-205">2 = Multiparty session.</span></span> <span data-ttu-id="b2392-206">Lync 2013 在本地启动应用程序，然后向其他用户发送系统通知，提示用户在其计算机上启动指定的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b2392-206">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2392-207">MCUType</span><span class="sxs-lookup"><span data-stu-id="b2392-207">MCUType</span></span></p></td>
<td><p><span data-ttu-id="b2392-208">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-208">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-209">DATA = 服务器的类型。</span><span class="sxs-lookup"><span data-stu-id="b2392-209">DATA = The type of server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2392-210">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="b2392-210">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="b2392-211">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b2392-211">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b2392-212">将显示此命令的菜单的列表，用分号分隔。</span><span class="sxs-lookup"><span data-stu-id="b2392-212">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="b2392-213">可能的值：</span><span class="sxs-lookup"><span data-stu-id="b2392-213">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2392-214">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="b2392-214">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="b2392-215">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="b2392-215">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="b2392-216">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="b2392-216">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="b2392-217">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="b2392-217">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="b2392-218">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="b2392-218">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="b2392-219">如果未定义 ExtensibleMenu，则使用 MainWindowRightClick 和 ConversationWindowActions 的默认值。</span><span class="sxs-lookup"><span data-stu-id="b2392-219">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b2392-220">以下示例添加了从 Lync 2013 中启动 ADatum 协作客户端的命令：</span><span class="sxs-lookup"><span data-stu-id="b2392-220">The following example adds commands to start ADatum Collaboration Client from within Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{27877e66-615c-4582-ab88-0cb2ca05d951}]
    "Path"="meet:%conf-uri%"
    "SessionType"=dword:00000002
    "LiveServerIntegration"=dword:00000001
    "ApplicationType"=dword:00000001
    "Name"="ADatum Collaboration Client"
    "MCUType"="Data"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"

<span data-ttu-id="b2392-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2392-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

