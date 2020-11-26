---
title: Lync Server 2013：返回 A/V 边缘服务器配置信息
description: Lync Server 2013：返回 A/V 边缘服务器配置信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Return A/V Edge Server configuration information
ms:assetid: b041f5a4-2387-4075-846c-ec4f99640903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721850(v=OCS.15)
ms:contentKeyID: 49733783
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4f72fccfe51b946dc0dc285aee12a07e59c844b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442472"
---
# <a name="return-av-edge-server-configuration-information-in-lync-server-2013"></a><span data-ttu-id="c3193-103">返回 Lync Server 2013 中的 A/V 边缘服务器配置信息</span><span class="sxs-lookup"><span data-stu-id="c3193-103">Return A/V Edge Server configuration information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3193-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3193-104">

<span> </span></span></span>

<span data-ttu-id="c3193-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="c3193-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="c3193-106">A/V 边缘服务为登录到你的组织网络的用户提供了一种方式 () 与外部用户共享音频和视频 (未登录到你的组织网络) 的用户。</span><span class="sxs-lookup"><span data-stu-id="c3193-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="c3193-107">A/V 边缘服务主要通过使用 A/V 边缘配置设置进行管理，可以在网站范围或服务范围内配置的设置 (也可以为单个 A/V 边缘服务器) 进行配置。</span><span class="sxs-lookup"><span data-stu-id="c3193-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="c3193-108">若要返回有关在你的组织中使用的 A/V 边缘配置设置的信息，必须使用 Windows PowerShell 和 Get-CsAVEdgeConfiguration cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3193-108">To return information about the A/V Edge configuration settings in use in your organization, you must use Windows PowerShell and the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="c3193-109">有关详细信息，请参阅 [CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="c3193-109">For more information, see the help topic for the [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) cmdlet.</span></span>

<span data-ttu-id="c3193-110">从 Get-CsAVEdgeConfiguration cmdlet 返回的信息将如下所示：</span><span class="sxs-lookup"><span data-stu-id="c3193-110">Information returned from the Get-CsAVEdgeConfiguration cmdlet will look similar to this:</span></span>

    Identity              : Global
    MaxTokenLifetime      : 08:00:00
    MaxBandwidthPerUserKb : 10000
    MaxBandwidthPerPortKb : 3000

<div>

## <a name="to-return-information-for-all-your-av-edge-configuration-settings"></a><span data-ttu-id="c3193-111">返回所有 A/V 边缘配置设置的信息</span><span class="sxs-lookup"><span data-stu-id="c3193-111">To return information for all your A/V Edge configuration settings</span></span>

  - <span data-ttu-id="c3193-112">以下命令将返回你的组织中当前使用的所有 A/V 边缘配置设置的相关信息：</span><span class="sxs-lookup"><span data-stu-id="c3193-112">The following command returns information about all the A/V Edge configuration settings currently in use in your organization:</span></span>
    
        Get-CsAVEdgeConfiguration

</div>

<div>

## <a name="to-return-information-for-site-scoped-av-edge-configuration-settings"></a><span data-ttu-id="c3193-113">返回网站范围的 A/V 边缘配置设置的信息</span><span class="sxs-lookup"><span data-stu-id="c3193-113">To return information for site-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="c3193-114">若要返回有关 A/V 边缘配置设置的特定集合的信息，请在运行 Get-CsAVEdgeConfiguration cmdlet 时指定该集合的标识。</span><span class="sxs-lookup"><span data-stu-id="c3193-114">To return information about a specific collection of A/V Edge configuration settings, specify the Identity of that collection when running the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="c3193-115">例如，此命令仅返回对雷德蒙站点应用的设置的信息：</span><span class="sxs-lookup"><span data-stu-id="c3193-115">For example, this command returns information only for the settings applied to the Redmond site:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-return-information-for-service-scoped-av-edge-configuration-settings"></a><span data-ttu-id="c3193-116">返回有关服务范围的 A/V 边缘配置设置的信息</span><span class="sxs-lookup"><span data-stu-id="c3193-116">To return information for service-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="c3193-117">此命令仅为应用了特定的 A/V 边缘服务器的设置返回信息：</span><span class="sxs-lookup"><span data-stu-id="c3193-117">And this command returns information only for settings applied the a specific A/V Edge server:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c3193-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c3193-118">See Also</span></span>


[<span data-ttu-id="c3193-119">在 Lync Server 2013 中创建或修改 A/V 边缘服务器配置设置的集合</span><span class="sxs-lookup"><span data-stu-id="c3193-119">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)  
[<span data-ttu-id="c3193-120">在 Lync Server 2013 中删除 A/V 边缘服务器配置设置的现有集合</span><span class="sxs-lookup"><span data-stu-id="c3193-120">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="c3193-121">Lync Server 2013 中的音频/视频 (A/V) 边缘服务器</span><span class="sxs-lookup"><span data-stu-id="c3193-121">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
  

<span data-ttu-id="c3193-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3193-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

