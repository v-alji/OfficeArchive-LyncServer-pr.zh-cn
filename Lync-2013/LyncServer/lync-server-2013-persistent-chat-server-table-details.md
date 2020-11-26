---
title: Lync Server 2013：持久聊天服务器表详细信息
description: Lync Server 2013：持久聊天服务器表的详细信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server table details
ms:assetid: c22d4a76-da50-49de-9038-e0ed7b8e1b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615034(v=OCS.15)
ms:contentKeyID: 48185323
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a27feaaccf861d537127f06920cf903be5ae000
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443081"
---
# <a name="persistent-chat-server-table-details-in-lync-server-2013"></a><span data-ttu-id="fbbb3-103">Lync Server 2013 中的持久聊天服务器表详细信息</span><span class="sxs-lookup"><span data-stu-id="fbbb3-103">Persistent Chat Server table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fbbb3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fbbb3-104">

<span> </span></span></span>

<span data-ttu-id="fbbb3-105">_**主题上次修改时间：** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="fbbb3-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="fbbb3-106">以下主题详细介绍了每个持久聊天数据库架构表中的列。</span><span class="sxs-lookup"><span data-stu-id="fbbb3-106">The following topics detail the columns in each of the Persistent Chat database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fbbb3-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="fbbb3-107">In This Section</span></span>

  - [<span data-ttu-id="fbbb3-108">Lync Server 2013 中的 tblADCookie</span><span class="sxs-lookup"><span data-stu-id="fbbb3-108">tblADCookie in Lync Server 2013</span></span>](lync-server-2013-tbladcookie.md)

  - [<span data-ttu-id="fbbb3-109">Lync Server 2013 中的 tblPrincipalMemberDifference</span><span class="sxs-lookup"><span data-stu-id="fbbb3-109">tblPrincipalMemberDifference in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmemberdifference.md)

  - [<span data-ttu-id="fbbb3-110">Lync Server 2013 中的 tblADUpdates</span><span class="sxs-lookup"><span data-stu-id="fbbb3-110">tblADUpdates in Lync Server 2013</span></span>](lync-server-2013-tbladupdates.md)

  - [<span data-ttu-id="fbbb3-111">Lync Server 2013 中的 tblPrincipalMembers</span><span class="sxs-lookup"><span data-stu-id="fbbb3-111">tblPrincipalMembers in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmembers.md)

  - [<span data-ttu-id="fbbb3-112">Lync Server 2013 中的 tblPrincipalMeta</span><span class="sxs-lookup"><span data-stu-id="fbbb3-112">tblPrincipalMeta in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmeta.md)

  - [<span data-ttu-id="fbbb3-113">Lync Server 2013 中的 tblSkippedAffiliations</span><span class="sxs-lookup"><span data-stu-id="fbbb3-113">tblSkippedAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblskippedaffiliations.md)

  - [<span data-ttu-id="fbbb3-114">Lync Server 2013 中的 tblPrincipalType</span><span class="sxs-lookup"><span data-stu-id="fbbb3-114">tblPrincipalType in Lync Server 2013</span></span>](lync-server-2013-tblprincipaltype.md)

  - [<span data-ttu-id="fbbb3-115">Lync Server 2013 中的 tblPrincipal</span><span class="sxs-lookup"><span data-stu-id="fbbb3-115">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)

  - [<span data-ttu-id="fbbb3-116">Lync Server 2013 中的 tblPrincipalAffiliations</span><span class="sxs-lookup"><span data-stu-id="fbbb3-116">tblPrincipalAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblprincipalaffiliations.md)

  - [<span data-ttu-id="fbbb3-117">Lync Server 2013 中的 tblNode</span><span class="sxs-lookup"><span data-stu-id="fbbb3-117">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)

  - [<span data-ttu-id="fbbb3-118">Lync Server 2013 中的 tblRoleType</span><span class="sxs-lookup"><span data-stu-id="fbbb3-118">tblRoleType in Lync Server 2013</span></span>](lync-server-2013-tblroletype.md)

  - [<span data-ttu-id="fbbb3-119">Lync Server 2013 中的 tblScopePrincipal</span><span class="sxs-lookup"><span data-stu-id="fbbb3-119">tblScopePrincipal in Lync Server 2013</span></span>](lync-server-2013-tblscopeprincipal.md)

  - [<span data-ttu-id="fbbb3-120">Lync Server 2013 中的 tblPrincipalRole</span><span class="sxs-lookup"><span data-stu-id="fbbb3-120">tblPrincipalRole in Lync Server 2013</span></span>](lync-server-2013-tblprincipalrole.md)

  - [<span data-ttu-id="fbbb3-121">Lync Server 2013 中的 tblSiopWhiteList</span><span class="sxs-lookup"><span data-stu-id="fbbb3-121">tblSiopWhiteList in Lync Server 2013</span></span>](lync-server-2013-tblsiopwhitelist.md)

  - [<span data-ttu-id="fbbb3-122">Lync Server 2013 中的 tblEnumAttribute</span><span class="sxs-lookup"><span data-stu-id="fbbb3-122">tblEnumAttribute in Lync Server 2013</span></span>](lync-server-2013-tblenumattribute.md)

  - [<span data-ttu-id="fbbb3-123">Lync Server 2013 中的 tblEnumValue</span><span class="sxs-lookup"><span data-stu-id="fbbb3-123">tblEnumValue in Lync Server 2013</span></span>](lync-server-2013-tblenumvalue.md)

  - [<span data-ttu-id="fbbb3-124">Lync Server 2013 中的 tblPrincipalInvites</span><span class="sxs-lookup"><span data-stu-id="fbbb3-124">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)

  - [<span data-ttu-id="fbbb3-125">Lync Server 2013 中的 tblChat</span><span class="sxs-lookup"><span data-stu-id="fbbb3-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)

  - [<span data-ttu-id="fbbb3-126">Lync Server 2013 中的 tblLastInviteId</span><span class="sxs-lookup"><span data-stu-id="fbbb3-126">tblLastInviteId in Lync Server 2013</span></span>](lync-server-2013-tbllastinviteid.md)

  - [<span data-ttu-id="fbbb3-127">Lync Server 2013 中的 tblLastChatId</span><span class="sxs-lookup"><span data-stu-id="fbbb3-127">tblLastChatId in Lync Server 2013</span></span>](lync-server-2013-tbllastchatid.md)

  - [<span data-ttu-id="fbbb3-128">Lync Server 2013 中的 tblPreference</span><span class="sxs-lookup"><span data-stu-id="fbbb3-128">tblPreference in Lync Server 2013</span></span>](lync-server-2013-tblpreference.md)

  - [<span data-ttu-id="fbbb3-129">Lync Server 2013 中的 tblFileToken</span><span class="sxs-lookup"><span data-stu-id="fbbb3-129">tblFileToken in Lync Server 2013</span></span>](lync-server-2013-tblfiletoken.md)

  - [<span data-ttu-id="fbbb3-130">Lync Server 2013 中的 tblServerIdentity</span><span class="sxs-lookup"><span data-stu-id="fbbb3-130">tblServerIdentity in Lync Server 2013</span></span>](lync-server-2013-tblserveridentity.md)

  - [<span data-ttu-id="fbbb3-131">Lync Server 2013 中的 tblAdminLock</span><span class="sxs-lookup"><span data-stu-id="fbbb3-131">tblAdminLock in Lync Server 2013</span></span>](lync-server-2013-tbladminlock.md)

  - [<span data-ttu-id="fbbb3-132">Lync Server 2013 中的 tblSystemRevision</span><span class="sxs-lookup"><span data-stu-id="fbbb3-132">tblSystemRevision in Lync Server 2013</span></span>](lync-server-2013-tblsystemrevision.md)

  - [<span data-ttu-id="fbbb3-133">Lync Server 2013 中的 tblActivePeers</span><span class="sxs-lookup"><span data-stu-id="fbbb3-133">tblActivePeers in Lync Server 2013</span></span>](lync-server-2013-tblactivepeers.md)

  - [<span data-ttu-id="fbbb3-134">Lync Server 2013 中的 tblConfig</span><span class="sxs-lookup"><span data-stu-id="fbbb3-134">tblConfig in Lync Server 2013</span></span>](lync-server-2013-tblconfig.md)

  - [<span data-ttu-id="fbbb3-135">Lync Server 2013 中的 tblComplianceData</span><span class="sxs-lookup"><span data-stu-id="fbbb3-135">tblComplianceData in Lync Server 2013</span></span>](lync-server-2013-tblcompliancedata.md)

  - [<span data-ttu-id="fbbb3-136">Lync Server 2013 中的 tblComplianceFanout</span><span class="sxs-lookup"><span data-stu-id="fbbb3-136">tblComplianceFanout in Lync Server 2013</span></span>](lync-server-2013-tblcompliancefanout.md)

  - [<span data-ttu-id="fbbb3-137">Lync Server 2013 中的 tblComplianceParticipant</span><span class="sxs-lookup"><span data-stu-id="fbbb3-137">tblComplianceParticipant in Lync Server 2013</span></span>](lync-server-2013-tblcomplianceparticipant.md)

  - [<span data-ttu-id="fbbb3-138">Lync Server 2013 中的 tblComplianceState</span><span class="sxs-lookup"><span data-stu-id="fbbb3-138">tblComplianceState in Lync Server 2013</span></span>](lync-server-2013-tblcompliancestate.md)

<span data-ttu-id="fbbb3-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fbbb3-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

