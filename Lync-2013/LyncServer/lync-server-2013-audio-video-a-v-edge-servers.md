---
title: Lync Server 2013：音频/视频 (A/V) 边缘服务器
description: Lync Server 2013：音频/视频 (A/V) 边缘服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Audio/Video (A/V) Edge Servers
ms:assetid: b0cc538b-77eb-47fb-be82-5ab0631c6219
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721852(v=OCS.15)
ms:contentKeyID: 49733785
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d5aefd4516540485b84ba0eb80f1a809d89eba0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438237"
---
# <a name="audiovideo-av-edge-servers-in-lync-server-2013"></a><span data-ttu-id="602c8-103">Lync Server 2013 中的音频/视频 (A/V) 边缘服务器</span><span class="sxs-lookup"><span data-stu-id="602c8-103">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="602c8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="602c8-104">

<span> </span></span></span>

<span data-ttu-id="602c8-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="602c8-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="602c8-106">A/V 边缘服务为登录到你的组织网络的用户提供了一种方式 () 与外部用户共享音频和视频 (未登录到你的组织网络) 的用户。</span><span class="sxs-lookup"><span data-stu-id="602c8-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="602c8-107">除了音频和视频，A/V 边缘服务还提供有关桌面共享和文件传输等方面的支持。</span><span class="sxs-lookup"><span data-stu-id="602c8-107">In addition to audio and video, the A/V Edge service also provides support for such things desktop sharing and file transfer.</span></span>

<span data-ttu-id="602c8-108">A/V 边缘服务主要通过使用 A/V 边缘配置进行管理;使用这些设置，你可以管理每个端口和每个用户分配的最大带宽量，并指定在必须续订该令牌之前可以使用身份验证令牌的时间长度。</span><span class="sxs-lookup"><span data-stu-id="602c8-108">The A/V Edge service is primarily managed by using A/V Edge configuration; these settings enable you to manage the maximum amount of bandwidth to be allocated per port and per user, and to specify the length of time that an authentication token can be used before that token must be renewed.</span></span> <span data-ttu-id="602c8-109">A/V 边缘配置设置可应用于网站或单个 A/V 边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="602c8-109">A/V Edge configuration settings can be applied to sites or to individual A/V Edge servers.</span></span> <span data-ttu-id="602c8-110">确定哪个设置集合优先时，请使用以下指南：</span><span class="sxs-lookup"><span data-stu-id="602c8-110">When determining which collection of settings will take priority, use the following guide:</span></span>

  - <span data-ttu-id="602c8-111">在服务作用域上配置的设置 (也就是说，在单个服务器上) 优先处理所有内容。</span><span class="sxs-lookup"><span data-stu-id="602c8-111">Settings configured at the service scope (that is, on an individual server) take priority over everything.</span></span>

  - <span data-ttu-id="602c8-112">在网站范围内配置的设置优先于在全局范围内配置的设置。</span><span class="sxs-lookup"><span data-stu-id="602c8-112">Settings configured at the site scope take priority over settings configured at the global scope.</span></span> <span data-ttu-id="602c8-113">但是，服务范围设置还将取代网站范围的设置。</span><span class="sxs-lookup"><span data-stu-id="602c8-113">However, service scope settings will also supersede site-scope settings.</span></span>

  - <span data-ttu-id="602c8-114">只有在单个服务器上没有配置任何服务设置且该服务器所在的网站没有网站设置的情况下，才会使用全局范围内的设置。</span><span class="sxs-lookup"><span data-stu-id="602c8-114">Settings at the global scope will be used only if there are no service settings configured on the individual server and if there are no site settings for the site where that server is located.</span></span>

<span data-ttu-id="602c8-115">只有使用 Lync Server PowerShell 和 CsAVEdgeConfiguration cmdlet 才能管理 A/V 边缘服务。</span><span class="sxs-lookup"><span data-stu-id="602c8-115">The A/V Edge service can only be managed by using Lync Server PowerShell and the CsAVEdgeConfiguration cmdlets.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="602c8-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="602c8-116">In This Section</span></span>

  - [<span data-ttu-id="602c8-117">返回 Lync Server 2013 中的 A/V 边缘服务器配置信息</span><span class="sxs-lookup"><span data-stu-id="602c8-117">Return A/V Edge Server configuration information in Lync Server 2013</span></span>](lync-server-2013-return-a-v-edge-server-configuration-information.md)

  - [<span data-ttu-id="602c8-118">在 Lync Server 2013 中创建或修改 A/V 边缘服务器配置设置的集合</span><span class="sxs-lookup"><span data-stu-id="602c8-118">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)

  - [<span data-ttu-id="602c8-119">在 Lync Server 2013 中删除 A/V 边缘服务器配置设置的现有集合</span><span class="sxs-lookup"><span data-stu-id="602c8-119">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)

<span data-ttu-id="602c8-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="602c8-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

