---
title: Lync Server 2013：呼叫寄存的部署过程
description: Lync Server 2013：呼叫寄存的部署过程。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Call Park
ms:assetid: 2000d672-a85f-4262-9d69-0bee9ae3709a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398283(v=OCS.15)
ms:contentKeyID: 48183586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 149252d39ba3fc0c552900c87e453c60e1651a08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392301"
---
# <a name="deployment-process-for-call-park-in-lync-server-2013"></a><span data-ttu-id="daa93-103">Lync Server 2013 中的呼叫寄存的部署过程</span><span class="sxs-lookup"><span data-stu-id="daa93-103">Deployment process for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="daa93-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="daa93-104">

<span> </span></span></span>

<span data-ttu-id="daa93-105">_**主题上次修改时间：** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="daa93-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="daa93-106">本部分概述了部署通话寄存应用程序时所涉及的步骤。</span><span class="sxs-lookup"><span data-stu-id="daa93-106">This section provides an overview of the steps involved in deploying the Call Park application.</span></span> <span data-ttu-id="daa93-107">您必须先部署企业版或具有企业语音的标准版，然后才能配置呼叫寄存。</span><span class="sxs-lookup"><span data-stu-id="daa93-107">You must deploy Enterprise Edition or Standard Edition with Enterprise Voice before you configure Call Park.</span></span> <span data-ttu-id="daa93-108">部署 "企业语音" 时，将安装并启用 "呼叫寄存" 所需的组件。</span><span class="sxs-lookup"><span data-stu-id="daa93-108">The components required by Call Park are installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="call-park-deployment-process"></a><span data-ttu-id="daa93-109">呼叫寄存部署过程</span><span class="sxs-lookup"><span data-stu-id="daa93-109">Call Park Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daa93-110">阶段</span><span class="sxs-lookup"><span data-stu-id="daa93-110">Phase</span></span></th>
<th><span data-ttu-id="daa93-111">步骤</span><span class="sxs-lookup"><span data-stu-id="daa93-111">Steps</span></span></th>
<th><span data-ttu-id="daa93-112">所需的组和角色</span><span class="sxs-lookup"><span data-stu-id="daa93-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="daa93-113">部署文档</span><span class="sxs-lookup"><span data-stu-id="daa93-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daa93-114">在通道表中配置呼叫寄存通道范围</span><span class="sxs-lookup"><span data-stu-id="daa93-114">Configure the call park orbit ranges in the orbit table</span></span></p></td>
<td><p><span data-ttu-id="daa93-115">使用 Lync Server 控制面板或 <strong>CSCallParkOrbit</strong> cmdlet 在 "呼叫公园轨道" 表中创建轨道范围，并将它们与托管呼叫寄存应用程序的应用程序服务相关联。</span><span class="sxs-lookup"><span data-stu-id="daa93-115">Use Lync Server Control Panel or the <strong>New-CSCallParkOrbit</strong> cmdlet to create the orbit ranges in the call park orbit table and associate them with the Application service that hosts the Call Park application.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="daa93-p102">为与现有拨号计划进行无缝集成，通道范围通常配置为虚拟分机块。不支持将外线直拨分机 (DID) 号码分配为呼叫寄存通道表中的通道号码。</span><span class="sxs-lookup"><span data-stu-id="daa93-p102">For seamless integration with existing dial plans, orbit ranges are typically configured as a block of virtual extensions. Assigning Direct Inward Dialing (DID) numbers as orbit numbers in the call park orbit table is not supported.</span></span>


</div></td>
<td><p><span data-ttu-id="daa93-118">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="daa93-118">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="daa93-119">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-119">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="daa93-120">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-120">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="daa93-121">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-121">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="daa93-122"><a href="lync-server-2013-create-or-modify-a-call-park-orbit-range.md">在 Lync Server 2013 中创建或修改呼叫寄存的轨道范围</a></span><span class="sxs-lookup"><span data-stu-id="daa93-122"><a href="lync-server-2013-create-or-modify-a-call-park-orbit-range.md">Create or modify a Call Park orbit range in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa93-123">配置呼叫寄存设置</span><span class="sxs-lookup"><span data-stu-id="daa93-123">Configure Call Park settings</span></span></p></td>
<td><p><span data-ttu-id="daa93-124">使用 <strong>CsCpsConfiguration</strong> Cmdlet 配置呼叫寄存设置。</span><span class="sxs-lookup"><span data-stu-id="daa93-124">Use the <strong>Set-CsCpsConfiguration</strong> cmdlet to configure Call Park settings.</span></span> <span data-ttu-id="daa93-125">我们建议你将 <strong>OnTimeoutURI</strong> 选项配置为配置备用目标以在停止通话超时时使用。您还可以配置以下设置：</span><span class="sxs-lookup"><span data-stu-id="daa93-125">At a minimum, we recommend that you configure the <strong>OnTimeoutURI</strong> option to configure the fallback destination to use when a parked call times out. You can also configure the following settings:</span></span></p>
<ul>
<li><p><span data-ttu-id="daa93-126">（可选）配置 <strong>EnableMusicOnHold</strong> 以启用或禁用保持音乐。</span><span class="sxs-lookup"><span data-stu-id="daa93-126">(Optional) <strong>EnableMusicOnHold</strong> to enable or disable music on hold.</span></span></p></li>
<li><p><span data-ttu-id="daa93-127">（可选）配置 <strong>MaxCallPickupAttempts</strong> 以确定将寄存呼叫转接到回退统一资源标识符 (URI) 之前该呼叫回拨应答电话的次数。</span><span class="sxs-lookup"><span data-stu-id="daa93-127">(Optional) <strong>MaxCallPickupAttempts</strong> to determine the number of times a parked call rings back to the answering phone before forwarding the call to the fallback Uniform Resource Identifier (URI).</span></span></p></li>
<li><p><span data-ttu-id="daa93-128">（可选）配置 <strong>CallPickupTimeoutThreshold</strong> 以确定呼叫寄存后到回拨应答该呼叫的电话之前等待的时间。</span><span class="sxs-lookup"><span data-stu-id="daa93-128">(Optional) <strong>CallPickupTimeoutThreshold</strong> to determine the amount of time that elapses after a call has been parked before it rings back to the phone where the call was answered.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="daa93-129">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="daa93-129">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="daa93-130">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-130">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="daa93-131">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-131">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="daa93-132">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-132">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="daa93-133"><a href="lync-server-2013-configure-call-park-settings.md">在 Lync Server 2013 中配置呼叫寄存设置</a></span><span class="sxs-lookup"><span data-stu-id="daa93-133"><a href="lync-server-2013-configure-call-park-settings.md">Configure Call Park settings in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa93-134">（可选）自定义保持音乐</span><span class="sxs-lookup"><span data-stu-id="daa93-134">Optionally, customize the music on hold</span></span></p></td>
<td><p><span data-ttu-id="daa93-135">使用 <strong>Set-CsCallParkServiceMusicOnHoldFile</strong> cmdlet 自定义并上载音频文件（如果不使用默认的保持音乐）。</span><span class="sxs-lookup"><span data-stu-id="daa93-135">Use the <strong>Set-CsCallParkServiceMusicOnHoldFile</strong> cmdlet to customize and upload an audio file, if you don't want to use the default music on hold.</span></span></p></td>
<td><p><span data-ttu-id="daa93-136">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="daa93-136">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="daa93-137">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-137">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="daa93-138">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-138">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="daa93-139">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-139">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="daa93-140"><a href="lync-server-2013-customize-call-park-music-on-hold.md">在 Lync Server 2013 中自定义呼叫寄存音乐处于暂停状态</a></span><span class="sxs-lookup"><span data-stu-id="daa93-140"><a href="lync-server-2013-customize-call-park-music-on-hold.md">Customize Call Park music on hold in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa93-141">配置语音策略以为用户启用呼叫寄存</span><span class="sxs-lookup"><span data-stu-id="daa93-141">Configure voice policy to enable Call Park for users</span></span></p></td>
<td><p><span data-ttu-id="daa93-142">使用 "Lync Server 控制面板" 或 <strong>CSVoicePolicy</strong> Cmdlet 和 <strong>EnableCallPark</strong> 选项为语音策略中的用户启用呼叫寄存。</span><span class="sxs-lookup"><span data-stu-id="daa93-142">Use Lync Server Control Panel or the <strong>Set-CSVoicePolicy</strong> cmdlet with the <strong>EnableCallPark</strong> option to enable Call Park for users in voice policy.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="daa93-143">默认情况下，将对所有用户禁用 "呼叫寄存"。</span><span class="sxs-lookup"><span data-stu-id="daa93-143">By default, Call Park is disabled for all users.</span></span>


</div>
<div>

> [!NOTE]  
> <span data-ttu-id="daa93-144">如果具有多个语音策略，请确保为每个语音策略（而不只是默认策略）设置 EnableCallPark 属性。</span><span class="sxs-lookup"><span data-stu-id="daa93-144">If you have multiple voice policies, make sure the EnableCallPark property is set for each voice policy, not just for the default policy.</span></span>


</div></td>
<td><p><span data-ttu-id="daa93-145">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="daa93-145">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="daa93-146">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-146">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="daa93-147">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-147">CsUserAdministrator</span></span></p>
<p><span data-ttu-id="daa93-148">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-148">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="daa93-149"><a href="lync-server-2013-enable-call-park-for-users.md">在 Lync Server 2013 中为用户启用呼叫寄存</a></span><span class="sxs-lookup"><span data-stu-id="daa93-149"><a href="lync-server-2013-enable-call-park-for-users.md">Enable Call Park for users in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa93-150">验证呼叫寄存的规范化规则</span><span class="sxs-lookup"><span data-stu-id="daa93-150">Verify normalization rules for Call Park</span></span></p></td>
<td><p><span data-ttu-id="daa93-p104">不能对呼叫寄存通道进行规范化。验证规范化规则是否未包含任何通道范围。如有必要，创建其他规范化规则以阻止对通道进行规范化。</span><span class="sxs-lookup"><span data-stu-id="daa93-p104">Call park orbits must not be normalized. Verify that your normalization rules do not include any of your orbit ranges. If necessary, create additional normalization rules to prevent orbits being normalized.</span></span></p></td>
<td><p><span data-ttu-id="daa93-154">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="daa93-154">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="daa93-155">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-155">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="daa93-156">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-156">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="daa93-157">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="daa93-157">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="daa93-158"><a href="lync-server-2013-verify-normalization-rules-for-call-park.md">在 Lync Server 2013 中验证呼叫寄存的规范化规则</a></span><span class="sxs-lookup"><span data-stu-id="daa93-158"><a href="lync-server-2013-verify-normalization-rules-for-call-park.md">Verify normalization rules for Call Park in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa93-159">验证您的电话寄存部署</span><span class="sxs-lookup"><span data-stu-id="daa93-159">Verify your Call Park deployment</span></span></p></td>
<td><p><span data-ttu-id="daa93-160">测试寄存和取回呼叫以确保配置按预期工作。</span><span class="sxs-lookup"><span data-stu-id="daa93-160">Test parking and retrieving calls to make sure that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="daa93-161"><a href="lync-server-2013-optional-verify-call-park-deployment.md"> (可选) 在 Lync Server 2013 中验证呼叫寄存部署</a></span><span class="sxs-lookup"><span data-stu-id="daa93-161"><a href="lync-server-2013-optional-verify-call-park-deployment.md">(Optional) Verify Call Park deployment in Lync Server 2013</a></span></span></p></td>
</tr><span data-ttu-id="daa93-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="daa93-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

