---
title: Lync Server 2013：配置呼叫装货组号码
description: Lync Server 2013：配置呼叫装货组号码。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure call pickup group numbers
ms:assetid: 5cc67f0b-d70d-446a-8db1-befda8671121
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945631(v=OCS.15)
ms:contentKeyID: 51541479
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ddffae2e385ce6c3fd7a700a9b94a89b1b6679f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391755"
---
# <a name="configure-call-pickup-group-numbers-in-lync-server-2013"></a><span data-ttu-id="6fb94-103">在 Lync Server 2013 中配置呼叫装货组号码</span><span class="sxs-lookup"><span data-stu-id="6fb94-103">Configure call pickup group numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6fb94-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6fb94-104">

<span> </span></span></span>

<span data-ttu-id="6fb94-105">_**主题上次修改时间：** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="6fb94-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="6fb94-106">组呼叫分拣基于呼叫寄存应用程序。</span><span class="sxs-lookup"><span data-stu-id="6fb94-106">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="6fb94-107">当您部署组呼叫时，可将 "呼叫公园轨道" 表配置为指定为 "呼叫装货组号码" 的电话号码范围。</span><span class="sxs-lookup"><span data-stu-id="6fb94-107">When you deploy Group Call Pickup, you configure the call park orbit table with ranges of phone numbers that are designated as call pickup group numbers.</span></span> <span data-ttu-id="6fb94-108">这些组号码是用户拨打以应答为另一个用户响铃的呼叫的号码。</span><span class="sxs-lookup"><span data-stu-id="6fb94-108">These group numbers are the numbers that users dial to pick up calls that are ringing for another user.</span></span>

<span data-ttu-id="6fb94-109">与呼叫寄存轨道号码类似，呼叫应答组号码需要是没有为其分配用户或电话的虚拟分机号。</span><span class="sxs-lookup"><span data-stu-id="6fb94-109">Like call park orbit numbers, call pickup group numbers need to be virtual extensions that have no user or phone assigned to them.</span></span> <span data-ttu-id="6fb94-110">你在其中部署组呼叫装货的每个前端池都可以具有一个或多个呼叫装货组编号范围。</span><span class="sxs-lookup"><span data-stu-id="6fb94-110">Each Front End pool where you deploy Group Call Pickup can have one or more ranges of call pickup group numbers.</span></span> <span data-ttu-id="6fb94-111">组编号范围在 Lync Server 部署中必须是全局唯一的。</span><span class="sxs-lookup"><span data-stu-id="6fb94-111">The group number ranges must be globally unique across the Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6fb94-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="6fb94-112">In This Section</span></span>

[<span data-ttu-id="6fb94-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fb94-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-group-call-pickup-number-range.md)

<span data-ttu-id="6fb94-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6fb94-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

