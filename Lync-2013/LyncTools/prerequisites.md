---
title: 先决条件
description: 项.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prerequisites
ms:assetid: 48016bea-be3b-4ba5-8df8-d8ad4d9243d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945592(v=OCS.15)
ms:contentKeyID: 51541417
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 936e52961539ed57fe1b610d42fb1c9cf35589b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446402"
---
# <a name="prerequisites"></a><span data-ttu-id="7a2b1-103">先决条件</span><span class="sxs-lookup"><span data-stu-id="7a2b1-103">Prerequisites</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a2b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a2b1-104">

<span> </span></span></span>

<span data-ttu-id="7a2b1-105">_**主题上次修改时间：** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="7a2b1-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="7a2b1-106">需要运行 Lync Server 2013 应力和性能工具的各种硬件、软件和系统配置要求。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-106">There are various hardware, software, and system configuration requirements that you’ll need to run the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="client-hardware-requirements"></a><span data-ttu-id="7a2b1-107">客户端硬件要求</span><span class="sxs-lookup"><span data-stu-id="7a2b1-107">Client Hardware Requirements</span></span>

<span data-ttu-id="7a2b1-108">若要在 Lync Server 2013 部署上运行 Lync Server 2013 应力和性能工具，对于要模拟其负载的每个4500用户，您至少需要一台专用计算机，满足以下最低硬件要求：</span><span class="sxs-lookup"><span data-stu-id="7a2b1-108">To run the Lync Server 2013 Stress and Performance Tool on your Lync Server 2013 deployment, for every 4,500 users whose load you want to simulate, you’ll need at least one dedicated computer that meets the following minimum hardware requirements:</span></span>

  - <span data-ttu-id="7a2b1-109">1 GB 的网络适配器</span><span class="sxs-lookup"><span data-stu-id="7a2b1-109">1 gigabit network adapter</span></span>

  - <span data-ttu-id="7a2b1-110">8 GB ram</span><span class="sxs-lookup"><span data-stu-id="7a2b1-110">8-GB ram</span></span>

  - <span data-ttu-id="7a2b1-111">2个双核中央处理单元 (Cpu) </span><span class="sxs-lookup"><span data-stu-id="7a2b1-111">2 dual-core central processing units (CPUs)</span></span>

</div>

<div>

## <a name="client-software-requirements"></a><span data-ttu-id="7a2b1-112">客户端软件要求</span><span class="sxs-lookup"><span data-stu-id="7a2b1-112">Client Software Requirements</span></span>

<span data-ttu-id="7a2b1-113">若要在 Lync Server 2013 部署上运行 Lync Server 2013 应力和性能工具，受支持的操作系统包括：</span><span class="sxs-lookup"><span data-stu-id="7a2b1-113">To run the Lync Server 2013 Stress and Performance Tool on your Lync Server 2013 deployment, the supported operating systems are:</span></span>

  - <span data-ttu-id="7a2b1-114">Windows Server 2012 操作系统</span><span class="sxs-lookup"><span data-stu-id="7a2b1-114">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="7a2b1-115">Windows Server 2008 操作系统 (64 位版) </span><span class="sxs-lookup"><span data-stu-id="7a2b1-115">Windows Server 2008 operating system (64-bit edition)</span></span>

<span data-ttu-id="7a2b1-116">客户端计算机必须满足以下软件要求：</span><span class="sxs-lookup"><span data-stu-id="7a2b1-116">Your client computer must meet the following software requirements:</span></span>

  - <span data-ttu-id="7a2b1-117">必须安装 [Microsoft .Net Framework 4.5](https://go.microsoft.com/fwlink/?linkid=143212) 运行时。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-117">You must have the [Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?linkid=143212) runtime installed.</span></span>

  - <span data-ttu-id="7a2b1-118">在 Windows Server 2008/Windows Server 2012 上，必须启用 "桌面体验" 功能。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-118">On Windows Server 2008/Windows Server 2012, the Desktop Experience feature must be enabled.</span></span>

  - <span data-ttu-id="7a2b1-119">必须安装有 [Microsoft Visual c + + 2012 可再发行程序包](https://go.microsoft.com/fwlink/?linkid=143216) (x64) 。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-119">You must have the [Microsoft Visual C++ 2012 redistributable package](https://go.microsoft.com/fwlink/?linkid=143216) (x64) installed.</span></span>

  - <span data-ttu-id="7a2b1-120">已完全配置的 Lync Server 2013 部署。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-120">A fully configured Lync Server 2013 deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7a2b1-121">Microsoft 统一通信托管 API (UCMA) 4.0 库包含在安装程序包中，因此 UCMA 不是必需的，不应在客户端计算机上安装。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-121">Microsoft Unified Communications Managed API (UCMA) 4.0 libraries are included in the installation package, so UCMA is not required and should not be installed on client computers.</span></span>



</div>

</div>

<div>

## <a name="configuration-requirements"></a><span data-ttu-id="7a2b1-122">配置要求</span><span class="sxs-lookup"><span data-stu-id="7a2b1-122">Configuration Requirements</span></span>

<span data-ttu-id="7a2b1-123">将运行 Lync Server 2013 应力和性能工具的计算机必须按照以下要求进行配置：</span><span class="sxs-lookup"><span data-stu-id="7a2b1-123">The computers that will run the Lync Server 2013 Stress and Performance Tool must be configured according to the following requirements:</span></span>

1.  <span data-ttu-id="7a2b1-124">您必须以 "域" 或 "本地管理员" 组的成员身份登录。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-124">You must be logged on as a member of the Domain or Local Admins group.</span></span>

2.  <span data-ttu-id="7a2b1-125">Lync Server 2013 应力和性能工具 ( # A0) 不能在同时运行 Lync Server 2013 组件的计算机上运行。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-125">Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) cannot be run on a computer that is also running Lync Server 2013 components.</span></span>

3.  <span data-ttu-id="7a2b1-126">必须在前端服务器或用户帐户所驻留的标准版服务器上运行 Lync Server 2013 用户创建工具 ( # A0) 。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-126">You must run the Lync Server 2013 User Creation tool (UserProvisioningTool.exe) on the Front End Server or on the Standard Edition server where the user accounts will reside.</span></span> <span data-ttu-id="7a2b1-127">当该工具运行多次时，已启用 Microsoft 统一通信的每个用户都必须具有唯一的电话号码。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-127">When the tool is run multiple times, each user who is enabled for Microsoft Unified Communications must have a unique phone number.</span></span>

4.  <span data-ttu-id="7a2b1-128">页面文件大小应由系统管理，或者在系统上的 RAM 数量至少应为1.5 倍。</span><span class="sxs-lookup"><span data-stu-id="7a2b1-128">The page file size should be system-managed, or should be at least 1.5 times the amount of RAM on the system.</span></span>

<span data-ttu-id="7a2b1-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a2b1-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

