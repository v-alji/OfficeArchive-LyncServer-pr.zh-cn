---
title: Lync Server 2013：CDR 表详细信息
description: Lync Server 2013： CDR 表详细信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CDR table details
ms:assetid: 896198f5-672b-48ea-852f-0211c0c90857
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398693(v=OCS.15)
ms:contentKeyID: 48184730
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 331a3dfd4ffccac2ac4a442eeb9ad9171defb41c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435479"
---
# <a name="cdr-table-details-in-lync-server-2013"></a><span data-ttu-id="16ce9-103">Lync Server 2013 中的 CDR 表详细信息</span><span class="sxs-lookup"><span data-stu-id="16ce9-103">CDR table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16ce9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16ce9-104">

<span> </span></span></span>

<span data-ttu-id="16ce9-105">_**主题上次修改时间：** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="16ce9-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="16ce9-106">以下主题详细介绍了 (CDR) 数据库架构表中的每个 "调用详细信息" 记录中的列。</span><span class="sxs-lookup"><span data-stu-id="16ce9-106">The following topics detail the columns in each of the call detail records (CDR) database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="16ce9-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="16ce9-107">In This Section</span></span>

  - [<span data-ttu-id="16ce9-108">Lync Server 2013 中的 Application 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-108">Application table in Lync Server 2013</span></span>](lync-server-2013-application-table.md)

  - [<span data-ttu-id="16ce9-109">Lync Server 2013 中的 CallPriorities 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-109">CallPriorities table in Lync Server 2013</span></span>](lync-server-2013-callpriorities-table.md)

  - [<span data-ttu-id="16ce9-110">Lync Server 2013 中的 CallType 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-110">CallType table in Lync Server 2013</span></span>](lync-server-2013-calltype-table.md)

  - [<span data-ttu-id="16ce9-111">Lync Server 2013 中的 ClientVersions 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-111">ClientVersions table in Lync Server 2013</span></span>](lync-server-2013-clientversions-table.md)

  - [<span data-ttu-id="16ce9-112">Lync Server 2013 中的 ConferenceJoinTimeThresholds 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-112">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>](lync-server-2013-conferencejointimethresholds-table.md)

  - [<span data-ttu-id="16ce9-113">Lync Server 2013 中的 ConferenceMessageCount 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-113">ConferenceMessageCount table in Lync Server 2013</span></span>](lync-server-2013-conferencemessagecount-table.md)

  - [<span data-ttu-id="16ce9-114">Lync Server 2013 中的 Conferences 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-114">Conferences table in Lync Server 2013</span></span>](lync-server-2013-conferences-table.md)

  - [<span data-ttu-id="16ce9-115">Lync Server 2013 中的 ConferenceSessionDetails 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-115">ConferenceSessionDetails table in Lync Server 2013</span></span>](lync-server-2013-conferencesessiondetails-table.md)

  - [<span data-ttu-id="16ce9-116">Lync Server 2013 中的 ConferenceUris 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-116">ConferenceUris table in Lync Server 2013</span></span>](lync-server-2013-conferenceuris-table.md)

  - [<span data-ttu-id="16ce9-117">Lync Server 2013 中的 ContentTypes 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-117">ContentTypes table in Lync Server 2013</span></span>](lync-server-2013-contenttypes-table.md)

  - [<span data-ttu-id="16ce9-118">Lync Server 2013 中的 DeRegisterType 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-118">DeRegisterType table in Lync Server 2013</span></span>](lync-server-2013-deregistertype-table.md)

  - [<span data-ttu-id="16ce9-119">Lync Server 2013 中的 Devices 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-119">Devices table in Lync Server 2013</span></span>](lync-server-2013-devices-table.md)

  - [<span data-ttu-id="16ce9-120">Lync Server 2013 中的 Dialogs 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-120">Dialogs table in Lync Server 2013</span></span>](lync-server-2013-dialogs-table.md)

  - [<span data-ttu-id="16ce9-121">Lync Server 2013 中的 EdgeServers 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-121">EdgeServers table in Lync Server 2013</span></span>](lync-server-2013-edgeservers-table.md)

  - [<span data-ttu-id="16ce9-122">Lync Server 2013 中的 ErrorCategory 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-122">ErrorCategory table in Lync Server 2013</span></span>](lync-server-2013-errorcategory-table.md)

  - [<span data-ttu-id="16ce9-123">Lync Server 2013 中的 ErrorDef 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-123">ErrorDef table in Lync Server 2013</span></span>](lync-server-2013-errordef-table.md)

  - [<span data-ttu-id="16ce9-124">Lync Server 2013 中的 ErrorReport 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-124">ErrorReport table in Lync Server 2013</span></span>](lync-server-2013-errorreport-table.md)

  - [<span data-ttu-id="16ce9-125">Lync Server 2013 中的 FileTransfers 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-125">FileTransfers table in Lync Server 2013</span></span>](lync-server-2013-filetransfers-table.md)

  - [<span data-ttu-id="16ce9-126">Lync Server 2013 中的 FocusJoinsAndLeaves 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-126">FocusJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-focusjoinsandleaves-table.md)

  - [<span data-ttu-id="16ce9-127">Lync Server 2013 中的前端表</span><span class="sxs-lookup"><span data-stu-id="16ce9-127">FrontEnd table in Lync Server 2013</span></span>](lync-server-2013-frontend-table.md)

  - [<span data-ttu-id="16ce9-128">Lync Server 2013 中的 Gateways 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-128">Gateways table in Lync Server 2013</span></span>](lync-server-2013-gateways-table.md)

  - [<span data-ttu-id="16ce9-129">Lync Server 2013 中的 HardwareVersions 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-129">HardwareVersions table in Lync Server 2013</span></span>](lync-server-2013-hardwareversions-table.md)

  - [<span data-ttu-id="16ce9-130">Lync Server 2013 中的 IMReportSummary 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-130">IMReportSummary table in Lync Server 2013</span></span>](lync-server-2013-imreportsummary-table.md)

  - [<span data-ttu-id="16ce9-131">Lync Server 2013 中的 Locations 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-131">Locations table in Lync Server 2013</span></span>](lync-server-2013-locations-table.md)

  - [<span data-ttu-id="16ce9-132">Lync Server 2013 中的 Manufacturers 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-132">Manufacturers table in Lync Server 2013</span></span>](lync-server-2013-manufacturers-table.md)

  - [<span data-ttu-id="16ce9-133">Lync Server 2013 中的 McuJoinsAndLeaves 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-133">McuJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-mcujoinsandleaves-table.md)

  - [<span data-ttu-id="16ce9-134">Lync Server 2013 中的 Mcus 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-134">Mcus table in Lync Server 2013</span></span>](lync-server-2013-mcus-table.md)

  - [<span data-ttu-id="16ce9-135">Lync Server 2013 中的 Media 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-135">Media table in Lync Server 2013</span></span>](lync-server-2013-media-table.md)

  - [<span data-ttu-id="16ce9-136">Lync Server 2013 中的 MediaList 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-136">MediaList table in Lync Server 2013</span></span>](lync-server-2013-medialist-table.md)

  - [<span data-ttu-id="16ce9-137">Lync Server 2013 中的 MediationServers 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-137">MediationServers table in Lync Server 2013</span></span>](lync-server-2013-mediationservers-table.md)

  - [<span data-ttu-id="16ce9-138">Lync Server 2013 中的 MSMQProcessing 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-138">MSMQProcessing table in Lync Server 2013</span></span>](lync-server-2013-msmqprocessing-table.md)

  - [<span data-ttu-id="16ce9-139">Lync Server 2013 中的 Phones 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-139">Phones table in Lync Server 2013</span></span>](lync-server-2013-phones-table.md)

  - [<span data-ttu-id="16ce9-140">Lync Server 2013 中的 Pools 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-140">Pools table in Lync Server 2013</span></span>](lync-server-2013-pools-table.md)

  - [<span data-ttu-id="16ce9-141">Lync Server 2013 中的 ProgressReport 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-141">ProgressReport table in Lync Server 2013</span></span>](lync-server-2013-progressreport-table.md)

  - [<span data-ttu-id="16ce9-142">Lync Server 2013 中的 PurgeSettings 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-142">PurgeSettings table in Lync Server 2013</span></span>](lync-server-2013-purgesettings-table.md)

  - [<span data-ttu-id="16ce9-143">Lync Server 2013 中的 Registration 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-143">Registration table in Lync Server 2013</span></span>](lync-server-2013-registration-table.md)

  - [<span data-ttu-id="16ce9-144">Lync Server 2013 中的 Roles 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-144">Roles table in Lync Server 2013</span></span>](lync-server-2013-roles-table.md)

  - [<span data-ttu-id="16ce9-145">Lync Server 2013 中的 Servers 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-145">Servers table in Lync Server 2013</span></span>](lync-server-2013-servers-table.md)

  - [<span data-ttu-id="16ce9-146">Lync Server 2013 中的 SessionDetails 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-146">SessionDetails table in Lync Server 2013</span></span>](lync-server-2013-sessiondetails-table.md)

  - [<span data-ttu-id="16ce9-147">Lync Server 2013 中的 SIPResponseMetaData 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-147">SIPResponseMetaData table in Lync Server 2013</span></span>](lync-server-2013-sipresponsemetadata-table.md)

  - [<span data-ttu-id="16ce9-148">Lync Server 2013 中的 Syndicators 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-148">Syndicators table in Lync Server 2013</span></span>](lync-server-2013-syndicators-table.md)

  - [<span data-ttu-id="16ce9-149">Lync Server 2013 中的 SyndicatorsTenantMap 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-149">SyndicatorsTenantMap table in Lync Server 2013</span></span>](lync-server-2013-syndicatorstenantmap-table.md)

  - [<span data-ttu-id="16ce9-150">Lync Server 2013 中的任务表</span><span class="sxs-lookup"><span data-stu-id="16ce9-150">Task table in Lync Server 2013</span></span>](lync-server-2013-task-table.md)

  - [<span data-ttu-id="16ce9-151">Lync Server 2013 中的 Tenants 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-151">Tenants table in Lync Server 2013</span></span>](lync-server-2013-tenants-table.md)

  - [<span data-ttu-id="16ce9-152">Lync Server 2013 中的 UriTypes 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-152">UriTypes table in Lync Server 2013</span></span>](lync-server-2013-uritypes-table.md)

  - [<span data-ttu-id="16ce9-153">Lync Server 2013 中的 Users 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-153">Users table in Lync Server 2013</span></span>](lync-server-2013-users-table.md)

  - [<span data-ttu-id="16ce9-154">Lync Server 2013 中的 UserAgentDef 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-154">UserAgentDef table in Lync Server 2013</span></span>](lync-server-2013-useragentdef-table.md)

  - [<span data-ttu-id="16ce9-155">Lync Server 2013 中的 UserStatistics 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-155">UserStatistics table in Lync Server 2013</span></span>](lync-server-2013-userstatistics-table.md)

  - [<span data-ttu-id="16ce9-156">Lync Server 2013 中的 VoipDetails 表</span><span class="sxs-lookup"><span data-stu-id="16ce9-156">VoipDetails table in Lync Server 2013</span></span>](lync-server-2013-voipdetails-table.md)

<span data-ttu-id="16ce9-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16ce9-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

