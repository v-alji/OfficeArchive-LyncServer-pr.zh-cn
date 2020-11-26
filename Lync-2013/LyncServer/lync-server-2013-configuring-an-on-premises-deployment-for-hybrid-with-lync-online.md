---
title: 使用 Lync Online 配置本地混合部署
description: 配置与 Lync Online 的混合部署内部部署。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring an on-premises deployment for hybrid with Lync Online
ms:assetid: c26addb0-2936-4eea-9071-3ab95825154b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205237(v=OCS.15)
ms:contentKeyID: 48185321
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 717900389db98fc14513a7d54bd37813757f98ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433386"
---
# <a name="configuring-an-on-premises-deployment-for-hybrid-with-lync-online"></a><span data-ttu-id="4fac2-103">使用 Lync Online 配置本地混合部署</span><span class="sxs-lookup"><span data-stu-id="4fac2-103">Configuring an on-premises deployment for hybrid with Lync Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4fac2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4fac2-104">

<span> </span></span></span>

<span data-ttu-id="4fac2-105">_**主题上次修改时间：** 2014-05-28_</span><span class="sxs-lookup"><span data-stu-id="4fac2-105">_**Topic Last Modified:** 2014-05-28_</span></span>

<span data-ttu-id="4fac2-106">混合部署是一种部署，其中某些用户在本地托管，某些用户处于联机状态，但所有用户共享相同的域，如 user@contoso.com。</span><span class="sxs-lookup"><span data-stu-id="4fac2-106">A hybrid deployment is a deployment in which some users are homed on-premises and some users are homed online, but all users share the same domain, such as user@contoso.com.</span></span> <span data-ttu-id="4fac2-107">本部分将指导你部署混合部署所需的应用程序，然后配置你的部署以启用它。</span><span class="sxs-lookup"><span data-stu-id="4fac2-107">This section guides you through deploying the applications required for a hybrid deployment, and then configuring your deployment to enable it.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4fac2-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="4fac2-108">In This Section</span></span>

  - [<span data-ttu-id="4fac2-109">Lync Server 2013 混合环境概述</span><span class="sxs-lookup"><span data-stu-id="4fac2-109">Overview of the Lync Server 2013 hybrid environment</span></span>](lync-server-2013-overview-of-the-lync-server-hybrid-environment.md)

  - [<span data-ttu-id="4fac2-110">准备和部署 Lync Server 2013 混合环境的步骤</span><span class="sxs-lookup"><span data-stu-id="4fac2-110">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>](lync-server-2013-steps-to-prepare-and-deploy-lync-server-hybrid-environment.md)

  - [<span data-ttu-id="4fac2-111">配置 Lync Server 2013 与 Lync Online 的联合</span><span class="sxs-lookup"><span data-stu-id="4fac2-111">Configure federation of Lync Server 2013 with Lync Online</span></span>](lync-server-2013-configure-federation-with-lync-online.md)

  - [<span data-ttu-id="4fac2-112">在 Lync Server 2013 中配置音频会议提供商的联盟</span><span class="sxs-lookup"><span data-stu-id="4fac2-112">Configure federation for an audio conferencing provider in Lync Server 2013</span></span>](lync-server-2013-configure-federation-for-an-audio-conferencing-provider.md)

  - [<span data-ttu-id="4fac2-113">在 Lync Server 2013 中将用户移动到 Lync Online</span><span class="sxs-lookup"><span data-stu-id="4fac2-113">Move users to Lync Online in Lync Server 2013</span></span>](lync-server-2013-move-users-to-lync-online.md)

  - [<span data-ttu-id="4fac2-114">管理混合 Lync Server 2013 部署中的用户</span><span class="sxs-lookup"><span data-stu-id="4fac2-114">Administering users in a hybrid Lync Server 2013 deployment</span></span>](lync-server-2013-administering-users-in-a-hybrid-deployment.md)

<span data-ttu-id="4fac2-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4fac2-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

