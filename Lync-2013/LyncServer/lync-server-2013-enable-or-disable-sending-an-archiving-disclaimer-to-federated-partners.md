---
title: 启用或禁用向联盟伙伴发送存档免责声明
description: 启用或禁用向联盟伙伴发送存档免责声明。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable sending an Archiving disclaimer to federated partners
ms:assetid: c8e9a2fa-9dc1-4e4d-919f-56ece8004864
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182584(v=OCS.15)
ms:contentKeyID: 48185391
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6c1523a19bc2758e170c044a306398bef45ec33f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437537"
---
# <a name="enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners-in-lync-server-2013"></a><span data-ttu-id="f2d43-103">在 Lync Server 2013 中启用或禁用向联盟伙伴发送存档免责声明</span><span class="sxs-lookup"><span data-stu-id="f2d43-103">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2d43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2d43-104">

<span> </span></span></span>

<span data-ttu-id="f2d43-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f2d43-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f2d43-106">在部署你的边缘服务器并为你的组织启用联盟后，你应该已指定是否要将存档免责声明自动发送给联盟伙伴。</span><span class="sxs-lookup"><span data-stu-id="f2d43-106">At the time you deployed your Edge Servers and enabled federation for your organization, you should have specified whether to automatically send the archiving disclaimer to federated partners.</span></span> <span data-ttu-id="f2d43-107">如果您存档外部通信，则应启用发送存档免责声明。</span><span class="sxs-lookup"><span data-stu-id="f2d43-107">If you archive external communications, you should enable the sending of an archiving disclaimer.</span></span> <span data-ttu-id="f2d43-108">使用本主题中的过程更改该配置。</span><span class="sxs-lookup"><span data-stu-id="f2d43-108">Use the procedure in this topic to change that configuration.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="f2d43-109">以下过程假定你已为你的组织启用联盟。</span><span class="sxs-lookup"><span data-stu-id="f2d43-109">The following procedure assumes that you have already enabled federation for your organization.</span></span> <span data-ttu-id="f2d43-110">有关启用联盟的详细信息，请参阅在部署文档或操作文档中 <A href="lync-server-2013-enable-or-disable-remote-user-access.md">启用或禁用 Lync Server 2013 中的远程用户访问</A> 。</span><span class="sxs-lookup"><span data-stu-id="f2d43-110">For details about enabling federation, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A> in the Deployment documentation or the Operations documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-sending-of-an-archiving-disclaimer-to-federated-partners"></a><span data-ttu-id="f2d43-111">启用或禁用向联盟伙伴发送存档免责声明</span><span class="sxs-lookup"><span data-stu-id="f2d43-111">To enable or disable sending of an archiving disclaimer to federated partners</span></span>

1.  <span data-ttu-id="f2d43-112">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="f2d43-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f2d43-113">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="f2d43-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f2d43-114">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="f2d43-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f2d43-115">在左侧导航栏中，单击 " **外部用户访问**"，然后单击 " **访问边缘配置**"。</span><span class="sxs-lookup"><span data-stu-id="f2d43-115">In the left navigation bar, click **External User Access**, click **Access Edge Configuration**.</span></span>

4.  <span data-ttu-id="f2d43-116">在“**访问边缘配置**”选项卡上，单击“**全局**”，再单击“**编辑**”，然后单击“**显示详细信息**”。</span><span class="sxs-lookup"><span data-stu-id="f2d43-116">On the **Access Edge Configuration** tab, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="f2d43-117">在 " **编辑访问边缘配置**" 下的 " **启用与联盟用户的通信**" 下，选中或清除 " **将存档声明发送给联盟伙伴** " 复选框以启用或禁用自动发送存档免责声明。</span><span class="sxs-lookup"><span data-stu-id="f2d43-117">In **Edit Access Edge Configuration**, under **Enable communications with federated users**, select or clear the **Send archiving disclaimer to federated partners** check box to enable or disable automatically sending the archiving disclaimer.</span></span>

6.  <span data-ttu-id="f2d43-118">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="f2d43-118">Click **Commit**.</span></span>

<span data-ttu-id="f2d43-119">若要使联盟用户能够与 Lync Server 2013 部署中的用户进行协作，你必须也配置了至少一个外部访问策略来支持联合用户访问。</span><span class="sxs-lookup"><span data-stu-id="f2d43-119">To enable federated users to collaborate with users in your Lync Server 2013 deployment, you must have also configured at least one external access policy to support federated user access.</span></span> <span data-ttu-id="f2d43-120">有关详细信息，请参阅在部署文档或操作文档中 [管理 Lync Server 2013 中的 XMPP 联盟合作伙伴](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) 。</span><span class="sxs-lookup"><span data-stu-id="f2d43-120">For details, see [Manage XMPP federated partners in Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) in the Deployment documentation or the Operations documentation.</span></span> <span data-ttu-id="f2d43-121">有关控制特定联盟域的访问权限的详细信息，请参阅部署文档或操作文档中的 [在 Lync Server 2013 中配置对允许的外部域的支持](lync-server-2013-configure-support-for-allowed-external-domains.md) 。</span><span class="sxs-lookup"><span data-stu-id="f2d43-121">For details about controlling access for specific federated domains, see [Configure support for allowed external domains in Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md) in the Deployment documentation or Operations documentation.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-the-archiving-disclaimer-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="f2d43-122">使用 Windows PowerShell Cmdlet 启用或禁用存档放弃声明</span><span class="sxs-lookup"><span data-stu-id="f2d43-122">Enabling or Disabling the Archiving Disclaimer by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="f2d43-123">可通过使用 Windows PowerShell 和 Set-CsAccessEdgeConfiguration cmdlet 来管理存档否认使用。</span><span class="sxs-lookup"><span data-stu-id="f2d43-123">The use of the archiving disclaimer can be managed by using Windows PowerShell and the Set-CsAccessEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="f2d43-124">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="f2d43-124">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="f2d43-125">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="f2d43-125">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-archiving-disclaimer"></a><span data-ttu-id="f2d43-126">启用存档免责声明</span><span class="sxs-lookup"><span data-stu-id="f2d43-126">To enable the archiving disclaimer</span></span>

  - <span data-ttu-id="f2d43-127">要启用存档免责声明，请将 **EnableArchivingDisclaimer** 属性的值设置为 True ($True)：</span><span class="sxs-lookup"><span data-stu-id="f2d43-127">To enable the archiving disclaimer, set the value of the **EnableArchivingDisclaimer** property to True ($True):</span></span>
    
        Set-CsAccessEdgeConfiguration -EnableArchivingDisclaimer $True

</div>

<div>

## <a name="to-disable-the-archiving-disclaimer"></a><span data-ttu-id="f2d43-128">禁用存档放弃声明</span><span class="sxs-lookup"><span data-stu-id="f2d43-128">To disable the archiving disclaimer</span></span>

  - <span data-ttu-id="f2d43-129">要禁用存档免责声明，请将 **EnableArchivingDisclaimer** 属性的值设置为 False ($False)：</span><span class="sxs-lookup"><span data-stu-id="f2d43-129">To disable the archiving disclaimer, set the value of the **EnableArchivingDisclaimer** property to False ($False):</span></span>
    
        Set-CsAccessEdgeConfiguration -EnableArchivingDisclaimer $False

<span data-ttu-id="f2d43-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2d43-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

