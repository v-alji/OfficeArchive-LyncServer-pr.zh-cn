---
title: Lync Server 2013：部署共享行外观
description: Lync Server 2013：部署共享线路外观。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy Shared Line Appearance
ms:assetid: 6666dfef-9ecf-4834-af6a-2d5da227dfa3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Mt712152(v=OCS.15)
ms:contentKeyID: 72522137
ms.date: 06/13/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c83c06bbc9b91e11cabc0abee20de28fc7281205
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430173"
---
# <a name="deploy-shared-line-appearance-in-lync-server-2013"></a><span data-ttu-id="eb708-103">在 Lync Server 2013 中部署共享行外观</span><span class="sxs-lookup"><span data-stu-id="eb708-103">Deploy Shared Line Appearance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb708-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb708-104">

<span> </span></span></span>

<span data-ttu-id="eb708-105">_**主题上次修改时间：** 2016-06-13_</span><span class="sxs-lookup"><span data-stu-id="eb708-105">_**Topic Last Modified:** 2016-06-13_</span></span>

<span data-ttu-id="eb708-106">阅读本主题，了解如何在 Lync Server 2013 中 (SLA) 部署共享行外观，累积更新4月2016。</span><span class="sxs-lookup"><span data-stu-id="eb708-106">Read this topic to learn how to deploy Shared Line Appearance (SLA) in Lync Server 2013, Cumulative Update April 2016.</span></span> <span data-ttu-id="eb708-107">SLA 是用于处理对特定号码（称为“共享号码”）的多个呼叫的功能。</span><span class="sxs-lookup"><span data-stu-id="eb708-107">SLA is a feature for handling multiple calls on a specific number called a shared number.</span></span>

<span data-ttu-id="eb708-108">有关此功能的详细信息，请参阅 [Lync Server 2013 中的共享行外观计划](lync-server-2013-plan-for-shared-line-appearance.md)。</span><span class="sxs-lookup"><span data-stu-id="eb708-108">For more information about this feature, see [Plan for Shared Line Appearance in Lync Server 2013](lync-server-2013-plan-for-shared-line-appearance.md).</span></span>

<span data-ttu-id="eb708-109"> (SLA) 的共享行外观是 Lync Server 2013 中的新功能，累积更新4月2016。</span><span class="sxs-lookup"><span data-stu-id="eb708-109">Shared Line Appearance (SLA) is a new feature in Lync Server 2013, Cumulative Update April 2016.</span></span> <span data-ttu-id="eb708-110">要启用此功能，必须首先部署此累积更新。</span><span class="sxs-lookup"><span data-stu-id="eb708-110">To enable this feature, you must have first deployed this cumulative update.</span></span>

<div>

## <a name="install-shared-line-appearance"></a><span data-ttu-id="eb708-111">安装共享线路外观</span><span class="sxs-lookup"><span data-stu-id="eb708-111">Install Shared Line Appearance</span></span>

1.  <span data-ttu-id="eb708-112">在 Lync Server 2013 之后，将部署 "累积更新4月 2016"，默认情况下不启用 SLA 应用程序。</span><span class="sxs-lookup"><span data-stu-id="eb708-112">After Lync Server 2013, Cumulative Update April 2016 is deployed, the SLA application is not enabled by default.</span></span> <span data-ttu-id="eb708-113">若要启用该应用程序，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="eb708-113">To enable the application, follow the steps below:</span></span>
    
    1.  <span data-ttu-id="eb708-114">为每个池运行以下命令，以便将 SLA 注册为服务器应用程序：</span><span class="sxs-lookup"><span data-stu-id="eb708-114">Register SLA as a server application by running the following command for each pool:</span></span>
        ```powershell
        New-CsServerApplication -Identity
                        'Service:Registrar:%FQDN%/SharedLineAppearance' -Uri
                        http://www.microsoft.com/LCS/SharedLineAppearance -Critical $false -Enabled
                        $true -Priority (Get-CsServerApplication -Identity
                        'Service:Registrar:%FQDN%/UserServices').Priority 
        ```
        <span data-ttu-id="eb708-115">其中，%FQDN% 是池的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="eb708-115">where %FQDN% is the fully qualified domain name of the pool.</span></span>
    
    2.  <span data-ttu-id="eb708-116">运行以下命令来更新 SLA cmdlet 的 RBAC 角色：</span><span class="sxs-lookup"><span data-stu-id="eb708-116">Run the following command to update the RBAC roles for the SLA cmdlets:</span></span>
        ```powershell
        Update-CsAdminRole 
        ```
    3.  <span data-ttu-id="eb708-117">重新启动所有池中已安装并启用 SLA 的所有前端服务器（RTCSRV 服务）：</span><span class="sxs-lookup"><span data-stu-id="eb708-117">Restart all the Front End Servers (RTCSRV service) in all the pools where SLA was installed and enabled:</span></span>
        
        ```powershell 
        Stop-CsWindowsService RTCSRV Start-CsWindowsService RTCSRV
                        
        ```

</div>

<div>

## <a name="create-an-sla-group-and-add-users-to-it"></a><span data-ttu-id="eb708-118">创建一个 SLA 组并向该组添加用户</span><span class="sxs-lookup"><span data-stu-id="eb708-118">Create an SLA group and add users to it</span></span>

1.  <span data-ttu-id="eb708-119">使用 [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet 创建 SLA 组：</span><span class="sxs-lookup"><span data-stu-id="eb708-119">Create the SLA group by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup>
                -MaxNumberOfCalls <Number> -BusyOption
                <BusyOnBusy|Voicemail|Forward> [-Target
                <TargetUserOrPhoneNumber>]
    ```
    <span data-ttu-id="eb708-p104">Set-CsSlaConfiguration cmdlet 会将企业语音帐户 SLAGroup1 标记为 SLA 实体，并且 SLAGroup1 的号码将变为 SLA 组的号码。对 SLAGroup1 的所有呼叫将拨打整个 SLA 组。</span><span class="sxs-lookup"><span data-stu-id="eb708-p104">The Set-CsSlaConfiguration cmdlet marks the Enterprise Voice account SLAGroup1 as an SLA entity, and the number of SLAGroup1 becomes the number for the SLA group. All calls to SLAGroup1 will ring the entire SLA group.</span></span>
    
    <span data-ttu-id="eb708-122">以下示例将为现有企业语音用户创建 SLA 组 SLAGroup1，并使用为 SLAGroup1 分配的号码作为 SLA 主线路号码。</span><span class="sxs-lookup"><span data-stu-id="eb708-122">The following example creates an SLA group for an existing Enterprise Voice user, SLAGroup1, and uses the number assigned for SLAGroup1 as the SLA mainline number.</span></span>
    
    <span data-ttu-id="eb708-123">命令会将新 SLA 组的最大并发呼叫数设置为 3，超过该数目的呼叫将听到忙音信号：</span><span class="sxs-lookup"><span data-stu-id="eb708-123">The command sets the maximum number of concurrent calls for the new SLA group to 3, and for calls in excess of that to hear a busy signal:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -MaxNumberOfCalls 3
                -BusyOption BusyOnBusy
    ```
    <span data-ttu-id="eb708-124">您可以使用 Set-CsSlaConfiguration 创建新的 SLA 组或修改现有 SLA 组。</span><span class="sxs-lookup"><span data-stu-id="eb708-124">You can use Set-CsSlaConfiguration to create a new SLA group or modify an existing one.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="eb708-125">请注意，为指定的内容 <CODE>-Identity</CODE> 必须是有效的现有企业语音的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="eb708-125">Note that what you specify for <CODE>-Identity</CODE> must be a valid existing Enterprise Voice-enabled user account.</span></span>

    
    </div>

2.  <span data-ttu-id="eb708-126">使用 [Add-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/add-cssladelegates) cmdlet 向组添加代理人：</span><span class="sxs-lookup"><span data-stu-id="eb708-126">Add delegates to the group by using the [Add-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/add-cssladelegates) cmdlet:</span></span>
    ```powershell
    Add-CsSlaDelegates -Identity <IdentityOfGroup> -Delegate
              <NameOfDelegate@domain>
    ```
    <span data-ttu-id="eb708-127">以下示例将向 SLA 组添加一个用户。</span><span class="sxs-lookup"><span data-stu-id="eb708-127">The following example adds a user to the SLA group.</span></span> <span data-ttu-id="eb708-128">添加到该组的每个用户都必须是有效的企业语音支持的用户：</span><span class="sxs-lookup"><span data-stu-id="eb708-128">Each user added to the group must be a valid Enterprise Voice-enabled user:</span></span>
    ```powershell
    Add-CsSlaDelegates -Identity SLAGroup1 -Delegate
              sip:SLA_Delegate1@contoso.com
    ```
    <span data-ttu-id="eb708-p106">对要添加到组的每个用户重复该 cmdlet。用户只能属于单个 SLA 组。</span><span class="sxs-lookup"><span data-stu-id="eb708-p106">Repeat the cmdlet for each user you want to add to the group. Users can only belong to a single SLA group.</span></span>

</div>

<div>

## <a name="configure-the-sla-group-busy-option"></a><span data-ttu-id="eb708-131">配置 SLA 组忙碌选项</span><span class="sxs-lookup"><span data-stu-id="eb708-131">Configure the SLA group Busy Option</span></span>

1.  <span data-ttu-id="eb708-132">使用 [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet 配置 SLA 组忙碌选项：</span><span class="sxs-lookup"><span data-stu-id="eb708-132">Configure the SLA group Busy Option by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup>
              -BusyOption <Option> [-Target <TargetUserOrPhoneNumber>]
    ```
    <span data-ttu-id="eb708-133">以下示例会将超过最大并发呼叫数的呼叫设置为转接到电话号码 202-555-1234。</span><span class="sxs-lookup"><span data-stu-id="eb708-133">The following example sets calls that exceed the maximum number of concurrent calls to be forwarded to the telephone number 202-555-1234.</span></span> <span data-ttu-id="eb708-134">目标可以是组织中的用户，而不是电话号码;在这种情况下，接收转接呼叫的用户的语法与您指定代理人时的语法相同： `sip:<NameofDelegate@domain>` 。</span><span class="sxs-lookup"><span data-stu-id="eb708-134">The target could be a user in your organization instead of a phone number; in that case, the syntax for the person to receive the forwarded calls is the same as when you specify a delegate: `sip:<NameofDelegate@domain>`.</span></span> <span data-ttu-id="eb708-135">的另一个可能的参数 `BusyOption` 是 `Voicemail` ：</span><span class="sxs-lookup"><span data-stu-id="eb708-135">The other possible parameter for `BusyOption` is `Voicemail`:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -BusyOption Forward
              -Target tel:+2025551234]
    ```
</div>

<div>

## <a name="configure-the-sla-group-missed-call-option"></a><span data-ttu-id="eb708-136">配置 SLA 组未接来电选项</span><span class="sxs-lookup"><span data-stu-id="eb708-136">Configure the SLA group Missed Call Option</span></span>

1.  <span data-ttu-id="eb708-137">使用 [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet 配置 SLA 组未接来电选项：</span><span class="sxs-lookup"><span data-stu-id="eb708-137">Configure the SLA group Missed Call Option by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup> 
              -MissedCallOption <Option> -MissedCallForwardTarget
              <TargetUserOrPhoneNumber> -BusyOption <Option> -MaxNumberofCalls <#> -Target [Target]
    ```
    <span data-ttu-id="eb708-138">以下示例指定将未接来电转发到名为的用户 `sla_forward_number` 。</span><span class="sxs-lookup"><span data-stu-id="eb708-138">The following example specifies that missed calls are to be forwarded to the user named `sla_forward_number`.</span></span> <span data-ttu-id="eb708-139">参数的有效选项为 `-MissedCallOption` `Forward` 、 `BusySignal` 或 `Disconnect` 。</span><span class="sxs-lookup"><span data-stu-id="eb708-139">The valid options for the `-MissedCallOption` parameter are `Forward`, `BusySignal`, or `Disconnect`.</span></span> <span data-ttu-id="eb708-140">如果选择 `Forward` ""，则还必须包括 `-MissedCallForwardTarget` 参数，将用户或电话号码用作目标：</span><span class="sxs-lookup"><span data-stu-id="eb708-140">If you choose `Forward`, you must also include the `-MissedCallForwardTarget` parameter, with a user or phone number as the target:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -MissedCallOption
              Forward -MissedCallForwardTarget sip:sla_forward_number@contoso.com 
        -BusyOption Forward -MaxNumberOfCalls 2 -Target sip:sla_forward_number@contoso.com 
    ```
</div>

<div>

## <a name="remove-a-delegate-from-a-group"></a><span data-ttu-id="eb708-141">从组中删除代理人</span><span class="sxs-lookup"><span data-stu-id="eb708-141">Remove a delegate from a group</span></span>

1.  <span data-ttu-id="eb708-142">使用 [Remove-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/remove-cssladelegates) cmdlet 从组中删除代理人：</span><span class="sxs-lookup"><span data-stu-id="eb708-142">Remove a delegate from a group by using the [Remove-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/remove-cssladelegates) cmdlet:</span></span>
    ```powershell
    Remove-CsSlaDelegates -Identity <IdentityOfGroup> -Delegate
              <NameOfDelegate@domain>
    ```
    <span data-ttu-id="eb708-143">例如：</span><span class="sxs-lookup"><span data-stu-id="eb708-143">For example:</span></span>
    ```powershell
    Remove-CsSlaDelegates -Identity SLAGroup1 -Delegate
              sip:SLA_Delegate3@contoso.com
    ```
</div>

<div>

## <a name="delete-an-sla-group"></a><span data-ttu-id="eb708-144">删除 SLA 组</span><span class="sxs-lookup"><span data-stu-id="eb708-144">Delete an SLA group</span></span>

1.  <span data-ttu-id="eb708-145">使用 [Remove-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/remove-csslaconfiguration?view=skype-ps) cmdlet 删除 SLA 组：</span><span class="sxs-lookup"><span data-stu-id="eb708-145">Delete an SLA group by using the [Remove-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/remove-csslaconfiguration?view=skype-ps) cmdlet:</span></span>
    
    ```powershell
    Remove-CsSlaConfiguration -Identity <IdentityOfGroup>
              
    ```
    
    <span data-ttu-id="eb708-146">例如：</span><span class="sxs-lookup"><span data-stu-id="eb708-146">For example:</span></span>
    ```powershell
    Remove-CsSlaConfiguration -Identity SLAGroup1 
    ```
<span data-ttu-id="eb708-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb708-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

