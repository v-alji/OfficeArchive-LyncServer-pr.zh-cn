---
title: Lync Server 2013：指定可用于登录 Lync Server 2013 的客户端应用程序
description: Lync Server 2013：指定可用于登录 Lync Server 2013 的客户端应用程序。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Specifying the client applications that can be used to log on to Lync Server 2013
ms:assetid: d256a581-9a48-4d1a-82cc-2e1f520d7d2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182591(v=OCS.15)
ms:contentKeyID: 48185450
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 907f4b99f1aa87ccee62ad39fdaccad1aa9d256d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441583"
---
# <a name="specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013"></a><span data-ttu-id="dc503-103">指定可用于登录 Lync Server 2013 的客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="dc503-103">Specifying the client applications that can be used to log on to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc503-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc503-104">

<span> </span></span></span>

<span data-ttu-id="dc503-105">_**主题上次修改时间：** 2012-12-11_</span><span class="sxs-lookup"><span data-stu-id="dc503-105">_**Topic Last Modified:** 2012-12-11_</span></span>

<span data-ttu-id="dc503-106">Lync Server 2013 使你能够指定你的环境支持的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="dc503-106">Lync Server 2013 enables you to specify the version of clients that are supported in your environment.</span></span> <span data-ttu-id="dc503-107">使用客户端版本策略可以帮助降低与支持多个客户端版本相关的成本。</span><span class="sxs-lookup"><span data-stu-id="dc503-107">Using client version policies can help reduce the costs associated with supporting multiple client versions.</span></span> <span data-ttu-id="dc503-108">它还可以改进整体用户体验，因为当客户端的早期版本和更高版本的客户端交互时，可用的功能可以受到较早版本的客户端的限制。</span><span class="sxs-lookup"><span data-stu-id="dc503-108">It can also improve the overall user experience, because when earlier and later versions of clients interact, the available features can be limited by the earlier version of the client.</span></span>

<span data-ttu-id="dc503-109">客户端版本控制有三个组件：</span><span class="sxs-lookup"><span data-stu-id="dc503-109">There are three components of client version control:</span></span>

  - <span data-ttu-id="dc503-110">客户端版本配置设置用于打开或关闭客户端版本控制，无论是全局还是针对特定网站。</span><span class="sxs-lookup"><span data-stu-id="dc503-110">Client version configuration settings are used to turn client version control on or off, either globally or for particular sites.</span></span>

  - <span data-ttu-id="dc503-111">客户端版本策略用于全局分配一组规则，或分配给特定网站、池或用户组。</span><span class="sxs-lookup"><span data-stu-id="dc503-111">Client version policies are used to assign a set of rules globally, or to a particular site, pool, or group of users.</span></span>

  - <span data-ttu-id="dc503-112">客户端版本策略规则构成了客户端版本策略，用于定义当用户尝试使用特定客户端和客户端版本登录时应采取的操作。</span><span class="sxs-lookup"><span data-stu-id="dc503-112">Client version policy rules make up a client version policy, and are used to define the actions that should be taken when users attempt to log on with specific clients and client versions.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dc503-113">由于匿名用户未与用户、站点或服务关联，因此匿名用户仅受全局级别策略的影响。</span><span class="sxs-lookup"><span data-stu-id="dc503-113">Because anonymous users are not associated with a user, site, or service, anonymous users are affected by global-level policies only.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="dc503-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="dc503-114">In This Section</span></span>

  - [<span data-ttu-id="dc503-115">Lync Server 2013 中的客户端版本配置设置</span><span class="sxs-lookup"><span data-stu-id="dc503-115">Client version configuration settings in Lync Server 2013</span></span>](lync-server-2013-client-version-configuration-settings.md)

  - [<span data-ttu-id="dc503-116">Lync Server 2013 中的客户端版本策略</span><span class="sxs-lookup"><span data-stu-id="dc503-116">Client version policies in Lync Server 2013</span></span>](lync-server-2013-client-version-policies.md)

  - [<span data-ttu-id="dc503-117">Lync Server 2013 中的客户端版本规则</span><span class="sxs-lookup"><span data-stu-id="dc503-117">Client version rules in Lync Server 2013</span></span>](lync-server-2013-client-version-rules.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dc503-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc503-118">See Also</span></span>


[<span data-ttu-id="dc503-119">在 Lync Server 2013 中管理设备、电话和客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="dc503-119">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="dc503-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc503-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

