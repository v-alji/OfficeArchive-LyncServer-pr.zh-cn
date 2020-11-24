---
title: Lync Server 2013：管理未分配号码的呼叫
description: Lync Server 2013：管理对未分配号码的呼叫。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing calls to unassigned numbers
ms:assetid: a45a7546-5ee6-4c1e-ab13-20a71a058f80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688167(v=OCS.15)
ms:contentKeyID: 49733772
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a91c1ec30ea1e942fa3ea27fbcd369572884a52a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392142"
---
# <a name="managing-calls-to-unassigned-numbers-in-lync-server-2013"></a><span data-ttu-id="cf6f8-103">管理 Lync Server 2013 中未分配号码的呼叫</span><span class="sxs-lookup"><span data-stu-id="cf6f8-103">Managing calls to unassigned numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf6f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf6f8-104">

<span> </span></span></span>

<span data-ttu-id="cf6f8-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="cf6f8-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="cf6f8-106">Lync Server 让你可以配置当拨出的号码对你的组织有效，但未分配给用户或电话时对传入电话呼叫的处理。</span><span class="sxs-lookup"><span data-stu-id="cf6f8-106">Lync Server lets you configure the handling of incoming phone calls when the dialed number is valid for your organization, but is not assigned to a user or phone.</span></span> <span data-ttu-id="cf6f8-107">你可以使用公告应用程序将这些呼叫转移到预先确定的目的地 (电话号码、SIP URI 或语音邮件) 或播放音频公告。</span><span class="sxs-lookup"><span data-stu-id="cf6f8-107">You can use the Announcement application to transfer these calls to a predetermined destination (phone number, SIP URI, or voice mail), or play an audio announcement, or both.</span></span> <span data-ttu-id="cf6f8-108">您还可以将这些呼叫转移到 Exchange UM 自动助理电话号码。</span><span class="sxs-lookup"><span data-stu-id="cf6f8-108">You can also transfer these calls to an Exchange UM Auto Attendant phone number.</span></span> <span data-ttu-id="cf6f8-109">通过以下方法之一处理对未分配号码的调用可帮助你避免呼叫者 misdials 的情况，然后听到占线音，或者 SIP 客户端收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="cf6f8-109">Handling calls to unassigned numbers in one of these ways helps you avoid the situations in which a caller misdials and then hears a busy tone, or the SIP client receives an error message.</span></span>

<span data-ttu-id="cf6f8-110">本部分介绍如何管理未分配的号码范围以处理未分配电话号码的呼叫。</span><span class="sxs-lookup"><span data-stu-id="cf6f8-110">This section describes how to manage unassigned number ranges to handle calls to unassigned phone numbers.</span></span> <span data-ttu-id="cf6f8-111">本部分还介绍了如何在中断期间需要此功能的情况下管理灾难恢复期间的公告。</span><span class="sxs-lookup"><span data-stu-id="cf6f8-111">The section also describes how to manage Announcements during disaster recovery if you want this functionality during an outage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cf6f8-112">在中断期间使用未分配的号码处理是可选的。</span><span class="sxs-lookup"><span data-stu-id="cf6f8-112">Using unassigned number handling during an outage is optional.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cf6f8-113">本节内容</span><span class="sxs-lookup"><span data-stu-id="cf6f8-113">In This Section</span></span>

  - [<span data-ttu-id="cf6f8-114">在 Lync Server 2013 中创建公告</span><span class="sxs-lookup"><span data-stu-id="cf6f8-114">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)

  - [<span data-ttu-id="cf6f8-115">在 Lync Server 2013 中配置未分配的电话号码</span><span class="sxs-lookup"><span data-stu-id="cf6f8-115">Configure unassigned phone numbers in Lync Server 2013</span></span>](lync-server-2013-configure-unassigned-phone-numbers.md)

  - [<span data-ttu-id="cf6f8-116">在 Lync Server 2013 中灾难恢复期间管理通知</span><span class="sxs-lookup"><span data-stu-id="cf6f8-116">Manage announcements during disaster recovery in Lync Server 2013</span></span>](lync-server-2013-manage-announcements-during-disaster-recovery.md)

<span data-ttu-id="cf6f8-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf6f8-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

