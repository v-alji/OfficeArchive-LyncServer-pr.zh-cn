---
title: 在 Lync Server 中创建和配置用于存档的用户策略
description: 在 Lync Server 中创建和配置用于存档的用户策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating and configuring user policies for Archiving in Lync Server
ms:assetid: 5af0e605-3563-4d6f-a3c6-511d204a3165
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204923(v=OCS.15)
ms:contentKeyID: 48184234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dad260910f01e10c71dbbde67af98ea9a207e33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431538"
---
# <a name="creating-and-configuring-user-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="9630d-103">在 Lync Server 2013 中创建和配置用于存档的用户策略</span><span class="sxs-lookup"><span data-stu-id="9630d-103">Creating and configuring user policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9630d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9630d-104">

<span> </span></span></span>

<span data-ttu-id="9630d-105">_**主题上次修改时间：** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="9630d-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="9630d-106">若要启用或禁用驻留在 Lync Server 上的特定用户的存档，必须首先创建一个用户策略，然后将该策略应用于一个或多个用户或用户组。</span><span class="sxs-lookup"><span data-stu-id="9630d-106">To enable or disable Archiving for specific users homed on Lync Server, you must first create a user policy and then apply the policy to one or more users or user groups.</span></span> <span data-ttu-id="9630d-107">有关将用户策略应用于特定用户和用户组的详细信息，请参阅部署文档中 Lync server 2013 中的 [用户应用 Lync Server 存档策略](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) 。</span><span class="sxs-lookup"><span data-stu-id="9630d-107">For details about applying user policies to specific users and user groups, see [Applying a Lync Server Archiving policy to a user in Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in the Deployment documentation.</span></span>

<span data-ttu-id="9630d-108">有关存档策略的工作原理的详细信息（包括全局、网站和用户策略的层次结构），请参阅在计划文档、部署文档或操作文档中的 [存档在 Lync Server 2013 中的工作方式](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="9630d-108">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, in the Deployment documentation, or in the Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="9630d-109">如果为你的部署启用了 Microsoft Exchange 集成，Exchange In-Place 保留策略控制是否为托管于 Exchange 2013 的用户启用存档，并将其邮箱置于 In-Place 保留状态。</span><span class="sxs-lookup"><span data-stu-id="9630d-109">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="9630d-110">有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">使用 Exchange Server 集成时在 Lync Server 2013 中设置存档策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="9630d-110">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="9630d-111">在启用存档之前，应在存档配置中指定所有适当的选项。</span><span class="sxs-lookup"><span data-stu-id="9630d-111">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="9630d-112">有关详细信息，请参阅部署文档中 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 中的 "配置存档选项</A> "。</span><span class="sxs-lookup"><span data-stu-id="9630d-112">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-an-archiving-policy-for-users-homed-on-lync-server"></a><span data-ttu-id="9630d-113">为驻留在 Lync Server 上的用户配置存档策略</span><span class="sxs-lookup"><span data-stu-id="9630d-113">To configure an archiving policy for users homed on Lync Server</span></span>

1.  <span data-ttu-id="9630d-114">使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="9630d-114">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9630d-115">打开一个浏览器窗口，然后输入管理员 URL 以打开 Lync Server 2013 控制面板。</span><span class="sxs-lookup"><span data-stu-id="9630d-115">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="9630d-116">有关可用于启动 Lync Server 2013 控制面板的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="9630d-116">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9630d-117">在左侧导航栏中，单击“监控和存档”，然后单击“存档策略”。</span><span class="sxs-lookup"><span data-stu-id="9630d-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="9630d-118">单击“**新建**”，然后单击“**用户策略**”。</span><span class="sxs-lookup"><span data-stu-id="9630d-118">Click **New**, and then click **User policy**.</span></span>

5.  <span data-ttu-id="9630d-119">在“**新建存档策略**”中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="9630d-119">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="9630d-120">在“**名称**”中，指定用户策略的名称。</span><span class="sxs-lookup"><span data-stu-id="9630d-120">In **Name**, specify the name for the user policy.</span></span>
    
      - <span data-ttu-id="9630d-121">在“**说明**”中，提供有关该用户策略内容的信息（例如，法律部门的用户策略）。</span><span class="sxs-lookup"><span data-stu-id="9630d-121">In **Description**, provide information about what the user policy is (for example, user policy for legal department).</span></span>
    
      - <span data-ttu-id="9630d-122">若要控制用户策略的内部通信存档，请选中或清除“**存档内部通信**”复选框。</span><span class="sxs-lookup"><span data-stu-id="9630d-122">To control archiving of internal communications for the user policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="9630d-123">若要控制用户策略的外部通信存档，请选中或清除“**存档外部通信**”复选框。</span><span class="sxs-lookup"><span data-stu-id="9630d-123">To control archiving of external communications for the user policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="9630d-124">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="9630d-124">Click **Commit**.</span></span>

<span data-ttu-id="9630d-125">用户策略仅适用于为其分配策略的用户。</span><span class="sxs-lookup"><span data-stu-id="9630d-125">A user policy applies only to users to whom you assign the policy.</span></span> <span data-ttu-id="9630d-126">有关将用户策略应用于特定用户的详细信息，请参阅部署文档中 Lync server 2013 中的 [用户应用 Lync Server 存档策略](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) 。</span><span class="sxs-lookup"><span data-stu-id="9630d-126">For details about applying a user policy to specific users, see [Applying a Lync Server Archiving policy to a user in Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in the Deployment documentation.</span></span>

<span data-ttu-id="9630d-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9630d-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

