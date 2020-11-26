---
title: Lync Server 2013：启用或禁用远程用户访问
description: Lync Server 2013：启用或禁用远程用户访问。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable remote user access
ms:assetid: cd9d3ddc-4839-457a-86d9-b15413e74002
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182586(v=OCS.15)
ms:contentKeyID: 48185660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dea2d58c1978ac2d52365a4a453c40b38dd89c44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428872"
---
# <a name="enable-or-disable-remote-user-access-in-lync-server-2013"></a><span data-ttu-id="8cc6c-103">在 Lync Server 2013 中启用或禁用远程用户访问</span><span class="sxs-lookup"><span data-stu-id="8cc6c-103">Enable or disable remote user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8cc6c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8cc6c-104">

<span> </span></span></span>

<span data-ttu-id="8cc6c-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="8cc6c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="8cc6c-106">远程用户是组织内具有永久 Active Directory 标识的用户。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-106">Remote users are users in your organization who have a persistent Active Directory identity within the organization.</span></span> <span data-ttu-id="8cc6c-107">远程用户通常使用虚拟专用网络从网络外部登录到 Lync Server，方法是在未连接到组织网络时使用虚拟专用网络 (VPN) 。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-107">Remote users often sign in to Lync Server from outside your network by using a virtual private network (VPN) when they are not connected to your organization’s network.</span></span> <span data-ttu-id="8cc6c-108">远程用户包括在家中或在路上和其他远程工作人员（如受信任的供应商，他们已授予企业凭据）工作的员工。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-108">Remote users include employees working at home or on the road and other remote workers, such as trusted vendors, who have been granted enterprise credentials.</span></span> <span data-ttu-id="8cc6c-109">如果为远程用户启用远程用户访问，受支持的远程用户通过 Internet 进行连接，并且不必使用 VPN 进行连接，以便与使用 Lync Server 的内部用户进行协作。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-109">If you enable remote user access for remote users, supported remote users connect over the Internet and do not have to connect using a VPN in order to collaborate with internal users using Lync Server.</span></span>

<span data-ttu-id="8cc6c-110">若要支持远程用户访问，必须启用远程用户访问。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-110">To support remote user access, you must enable remote user access.</span></span> <span data-ttu-id="8cc6c-111">启用远程用户访问时，将为整个组织启用它。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-111">When you enable remote user access, you enable it for your entire organization.</span></span> <span data-ttu-id="8cc6c-112">如果稍后想要临时或永久阻止远程用户访问，则可以为你的组织禁用它。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-112">If you later want to temporarily or permanently prevent remote user access, you can disable it for your organization.</span></span> <span data-ttu-id="8cc6c-113">使用此部分中的过程可为你的组织启用或禁用远程用户访问。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-113">Use the procedure in this section to enable or disable remote user access for your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8cc6c-114">启用远程用户访问仅指定运行 Access Edge 服务的服务器支持与远程用户的通信，但远程用户无法在即时消息中 (IM) 或组织中的会议，直到还配置了至少一个策略来管理远程用户访问的使用。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-114">Enabling remote user access only specifies that your servers running the Access Edge service support communications with remote users, but remote users cannot participate in instant messaging (IM) or conferences in your organization until you also configure at least one policy to manage the use of remote user access.</span></span> <span data-ttu-id="8cc6c-115">在一个策略级别应用的 Lync Server 策略设置可以覆盖在其他策略级别应用的设置。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-115">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="8cc6c-116">Lync 服务器策略优先级为：用户策略 (大多数影响) 覆盖网站策略，然后网站策略将覆盖全局策略 (最少影响) 。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-116">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="8cc6c-117">这意味着，策略设置与策略所影响的对象距离越近，它对该对象的影响力越大。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-117">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span> <span data-ttu-id="8cc6c-118">有关配置使用远程用户访问策略的详细信息，请参阅 <A href="lync-server-2013-configure-policies-to-control-remote-user-access.md">在 Lync Server 2013 中配置用于控制远程用户访问的策略</A>。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-118">For details about configuring policies for the use of remote user access, see <A href="lync-server-2013-configure-policies-to-control-remote-user-access.md">Configure policies to control remote user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-remote-user-access-for-your-organization"></a><span data-ttu-id="8cc6c-119">为你的组织启用或禁用远程用户访问</span><span class="sxs-lookup"><span data-stu-id="8cc6c-119">To enable or disable remote user access for your organization</span></span>

1.  <span data-ttu-id="8cc6c-120">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-120">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8cc6c-121">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8cc6c-122">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8cc6c-123">在左侧导航栏中，单击“**联盟和外部访问**”，然后单击“**访问边缘配置**”。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-123">In the left navigation bar, click **Federation and External Access**, and then click **Access Edge Configuration**.</span></span>

4.  <span data-ttu-id="8cc6c-124">在 " **访问边缘配置** " 页面上，单击 " **全局**"，单击 " **编辑**"，然后单击 " **显示详细信息**"。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-124">On the **Access Edge Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="8cc6c-125">在 " **编辑访问边缘配置**" 中，执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="8cc6c-125">In **Edit Access Edge Configuration**, do one of the following:</span></span>
    
      - <span data-ttu-id="8cc6c-126">若要为你的组织启用远程用户访问权限，请选中 " **启用远程用户访问** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-126">To enable remote user access for your organization, select the **Enable remote user access** check box.</span></span>
    
      - <span data-ttu-id="8cc6c-127">若要为你的组织禁用远程用户访问权限，请清除 " **启用远程用户访问** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-127">To disable remote user access for your organization, clear the **Enable remote user access** check box.</span></span>

6.  <span data-ttu-id="8cc6c-128">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-128">Click **Commit**.</span></span>

<span data-ttu-id="8cc6c-129">若要使远程用户能够登录到运行 Lync Server 的服务器，还必须至少配置一个外部访问策略以支持远程用户访问。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-129">To enable remote users to sign in to your servers running Lync Server, you must also configure at least one external access policy to support remote user access.</span></span> <span data-ttu-id="8cc6c-130">有关详细信息，请参阅在部署文档或操作文档中的 " [配置用于控制 Lync Server 2013 中的远程用户访问的策略](lync-server-2013-configure-policies-to-control-remote-user-access.md) "。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-130">For details, see [Configure policies to control remote user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-remote-user-access.md) in the Deployment documentation or the Operations documentation.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-remote-user-access-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="8cc6c-131">使用 Windows PowerShell Cmdlet 启用或禁用远程用户访问</span><span class="sxs-lookup"><span data-stu-id="8cc6c-131">Enabling or Disabling Remote User Access by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="8cc6c-132">可使用 Windows PowerShell 和 Set-CsAccessEdgeConfiguration cmdlet 管理远程用户访问。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-132">Remote user access can be managed by using Windows PowerShell and the Set-CsAccessEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="8cc6c-133">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-133">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="8cc6c-134">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="8cc6c-134">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-remote-user-access"></a><span data-ttu-id="8cc6c-135">启用远程用户访问</span><span class="sxs-lookup"><span data-stu-id="8cc6c-135">To enable remote user access</span></span>

  - <span data-ttu-id="8cc6c-136">若要启用远程用户访问，请将 **AllowOutsideUsers** 属性的值设置为 True ($True) ：</span><span class="sxs-lookup"><span data-stu-id="8cc6c-136">To enable remote user access, set the value of the **AllowOutsideUsers** property to True ($True):</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowOutsideUsers $True

</div>

<div>

## <a name="to-disable-remote-user-access"></a><span data-ttu-id="8cc6c-137">禁用远程用户访问</span><span class="sxs-lookup"><span data-stu-id="8cc6c-137">To disable remote user access</span></span>

  - <span data-ttu-id="8cc6c-138">若要禁用远程用户访问，请将 **AllowOutsideUsers** 属性的值设置为 False ($False) ：</span><span class="sxs-lookup"><span data-stu-id="8cc6c-138">To disable remote user access, set the value of the **AllowOutsideUsers** property to False ($False):</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowOutsideUsers $False

<span data-ttu-id="8cc6c-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8cc6c-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

