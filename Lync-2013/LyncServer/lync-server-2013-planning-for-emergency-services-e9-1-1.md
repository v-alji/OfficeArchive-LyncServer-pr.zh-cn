---
title: Lync Server 2013：规划紧急服务 (E9-1-1)
description: Lync Server 2013：规划紧急服务 (E9-1-1) 。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for emergency services (E9-1-1)
ms:assetid: 0a76f97b-474a-4bc1-8cd3-28c7e2bb57b9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398154(v=OCS.15)
ms:contentKeyID: 48183363
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4113b2355db0b1aade0ab6766e8ba7a5972aee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424602"
---
# <a name="planning-for-emergency-services-e9-1-1-in-lync-server-2013"></a><span data-ttu-id="8407f-103">在 Lync Server 2013 中规划紧急服务 (E9-1-1)</span><span class="sxs-lookup"><span data-stu-id="8407f-103">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8407f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8407f-104">

<span> </span></span></span>

<span data-ttu-id="8407f-105">_**主题上次修改时间：** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="8407f-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="8407f-106">Lync Server 2013 支持增强的 9-1-1 (E9 中的一种) 服务，作为企业语音部署的一部分。</span><span class="sxs-lookup"><span data-stu-id="8407f-106">Lync Server 2013 supports Enhanced 9-1-1 (E9-1-1) services within the United States as part of an Enterprise Voice deployment.</span></span> <span data-ttu-id="8407f-107">E9-1-1 是一项紧急派发功能，对于来自办公楼和其他多租户设施的呼叫，该功能可将 9-1-1 呼叫与紧急响应位置 (ERL) 相关联，紧急响应位置包含市政（即街道）地址和其他更具体的位置信息，例如楼层号。</span><span class="sxs-lookup"><span data-stu-id="8407f-107">E9-1-1 is an emergency dispatch feature that associates a 9-1-1 call with an Emergency Response Location (ERL) that consists of civic (that is, street) addresses and other more specific location information, such as floor numbers, for calls from office buildings and other multitenant facilities.</span></span> <span data-ttu-id="8407f-108">通过使用提供的 ERL，公共安全应答点 (PSAP) 可以立即向需要帮助的呼叫者派遣第一批响应者，从而降低因疏忽而将响应者指向不正确或模糊不清的位置的风险。</span><span class="sxs-lookup"><span data-stu-id="8407f-108">By using the provided ERL, a Public Safety Answering Point (PSAP) can immediately dispatch first responders to the caller in distress with reduced risk of inadvertently directing the responder to an incorrect or ambiguous location.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8407f-109">Lync 服务器具有三个高级的企业语音功能：呼叫许可控制、紧急服务 (E9-1) 和媒体旁路。</span><span class="sxs-lookup"><span data-stu-id="8407f-109">Lync Server has three advanced Enterprise Voice features: call admission control, emergency services (E9-1-1), and media bypass.</span></span> <span data-ttu-id="8407f-110">有关所有三种功能通用的计划信息的概述，请参阅 <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Lync Server 2013 中的高级企业语音功能的网络设置</A>。</span><span class="sxs-lookup"><span data-stu-id="8407f-110">For an overview of planning information that is common to all three of these features, see <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8407f-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="8407f-111">In This Section</span></span>

  - [<span data-ttu-id="8407f-112">Lync Server 2013 中的 E9-1-1 概述</span><span class="sxs-lookup"><span data-stu-id="8407f-112">Overview of E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-overview-of-e9-1-1.md)

  - [<span data-ttu-id="8407f-113">在 Lync Server 2013 中定义紧急呼叫要求</span><span class="sxs-lookup"><span data-stu-id="8407f-113">Defining your requirements for emergency calls in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-emergency-calls.md)

  - [<span data-ttu-id="8407f-114">Lync Server 2013 中的 E9 的部署清单-1</span><span class="sxs-lookup"><span data-stu-id="8407f-114">Deployment checklist for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-e9-1-1.md)

<span data-ttu-id="8407f-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8407f-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

