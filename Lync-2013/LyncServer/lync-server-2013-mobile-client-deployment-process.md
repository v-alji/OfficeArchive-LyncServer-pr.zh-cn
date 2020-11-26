---
title: Lync Server 2013：移动客户端部署过程
description: Lync Server 2013：移动客户端部署过程。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobile client deployment process
ms:assetid: 6498235b-2fa9-421d-bfa0-0ccc09508dbd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690982(v=OCS.15)
ms:contentKeyID: 51541484
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fa4e9e1d272915e06009df5c06480309ce104e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425561"
---
# <a name="mobile-client-deployment-process-in-lync-server-2013"></a><span data-ttu-id="ff36f-103">Lync Server 2013 中的移动客户端部署过程</span><span class="sxs-lookup"><span data-stu-id="ff36f-103">Mobile client deployment process in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff36f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff36f-104">

<span> </span></span></span>

<span data-ttu-id="ff36f-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="ff36f-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="ff36f-106">完成 Microsoft Lync Server 2013 的部署后，用户可以从移动市场安装 Lync 2013 应用，他们习惯于为其特定设备使用。</span><span class="sxs-lookup"><span data-stu-id="ff36f-106">After a deployment of Microsoft Lync Server 2013 has been completed, users can install the Lync 2013 app from the mobile marketplace that they are accustomed to using for their specific device.</span></span>

<div>

## <a name="lync-mobile-deployment-process"></a><span data-ttu-id="ff36f-107">Lync Mobile 部署过程</span><span class="sxs-lookup"><span data-stu-id="ff36f-107">Lync Mobile Deployment Process</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff36f-108">阶段</span><span class="sxs-lookup"><span data-stu-id="ff36f-108">Phase</span></span></th>
<th><span data-ttu-id="ff36f-109">步骤</span><span class="sxs-lookup"><span data-stu-id="ff36f-109">Steps</span></span></th>
<th><span data-ttu-id="ff36f-110">权限</span><span class="sxs-lookup"><span data-stu-id="ff36f-110">Permissions</span></span></th>
<th><span data-ttu-id="ff36f-111">文档</span><span class="sxs-lookup"><span data-stu-id="ff36f-111">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff36f-112">执行预设置任务。</span><span class="sxs-lookup"><span data-stu-id="ff36f-112">Perform pre-setup tasks.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="ff36f-113">验证 Lync Server 2013 部署。</span><span class="sxs-lookup"><span data-stu-id="ff36f-113">Verify Lync Server 2013 deployment.</span></span></p></li>
<li><p><span data-ttu-id="ff36f-114">验证证书要求。</span><span class="sxs-lookup"><span data-stu-id="ff36f-114">Verify certificate requirements.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="ff36f-115">Administrator</span><span class="sxs-lookup"><span data-stu-id="ff36f-115">Administrator</span></span></p></td>
<td><p><span data-ttu-id="ff36f-116">在服务器规划文档中，在<a href="lync-server-2013-planning-for-mobility.md">Lync Server 2013 中规划行动</a>。</span><span class="sxs-lookup"><span data-stu-id="ff36f-116"><a href="lync-server-2013-planning-for-mobility.md">Planning for mobility in Lync Server 2013</a> in the server planning documentation.</span></span></p>
<p><span data-ttu-id="ff36f-117">在服务器部署文档的<a href="lync-server-2013-deploying-mobility.md">Lync Server 2013 中部署移动性</a>。</span><span class="sxs-lookup"><span data-stu-id="ff36f-117"><a href="lync-server-2013-deploying-mobility.md">Deploying mobility in Lync Server 2013</a> in the server deployment documentation.</span></span></p>
<p><span data-ttu-id="ff36f-118">服务器规划文档中<a href="lync-server-2013-certificate-infrastructure-requirements.md">Lync Server 2013 的证书基础结构要求</a>。</span><span class="sxs-lookup"><span data-stu-id="ff36f-118"><a href="lync-server-2013-certificate-infrastructure-requirements.md">Certificate infrastructure requirements for Lync Server 2013</a> in the server planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff36f-119">在测试设备上安装 Lync 应用程序。</span><span class="sxs-lookup"><span data-stu-id="ff36f-119">Install the Lync application on a test device.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="ff36f-120">安装先决条件。</span><span class="sxs-lookup"><span data-stu-id="ff36f-120">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="ff36f-121">从特定于移动设备的市场安装。</span><span class="sxs-lookup"><span data-stu-id="ff36f-121">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="ff36f-122">Administrator</span><span class="sxs-lookup"><span data-stu-id="ff36f-122">Administrator</span></span></p></td>
<td><p><span data-ttu-id="ff36f-123">在 <a href="lync-server-2013-deploying-mobile-clients.md">Lync Server 2013 中部署移动客户端</a>的移动设备特定的安装说明。</span><span class="sxs-lookup"><span data-stu-id="ff36f-123">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff36f-124">配置客户端。</span><span class="sxs-lookup"><span data-stu-id="ff36f-124">Configure the client.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="ff36f-125">配置登录设置和服务器信息。</span><span class="sxs-lookup"><span data-stu-id="ff36f-125">Configure sign-in settings and server information.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ff36f-126">Administrator</span><span class="sxs-lookup"><span data-stu-id="ff36f-126">Administrator</span></span></p></td>
<td><p><span data-ttu-id="ff36f-127"><a href="lync-server-2013-deploying-mobile-clients.md">在 Lync Server 2013 中部署移动客户端</a></span><span class="sxs-lookup"><span data-stu-id="ff36f-127"><a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff36f-128">测试移动方案。</span><span class="sxs-lookup"><span data-stu-id="ff36f-128">Test mobile scenarios.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="ff36f-129">测试即时消息 (IM) 和状态。</span><span class="sxs-lookup"><span data-stu-id="ff36f-129">Test instant messaging (IM) and presence.</span></span></p></li>
<li><p><span data-ttu-id="ff36f-130">测试拨出式会议。</span><span class="sxs-lookup"><span data-stu-id="ff36f-130">Test dial-out conferencing.</span></span></p></li>
<li><p><span data-ttu-id="ff36f-131">在公司目录中搜索联系人。</span><span class="sxs-lookup"><span data-stu-id="ff36f-131">Search for a contact in the corporate directory.</span></span></p></li>
<li><p><span data-ttu-id="ff36f-132">测试推送通知。</span><span class="sxs-lookup"><span data-stu-id="ff36f-132">Test push notifications.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="ff36f-133">Administrator</span><span class="sxs-lookup"><span data-stu-id="ff36f-133">Administrator</span></span></p></td>
<td><p><span data-ttu-id="ff36f-134">在 <a href="lync-server-2013-deploying-mobile-clients.md">Lync Server 2013 中部署移动客户端</a>的特定于移动设备的验证说明。</span><span class="sxs-lookup"><span data-stu-id="ff36f-134">Verification instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff36f-135">在移动电话上安装 Lync 应用程序。</span><span class="sxs-lookup"><span data-stu-id="ff36f-135">Install the Lync application on mobile phones.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="ff36f-136">安装先决条件。</span><span class="sxs-lookup"><span data-stu-id="ff36f-136">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="ff36f-137">从特定于移动设备的市场安装。</span><span class="sxs-lookup"><span data-stu-id="ff36f-137">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="ff36f-138">用户</span><span class="sxs-lookup"><span data-stu-id="ff36f-138">User</span></span></p></td>
<td><p><span data-ttu-id="ff36f-139">在 <a href="lync-server-2013-deploying-mobile-clients.md">Lync Server 2013 中部署移动客户端</a>的移动设备特定的安装说明。</span><span class="sxs-lookup"><span data-stu-id="ff36f-139">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ff36f-140">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff36f-140">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

