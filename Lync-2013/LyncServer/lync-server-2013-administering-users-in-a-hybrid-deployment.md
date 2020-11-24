---
title: Lync Server 2013：管理混合部署中的用户
description: Lync Server 2013：管理混合部署中的用户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391771"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a><span data-ttu-id="5fa94-103">管理混合 Lync Server 2013 部署中的用户</span><span class="sxs-lookup"><span data-stu-id="5fa94-103">Administering users in a hybrid Lync Server 2013 deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5fa94-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5fa94-104">

<span> </span></span></span>

<span data-ttu-id="5fa94-105">_**主题上次修改时间：** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="5fa94-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="5fa94-106">你可以使用 Microsoft 365 管理中心提供的用户管理功能管理迁移到 Lync Online 的用户的用户设置和策略。</span><span class="sxs-lookup"><span data-stu-id="5fa94-106">You can manage user settings and policies for users migrated to Lync Online by using the User Management features available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="5fa94-107">您必须使用租户管理员帐户登录才能执行管理任务。</span><span class="sxs-lookup"><span data-stu-id="5fa94-107">You must sign in by using your tenant administrator account to perform administration tasks.</span></span>

<div>

## <a name="moving-users-back-to-on-premises"></a><span data-ttu-id="5fa94-108">将用户移回本地</span><span class="sxs-lookup"><span data-stu-id="5fa94-108">Moving Users Back to On-premises</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="5fa94-109">此部分仅适用于为本地 Lync 创建和启用的用户，然后从本地部署移动到 Lync Online。</span><span class="sxs-lookup"><span data-stu-id="5fa94-109">This section applies only to users that were created and enabled for Lync on-premises and then moved from an on-premises deployment to Lync Online.</span></span> <span data-ttu-id="5fa94-110">如果你想要移动在 Lync Online 中创建的用户 (并且尚未在本地) 部署中启用 Lync，请参阅在 <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013 中将用户从 Lync Online 移动到本地 lync</A>。</span><span class="sxs-lookup"><span data-stu-id="5fa94-110">If you want to move users that were created in Lync Online (and not ever enabled for Lync in an on-premises deployment) see, <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

  - <span data-ttu-id="5fa94-111">运行以下 cmdlet，将用户从 Lync Online 移回本地 Lync：</span><span class="sxs-lookup"><span data-stu-id="5fa94-111">Run the following cmdlets to move a user from Lync Online back to Lync on-premises:</span></span>
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

<span data-ttu-id="5fa94-112">为 **HostedMigrationOverrideUrl** 参数指定的 URL 的格式必须为运行托管迁移服务的池的 URL，格式如下：</span><span class="sxs-lookup"><span data-stu-id="5fa94-112">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format:</span></span>

<span data-ttu-id="5fa94-113"> Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc。</span><span class="sxs-lookup"><span data-stu-id="5fa94-113">Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc.</span></span> <span data-ttu-id="5fa94-114">你可以通过查看 Microsoft 365 或 Office 365 组织帐户的 Lync Online 控制面板的 URL 来确定托管迁移服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="5fa94-114">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>

<span data-ttu-id="5fa94-115">**确定 Microsoft 365 或 Office 365 组织的托管迁移服务 URL**</span><span class="sxs-lookup"><span data-stu-id="5fa94-115">**To determine the Hosted Migration Service URL for your Microsoft 365 or Office 365 organization**</span></span>

1.  <span data-ttu-id="5fa94-116">以管理员身份登录您的组织。</span><span class="sxs-lookup"><span data-stu-id="5fa94-116">Log in to your organization as an administrator.</span></span>

2.  <span data-ttu-id="5fa94-117">打开 **Lync 管理中心**。</span><span class="sxs-lookup"><span data-stu-id="5fa94-117">Open the **Lync admin center**.</span></span>

3.  <span data-ttu-id="5fa94-118">在显示 **Lync 管理中心** 的情况下，在地址栏中选择并将 URL 复制到 **lync.com**。</span><span class="sxs-lookup"><span data-stu-id="5fa94-118">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="5fa94-119">示例 URL 如下所示：</span><span class="sxs-lookup"><span data-stu-id="5fa94-119">An example URL looks similar to the following:</span></span>
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  <span data-ttu-id="5fa94-120">将 URL 中的 **webdir** 替换为 **admin**，得到以下 URL：</span><span class="sxs-lookup"><span data-stu-id="5fa94-120">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
    
    `https://admin0a.online.lync.com`

5.  <span data-ttu-id="5fa94-121">向 URL 附加以下字符串：**/HostedMigration/hostedmigrationservice.svc**。</span><span class="sxs-lookup"><span data-stu-id="5fa94-121">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
    
    <span data-ttu-id="5fa94-122">得到的 URL 是 **HostedMigrationOverrideUrl** 的值，应类似于以下形式：</span><span class="sxs-lookup"><span data-stu-id="5fa94-122">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

<span data-ttu-id="5fa94-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5fa94-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

