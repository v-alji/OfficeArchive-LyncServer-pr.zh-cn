---
title: Lync Server 2013：为音频会议提供商配置联盟
description: Lync Server 2013：为音频会议提供商配置联盟。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure federation for an audio conferencing provider
ms:assetid: 08dedcce-0d3f-45da-8282-cf2634a41665
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn510996(v=OCS.15)
ms:contentKeyID: 60595883
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c74654224c42618768d881a95031d58be4d55df5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434051"
---
# <a name="configure-federation-for-an-audio-conferencing-provider-in-lync-server-2013"></a><span data-ttu-id="3b5c5-103">在 Lync Server 2013 中配置音频会议提供商的联盟</span><span class="sxs-lookup"><span data-stu-id="3b5c5-103">Configure federation for an audio conferencing provider in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b5c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b5c5-104">

<span> </span></span></span>

<span data-ttu-id="3b5c5-105">_**主题上次修改时间：** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="3b5c5-105">_**Topic Last Modified:** 2014-07-24_</span></span>

<span data-ttu-id="3b5c5-106">如果你想要在混合 (部署中使用音频会议提供商 (ACP) 本地 lync Server 与 Lync Online) ，你需要在本地 Lync 部署和 ACP 合作伙伴之间配置联盟作为允许的伙伴服务器。</span><span class="sxs-lookup"><span data-stu-id="3b5c5-106">If you want to use an Audio Conferencing Provider (ACP) in your hybrid deployment (Lync Server on-premises with Lync Online), you need to configure federation between your on-premises Lync deployment and the ACP partner as an Allowed Partner Server.</span></span> <span data-ttu-id="3b5c5-107">您可以通过向本地部署的联盟域列表添加 ACP 合作伙伴域和边缘服务器（可称为访问代理）来配置联盟。</span><span class="sxs-lookup"><span data-stu-id="3b5c5-107">You can configure federation by adding the ACP partner domain and Edge server (this may also be called the Access Proxy) to the Federated Domains list for your on-premises deployment.</span></span> <span data-ttu-id="3b5c5-108">然后，ACP 合作伙伴需要将您的本地边缘服务器池的 FQDN 添加到允许的联盟域列表。</span><span class="sxs-lookup"><span data-stu-id="3b5c5-108">Your ACP partner then needs to add the FQDN of your on-premises Edge Server pool to their allowed federated domains list.</span></span> <span data-ttu-id="3b5c5-109">联系你的 ACP 提供商以获取其他 detailsYour ACP 合作伙伴，然后需要将本地边缘服务器池的 FQDN 添加到其允许的联盟域列表。</span><span class="sxs-lookup"><span data-stu-id="3b5c5-109">Contact your ACP provider for additional detailsYour ACP partner then needs to add the FQDN of your on-premises Edge Server pool to their allowed federated domains list.</span></span>

  - <span data-ttu-id="3b5c5-110">**将 ACP 域和边缘服务器添加为允许的联盟域**</span><span class="sxs-lookup"><span data-stu-id="3b5c5-110">**Adding the ACP Domain and Edge Server as an Allowed Federated Domain**</span></span>
    
    <span data-ttu-id="3b5c5-111">若要将 ACP 域作为允许的伙伴服务器添加 (允许的联盟域) ，请按照在 [Lync Server 2013 中配置对允许的外部域的支持](lync-server-2013-configure-support-for-allowed-external-domains.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="3b5c5-111">To add the ACP domain as an Allowed Partner Server (allowed Federated Domain), follow the steps in [Configure support for allowed external domains in Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span></span> <span data-ttu-id="3b5c5-112">对于边缘服务器，请添加 ACP 合作伙伴的边缘服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="3b5c5-112">For the Edge Server, add the FQDN of the ACP partner’s Edge Server.</span></span> <span data-ttu-id="3b5c5-113">您可能需要联系 ACP 合作伙伴，获得其边缘服务器的 FQDN，ACP 也可能称之为访问代理。</span><span class="sxs-lookup"><span data-stu-id="3b5c5-113">You may need to contact your ACP partner to obtain the FQDN for their Edge Server, which may also be referred to by your ACP as their Access Proxy.</span></span>

  - <span data-ttu-id="3b5c5-114">**向 ACP 合作伙伴提供您的边缘服务器池的 FQDN**</span><span class="sxs-lookup"><span data-stu-id="3b5c5-114">**Provide the FQDN of your Edge Server Pool to the ACP partner**</span></span>
    
    <span data-ttu-id="3b5c5-115">ACP 合作伙伴需要将您的边缘服务器池的 FQDN 添加到允许的联盟域列表，以便配置联盟，将您的本地域添加为允许的合作伙伴服务器。</span><span class="sxs-lookup"><span data-stu-id="3b5c5-115">The ACP partner needs to configure federation to add your on-premises domain as an Allowed Partner Server by adding the FQDN of your Edge Server pool as an allowed Federated domain.</span></span>

<span data-ttu-id="3b5c5-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b5c5-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

