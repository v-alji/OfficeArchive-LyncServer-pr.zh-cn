---
title: Lync Server 2013：在外围网络外部的观察程序节点上安装证书
description: Lync Server 2013：在位于外围网络外部的观察程序节点上安装证书。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing a certificate on a watcher node located outside the perimeter network
ms:assetid: 825c9c02-1951-4d7a-a25e-a313a85333f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688113(v=OCS.15)
ms:contentKeyID: 49733711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 66f40886e9784b5bd4182a60b955745b5daf2034
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427056"
---
# <a name="installing-a-certificate-on-a-watcher-node-located-outside-the-perimeter-network-of-lync-server-2013"></a><span data-ttu-id="4de00-103">在 Lync Server 2013 外围网络外部的观察程序节点上安装证书</span><span class="sxs-lookup"><span data-stu-id="4de00-103">Installing a certificate on a watcher node located outside the perimeter network of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4de00-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4de00-104">

<span> </span></span></span>

<span data-ttu-id="4de00-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="4de00-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="4de00-106">在外围网络中运行的 System Center Operations Manager 代理 (如 Lync Server Edge 服务器) ，在企业 (（如外部合成事务观察程序节点) 或跨 Active Directory 域服务信任边界）之外，可能需要配置 System Center Operations Manager 网关服务器。</span><span class="sxs-lookup"><span data-stu-id="4de00-106">System Center Operations Manager agents running in a perimeter network (such as a Lync Server Edge Server), outside of the enterprise (such as an external synthetic transaction watcher node), or across an Active Directory Domain Services trust boundary, might require the configuration of a System Center Operations Manager Gateway Server.</span></span> <span data-ttu-id="4de00-107">此服务器角色允许与根管理服务器不具有信任关系的代理引发警报。</span><span class="sxs-lookup"><span data-stu-id="4de00-107">This server role allows agents that do not have a trust relationship with the Root Management Server to raise alerts.</span></span> <span data-ttu-id="4de00-108">有关详细信息，请参阅 System Center Operations Manager TechNet 库中的 "管理 Operations Manager 2007 中的网关服务器" [https://go.microsoft.com/fwlink/p/?LinkId=268703](https://go.microsoft.com/fwlink/p/?linkid=268703) 。</span><span class="sxs-lookup"><span data-stu-id="4de00-108">For details, see "Managing Gateway Servers in Operations Manager 2007" in the System Center Operations Manager TechNet Library at [https://go.microsoft.com/fwlink/p/?LinkId=268703](https://go.microsoft.com/fwlink/p/?linkid=268703).</span></span>

<span data-ttu-id="4de00-109">如果在其中一个位置中部署代理，你还需要请求和配置一个允许观察程序节点向 System Center Operations Manager 发送警报的证书。</span><span class="sxs-lookup"><span data-stu-id="4de00-109">If you deploy an agent in one of these locations, you will also need to request and configure a certificate that enables the watcher node to send alerts to System Center Operations Manager.</span></span> <span data-ttu-id="4de00-110">为简化此过程，Operations Manager 团队已创建一组实用工具，可让你在观察程序节点计算机上请求和安装正确的证书类型。</span><span class="sxs-lookup"><span data-stu-id="4de00-110">To simplify this process, the Operations Manager team has created a set of utilities that enable you to request and install the correct type of certificate on the watcher node computer.</span></span> <span data-ttu-id="4de00-111">有关详细信息，以及要下载这些实用程序，请参阅中的 "通过证书生成向导为非域加入的代理获取证书" 中的 "博客文章" [https://go.microsoft.com/fwlink/p/?LinkId=267421](https://go.microsoft.com/fwlink/p/?linkid=267421) 。</span><span class="sxs-lookup"><span data-stu-id="4de00-111">For details, and to download these utilities, see the "Obtaining Certificates for Non-Domain Joined Agents Made Easy With Certificate Generation Wizard" blog article at [https://go.microsoft.com/fwlink/p/?LinkId=267421](https://go.microsoft.com/fwlink/p/?linkid=267421).</span></span>

<span data-ttu-id="4de00-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4de00-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

