---
title: Lync Server 2013：在 Survivable Branch Appliance 或 Survivable Branch Server 上承载用户
description: Lync Server 2013： Survivable 分支装置或服务器上的家庭用户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Home users on a Survivable Branch Appliance or Server
ms:assetid: faf1ebb9-6d7d-4a58-8ff7-801b7b31d3ba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413066(v=OCS.15)
ms:contentKeyID: 48185926
ms.date: 12/11/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 124eb7a51a8d5ff672d720fdad8956f682e29090
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427612"
---
# <a name="home-users-on-a-survivable-branch-appliance-or-server-in-lync-server-2013"></a><span data-ttu-id="f5faa-103">在 Lync Server 2013 中在 Survivable Branch Appliance 或 Survivable Branch Server 上承载用户</span><span class="sxs-lookup"><span data-stu-id="f5faa-103">Home users on a Survivable Branch Appliance or Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5faa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5faa-104">

<span> </span></span></span>

<span data-ttu-id="f5faa-105">_**主题上次修改时间：** 2014-12-10_</span><span class="sxs-lookup"><span data-stu-id="f5faa-105">_**Topic Last Modified:** 2014-12-10_</span></span>

<span data-ttu-id="f5faa-106">在 Survivable 分支设备或 Survivable 分支服务器上托管用户的过程与在前端池中托管用户的过程类似。</span><span class="sxs-lookup"><span data-stu-id="f5faa-106">The process of homing users on a Survivable Branch Appliance or a Survivable Branch Server is similar to the process of homing users on a Front End pool.</span></span> <span data-ttu-id="f5faa-107">在中央站点上执行 Survivable 分支装置或 Survivable 分支服务器过程。</span><span class="sxs-lookup"><span data-stu-id="f5faa-107">Perform the Survivable Branch Appliance or Survivable Branch Server procedure at the central site.</span></span>

<div>

## <a name="to-home-users-on-survivable-branch-appliance-or-survivable-branch-server"></a><span data-ttu-id="f5faa-108">在 Survivable 分支装置或 Survivable 分支服务器上家庭用户</span><span class="sxs-lookup"><span data-stu-id="f5faa-108">To home users on Survivable Branch Appliance or Survivable Branch Server</span></span>

1.  <span data-ttu-id="f5faa-109">将用户移动到 Survivable 分支服务器或 Survivable 分支服务器之前，请打开 Lync Server 命令行管理程序，然后执行以下所有操作：</span><span class="sxs-lookup"><span data-stu-id="f5faa-109">Before moving users to the Survivable Branch Server or Survivable Branch Server, open the Lync Server Management Shell, and then do all of the following:</span></span>
    
      - <span data-ttu-id="f5faa-110">运行 cmdlet **Test-CsPstnOutboundCall** 以验证 Survivable 分支服务器是否正在运行，以及是否已配置公共交换电话网络 (PSTN) 连接。</span><span class="sxs-lookup"><span data-stu-id="f5faa-110">Run the cmdlet **Test-CsPstnOutboundCall** to verify that the Survivable Branch Server is running and that the public switched telephone network (PSTN) connectivity is configured.</span></span> <span data-ttu-id="f5faa-111">如果需要修改 PSTN 网关属性，请使用 cmdlet **CsPstnGateway**。</span><span class="sxs-lookup"><span data-stu-id="f5faa-111">If you need to modify PSTN gateway properties, use the cmdlet **Set-CsPstnGateway**.</span></span>
    
      - <span data-ttu-id="f5faa-112">运行 cmdlet **CsVoicePolicy** 以验证将托管在 Survivable 分支服务器上的用户是否具有相应的 VoIP 路由策略。</span><span class="sxs-lookup"><span data-stu-id="f5faa-112">Run the cmdlet **Get-CsVoicePolicy** to verify that the users who will be homed on the Survivable Branch Server have the appropriate VoIP routing policy.</span></span> <span data-ttu-id="f5faa-113">如果需要修改 VoIP 策略，请使用 cmdlet **Set-CsVoicePolicy**。</span><span class="sxs-lookup"><span data-stu-id="f5faa-113">If you need to modify the VoIP policy, use the cmdlet **Set-CsVoicePolicy**.</span></span>
    
      - <span data-ttu-id="f5faa-114">运行 cmdlet **CsVoicemailReroutingConfiguration** 以验证是否配置了语音邮件重新路由设置。</span><span class="sxs-lookup"><span data-stu-id="f5faa-114">Run the cmdlet **Get-CsVoicemailReroutingConfiguration** to verify that the voice mail rerouting settings are configured.</span></span> <span data-ttu-id="f5faa-115">如果需要修改语音邮件重新路由设置，请使用 cmdlet **CsVoicemailReroutingConfiguration**。</span><span class="sxs-lookup"><span data-stu-id="f5faa-115">If you need to modify the voice mail rerouting settings, use the cmdlet **Set-CsVoicemailReroutingConfiguration**.</span></span>

2.  <span data-ttu-id="f5faa-116">在 Lync Server Management Shell 中，运行 cmdlet **move-move-csuser** 移动家庭用户。</span><span class="sxs-lookup"><span data-stu-id="f5faa-116">In the Lync Server Management Shell, run the cmdlet **Move-CsUser** to move home users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f5faa-117">您也可以使用 Lync Server 控制面板验证先决条件和家庭用户。</span><span class="sxs-lookup"><span data-stu-id="f5faa-117">You can also use Lync Server Control Panel to verify prerequisites and home users.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="f5faa-118">在 Lync Server Survivable 分支设备上托管的用户无法创建新的聊天室或查看现有聊天室的聊天室卡片。</span><span class="sxs-lookup"><span data-stu-id="f5faa-118">Users who are homed on a Lync Server Survivable Branch Appliance are unable to create new chat rooms or view the room card for existing rooms.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f5faa-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5faa-119">See Also</span></span>


[<span data-ttu-id="f5faa-120">Test-CsPstnOutboundCall</span><span class="sxs-lookup"><span data-stu-id="f5faa-120">Test-CsPstnOutboundCall</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall)  
[<span data-ttu-id="f5faa-121">CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="f5faa-121">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="f5faa-122">CsVoicemailReroutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5faa-122">Get-CsVoicemailReroutingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicemailReroutingConfiguration)  
[<span data-ttu-id="f5faa-123">移动-Move-csuser</span><span class="sxs-lookup"><span data-stu-id="f5faa-123">Move-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Move-CsUser)  
  

<span data-ttu-id="f5faa-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5faa-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

