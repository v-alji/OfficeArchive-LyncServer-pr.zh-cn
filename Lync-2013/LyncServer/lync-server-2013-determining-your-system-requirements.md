---
title: Lync Server 2013：确定系统要求
description: Lync Server 2013：确定你的系统要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determining your system requirements
ms:assetid: 620e81e2-42df-4eda-8498-bd56a14aa0e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398438(v=OCS.15)
ms:contentKeyID: 48184286
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ceca8eabb234ae7fd483372ff5e611664ecc4fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429487"
---
# <a name="determining-your-system-requirements-for-lync-server-2013"></a><span data-ttu-id="008f4-103">确定 Lync Server 2013 的系统要求</span><span class="sxs-lookup"><span data-stu-id="008f4-103">Determining your system requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="008f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="008f4-104">

<span> </span></span></span>

<span data-ttu-id="008f4-105">_**主题上次修改时间：** 2014-01-02_</span><span class="sxs-lookup"><span data-stu-id="008f4-105">_**Topic Last Modified:** 2014-01-02_</span></span>

<span data-ttu-id="008f4-106">运行 Lync Server 的所有服务器必须满足一定的最低系统要求。</span><span class="sxs-lookup"><span data-stu-id="008f4-106">All servers running Lync Server must meet certain minimum system requirements.</span></span> <span data-ttu-id="008f4-107">Lync Server 的系统要求包括服务器硬件、要在每台服务器上安装的操作系统以及相关软件要求（如 Windows 更新和必须安装在服务器上的其他软件）。</span><span class="sxs-lookup"><span data-stu-id="008f4-107">System requirements for Lync Server include the server hardware, the operating system to be installed on each server, and related software requirements, such as the Windows updates and other software that must be installed on the servers.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="008f4-108">Lync Server 仅在64位版本中可用，这需要64位硬件和一个64位的 Windows Server 版本。</span><span class="sxs-lookup"><span data-stu-id="008f4-108">Lync Server is available only in a 64-bit edition, which requires 64-bit hardware and a 64-bit edition of Windows Server.</span></span> <span data-ttu-id="008f4-109">例外情况是 Microsoft Lync Server 2013、计划工具，可在32位版本中使用。</span><span class="sxs-lookup"><span data-stu-id="008f4-109">The exception is the Microsoft Lync Server 2013, Planning Tool, which is available in a 32-bit edition.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="008f4-110">有关 Active Directory 支持、支持的拓扑、服务器 collocation 和其他支持问题的详细信息，请参阅 <A href="lync-server-2013-supportability.md">Lync server 2013 的支持支持</A>。</span><span class="sxs-lookup"><span data-stu-id="008f4-110">For details about Active Directory support, supported topologies, server collocation, and other supportability issues, see <A href="lync-server-2013-supportability.md">Supportability for Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="008f4-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="008f4-111">In This Section</span></span>

  - [<span data-ttu-id="008f4-112">Lync Server 2013 的服务器硬件平台</span><span class="sxs-lookup"><span data-stu-id="008f4-112">Server hardware platforms for Lync Server 2013</span></span>](lync-server-2013-server-hardware-platforms.md)

  - [<span data-ttu-id="008f4-113">Lync Server 2013 中的服务器和工具操作系统支持</span><span class="sxs-lookup"><span data-stu-id="008f4-113">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)

  - [<span data-ttu-id="008f4-114">Lync Server 2013 中的数据库软件支持</span><span class="sxs-lookup"><span data-stu-id="008f4-114">Database software support in Lync Server 2013</span></span>](lync-server-2013-database-software-support.md)

  - [<span data-ttu-id="008f4-115">Lync Server 2013 的其他软件要求</span><span class="sxs-lookup"><span data-stu-id="008f4-115">Additional software requirements for Lync Server 2013</span></span>](lync-server-2013-additional-software-requirements.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="008f4-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="008f4-116">See Also</span></span>


[<span data-ttu-id="008f4-117">Lync Server 2013 中的客户端和设备硬件支持</span><span class="sxs-lookup"><span data-stu-id="008f4-117">Client and device hardware support in Lync Server 2013</span></span>](lync-server-2013-client-and-device-hardware-support.md)  
[<span data-ttu-id="008f4-118">Lync Server 2013 的可支持性</span><span class="sxs-lookup"><span data-stu-id="008f4-118">Supportability for Lync Server 2013</span></span>](lync-server-2013-supportability.md)  
  

<span data-ttu-id="008f4-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="008f4-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

