---
title: Lync Server 2013：验证语音号码规范化和路由
description: Lync Server 2013：验证语音号码规范化和路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating voice number normalization and routing
ms:assetid: a6a825c7-6928-4e80-b7e9-803b7f7ebd13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720922(v=OCS.15)
ms:contentKeyID: 63969633
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f28f679cbb991bdb90362eb61c9c7b68879791e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438622"
---
# <a name="validating-voice-number-normalization-and-routing-in-lync-server-2013"></a><span data-ttu-id="7c8a0-103">在 Lync Server 2013 中验证语音号码标准化和路由</span><span class="sxs-lookup"><span data-stu-id="7c8a0-103">Validating voice number normalization and routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c8a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c8a0-104">

<span> </span></span></span>

<span data-ttu-id="7c8a0-105">_**主题上次修改时间：** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="7c8a0-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="7c8a0-106">正确的数字规范化和路由对于功能企业语音环境非常重要。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-106">Correct number normalization and routing is very important for functional Enterprise Voice environment.</span></span> <span data-ttu-id="7c8a0-107">尤其是在从专用分支 exchange 迁移 (PBX) 到独立的 Lync Server 环境期间，成功迁移的一个关键是展示并记录所有现有的拨号规则，并创建相应的规范化规则、语音策略、电话使用情况和路由。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-107">Especially during migrations from private branch exchange (PBX) to stand-alone Lync Server environment, one of the keys to successful migration is to reveal and document all existing dialing rules, and create appropriate normalization rules, voice policies, phone usages and routes.</span></span>

<span data-ttu-id="7c8a0-108">验证数字规范化和路由不仅在迁移过程中很重要，还在系统的正常稳定操作期间也很重要。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-108">Validating number normalization and routing is important not only during migrations but also during normal, stable operation of the system.</span></span>

<span data-ttu-id="7c8a0-109">我们建议每天使用 Lync Server 控制面板执行此验证，从针对 Lync Server 全局设置中发布的当前规范化规则集开发一组强大的测试事例开始。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-109">We recommend conducting this validation daily by using the Lync Server Control Panel, starting with developing a robust set of test cases against the current set of normalization rules that were published in the Lync Server global settings.</span></span> <span data-ttu-id="7c8a0-110">应每天运行这些测试用例，以突出显示已进行并提交到拨号计划的任何不需要的更改。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-110">These test cases should be run daily to highlight any unwanted changes that were made and committed to the dial plan.</span></span>

<span data-ttu-id="7c8a0-111">Lync Server 控制面板还可帮助你直观、测试、更改、存档和共享有关语音路由和更改企业语音数字规范化规则、拨号计划、语音策略和路线的配置信息。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-111">Lync Server Control Panel also helps you visualize, test, change, archive, and share configuration information about voice routing and in changing Enterprise Voice number normalization rules, dial plans, voice policy, and routes.</span></span> <span data-ttu-id="7c8a0-112">它具有执行以下操作的其他功能：</span><span class="sxs-lookup"><span data-stu-id="7c8a0-112">It has additional features for doing the following:</span></span>

  - <span data-ttu-id="7c8a0-113">导出和导入或备份系统之间的语音路由数据。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-113">Exporting and importing or backing up voice routing data between systems.</span></span>

  - <span data-ttu-id="7c8a0-114">在将配置更改上载到实时系统之前对其进行测试。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-114">Testing configuration changes before uploading them to a live system.</span></span>

  - <span data-ttu-id="7c8a0-115">创建和运行配置测试案例以帮助确保在对已部署的系统进行更改之后，在对其进行更改之后，路由数据的可用性。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-115">Creating and running configuration test cases to help ensure the usability of routing data after you make changes to it, but before committing them the changes to a deployed system.</span></span>

  - <span data-ttu-id="7c8a0-116">创建和更改数字规范化规则、位置配置文件、语音策略和路由数据，而无需编写所需的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-116">Creating and changing number normalization rules, location profiles, voice policy, and routing data without writing the necessary regular expressions.</span></span>

  - <span data-ttu-id="7c8a0-117">分析位置配置文件，以便与 Lync Server Phone Edition 兼容。</span><span class="sxs-lookup"><span data-stu-id="7c8a0-117">Analyzing a location profile for compatibility with the Lync Server Phone Edition.</span></span>

  - <span data-ttu-id="7c8a0-118">有关语音路由测试的详细信息，请参阅 [Lync Server 2013 中的测试语音路由](lync-server-2013-test-voice-routing.md)</span><span class="sxs-lookup"><span data-stu-id="7c8a0-118">More information about voice routing tests can be found at [Test voice routing in Lync Server 2013](lync-server-2013-test-voice-routing.md)</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="7c8a0-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7c8a0-119">See Also</span></span>


[<span data-ttu-id="7c8a0-120">在 Lync Server 2013 中测试语音路由</span><span class="sxs-lookup"><span data-stu-id="7c8a0-120">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="7c8a0-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c8a0-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

