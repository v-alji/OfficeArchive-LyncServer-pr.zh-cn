---
title: Lync Server 2013： (可选) 验证响应组部署
description: Lync Server 2013： (可选) 验证响应组部署。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Response Group deployment
ms:assetid: 202ca4ab-8e6d-44a4-b7c8-071133074feb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687989(v=OCS.15)
ms:contentKeyID: 49733579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cfe15026bc1fcfbe10b593987d2717fc0dc8104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424847"
---
# <a name="optional-verify-response-group-deployment-in-lync-server-2013"></a><span data-ttu-id="8ddd9-103"> (可选) 在 Lync Server 2013 中验证响应组部署</span><span class="sxs-lookup"><span data-stu-id="8ddd9-103">(Optional) Verify Response Group deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ddd9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ddd9-104">

<span> </span></span></span>

<span data-ttu-id="8ddd9-105">_**主题上次修改时间：** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="8ddd9-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="8ddd9-106">配置响应组后，你需要验证配置，以确保你的响应组按预期工作。</span><span class="sxs-lookup"><span data-stu-id="8ddd9-106">After you configure Response Group, you need to verify the configuration to make sure your response groups work as expected.</span></span> <span data-ttu-id="8ddd9-107">至少应使用以下用户类型验证以下方案：</span><span class="sxs-lookup"><span data-stu-id="8ddd9-107">At minimum, verify the following scenarios by using the following types of users:</span></span>

<span data-ttu-id="8ddd9-108">**用户**</span><span class="sxs-lookup"><span data-stu-id="8ddd9-108">**Users**</span></span>

  - <span data-ttu-id="8ddd9-109">Lync Server 2013 上托管的用户</span><span class="sxs-lookup"><span data-stu-id="8ddd9-109">A user who is homed on Lync Server 2013</span></span>

  - <span data-ttu-id="8ddd9-110">使用公用电话交换网 (PSTN) 的外部用户</span><span class="sxs-lookup"><span data-stu-id="8ddd9-110">An external user who uses the public switched telephone network (PSTN)</span></span>

  - <span data-ttu-id="8ddd9-111">在 Lync Server 2013 上托管的代理</span><span class="sxs-lookup"><span data-stu-id="8ddd9-111">An agent who is homed on Lync Server 2013</span></span>

<span data-ttu-id="8ddd9-112">**应用场景**</span><span class="sxs-lookup"><span data-stu-id="8ddd9-112">**Scenarios**</span></span>

  - <span data-ttu-id="8ddd9-113">Lync Server 2013 用户调用响应组。</span><span class="sxs-lookup"><span data-stu-id="8ddd9-113">The Lync Server 2013 user calls the response group.</span></span>

  - <span data-ttu-id="8ddd9-114">外部用户呼叫响应组。</span><span class="sxs-lookup"><span data-stu-id="8ddd9-114">The external user calls the response group.</span></span>

  - <span data-ttu-id="8ddd9-115">用户在代理处理其他呼叫时呼叫响应组，并进入队列。</span><span class="sxs-lookup"><span data-stu-id="8ddd9-115">A user calls the response group while the agent is on another call and goes to the queue.</span></span>

<span data-ttu-id="8ddd9-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ddd9-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

