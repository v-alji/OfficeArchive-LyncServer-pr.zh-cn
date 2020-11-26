---
title: Lync Server 2013：会议策略
description: Lync Server 2013：会议策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing policies
ms:assetid: 8f92eb7c-ee66-4df6-a726-4bff93b122cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688133(v=OCS.15)
ms:contentKeyID: 49733732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f117cfb077fc24c3e728e208d8bef78cd3284ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434310"
---
# <a name="conferencing-policies-in-lync-server-2013"></a><span data-ttu-id="71a4f-103">Lync Server 2013 中的会议策略</span><span class="sxs-lookup"><span data-stu-id="71a4f-103">Conferencing policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71a4f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71a4f-104">

<span> </span></span></span>

<span data-ttu-id="71a4f-105">_**主题上次修改时间：** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="71a4f-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="71a4f-106">会议策略定义用户在会议中可用的功能和功能 (也称为会议) 。</span><span class="sxs-lookup"><span data-stu-id="71a4f-106">Conferencing policy defines the features and capabilities that users have available during a conference (also known as a meeting).</span></span> <span data-ttu-id="71a4f-107">会议策略设置包含各种安排和参与选项，包括从会议能否包括 IP 音频和视频，到可参与会议的最大人数。</span><span class="sxs-lookup"><span data-stu-id="71a4f-107">Conferencing policy settings encompass a wide variety of scheduling and participation options, ranging from whether a meeting can include IP audio and video to the maximum number of people who can attend.</span></span> <span data-ttu-id="71a4f-108">管理员可以使用会议策略来管理会议的安全、带宽和法律方面。</span><span class="sxs-lookup"><span data-stu-id="71a4f-108">Administrators can use conferencing policy to manage security, bandwidth, and legal aspects of meetings.</span></span>

<span data-ttu-id="71a4f-109">可以在三个级别定义会议策略：全局作用域、站点作用域和用户作用域。</span><span class="sxs-lookup"><span data-stu-id="71a4f-109">You can define conferencing policy on three levels: global scope, site scope, and user scope.</span></span> <span data-ttu-id="71a4f-110">可以为不同范围的作用域中的特定用户应用设置。</span><span class="sxs-lookup"><span data-stu-id="71a4f-110">Settings apply to a specific user from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="71a4f-111">如果向用户分配用户策略，这些设置优先。</span><span class="sxs-lookup"><span data-stu-id="71a4f-111">If you assign a user policy to a user, those settings take precedence.</span></span> <span data-ttu-id="71a4f-112">如果未分配用户策略，则应用站点设置。</span><span class="sxs-lookup"><span data-stu-id="71a4f-112">If you do not assign a user policy, site settings apply.</span></span> <span data-ttu-id="71a4f-113">如果未应用用户策略或站点策略，则全局策略会提供默认设置。</span><span class="sxs-lookup"><span data-stu-id="71a4f-113">If no user or site policies apply, global policy provides the default settings.</span></span>

<span data-ttu-id="71a4f-114">默认情况下，全局策略已存在，因此不能创建新的全局策略。</span><span class="sxs-lookup"><span data-stu-id="71a4f-114">A global policy exists by default, so you cannot create a new global policy.</span></span> <span data-ttu-id="71a4f-115">也不能删除现有全局策略，但可以更改现有全局策略以自定义默认设置。</span><span class="sxs-lookup"><span data-stu-id="71a4f-115">You also cannot delete the existing global policy, but you can change the existing global policy to customize your default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="71a4f-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="71a4f-116">In This Section</span></span>

  - [<span data-ttu-id="71a4f-117">在 Lync Server 2013 中查看会议策略信息</span><span class="sxs-lookup"><span data-stu-id="71a4f-117">View conferencing policy information in Lync Server 2013</span></span>](lync-server-2013-view-conferencing-policy-information.md)

  - [<span data-ttu-id="71a4f-118">在 Lync Server 2013 中创建或修改会议策略</span><span class="sxs-lookup"><span data-stu-id="71a4f-118">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)

  - [<span data-ttu-id="71a4f-119">在 Lync Server 2013 中删除现有会议策略</span><span class="sxs-lookup"><span data-stu-id="71a4f-119">Delete an existing conferencing policy in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-conferencing-policy.md)

  - [<span data-ttu-id="71a4f-120">Lync Server 2013 的会议策略设置参考</span><span class="sxs-lookup"><span data-stu-id="71a4f-120">Conferencing policy settings reference for Lync Server 2013</span></span>](lync-server-2013-conferencing-policy-settings-reference.md)

<span data-ttu-id="71a4f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71a4f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

