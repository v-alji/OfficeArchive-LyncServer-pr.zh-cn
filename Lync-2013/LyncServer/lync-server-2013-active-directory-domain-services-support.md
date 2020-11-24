---
title: Lync Server 2013：Active Directory 域服务支持
description: Lync Server 2013： Active Directory 域服务支持。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory Domain Services support
ms:assetid: aeb62d5e-e424-473a-b795-9452150c98dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412831(v=OCS.15)
ms:contentKeyID: 48185136
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb2a85bab90557c28c4802721d4202f6188cb3f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391779"
---
# <a name="active-directory-domain-services-support-in-lync-server-2013"></a><span data-ttu-id="89e89-103">Lync Server 2013 中的 Active Directory 域服务支持</span><span class="sxs-lookup"><span data-stu-id="89e89-103">Active Directory Domain Services support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89e89-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89e89-104">

<span> </span></span></span>

<span data-ttu-id="89e89-105">_**主题上次修改时间：** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="89e89-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="89e89-106">Lync Server 2013 使用中央管理存储来存储服务器和服务的配置数据，而不是依赖于 Active Directory 域服务处理此信息，就像过去一样。</span><span class="sxs-lookup"><span data-stu-id="89e89-106">Lync Server 2013 uses the Central Management store to store configuration data for servers and services, instead of relying on Active Directory Domain Services for this information, as in the past.</span></span> <span data-ttu-id="89e89-107">Lync Server 2013 仍在 AD DS 中存储以下内容：</span><span class="sxs-lookup"><span data-stu-id="89e89-107">Lync Server 2013 still stores the following in AD DS:</span></span>

  - <span data-ttu-id="89e89-108">**架构扩展**</span><span class="sxs-lookup"><span data-stu-id="89e89-108">**Schema extensions**</span></span>
    
      - <span data-ttu-id="89e89-109">用户对象扩展</span><span class="sxs-lookup"><span data-stu-id="89e89-109">User object extensions</span></span>
    
      - <span data-ttu-id="89e89-110">Lync Server 2010 和 Office 通信服务器 2007 R2 类的扩展，可保持与以前支持的版本的向后兼容性</span><span class="sxs-lookup"><span data-stu-id="89e89-110">Extensions for Lync Server 2010 and Office Communications Server 2007 R2 classes to maintain backward compatibility with previous supported versions</span></span>

  - <span data-ttu-id="89e89-111">存储在 Lync Server 2013 扩展架构和现有类中的 **数据** () </span><span class="sxs-lookup"><span data-stu-id="89e89-111">**Data** (stored in Lync Server 2013 extended schema and in existing classes)</span></span>
    
      - <span data-ttu-id="89e89-112">用户 SIP URI 和其他用户设置</span><span class="sxs-lookup"><span data-stu-id="89e89-112">User SIP URI and other user settings</span></span>
    
      - <span data-ttu-id="89e89-113">应用程序的联系人对象 (例如，"响应组" 应用程序和 "会议助理" 应用程序) </span><span class="sxs-lookup"><span data-stu-id="89e89-113">Contact objects for applications (for example, the Response Group application and the Conferencing Attendant application)</span></span>
    
      - <span data-ttu-id="89e89-114">为实现向后兼容而发布的数据</span><span class="sxs-lookup"><span data-stu-id="89e89-114">Data published for backward compatibility</span></span>
    
      - <span data-ttu-id="89e89-115">中央管理存储的服务控制点 (SCP)</span><span class="sxs-lookup"><span data-stu-id="89e89-115">A service control point (SCP) for the Central Management store</span></span>
    
      - <span data-ttu-id="89e89-116">Kerberos 身份验证帐户（可选计算机对象）</span><span class="sxs-lookup"><span data-stu-id="89e89-116">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="89e89-117">本部分介绍 Lync Server 2013 的 AD DS 支持要求。</span><span class="sxs-lookup"><span data-stu-id="89e89-117">This section describes the AD DS support requirements for Lync Server 2013.</span></span> <span data-ttu-id="89e89-118">有关拓扑支持的详细信息，请参阅支持文档中的 [Lync Server 2013 中支持的 Active Directory 拓扑](lync-server-2013-supported-active-directory-topologies.md) 。</span><span class="sxs-lookup"><span data-stu-id="89e89-118">For details about topology support, see [Supported Active Directory topologies in Lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) in the Supportability documentation.</span></span>

<div>

## <a name="supported-domain-controller-operating-systems"></a><span data-ttu-id="89e89-119">支持的域控制器操作系统</span><span class="sxs-lookup"><span data-stu-id="89e89-119">Supported Domain Controller Operating Systems</span></span>

<span data-ttu-id="89e89-120">Lync Server 2013 支持运行以下操作系统的域控制器：</span><span class="sxs-lookup"><span data-stu-id="89e89-120">Lync Server 2013 supports domain controllers running the following operating systems:</span></span>

  - <span data-ttu-id="89e89-121">Windows Server 2012 R2 操作系统</span><span class="sxs-lookup"><span data-stu-id="89e89-121">Windows Server 2012 R2 operating system</span></span>

  - <span data-ttu-id="89e89-122">Windows Server 2012 操作系统</span><span class="sxs-lookup"><span data-stu-id="89e89-122">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="89e89-123">Windows Server 2008 R2 操作系统</span><span class="sxs-lookup"><span data-stu-id="89e89-123">Windows Server 2008 R2 operating system</span></span>

  - <span data-ttu-id="89e89-124">Windows Server 2008 操作系统</span><span class="sxs-lookup"><span data-stu-id="89e89-124">Windows Server 2008 operating system</span></span>

  - <span data-ttu-id="89e89-125">Windows Server 2008 企业版32位</span><span class="sxs-lookup"><span data-stu-id="89e89-125">Windows Server 2008 Enterprise 32-Bit</span></span>

  - <span data-ttu-id="89e89-126">32位或64位版本的窗口服务器 2003 R2 操作系统</span><span class="sxs-lookup"><span data-stu-id="89e89-126">The 32-bit or 64-bit versions of the Window Server 2003 R2 operating system</span></span>

  - <span data-ttu-id="89e89-127">32位或64位版本的 Windows Server 2003 操作系统</span><span class="sxs-lookup"><span data-stu-id="89e89-127">The 32-bit or 64-bit versions of the Windows Server 2003 operating system</span></span>

</div>

<div>

## <a name="forest-and-domain-functional-level"></a><span data-ttu-id="89e89-128">林和域功能级别</span><span class="sxs-lookup"><span data-stu-id="89e89-128">Forest and Domain Functional Level</span></span>

<span data-ttu-id="89e89-129">你必须将 Lync Server 2013 部署到的所有域都提升为 Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2、Windows Server 2008 或 Windows Server 2003 至少的域功能级别。</span><span class="sxs-lookup"><span data-stu-id="89e89-129">You must raise all domains in which you deploy Lync Server 2013 to a domain functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

<span data-ttu-id="89e89-130">必须将部署 Lync Server 2013 的所有林都提升为 Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2、Windows Server 2008 或至少 Windows Server 2003 的林功能级别。</span><span class="sxs-lookup"><span data-stu-id="89e89-130">All forests in which you deploy Lync Server 2013 must be raised to a forest functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

</div>

<div>

## <a name="support-for-read-only-domain-controllers"></a><span data-ttu-id="89e89-131">Read-Only 域控制器的支持</span><span class="sxs-lookup"><span data-stu-id="89e89-131">Support for Read-Only Domain Controllers</span></span>

<span data-ttu-id="89e89-132">Lync Server 2013 支持包含只读域控制器或只读全局编录服务器的 Active Directory 域服务部署（只要有可写域控制器可用）。</span><span class="sxs-lookup"><span data-stu-id="89e89-132">Lync Server 2013 supports Active Directory Domain Services deployments that include read-only domain controllers or read-only global catalog servers, as long as there are writable domain controllers available.</span></span>

</div>

<div>

## <a name="domain-names"></a><span data-ttu-id="89e89-133">域名</span><span class="sxs-lookup"><span data-stu-id="89e89-133">Domain Names</span></span>

<span data-ttu-id="89e89-134">Lync 服务器不支持单标记的域。</span><span class="sxs-lookup"><span data-stu-id="89e89-134">Lync Server does not support single-labeled domains.</span></span> <span data-ttu-id="89e89-135">例如，支持一个名为 " **contoso. local** " 的根域的林，但不支持名为 **local** 的根域。</span><span class="sxs-lookup"><span data-stu-id="89e89-135">For example, a forest with a root domain named **contoso.local** is supported, but a root domain named **local** is not supported.</span></span> <span data-ttu-id="89e89-136">有关详细信息，请参阅 Microsoft 知识库文章 300684 "有关为具有单标签 DNS 名称的域配置 Windows 的信息" [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752) 。</span><span class="sxs-lookup"><span data-stu-id="89e89-136">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="89e89-137">Lync Server 不支持重命名域。</span><span class="sxs-lookup"><span data-stu-id="89e89-137">Lync Server does not support renaming domains.</span></span> <span data-ttu-id="89e89-138">如果需要重命名 Lync Server 部署到的域，你需要先卸载 Lync Server，然后重命名域，然后重新安装 Lync Server。</span><span class="sxs-lookup"><span data-stu-id="89e89-138">If you need to rename a domain where Lync Server is deployed, you need to first uninstall Lync Server, then rename the domain, and then reinstall Lync Server.</span></span>



</div>

</div>

<div>

## <a name="locked-down-ad-ds-environments"></a><span data-ttu-id="89e89-139">锁定的 AD DS 环境</span><span class="sxs-lookup"><span data-stu-id="89e89-139">Locked Down AD DS Environments</span></span>

<span data-ttu-id="89e89-140">在锁定的 AD DS 环境中，用户和计算机对象通常位于特定的组织单位中 (Ou 中) 禁用权限继承以帮助保护管理委派和启用组策略对象 (Gpo) 实施安全策略。</span><span class="sxs-lookup"><span data-stu-id="89e89-140">In a locked-down AD DS environment, Users and Computer objects are often placed in specific organizational units (OUs) with permissions inheritance disabled to help secure administrative delegation and to enable use of Group Policy objects (GPOs) to enforce security policies.</span></span> <span data-ttu-id="89e89-141">可以在锁定的活动目录环境中部署 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="89e89-141">Lync Server 2013 can be deployed in a locked-down Active Directory environment.</span></span> <span data-ttu-id="89e89-142">有关在锁定环境中部署 Lync Server 所需内容的详细信息，请参阅部署文档中的 [在 Lync server 2013 中准备锁定的 Active Directory 域服务](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) 。</span><span class="sxs-lookup"><span data-stu-id="89e89-142">For details about what is required to deploy Lync Server in a locked-down environment, see [Preparing a locked-down Active Directory Domain Services in Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) in the Deployment documentation.</span></span>

<span data-ttu-id="89e89-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89e89-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

