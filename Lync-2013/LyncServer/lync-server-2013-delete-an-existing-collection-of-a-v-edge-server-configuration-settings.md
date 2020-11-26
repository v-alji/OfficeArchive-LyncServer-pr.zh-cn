---
title: 删除 A/V 边缘服务器配置设置的现有集合
description: 删除 A/V 边缘服务器配置设置的现有集合。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of A/V Edge Server configuration settings
ms:assetid: 668d3613-e464-4b68-967a-cfff90b9ce4b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688077(v=OCS.15)
ms:contentKeyID: 49733673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7fe444e8bcb7e7e8e2633e59c23aeb2e80e9b98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430572"
---
# <a name="delete-an-existing-collection-of-av-edge-server-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="b736f-103">在 Lync Server 2013 中删除 A/V 边缘服务器配置设置的现有集合</span><span class="sxs-lookup"><span data-stu-id="b736f-103">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b736f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b736f-104">

<span> </span></span></span>

<span data-ttu-id="b736f-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b736f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b736f-106">A/V 边缘服务为登录到你的组织网络的用户提供了一种方式 () 与外部用户共享音频和视频 (未登录到你的组织网络) 的用户。</span><span class="sxs-lookup"><span data-stu-id="b736f-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="b736f-107">A/V 边缘服务主要通过使用 A/V 边缘配置设置进行管理，可以在网站范围或服务范围内配置的设置 (也可以为单个 A/V 边缘服务器) 进行配置。</span><span class="sxs-lookup"><span data-stu-id="b736f-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="b736f-108">安装 Lync Server 时，将为你创建一个/V 边缘配置设置的全局集合。</span><span class="sxs-lookup"><span data-stu-id="b736f-108">When you install Lync Server, a global collection of A/V Edge configuration settings is created for you.</span></span> <span data-ttu-id="b736f-109">无法删除此全局集合。</span><span class="sxs-lookup"><span data-stu-id="b736f-109">This global collection cannot be deleted.</span></span> <span data-ttu-id="b736f-110">但是，你可以使用 Windows PowerShell 和 Remove-CsAVEdgeConfiguration cmdlet "重置" 全局集合;这只意味着全局集合中的所有属性值都将重置为其默认值。</span><span class="sxs-lookup"><span data-stu-id="b736f-110">However, you can use the Windows PowerShell and the Remove-CsAVEdgeConfiguration cmdlet to "reset" the global collection; that simply means that all the property values in the global collection will be reset to their default value.</span></span> <span data-ttu-id="b736f-111">例如，如果您已将 MaxTokenLifetime 属性设置为16小时，则该属性将重置为其默认值8小时。</span><span class="sxs-lookup"><span data-stu-id="b736f-111">For example, if you have set the MaxTokenLifetime property for 16 hours, that property will be reset to its default value of 8 hours.</span></span>

<span data-ttu-id="b736f-112">但是，你可以使用 Remove-CsAVEdgeConfiguration cmdlet 删除你在网站范围或服务范围内创建的自定义设置集合。</span><span class="sxs-lookup"><span data-stu-id="b736f-112">However, custom settings collections that you have created at either the site scope or the service scope can be deleted by using the Remove-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="b736f-113">如果您删除网站设置，则该网站中的 A/V 边缘服务器将由全局设置管理。</span><span class="sxs-lookup"><span data-stu-id="b736f-113">If you delete site settings then A/V Edge servers in that site will be managed by the global settings.</span></span> <span data-ttu-id="b736f-114">如果你删除了服务范围设置，则该服务器将由其网站设置（如果存在）或全局设置管理（如果没有可用的网站设置）。</span><span class="sxs-lookup"><span data-stu-id="b736f-114">If you delete service-scope settings,, that server will then be managed by its site settings, if they exist, or by the global settings if no site settings are available.</span></span>

<span data-ttu-id="b736f-115">有关详细信息，请参阅 [CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15)) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="b736f-115">For more information, see the help topic for the [Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15)) cmdlet.</span></span>

<div>

## <a name="to-reset-the-global-collection"></a><span data-ttu-id="b736f-116">重置全局集合</span><span class="sxs-lookup"><span data-stu-id="b736f-116">To reset the global collection</span></span>

  - <span data-ttu-id="b736f-117">以下命令将重置 A/V 边缘配置设置的全局集合：</span><span class="sxs-lookup"><span data-stu-id="b736f-117">The following command resets the global collection of A/V Edge configuration settings:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "global"

</div>

<div>

## <a name="to-remove-a-collection-from-the-site-scope"></a><span data-ttu-id="b736f-118">从网站范围中删除集合</span><span class="sxs-lookup"><span data-stu-id="b736f-118">To remove a collection from the site scope</span></span>

  - <span data-ttu-id="b736f-119">此命令将删除应用于 Redmond 网站的 A/V 边缘配置设置：</span><span class="sxs-lookup"><span data-stu-id="b736f-119">This command removes the A/V Edge configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-a-collection-from-the-service-scope"></a><span data-ttu-id="b736f-120">从服务范围中删除集合</span><span class="sxs-lookup"><span data-stu-id="b736f-120">To remove a collection from the service scope</span></span>

  - <span data-ttu-id="b736f-121">此命令将删除应用到 A/V 边缘服务器 atl-edge-001.litwareinc.com 的设置：</span><span class="sxs-lookup"><span data-stu-id="b736f-121">This command removes the settings applied to the A/V Edge server atl-edge-001.litwareinc.com:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b736f-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b736f-122">See Also</span></span>


[<span data-ttu-id="b736f-123">返回 Lync Server 2013 中的 A/V 边缘服务器配置信息</span><span class="sxs-lookup"><span data-stu-id="b736f-123">Return A/V Edge Server configuration information in Lync Server 2013</span></span>](lync-server-2013-return-a-v-edge-server-configuration-information.md)  
[<span data-ttu-id="b736f-124">在 Lync Server 2013 中创建或修改 A/V 边缘服务器配置设置的集合</span><span class="sxs-lookup"><span data-stu-id="b736f-124">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="b736f-125">Lync Server 2013 中的音频/视频 (A/V) 边缘服务器</span><span class="sxs-lookup"><span data-stu-id="b736f-125">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
<span data-ttu-id="b736f-126">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="b736f-126">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span></span>  
  

<span data-ttu-id="b736f-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b736f-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

