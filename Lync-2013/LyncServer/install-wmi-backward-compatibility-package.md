---
title: 安装 WMI 向后兼容程序包
description: 安装 WMI 向后兼容程序包。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439570"
---
# <a name="install-wmi-backward-compatibility-package"></a><span data-ttu-id="f03e2-103">安装 WMI 向后兼容程序包</span><span class="sxs-lookup"><span data-stu-id="f03e2-103">Install WMI Backward Compatibility package</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f03e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f03e2-104">

<span> </span></span></span>

<span data-ttu-id="f03e2-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="f03e2-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="f03e2-106">如果您尝试运行拓扑生成器合并向导而不安装 WMI 向后兼容性程序包，则会看到以下错误：</span><span class="sxs-lookup"><span data-stu-id="f03e2-106">If you attempt to run the Topology Builder Merge wizard without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="f03e2-107">![WMI 错误消息](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI 错误消息")</span><span class="sxs-lookup"><span data-stu-id="f03e2-107">![WMI error message](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI error message")</span></span>

<span data-ttu-id="f03e2-108">如果尝试在不安装 WMI 向后兼容程序包的情况下运行 **CsLegacytopology** cmdlet，则会看到以下错误：</span><span class="sxs-lookup"><span data-stu-id="f03e2-108">If you attempt to run the **Merge-CsLegacytopology** cmdlet without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="f03e2-109">![Windows PowerShell WMI 提供程序错误](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell WMI 提供程序错误")</span><span class="sxs-lookup"><span data-stu-id="f03e2-109">![Windows PowerShell WMI Provider Error](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell WMI Provider Error")</span></span>

<span data-ttu-id="f03e2-110">安装 WMI 向后兼容包</span><span class="sxs-lookup"><span data-stu-id="f03e2-110">To install the WMI Backward Compatibility Package</span></span>

1.  <span data-ttu-id="f03e2-111">从安装媒体中，导航到 " \\ 设置 \\ AMD64 设置" \\ \\OCSWMIBC.MSI。</span><span class="sxs-lookup"><span data-stu-id="f03e2-111">From your installation media, navigate to \\SETUP\\AMD64\\SETUP\\OCSWMIBC.MSI.</span></span>

2.  <span data-ttu-id="f03e2-112">安装 OCSWMIBC.MSI。</span><span class="sxs-lookup"><span data-stu-id="f03e2-112">Install OCSWMIBC.MSI.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f03e2-113">OCSWMIBC.msi 必须安装在运行拓扑生成器合并向导的计算机上。</span><span class="sxs-lookup"><span data-stu-id="f03e2-113">OCSWMIBC.msi must be installed on the computer where the Topology Builder Merge wizard is run.</span></span> <span data-ttu-id="f03e2-114">但是，我们建议在拓扑中的所有前端服务器上安装 OCSWMIBC.msi。</span><span class="sxs-lookup"><span data-stu-id="f03e2-114">However, we recommend installing OCSWMIBC.msi on all Front End servers in your topology.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f03e2-115">OCSWMIBC.msi 可以安装在具有 Lync Server 2013 核心组件和安装了 Lync Server 2013 管理外壳的域中的任何计算机上，并且有权访问 Office 通信服务器 2007 R2 拓扑 (WMI 提供程序与 Active Directory 域服务 (AD DS) 和 SQL Server) 。</span><span class="sxs-lookup"><span data-stu-id="f03e2-115">OCSWMIBC.msi can be installed on any computer in the domain that has the Lync Server 2013 Core Components and the Lync Server 2013 Management Shell installed, and has access to the Office Communications Server 2007 R2 topology (WMI provider to Active Directory Domain Services (AD DS) and SQL Server).</span></span>

    
    <span data-ttu-id="f03e2-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f03e2-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

