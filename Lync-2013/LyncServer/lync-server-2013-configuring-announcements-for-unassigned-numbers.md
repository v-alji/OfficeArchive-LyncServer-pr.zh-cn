---
title: Lync Server 2013：配置未分配号码的通知
description: Lync Server 2013：配置未分配号码的公告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring announcements for unassigned numbers
ms:assetid: 45633dd3-78de-4934-867e-33969fc25368
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425944(v=OCS.15)
ms:contentKeyID: 48184035
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16ab636f0c6157118a00d5e46521555086c5e520
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392160"
---
# <a name="configuring-announcements-for-unassigned-numbers-in-lync-server-2013"></a><span data-ttu-id="97e2d-103">在 Lync Server 2013 中配置未分配号码的通知</span><span class="sxs-lookup"><span data-stu-id="97e2d-103">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97e2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97e2d-104">

<span> </span></span></span>

<span data-ttu-id="97e2d-105">_**主题上次修改时间：** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="97e2d-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="97e2d-106">"发布" 应用程序是一种企业语音功能，可让你配置调用未分配的扩展 (对你的组织有效但未分配给个人或电话) 的扩展。</span><span class="sxs-lookup"><span data-stu-id="97e2d-106">The Announcement application is an Enterprise Voice feature that enables you to configure what happens to calls to unassigned extensions (extensions that are valid for your organization, but are not assigned to a person or a phone).</span></span> <span data-ttu-id="97e2d-107">例如，可以将对未分配号码的呼叫配置为播放消息或转接至其他目标，或者同时执行这两种操作。</span><span class="sxs-lookup"><span data-stu-id="97e2d-107">For example, you can configure calls to unassigned numbers to play a message, or to be transferred to a different destination, or both.</span></span>

<span data-ttu-id="97e2d-108">在部署企业语音时，"发布" 应用程序作为 "响应组应用程序" 的一项功能安装在前端服务器或标准版服务器上。</span><span class="sxs-lookup"><span data-stu-id="97e2d-108">The Announcement application is installed as a feature of Response Group application on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="97e2d-109">需要上载音频文件或配置文本到语音转换 (TTS)，并配置未分配号码表来配置通知。</span><span class="sxs-lookup"><span data-stu-id="97e2d-109">You need to configure Announcements by uploading your audio files or by configuring text-to-speech (TTS) and configuring the unassigned number table.</span></span>

<span data-ttu-id="97e2d-110">本部分将指导你完成 Lync Server 公告的配置。</span><span class="sxs-lookup"><span data-stu-id="97e2d-110">This section guides you through the configuration of Lync Server Announcements.</span></span> <span data-ttu-id="97e2d-111">它假设你已阅读与公告相关的规划部分，并使用企业语音部署企业版服务器或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="97e2d-111">It assumes that you have already read the planning sections related to Announcements and deployed an Enterprise Edition server or a Standard Edition server with Enterprise Voice.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="97e2d-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="97e2d-112">In This Section</span></span>

  - [<span data-ttu-id="97e2d-113">Lync Server 2013 中的通知配置先决条件和角色</span><span class="sxs-lookup"><span data-stu-id="97e2d-113">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>](lync-server-2013-announcement-configuration-prerequisites-and-roles.md)

  - [<span data-ttu-id="97e2d-114">Lync Server 2013 中的公告应用程序的部署过程</span><span class="sxs-lookup"><span data-stu-id="97e2d-114">Deployment process for the Announcement application in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-the-announcement-application.md)

  - [<span data-ttu-id="97e2d-115">在 Lync Server 2013 中创建公告</span><span class="sxs-lookup"><span data-stu-id="97e2d-115">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)

  - [<span data-ttu-id="97e2d-116">在 Lync Server 2013 中配置未分配号码表</span><span class="sxs-lookup"><span data-stu-id="97e2d-116">Configure the unassigned number table in Lync Server 2013</span></span>](lync-server-2013-configure-the-unassigned-number-table.md)

  - [<span data-ttu-id="97e2d-117"> (可选) 在 Lync Server 2013 中验证公告部署</span><span class="sxs-lookup"><span data-stu-id="97e2d-117">(Optional) Verify Announcement deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-announcement-deployment.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="97e2d-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="97e2d-118">See Also</span></span>


[<span data-ttu-id="97e2d-119">在 Lync Server 2013 中规划呼叫管理功能</span><span class="sxs-lookup"><span data-stu-id="97e2d-119">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="97e2d-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97e2d-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

