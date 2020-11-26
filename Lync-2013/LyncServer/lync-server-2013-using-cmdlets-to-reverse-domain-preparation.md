---
title: Lync Server 2013：使用 Cmdlet 反向执行域准备
description: Lync Server 2013：使用 cmdlet 反向域准备。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using cmdlets to reverse domain preparation
ms:assetid: 014dba5d-fcb3-44c9-9d63-ae0755276dac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398071(v=OCS.15)
ms:contentKeyID: 48183227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d26cc97ee934ee959838f38f4e2f52f9bf89566
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439014"
---
# <a name="using-cmdlets-to-reverse-domain-preparation-for-lync-server-2013"></a><span data-ttu-id="b2808-103">使用 Cmdlet 为 Lync Server 2013 反向执行域准备</span><span class="sxs-lookup"><span data-stu-id="b2808-103">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2808-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2808-104">

<span> </span></span></span>

<span data-ttu-id="b2808-105">_**主题上次修改时间：** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="b2808-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="b2808-106">使用 **CsAdDomain** cmdlet 可撤消域准备步骤。</span><span class="sxs-lookup"><span data-stu-id="b2808-106">Use the **Disable-CsAdDomain** cmdlet to reverse the domain preparation step.</span></span>

<div>

## <a name="to-use-cmdlets-to-reverse-domain-preparation"></a><span data-ttu-id="b2808-107">使用 cmdlet 反向域准备</span><span class="sxs-lookup"><span data-stu-id="b2808-107">To use cmdlets to reverse domain preparation</span></span>

1.  <span data-ttu-id="b2808-108">以域管理员组的成员身份登录域中的任何服务器。</span><span class="sxs-lookup"><span data-stu-id="b2808-108">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="b2808-109">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="b2808-109">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="b2808-110">运行：</span><span class="sxs-lookup"><span data-stu-id="b2808-110">Run:</span></span>
    
        Disable-CsAdDomain [-Domain <Fqdn>] [-DomainController <Fqdn>] [-Force <SwitchParameter>] 
        [-GlobalCatalog <Fqdn>] [-GlobalSettingsDomainController <Fqdn>] 
    
    <span data-ttu-id="b2808-111">例如：</span><span class="sxs-lookup"><span data-stu-id="b2808-111">For example:</span></span>
    
        Disable-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.net -Force
    
    <span data-ttu-id="b2808-112">如果存在 Force 参数，即使已激活域中的一个或多个前端服务器或 A/V 会议服务器，也会回退域准备。</span><span class="sxs-lookup"><span data-stu-id="b2808-112">If the Force parameter is present, domain preparation is rolled back, even if one or more Front End Servers or A/V Conferencing Servers in the domain are activated.</span></span> <span data-ttu-id="b2808-113">如果 Force 参数不存在，则在激活域中的任何前端服务器或 A/V 会议服务器时，将终止域准备回退。</span><span class="sxs-lookup"><span data-stu-id="b2808-113">If the Force parameter is not present, domain preparation rollback is terminated if any Front End Servers or A/V Conferencing Servers in the domain are activated.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b2808-114">参数 GlobalSettingsDomainController 允许你指示全局设置的存储位置。</span><span class="sxs-lookup"><span data-stu-id="b2808-114">The parameter GlobalSettingsDomainController allows you to indicate where global settings are stored.</span></span> <span data-ttu-id="b2808-115">如果你的设置存储在系统容器中 (这通常是由于尚未将全局设置迁移到配置容器) 的升级部署，你可以在 Active Directory 林的根中定义域控制器。</span><span class="sxs-lookup"><span data-stu-id="b2808-115">If your settings are stored in the System container (which is typical with upgrade deployments that have not had the global setting migrated to the Configuration container), you define a domain controller in the root of your Active Directory forest.</span></span> <span data-ttu-id="b2808-116">如果全局设置存储在“配置”容器中（在新部署或设置已迁移到“配置”容器的升级部署中时通常是这种情况），则定义林中的任何域控制器。</span><span class="sxs-lookup"><span data-stu-id="b2808-116">If the global settings are in the Configuration container (which is typical with new deployments or upgrade deployments where the settings have been migrated to the Configuration container), you define any domain controller in the forest.</span></span> <span data-ttu-id="b2808-117">如果不指定此参数，则 cmdlet 假定设置存储在配置容器中，并引用 AD DS 中的任何域控制器 &nbsp; 。</span><span class="sxs-lookup"><span data-stu-id="b2808-117">If you do not specify this parameter, the cmdlet assumes that the settings are stored in the Configuration container and refers to any domain controller in AD&nbsp;DS.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b2808-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2808-118">See Also</span></span>


[<span data-ttu-id="b2808-119">为 Lync Server 2013 运行域准备</span><span class="sxs-lookup"><span data-stu-id="b2808-119">Running domain preparation for Lync Server 2013</span></span>](lync-server-2013-running-domain-preparation.md)  


[<span data-ttu-id="b2808-120">为 Lync Server 2013 准备域</span><span class="sxs-lookup"><span data-stu-id="b2808-120">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="b2808-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2808-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

