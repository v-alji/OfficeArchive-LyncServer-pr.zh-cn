---
title: Lync Server 2013：Lync Server 使用的 Active Directory 架构扩展、类和属性
description: Lync Server 2013： Active Directory 架构扩展、类和 Lync Server 使用的属性。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory schema extensions, classes, and attributes used by Lync Server 2013
ms:assetid: 579bfa5a-9443-46dd-9a8e-07d00ba2824d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398379(v=OCS.15)
ms:contentKeyID: 48184188
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: beac778d3315573f4d5cc6cb9c827a3a2fce9d0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391773"
---
# <a name="active-directory-schema-extensions-classes-and-attributes-used-by-lync-server-2013"></a><span data-ttu-id="c9598-103">Lync Server 2013 使用的 Active Directory 架构扩展、类和属性</span><span class="sxs-lookup"><span data-stu-id="c9598-103">Active Directory schema extensions, classes, and attributes used by Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9598-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9598-104">

<span> </span></span></span>

<span data-ttu-id="c9598-105">_**主题上次修改时间：** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="c9598-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="c9598-106">本参考部分包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="c9598-106">This reference section includes the following information:</span></span>

  - <span data-ttu-id="c9598-107">Lync Server 2013 的新的或已更改的 Active Directory 架构扩展</span><span class="sxs-lookup"><span data-stu-id="c9598-107">Active Directory schema extensions that are new or changed for Lync Server 2013</span></span>
    
    <span data-ttu-id="c9598-108">Active Directory 架构包含可在 Active Directory 林中创建的每个对象类的正式定义。</span><span class="sxs-lookup"><span data-stu-id="c9598-108">The Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="c9598-109">该架构还包含可存在于 Active Directory 对象上的每个属性的正式定义。</span><span class="sxs-lookup"><span data-stu-id="c9598-109">The schema also contains formal definitions of every attribute that can exist on an Active Directory object.</span></span> <span data-ttu-id="c9598-110">Active Directory 全局编录包含林的所有对象的副本，以及每个对象的属性子集。</span><span class="sxs-lookup"><span data-stu-id="c9598-110">The Active Directory global catalog contains replicas of all the objects for the forest, along with a subset of the attributes for each object.</span></span> <span data-ttu-id="c9598-111">本部分介绍 Lync Server 2013 中新增或更改的类和属性。</span><span class="sxs-lookup"><span data-stu-id="c9598-111">This section describes the classes and attributes that are new or changed in Lync Server 2013.</span></span>

  - <span data-ttu-id="c9598-112">Lync Server 使用的所有类，以及每个类的说明</span><span class="sxs-lookup"><span data-stu-id="c9598-112">All the classes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="c9598-113">Lync Server 使用的所有属性，以及每个属性的说明</span><span class="sxs-lookup"><span data-stu-id="c9598-113">All the attributes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="c9598-114">Lync Server 使用的类列表，每个类都可能包含的属性</span><span class="sxs-lookup"><span data-stu-id="c9598-114">A list of the classes used by Lync Server, with the attributes each may contain</span></span>

  - <span data-ttu-id="c9598-115">全局设置和对象，以及林准备期间创建的通用服务和管理组</span><span class="sxs-lookup"><span data-stu-id="c9598-115">Global settings and objects, in addition to the universal service and administration groups that are created during forest preparation</span></span>

  - <span data-ttu-id="c9598-116">在域准备期间在域根和内置容器上创建的 (Ace) 的访问控制条目</span><span class="sxs-lookup"><span data-stu-id="c9598-116">Access control entries (ACEs) that are created on the domain root and built-in containers during domain preparation</span></span>

  - <span data-ttu-id="c9598-117">通过授予 CsSetupPermission cmdlet) 在 Active Directory 组织单位 (OU 上进行的更改 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c9598-117">Changes that are made on an Active Directory organizational unit (OU) by the Grant\_CsSetupPermission cmdlet.</span></span>

  - <span data-ttu-id="c9598-118">通过授予 CsOUPermission cmdlet 在 Active Directory OU 上进行的更改 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c9598-118">Changes that are made on an Active Directory OU by the Grant\_CsOUPermission cmdlet.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c9598-119">本节内容</span><span class="sxs-lookup"><span data-stu-id="c9598-119">In This Section</span></span>

  - [<span data-ttu-id="c9598-120">Lync Server 2013 中的架构更改</span><span class="sxs-lookup"><span data-stu-id="c9598-120">Schema changes in Lync Server 2013</span></span>](lync-server-2013-schema-changes-in-lync-server-2013.md)

  - [<span data-ttu-id="c9598-121">Lync Server 2013 中的架构类和说明</span><span class="sxs-lookup"><span data-stu-id="c9598-121">Schema classes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-classes-and-descriptions.md)

  - [<span data-ttu-id="c9598-122">Lync Server 2013 中的架构属性和说明</span><span class="sxs-lookup"><span data-stu-id="c9598-122">Schema attributes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-and-descriptions.md)

  - [<span data-ttu-id="c9598-123">Lync Server 2013 中按类分类的架构属性</span><span class="sxs-lookup"><span data-stu-id="c9598-123">Schema attributes by class in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-by-class.md)

  - [<span data-ttu-id="c9598-124">Lync Server 2013 中的林准备所做的更改</span><span class="sxs-lookup"><span data-stu-id="c9598-124">Changes made by forest preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-forest-preparation.md)

  - [<span data-ttu-id="c9598-125">Lync Server 2013 中的域准备进行的更改</span><span class="sxs-lookup"><span data-stu-id="c9598-125">Changes made by domain preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-domain-preparation.md)

  - [<span data-ttu-id="c9598-126">Lync Server 2013 中 Grant-CsSetupPermission 所做的更改</span><span class="sxs-lookup"><span data-stu-id="c9598-126">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission)

  - [<span data-ttu-id="c9598-127">Lync Server 2013 中 Grant-CsOUPermission 所做的更改</span><span class="sxs-lookup"><span data-stu-id="c9598-127">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission)

<span data-ttu-id="c9598-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9598-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

