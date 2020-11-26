---
title: Lync Server 2013：准备 Active Directory 域服务
description: Lync Server 2013：准备 Active Directory 域服务。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing Active Directory Domain Services for Lync Server 2013
ms:assetid: 7e126464-5d29-4013-9c44-0ccc2fbdea0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398630(v=OCS.15)
ms:contentKeyID: 48184620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6ecfcffd55739bc6d1bf1b83a701a0fd515ec56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424217"
---
# <a name="preparing-active-directory-domain-services-for-lync-server-2013"></a><span data-ttu-id="fc1b0-103">为 Lync Server 2013 准备 Active Directory 域服务</span><span class="sxs-lookup"><span data-stu-id="fc1b0-103">Preparing Active Directory Domain Services for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc1b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc1b0-104">

<span> </span></span></span>

<span data-ttu-id="fc1b0-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="fc1b0-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="fc1b0-106">在部署和操作 Lync Server 2013 之前，必须通过扩展架构，然后创建和配置对象来准备 Active Directory 域服务。</span><span class="sxs-lookup"><span data-stu-id="fc1b0-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema and then creating and configuring objects.</span></span> <span data-ttu-id="fc1b0-107">架构扩展添加 Lync Server 所需的 Active Directory 类和属性。</span><span class="sxs-lookup"><span data-stu-id="fc1b0-107">The schema extensions add the Active Directory classes and attributes that are required by Lync Server.</span></span>

<span data-ttu-id="fc1b0-108">本部分中的主题介绍如何准备用于部署 Lync Server 的 AD DS 以及如何将设置和组织单位 (OU) 权限。</span><span class="sxs-lookup"><span data-stu-id="fc1b0-108">The topics in this section describe how to prepare AD DS for deploying Lync Server and how to assign setup and organizational unit (OU) permissions.</span></span> <span data-ttu-id="fc1b0-109">有关 Lync Server 所需的架构更改的详细信息，请参阅 [Lync server 2013 使用的 Active Directory 架构扩展、类和属性](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md)。</span><span class="sxs-lookup"><span data-stu-id="fc1b0-109">For details about the schema changes required for Lync Server, see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fc1b0-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="fc1b0-110">In This Section</span></span>

  - [<span data-ttu-id="fc1b0-111">Lync Server 2013 的 Active Directory 基础结构要求</span><span class="sxs-lookup"><span data-stu-id="fc1b0-111">Active Directory infrastructure requirements for Lync Server 2013</span></span>](lync-server-2013-active-directory-infrastructure-requirements.md)

  - [<span data-ttu-id="fc1b0-112">Lync Server 2013 中的 Active Directory 域服务准备概述</span><span class="sxs-lookup"><span data-stu-id="fc1b0-112">Overview of Active Directory Domain Services preparation in Lync Server 2013</span></span>](lync-server-2013-overview-of-active-directory-domain-services-preparation.md)

  - [<span data-ttu-id="fc1b0-113">在 Lync Server 2013 中准备 Active Directory 域服务</span><span class="sxs-lookup"><span data-stu-id="fc1b0-113">Preparing Active Directory Domain Services in Lync Server 2013</span></span>](lync-server-2013-preparing-active-directory-domain-services.md)

  - [<span data-ttu-id="fc1b0-114">在 Lync Server 2013 中准备锁定的 Active Directory 域服务</span><span class="sxs-lookup"><span data-stu-id="fc1b0-114">Preparing a locked-down Active Directory Domain Services in Lync Server 2013</span></span>](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md)

  - [<span data-ttu-id="fc1b0-115">在 Lync Server 2013 中授予权限</span><span class="sxs-lookup"><span data-stu-id="fc1b0-115">Granting permissions in Lync Server 2013</span></span>](lync-server-2013-granting-permissions.md)

<span data-ttu-id="fc1b0-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc1b0-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

