---
title: Lync Server 2013：创建或修改新的客户端版本策略规则
description: Lync Server 2013：创建或修改新的客户端版本策略规则。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a new client version policy rule
ms:assetid: 6f879d99-8401-41e0-a562-195c890d63ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ898478(v=OCS.15)
ms:contentKeyID: 50873758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11ebcf17d5cb14fd519fba8ad36be10894fabdb9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392158"
---
# <a name="create-or-modify-a-new-client-version-policy-rule-in-lync-server-2013"></a><span data-ttu-id="dcec3-103">在 Lync Server 2013 中创建或修改新的客户端版本策略规则</span><span class="sxs-lookup"><span data-stu-id="dcec3-103">Create or modify a new client version policy rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dcec3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dcec3-104">

<span> </span></span></span>

<span data-ttu-id="dcec3-105">_**主题上次修改时间：** 2013-01-21_</span><span class="sxs-lookup"><span data-stu-id="dcec3-105">_**Topic Last Modified:** 2013-01-21_</span></span>

<span data-ttu-id="dcec3-106">客户端版本策略规则定义当用户尝试使用特定客户端和客户端版本登录时应采取的操作。</span><span class="sxs-lookup"><span data-stu-id="dcec3-106">Client version policy rules define the actions that should be taken when users attempt to log on with specific clients and client versions.</span></span> <span data-ttu-id="dcec3-107">你可以从 Lync Server 2013 控制面板创建或修改客户端版本策略的单个规则。</span><span class="sxs-lookup"><span data-stu-id="dcec3-107">You can create or modify individual rules for a client version policy from Lync Server 2013 Control Panel.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="dcec3-108">规则按优先级顺序列出。</span><span class="sxs-lookup"><span data-stu-id="dcec3-108">Rules are listed in order of precedence.</span></span> <span data-ttu-id="dcec3-109">例如，如果你有允许运行版本1.5 的客户端连接的规则，然后是阻止运行2.0 之前的版本的客户端的规则，则将优先使用运行版本1.5 的客户端，并且允许运行版本的客户端进行连接。</span><span class="sxs-lookup"><span data-stu-id="dcec3-109">For example, if you have a rule that allows clients running version 1.5 to connect, followed by a rule that blocks clients running a version earlier than 2.0, the first rule takes precedence, and clients running version 1.5 are allowed to connect.</span></span>



</div>

<div>

## <a name="to-create-or-modify-client-version-policy-rules-with-lync-server-control-panel"></a><span data-ttu-id="dcec3-110">通过 Lync Server "控制面板" 创建或修改客户端版本策略规则</span><span class="sxs-lookup"><span data-stu-id="dcec3-110">To create or modify client version policy rules with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="dcec3-111">使用 Lync Server "控制面板"[在 Lync server 2013 中创建或修改新的客户端版本策略](lync-server-2013-create-or-modify-a-new-client-version-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="dcec3-111">[Create or modify a new client version policy in Lync Server 2013](lync-server-2013-create-or-modify-a-new-client-version-policy.md) with Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="dcec3-112">在 " **编辑客户端版本策略** " 页面上，执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="dcec3-112">On the **Edit Client Version Policy** page, do one of the following:</span></span>
    
      - <span data-ttu-id="dcec3-113">单击 " **新建** " 以创建新的客户端版本规则。</span><span class="sxs-lookup"><span data-stu-id="dcec3-113">Click **New** to create a new client version rule.</span></span>
    
      - <span data-ttu-id="dcec3-114">单击列表中某个已定义的客户端类型，然后单击 " **显示详细信息**"。</span><span class="sxs-lookup"><span data-stu-id="dcec3-114">Click one of the defined client types in the list, and then click **Show details**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dcec3-115">可以使用通配符指示客户端类型。</span><span class="sxs-lookup"><span data-stu-id="dcec3-115">You can use wildcards to indicate the client type.</span></span>

    
    </div>

3.  <span data-ttu-id="dcec3-116">在 " **用户代理**" 中，选择一种客户端类型。</span><span class="sxs-lookup"><span data-stu-id="dcec3-116">In **User agent**, select a client type.</span></span>

4.  <span data-ttu-id="dcec3-117">在 " **版本号**" 下，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="dcec3-117">Under **Version number**, do the following:</span></span>
    
      - <span data-ttu-id="dcec3-118">在 " **主要版本**" 中，键入与客户端的主要版本相对应的数字。</span><span class="sxs-lookup"><span data-stu-id="dcec3-118">In **Major version**, type the number that corresponds to the major release of the client.</span></span>
    
      - <span data-ttu-id="dcec3-119">在 " **次要版本**" 中，键入与客户端的次要版本相对应的数字。</span><span class="sxs-lookup"><span data-stu-id="dcec3-119">In **Minor version**, type the number that corresponds to the minor release of the client.</span></span>
    
      - <span data-ttu-id="dcec3-120">在 " **生成**" 中，键入与客户端的主要和次要版本相对应的数字。</span><span class="sxs-lookup"><span data-stu-id="dcec3-120">In **Build**, type the number that corresponds to the major and minor release of the client.</span></span>
    
      - <span data-ttu-id="dcec3-121">在 " **更新**" 中，键入与客户端更新的版本相对应的数字。</span><span class="sxs-lookup"><span data-stu-id="dcec3-121">In **Update**, type the number that corresponds to the updated release of the client.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dcec3-122">可以使用通配符指示客户端版本号。</span><span class="sxs-lookup"><span data-stu-id="dcec3-122">You can use wildcards to indicate the client version number.</span></span>

    
    </div>

5.  <span data-ttu-id="dcec3-123">若要为您在前面的步骤中指定的客户端版本指定匹配操作，请在 " **比较" 操作** 中，单击下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="dcec3-123">To specify the matching operation for the client version you specified in the preceding steps, in **Comparison operation**, click one of the following:</span></span>
    
      - <span data-ttu-id="dcec3-124">**相同**</span><span class="sxs-lookup"><span data-stu-id="dcec3-124">**Same as**</span></span>
    
      - <span data-ttu-id="dcec3-125">**不是**</span><span class="sxs-lookup"><span data-stu-id="dcec3-125">**Is not**</span></span>
    
      - <span data-ttu-id="dcec3-126">**更高**</span><span class="sxs-lookup"><span data-stu-id="dcec3-126">**Newer than**</span></span>
    
      - <span data-ttu-id="dcec3-127">**更高或相同**</span><span class="sxs-lookup"><span data-stu-id="dcec3-127">**Newer than or same as**</span></span>
    
      - <span data-ttu-id="dcec3-128">**更低**</span><span class="sxs-lookup"><span data-stu-id="dcec3-128">**Older than**</span></span>
    
      - <span data-ttu-id="dcec3-129">**更低或相同**</span><span class="sxs-lookup"><span data-stu-id="dcec3-129">**Older than or same as**</span></span>

6.  <span data-ttu-id="dcec3-130">若要指定在满足前面步骤中的条件时要执行的操作，请单击下列 **操作** 之一：</span><span class="sxs-lookup"><span data-stu-id="dcec3-130">To specify the action to perform when the criteria in the preceding steps are met, click one of the following in **Action**:</span></span>
    
      - <span data-ttu-id="dcec3-131">要允许客户登录，请单击 " **允许**"。</span><span class="sxs-lookup"><span data-stu-id="dcec3-131">To allow the client to log on, click **Allow**.</span></span>
    
      - <span data-ttu-id="dcec3-132">若要允许客户登录并接收来自 Windows Server 更新服务或 Microsoft 更新的更新，请单击 " **允许和升级**"。</span><span class="sxs-lookup"><span data-stu-id="dcec3-132">To allow the client to log on and receive updates from Windows Server Update Service or Microsoft Update, click **Allow and Upgrade**.</span></span> <span data-ttu-id="dcec3-133">仅当选择了 "用户代理 **OC** " 时，此操作才可用。</span><span class="sxs-lookup"><span data-stu-id="dcec3-133">This action is available only when user agent **OC** is selected.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="dcec3-134">选择此操作会导致在用户下次登录 Lync 2013 时显示通知。</span><span class="sxs-lookup"><span data-stu-id="dcec3-134">Selecting this action causes a notification to appear the next time users sign in to Lync 2013.</span></span> <span data-ttu-id="dcec3-135">该通知指出有可用更新，即使更新尚未发布到 Windows Server Update Service 或 Microsoft Update。</span><span class="sxs-lookup"><span data-stu-id="dcec3-135">The notification states that an update is available, even if updates have not yet been released to Windows Server Update Service or Microsoft Update.</span></span> <span data-ttu-id="dcec3-136">为了避免混淆，您只应在更新可用后选择此操作。</span><span class="sxs-lookup"><span data-stu-id="dcec3-136">To avoid confusion, you should choose this action only after updates become available.</span></span>

        
        </div>
    
      - <span data-ttu-id="dcec3-137">若要允许客户登录并显示有关从何处下载另一个客户端版本的消息，请单击 " **允许使用 URL**"。</span><span class="sxs-lookup"><span data-stu-id="dcec3-137">To allow the client to log on and display a message about where to download another client version, click **Allow with URL**.</span></span> <span data-ttu-id="dcec3-138">在此过程后面的部分中指定 URL。</span><span class="sxs-lookup"><span data-stu-id="dcec3-138">You specify the URL later in this procedure.</span></span>
    
      - <span data-ttu-id="dcec3-139">若要阻止客户端登录，请单击 " **阻止**"。</span><span class="sxs-lookup"><span data-stu-id="dcec3-139">To prevent the client from logging on, click **Block**.</span></span>
    
      - <span data-ttu-id="dcec3-140">若要阻止客户端登录并允许客户从 Windows Server 更新服务或 Microsoft 更新接收更新，请单击 " **阻止和升级**"。</span><span class="sxs-lookup"><span data-stu-id="dcec3-140">To prevent the client from logging on and allow the client to receive updates from Windows Server Update Service or Microsoft Update, click **Block and Upgrade**.</span></span> <span data-ttu-id="dcec3-141">仅当选择了 "用户代理 **OC** " 时，此操作才可用。</span><span class="sxs-lookup"><span data-stu-id="dcec3-141">This action is available only when user agent **OC** is selected.</span></span>
    
      - <span data-ttu-id="dcec3-142">若要阻止客户登录并显示有关从何处下载另一个客户端版本的消息，请单击 " **带 URL 阻止**"。</span><span class="sxs-lookup"><span data-stu-id="dcec3-142">To prevent the client from logging on and display a message about where to download another client version, click **Block with URL**.</span></span> <span data-ttu-id="dcec3-143">在此过程后面的部分中指定 URL。</span><span class="sxs-lookup"><span data-stu-id="dcec3-143">You specify the URL later in this procedure.</span></span>

7.  <span data-ttu-id="dcec3-144"> (可选) 如果在上一步中单击 " **允许 url** 或带 Url 的 **阻止** "，请键入要包含在 **url** 中的消息中的客户端下载 URL。</span><span class="sxs-lookup"><span data-stu-id="dcec3-144">(Optional) If you clicked **Allow with URL** or **Block with URL** in the previous step, type the client download URL to include in the message in **URL**.</span></span>

8.  <span data-ttu-id="dcec3-145">单击 **"确定**"，然后单击 " **提交**"。</span><span class="sxs-lookup"><span data-stu-id="dcec3-145">Click **OK**, and then click **Commit**.</span></span>

<span data-ttu-id="dcec3-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dcec3-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

