---
title: 管理 XMPP 联盟
description: 正在迁移 XMPP 联合身份验证。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating XMPP federation
ms:assetid: b8d2b4b9-d0ed-4b48-820a-2c257fbdd2fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721861(v=OCS.15)
ms:contentKeyID: 49733794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e63c9f6fd3f1c1d45de77c27417987505678f74b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440358"
---
# <a name="migrating-xmpp-federation"></a><span data-ttu-id="03b8d-103">管理 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="03b8d-103">Migrating XMPP federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03b8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03b8d-104">

<span> </span></span></span>

<span data-ttu-id="03b8d-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="03b8d-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="03b8d-106">以前版本的 Lync Server 和 Office 通信服务器提供了可扩展消息和状态协议 (XMPP) 网关，可部署为单独的服务器角色，以便允许与 XMPP 部署进行联盟。</span><span class="sxs-lookup"><span data-stu-id="03b8d-106">Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments.</span></span> <span data-ttu-id="03b8d-107">在 Lync Server 2013 中，XMPP 功能可以部署为功能。</span><span class="sxs-lookup"><span data-stu-id="03b8d-107">In Lync Server 2013, the XMPP functionality can be deployed as a feature.</span></span> <span data-ttu-id="03b8d-108">XMPP 功能安装在两个部分中：作为在 Lync Server 2013 Edge 服务器上运行的 XMPP 代理，以及在 Lync Server 2013 前端服务器上运行的 XMPP 网关。</span><span class="sxs-lookup"><span data-stu-id="03b8d-108">XMPP functionality is installed in two parts: as an XMPP proxy that runs on the Lync Server 2013 Edge Server, and the XMPP Gateway that runs on the Lync Server 2013 Front End Server.</span></span>

<span data-ttu-id="03b8d-109">从迁移的角度来看，Lync 服务器用户帐户可以移到 Lync Server 2013 池，并继续使用旧版 XMPP 网关。</span><span class="sxs-lookup"><span data-stu-id="03b8d-109">From a migration perspective, a Lync Server user account can be moved to a Lync Server 2013 pool and continue to use the legacy XMPP gateway.</span></span> <span data-ttu-id="03b8d-110">仅当未在 Lync Server 2013 中配置 XMPP 联盟合作伙伴时，才可以这样做。</span><span class="sxs-lookup"><span data-stu-id="03b8d-110">This is possible only when the XMPP federated partner is not configured in Lync Server 2013.</span></span>

<span data-ttu-id="03b8d-111">总而言之，如果已部署 Lync Server 2010 的 Office 通信服务器 2007 R2 XMPP 网关，并且 XMPP 联盟已针对旧版 Lync Server 2010 用户启用，则要将 XMPP 联合迁移到 Lync Server 2013，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="03b8d-111">In summary, if Lync Server 2010 has been deployed with the Office Communications Server 2007 R2 XMPP Gateway and XMPP federation has been enabled for legacy Lync Server 2010 users, to migrate the XMPP federation to Lync Server 2013:</span></span>

1.  <span data-ttu-id="03b8d-112">部署 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="03b8d-112">Deploy a Lync Server 2013 pool.</span></span>

2.  <span data-ttu-id="03b8d-113">部署 Lync Server 2013 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="03b8d-113">Deploy a Lync Server 2013 Edge server.</span></span>

3.  <span data-ttu-id="03b8d-114">将所有用户移到 Lync Server 2013 池</span><span class="sxs-lookup"><span data-stu-id="03b8d-114">Move all users to the Lync Server 2013 pool</span></span>

4.  <span data-ttu-id="03b8d-115">为 Edge 服务器创建 XMPP 访问策略和证书。</span><span class="sxs-lookup"><span data-stu-id="03b8d-115">Create XMPP access policies and certificates for the Edge Server.</span></span>

5.  <span data-ttu-id="03b8d-116">在 Lync Server 2013 中启用 XMPP 联合身份验证。</span><span class="sxs-lookup"><span data-stu-id="03b8d-116">Enable XMPP federation in Lync Server 2013.</span></span> 

6.  <span data-ttu-id="03b8d-117">将 DNS 条目更新为指向 Lync Server 2013 XMPP 网关。</span><span class="sxs-lookup"><span data-stu-id="03b8d-117">Update the DNS entries to point to the Lync Server 2013 XMPP Gateway.</span></span>

<span data-ttu-id="03b8d-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03b8d-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

