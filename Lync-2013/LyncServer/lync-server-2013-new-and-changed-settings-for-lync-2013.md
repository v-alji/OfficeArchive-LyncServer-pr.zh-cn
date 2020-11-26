---
title: Lync Server 2013： Lync 2013 的新增和更改的设置
description: Lync Server 2013： Lync 2013 的新增和更改的设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New and changed settings for Lync 2013
ms:assetid: bb13789c-7eda-461c-a387-02ea8ca4dabe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205204(v=OCS.15)
ms:contentKeyID: 48185241
ms.date: 12/08/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bf744e1bae774904733390ec624be523ad32bc1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445482"
---
# <a name="new-and-changed-settings-for-lync-2013"></a><span data-ttu-id="ef0c5-103">Lync 2013 的新增和更改的设置</span><span class="sxs-lookup"><span data-stu-id="ef0c5-103">New and changed settings for Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef0c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef0c5-104">

<span> </span></span></span>

<span data-ttu-id="ef0c5-105">_**主题上次修改时间：** 2014-12-05_</span><span class="sxs-lookup"><span data-stu-id="ef0c5-105">_**Topic Last Modified:** 2014-12-05_</span></span>

<span data-ttu-id="ef0c5-106">本主题讨论直接与客户端管理相关的 Lync Server Management Shell cmdlet 的更改。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-106">This topic discusses changes to Lync Server Management Shell cmdlets that relate directly to client management.</span></span> <span data-ttu-id="ef0c5-107">Lync Server 2013 引入了一些新参数，以及 deprecates 可通过其他方式配置的功能的参数。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-107">Lync Server 2013 introduces several new parameters, and deprecates parameters for features that can be configured through other means.</span></span>

<div>

## <a name="new-client-management-parameters"></a><span data-ttu-id="ef0c5-108">新的客户端管理参数</span><span class="sxs-lookup"><span data-stu-id="ef0c5-108">New Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef0c5-109">新增功能</span><span class="sxs-lookup"><span data-stu-id="ef0c5-109">New</span></span></th>
<th><span data-ttu-id="ef0c5-110">Lync Server Management Shell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef0c5-110">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="ef0c5-111">说明</span><span class="sxs-lookup"><span data-stu-id="ef0c5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef0c5-112">TracingLevel</span><span class="sxs-lookup"><span data-stu-id="ef0c5-112">TracingLevel</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-113">Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="ef0c5-113">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-114">当设置为 True 时，将在 Lync 中启用软件跟踪;当设置为 False 时，软件跟踪将被禁用。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-114">When set to True, software tracing will be enabled in Lync; when set to False, software tracing will be disabled.</span></span> <span data-ttu-id="ef0c5-115">软件跟踪包括对程序执行的所有操作的详细记录 (包括跟踪 API 调用) 。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-115">Software tracing involves keeping a detailed record of everything that a program does (including tracking API calls).</span></span> <span data-ttu-id="ef0c5-116">跟踪主要适用于开发人员和应用程序支持人员。此设置等效于 "通信服务器 2007 R2 组策略" 设置 " &quot; 启用对 Communicator 的跟踪"。 &quot; 这些设置如下所示：</span><span class="sxs-lookup"><span data-stu-id="ef0c5-116">Tracing is mostly useful to developers and to application support personnel.This setting is equivalent to the Communications Server 2007 R2 Group Policy setting &quot;Turn on tracing for Communicator.&quot; The settings are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef0c5-117">关闭 = 禁用跟踪，用户无法更改此设置。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-117">Off = Tracing is disabled and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="ef0c5-118">浅色 = 执行最短跟踪，用户无法更改此设置。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-118">Light = Minimal tracing is performed, and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="ef0c5-119">On = 执行详细跟踪，用户无法更改此设置。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-119">On = Verbose tracing is performed, and the user cannot change this setting.</span></span></p></li>
</ul>
<p><span data-ttu-id="ef0c5-120">默认情况下，TracingLevel 设置为 null 值。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-120">By default TracingLevel is set to a null value.</span></span> <span data-ttu-id="ef0c5-121">这意味着将执行最少的跟踪，但用户可以启用或禁用此最小跟踪。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-121">That means that minimal tracing is performed, but the user can enable or disable this minimal tracing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef0c5-122">EnableMediaRedirection</span><span class="sxs-lookup"><span data-stu-id="ef0c5-122">EnableMediaRedirection</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-123">Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="ef0c5-123">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-124">如果设置为 True ($True) 允许将音频和视频流与其他网络流量分开，则这允许客户端设备在本地进行音频和视频编码和解码。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-124">When set to True ($True) allows audio and video streams to be separated from other network traffic, In turn, this allows client devices to do encoding and decoding of audio and video locally.</span></span> <span data-ttu-id="ef0c5-125">媒体重定向通常会导致带宽使用较低、服务器可伸缩性更高，以及与类似技术（如设备远程处理或编解码器压缩）相比的更为最佳的用户体验。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-125">Media redirection typically results in lower bandwidth usage, higher server scalability, and a more-optimal user experience compared to similar techniques such as device remoting or codec compression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef0c5-126">AllowLargeMeetings</span><span class="sxs-lookup"><span data-stu-id="ef0c5-126">AllowLargeMeetings</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-127">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="ef0c5-127">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-128">当设置为 True 时，所有 Lync 会议均被视为 &quot; 大型会议。 &quot; 使用较大的会议时，将对发送给参与者的通知的数量以及默认情况下传输的会议名单的大小进行限制。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-128">When set to True, all Lync Meetings are treated as &quot;large meetings.&quot; With a large meeting, restrictions are placed on the number of notifications that are sent to participants, in addition to the size of the meeting roster that is transmitted by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef0c5-129">DisablePowerPointAnnotations</span><span class="sxs-lookup"><span data-stu-id="ef0c5-129">DisablePowerPointAnnotations</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-130">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="ef0c5-130">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-131">如果设置为 True ($True) 用户将无法向会议中使用的 PowerPoint 幻灯片添加批注。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-131">When set to True ($True) users won’t be able to add annotations to PowerPoint slides used in a conference.</span></span> <span data-ttu-id="ef0c5-132">但是 (根据 AllowAnnotations 属性的值) ，用户仍可访问其他 whiteboarding 功能。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-132">However (depending on the value of the AllowAnnotations property), users will still have access to other whiteboarding features.</span></span> <span data-ttu-id="ef0c5-133">默认值为 False，表示允许使用 PowerPoint 注释。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-133">The default value is False, meaning that PowerPoint annotations are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef0c5-134">AllowSharedNotes</span><span class="sxs-lookup"><span data-stu-id="ef0c5-134">AllowSharedNotes</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-135">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="ef0c5-135">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-136">如果设置为 True (默认值) 则链接到会议的任何打开的 OneNote 笔记本将自动更新，其中包含会议参与者和会议期间共享的内容的详细信息（如会议参与者）。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-136">When set to True (the default value) any open OneNote notebooks linked to the conference will automatically be updated with information such as conference participants and details about content shared during the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef0c5-137">EnableInviteCustomization</span><span class="sxs-lookup"><span data-stu-id="ef0c5-137">EnableInviteCustomization</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-138">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef0c5-138">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-139">与其他新的 CsMeetingConfiguration 参数一起使用，自定义 Lync 2013 的联机会议加载项生成的会议邀请。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-139">Used along with the other new CsMeetingConfiguration parameters to customize the meeting invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef0c5-140">LogoURL</span><span class="sxs-lookup"><span data-stu-id="ef0c5-140">LogoURL</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-141">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef0c5-141">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-142">将组织的徽标添加到由 Lync 2013 的联机会议加载项生成的所有邀请。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-142">Adds your organization’s logo to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="ef0c5-143">指定 GIF 或 JPG 图像的 URL。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-143">You specify the URL of a GIF or JPG image.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef0c5-144">HelpURL</span><span class="sxs-lookup"><span data-stu-id="ef0c5-144">HelpURL</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-145">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef0c5-145">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-146">将组织的帮助或支持 URL 添加到由 Lync 2013 的联机会议加载项生成的所有邀请。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-146">Adds your organization’s help or support URL to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef0c5-147">LegalURL</span><span class="sxs-lookup"><span data-stu-id="ef0c5-147">LegalURL</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-148">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef0c5-148">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-149">将法律文本或免责声明文本添加到由 Lync 2013 的联机会议加载项生成的所有邀请中。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-149">Adds legal text or disclaimer text to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="ef0c5-150">指定文本位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-150">You specify the URL for the location of the text.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef0c5-151">CustomFooterText</span><span class="sxs-lookup"><span data-stu-id="ef0c5-151">CustomFooterText</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-152">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef0c5-152">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-153">将自定义页脚添加到由 Lync 2013 的联机会议加载项生成的所有邀请。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-153">Adds a custom footer to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="ef0c5-154">为自定义页脚文本的位置指定 URL。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-154">You specify the URL for the location of the custom footer text.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="deprecated-client-management-parameters"></a><span data-ttu-id="ef0c5-155">已过时的客户端管理参数</span><span class="sxs-lookup"><span data-stu-id="ef0c5-155">Deprecated Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef0c5-156">参数</span><span class="sxs-lookup"><span data-stu-id="ef0c5-156">Parameter</span></span></th>
<th><span data-ttu-id="ef0c5-157">Lync Server Management Shell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef0c5-157">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="ef0c5-158">说明</span><span class="sxs-lookup"><span data-stu-id="ef0c5-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef0c5-159">CustomizedHelpUrl</span><span class="sxs-lookup"><span data-stu-id="ef0c5-159">CustomizedHelpUrl</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-160">Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="ef0c5-160">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-161">此参数已弃用，无法用于 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-161">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="ef0c5-162">当与 EnableEnterpriseCustomizedHelp 结合使用时，此参数使组织可以指定 URL，以便在用户单击 Lync 中的 "帮助" 菜单时，将显示自定义帮助。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-162">When used in conjunction with EnableEnterpriseCustomizedHelp, this parameter enabled an organization to specify a URL so that when users clicked the Help menu in Lync, customized help would display.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef0c5-163">EnableEnterpriseCustomizedHelp</span><span class="sxs-lookup"><span data-stu-id="ef0c5-163">EnableEnterpriseCustomizedHelp</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-164">Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="ef0c5-164">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-165">此参数已弃用，无法用于 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-165">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="ef0c5-166">当与 CustomizedHelpUrl 结合使用时，此参数允许组织显示自定义帮助。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-166">When used in conjunction with CustomizedHelpUrl, this parameter enabled organizations to display customized help.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef0c5-167">EnableSQMData</span><span class="sxs-lookup"><span data-stu-id="ef0c5-167">EnableSQMData</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-168">Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="ef0c5-168">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-169">已在 Lync Server 2013 中删除 Set-CSClientPolicy cmdlet 的 EnableSQMData 参数。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-169">The EnableSQMData parameter of the Set-CSClientPolicy cmdlet has been removed in Lync Server 2013.</span></span> <span data-ttu-id="ef0c5-170">相反，你可以使用软件质量管理 (SQM) 数据的共享组策略设置来确定 "Lync 客户端常规选项" 页面中的 "客户体验改善" 选项的用户界面：</span><span class="sxs-lookup"><span data-stu-id="ef0c5-170">Instead, you can use the shared Group Policy setting for Software Quality Management (SQM) data to determine the user interface for the Customer Experience Improvement option in the Lync client General options page:</span></span></p>
<p><span data-ttu-id="ef0c5-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span><span class="sxs-lookup"><span data-stu-id="ef0c5-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span></span></p>
<p><span data-ttu-id="ef0c5-172">相对值</span><span class="sxs-lookup"><span data-stu-id="ef0c5-172">Values:</span></span></p>
<p><span data-ttu-id="ef0c5-173">1 = 显示并选中复选框 (用户可以清除复选框) </span><span class="sxs-lookup"><span data-stu-id="ef0c5-173">1 = Display and select the check box (the user can clear the check box)</span></span></p>
<p><span data-ttu-id="ef0c5-174">0 = 关闭并禁用复选框 (用户不能替代) </span><span class="sxs-lookup"><span data-stu-id="ef0c5-174">0 = Turn off and disable the check box (user can't override)</span></span></p>
<p><span data-ttu-id="ef0c5-175">Null = 该值由 Office 安装程序确定，用户将显示复选框供用户选择</span><span class="sxs-lookup"><span data-stu-id="ef0c5-175">Null = The value is determined by Office setup, and the check box is displayed for users to set as they choose</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef0c5-176">AllowExchangeContactStore</span><span class="sxs-lookup"><span data-stu-id="ef0c5-176">AllowExchangeContactStore</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-177">Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="ef0c5-177">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-178">此参数已被删除。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-178">This parameter has been removed.</span></span> <span data-ttu-id="ef0c5-179">当你部署 Lync Server 2013 并发布拓扑时，默认情况下为所有用户启用 "统一联系人存储"。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-179">Instead, when you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="ef0c5-180">这意味着，所有用户的联系人都将保留在 Exchange 中，并且在 Lync、Outlook 和 Outlook Web Access 中可用。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-180">This means that all a user’s contacts are kept in Exchange and are available in Lync, Outlook, and Outlook Web Access.</span></span> <span data-ttu-id="ef0c5-181">你可以使用 Set-CsUserServicesPolicy cmdlet 自定义哪些用户具有可用的统一联系人存储。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-181">You can use the Set-CsUserServicesPolicy cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="ef0c5-182">你可以按网站、租户、个人或个人组来启用用户。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-182">You can enable users globally, by site, by tenant, or by individuals or groups of individuals.</span></span> <span data-ttu-id="ef0c5-183">有关详细信息，请参阅 <a href="lync-server-2013-enable-users-for-unified-contact-store.md">在 Lync Server 2013 中为统一联系人存储启用用户</a>。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-183">For details, see <a href="lync-server-2013-enable-users-for-unified-contact-store.md">Enable users for unified contact store in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef0c5-184">MAPIPollInterval</span><span class="sxs-lookup"><span data-stu-id="ef0c5-184">MAPIPollInterval</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-185">Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="ef0c5-185">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-186">Lync 2013 不使用此参数。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-186">This parameter is not used by Lync 2013.</span></span> <span data-ttu-id="ef0c5-187">在以前的版本中，此参数指定客户端从 Exchange 公用文件夹检索 MAPI 数据的频率</span><span class="sxs-lookup"><span data-stu-id="ef0c5-187">In previous releases, this parameter specified how often the client retrieved MAPI data from Exchange public folders</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef0c5-188">DisableICE</span><span class="sxs-lookup"><span data-stu-id="ef0c5-188">DisableICE</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-189">Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="ef0c5-189">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="ef0c5-190">此参数在 Lync 2013 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="ef0c5-190">This parameter was deprecated in Lync 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ef0c5-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef0c5-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

