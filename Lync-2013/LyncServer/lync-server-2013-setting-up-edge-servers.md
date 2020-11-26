---
title: Lync Server 2013：设置边缘服务器
description: Lync Server 2013：设置边缘服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Edge Servers
ms:assetid: 09a22919-e36f-4122-8f0d-8d041198912d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398147(v=OCS.15)
ms:contentKeyID: 48183354
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e25c40e8d642d38b38afbab35225b2c7dda4d68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423979"
---
# <a name="setting-up-edge-servers-in-lync-server-2013"></a><span data-ttu-id="d052c-103">在 Lync Server 2013 中设置边缘服务器</span><span class="sxs-lookup"><span data-stu-id="d052c-103">Setting up Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d052c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d052c-104">

<span> </span></span></span>

<span data-ttu-id="d052c-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="d052c-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="d052c-106">设置边缘服务器所需的主要任务与安装单个边缘服务器或负载平衡的边缘服务器池相同，但硬件负载平衡的边缘服务器池需要部署负载平衡器和在多台边缘服务器上复制设置的其他步骤。</span><span class="sxs-lookup"><span data-stu-id="d052c-106">The primary tasks required to set up Edge Servers are the same for installing a single Edge Server or a load-balanced pool of Edge Servers, except that a pool of hardware load balanced Edge Servers requires deployment of the load balancers and additional steps for replicating the set up on multiple Edge Servers.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d052c-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="d052c-107">In This Section</span></span>

  - [<span data-ttu-id="d052c-108">在 Lync Server 2013 中设置边缘服务器的网络接口</span><span class="sxs-lookup"><span data-stu-id="d052c-108">Set up network interfaces for Edge Servers in Lync Server 2013</span></span>](lync-server-2013-set-up-network-interfaces-for-edge-servers.md)

  - [<span data-ttu-id="d052c-109">在 Lync Server 2013 边缘服务器上安装必备软件</span><span class="sxs-lookup"><span data-stu-id="d052c-109">Install prerequisite software on Edge Servers for Lync Server 2013</span></span>](lync-server-2013-install-prerequisite-software-on-edge-servers.md)

  - [<span data-ttu-id="d052c-110">导出 Lync Server 2013 拓扑并将其复制到外部媒体以用于边缘安装</span><span class="sxs-lookup"><span data-stu-id="d052c-110">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

  - [<span data-ttu-id="d052c-111">安装适用于 Lync Server 2013 的边缘服务器</span><span class="sxs-lookup"><span data-stu-id="d052c-111">Install Edge Servers for Lync Server 2013</span></span>](lync-server-2013-install-edge-servers.md)

  - [<span data-ttu-id="d052c-112">为 Lync Server 2013 设置边缘证书</span><span class="sxs-lookup"><span data-stu-id="d052c-112">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)

  - [<span data-ttu-id="d052c-113">在 Lync Server 2013 中启动边缘服务器</span><span class="sxs-lookup"><span data-stu-id="d052c-113">Start Edge Servers in Lync Server 2013</span></span>](lync-server-2013-start-edge-servers.md)

  - [<span data-ttu-id="d052c-114">为 Lync Server 2013 设置反向代理服务器</span><span class="sxs-lookup"><span data-stu-id="d052c-114">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)

<span data-ttu-id="d052c-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d052c-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

