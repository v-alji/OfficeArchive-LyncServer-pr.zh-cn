---
title: Lync Server 2013：准备林
description: Lync Server 2013：准备林。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the forest
ms:assetid: 3d188fcb-c64e-46cf-a3a7-9e3ebefed7fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425898(v=OCS.15)
ms:contentKeyID: 48183926
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 275d861ebfe7e0350e7baf120b6e6f2bae6a26ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424105"
---
# <a name="preparing-the-forest-for-lync-server-2013"></a><span data-ttu-id="54332-103">为 Lync Server 2013 准备林</span><span class="sxs-lookup"><span data-stu-id="54332-103">Preparing the forest for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54332-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54332-104">

<span> </span></span></span>

<span data-ttu-id="54332-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="54332-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="54332-106">林准备创建用于 Lync Server 2013 的 Active Directory 全局设置和对象以及 Active Directory 通用组，并在 Active Directory 对象上授予合适的访问权限。</span><span class="sxs-lookup"><span data-stu-id="54332-106">Forest preparation creates Active Directory global settings and objects and Active Directory universal groups for use by Lync Server 2013, and grants suitable access permissions on the Active Directory objects.</span></span> <span data-ttu-id="54332-107">有关通用组和由林准备创建的全局设置和对象的说明，请参阅 [Lync Server 2013 中的林准备所做的更改](lync-server-2013-changes-made-by-forest-preparation.md)。</span><span class="sxs-lookup"><span data-stu-id="54332-107">For a description of the universal groups and the global settings and objects created by forest preparation, see [Changes made by forest preparation in Lync Server 2013](lync-server-2013-changes-made-by-forest-preparation.md).</span></span>

<span data-ttu-id="54332-108">林准备还会创建包含由 Lync Server 2013 使用的属性集和显示说明符的对象，并将它们存储在配置容器中。</span><span class="sxs-lookup"><span data-stu-id="54332-108">Forest preparation also creates objects that contain property sets and display specifiers that are used by Lync Server 2013, and stores them in the Configuration container.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="54332-109">在执行林准备过程之前，请确保架构准备更改已复制到所有域控制器。</span><span class="sxs-lookup"><span data-stu-id="54332-109">Make sure that schema preparation changes have replicated to all domain controllers before performing the forest preparation procedure.</span></span> <span data-ttu-id="54332-110">如果复制未完成，则会出现错误。</span><span class="sxs-lookup"><span data-stu-id="54332-110">If replication is not completed, an error occurs.</span></span>



</div>

<span data-ttu-id="54332-111">如果你正在执行新的 Lync 服务器部署，则必须将全局设置存储在配置容器中。</span><span class="sxs-lookup"><span data-stu-id="54332-111">If you are performing a new Lync Server deployment, you must store global settings in the Configuration container.</span></span> <span data-ttu-id="54332-112">如果从早期版本升级，但仍将全局设置存储在系统容器中，则可以继续使用系统容器。</span><span class="sxs-lookup"><span data-stu-id="54332-112">If you are upgrading from an earlier version and you still store global settings in the System container, you can continue to use the System container.</span></span>

<span data-ttu-id="54332-113">你必须是林根域的企业管理员或域管理员组的成员才能执行此过程。</span><span class="sxs-lookup"><span data-stu-id="54332-113">You must be a member of the Enterprise Admins or Domain Admins group for the forest root domain to perform this procedure.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="54332-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="54332-114">In This Section</span></span>

  - [<span data-ttu-id="54332-115">为 Lync Server 2013 运行林准备</span><span class="sxs-lookup"><span data-stu-id="54332-115">Running forest preparation for Lync Server 2013</span></span>](lync-server-2013-running-forest-preparation.md)

  - [<span data-ttu-id="54332-116">针对 Lync Server 2013 使用 Cmdlet 反向执行林准备</span><span class="sxs-lookup"><span data-stu-id="54332-116">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-forest-preparation.md)

<span data-ttu-id="54332-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54332-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

