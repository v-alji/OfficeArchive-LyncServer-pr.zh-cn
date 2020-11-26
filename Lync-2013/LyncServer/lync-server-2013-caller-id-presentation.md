---
title: Lync Server 2013：呼叫方 ID 演示文稿
description: Lync Server 2013：呼叫方 ID 演示文稿。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Caller ID presentation
ms:assetid: 6a643961-a0a1-41d1-96ba-6c428a89d82e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204980(v=OCS.15)
ms:contentKeyID: 48184425
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 651c9c8da8b6a1ed13669255008ca639a90e1806
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435633"
---
# <a name="caller-id-presentation-in-lync-server-2013"></a><span data-ttu-id="8bf63-103">Lync Server 2013 中的呼叫者 ID 演示文稿</span><span class="sxs-lookup"><span data-stu-id="8bf63-103">Caller ID presentation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8bf63-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8bf63-104">

<span> </span></span></span>

<span data-ttu-id="8bf63-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="8bf63-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="8bf63-106">使用 Lync Server 2010，呼叫方的电话号码 (也就是说，电话号码) 可以从格式转换为中继对等 (的本地拨号格式，即关联网关、专用分支 exchange (PBX) 或 SIP 中继) 。</span><span class="sxs-lookup"><span data-stu-id="8bf63-106">With Lync Server 2010, the called party’s phone number (that is, the phone number called) can be translated from E.164 format to the local dialing format that is required by the trunk peer (that is, the associated gateway, private branch exchange (PBX), or SIP trunk).</span></span> <span data-ttu-id="8bf63-107">为此，必须定义一个或多个转换规则，以便在将请求 URI 路由至中继对等方之前对其执行转换。</span><span class="sxs-lookup"><span data-stu-id="8bf63-107">To do this, you must define one or more translation rules to translate the Request URI before routing it to the trunk peer.</span></span>

<span data-ttu-id="8bf63-108">Lync Server 2013 引入了同时转换呼叫方的电话号码的选项 (也就是说，呼叫) 方将从格式的电话号码转换为中继对等所需的本地拨号格式。</span><span class="sxs-lookup"><span data-stu-id="8bf63-108">Lync Server 2013 introduces the option to also translate the calling party’s phone number (that is, the phone number that the caller is calling from) from E.164 format to the local dialing format that is required by the trunk peer.</span></span> <span data-ttu-id="8bf63-109">例如，可以编写用于删除拨号串开头的 +44 并将其替换为 0144 的转换规则。</span><span class="sxs-lookup"><span data-stu-id="8bf63-109">For example, you can write a translation rule to remove +44 from the beginning of a dial string and replace it with 0144.</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="8bf63-110">**使用 Lync Server "控制面板" 配置呼叫方 ID**</span><span class="sxs-lookup"><span data-stu-id="8bf63-110">**To configure Caller ID by using Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="8bf63-111">以 RTCUniversalServerAdmins 组成员的身份或者以 CsVoiceAdministrator、CsServerAdministrator 或 CsAdministrator 角色成员的身份登录计算机。</span><span class="sxs-lookup"><span data-stu-id="8bf63-111">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="8bf63-112">有关详细信息，请参阅 [在 Lync Server 2013 中委派设置权限](lync-server-2013-delegate-setup-permissions.md)。</span><span class="sxs-lookup"><span data-stu-id="8bf63-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="8bf63-113">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="8bf63-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8bf63-114">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="8bf63-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8bf63-115">在左侧导航栏中，单击“语音路由”，然后单击“Trunk 配置”。</span><span class="sxs-lookup"><span data-stu-id="8bf63-115">In the left navigation bar, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

4.  <span data-ttu-id="8bf63-116">在“Trunk 配置”页上，双击一个现有中继（例如，“全局”中继）以显示“编辑 Trunk 配置”对话框。</span><span class="sxs-lookup"><span data-stu-id="8bf63-116">On the **Trunk Configuration** page, double-click an existing trunk (for example, the **Global** trunk) to display the **Edit Trunk Configuration** dialog box.</span></span>

5.  <span data-ttu-id="8bf63-117">配置呼叫者 ID 显示：</span><span class="sxs-lookup"><span data-stu-id="8bf63-117">To configure caller ID presentation:</span></span>
    
      - <span data-ttu-id="8bf63-118">若要从您的企业语音部署中可用的所有翻译规则列表中选择一个或多个规则，请单击 " **选择**"。</span><span class="sxs-lookup"><span data-stu-id="8bf63-118">To choose one or more rules from a list of all translation rules available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="8bf63-119">在“主叫号码转换规则”中，单击要与中继关联的规则，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8bf63-119">In **Calling number translation rules**, click the rules that you want to associate with the trunk, and then click **OK**.</span></span>
    
      - <span data-ttu-id="8bf63-120">要定义新的转换规则并将其与中继相关联，请单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8bf63-120">To define a new translation rule and associate it with the trunk, click **New**.</span></span> <span data-ttu-id="8bf63-121">有关定义新规则的详细信息，请参阅部署文档中 [Lync Server 2013 中的 "定义翻译规则](lync-server-2013-defining-translation-rules.md) "。</span><span class="sxs-lookup"><span data-stu-id="8bf63-121">For details about defining a new rule, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="8bf63-122">要编辑已与中继关联的转换规则，请单击相应的规则名称，然后单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="8bf63-122">To edit a translation rule that is already associated with the trunk, click the rule name, and then click **Show details**.</span></span> <span data-ttu-id="8bf63-123">有关详细信息，请参阅部署文档中 [Lync Server 2013 中的 "定义翻译规则](lync-server-2013-defining-translation-rules.md) "。</span><span class="sxs-lookup"><span data-stu-id="8bf63-123">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="8bf63-124">要复制现有的转换规则以作为定义新规则的起点，请单击相应的规则名称，再单击“复制”，然后单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="8bf63-124">To copy an existing translation rule to use as a starting point for defining a new rule, click the rule name and click **Copy**, and then click **Paste**.</span></span> <span data-ttu-id="8bf63-125">有关详细信息，请参阅 [在 Lync Server 2013 中定义翻译规则](lync-server-2013-defining-translation-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="8bf63-125">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span></span>
    
      - <span data-ttu-id="8bf63-126">要从中继删除某个转换规则，请突出显示相应的规则名称，然后单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="8bf63-126">To remove a translation rule from the trunk, highlight the rule name and click **Remove**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="8bf63-127">如果已在关联的中继对等方上配置了转换规则，则不要将任何转换规则与中继相关联，因为这两种规则可能会发生冲突。</span><span class="sxs-lookup"><span data-stu-id="8bf63-127">Do not associate translation rules with a trunk if you have configured translation rules on the associated trunk peer, because the two rules might conflict.</span></span>

    
    <span data-ttu-id="8bf63-128"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8bf63-128"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

