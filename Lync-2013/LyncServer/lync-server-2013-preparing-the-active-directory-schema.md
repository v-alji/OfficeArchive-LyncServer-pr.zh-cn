---
title: Lync Server 2013：准备 Active Directory 架构
description: Lync Server 2013：准备 Active Directory 架构。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the Active Directory schema
ms:assetid: 067726ae-fd3f-4133-a32f-26d2603ac674
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398119(v=OCS.15)
ms:contentKeyID: 48183300
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3df7533dcbabe278fd366b441cfd8daa83f54b23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424107"
---
# <a name="preparing-the-active-directory-schema-in-lync-server-2013"></a><span data-ttu-id="a1ed8-103">在 Lync Server 2013 中准备 Active Directory 架构</span><span class="sxs-lookup"><span data-stu-id="a1ed8-103">Preparing the Active Directory schema in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a1ed8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a1ed8-104">

<span> </span></span></span>

<span data-ttu-id="a1ed8-105">_**主题上次修改时间：** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="a1ed8-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="a1ed8-106">在开始准备 Active Directory 域服务之前，你可以使用文本编辑器（如 Windows 记事本）打开架构文件，或者查看 [由 Lync server 2013 使用的 Active directory 架构扩展、类和属性](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) ，以查看将针对 Lync server 2013 进行修改的所有 Active Directory 域服务架构扩展。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-106">Before you begin preparing Active Directory Domain Services, you can open the schema files by using a text editor, such as Windows Notepad, or see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) to review all the Active Directory Domain Services schema extensions that will be modified for Lync Server 2013.</span></span> <span data-ttu-id="a1ed8-107">Lync 服务器使用四个架构文件：</span><span class="sxs-lookup"><span data-stu-id="a1ed8-107">Lync Server uses four schema files:</span></span>

  - <span data-ttu-id="a1ed8-108">ExternalSchema 用于与 Microsoft Exchange Server 的互操作性</span><span class="sxs-lookup"><span data-stu-id="a1ed8-108">ExternalSchema.ldf, which is used for interoperability with Microsoft Exchange Server</span></span>

  - <span data-ttu-id="a1ed8-109">ServerSchema，它是主 Lync Server 2013 架构文件</span><span class="sxs-lookup"><span data-stu-id="a1ed8-109">ServerSchema.ldf, which is the primary Lync Server 2013 schema file</span></span>

  - <span data-ttu-id="a1ed8-110">BackCompatSchema 用于与以前版本中的任何组件的互操作性</span><span class="sxs-lookup"><span data-stu-id="a1ed8-110">BackCompatSchema.ldf, which is used for interoperability with any components from prior releases</span></span>

  - <span data-ttu-id="a1ed8-111">VersionSchema 用于预准备架构的版本信息</span><span class="sxs-lookup"><span data-stu-id="a1ed8-111">VersionSchema.ldf, which is used for version information of the prepared schema</span></span>

<span data-ttu-id="a1ed8-112">无论是从以前的版本迁移还是执行全新安装，都将在架构准备期间安装所有 .ldf 文件。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-112">All .ldf files are installed during schema preparation, regardless of whether you are migrating from a previous release or performing a clean installation.</span></span> <span data-ttu-id="a1ed8-113">这些架构文件按照前面列表中显示的顺序安装，位于 \\ 安装媒体上的 "支持 \\ 架构" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-113">These schema files are installed in the sequence shown in the preceding list and are located in the \\Support\\schema folder on the installation media.</span></span>

<span data-ttu-id="a1ed8-114">Lync Server 架构扩展跨所有域复制，这会影响网络流量。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-114">The Lync Server schema extensions are replicated across all domains, which impacts network traffic.</span></span> <span data-ttu-id="a1ed8-115">当网络使用率较低时，请一次运行架构准备。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-115">Run schema preparation at a time when network usage is low.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a1ed8-116">如果需要将 Microsoft® Office Communicator Mobile 2007 R2 for Java 和 Microsoft® Office Communicator Mobile for Nokia 1.0 移动客户端的支持添加到 Lync Server 2013 部署，则需要在安装 Lync Server 2013 期间准备适用于 Microsoft Office 通信服务器 2007 R2 的 Active Directory 架构。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-116">If you need to add support for Microsoft® Office Communicator Mobile 2007 R2 for Java and Microsoft® Office Communicator Mobile for Nokia 1.0 mobile clients to your Lync Server 2013 deployment, you need to prepare the Active Directory schema for Microsoft Office Communications Server 2007 R2 during installation of Lync Server 2013.</span></span> <span data-ttu-id="a1ed8-117">有关必需的软件和文档，请参阅 <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A> 。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-117">For the necessary software and documentation, see <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A>.</span></span>



</div>

<div>

## <a name="adsi-edit"></a><span data-ttu-id="a1ed8-118">ADSI 编辑器</span><span class="sxs-lookup"><span data-stu-id="a1ed8-118">ADSI Edit</span></span>

<span data-ttu-id="a1ed8-119">Active Directory 服务界面编辑器 (ADSI Edit) 是一种可用于验证架构准备和复制的 AD DS 管理工具。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-119">Active Directory Service Interfaces Editor (ADSI Edit) is an AD DS administration tool that you can use to verify schema preparation and replication.</span></span>

<span data-ttu-id="a1ed8-120">安装 AD DS 角色以使服务器成为域控制器时，默认情况下会安装 "ADSI 编辑"。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-120">ADSI Edit is installed by default when you install the AD DS role to make a server a domain controller.</span></span> <span data-ttu-id="a1ed8-121">对于 Windows Server 2008 和 Windows Server 2008 R2，ADSI Edit (adsiedit) 包含在远程服务器管理工具 (RSAT) 中。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-121">For Windows Server 2008 and Windows Server 2008 R2, ADSI Edit (adsiedit.msc) is included with the Remote Server Administration Tools (RSAT).</span></span> <span data-ttu-id="a1ed8-122">您也可以在域成员服务器或独立服务器上安装 RSAT。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-122">You can also install RSAT on domain member servers or stand-alone servers.</span></span> <span data-ttu-id="a1ed8-123">默认情况下，将在安装 Windows 时将 RSAT 程序包复制到这些服务器，但默认情况下不会安装该程序包。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-123">The RSAT package is copied to these servers by default when you install Windows, but it is not installed by default.</span></span> <span data-ttu-id="a1ed8-124">使用服务器管理器安装单个工具。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-124">You install individual tools by using Server Manager.</span></span> <span data-ttu-id="a1ed8-125">" **角色管理工具**"、" **Active Directory 域服务工具**"、" **active directory 域控制器工具**" 下包含 "ADSI 编辑"。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-125">ADSI Edit is included under **Role Administration Tools**, **Active Directory Domain Services Tools**, **Active Directory Domain Controller Tools**.</span></span>

<span data-ttu-id="a1ed8-126">对于 Windows Server 2003，"支持工具" 中附带了 "ADSI 编辑"。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-126">For Windows Server 2003, ADSI Edit is included with the Support Tools.</span></span> <span data-ttu-id="a1ed8-127">支持工具可从 Windows Server 2003 CD 的 " \\ 支持工具" 文件夹中获得 \\ ，也可从 "windows Server 2003 Service Pack 2 32 位支持工具" 下载 [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770) 。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-127">The Support Tools are available from the Windows Server 2003 CD in the \\SUPPORT\\TOOLS folder, or you can download them from “Windows Server 2003 Service Pack 2 32-bit Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770).</span></span> <span data-ttu-id="a1ed8-128">有关从产品 CD 安装支持工具的说明，请访问 "安装 Windows 支持工具" [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771) 。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-128">Instructions for installing the Support Tools from the product CD are available from “Install Windows Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771).</span></span> <span data-ttu-id="a1ed8-129">安装支持工具时，将自动注册 Adsiedit.dll。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-129">Adsiedit.dll is automatically registered when you install the support tools.</span></span> <span data-ttu-id="a1ed8-130">但是，如果您已将文件复制到计算机，则必须运行 **regsvr32** 命令来注册 adsiedit.dll 文件，然后才能运行该工具。</span><span class="sxs-lookup"><span data-stu-id="a1ed8-130">If, however, you copied the files to your computer, you must run the **regsvr32** command to register the adsiedit.dll file before you can run the tool.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a1ed8-131">本节内容</span><span class="sxs-lookup"><span data-stu-id="a1ed8-131">In This Section</span></span>

  - [<span data-ttu-id="a1ed8-132">在 Lync Server 2013 中运行 Active Directory 架构准备</span><span class="sxs-lookup"><span data-stu-id="a1ed8-132">Running Active Directory schema preparation in Lync Server 2013</span></span>](lync-server-2013-running-schema-preparation.md)

  - [<span data-ttu-id="a1ed8-133">在 Lync Server 2013 中验证 Active Directory 架构复制</span><span class="sxs-lookup"><span data-stu-id="a1ed8-133">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a1ed8-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a1ed8-134">See Also</span></span>


[<span data-ttu-id="a1ed8-135">为 Lync Server 2013 准备林</span><span class="sxs-lookup"><span data-stu-id="a1ed8-135">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
[<span data-ttu-id="a1ed8-136">为 Lync Server 2013 准备域</span><span class="sxs-lookup"><span data-stu-id="a1ed8-136">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="a1ed8-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a1ed8-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

