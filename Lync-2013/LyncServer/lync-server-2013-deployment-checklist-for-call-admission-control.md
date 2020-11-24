---
title: Lync Server 2013：呼叫允许控制的部署清单
description: Lync Server 2013：用于呼叫许可控制的部署核对清单。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for call admission control
ms:assetid: 7e56a169-3e63-44ab-bf28-1fdeb52381c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398631(v=OCS.15)
ms:contentKeyID: 48184621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea5b16d41228faf01637e7e0d78f5ce56f950a19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391749"
---
# <a name="deployment-checklist-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="886c7-103">Lync Server 2013 中呼叫允许控制的部署清单</span><span class="sxs-lookup"><span data-stu-id="886c7-103">Deployment checklist for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="886c7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="886c7-104">

<span> </span></span></span>

<span data-ttu-id="886c7-105">_**主题上次修改时间：** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="886c7-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="886c7-106">要有效地为呼叫许可控制计划 (CAC) ，您需要考虑以下事项：</span><span class="sxs-lookup"><span data-stu-id="886c7-106">To plan effectively for call admission control (CAC), you need to consider the following:</span></span>

  - <span data-ttu-id="886c7-107">部署 CAC 的先决条件。</span><span class="sxs-lookup"><span data-stu-id="886c7-107">Prerequisites for deploying CAC.</span></span>

  - <span data-ttu-id="886c7-108">在部署之前必须进行的 CAC 和配置决策所需的信息。</span><span class="sxs-lookup"><span data-stu-id="886c7-108">Information required for CAC and configuration decisions that you must make in advance of deployment.</span></span>

<div>

## <a name="deployment-prerequisites-for-call-admission-control"></a><span data-ttu-id="886c7-109">呼叫许可控制的部署先决条件</span><span class="sxs-lookup"><span data-stu-id="886c7-109">Deployment Prerequisites for Call Admission Control</span></span>

<span data-ttu-id="886c7-110">在部署 "呼叫许可控制" 之前，您必须已部署了 Lync Server 2013 内部服务器，包括 "前端" 池或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="886c7-110">Before you deploy call admission control, you must already have deployed your Lync Server 2013 internal servers, including either a Front End pool or a Standard Edition server.</span></span>

</div>

<div>

## <a name="information-requirements-for-call-admission-control"></a><span data-ttu-id="886c7-111">呼叫许可控制的信息要求</span><span class="sxs-lookup"><span data-stu-id="886c7-111">Information Requirements for Call Admission Control</span></span>

<span data-ttu-id="886c7-112">下表总结了部署 "呼叫许可控制" 所需的信息。</span><span class="sxs-lookup"><span data-stu-id="886c7-112">The following table summarizes the required information for deploying call admission control.</span></span>

### <a name="information-requirements-for-call-admission-control-deployment"></a><span data-ttu-id="886c7-113">呼叫许可控制部署的信息要求</span><span class="sxs-lookup"><span data-stu-id="886c7-113">Information Requirements for Call Admission Control Deployment</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="886c7-114">信息</span><span class="sxs-lookup"><span data-stu-id="886c7-114">Information</span></span></th>
<th><span data-ttu-id="886c7-115">所需信息摘要</span><span class="sxs-lookup"><span data-stu-id="886c7-115">Summary of Information Required</span></span></th>
<th><span data-ttu-id="886c7-116">文档</span><span class="sxs-lookup"><span data-stu-id="886c7-116">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="886c7-117">您的组织所需的 Lync 服务器功能</span><span class="sxs-lookup"><span data-stu-id="886c7-117">Lync Server capabilities required by your organization</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="886c7-118">您的组织支持的功能</span><span class="sxs-lookup"><span data-stu-id="886c7-118">Capabilities to be supported by your organization</span></span></p></li>
<li><p><span data-ttu-id="886c7-119">为单个用户启用的功能</span><span class="sxs-lookup"><span data-stu-id="886c7-119">Capabilities to be enabled for individual users</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="886c7-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">在 Lync Server 2013 中定义呼叫允许控制要求</a></span><span class="sxs-lookup"><span data-stu-id="886c7-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="886c7-121">要部署的拓扑和组件</span><span class="sxs-lookup"><span data-stu-id="886c7-121">Topologies and components to be deployed</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="886c7-122">CAC 相关组件将作为 Lync Server 2013 的一部分自动安装</span><span class="sxs-lookup"><span data-stu-id="886c7-122">CAC related components are automatically installed as part of Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="886c7-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">在 Lync Server 2013 中定义呼叫允许控制要求</a></span><span class="sxs-lookup"><span data-stu-id="886c7-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="886c7-124">系统要求</span><span class="sxs-lookup"><span data-stu-id="886c7-124">System requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="886c7-125">硬件要求</span><span class="sxs-lookup"><span data-stu-id="886c7-125">Hardware requirements</span></span></p></li>
<li><p><span data-ttu-id="886c7-126">软件要求</span><span class="sxs-lookup"><span data-stu-id="886c7-126">Software requirements</span></span></p></li>
<li><p><span data-ttu-id="886c7-127">Collocation 要求</span><span class="sxs-lookup"><span data-stu-id="886c7-127">Collocation requirements</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="886c7-128"><a href="lync-server-2013-determining-your-system-requirements.md">确定 Lync Server 2013 的系统要求</a></span><span class="sxs-lookup"><span data-stu-id="886c7-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="886c7-129">基础结构要求</span><span class="sxs-lookup"><span data-stu-id="886c7-129">Infrastructure requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="886c7-130">CAC 不需要特定的基础结构要求</span><span class="sxs-lookup"><span data-stu-id="886c7-130">No specific infrastructure requirements are necessary for CAC</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="886c7-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Lync Server 2013 中呼叫允许控制的基础结构要求</a></span><span class="sxs-lookup"><span data-stu-id="886c7-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Infrastructure requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="886c7-132">网络接口要求</span><span class="sxs-lookup"><span data-stu-id="886c7-132">Network interface requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="886c7-133">内部和外部接口信息</span><span class="sxs-lookup"><span data-stu-id="886c7-133">Internal and external interface information</span></span></p></li>
<li><p><span data-ttu-id="886c7-134">路由信息 (包括有关在 <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a> Microsoft Lync Server 团队的客户响应频道中的 NextHop 博客的信息) </span><span class="sxs-lookup"><span data-stu-id="886c7-134">Routing information (including information on the NextHop blog at <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a>, Microsoft Lync Server team’s customer response channel)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="886c7-135"><a href="lync-server-2013-deploying-external-user-access.md">在 Lync Server 2013 中部署外部用户访问</a></span><span class="sxs-lookup"><span data-stu-id="886c7-135"><a href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="886c7-136">部署策略</span><span class="sxs-lookup"><span data-stu-id="886c7-136">Deployment strategy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="886c7-137">部署序列</span><span class="sxs-lookup"><span data-stu-id="886c7-137">Deployment sequence</span></span></p></li>
<li><p><span data-ttu-id="886c7-138">工作组或域</span><span class="sxs-lookup"><span data-stu-id="886c7-138">Workgroup or domain</span></span></p></li>
<li><p><span data-ttu-id="886c7-139">安全性</span><span class="sxs-lookup"><span data-stu-id="886c7-139">Security</span></span></p></li>
<li><p><span data-ttu-id="886c7-140">监视和审核</span><span class="sxs-lookup"><span data-stu-id="886c7-140">Monitoring and auditing</span></span></p></li>
<li><p><span data-ttu-id="886c7-141">硬件注意事项</span><span class="sxs-lookup"><span data-stu-id="886c7-141">Hardware considerations</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="886c7-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Lync Server 2013 中呼叫允许控制的最佳做法</a></span><span class="sxs-lookup"><span data-stu-id="886c7-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Best practices for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="886c7-143">部署过程</span><span class="sxs-lookup"><span data-stu-id="886c7-143">Deployment process</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="886c7-144">先决条件</span><span class="sxs-lookup"><span data-stu-id="886c7-144">Prerequisites</span></span></p></li>
<li><p><span data-ttu-id="886c7-145">信息要求</span><span class="sxs-lookup"><span data-stu-id="886c7-145">Information requirements</span></span></p></li>
<li><p><span data-ttu-id="886c7-146">流程和过程</span><span class="sxs-lookup"><span data-stu-id="886c7-146">Process and procedures</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="886c7-147"><a href="lync-server-2013-configure-call-admission-control.md">在 Lync Server 2013 中配置呼叫许可控制</a></span><span class="sxs-lookup"><span data-stu-id="886c7-147"><a href="lync-server-2013-configure-call-admission-control.md">Configure call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="886c7-148">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="886c7-148">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

