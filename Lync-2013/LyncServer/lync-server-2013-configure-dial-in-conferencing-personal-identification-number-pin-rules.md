---
title: 配置拨入式会议个人识别码 (引脚) 规则
description: 将电话拨入式会议个人识别号配置 (固定) 规则。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial-in conferencing personal identification number (PIN) rules
ms:assetid: 27b79fb1-e2dc-4f71-bc82-b6eb61be2b16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520967(v=OCS.15)
ms:contentKeyID: 48183668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 799092ba57e9a85cd196840fc81c1f46b96e9900
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392406"
---
# <a name="configure-dial-in-conferencing-personal-identification-number-pin-rules-in-lync-server-2013"></a><span data-ttu-id="13bf1-103">在 Lync Server 2013 中配置电话拨入式会议个人识别号 (固定) 规则</span><span class="sxs-lookup"><span data-stu-id="13bf1-103">Configure dial-in conferencing personal identification number (PIN) rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13bf1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13bf1-104">

<span> </span></span></span>

<span data-ttu-id="13bf1-105">_**主题上次修改时间：** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="13bf1-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="13bf1-106">具有 Active Directory 域服务 (组织中的 AD DS) 凭据的 Lync Server 2013 用户可以使用个人识别码 (PIN) 将电话拨入式会议作为已验证用户加入电话拨入式会议。</span><span class="sxs-lookup"><span data-stu-id="13bf1-106">Lync Server 2013 users who have Active Directory Domain Services (AD DS) credentials in your organization can join dial-in conferences as authenticated users by using a personal identification number (PIN).</span></span> <span data-ttu-id="13bf1-107">PIN 策略定义电话拨入式会议 PIN 工作方式的规则。</span><span class="sxs-lookup"><span data-stu-id="13bf1-107">PIN policy defines the rules for how dial-in conferencing PINs work.</span></span>

<span data-ttu-id="13bf1-108">如果要将特定策略应用于某个站点或某个用户组，可以创建新的 PIN 策略。</span><span class="sxs-lookup"><span data-stu-id="13bf1-108">You can create a new PIN policy if you want a specific policy to apply to a site or to a certain group of users.</span></span> <span data-ttu-id="13bf1-109">如果要在整个组织中使用相同的 PIN 策略，则可以使用全局 PIN 策略并根据需要对其进行修改。</span><span class="sxs-lookup"><span data-stu-id="13bf1-109">If you want to use the same PIN policy for your entire organization, you can use the global PIN policy and modify it as needed.</span></span> <span data-ttu-id="13bf1-110">PIN 策略既可以应用于少数用户，也可以应用于众多用户。</span><span class="sxs-lookup"><span data-stu-id="13bf1-110">PIN policies apply to users from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="13bf1-111">如果为用户分配用户级别的 PIN 策略，则优先应用这些设置。</span><span class="sxs-lookup"><span data-stu-id="13bf1-111">If you assign a user-level PIN policy to a user, those settings take precedence.</span></span> <span data-ttu-id="13bf1-112">如果没有分配用户策略，则将应用站点级别的 PIN 策略（如果存在）。</span><span class="sxs-lookup"><span data-stu-id="13bf1-112">If you do not assign a user policy, the site-level PIN policy applies, if it exists.</span></span> <span data-ttu-id="13bf1-113">如果未应用用户策略或站点策略，则全局 PIN 策略会提供默认设置。</span><span class="sxs-lookup"><span data-stu-id="13bf1-113">If no user or site policies apply, global PIN policy provides the default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="13bf1-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="13bf1-114">In This Section</span></span>

  - [<span data-ttu-id="13bf1-115">在 Lync Server 2013 中修改默认电话拨入式会议 PIN 设置</span><span class="sxs-lookup"><span data-stu-id="13bf1-115">Modify the default dial-in conferencing PIN settings in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-dial-in-conferencing-pin-settings.md)

  - [<span data-ttu-id="13bf1-116">在 Lync Server 2013 中创建或修改站点或用户组的电话拨入式会议 PIN 设置</span><span class="sxs-lookup"><span data-stu-id="13bf1-116">Create or modify dial-in conferencing PIN settings in Lync Server 2013 for a site or group of users</span></span>](lync-server-2013-create-or-modify-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

  - [<span data-ttu-id="13bf1-117">在 Lync Server 2013 中删除一个网站或一组用户的电话拨入式会议 PIN 设置</span><span class="sxs-lookup"><span data-stu-id="13bf1-117">Delete dial-in conferencing PIN settings for a site or group of users in Lync Server 2013</span></span>](lync-server-2013-delete-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

<span data-ttu-id="13bf1-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13bf1-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

