---
title: Lync Server 2013：删除工作流
description: Lync Server 2013：删除工作流。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a workflow
ms:assetid: 0469a6b8-ce1e-459b-bc3d-4c8adf2d97d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520944(v=OCS.15)
ms:contentKeyID: 48183274
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9a588a1dc0428660db95d4d492abbd1b157ca7a0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430649"
---
# <a name="delete-a-workflow-in-lync-server-2013"></a><span data-ttu-id="7d71f-103">在 Lync Server 2013 中删除工作流</span><span class="sxs-lookup"><span data-stu-id="7d71f-103">Delete a workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d71f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d71f-104">

<span> </span></span></span>

<span data-ttu-id="7d71f-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="7d71f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="7d71f-106">使用以下过程之一删除工作流。</span><span class="sxs-lookup"><span data-stu-id="7d71f-106">Use one of the following procedures to delete a workflow.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-delete-a-workflow"></a><span data-ttu-id="7d71f-107">使用 Lync Server "控制面板" 删除工作流</span><span class="sxs-lookup"><span data-stu-id="7d71f-107">To use Lync Server Control Panel delete a workflow</span></span>

1.  <span data-ttu-id="7d71f-108">以 RTCUniversalServerAdmins 组成员的身份，或支持响应组的某个预定义管理角色的成员身份登录。</span><span class="sxs-lookup"><span data-stu-id="7d71f-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="7d71f-109">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="7d71f-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7d71f-110">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="7d71f-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7d71f-111">在左侧导航栏中，单击“响应组”，然后单击“工作流”。</span><span class="sxs-lookup"><span data-stu-id="7d71f-111">In the left navigation bar, click **Response Groups**, and then click **Workflow**.</span></span>

4.  <span data-ttu-id="7d71f-112">在“工作流”页上，单击“创建或编辑工作流”。</span><span class="sxs-lookup"><span data-stu-id="7d71f-112">On the **Workflow** page, click **Create or edit a workflow**.</span></span>

5.  <span data-ttu-id="7d71f-113">在 " **选择服务** 搜索" 字段中，键入托管要删除的工作流的 **ApplicationServer** 服务的部分或所有名称。</span><span class="sxs-lookup"><span data-stu-id="7d71f-113">In the **Select a Service** search field, type part or all of the name of the **ApplicationServer** service that hosts the workflow that you want to delete.</span></span>

6.  <span data-ttu-id="7d71f-114">在服务列表中，单击所需的服务，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="7d71f-114">In the list of services, click the service that you want, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7d71f-115">此时将打开 "响应组配置工具" 网页。</span><span class="sxs-lookup"><span data-stu-id="7d71f-115">The Response Group Configuration Tool webpage opens.</span></span> <span data-ttu-id="7d71f-116">您还可以通过连接到 <STRONG>Https:// &lt; webPoolFqdn &gt; /RgsConfig</STRONG>，直接从 web 浏览器打开 "响应组配置" 工具网页。</span><span class="sxs-lookup"><span data-stu-id="7d71f-116">You can also open the Response Group Configuration Tool webpage directly from a web browser by connecting to <STRONG>https://&lt;webPoolFqdn&gt;/RgsConfig</STRONG>.</span></span>

    
    </div>

7.  <span data-ttu-id="7d71f-117">在 " **管理现有工作流**" 下，找到要删除的工作流，然后在 " **操作**" 下单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="7d71f-117">Under **Manage an Existing Workflow**, locate the workflow you want to delete, and then under **Action**, click **Delete**.</span></span>

8.  <span data-ttu-id="7d71f-118">单击“**是**”。</span><span class="sxs-lookup"><span data-stu-id="7d71f-118">Click **Yes**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-a-workflow"></a><span data-ttu-id="7d71f-119">使用 Windows PowerShell 删除工作流</span><span class="sxs-lookup"><span data-stu-id="7d71f-119">To use Windows PowerShell to delete a workflow</span></span>

1.  <span data-ttu-id="7d71f-120">以 RTCUniversalServerAdmins 组成员的身份，或支持响应组的某个预定义管理角色的成员身份登录。</span><span class="sxs-lookup"><span data-stu-id="7d71f-120">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="7d71f-121">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="7d71f-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7d71f-122">在命令行中运行：</span><span class="sxs-lookup"><span data-stu-id="7d71f-122">At the command line, run:</span></span>
    
        Get-CsRgsWorkflow -Identity <Application Server service> -Name "<name of workflow>" | Remove-CsRgsWorkflow
    
    <span data-ttu-id="7d71f-123">例如：</span><span class="sxs-lookup"><span data-stu-id="7d71f-123">For example:</span></span>
    
        Get-CsRgsWorkflow -Identity service:ApplicationServer:redmond.contoso.com -Name "Help Desk" | Remove-CsRgsWorkflow

<span data-ttu-id="7d71f-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d71f-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

