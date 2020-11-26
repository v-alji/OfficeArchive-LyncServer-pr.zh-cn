---
title: Lync Server 2013：（可选）修改 DTMF 命令的键映射
description: Lync Server 2013： (可选) Modify DTMF 命令的键映射。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Modify key mapping for DTMF commands
ms:assetid: d753b78d-400c-4df2-957f-e7576b2019c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398943(v=OCS.15)
ms:contentKeyID: 48185563
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7581001c31d929163962378a8734435f6d07c6c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424889"
---
# <a name="optional-modify-key-mapping-for-dtmf-commands-in-lync-server-2013"></a><span data-ttu-id="b56c4-103">（可选）在 Lync Server 2013 中修改 DTMF 命令的键映射</span><span class="sxs-lookup"><span data-stu-id="b56c4-103">(Optional) Modify key mapping for DTMF commands in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b56c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b56c4-104">

<span> </span></span></span>

<span data-ttu-id="b56c4-105">_**主题上次修改时间：** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="b56c4-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="b56c4-106">电话拨入式会议用户可以在电话小键盘上按键以执行双音多频 (DTMF) 命令。</span><span class="sxs-lookup"><span data-stu-id="b56c4-106">Dial-in conferencing users can press keys on the telephone keypad to perform dual-tone multi-frequency (DTMF) commands.</span></span> <span data-ttu-id="b56c4-107">通过 DTMF 命令，拨入会议的用户可以使用其电话上的小键盘控制会议设置（例如，将自己静音和取消静音，或者锁定和解锁会议）。</span><span class="sxs-lookup"><span data-stu-id="b56c4-107">DTMF commands enable users who dial in to a conference to control conference settings (such as muting and unmuting themselves or locking and unlocking the conference) by using the keypad on their telephone.</span></span> <span data-ttu-id="b56c4-108">你可以使用 cmdlet 修改 DTMF 命令使用的密钥。</span><span class="sxs-lookup"><span data-stu-id="b56c4-108">You can use cmdlets to modify the keys used for the DTMF commands.</span></span> <span data-ttu-id="b56c4-109">此步骤是可选的。</span><span class="sxs-lookup"><span data-stu-id="b56c4-109">This step is optional.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b56c4-110">有关这些 cmdlet 以及可能的 DTMF 选项的详细信息，请参阅 Lync Server 命令行管理程序文档或 Lync Server Management Shell 命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="b56c4-110">For details about these cmdlets and the possible DTMF options, see Lync Server Management Shell documentation or Lync Server Management Shell command-line Help.</span></span>



</div>

<div>

## <a name="to-modify-the-key-mapping-of-dtmf-commands"></a><span data-ttu-id="b56c4-111">修改 DTMF 命令的键映射</span><span class="sxs-lookup"><span data-stu-id="b56c4-111">To modify the key mapping of DTMF commands</span></span>

1.  <span data-ttu-id="b56c4-112">以 **RTCUniversalServerAdmins** 组成员的身份登录计算机，或者作为 **Cs-ServerAdministrator** 或 **CsAdministrator** 角色的成员登录到计算机。</span><span class="sxs-lookup"><span data-stu-id="b56c4-112">Log on to the computer as a member of the **RTCUniversalServerAdmins** group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="b56c4-113">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="b56c4-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="b56c4-114">在命令提示符下，运行以下内容：</span><span class="sxs-lookup"><span data-stu-id="b56c4-114">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingDtmfConfiguration
    
    <span data-ttu-id="b56c4-115">此 cmdlet 返回用于拨入式会议的 DTMF 设置。</span><span class="sxs-lookup"><span data-stu-id="b56c4-115">This cmdlet returns the DTMF settings used for dial-in conferencing.</span></span>

4.  <span data-ttu-id="b56c4-116">运行以下 cmdlet 并为要更改的每个选项指定要按下的键：</span><span class="sxs-lookup"><span data-stu-id="b56c4-116">Run the following cmdlet and specify the key to be pressed for each option that you want to change:</span></span>
    
        Set-CsDialinConferencingDtmfConfiguration [-Identity <global or site collection to be changed>]
        [-AdmitAll <default key is 8>] [-AudienceMuteCommand <default key is 4>]
        [-CommandCharacter <* (default) | #>] [-EnableDisableAnnouncementsCommand <default key is 9>]
        [-HelpCommand <default key is 1>] [-LockUnlockConferenceCommand <default key is 7>]
        [-MuteUnmuteCommand <default key is 6>] [-PrivateRollCallCommand <default key is 3>]
    
    <span data-ttu-id="b56c4-117">此 cmdlet 修改用于拨入式会议的 DTMF 设置。</span><span class="sxs-lookup"><span data-stu-id="b56c4-117">This cmdlet modifies the DTMF settings used for dial-in conferencing.</span></span>
    
    <span data-ttu-id="b56c4-118">例如：</span><span class="sxs-lookup"><span data-stu-id="b56c4-118">For example:</span></span>
    
        Set-CsDialinConferencingDtmfConfiguration -EnableDisableAnnouncementsCommand 4 -AudienceMuteCommand 9
    
    <span data-ttu-id="b56c4-119">此示例交换按下的键，以启用或禁用通知以及为所有参与者按下静音和取消静音的键。</span><span class="sxs-lookup"><span data-stu-id="b56c4-119">This example swaps the key that is pressed to enable or disable announcements and the key that is pressed to mute and unmute all participants.</span></span> <span data-ttu-id="b56c4-120">由于没有指定标识，这些更改将应用于全局 DTMF 设置。</span><span class="sxs-lookup"><span data-stu-id="b56c4-120">Because no Identity is specified, these changes apply to the global DTMF settings.</span></span>

5.  <span data-ttu-id="b56c4-121">（可选）若要为特定站点创建其他 DTMF 命令集，请使用带有站点 Identity 的 **New-CsDialinConferencingDtmfConfiguration** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b56c4-121">(Optional) To create additional sets of DTMF commands for specific sites, use the **New-CsDialinConferencingDtmfConfiguration** cmdlet with a site identity.</span></span> <span data-ttu-id="b56c4-122">为站点创建新的 DTMF 设置后，站点设置将优先于全局设置。</span><span class="sxs-lookup"><span data-stu-id="b56c4-122">When you create new DTMF settings for sites, the site settings take precedence over the global settings.</span></span> <span data-ttu-id="b56c4-123">有关详细信息，请参阅 Lync Server 命令行管理程序文档或 Lync Server Management Shell 命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="b56c4-123">For details, see Lync Server Management Shell documentation or Lync Server Management Shell command-line Help.</span></span>

<span data-ttu-id="b56c4-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b56c4-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

