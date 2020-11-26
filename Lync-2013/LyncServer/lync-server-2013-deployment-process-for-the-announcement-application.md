---
title: Lync Server 2013：公告应用程序的部署过程
description: Lync Server 2013：公告应用程序的部署过程。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for the Announcement application
ms:assetid: 72c66249-c4ce-48ce-b1b9-90ebf77d7805
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398545(v=OCS.15)
ms:contentKeyID: 48184500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 559977c32f63fae312164b5b0c36698fa13afb09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429641"
---
# <a name="deployment-process-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="90fd2-103">Lync Server 2013 中的公告应用程序的部署过程</span><span class="sxs-lookup"><span data-stu-id="90fd2-103">Deployment process for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90fd2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90fd2-104">

<span> </span></span></span>

<span data-ttu-id="90fd2-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="90fd2-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="90fd2-106">本部分概述了部署公告应用程序所涉及的步骤。</span><span class="sxs-lookup"><span data-stu-id="90fd2-106">This section provides an overview of the steps involved in deploying the Announcement application.</span></span> <span data-ttu-id="90fd2-107">您必须先部署企业语音，然后才能配置公告。</span><span class="sxs-lookup"><span data-stu-id="90fd2-107">You must deploy Enterprise Voice before you configure announcements.</span></span> <span data-ttu-id="90fd2-108">部署 "企业语音" 时，安装并启用公告应用程序所需的组件。</span><span class="sxs-lookup"><span data-stu-id="90fd2-108">The components required by the Announcement application are installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="announcement-deployment-process"></a><span data-ttu-id="90fd2-109">通知部署过程</span><span class="sxs-lookup"><span data-stu-id="90fd2-109">Announcement Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90fd2-110">阶段</span><span class="sxs-lookup"><span data-stu-id="90fd2-110">Phase</span></span></th>
<th><span data-ttu-id="90fd2-111">步骤</span><span class="sxs-lookup"><span data-stu-id="90fd2-111">Steps</span></span></th>
<th><span data-ttu-id="90fd2-112">角色</span><span class="sxs-lookup"><span data-stu-id="90fd2-112">Roles</span></span></th>
<th><span data-ttu-id="90fd2-113">部署文档</span><span class="sxs-lookup"><span data-stu-id="90fd2-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90fd2-114">配置通知设置</span><span class="sxs-lookup"><span data-stu-id="90fd2-114">Configure Announcement settings</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="90fd2-115">通过录制并上载音频文件或使用文本到语音转换 (TTS) 来创建通知。</span><span class="sxs-lookup"><span data-stu-id="90fd2-115">Create the announcement by recording and uploading audio files or by using text-to-speech (TTS).</span></span></p></li>
<li><p><span data-ttu-id="90fd2-116">配置未分配号码表中的未分配号码范围，然后将其与相应的通知关联。</span><span class="sxs-lookup"><span data-stu-id="90fd2-116">Configure the unassigned number ranges in the unassigned number table and associate them with the appropriate announcement.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="90fd2-117">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="90fd2-117">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="90fd2-118">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="90fd2-118">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="90fd2-119">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="90fd2-119">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="90fd2-120">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="90fd2-120">CsAdministrator</span></span></p>
<p><span data-ttu-id="90fd2-121">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="90fd2-121">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="90fd2-122"><a href="lync-server-2013-create-an-announcement.md">在 Lync Server 2013 中创建公告</a></span><span class="sxs-lookup"><span data-stu-id="90fd2-122"><a href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="90fd2-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">在 Lync Server 2013 中配置未分配号码表</a></span><span class="sxs-lookup"><span data-stu-id="90fd2-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Configure the unassigned number table in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90fd2-124">验证通知部署</span><span class="sxs-lookup"><span data-stu-id="90fd2-124">Verify your Announcement deployment</span></span></p></td>
<td><p><span data-ttu-id="90fd2-125">通过侦听通知来进行测试以验证配置是否按预期工作。</span><span class="sxs-lookup"><span data-stu-id="90fd2-125">Test by listening to announcements to verify that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="90fd2-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md"> (可选) 在 Lync Server 2013 中验证公告部署</a></span><span class="sxs-lookup"><span data-stu-id="90fd2-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">(Optional) Verify Announcement deployment in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="90fd2-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90fd2-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

