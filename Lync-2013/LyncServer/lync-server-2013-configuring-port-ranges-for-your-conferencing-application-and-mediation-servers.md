---
title: Lync Server 2013：为你的会议、应用程序和中介服务器配置端口范围
description: Lync Server 2013：为你的会议、应用程序和中介服务器配置端口范围。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Conferencing, Application, and Mediation servers
ms:assetid: 4d6eaa5d-0127-453f-be6a-e55384772d83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204872(v=OCS.15)
ms:contentKeyID: 48184074
ms.date: 05/01/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eb3f51e42c86b667b6990f41640bf09e12e840c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432756"
---
# <a name="configuring-port-ranges-in-lync-server-2013-for-your-conferencing-application-and-mediation-servers"></a><span data-ttu-id="99778-103">为你的会议、应用程序和中介服务器在 Lync Server 2013 中配置端口范围</span><span class="sxs-lookup"><span data-stu-id="99778-103">Configuring port ranges in Lync Server 2013 for your Conferencing, Application, and Mediation servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99778-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99778-104">

<span> </span></span></span>

<span data-ttu-id="99778-105">_**主题上次修改时间：** 2015-04-30_</span><span class="sxs-lookup"><span data-stu-id="99778-105">_**Topic Last Modified:** 2015-04-30_</span></span>

<span data-ttu-id="99778-106">为了实现服务质量，你应该为你的会议、应用程序和中介服务器上的音频、视频和应用程序共享配置相同的端口范围;此外，这些端口范围不得以任何方式重叠。</span><span class="sxs-lookup"><span data-stu-id="99778-106">In order to implement Quality of Service, you should configure identical port ranges for audio, video, and application sharing on your Conferencing, Application, and Mediation servers; furthermore, those port ranges must not overlap in any way.</span></span> <span data-ttu-id="99778-107">若要使用一个简单的示例，请假设你在你的会议服务器上使用端口10000到10999获取视频。</span><span class="sxs-lookup"><span data-stu-id="99778-107">To use a simple example, suppose you use ports 10000 through 10999 for video on your Conferencing servers.</span></span> <span data-ttu-id="99778-108">这意味着你还必须为应用程序和中介服务器上的视频保留端口10000到10999。</span><span class="sxs-lookup"><span data-stu-id="99778-108">That means that you must also reserve ports 10000 through 10999 for video on your Application and Mediation servers.</span></span> <span data-ttu-id="99778-109">如果不这样做，QoS 将不会按预期工作。</span><span class="sxs-lookup"><span data-stu-id="99778-109">If you do not, QoS will not work as expected.</span></span>

<span data-ttu-id="99778-110">同样，假设您为视频保留了端口10000到10999，但随后为音频保留了端口10500至11999。</span><span class="sxs-lookup"><span data-stu-id="99778-110">Similarly, suppose you reserve ports 10000 through 10999 for video, but then reserve ports 10500 through 11999 for audio.</span></span> <span data-ttu-id="99778-111">这可能会导致服务质量出现问题，因为端口范围重叠。</span><span class="sxs-lookup"><span data-stu-id="99778-111">This can create problems for Quality of Service, because the port ranges overlap.</span></span> <span data-ttu-id="99778-112">使用 QoS，每个模态必须具有一组独特的端口：如果将端口10000到10999用于视频，则必须使用不同的范围 (例如，11000到11999进行音频) 。</span><span class="sxs-lookup"><span data-stu-id="99778-112">With QoS, each modality must have a unique set of ports: if you use ports 10000 through 10999 for video, then you'll have to use a different range (for example, 11000 through 11999 for audio).</span></span>

<span data-ttu-id="99778-113">默认情况下，在 Microsoft Lync Server 2013 中，音频和视频端口范围不重叠;但是，分配给应用程序共享的端口范围与音频和视频端口范围重叠。</span><span class="sxs-lookup"><span data-stu-id="99778-113">By default, audio and video port ranges do not overlap in Microsoft Lync Server 2013; however, the port ranges assigned to application sharing overlap with both the audio and video port ranges.</span></span> <span data-ttu-id="99778-114"> (这意味着这些范围都不是唯一的。 ) 你可以通过从 Lync Server 2013 管理外壳程序中运行以下三个命令来验证你的会议、应用程序和中介服务器的现有端口范围：</span><span class="sxs-lookup"><span data-stu-id="99778-114">(Which, in turn, means that none of these ranges are unique.) You can verify the existing port ranges for your Conferencing, Application, and Mediation servers by running the following three commands from within the Lync Server 2013 Management Shell:</span></span>

    Get-CsService -ConferencingServer | Select-Object Identity, AudioPortStart, AudioPortCount, VideoPortStart, VideoPortCount, AppSharingPortStart, AppSharingPortCount
    
    Get-CsService -ApplicationServer | Select-Object Identity, AudioPortStart, AudioPortCount
    
    Get-CsService -MediationServer | Select-Object Identity, AudioPortStart, AudioPortCount

<div>


> [!WARNING]  
> <span data-ttu-id="99778-115">正如您在前面的命令中所看到的，每个端口类型（音频、视频和应用程序共享）都分配有两个单独的属性值：端口开始和端口计数。</span><span class="sxs-lookup"><span data-stu-id="99778-115">As you can see in the preceding commands, each port type – audio, video, and application sharing – is assigned two separate property values: the port start and the port count.</span></span> <span data-ttu-id="99778-116">端口启动指示用于该模态的第一个端口;例如，如果音频端口开始等于50000，则表示音频流量使用的第一个端口是端口50000。</span><span class="sxs-lookup"><span data-stu-id="99778-116">The port start indicates the first port used for that modality; for example, if the audio port start is equal to 50000 that means that the first port used for audio traffic is port 50000.</span></span> <span data-ttu-id="99778-117">如果音频端口计数为 2 (它不是有效值，但在此处用于说明用途) 这意味着仅为音频分配两个端口。</span><span class="sxs-lookup"><span data-stu-id="99778-117">If the audio port count is 2 (which is not a valid value, but is used here for illustration purposes) that means that only 2 ports are allocated for audio.</span></span> <span data-ttu-id="99778-118">如果第一个端口是端口50000，并且总共有两个端口，则意味着第二个端口必须是端口 50001 (端口范围必须是相邻的) 。</span><span class="sxs-lookup"><span data-stu-id="99778-118">If the first port is port 50000 and there are a total of two ports, that means the second port must be port 50001 (port ranges have to be contiguous).</span></span> <span data-ttu-id="99778-119">因此，音频的端口范围将是端口50000到50001（包括端口到）。</span><span class="sxs-lookup"><span data-stu-id="99778-119">As a result, the port range for audio would be ports 50000 through 50001, inclusive.</span></span><BR><span data-ttu-id="99778-120">请注意，应用服务器和中介服务器仅支持音频的 QoS;无需在应用程序服务器或中介服务器中更改视频或应用程序共享端口。</span><span class="sxs-lookup"><span data-stu-id="99778-120">Note, too that Application server and Mediation server only support QoS for audio; you do not need to change video or application sharing ports in your Application servers or Mediation servers.</span></span>



</div>

<span data-ttu-id="99778-121">如果你运行上述三个命令，你将看到 Lync Server 2013 的默认端口值配置如下：</span><span class="sxs-lookup"><span data-stu-id="99778-121">If you run the preceding three commands you'll see that the default port values for Lync Server 2013 are configured like this:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99778-122">属性</span><span class="sxs-lookup"><span data-stu-id="99778-122">Property</span></span></th>
<th><span data-ttu-id="99778-123">会议服务器</span><span class="sxs-lookup"><span data-stu-id="99778-123">Conferencing Server</span></span></th>
<th><span data-ttu-id="99778-124">应用程序服务器</span><span class="sxs-lookup"><span data-stu-id="99778-124">Application Server</span></span></th>
<th><span data-ttu-id="99778-125">中介服务器</span><span class="sxs-lookup"><span data-stu-id="99778-125">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99778-126">AudioPortStart</span><span class="sxs-lookup"><span data-stu-id="99778-126">AudioPortStart</span></span></p></td>
<td><p><span data-ttu-id="99778-127">49152</span><span class="sxs-lookup"><span data-stu-id="99778-127">49152</span></span></p></td>
<td><p><span data-ttu-id="99778-128">49152</span><span class="sxs-lookup"><span data-stu-id="99778-128">49152</span></span></p></td>
<td><p><span data-ttu-id="99778-129">49152</span><span class="sxs-lookup"><span data-stu-id="99778-129">49152</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99778-130">AudioPortCount</span><span class="sxs-lookup"><span data-stu-id="99778-130">AudioPortCount</span></span></p></td>
<td><p><span data-ttu-id="99778-131">8348</span><span class="sxs-lookup"><span data-stu-id="99778-131">8348</span></span></p></td>
<td><p><span data-ttu-id="99778-132">8348</span><span class="sxs-lookup"><span data-stu-id="99778-132">8348</span></span></p></td>
<td><p><span data-ttu-id="99778-133">8348</span><span class="sxs-lookup"><span data-stu-id="99778-133">8348</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99778-134">VideoPortStart</span><span class="sxs-lookup"><span data-stu-id="99778-134">VideoPortStart</span></span></p></td>
<td><p><span data-ttu-id="99778-135">57501</span><span class="sxs-lookup"><span data-stu-id="99778-135">57501</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99778-136">VideoPortCount</span><span class="sxs-lookup"><span data-stu-id="99778-136">VideoPortCount</span></span></p></td>
<td><p><span data-ttu-id="99778-137">8034</span><span class="sxs-lookup"><span data-stu-id="99778-137">8034</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99778-138">ApplicationSharingPortStart</span><span class="sxs-lookup"><span data-stu-id="99778-138">ApplicationSharingPortStart</span></span></p></td>
<td><p><span data-ttu-id="99778-139">49152</span><span class="sxs-lookup"><span data-stu-id="99778-139">49152</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99778-140">ApplicationSharingPortCount</span><span class="sxs-lookup"><span data-stu-id="99778-140">ApplicationSharingPortCount</span></span></p></td>
<td><p><span data-ttu-id="99778-141">16383</span><span class="sxs-lookup"><span data-stu-id="99778-141">16383</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="99778-142">如前所述，为 QoS 配置 Lync 服务器端口时，应确保： 1) 音频端口设置在你的所有会议、应用程序和中介服务器上都相同;2) 端口范围不重叠。</span><span class="sxs-lookup"><span data-stu-id="99778-142">As noted previously, when configuring Lync Server ports for QoS, you should ensure that: 1) audio port settings are identical across yours Conferencing, Application, and Mediation servers; and, 2) port ranges do not overlap.</span></span> <span data-ttu-id="99778-143">如果仔细查看上表，您将看到端口范围在三种服务器类型中相同。</span><span class="sxs-lookup"><span data-stu-id="99778-143">If you look closely at the preceding table, you will see that the port ranges are identical across the three server types.</span></span> <span data-ttu-id="99778-144">例如，每个服务器类型上的起始音频端口设置为端口49152，并且每台服务器中为音频保留的端口总数也相同：8348。</span><span class="sxs-lookup"><span data-stu-id="99778-144">For example, the starting audio port is set to port 49152 on each server type, and the total number of ports reserved for audio in each server is also identical: 8348.</span></span> <span data-ttu-id="99778-145">但是，端口范围重叠：音频端口从端口49152开始，但将为应用程序共享预留端口。</span><span class="sxs-lookup"><span data-stu-id="99778-145">However, the port ranges overlap: audio ports start at port 49152, but so do the ports set aside for application sharing.</span></span> <span data-ttu-id="99778-146">为了获得最佳使用服务质量，应将应用程序共享重新配置为使用唯一的端口范围。</span><span class="sxs-lookup"><span data-stu-id="99778-146">In order to make optimal use of Quality of Service, application sharing should be reconfigured to use a unique port range.</span></span> <span data-ttu-id="99778-147">例如，你可以将应用程序共享配置为从端口40803开始，并使用8348端口。</span><span class="sxs-lookup"><span data-stu-id="99778-147">For example, you could configure application sharing to start at port 40803 and to use 8348 ports.</span></span> <span data-ttu-id="99778-148"> (为什么是8348端口？</span><span class="sxs-lookup"><span data-stu-id="99778-148">(Why 8348 ports?</span></span> <span data-ttu-id="99778-149">如果将这些值一起添加-40803 + 8348-这意味着应用程序共享将通过端口49150使用端口40803。</span><span class="sxs-lookup"><span data-stu-id="99778-149">If you add those values together -- 40803 + 8348 -- that means that application sharing will use ports 40803 through port 49150.</span></span> <span data-ttu-id="99778-150">由于音频端口不会在端口49152开始，因此你将不再有任何重叠的端口范围。 ) </span><span class="sxs-lookup"><span data-stu-id="99778-150">Because audio ports do not begin until port 49152, you will no longer have any overlapping port ranges.)</span></span>

<span data-ttu-id="99778-151">为应用程序共享选择新的端口范围后，您可以使用 Set-CsConferencingServer cmdlet 进行更改。</span><span class="sxs-lookup"><span data-stu-id="99778-151">After you have selected the new port range for application sharing you can make your change by using the Set-CsConferencingServer cmdlet.</span></span> <span data-ttu-id="99778-152">无需在应用程序服务器或中介服务器上进行此更改，因为这些服务器不处理应用程序共享流量。</span><span class="sxs-lookup"><span data-stu-id="99778-152">This change does not need to be made on your Application servers or on your Mediation servers, because these servers do not handle application sharing traffic.</span></span> <span data-ttu-id="99778-153">如果你决定重新分配用于音频流量的端口，则只需在这些服务器上更改端口值。</span><span class="sxs-lookup"><span data-stu-id="99778-153">You only need to change port values on these servers if you decide to reassign the ports used for audio traffic.</span></span>

<span data-ttu-id="99778-154">若要修改单个会议服务器上的应用程序共享的端口值，请在 Lync Server Management Shell 中运行类似下面的命令：</span><span class="sxs-lookup"><span data-stu-id="99778-154">To modify the port values for application sharing on a single Conferencing server run a command similar to this from within the Lync Server Management Shell:</span></span>

    Set-CsConferenceServer -Identity ConferencingServer:atl-cs-001.litwareinc.com -AppSharingPortStart 40803 -AppSharingPortCount 8348

<span data-ttu-id="99778-155">如果要在所有的会议服务器上进行这些更改，可以改为运行此命令：</span><span class="sxs-lookup"><span data-stu-id="99778-155">If you want to make these changes on all your Conferencing servers you can run this command instead:</span></span>

    Get-CsService -ConferencingServer | ForEach-Object {Set-CsConferenceServer -Identity $_.Identity -AppSharingPortStart 40803 -AppSharingPortCount 8348}

<span data-ttu-id="99778-156">更改端口设置后，你应该停止并重新启动受更改影响的每个服务。</span><span class="sxs-lookup"><span data-stu-id="99778-156">After changing port settings you should stop and then restart each service affected by the changes.</span></span>

<span data-ttu-id="99778-157">不强制您的会议服务器、应用程序服务器和中介服务器共享完全相同的端口范围;唯一的真正要求是，您可以在所有服务器上留出唯一的端口范围。</span><span class="sxs-lookup"><span data-stu-id="99778-157">It is not mandatory that your Conferencing servers, Application servers, and Mediation servers share the exact same port range; the only true requirement is that you set aside unique port ranges on all your servers.</span></span> <span data-ttu-id="99778-158">但是，如果你在所有服务器上使用相同的端口集，管理通常会更容易。</span><span class="sxs-lookup"><span data-stu-id="99778-158">However, administration will typically be easier if you use the same set of ports on all your servers.</span></span>

<span data-ttu-id="99778-159"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99778-159"></div>

<span> </span>

</div>

</div>

</span></span></div>

