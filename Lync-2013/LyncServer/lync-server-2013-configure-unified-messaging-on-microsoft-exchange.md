---
title: Lync Server 2013：在 Microsoft Exchange 上配置统一消息
description: Lync Server 2013：在 Microsoft Exchange 上配置统一消息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Unified Messaging on Microsoft Exchange
ms:assetid: 07547968-c59b-4dde-ace4-9fd286933759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398129(v=OCS.15)
ms:contentKeyID: 48183311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8db43bbe50061a1a044bdd34b637ba86f626ca85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392458"
---
# <a name="configure-unified-messaging-on-microsoft-exchange-for-lync-server-2013"></a><span data-ttu-id="04d25-103">在 Microsoft Exchange for Lync Server 2013 上配置统一消息</span><span class="sxs-lookup"><span data-stu-id="04d25-103">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04d25-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04d25-104">

<span> </span></span></span>

<span data-ttu-id="04d25-105">_**主题上次修改时间：** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="04d25-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="04d25-106">本主题介绍了如何在 Microsoft Exchange Server 上配置 Exchange 统一消息 (UM) ，以便与企业语音配合使用。</span><span class="sxs-lookup"><span data-stu-id="04d25-106">This topic describes how to configure Exchange Unified Messaging (UM) on a Microsoft Exchange Server for use with Enterprise Voice.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="04d25-107">本主题中的 cmdlet 示例提供 exchange 2007 版本的 Exchange 命令行管理程序的语法。</span><span class="sxs-lookup"><span data-stu-id="04d25-107">The cmdlet examples in this topic provide syntax for the Exchange 2007 version of Exchange Management Shell.</span></span> <span data-ttu-id="04d25-108">如果您运行的是 Exchange 2010 或 Exchange 2013，请参阅参考的相应文档。</span><span class="sxs-lookup"><span data-stu-id="04d25-108">If you are running Exchange 2010 or Exchange 2013, see the appropriate documentation as referenced.</span></span>



</div>

<div>

## <a name="to-configure-a-server-running-exchange-server-um"></a><span data-ttu-id="04d25-109">配置运行 Exchange Server UM 的服务器</span><span class="sxs-lookup"><span data-stu-id="04d25-109">To configure a server running Exchange Server UM</span></span>

1.  <span data-ttu-id="04d25-110">为每个企业语音位置配置文件创建 UM 会话初始协议 (SIP) 统一资源标识符 (URI) 拨号计划。</span><span class="sxs-lookup"><span data-stu-id="04d25-110">Create a UM Session Initiation Protocol (SIP) Uniform Resource Identifier (URI) dial plan for each of your Enterprise Voice location profiles.</span></span> <span data-ttu-id="04d25-111">如果你选择使用 Exchange 管理控制台，请创建一个新的拨号计划，安全设置 **(首选)**。</span><span class="sxs-lookup"><span data-stu-id="04d25-111">If you choose to use the Exchange Management Console, create a new dial plan with the security setting **Secured (preferred)**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="04d25-112">如果将 "安全设置" 值设置为 " <STRONG>Sip 安全</STRONG> " 以仅要求 sip 通信加密，如之前建议的，请注意，如果前端池配置为要求加密，则拨号计划中的此安全设置不是足够的，这意味着池要求对 SIP 和 RTP 流量加密。</span><span class="sxs-lookup"><span data-stu-id="04d25-112">If you set your security setting value to <STRONG>SIP Secured</STRONG> to require encryption for SIP traffic only, as previously recommended, note that this security setting on a dial plan is insufficient if the Front End pool is configured to require encryption, which means the pool requires encryption for both SIP and RTP traffic.</span></span> <span data-ttu-id="04d25-113">当拨号计划和池安全设置不兼容时，从前端池中调用 Exchange UM 的所有呼叫都将失败，从而导致错误，表明您的 "安全设置不兼容"。</span><span class="sxs-lookup"><span data-stu-id="04d25-113">When the dial plan and pool security settings are not compatible, all calls to Exchange UM from the Front End pool will fail, resulting in an error indicating that you have an "Incompatible security setting."</span></span>

    
    </div>
    
    <span data-ttu-id="04d25-114">如果您使用的是 Exchange 命令行管理程序，请键入：</span><span class="sxs-lookup"><span data-stu-id="04d25-114">If you use the Exchange Management Shell, type:</span></span>
    ```powershell
     New-UMDialPlan -Name <dial plan name> -UriType "SipName" -VoipSecurity <SIPSecured|Unsecured|Secured> -NumberOfDigitsInExtension <number of digits> -AccessTelephoneNumbers <access number in E.164 format>
    ```
    <span data-ttu-id="04d25-115">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="04d25-115">For details, see:</span></span>
    
      - <span data-ttu-id="04d25-116">有关 Office 通信服务器2007，请参阅 "如何创建统一消息 SIP URI 拨号计划" [https://go.microsoft.com/fwlink/p/?LinkId=268632](https://go.microsoft.com/fwlink/p/?linkid=268632) 和 "新-UMDialplan： Exchange 2007 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268666](https://go.microsoft.com/fwlink/p/?linkid=268666) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-116">For Office Communications Server 2007, see "How to Create a Unified Messaging SIP URI Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268632](https://go.microsoft.com/fwlink/p/?linkid=268632) and "New-UMDialplan: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268666](https://go.microsoft.com/fwlink/p/?linkid=268666).</span></span>
    
      - <span data-ttu-id="04d25-117">对于 Exchange 2010，请参阅 "创建 UM 拨号计划" [https://go.microsoft.com/fwlink/p/?LinkId=268674](https://go.microsoft.com/fwlink/p/?linkid=268674) 和 "新-UMDialplan： Exchange 2010 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268680](https://go.microsoft.com/fwlink/p/?linkid=268680) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-117">For Exchange 2010, see "Create a UM Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268674](https://go.microsoft.com/fwlink/p/?linkid=268674) and "New-UMDialplan: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268680](https://go.microsoft.com/fwlink/p/?linkid=268680).</span></span>
    
      - <span data-ttu-id="04d25-118">有关 Exchange 2013，请参阅的 "统一消息" [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-118">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="04d25-119">选择的安全级别是 <STRONG>SIPSecured</STRONG> <STRONG>还是安全级别取决于</STRONG> 是否为媒体加密激活或停用) 安全的实时传输协议 (SRTP。</span><span class="sxs-lookup"><span data-stu-id="04d25-119">Whether you select a security level of <STRONG>SIPSecured</STRONG> or <STRONG>Secured</STRONG> depends on whether secure real-time transport protocol (SRTP) is activated or deactivated for media encryption.</span></span> <span data-ttu-id="04d25-120">对于 Lync Server 2010 与 Exchange UM 的集成，这应对应于 Lync Server 媒体配置中的加密级别。</span><span class="sxs-lookup"><span data-stu-id="04d25-120">For the Lync Server 2010 integration with Exchange UM, this should correspond to the encryption level in the Lync Server media configuration.</span></span> <span data-ttu-id="04d25-121">可通过运行 <STRONG>CsMediaConfiguration</STRONG> Cmdlet 查看 Lync Server 媒体配置。</span><span class="sxs-lookup"><span data-stu-id="04d25-121">The Lync Server media configuration can be viewed by running the <STRONG>Get-CsMediaConfiguration</STRONG> cmdlet.</span></span> <span data-ttu-id="04d25-122">有关详细信息，请参阅 Lync Server Management Shell 文档中的 Get-CsMediaConfiguration。</span><span class="sxs-lookup"><span data-stu-id="04d25-122">For details, see Get-CsMediaConfiguration in the Lync Server Management Shell documentation.</span></span><BR><span data-ttu-id="04d25-123">有关选择相应的 VoIP 安全设置的详细信息，请参阅 <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">集成本地统一消息和 Lync Server 2013 的部署过程</A>。</span><span class="sxs-lookup"><span data-stu-id="04d25-123">For details about selecting the appropriate VoIP Security setting, see <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="04d25-124">运行以下 cmdlet 以获取每个 UM 拨号计划 (FQDN) 的完全限定的域名：</span><span class="sxs-lookup"><span data-stu-id="04d25-124">Run the following cmdlet to obtain the fully qualified domain name (FQDN) for each UM dial plan:</span></span>
    
    ```powershell
    (Get-UMDialPlan <dialplanname>).PhoneContext  
    ```
    
    <span data-ttu-id="04d25-125">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="04d25-125">For details, see:</span></span>
    
      - <span data-ttu-id="04d25-126">有关 Exchange 2007，请参阅 "UMDialplan： Exchange 2007 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268678](https://go.microsoft.com/fwlink/p/?linkid=268678) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-126">For Exchange 2007, see "Get-UMDialplan: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268678](https://go.microsoft.com/fwlink/p/?linkid=268678).</span></span>
    
      - <span data-ttu-id="04d25-127">有关 Exchange 2010，请参阅 "UMDialplan： Exchange 2010 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268679](https://go.microsoft.com/fwlink/p/?linkid=268679) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-127">For Exchange 2010, see "Get-UMDialplan: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268679](https://go.microsoft.com/fwlink/p/?linkid=268679).</span></span>
    
      - <span data-ttu-id="04d25-128">有关 Exchange 2013，请参阅的 "统一消息" [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-128">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>

3.  <span data-ttu-id="04d25-129">记录每个 UM 拨号计划的拨号计划名称。</span><span class="sxs-lookup"><span data-stu-id="04d25-129">Record the dial plan name of each UM dial plan.</span></span> <span data-ttu-id="04d25-130">根据你的 Exchange Server 版本，你可能需要先使用每个拨号计划名称的 FQDN 作为每个 UM 拨号计划的相应 Lync 服务器拨号计划的名称，以便拨入计划名称匹配。</span><span class="sxs-lookup"><span data-stu-id="04d25-130">Depending on your version of Exchange Server, you may need to use the FQDN of each dial plan name later as the name of each UM dial plan’s corresponding Lync Server dial plan so that the dial plan names match.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="04d25-131">只有当 UM 拨号计划在 <EM>早</EM> 于 EXCHANGE 2010 SP1 的 exchange 版本上运行时，Lync Server 拨号计划名称才必须匹配 um 拨号计划名称。</span><span class="sxs-lookup"><span data-stu-id="04d25-131">Lync Server dial plan names must match UM dial plan names only if the UM dial plan is running on a version of Exchange <EM>earlier</EM> than Exchange 2010 SP1.</span></span>

    
    </div>

4.  <span data-ttu-id="04d25-132">将拨号计划添加到运行 Exchange UM 的服务器，如下所示：</span><span class="sxs-lookup"><span data-stu-id="04d25-132">Add the dial plan to the server running Exchange UM as follows:</span></span>
    
      - <span data-ttu-id="04d25-133">如果您选择使用 Exchange 管理控制台，则可以从服务器的属性表中添加拨号计划。</span><span class="sxs-lookup"><span data-stu-id="04d25-133">If you choose to use the Exchange Management Console, you can add the dial plan from the property sheet for the server.</span></span> <span data-ttu-id="04d25-134">有关特定说明，请参阅 Exchange Server 产品文档。</span><span class="sxs-lookup"><span data-stu-id="04d25-134">For specific instructions, see the Exchange Server product documentation.</span></span>
        
        <span data-ttu-id="04d25-135">对于 Exchange 2007，请参阅 "如何将统一消息服务器添加到拨号计划" [https://go.microsoft.com/fwlink/p/?LinkId=268681](https://go.microsoft.com/fwlink/p/?linkid=268681) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-135">For Exchange 2007, see "How to Add Unified Messaging Server to a Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268681](https://go.microsoft.com/fwlink/p/?linkid=268681).</span></span>
        
        <span data-ttu-id="04d25-136">对于 Exchange 2010，请参阅 "查看或配置 UM 服务器的属性" [https://go.microsoft.com/fwlink/p/?LinkId=268682](https://go.microsoft.com/fwlink/p/?linkid=268682) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-136">For Exchange 2010, see "View or Configure the Properties of a UM Server" at [https://go.microsoft.com/fwlink/p/?LinkId=268682](https://go.microsoft.com/fwlink/p/?linkid=268682).</span></span>
        
        <span data-ttu-id="04d25-137">有关 Exchange 2013，请参阅的 "统一消息" [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-137">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>
    
      - <span data-ttu-id="04d25-138">如果您使用的是 Exchange 命令行管理程序，请为您的每个 Exchange UM 服务器运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="04d25-138">If you use the Exchange Management Shell, run the following for each of your Exchange UM servers:</span></span>
        ```powershell
        $ums=get-umserver; 
        $dp=get-umdialplan -id <name of dial-plan created in step 1>; 
        $ums[0].DialPlans +=$dp.Identity; 
        set-umservice -instance $ums[0]
        ```
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="04d25-139">在执行以下步骤之前，请确保所有企业语音用户均已配置了 Exchange Server 邮箱。</span><span class="sxs-lookup"><span data-stu-id="04d25-139">Before you perform the following step, make sure that all Enterprise Voice users have been configured with an Exchange Server mailbox.</span></span><BR><span data-ttu-id="04d25-140">有关 Exchange 2007，请参阅中的 Exchange Server 2007 TechNet 库 <A href="https://go.microsoft.com/fwlink/p/?linkid=268685">https://go.microsoft.com/fwlink/p/?LinkId=268685</A> 。</span><span class="sxs-lookup"><span data-stu-id="04d25-140">For Exchange 2007, see the Exchange Server 2007 TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=268685">https://go.microsoft.com/fwlink/p/?LinkId=268685</A>.</span></span><BR><span data-ttu-id="04d25-141">有关 Exchange 2010，请参阅中的 Exchange Server 2010 TechNet 库 <A href="https://go.microsoft.com/fwlink/p/?linkid=268686">https://go.microsoft.com/fwlink/p/?LinkId=268686</A> 。</span><span class="sxs-lookup"><span data-stu-id="04d25-141">For Exchange 2010, see the Exchange Server 2010 TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=268686">https://go.microsoft.com/fwlink/p/?LinkId=268686</A>.</span></span><BR><span data-ttu-id="04d25-142">为在步骤1中创建的每个拨号计划指定邮箱策略时，请选择默认策略或已创建的策略。</span><span class="sxs-lookup"><span data-stu-id="04d25-142">When specifying a mailbox policy for each dial plan that you created in step 1, select either the default policy or one that you have created.</span></span>

    
    </div>

5.  <span data-ttu-id="04d25-143">导航到 \<Exchange installation directory\> \\ "脚本"，然后如果在单个林中部署了 Exchange，请键入：</span><span class="sxs-lookup"><span data-stu-id="04d25-143">Navigate to \<Exchange installation directory\>\\Scripts, and then if Exchange is deployed in a single forest, type:</span></span>
    ```console
    exchucutil.ps1
    ```
    <span data-ttu-id="04d25-144">或者，如果 Exchange 是在多个目录林中部署的，请键入：</span><span class="sxs-lookup"><span data-stu-id="04d25-144">Or, if Exchange is deployed in multiple forests, type:</span></span>
    ```console
    exchucutil.ps1 -Forest:"<forest FQDN>"
    ```
    <span data-ttu-id="04d25-145">其中，林 FQDN 指定了在其中部署 Lync 服务器的林。</span><span class="sxs-lookup"><span data-stu-id="04d25-145">where forest FQDN specifies the forest in which Lync Server is deployed.</span></span>
    
    <span data-ttu-id="04d25-146">如果您有一个或多个与多个 IP 网关相关联的 UM 拨号计划，请继续执行步骤6。</span><span class="sxs-lookup"><span data-stu-id="04d25-146">If you have one or more UM dial plans that are associated with multiple IP gateways, continue to step 6.</span></span> <span data-ttu-id="04d25-147">如果您的拨号计划仅与单个 IP 网关相关联，请跳过步骤6。</span><span class="sxs-lookup"><span data-stu-id="04d25-147">If your dial plans are each associated with only a single IP gateway, skip step 6.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="04d25-148">请确保在运行 exchucutil.ps1<EM>后</EM>重新启动<STRONG>Lync Server 前端</STRONG>服务 ( # A0) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-148">Be sure to restart the <STRONG>Lync Server Front-End</STRONG> service (rtcsrv.exe) <EM>after</EM> you run exchucutil.ps1.</span></span> <span data-ttu-id="04d25-149">否则，Lync Server 将不会检测拓扑中的统一消息。</span><span class="sxs-lookup"><span data-stu-id="04d25-149">Otherwise, Lync Server will not detect Unified Messaging in the topology.</span></span>

    
    </div>

6.  <span data-ttu-id="04d25-150">使用 Exchange 命令行管理程序或 Exchange 管理控制台，禁用除了一个与每个拨号计划关联的 IP 网关之外的所有其他 IP 网关的出站呼叫。</span><span class="sxs-lookup"><span data-stu-id="04d25-150">Using either the Exchange Management Shell or Exchange Management Console, disable outbound calling for all but one of the IP gateways associated with each of your dial plans.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="04d25-151">必须执行此步骤，以确保由运行 Exchange Server 统一消息的服务器与外部用户进行的出站调用 (例如，使用手机情况) 可靠地遍历企业防火墙的情况。</span><span class="sxs-lookup"><span data-stu-id="04d25-151">This step is necessary to make sure that outbound calls by the server running Exchange Server Unified Messaging to external users (for example, as is the case with play-on-phone scenarios) reliably traverse the corporate firewall.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="04d25-152">选择允许传出呼叫的 UM IP 网关时，选择可能处理最多流量的 UM IP 网关。</span><span class="sxs-lookup"><span data-stu-id="04d25-152">When selecting the UM IP gateway through which to allow outgoing calls, choose the one that is likely to handle the most traffic.</span></span> <span data-ttu-id="04d25-153">不允许传出流量通过连接到 Lync Server 控制器池的 IP 网关。</span><span class="sxs-lookup"><span data-stu-id="04d25-153">Do not allow outgoing traffic through an IP gateway that connects to a pool of Lync Server Directors.</span></span> <span data-ttu-id="04d25-154">还要避免在另一个中心站点或分支站点中使用池。</span><span class="sxs-lookup"><span data-stu-id="04d25-154">Also avoid pools in another central site or a branch site.</span></span> <span data-ttu-id="04d25-155">你可以使用以下任一方法阻止传出呼叫通过 IP 网关传递：</span><span class="sxs-lookup"><span data-stu-id="04d25-155">You can use either of the following methods to block outgoing calls from passing through an IP gateway:</span></span>

    
    </div>
    
      - <span data-ttu-id="04d25-156">如果使用 Exchange 命令行管理程序，请通过运行以下命令禁用每个 IP 网关：</span><span class="sxs-lookup"><span data-stu-id="04d25-156">If you use the Exchange Management Shell, disable each IP gateway by running the following command:</span></span>
        ```powershell
        Set-UMIPGateway <gatewayname> -OutcallsAllowed $false
        ```
        <span data-ttu-id="04d25-157">对于 Exchange 2007，请参阅 "Set-UMIPGateway： Exchange 2007 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268687](https://go.microsoft.com/fwlink/p/?linkid=268687) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-157">For Exchange 2007, see "Set-UMIPGateway: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268687](https://go.microsoft.com/fwlink/p/?linkid=268687).</span></span>
        
        <span data-ttu-id="04d25-158">对于 Exchange 2010，请参阅 "Set-UMIPGateway： Exchange 2010 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268688](https://go.microsoft.com/fwlink/p/?linkid=268688) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-158">For Exchange 2010, see "Set-UMIPGateway: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268688](https://go.microsoft.com/fwlink/p/?linkid=268688).</span></span>
    
      - <span data-ttu-id="04d25-159">如果您使用的是 Exchange 管理控制台，请清除 " **允许通过此 IP 网关拨出呼叫** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="04d25-159">If you use the Exchange Management Console, clear the **Allow outgoing calls through this IP gateway** check box.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="04d25-160">如果你的 UM SIP URI 拨号计划仅与单个 IP 网关相关联，请不要通过此网关禁止传出呼叫。</span><span class="sxs-lookup"><span data-stu-id="04d25-160">If your UM SIP URI dial plan is associated with only a single IP gateway, do not disallow outgoing calls through this gateway.</span></span>

    
    </div>

7.  <span data-ttu-id="04d25-161">为每个 Lync Server 拨号计划创建 UM 自动助理。</span><span class="sxs-lookup"><span data-stu-id="04d25-161">Create a UM auto-attendant for each Lync Server dial plan.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="04d25-162">不要在自动助理的名称中包含任何空格。</span><span class="sxs-lookup"><span data-stu-id="04d25-162">Do not include any spaces in the name of the auto attendant.</span></span>

    
    </div>
    
    ```powershell
    New-umautoattendant -name <auto attendant name> -umdialplan < name of dial plan created in step 1> -PilotIdentifierList <auto attendant phone number in E.164 format> -SpeechEnabled $true -Status Enabled
    ```
    <span data-ttu-id="04d25-163">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="04d25-163">For details, see:</span></span>
    
      - <span data-ttu-id="04d25-164">有关 Exchange 2007，请参阅 "New-UMAutoAttendant： Exchange 2007 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268689](https://go.microsoft.com/fwlink/p/?linkid=268689) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-164">For Exchange 2007, see "New-UMAutoAttendant: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268689](https://go.microsoft.com/fwlink/p/?linkid=268689).</span></span>
    
      - <span data-ttu-id="04d25-165">有关 Exchange 2010，请参阅 "New-UMAutoAttendant： Exchange 2010 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268690](https://go.microsoft.com/fwlink/p/?linkid=268690) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-165">For Exchange 2010, see "New-UMAutoAttendant: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268690](https://go.microsoft.com/fwlink/p/?linkid=268690).</span></span>
    
    <span data-ttu-id="04d25-166">在已启用 "适用于企业语音的 Lync Server 用户" 并了解其 SIP Uri 之后，应为每个用户执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="04d25-166">The following step should be performed for each user after you have enabled Lync Server users for Enterprise Voice and know their SIP URIs.</span></span>

8.  <span data-ttu-id="04d25-167">将 Exchange UM 用户关联 (每个用户都应使用 Exchange 邮箱) 与 UM 拨号计划一起配置，并为每个用户创建 SIP URI。</span><span class="sxs-lookup"><span data-stu-id="04d25-167">Associate Exchange UM users (each of whom should be configured with an Exchange mail box) with the UM dial plan and create a SIP URI for each user.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="04d25-168">以下示例中的 <STRONG>SIPResourceIdentifier</STRONG> 必须是 Lync 服务器用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="04d25-168">The <STRONG>SIPResourceIdentifier</STRONG> in the following sample must be the SIP address of the Lync Server user.</span></span>

    
    </div>
    
    ```powershell
    enable-ummailbox -id <user name> -ummailboxpolicy <name of the mailbox policy for the dial plan created in step 1> -Extensions <extension> -SIPResourceIdentifier "<user name>@<full domain name>" -PIN <user pin>
    ```
    <span data-ttu-id="04d25-169">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="04d25-169">For details, see:</span></span>
    
      - <span data-ttu-id="04d25-170">对于 Exchange 2007，请参阅 "Enable-UMMailbox： Exchange 2007 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268691](https://go.microsoft.com/fwlink/p/?linkid=268691) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-170">For Exchange 2007, see "Enable-UMMailbox: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268691](https://go.microsoft.com/fwlink/p/?linkid=268691).</span></span>
    
      - <span data-ttu-id="04d25-171">对于 Exchange 2010，请参阅 "Enable-UMMailbox： Exchange 2010 帮助" [https://go.microsoft.com/fwlink/p/?LinkId=268692](https://go.microsoft.com/fwlink/p/?linkid=268692) 。</span><span class="sxs-lookup"><span data-stu-id="04d25-171">For Exchange 2010, see "Enable-UMMailbox: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268692](https://go.microsoft.com/fwlink/p/?linkid=268692).</span></span>

<span data-ttu-id="04d25-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04d25-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

