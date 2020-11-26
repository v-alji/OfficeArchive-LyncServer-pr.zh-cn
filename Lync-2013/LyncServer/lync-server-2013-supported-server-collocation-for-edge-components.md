---
title: Lync Server 2013：边缘组件支持的服务器并置
description: Lync Server 2013：支持的适用于 edge 组件的服务器 collocation。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423636"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a><span data-ttu-id="71874-103">Lync Server 2013 中边缘组件支持的服务器并置</span><span class="sxs-lookup"><span data-stu-id="71874-103">Supported server collocation for edge components in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71874-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71874-104">

<span> </span></span></span>

<span data-ttu-id="71874-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="71874-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="71874-106">访问边缘服务、Web 会议边缘服务、A/V 边缘服务和 XMPP 代理服务在边缘服务器上 collocated。</span><span class="sxs-lookup"><span data-stu-id="71874-106">The Access Edge service, Web Conferencing Edge service, A/V Edge service and XMPP Proxy service are collocated on the Edge Servers.</span></span> <span data-ttu-id="71874-107">以下服务器提供外部用户访问所需的函数，并且必须部署为专用服务器：</span><span class="sxs-lookup"><span data-stu-id="71874-107">The following servers provide functions needed for external user access and must be deployed as dedicated servers:</span></span>

  - <span data-ttu-id="71874-108">边缘服务器</span><span class="sxs-lookup"><span data-stu-id="71874-108">Edge Server</span></span>

  - <span data-ttu-id="71874-109">导演 (可选) </span><span class="sxs-lookup"><span data-stu-id="71874-109">Director (Optional)</span></span>

  - <span data-ttu-id="71874-110">反向代理</span><span class="sxs-lookup"><span data-stu-id="71874-110">Reverse proxy</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="71874-111">反向代理无需专门为 Lync Server 2013 提供服务。</span><span class="sxs-lookup"><span data-stu-id="71874-111">The reverse proxy does not need to be dedicated to serving only Lync Server 2013.</span></span> <span data-ttu-id="71874-112">例如，你可以提供用于发布 Lync Server Web 服务的服务，并同时为另一个网站提供已发布的网站，该网站与 Lync 服务器根本没有任何关系。</span><span class="sxs-lookup"><span data-stu-id="71874-112">For example, you can provide services to publish the Lync Server Web services, and concurrently provide a published Web site for another Web site that has no bearing on Lync Server at all.</span></span> <span data-ttu-id="71874-113">如果外围网络中已有反向代理服务器支持其他服务，则可以将其用于 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="71874-113">If you already have a reverse proxy server in the perimeter network to support other services, you can use it for Lync Server 2013.</span></span>



<span data-ttu-id="71874-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71874-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

