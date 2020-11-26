---
title: 迁移现有会议和会议内容
description: 迁移现有会议和会议内容。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443802"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a><span data-ttu-id="6f1b7-103">迁移现有会议和会议内容</span><span class="sxs-lookup"><span data-stu-id="6f1b7-103">Migrate existing meetings and meeting content</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f1b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f1b7-104">

<span> </span></span></span>

<span data-ttu-id="6f1b7-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="6f1b7-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="6f1b7-106">当用户帐户从 Lync Server 2010 移动到 Lync Server 2013 服务器时，以下信息将与该用户帐户一起移动：</span><span class="sxs-lookup"><span data-stu-id="6f1b7-106">When a user account is moved from Lync Server 2010 to a Lync Server 2013 server, the following information is moved with that user account:</span></span>

  - <span data-ttu-id="6f1b7-107">**已由用户安排的会议**。</span><span class="sxs-lookup"><span data-stu-id="6f1b7-107">**Meetings already scheduled by the user**.</span></span> <span data-ttu-id="6f1b7-108">这包括移动会议目录和会议数据。</span><span class="sxs-lookup"><span data-stu-id="6f1b7-108">This includes moving the conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="6f1b7-109">**用户的个人识别码 (引脚)**。</span><span class="sxs-lookup"><span data-stu-id="6f1b7-109">**User’s personal identification number (PIN)**.</span></span> <span data-ttu-id="6f1b7-110">用户的当前 PIN 将继续工作，直到过期或用户请求新的 PIN。</span><span class="sxs-lookup"><span data-stu-id="6f1b7-110">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="6f1b7-111">以下用户帐户信息不会移动到新服务器。</span><span class="sxs-lookup"><span data-stu-id="6f1b7-111">The following user account information does not move to the new server.</span></span>

  - <span data-ttu-id="6f1b7-112">**会议内容**。</span><span class="sxs-lookup"><span data-stu-id="6f1b7-112">**Meeting content**.</span></span> <span data-ttu-id="6f1b7-113">为了移动在会议期间共享的内容（例如 PowerPoint、白板、附件或投票数据），请使用 **-MoveConferenceData** 参数作为 **move-csuser** cmdlet 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6f1b7-113">In order to move the content shared during a meeting, for example PowerPoint, Whiteboard, attachments or poll data, use the **-MoveConferenceData** parameter as part of the **Move-CsUser** cmdlet.</span></span>

<span data-ttu-id="6f1b7-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f1b7-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

