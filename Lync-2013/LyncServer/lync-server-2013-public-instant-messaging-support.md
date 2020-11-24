---
title: Lync Server 2013：公共即时消息支持
description: Lync Server 2013：公共即时消息支持。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Public instant messaging support
ms:assetid: 1f45163b-52c6-4a78-b9c8-dfe3abe4e5eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204732(v=OCS.15)
ms:contentKeyID: 48183582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e071e8b79be82d865a85a9488e48dd0a4264c7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392128"
---
# <a name="public-instant-messaging-support-in-lync-server-2013"></a><span data-ttu-id="28f71-103">Lync Server 2013 中的公共即时消息支持</span><span class="sxs-lookup"><span data-stu-id="28f71-103">Public instant messaging support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28f71-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28f71-104">

<span> </span></span></span>

<span data-ttu-id="28f71-105">_**主题上次修改时间：** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="28f71-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="28f71-106">Lync Server 2013 支持使用已授权的公共即时消息 (IM) 连接提供程序以及使用可扩展消息和状态协议 (XMPP) 实现一种特殊类型的联合，使 Lync Server 能够使用 Lync 2013 客户端访问配置的 XMPP 域合作伙伴。</span><span class="sxs-lookup"><span data-stu-id="28f71-106">Lync Server 2013 supports the use of licensed public instant messaging (IM) connectivity providers, as well as the use of eXtensible Messaging and Presence Protocol (XMPP) to implement a special type of federation that enables a Lync Server to access configured XMPP domain partners by using the Lync 2013 client.</span></span>

<div>

## <a name="public-im-connectivity-provider-support"></a><span data-ttu-id="28f71-107">公共 IM 连接提供程序支持</span><span class="sxs-lookup"><span data-stu-id="28f71-107">Public IM Connectivity Provider Support</span></span>

<span data-ttu-id="28f71-108">当前支持的公共即时消息连接合作伙伴包括：</span><span class="sxs-lookup"><span data-stu-id="28f71-108">The currently supported public instant messaging connectivity partners are:</span></span>

  - <span data-ttu-id="28f71-109">美洲在线</span><span class="sxs-lookup"><span data-stu-id="28f71-109">America Online</span></span>

  - <span data-ttu-id="28f71-110">Windows Live</span><span class="sxs-lookup"><span data-stu-id="28f71-110">Windows Live</span></span>

  - <span data-ttu-id="28f71-111">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="28f71-111">Yahoo\!</span></span>

<span data-ttu-id="28f71-112">对于与 Windows Live 用户的通信，Lync Server 2013 支持对等 IM 和音频和视频通话。</span><span class="sxs-lookup"><span data-stu-id="28f71-112">For communications with Windows Live users, Lync Server 2013 supports peer-to-peer IM and audio and video calls.</span></span> <span data-ttu-id="28f71-113">对于与 AOL 和 Yahoo 的通信 \! ，Lync Server 2013 支持对等 IM。</span><span class="sxs-lookup"><span data-stu-id="28f71-113">For communications with AOL and Yahoo\!, Lync Server 2013 supports peer-to-peer IM.</span></span> <span data-ttu-id="28f71-114">可能需要单独的许可证。</span><span class="sxs-lookup"><span data-stu-id="28f71-114">A separate license may be required.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="28f71-115">从2012年9月1日起，，Microsoft Lync 公共 IM 连接用户订阅许可证 ( "PIC USL" ) 不再可用于购买新的或续订协议。</span><span class="sxs-lookup"><span data-stu-id="28f71-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="28f71-116">具有活动许可证的客户将能够继续与 Yahoo！进行联盟</span><span class="sxs-lookup"><span data-stu-id="28f71-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="28f71-117">Messenger，直到服务关闭日期。</span><span class="sxs-lookup"><span data-stu-id="28f71-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="28f71-118">AOL 和 Yahoo！的有效期结束日期为2014年6月</span><span class="sxs-lookup"><span data-stu-id="28f71-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="28f71-119">已宣布。</span><span class="sxs-lookup"><span data-stu-id="28f71-119">has been announced.</span></span> <span data-ttu-id="28f71-120">有关详细信息，请参阅 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 中的公共即时消息连接支持</A>。</span><span class="sxs-lookup"><span data-stu-id="28f71-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="28f71-121">PIC USL 是 Lync Server 或 Office 通信服务器与 Yahoo！联合所需的每个每个用户每月订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="28f71-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="28f71-122">Messenger.</span><span class="sxs-lookup"><span data-stu-id="28f71-122">Messenger.</span></span> <span data-ttu-id="28f71-123">Microsoft 提供此服务的能力已作为对 Yahoo！的支持，它的底层协议被向下缠绕。</span><span class="sxs-lookup"><span data-stu-id="28f71-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="28f71-124">Lync 比以往更多，是一种强大的工具，用于跨组织和全球各地的人员进行连接。</span><span class="sxs-lookup"><span data-stu-id="28f71-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="28f71-125">与 Windows Live Messenger 的联盟不需要除 Lync 标准 CAL 之外的其他用户/设备许可证。</span><span class="sxs-lookup"><span data-stu-id="28f71-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="28f71-126">Skype 联盟将添加到此列表，使 Lync 用户可以通过 IM 和语音与成百上千人联系。</span><span class="sxs-lookup"><span data-stu-id="28f71-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="xmpp-federation-support"></a><span data-ttu-id="28f71-127">XMPP 联合身份验证支持</span><span class="sxs-lookup"><span data-stu-id="28f71-127">XMPP Federation Support</span></span>

<span data-ttu-id="28f71-128">XMPP 联合身份验证支持使用公共提供商的已配置 XMPP 域用户（如 GTalk）进行 Lync 用户通信。</span><span class="sxs-lookup"><span data-stu-id="28f71-128">XMPP federation supports Lync users communication with configured XMPP domain users who use a public provider, such as GTalk.</span></span> <span data-ttu-id="28f71-129">与这些用户的通信可包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="28f71-129">Communications with these users can include the following:</span></span>

  - <span data-ttu-id="28f71-130">对等 IM 和状态</span><span class="sxs-lookup"><span data-stu-id="28f71-130">Peer-to-peer IM and presence</span></span>

  - <span data-ttu-id="28f71-131">在 Lync 客户端中创建 XMPP 联盟联系人</span><span class="sxs-lookup"><span data-stu-id="28f71-131">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="28f71-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28f71-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

