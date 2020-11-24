---
title: Lync Server 2013：部署 Lync 会议室系统管理 Web 门户
description: Lync Server 2013：部署 Lync 会议室系统管理 Web 门户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying the Lync Room System Administrative Web Portal
ms:assetid: ecba5b36-632e-40b9-9c2e-ab825baf7a46
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436324(v=OCS.15)
ms:contentKeyID: 56737621
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e67723b3ddf3f452c53411e560420bb0b043128e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391834"
---
# <a name="deploying-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="0ed7e-103">Deploying the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ed7e-103">Deploying the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ed7e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ed7e-104">

<span> </span></span></span>

<span data-ttu-id="0ed7e-105">_**主题上次修改时间：** 2015-05-04_</span><span class="sxs-lookup"><span data-stu-id="0ed7e-105">_**Topic Last Modified:** 2015-05-04_</span></span>

<span data-ttu-id="0ed7e-106">Microsoft Lync Server 2013 Lync 会议室系统 (LRS) 管理 Web 门户是一个 Web 门户，组织可以使用该门户维护其 Lync 会议室系统会议室。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-106">The Microsoft Lync Server 2013 Lync Room System (LRS) Administrative Web Portal is a web portal that organizations can use to maintain their Lync Room System conference rooms.</span></span> <span data-ttu-id="0ed7e-107">管理员可以使用 LRS 管理 Web 门户监视 LRS 运行状况，例如通过监视连接的音频/视频设备进行监视。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-107">Administrators can use the LRS Administrative Web Portal to monitor LRS health, for example by monitoring audio/video devices that are connected.</span></span> <span data-ttu-id="0ed7e-108">通过此门户，管理员可以远程收集诊断信息以监控会议室的运行状况。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-108">With this portal, administrators can remotely collect diagnostic information to monitor conference room health.</span></span>

<span data-ttu-id="0ed7e-109">在每个 Lync 前端服务器上部署 LRS 管理 Web 门户。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-109">The LRS Administrative Web Portal is deployed on every Lync Front End Server.</span></span> <span data-ttu-id="0ed7e-110">本指南提供有关如何安装和配置 LRS 管理 Web 门户的管理员的说明。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-110">This guide provides instructions for administrators about how to install and configure the LRS Administrative Web Portal.</span></span> <span data-ttu-id="0ed7e-111">它适用于了解 Lync Server 管理知识的管理员，以及拥有修改 Lync Server 拓扑的管理员用户权限的人员。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-111">It is intended for administrators who have knowledge of Lync Server administration, and who have administrator user rights to modify the Lync Server topology.</span></span>

<span data-ttu-id="0ed7e-112">在服务器上部署 LRS 管理 Web 门户后，管理员可以通过从其自己的计算机或笔记本电脑登录网站来检查所有 LRS 聊天室的状态。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-112">After LRS Administrative Web Portal is deployed on the server, administrators can check the status of all LRS rooms by logging on to the site from their own computers or laptops.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0ed7e-113">在 Microsoft Lync Server 2013 部署中安装 LRS 管理 Web 门户时，应使用 <A href="https://go.microsoft.com/fwlink/p/?linkid=544806">适用于 Lync server 2013 的 Microsoft Lync 会议室系统管理 Web 门户</A>。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-113">When you install the LRS Administrative Web Portal in a Microsoft Lync Server 2013 deployment, you should use the <A href="https://go.microsoft.com/fwlink/p/?linkid=544806">Microsoft Lync Room System Administrative Web Portal for Lync Server 2013</A>.</span></span><BR><span data-ttu-id="0ed7e-114">Skype for business Server 2015 提供了新版本的 LRS 管理 Web 门户，但除非已部署 Skype for business Server 2015，否则不应安装该版本。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-114">A new version of the LRS Administrative Web Portal is available for Skype for Business Server 2015, but you should not install that version unless you have deployed Skype for Business Server 2015.</span></span> <span data-ttu-id="0ed7e-115">下载 <A href="https://go.microsoft.com/fwlink/?linkid=544807">适用于 Skype for Business Server 2015 的 Microsoft Lync 会议室系统管理 Web 门户</A>。</span><span class="sxs-lookup"><span data-stu-id="0ed7e-115">Download the <A href="https://go.microsoft.com/fwlink/?linkid=544807">Microsoft Lync Room System Administrative Web Portal for Skype for Business Server 2015</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0ed7e-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="0ed7e-116">In This Section</span></span>

[<span data-ttu-id="0ed7e-117">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span><span class="sxs-lookup"><span data-stu-id="0ed7e-117">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span></span>](lync-server-2013-configuring-your-environment-for-the-lync-room-system-administrative-web-portal.md)

[<span data-ttu-id="0ed7e-118">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ed7e-118">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>](lync-server-2013-installing-the-lync-room-system-administrative-web-portal.md)

[<span data-ttu-id="0ed7e-119">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ed7e-119">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>](lync-server-2013-using-the-lync-room-system-administrative-web-portal.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0ed7e-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0ed7e-120">See Also</span></span>


[<span data-ttu-id="0ed7e-121">在 Lync Server 2013 中部署会议</span><span class="sxs-lookup"><span data-stu-id="0ed7e-121">Deploying conferencing in Lync Server 2013</span></span>](lync-server-2013-deploying-conferencing.md)  
  

<span data-ttu-id="0ed7e-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ed7e-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

