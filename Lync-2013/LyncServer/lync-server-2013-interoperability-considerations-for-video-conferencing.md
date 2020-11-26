---
title: Lync Server 2013：视频会议的互操作性注意事项
description: Lync Server 2013：视频会议的互操作性注意事项。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Interoperability considerations for video conferencing
ms:assetid: 31ead3b5-ed95-42d4-96e2-7d9403d5c026
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204790(v=OCS.15)
ms:contentKeyID: 48183782
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89675954ea4c4f188f50aab8fb2cb49494bcc247
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426786"
---
# <a name="interoperability-considerations-for-video-conferencing-in-lync-server-2013"></a><span data-ttu-id="e7de0-103">Lync Server 2013 中的视频会议的互操作性注意事项</span><span class="sxs-lookup"><span data-stu-id="e7de0-103">Interoperability considerations for video conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7de0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7de0-104">

<span> </span></span></span>

<span data-ttu-id="e7de0-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="e7de0-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="e7de0-106">本部分介绍了当旧客户端与 Lync Server 2013 池或 Lync Server 2013 客户端和旧版池之间存在互操作时，迁移的共存阶段中的用户体验。</span><span class="sxs-lookup"><span data-stu-id="e7de0-106">This section describes the user experience during the coexistence phase of migration, when there is interoperability between legacy clients and a Lync Server 2013 pool or Lync Server 2013 clients and a legacy pool.</span></span>

<div>

## <a name="lync-server-2013-pools"></a><span data-ttu-id="e7de0-107">Lync Server 2013 池</span><span class="sxs-lookup"><span data-stu-id="e7de0-107">Lync Server 2013 Pools</span></span>

<span data-ttu-id="e7de0-108">当在 Lync Server 2013 池中使用旧客户端时，用户将遇到以下行为：</span><span class="sxs-lookup"><span data-stu-id="e7de0-108">Users will experience the following behavior when a legacy client is used in a Lync Server 2013 pool:</span></span>

  - <span data-ttu-id="e7de0-109">对于两方呼叫，视频分辨率与旧版池中的相同。</span><span class="sxs-lookup"><span data-stu-id="e7de0-109">For two-party calls, video resolution is the same as in the legacy pool.</span></span>

  - <span data-ttu-id="e7de0-110">对于多方会议，视频分辨率和视频会议功能与旧版池中的功能相同。</span><span class="sxs-lookup"><span data-stu-id="e7de0-110">For multiparty conferences, video resolution and video conferencing features are the same as in the legacy pool.</span></span> <span data-ttu-id="e7de0-111">库视图和高分辨率不可用。</span><span class="sxs-lookup"><span data-stu-id="e7de0-111">Gallery View and high resolution are not available.</span></span>

</div>

<div>

## <a name="legacy-pools"></a><span data-ttu-id="e7de0-112">旧版池</span><span class="sxs-lookup"><span data-stu-id="e7de0-112">Legacy Pools</span></span>

<span data-ttu-id="e7de0-113">当在旧版池中使用 Lync Server 2013 客户端时，用户将遇到以下行为：</span><span class="sxs-lookup"><span data-stu-id="e7de0-113">Users will experience the following behavior when a Lync Server 2013 client is used in a legacy pool:</span></span>

  - <span data-ttu-id="e7de0-114">对于两方呼叫，Lync Server 2013 客户端可以使用以下新功能：</span><span class="sxs-lookup"><span data-stu-id="e7de0-114">For two-party calls, Lync Server 2013 clients can use new features as follows:</span></span>
    
      - <span data-ttu-id="e7de0-115">如果两个参与者都在使用 Lync Server 2013 客户端，则可以使用 h-p。</span><span class="sxs-lookup"><span data-stu-id="e7de0-115">H.264 is available if both participants are using Lync Server 2013 clients.</span></span>
    
      - <span data-ttu-id="e7de0-116">Lync Server 2013 客户端对 TotalReceiveVideoBitRateKb 使用默认值，因为旧服务器不会使用带内设置发送此信息。</span><span class="sxs-lookup"><span data-stu-id="e7de0-116">The Lync Server 2013 client uses the default value for TotalReceiveVideoBitRateKb, since the legacy server doesn’t send this information with in-band provisioning.</span></span>

  - <span data-ttu-id="e7de0-117">对于多方会议，视频分辨率和视频会议功能与旧版池中的旧客户体验相同。</span><span class="sxs-lookup"><span data-stu-id="e7de0-117">For multiparty conferences, video resolution and video conferencing features are the same as experienced by a legacy client in the legacy pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e7de0-118">当旧式服务器托管 Lync Server 2013 客户端时，可以配置视频会议带宽，以便该池中的所有用户仅收到低分辨率视频，但发送高分辨率视频。</span><span class="sxs-lookup"><span data-stu-id="e7de0-118">When a legacy server hosts a Lync Server 2013 client, it's possible to configure video conferencing bandwidth so that all users on the pool receive only low-resolution video, but send high-resolution video.</span></span> <span data-ttu-id="e7de0-119">例如，在媒体配置中将 MaxVideoRateAllowed 设置为 CIF-250K 时，在会议策略中将 VideoBitRateKb 设置为 2000 kbps。</span><span class="sxs-lookup"><span data-stu-id="e7de0-119">An example of this is when MaxVideoRateAllowed is set to CIF-250K in the media configuration and VideoBitRateKb is set to 2000 kbps in conferencing policy.</span></span> <span data-ttu-id="e7de0-120">这种情况下的网络效果是不可能对池中的用户进行高分辨率。</span><span class="sxs-lookup"><span data-stu-id="e7de0-120">The net effect in this situation is that high resolution is not possible for users on the pool.</span></span><BR><span data-ttu-id="e7de0-121">由于 MaxVideoRateAllowed 不再用于 Lync Server 2013 客户端，因此它无法阻止 Lync Server 2013 客户端请求高分辨率视频。</span><span class="sxs-lookup"><span data-stu-id="e7de0-121">Because MaxVideoRateAllowed is no longer used for Lync Server 2013 clients, it cannot prevent Lync Server 2013 clients from requesting high-resolution video.</span></span> <span data-ttu-id="e7de0-122">请改为将 VideoBitRateKb 中的所有用户的会议策略设置为与 MaxVideoRateAllowed (相同的值，即 CIF 设置为 250 kbps 或将 VGA 设置为 600 kbps，或者将 HD 设置为 1500 kbps) 。</span><span class="sxs-lookup"><span data-stu-id="e7de0-122">Instead, set VideoBitRateKb in conferencing policy for all users on the pool to the same value as MaxVideoRateAllowed (that is, CIF is set to 250 kbps, or VGA is set to 600 kbps, or HD is set to 1500 kbps).</span></span>



<span data-ttu-id="e7de0-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7de0-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

