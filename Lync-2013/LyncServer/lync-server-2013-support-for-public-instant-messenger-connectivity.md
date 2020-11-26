---
title: Lync Server 2013 支持公共即时消息连接
description: Lync Server 2013 支持公共即时消息连接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for public instant messenger connectivity
ms:assetid: 9c6eb500-647b-4ccd-a00e-2b8dd7c44a76
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn458579(v=OCS.15)
ms:contentKeyID: 59170234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d4a58d71eb23012da960cf4505f1a55fd08df32c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441499"
---
# <a name="support-for-public-instant-messenger-connectivity-in-lync-server-2013"></a><span data-ttu-id="63bb9-103">Lync Server 2013 中的公共即时消息连接支持</span><span class="sxs-lookup"><span data-stu-id="63bb9-103">Support for public instant messenger connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63bb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63bb9-104">

<span> </span></span></span>

<span data-ttu-id="63bb9-105">_**主题上次修改时间：** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="63bb9-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<div>

## <a name="support-for-public-instant-messenger-connectivity"></a><span data-ttu-id="63bb9-106">对公共即时消息连接的支持</span><span class="sxs-lookup"><span data-stu-id="63bb9-106">Support for Public Instant Messenger Connectivity</span></span>

<span data-ttu-id="63bb9-107">本文提供 (PIC) 的公共 IM 连接的支持信息。</span><span class="sxs-lookup"><span data-stu-id="63bb9-107">This article provides information about support for Public IM Connectivity (PIC).</span></span> <span data-ttu-id="63bb9-108">PIC 是 Microsoft Lync 的一项功能，允许组织使其 Lync 用户能够通过其 Lync 客户端和标识与特定公共即时消息 (IM) 服务的用户进行连接。</span><span class="sxs-lookup"><span data-stu-id="63bb9-108">PIC is a feature of Microsoft Lync that allows organizations to enable their Lync users to connect with users of certain public instant messaging (IM) services through their Lync clients and identities.</span></span>

<span data-ttu-id="63bb9-109">最终用户可以通过其条款与客户、合作伙伴和供应商联系，从而获益。</span><span class="sxs-lookup"><span data-stu-id="63bb9-109">End-users benefit from being able to connect with customers, partners, and vendors on their terms.</span></span> <span data-ttu-id="63bb9-110">在保持 Lync 的控制、合规性和存档功能的同时支持单个实时通信客户端的好处。</span><span class="sxs-lookup"><span data-stu-id="63bb9-110">IT benefits from supporting a single real-time communications client while maintaining the control, compliance, and archiving features of Lync.</span></span> <span data-ttu-id="63bb9-111">Lync-Skype [在2013五月公开推出](https://blogs.technet.com/b/lync/archive/2013/05/23/lync-skype-connectivity-available-today.aspx)的连接，依赖于 Lync/Office 通信服务器 (OCS) /Live 通信服务器 (LCS) 首先在连接到 MSN/Windows LIVE、AOL 和 Yahoo 时与 PIC 建立联系。</span><span class="sxs-lookup"><span data-stu-id="63bb9-111">Lync-Skype connectivity, [publicly available in May 2013](https://blogs.technet.com/b/lync/archive/2013/05/23/lync-skype-connectivity-available-today.aspx), relies on the legacy that Lync/Office Communications Server (OCS)/Live Communications Server (LCS) first established with PIC in connecting to MSN/Windows Live, AOL, and Yahoo.</span></span>  <span data-ttu-id="63bb9-112">有关 Lync-Skype 连接的详细信息，请参阅 [Lync-Skype 连接](https://office.microsoft.com/lync/lync-skype-connectivity-fx103789635.aspx)。</span><span class="sxs-lookup"><span data-stu-id="63bb9-112">For more information on Lync-Skype connectivity, see the [Lync-Skype connectivity](https://office.microsoft.com/lync/lync-skype-connectivity-fx103789635.aspx).</span></span> <span data-ttu-id="63bb9-113">与 Windows Live、AOL 和 Yahoo 的联盟，每个都在一条路线上的生命周期结束。</span><span class="sxs-lookup"><span data-stu-id="63bb9-113">Federation with Windows Live, AOL, and Yahoo are each on a path towards end-of-life.</span></span> <span data-ttu-id="63bb9-114">此页面记录每个服务的状态。</span><span class="sxs-lookup"><span data-stu-id="63bb9-114">This page documents the status of each service.</span></span>

<span data-ttu-id="63bb9-115">若要使用 PIC，客户必须为每个公共 IM 服务提供商激活该服务。</span><span class="sxs-lookup"><span data-stu-id="63bb9-115">To use PIC, customers have been required to activate the service for each public IM service provider.</span></span> <span data-ttu-id="63bb9-116">如何执行此操作的要求和详细信息取决于 IM 服务提供商和客户的基础许可计划。</span><span class="sxs-lookup"><span data-stu-id="63bb9-116">The requirements and details for how to do this are dependent upon the IM service provider and the customer's underlying licensing program.</span></span>

<div>

## <a name="windows-live-messenger"></a><span data-ttu-id="63bb9-117">Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="63bb9-117">Windows Live Messenger</span></span>

<span data-ttu-id="63bb9-118">Microsoft 将 Windows Live Messenger 和 Skype 一起引入。</span><span class="sxs-lookup"><span data-stu-id="63bb9-118">Microsoft brought Windows Live Messenger and Skype together.</span></span> <span data-ttu-id="63bb9-119">2013年4月，在登录时，Messenger 用户已迁移到 Skype。</span><span class="sxs-lookup"><span data-stu-id="63bb9-119">In April 2013, Messenger users were migrated to Skype upon sign-in.</span></span> <span data-ttu-id="63bb9-120">即使在这些联系人更新到 Skype 后，依赖联盟的 Lync 客户仍然能够与他们的 Messenger 联系人进行通信。</span><span class="sxs-lookup"><span data-stu-id="63bb9-120">Lync customers who rely on federation with Messenger will continue to be able to communicate with their Messenger contacts, even after those contacts update to Skype.</span></span> <span data-ttu-id="63bb9-121">Lync 管理员或 Lync 最终用户无需执行此操作来维护服务的连续性，并且 Lync 中的此功能的管理与 Messenger 的通信方式相同。</span><span class="sxs-lookup"><span data-stu-id="63bb9-121">There is nothing that Lync administrators or Lync end-users need to do to maintain continuity of service, and management of this capability within Lync remains the same as it has been for communications with Messenger.</span></span> 

<span data-ttu-id="63bb9-122">当 Messenger 用户使用其 Microsoft 帐户登录到 Skype 时 (也就是说，用于 Messenger 的同一凭据) 其所有 Messenger 联系人（包括联合 Lync 联系人），请将其加入 Skype。</span><span class="sxs-lookup"><span data-stu-id="63bb9-122">When Messenger users sign into Skype using their Microsoft accounts (i.e., the same credentials used for Messenger) all of their Messenger contacts - including federated Lync contacts - follow them into Skype.</span></span> <span data-ttu-id="63bb9-123">可使用 Skype 和 Lync 之间的联机状态共享和即时消息功能。</span><span class="sxs-lookup"><span data-stu-id="63bb9-123">Presence sharing and instant messaging between Skype and Lync for these contacts is available.</span></span> 

<span data-ttu-id="63bb9-124">Lync-Skype 连接-联系人在 Lync 和 Skype 用户之间的添加、状态共享、即时消息和音频呼叫现在也可供所有 Lync 客户使用。</span><span class="sxs-lookup"><span data-stu-id="63bb9-124">Lync-Skype connectivity - contact adding, presence sharing, instant messaging, and audio calling between Lync and Skype users - is also now available to all Lync customers.</span></span>

</div>

<div>

## <a name="yahoo-and-aol-instant-messenger"></a><span data-ttu-id="63bb9-125">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="63bb9-125">Yahoo\!</span></span> <span data-ttu-id="63bb9-126">和 AOL 即时消息</span><span class="sxs-lookup"><span data-stu-id="63bb9-126">and AOL Instant Messenger</span></span>

<span data-ttu-id="63bb9-127">与 Yahoo 的联盟\!</span><span class="sxs-lookup"><span data-stu-id="63bb9-127">Federation with Yahoo\!</span></span> <span data-ttu-id="63bb9-128">AOL (和 Office 通信服务器) 的客户将在一条路线中使用 AOL。</span><span class="sxs-lookup"><span data-stu-id="63bb9-128">and AOL are both on a path toward end-of-life for customers of Lync (and Office Communications Server).</span></span> <span data-ttu-id="63bb9-129">Microsoft 提供每项服务的能力已被从 Yahoo 提供支持\!</span><span class="sxs-lookup"><span data-stu-id="63bb9-129">Microsoft’s ability to provide each of these services has been contingent upon support from Yahoo\!</span></span> <span data-ttu-id="63bb9-130">和 AOL，并向下缠绕这些协议的基础协议。</span><span class="sxs-lookup"><span data-stu-id="63bb9-130">and AOL, and the underlying agreements of these are winding down.</span></span> <span data-ttu-id="63bb9-131">对于这两个 Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="63bb9-131">For both Yahoo\!</span></span> <span data-ttu-id="63bb9-132">并且 AOL 的服务将继续至2014年6月。</span><span class="sxs-lookup"><span data-stu-id="63bb9-132">and AOL, service will continue through June 2014.</span></span>

  - <span data-ttu-id="63bb9-133">**Yahoo** ！服务将在2014年6月后继续，并且客户继续需要使用 Microsoft LYNC 公共 IM 连接用户订阅许可证 ( "PIC USL" ) 。</span><span class="sxs-lookup"><span data-stu-id="63bb9-133">**Yahoo** - Service will continue through June 2014, and customers continue to need to be licensed with the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”).</span></span>  <span data-ttu-id="63bb9-134">从2012年9月1日起，PIC USL 不能再购买新的或续订协议。</span><span class="sxs-lookup"><span data-stu-id="63bb9-134">As of September 1st, 2012, the PIC USL, is no longer available for purchase for new or renewing agreements.</span></span>  <span data-ttu-id="63bb9-135">在此日期之前购买许可证的客户将能够继续与 Yahoo 进行联盟\!</span><span class="sxs-lookup"><span data-stu-id="63bb9-135">Customers with licenses purchased prior to this date will be able to continue to federate with Yahoo\!</span></span> <span data-ttu-id="63bb9-136">直到较早的服务关闭日期或许可证过期。</span><span class="sxs-lookup"><span data-stu-id="63bb9-136">until the earlier of the service shut down date or their license expiration.</span></span> <span data-ttu-id="63bb9-137">阅读 Lync 团队博客上 [的公告](https://blogs.technet.com/b/lync/archive/2012/11/26/lync-and-yahoo-federation-end-of-life.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="63bb9-137">Read [the announcement](https://blogs.technet.com/b/lync/archive/2012/11/26/lync-and-yahoo-federation-end-of-life.aspx) on the Lync Team Blog.</span></span> <span data-ttu-id="63bb9-138">如果客户的许可证在2014年6月30日之前过期，则将按与年6月30日到2014之间的时间段的付款金额为比例，获得点数。</span><span class="sxs-lookup"><span data-stu-id="63bb9-138">Customers who have PIC licenses on agreements that extend past June 30, 2014 will receive a credit in proportion to the amount of the payments covering the time period following June 30, 2014.</span></span>

  - <span data-ttu-id="63bb9-139">**AOL** -在2014年6月30日，LYNC 的 IM 连接 ( "PIC" ) 服务将不再可用。</span><span class="sxs-lookup"><span data-stu-id="63bb9-139">**AOL** - On June 30, 2014, Lync's IM connectivity ("PIC") service will no longer be available.</span></span> <span data-ttu-id="63bb9-140">为了在服务结束时限制客户中断，我们已停止设置其他客户域。</span><span class="sxs-lookup"><span data-stu-id="63bb9-140">In order to limit customer disruption when the service ends, we have discontinued the provisioning of additional customer domains.</span></span> <span data-ttu-id="63bb9-141">在2014年6月30日之前，客户无需执行任何操作即可继续支持与目标的联盟通信。</span><span class="sxs-lookup"><span data-stu-id="63bb9-141">Until June 30, 2014, customers do not need to do anything to continue to support federated communications with AIM.</span></span> <span data-ttu-id="63bb9-142">除了本日期 (或对于想要在同一时间内预配其他域的客户) ，可直接从 AOL 获取替代服务。</span><span class="sxs-lookup"><span data-stu-id="63bb9-142">Beyond this date (or for customers that would like to provision additional domains in the meantime), a substitute service is available directly from AOL.</span></span> <span data-ttu-id="63bb9-143">有关 AOL 新服务的详细信息，请参阅 [建立与 AIM 的直接联盟](http://aimenterprise.aol.com/pic.php)  (在 AOL.com) 上打开新页面。</span><span class="sxs-lookup"><span data-stu-id="63bb9-143">For more information on AOL's new service, see [Establishing Direct Federation with AIM](http://aimenterprise.aol.com/pic.php)  (opens new page on AOL.com).</span></span>  

</div>

<div>

## <a name="public-im-provider-summary"></a><span data-ttu-id="63bb9-144">公共 IM 提供商摘要</span><span class="sxs-lookup"><span data-stu-id="63bb9-144">Public IM Provider Summary</span></span>

<span data-ttu-id="63bb9-145">下表提供了公用 IM 服务提供商、与 Lync 的联盟功能以及授权要求的摘要。</span><span class="sxs-lookup"><span data-stu-id="63bb9-145">The following table provides a summary of the Public IM service providers, federation capabilities with Lync, and licensing requirements.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63bb9-146">公用 IM 服务提供商</span><span class="sxs-lookup"><span data-stu-id="63bb9-146">Public IM Service Provider</span></span></th>
<th><span data-ttu-id="63bb9-147">联合功能</span><span class="sxs-lookup"><span data-stu-id="63bb9-147">Federated Capabilities</span></span></th>
<th><span data-ttu-id="63bb9-148">许可要求</span><span class="sxs-lookup"><span data-stu-id="63bb9-148">Licensing Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63bb9-149">Skype</span><span class="sxs-lookup"><span data-stu-id="63bb9-149">Skype</span></span></p></td>
<td><p><span data-ttu-id="63bb9-150">即时消息、状态、音频</span><span class="sxs-lookup"><span data-stu-id="63bb9-150">IM, Presence, Audio</span></span></p></td>
<td><p><span data-ttu-id="63bb9-151">Lync Server 客户端访问许可证，Lync Online 计划1/2/3</span><span class="sxs-lookup"><span data-stu-id="63bb9-151">Lync Server Client Access Licenses, Lync Online Plan 1/2/3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63bb9-152">Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="63bb9-152">Windows Live Messenger</span></span></p></td>
<td><p><span data-ttu-id="63bb9-153">即时消息、状态、音频/视频</span><span class="sxs-lookup"><span data-stu-id="63bb9-153">IM, Presence, Audio/Video</span></span></p></td>
<td><p><span data-ttu-id="63bb9-154"> (支持 Lync Server 客户端访问许可证，只要 WLM 处于市场) </span><span class="sxs-lookup"><span data-stu-id="63bb9-154">Lync Server Client Access Licenses (supported as long as WLM is in market)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63bb9-155">AOL</span><span class="sxs-lookup"><span data-stu-id="63bb9-155">AOL</span></span></p></td>
<td><p><span data-ttu-id="63bb9-156">即时消息、状态</span><span class="sxs-lookup"><span data-stu-id="63bb9-156">IM, Presence</span></span></p></td>
<td><p><span data-ttu-id="63bb9-157">Lync Server 客户端访问许可证;支持的现有客户2014年6月。</span><span class="sxs-lookup"><span data-stu-id="63bb9-157">Lync Server Client Access Licenses; supported through June 2014 for existing customers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63bb9-158">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="63bb9-158">Yahoo!</span></span></p></td>
<td><p><span data-ttu-id="63bb9-159">即时消息、状态</span><span class="sxs-lookup"><span data-stu-id="63bb9-159">IM, Presence</span></span></p></td>
<td><p><span data-ttu-id="63bb9-160">除了 Lync Server 客户端访问许可证外，还需要其他 Microsoft Lync 公共 IM 连接用户订阅许可证 ( "PIC USL" ) 。</span><span class="sxs-lookup"><span data-stu-id="63bb9-160">Requires additional Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) in addition to Lync Server Client Access Licences.</span></span> <span data-ttu-id="63bb9-161">从2012年9月的价目表中，PIC USL 不能再购买。</span><span class="sxs-lookup"><span data-stu-id="63bb9-161">As of the September 2012 Price List, the PIC USL is no longer available for purchase.</span></span> <span data-ttu-id="63bb9-162">具有活动许可证的客户可以继续与 Yahoo！进行联盟</span><span class="sxs-lookup"><span data-stu-id="63bb9-162">Customers with active licenses are able to continue to federate with Yahoo!</span></span> <span data-ttu-id="63bb9-163">Messenger，直到服务在2014年6月30日的关闭日期。</span><span class="sxs-lookup"><span data-stu-id="63bb9-163">Messenger until the service shut down date on June 30, 2014.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="63bb9-164">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63bb9-164">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

