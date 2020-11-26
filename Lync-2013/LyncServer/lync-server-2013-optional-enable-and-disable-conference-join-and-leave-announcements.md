---
title: （可选）启用和禁用会议加入和离开通知
description: " (可选) 启用和禁用会议加入并退出公告。"
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Enable and disable conference join and leave announcements
ms:assetid: c9529568-e66c-48d8-aef2-9072f9c336ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398834(v=OCS.15)
ms:contentKeyID: 48185403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 70cd6b452a44d7d40f23d5ca96b6e4b7b063d2ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445237"
---
# <a name="optional-enable-and-disable-conference-join-and-leave-announcements-in-lync-server-2013"></a><span data-ttu-id="2bda5-103">（可选）在 Lync Server 2013 中启用和禁用会议加入和离开通知</span><span class="sxs-lookup"><span data-stu-id="2bda5-103">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2bda5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2bda5-104">

<span> </span></span></span>

<span data-ttu-id="2bda5-105">_**主题上次修改时间：** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="2bda5-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="2bda5-106">当拨入用户加入或离开会议时，会议公告应用程序可以通过播放音频或说出其名称来宣布其进入或退出。</span><span class="sxs-lookup"><span data-stu-id="2bda5-106">When dial-in users join or leave a conference, the Conferencing Announcement application can announce their entrance or exit by playing a tone or saying their names.</span></span> <span data-ttu-id="2bda5-107">你可以通过运行 cmdlet 来更改通知的工作方式。</span><span class="sxs-lookup"><span data-stu-id="2bda5-107">You can change how announcements work by running cmdlets.</span></span> <span data-ttu-id="2bda5-108">此步骤是可选的。</span><span class="sxs-lookup"><span data-stu-id="2bda5-108">This step is optional.</span></span>

<div>

## <a name="to-modify-the-conference-join-and-leave-announcement-behavior"></a><span data-ttu-id="2bda5-109">修改会议加入和离开通知行为</span><span class="sxs-lookup"><span data-stu-id="2bda5-109">To modify the conference join and leave announcement behavior</span></span>

1.  <span data-ttu-id="2bda5-110">以 RTCUniversalServerAdmins 组成员的身份登录计算机，或者作为 **Cs-ServerAdministrator** 或 **CsAdministrator** 角色的成员登录到计算机。</span><span class="sxs-lookup"><span data-stu-id="2bda5-110">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="2bda5-111">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="2bda5-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="2bda5-112">在命令提示符下，运行以下内容：</span><span class="sxs-lookup"><span data-stu-id="2bda5-112">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingConfiguration
    
    <span data-ttu-id="2bda5-113">此 cmdlet 检索有关参与者是否需要在加入会议时记录其名称的信息，以及当参与者加入或离开电话拨入式会议时 Lync 服务器的响应方式。</span><span class="sxs-lookup"><span data-stu-id="2bda5-113">This cmdlet retrieves information about whether participants are required to record their name when joining a conference and how Lync Server responds when participants join or leave a dial-in conference.</span></span>

4.  <span data-ttu-id="2bda5-114">在命令提示符下，运行以下内容：</span><span class="sxs-lookup"><span data-stu-id="2bda5-114">Run the following at the command prompt:</span></span>
    
        Set-CsDialinConferencingConfiguration -Identity <identity of dial-in conferencing settings to be modified>
        [-EnableNameRecording <$true | $false>]
        [-EntryExitAnnouncementsEnabledByDefault <$true | $false>]
        [-EntryExitAnnouncementsType <UseNames | ToneOnly]
    
    <span data-ttu-id="2bda5-115">**EnableNameRecording**   确定在进入会议之前是否要求匿名参与者录制其姓名。</span><span class="sxs-lookup"><span data-stu-id="2bda5-115">**EnableNameRecording**   Determines whether anonymous participants are asked to record their name before entering the conference.</span></span> <span data-ttu-id="2bda5-116">默认值为 "$true"，这意味着在加入会议时，系统会提示匿名参与者声明其名称。</span><span class="sxs-lookup"><span data-stu-id="2bda5-116">The default value is "$true," which means that anonymous participants are prompted to state their name when joining a conference.</span></span> <span data-ttu-id="2bda5-117"> (经过身份验证的参与者不会记录其名称，因为使用其显示名称的是。 ) </span><span class="sxs-lookup"><span data-stu-id="2bda5-117">(Authenticated participants do not record their name because their display name is used instead.)</span></span>
    
    <span data-ttu-id="2bda5-118">**EntryExitAnnouncementsEnabledByDefault**   指示默认情况下是打开还是关闭公告。</span><span class="sxs-lookup"><span data-stu-id="2bda5-118">**EntryExitAnnouncementsEnabledByDefault**   Indicates whether announcements are turned on or off by default.</span></span> <span data-ttu-id="2bda5-119">默认值为“$false”，即默认情况下，在参与者加入或离开会议时没有通知。</span><span class="sxs-lookup"><span data-stu-id="2bda5-119">The default value is "$false," which means that by default there are no announcements when participants join or leave a conference.</span></span> <span data-ttu-id="2bda5-120">会议组织者在安排会议时可以覆盖此设置。</span><span class="sxs-lookup"><span data-stu-id="2bda5-120">The meeting organizer can override this setting when scheduling a meeting.</span></span>
    
    <span data-ttu-id="2bda5-121">**EntryExitAnnouncementsType**   指示每当参与者加入或离开已启用公告的会议时所采取的操作。</span><span class="sxs-lookup"><span data-stu-id="2bda5-121">**EntryExitAnnouncementsType**   Indicates the action taken whenever a participant joins or leaves a conference for which announcements are enabled.</span></span> <span data-ttu-id="2bda5-122">默认值为“UseNames”，即有通知，类似于：“Ken Myer 已加入会议”（如果已打开通知）。</span><span class="sxs-lookup"><span data-stu-id="2bda5-122">The default value is "UseNames," which means there is an announcement similar to the following: "Ken Myer has joined the conference" when announcements are turned on.</span></span>
    
    <span data-ttu-id="2bda5-p105">可以在 global 作用域或 site 作用域配置这些设置。在 site 作用域配置的设置的优先于在 global 作用域配置的设置。</span><span class="sxs-lookup"><span data-stu-id="2bda5-p105">You can configure these settings at the global scope or at the site scope. Settings configured at the site scope take precedence over settings configured at the global scope.</span></span>
    
    <span data-ttu-id="2bda5-125">例如：</span><span class="sxs-lookup"><span data-stu-id="2bda5-125">For example:</span></span>
    
        Set-CsDialinConferencingConfiguration -Identity site:Redmond
        -EnableNameRecording $false
        -EntryExitAnnouncementsEnabledByDefault $true
        -EntryExitAnnouncementsType ToneOnly
    
    <span data-ttu-id="2bda5-126">在此示例中，"雷德蒙" 的网站范围配置了 "设置"。</span><span class="sxs-lookup"><span data-stu-id="2bda5-126">In this example, settings are configured at the site scope for Redmond.</span></span> <span data-ttu-id="2bda5-127">通知已打开，但在参与者加入会议时系统未提示他们说出姓名。</span><span class="sxs-lookup"><span data-stu-id="2bda5-127">Announcements are turned on, but participants are not prompted to say their name when they join a conference.</span></span> <span data-ttu-id="2bda5-128">当参与者进入或离开会议时，将会播放音调。</span><span class="sxs-lookup"><span data-stu-id="2bda5-128">A tone is played when participants enter or leave a conference.</span></span>

<span data-ttu-id="2bda5-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2bda5-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

