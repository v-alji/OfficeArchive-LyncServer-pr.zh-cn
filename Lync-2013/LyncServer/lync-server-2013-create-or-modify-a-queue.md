---
title: Lync Server 2013：创建或修改队列
description: Lync Server 2013：创建或修改队列。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a queue
ms:assetid: b9d6366a-839f-4651-a01d-9254546cadeb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205207(v=OCS.15)
ms:contentKeyID: 48185247
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbd8d6d00df8d6a09ef5861d876bd1363db09e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431752"
---
# <a name="create-or-modify-a-queue-in-lync-server-2013"></a><span data-ttu-id="ee606-103">在 Lync Server 2013 中创建或修改队列</span><span class="sxs-lookup"><span data-stu-id="ee606-103">Create or modify a queue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee606-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee606-104">

<span> </span></span></span>

<span data-ttu-id="ee606-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ee606-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ee606-106">使用以下其中一个过程来创建或修改队列。</span><span class="sxs-lookup"><span data-stu-id="ee606-106">Use one of the following procedures to create or modify a queue.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-create-or-modify-a-queue"></a><span data-ttu-id="ee606-107">使用 Lync Server "控制面板" 创建或修改队列</span><span class="sxs-lookup"><span data-stu-id="ee606-107">To use Lync Server Control Panel to create or modify a queue</span></span>

1.  <span data-ttu-id="ee606-108">以 RTCUniversalServerAdmins 组成员的身份，或支持响应组的某个预定义管理角色的成员身份登录。</span><span class="sxs-lookup"><span data-stu-id="ee606-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee606-109">如果您是托管工作流的委派响应组管理员之一，则可以创建或修改响应组队列，并将其分配给您管理的工作流。</span><span class="sxs-lookup"><span data-stu-id="ee606-109">If you are one of the delegated Response Group Managers for a managed workflow, you can create or modify response group queues and assign them to the workflows that you manage.</span></span>

    
    </div>

2.  <span data-ttu-id="ee606-110">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="ee606-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ee606-111">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="ee606-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ee606-112">在左侧导航栏中，单击“响应组”，然后单击“队列”。</span><span class="sxs-lookup"><span data-stu-id="ee606-112">In the left navigation bar, click **Response Groups**, and then click **Queue**.</span></span>

4.  <span data-ttu-id="ee606-113">在“队列”页上，请执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="ee606-113">On the **Queue** page, do one of the following:</span></span>
    
      - <span data-ttu-id="ee606-114">要创建新队列，请单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ee606-114">To create a new queue, click **New**.</span></span> <span data-ttu-id="ee606-115">在“选择服务”中，键入要在搜索字段中添加队列的 **ApplicationServer** 服务的部分或全部名称。</span><span class="sxs-lookup"><span data-stu-id="ee606-115">In **Select a Service**, type part or all of the name of the **ApplicationServer** service where you want to add the queue in the search field.</span></span> <span data-ttu-id="ee606-116">在服务结果列表中，单击想要的服务，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee606-116">In the resulting list of services, click the service that you want, and then click **OK**.</span></span>
    
      - <span data-ttu-id="ee606-p103">要修改现有的队列，请在搜索字段中键入全部或部分队列名称。在队列结果列表中，单击想要的队列，再单击“编辑”，然后单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="ee606-p103">To modify an existing queue, type all or part of the queue name in the search field. In the resulting list of queues, click the queue that you want, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="ee606-119">在“名称”中，键入队列的识别名称。</span><span class="sxs-lookup"><span data-stu-id="ee606-119">In **Name**, type an identifying name for the queue.</span></span>

6.  <span data-ttu-id="ee606-120">在“说明”中，键入队列的说明。</span><span class="sxs-lookup"><span data-stu-id="ee606-120">In **Description**, type a description for the queue.</span></span>

7.  <span data-ttu-id="ee606-p104">在“组”中，指定要分配给队列的组。请执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="ee606-p104">In **Groups**, specify the groups you want to assign to the queue. Do one of the following:</span></span>
    
      - <span data-ttu-id="ee606-p105">要将组添加到队列，请单击“选择”。在“选择组”搜索字段中，键入要分配给队列的代理组的全部或部分名称，单击想要的代理组，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee606-p105">To add a group to the queue, click **Select**. In the **Select Groups** search field, type all or part of the name of the agent group that you want to assign to the queue, click the agent group that you want, and then click **OK**.</span></span>
    
      - <span data-ttu-id="ee606-125">要从队列中删除组，在代理组列表中，请单击要删除的组，然后单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="ee606-125">To remove a group from the queue, in the list of agent groups, click the group that you want to remove, and then click **Remove**.</span></span>
    
      - <span data-ttu-id="ee606-126">要更改代理的搜索顺序，在代理组列表中，请单击某个组，然后单击向上箭头或向下箭头。</span><span class="sxs-lookup"><span data-stu-id="ee606-126">To change the order in which agents are searched, in the list of agent groups, click a group, and then click the up arrow or down arrow.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="ee606-p106">服务器搜索队列的可用代理时，将使用组顺序。即，首先搜索列表中的第一个组，然后搜索列表中的第二个组，依此类推。</span><span class="sxs-lookup"><span data-stu-id="ee606-p106">When the server searches for an available agent for the queue, it uses group order. That is, the first group in the list is searched first, followed by the second group in the list, and so on.</span></span>

        
        </div>

8.  <span data-ttu-id="ee606-129">要指定代理应答呼叫之前呼叫者处于保持状态的最大时间长度，请选中“启用队列超时”复选框，然后执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="ee606-129">To specify a maximum period of time for a caller to wait on hold before an agent answers the call, select the **Enable queue time-out** check box, and then do the following:</span></span>
    
    1.  <span data-ttu-id="ee606-130">在“超时时段(秒)”中，指定呼叫者等待代理应答呼叫的最长时间（秒）。</span><span class="sxs-lookup"><span data-stu-id="ee606-130">In **Time-out period (seconds)**, specify the maximum number of seconds a caller waits for an agent to answer the call.</span></span>
    
    2.  <span data-ttu-id="ee606-131">在“呼叫操作”中，选择呼叫超时时执行的操作（如下所示）：</span><span class="sxs-lookup"><span data-stu-id="ee606-131">In **Call Action**, select the action that occurs when a call times out as follows:</span></span>
    
    <!-- end list -->
    
      - <span data-ttu-id="ee606-132">要在超时后断开呼叫，请单击“断开连接”。</span><span class="sxs-lookup"><span data-stu-id="ee606-132">To disconnect the call after the timeout, click **Disconnect**.</span></span>
    
      - <span data-ttu-id="ee606-133">若要将呼叫转移到语音邮件，请单击 "**转发到语音邮件**"，然后在 " **sip 地址**" 字段中键入 sip 的语音邮件地址： \<username\> @ \<domainname\> (例如，sip:bob@contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="ee606-133">To forward the call to voice mail, click **Forward to voice mail**, and then in the **SIP address** field, type a voice mail address in the format sip:\<username\>@\<domainname\> (for example, sip:bob@contoso.com).</span></span>
    
      - <span data-ttu-id="ee606-134">若要将呼叫转移到另一个电话号码，请单击 "**转发到电话号码**"，然后在 " **sip 地址**" 字段中，键入 sip 的格式的电话号码： \<number\> @ \<domainname\> (例如，sip:+14255550121@contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="ee606-134">To forward the call to another telephone number, click **Forward to telephone number**, and then in the **SIP address** field, type the telephone number in the format sip:\<number\>@\<domainname\> (for example, sip:+14255550121@contoso.com).</span></span>
    
      - <span data-ttu-id="ee606-135">若要将呼叫转移到其他用户，请单击 "**转发到 sip 地址**"，然后在 " **sip 地址**" 字段中，键入 sip 的格式的用户 URI： \<username\> @ \<domainname\> 。</span><span class="sxs-lookup"><span data-stu-id="ee606-135">To forward the call to another user, click **Forward to SIP address**, and then in the **SIP address** field, type the URI for the user in the format sip:\<username\>@\<domainname\>.</span></span>
    
      - <span data-ttu-id="ee606-136">要将呼叫转接到其他队列，请单击“转接到其他队列”，然后浏览至要使用的队列。</span><span class="sxs-lookup"><span data-stu-id="ee606-136">To forward the call to another queue, click **Forward to another queue**, and then browse to the queue that you want to use.</span></span>

9.  <span data-ttu-id="ee606-137">要指定队列可以容纳的最大呼叫数，请选中“启用队列溢出”复选框，然后执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="ee606-137">To specify a maximum number of calls that the queue can hold, select the **Enable queue overflow** check box, and then do the following:</span></span>
    
    1.  <span data-ttu-id="ee606-138">在“最大呼叫数”中，选择希望队列容纳的最大呼叫数。</span><span class="sxs-lookup"><span data-stu-id="ee606-138">In **Maximum number of calls**, select the maximum number of calls that you want the queue to hold.</span></span>
    
    2.  <span data-ttu-id="ee606-139">在“转接呼叫”中，选择队列已满时要转接的呼叫：“最新呼叫”或“最早呼叫”。</span><span class="sxs-lookup"><span data-stu-id="ee606-139">In **Forward the call**, select which call is to be forwarded when the queue is full: **Newest Call** or **Oldest Call**.</span></span>
    
    3.  <span data-ttu-id="ee606-140">在“呼叫操作”中，选择达到溢出阈值时要执行的操作，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ee606-140">In **Call action**, select the action that occurs when the overflow threshold is met as follows:</span></span>
    
    <!-- end list -->
    
      - <span data-ttu-id="ee606-141">要在超时后断开呼叫，请单击“断开连接”。</span><span class="sxs-lookup"><span data-stu-id="ee606-141">To disconnect the call after the timeout, click **Disconnect**.</span></span>
    
      - <span data-ttu-id="ee606-142">若要将呼叫转移到语音邮件，请单击 "**转发到语音邮件**"，然后在 " **sip 地址**" 字段中键入 sip 的语音邮件地址： \<username\> @ \<domainname\> (例如，sip:bob@contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="ee606-142">To forward the call to voice mail, click **Forward to voice mail**, and then in the **SIP address** field, type a voice mail address in the format sip:\<username\>@\<domainname\> (for example, sip:bob@contoso.com).</span></span>
    
      - <span data-ttu-id="ee606-143">若要将呼叫转移到另一个电话号码，请单击 "**转发到电话号码**"，然后在 " **sip 地址**" 字段中，键入 sip 的格式的电话号码： \<number\> @ \<domainname\> (例如，sip:+14255550121@contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="ee606-143">To forward the call to another telephone number, click **Forward to telephone number**, and then in the **SIP address** field, type the telephone number in the format sip:\<number\>@\<domainname\> (for example, sip:+14255550121@contoso.com).</span></span>
    
      - <span data-ttu-id="ee606-144">若要将呼叫转移到其他用户，请单击 "**转发到 sip 地址**"，然后在 " **sip 地址**" 字段中，键入 sip 的格式的用户 URI： \<username\> @ \<domainname\> 。</span><span class="sxs-lookup"><span data-stu-id="ee606-144">To forward the call to another user, click **Forward to SIP address**, and then in the **SIP address** field, type the URI for the user in the format sip:\<username\>@\<domainname\>.</span></span>
    
      - <span data-ttu-id="ee606-145">要将呼叫转接到其他队列，请单击“转接到其他队列”，然后浏览至要使用的队列。</span><span class="sxs-lookup"><span data-stu-id="ee606-145">To forward the call to another queue, click **Forward to another queue**, and then browse to the queue that you want to use.</span></span>

10. <span data-ttu-id="ee606-146">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="ee606-146">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-create-or-modify-a-queue"></a><span data-ttu-id="ee606-147">使用 Windows PowerShell 创建或修改队列</span><span class="sxs-lookup"><span data-stu-id="ee606-147">To use Windows PowerShell to create or modify a queue</span></span>

1.  <span data-ttu-id="ee606-148">以 RTCUniversalServerAdmins 组成员的身份，或支持响应组的某个预定义管理角色的成员身份登录。</span><span class="sxs-lookup"><span data-stu-id="ee606-148">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee606-149">如果您是托管工作流的委派响应组管理员，您将能够创建代理组和队列并将代理组分配给队列。</span><span class="sxs-lookup"><span data-stu-id="ee606-149">If you are one of the delegated Response Group Managers for a managed workflow, you will be able to create agent groups and queues, and assign agent groups to queues.</span></span>

    
    </div>

2.  <span data-ttu-id="ee606-150">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="ee606-150">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ee606-p107">创建在达到队列超时阈值时要显示的提示，并将其保存在变量中。在命令行中运行：</span><span class="sxs-lookup"><span data-stu-id="ee606-p107">Create the prompt to be played when the queue timeout threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $promptTO = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="ee606-153">例如：</span><span class="sxs-lookup"><span data-stu-id="ee606-153">For example:</span></span>
    
        "All agents are currently busy. Please call back later."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee606-154">要针对提示使用音频文件，请使用 <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee606-154">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="ee606-155">有关详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">导入-CsRgsAudioFile</A>。</span><span class="sxs-lookup"><span data-stu-id="ee606-155">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="ee606-p109">定义在达到队列超时阈值时要采取的操作，并将其保存在变量中。在命令行中运行：</span><span class="sxs-lookup"><span data-stu-id="ee606-p109">Define the action to be taken when the queue timeout threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $actionTO = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee606-158">有关可能的操作及其语法的详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">CsRgsCallAction</A>。</span><span class="sxs-lookup"><span data-stu-id="ee606-158">For details about possible actions and their syntax, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">New-CsRgsCallAction</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="ee606-159">例如：</span><span class="sxs-lookup"><span data-stu-id="ee606-159">For example:</span></span>
    
        $action = New-CsRgsCallAction -Prompt $promptTO -Action Terminate

5.  <span data-ttu-id="ee606-p110">创建在达到队列溢出阈值时要显示的提示，并将其保存在变量中。在命令行中运行：</span><span class="sxs-lookup"><span data-stu-id="ee606-p110">Create the prompt to be played when the queue overflow threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $promptOV = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="ee606-162">例如：</span><span class="sxs-lookup"><span data-stu-id="ee606-162">For example:</span></span>
    
        $promptOV = New-CsRgsPrompt -TextToSpeechPrompt "Too many calls are waiting. Please call back later."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee606-163">要针对提示使用音频文件，请使用 <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee606-163">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="ee606-164">有关详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">导入-CsRgsAudioFile</A>。</span><span class="sxs-lookup"><span data-stu-id="ee606-164">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

6.  <span data-ttu-id="ee606-p112">定义在达到队列溢出阈值时要采取的操作，并将其保存在变量中。在命令行中运行：</span><span class="sxs-lookup"><span data-stu-id="ee606-p112">Define the action to be taken when the queue overflow threshold is met, and save it in a variable. At the command line, run:</span></span>
    
        $actionOV = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee606-167">有关可能的操作及其语法的详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">CsRgsCallAction</A>。</span><span class="sxs-lookup"><span data-stu-id="ee606-167">For details about possible actions and their syntax, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction">New-CsRgsCallAction</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="ee606-168">例如：</span><span class="sxs-lookup"><span data-stu-id="ee606-168">For example:</span></span>
    
        $action = New-CsRgsCallAction -Prompt $promptOV -Action Terminate

7.  <span data-ttu-id="ee606-p113">检索响应组服务的服务名称，并将其分配到某个变量。在该命令行处，运行：</span><span class="sxs-lookup"><span data-stu-id="ee606-p113">Retrieve the service name for the Response Group service and assign it to a variable. At the command line, run:</span></span>
    
        $serviceId="service:"+(Get-CSService | ?{$_.Applications -Like "*RGS*"}).ServiceId;

8.  <span data-ttu-id="ee606-p114">获取要分配给队列的代理组的标识。在命令行中运行：</span><span class="sxs-lookup"><span data-stu-id="ee606-p114">Get the identity of the agent group to be assigned to the queue. At the command line, run:</span></span>
    
        $agid = (Get-CsRgsAgentGroup -Name "Help Desk").Identity;
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee606-173">有关创建代理组的详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsAgentGroup">新 CsRgsAgentGroup</A></span><span class="sxs-lookup"><span data-stu-id="ee606-173">For details about creating the agent group, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsAgentGroup">New-CsRgsAgentGroup</A></span></span>

    
    </div>

9.  <span data-ttu-id="ee606-p115">创建队列。在命令行中运行：</span><span class="sxs-lookup"><span data-stu-id="ee606-p115">Create the queue. At the command line, run:</span></span>
    
        $q = New-CsRgsQueue -Parent <saved service ID from previous step> -Name "<name of queue>" [-Description "<description for queue>"] [-TimeoutThreshold <# seconds before call times out>] [-TimeoutAction <saved timeout action>] [-OverflowThreshold <# calls queue can hold>] [-OverflowCandidate <call to be acted on when overflow threshold met>] [-OverflowAction <saved overflow action>] [-AgentGroupIDList(<agent group identity>)];
    
    <span data-ttu-id="ee606-176">例如：</span><span class="sxs-lookup"><span data-stu-id="ee606-176">For example:</span></span>
    
        $q = New-CsRgsQueue -Parent $serviceId -Name "Help Desk" -Description "Contoso Help Desk" -TimeoutThreshold 300 -TimeoutAction $actionTO -OverflowThreshold 10 -OverflowCandidate NewestCall -OverflowAction $actionOV -AgentGroupIDList($agid.Identity;

10. <span data-ttu-id="ee606-p116">确认已创建队列。运行：</span><span class="sxs-lookup"><span data-stu-id="ee606-p116">Confirm that the queue is created. Run:</span></span>
    
        Get-CsRgsQueue -Name "Help Desk"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ee606-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ee606-179">See Also</span></span>


[<span data-ttu-id="ee606-180">新-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="ee606-180">New-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue)  
[<span data-ttu-id="ee606-181">Set-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="ee606-181">Set-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsQueue)  
[<span data-ttu-id="ee606-182">New-CsRgsPrompt</span><span class="sxs-lookup"><span data-stu-id="ee606-182">New-CsRgsPrompt</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt)  
[<span data-ttu-id="ee606-183">新-CsRgsCallAction</span><span class="sxs-lookup"><span data-stu-id="ee606-183">New-CsRgsCallAction</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction)  
[<span data-ttu-id="ee606-184">CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="ee606-184">Get-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsQueue)  
[<span data-ttu-id="ee606-185">Import-CsRgsAudioFile</span><span class="sxs-lookup"><span data-stu-id="ee606-185">Import-CsRgsAudioFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile)  
[<span data-ttu-id="ee606-186">Remove-CsRgsQueue</span><span class="sxs-lookup"><span data-stu-id="ee606-186">Remove-CsRgsQueue</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsRgsQueue)  
  

<span data-ttu-id="ee606-187"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee606-187"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

