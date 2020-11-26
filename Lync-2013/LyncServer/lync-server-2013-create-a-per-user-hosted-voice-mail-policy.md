---
title: Lync Server 2013：创建每用户托管的语音邮件策略
description: Lync Server 2013：创建每用户托管的语音邮件策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a per-user hosted voice mail policy
ms:assetid: 39018a7c-e0c3-46a2-be4e-05604ec67a50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425867(v=OCS.15)
ms:contentKeyID: 48183902
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de528ceb9bc01114948c276c27f99039658aee38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432126"
---
# <a name="create-a-per-user-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="3c745-103">在 Lync Server 2013 中创建每用户托管语音邮件策略</span><span class="sxs-lookup"><span data-stu-id="3c745-103">Create a per-user hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c745-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c745-104">

<span> </span></span></span>

<span data-ttu-id="3c745-105">_**主题上次修改时间：** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="3c745-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="3c745-106">*每用户* 策略只能影响单个用户、组和联系人对象。</span><span class="sxs-lookup"><span data-stu-id="3c745-106">A *per-user* policy can only impact individual users, groups, and contact objects.</span></span> <span data-ttu-id="3c745-107">若要部署每用户策略，必须将策略显式分配给一个或多个用户、组或联系人对象。</span><span class="sxs-lookup"><span data-stu-id="3c745-107">To deploy a per-user policy, you must explicitly assign the policy to one or more users, groups, or contact objects.</span></span> <span data-ttu-id="3c745-108">有关详细信息，请参阅 [在 Lync Server 2013 中分配每用户托管语音邮件策略](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="3c745-108">For details, see [Assign a per-user hosted voice mail policy in Lync Server 2013](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md).</span></span>

<span data-ttu-id="3c745-109">有关使用每用户托管语音邮件策略的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="3c745-109">For details about working with per-user hosted voice mail policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="3c745-110">新-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="3c745-110">New-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="3c745-111">Set-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="3c745-111">Set-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="3c745-112">CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="3c745-112">Get-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostedVoicemailPolicy)

<div>

## <a name="to-create-a-per-user-hosted-voice-mail-policy"></a><span data-ttu-id="3c745-113">创建每用户托管的语音邮件策略</span><span class="sxs-lookup"><span data-stu-id="3c745-113">To create a per-user hosted voice mail policy</span></span>

1.  <span data-ttu-id="3c745-114">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="3c745-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="3c745-115">运行 New-CsHostedVoicemailPolicy cmdlet 以创建策略。</span><span class="sxs-lookup"><span data-stu-id="3c745-115">Run the New-CsHostedVoicemailPolicy cmdlet to create the policy.</span></span> <span data-ttu-id="3c745-116">例如，运行：</span><span class="sxs-lookup"><span data-stu-id="3c745-116">For example, run:</span></span>
    
        New-CsHostedVoicemailPolicy -Identity ExRedmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for Redmond users." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    <span data-ttu-id="3c745-117">前面的示例将创建具有每用户作用域的托管语音邮件策略，并设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="3c745-117">The previous example creates a hosted voice mail policy with per-user scope, and sets the following parameters:</span></span>
    
      - <span data-ttu-id="3c745-118">**标识** 指定策略的唯一标识符，其中包括范围。</span><span class="sxs-lookup"><span data-stu-id="3c745-118">**Identity** specifies a unique identifier for the policy, which includes the scope.</span></span> <span data-ttu-id="3c745-119">对于具有每用户范围的策略，此参数值指定为一个简单的字符串，例如 ExRedmond。</span><span class="sxs-lookup"><span data-stu-id="3c745-119">For a policy with per-user scope, this parameter value is specified as a simple string, for example, ExRedmond.</span></span>
    
      - <span data-ttu-id="3c745-120">**Destination** 指定托管 Exchange UM 服务 (FQDN) 的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="3c745-120">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="3c745-121">此参数是可选的，但如果你尝试为托管语音邮件启用用户，并且用户分配的策略没有目标值，则 enable 将失败。</span><span class="sxs-lookup"><span data-stu-id="3c745-121">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="3c745-122">**说明** 提供有关策略的可选描述性信息。</span><span class="sxs-lookup"><span data-stu-id="3c745-122">**Description** provides optional descriptive information about the policy.</span></span>
    
      - <span data-ttu-id="3c745-123">**组织** 指定用于家庭 Lync Server 2013 用户的 Exchange 租户的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="3c745-123">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users.</span></span> <span data-ttu-id="3c745-124">必须在托管 Exchange UM 服务上将每个租户指定为该租户的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="3c745-124">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3c745-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c745-125">See Also</span></span>


[<span data-ttu-id="3c745-126">在 Lync Server 2013 中分配每用户托管语音邮件策略</span><span class="sxs-lookup"><span data-stu-id="3c745-126">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)  
  

<span data-ttu-id="3c745-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c745-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

