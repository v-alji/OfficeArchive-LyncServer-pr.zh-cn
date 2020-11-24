---
title: Lync Server 2013：配置电话拨入式会议的拨号计划
description: Lync Server 2013：配置电话拨入式会议的拨号计划。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial plans for dial-in conferencing
ms:assetid: a3e0958e-384f-43e5-b4c9-686b6ecac7ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412768(v=OCS.15)
ms:contentKeyID: 48185051
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28123f905288ce35b6f470168962a3d8e6faa22b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392402"
---
# <a name="configure-dial-plans-for-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="df655-103">在 Lync Server 2013 中配置电话拨入式会议的拨号计划</span><span class="sxs-lookup"><span data-stu-id="df655-103">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df655-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df655-104">

<span> </span></span></span>

<span data-ttu-id="df655-105">_**主题上次修改时间：** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="df655-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="df655-106">部署电话拨入式会议时，需要创建或修改用于路由拨入访问电话号码的一个或多个拨号计划。</span><span class="sxs-lookup"><span data-stu-id="df655-106">When you deploy dial-in conferencing, you need to create or modify one or more dial plans for routing dial-in access phone numbers.</span></span> <span data-ttu-id="df655-107">请确保每个拨号计划中至少有一个规范化规则将电话分机号转换为以164格式表示的完整电话号码。</span><span class="sxs-lookup"><span data-stu-id="df655-107">Make sure that at least one normalization rule in each dial plan converts telephone extensions into complete phone numbers in E.164 format.</span></span> <span data-ttu-id="df655-108">电话拨入式会议的用户作为通过身份验证的企业用户，输入其个人标识号 (PIN) 和电话号码来加入会议。</span><span class="sxs-lookup"><span data-stu-id="df655-108">Users of dial-in conferencing join conferences as authenticated enterprise users by entering their personal identification number (PIN) and their phone number.</span></span> <span data-ttu-id="df655-109">你需要规范化规则来将分机号转换为完整电话号码，这样用户只要输入电话分机号，就可通过身份验证。</span><span class="sxs-lookup"><span data-stu-id="df655-109">You need a normalization rule to convert extensions into complete phone numbers so that users can be authenticated when they enter just a telephone extension.</span></span>

<span data-ttu-id="df655-110">若要设置电话拨入式会议的拨号计划，请执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="df655-110">To set up dial plans for dial-in conferencing, do the following:</span></span>

  - <span data-ttu-id="df655-111">无论是否部署企业语音，都需修改全局拨号计划，以添加电话拨入式会议区域，并确保规范化规则准确转换拨入访问号码。</span><span class="sxs-lookup"><span data-stu-id="df655-111">Whether or not you deploy Enterprise Voice, modify the global dial plan to add a dial-in conferencing region and to make sure that a normalization rule accurately converts your dial-in access numbers.</span></span> <span data-ttu-id="df655-112">有关详细说明，请参阅 [在 Lync Server 2013 中修改拨号计划](lync-server-2013-modify-a-dial-plan.md)。</span><span class="sxs-lookup"><span data-stu-id="df655-112">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

  - <span data-ttu-id="df655-113">如果不部署企业语音，请创建电话拨入式会议访问号码的拨号计划。</span><span class="sxs-lookup"><span data-stu-id="df655-113">If you did not deploy Enterprise Voice, create dial plans for your dial-in conferencing access numbers.</span></span> <span data-ttu-id="df655-114">确保其中包含电话拨入式会议区域。</span><span class="sxs-lookup"><span data-stu-id="df655-114">Be sure to include a dial-in conferencing region.</span></span> <span data-ttu-id="df655-115">有关详细说明，请参阅 [在 Lync Server 2013 中创建拨号计划](lync-server-2013-create-a-dial-plan.md)。</span><span class="sxs-lookup"><span data-stu-id="df655-115">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

  - <span data-ttu-id="df655-116">如果已部署企业语音，请根据需要修改企业语音拨号计划以纳入区域，并对拨入访问号码使用相应的规范化规则。</span><span class="sxs-lookup"><span data-stu-id="df655-116">If you deployed Enterprise Voice, modify Enterprise Voice dial plans as necessary to include regions and use appropriate normalization rules for dial-in access numbers.</span></span> <span data-ttu-id="df655-117">有关详细说明，请参阅 [在 Lync Server 2013 中修改拨号计划](lync-server-2013-modify-a-dial-plan.md)。</span><span class="sxs-lookup"><span data-stu-id="df655-117">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span> <span data-ttu-id="df655-118">还可以创建仅用于拨入访问号码的专用拨号计划。</span><span class="sxs-lookup"><span data-stu-id="df655-118">You can also create dedicated dial plans that are used only for dial-in access numbers.</span></span> <span data-ttu-id="df655-119">有关详细说明，请参阅 [在 Lync Server 2013 中创建拨号计划](lync-server-2013-create-a-dial-plan.md)。</span><span class="sxs-lookup"><span data-stu-id="df655-119">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

<span data-ttu-id="df655-120">有关规划区域的详细信息，请参阅规划文档中 [Lync Server 2013 中的电话拨入式会议要求](lync-server-2013-dial-in-conferencing-requirements.md) 。</span><span class="sxs-lookup"><span data-stu-id="df655-120">For details about planning regions, see [Dial-in conferencing requirements in Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="df655-121">本节内容</span><span class="sxs-lookup"><span data-stu-id="df655-121">In This Section</span></span>

  - [<span data-ttu-id="df655-122">在 Lync Server 2013 中查看拨号计划信息</span><span class="sxs-lookup"><span data-stu-id="df655-122">View dial plan information in Lync Server 2013</span></span>](lync-server-2013-view-dial-plan-information.md)

  - [<span data-ttu-id="df655-123">在 Lync Server 2013 中创建拨号计划</span><span class="sxs-lookup"><span data-stu-id="df655-123">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)

  - [<span data-ttu-id="df655-124">在 Lync Server 2013 中修改拨号计划</span><span class="sxs-lookup"><span data-stu-id="df655-124">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)

  - [<span data-ttu-id="df655-125">在 Lync Server 2013 中定义规范化规则</span><span class="sxs-lookup"><span data-stu-id="df655-125">Defining normalization rules in Lync Server 2013</span></span>](lync-server-2013-defining-normalization-rules.md)

<span data-ttu-id="df655-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df655-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

