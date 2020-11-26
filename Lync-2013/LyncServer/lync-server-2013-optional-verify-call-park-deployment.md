---
title: Lync Server 2013： (可选) 验证呼叫寄存部署
description: Lync Server 2013： (可选) 验证呼叫寄存部署。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Call Park deployment
ms:assetid: fcfe0962-1a9c-4cbd-847c-fed40e3b1480
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413076(v=OCS.15)
ms:contentKeyID: 48185952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 772392a3a791ed57c3220d80e9bd510d8803debb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424861"
---
# <a name="optional-verify-call-park-deployment-in-lync-server-2013"></a><span data-ttu-id="a48f8-103"> (可选) 在 Lync Server 2013 中验证呼叫寄存部署</span><span class="sxs-lookup"><span data-stu-id="a48f8-103">(Optional) Verify Call Park deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a48f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a48f8-104">

<span> </span></span></span>

<span data-ttu-id="a48f8-105">_**主题上次修改时间：** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="a48f8-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="a48f8-106">安装并配置呼叫寄存后，您需要验证配置，以确保停车和检索呼叫按预期工作。</span><span class="sxs-lookup"><span data-stu-id="a48f8-106">After you install and configure Call Park, you need to verify the configuration to make sure that parking and retrieving calls works as expected.</span></span> <span data-ttu-id="a48f8-107">至少必须验证以下内容：</span><span class="sxs-lookup"><span data-stu-id="a48f8-107">At minimum, verify the following:</span></span>

  - <span data-ttu-id="a48f8-108">呼叫已启用呼叫寄存并让用户寄存呼叫的用户。</span><span class="sxs-lookup"><span data-stu-id="a48f8-108">Call a user who has Call Park enabled and have the user park the call.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a48f8-109">如果在执行此测试之前已在语音策略中启用了呼叫寄存，则离开呼叫的用户需要注销 Lync 服务器，然后重新登录，以便能够在转接呼叫列表中看到呼叫寄存选项。</span><span class="sxs-lookup"><span data-stu-id="a48f8-109">If you enabled Call Park in voice policy just before performing this test, the user who is parking the call needs to sign out of Lync Server, and then sign back in, to be able to see the Call Park option in the transfer call list.</span></span>

    
    </div>

  - <span data-ttu-id="a48f8-110">拨打通道号码以取回此呼叫。</span><span class="sxs-lookup"><span data-stu-id="a48f8-110">Dial the orbit number to retrieve the call.</span></span>

  - <span data-ttu-id="a48f8-p102">寄存其他呼叫，使之前寄存的呼叫超时，并且不接听回拨。验证超时的呼叫是否正确路由到为 **OnTimeoutURI** 指定的回退目标。</span><span class="sxs-lookup"><span data-stu-id="a48f8-p102">Park another call, let the parked call time out, and do not pick up the ringback. Verify that the timed-out call is correctly routed to the fallback destination that is specified for **OnTimeoutURI**.</span></span>

<span data-ttu-id="a48f8-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a48f8-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

