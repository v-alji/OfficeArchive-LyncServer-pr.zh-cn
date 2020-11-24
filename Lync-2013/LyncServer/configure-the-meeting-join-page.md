---
title: 配置与会页面
description: 配置会议加入页面。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure the meeting join page
ms:assetid: 036c9d03-ad95-4d63-a3d8-6cae1a8ad530
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204635(v=OCS.15)
ms:contentKeyID: 48183260
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af49a57a6844c59bf6f6631d996d8efe12152c52
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392056"
---
# <a name="configure-the-meeting-join-page"></a><span data-ttu-id="1255c-103">配置与会页面</span><span class="sxs-lookup"><span data-stu-id="1255c-103">Configure the meeting join page</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1255c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1255c-104">

<span> </span></span></span>

<span data-ttu-id="1255c-105">_**主题上次修改时间：** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="1255c-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="1255c-106">当用户单击会议请求中的会议链接时，会议加入页面检测是否已在用户的计算机上安装了 Lync 2013 客户端。</span><span class="sxs-lookup"><span data-stu-id="1255c-106">When a user clicks a meeting link in a meeting request, the meeting join page detects whether a Lync 2013 client is already installed on the user’s computer.</span></span> <span data-ttu-id="1255c-107">如果已安装客户端，该客户端将打开并加入会议。</span><span class="sxs-lookup"><span data-stu-id="1255c-107">If a client is already installed, that client opens and joins the meeting.</span></span> <span data-ttu-id="1255c-108">如果未安装客户端，则默认情况下将打开2013版本的 Lync Web App。</span><span class="sxs-lookup"><span data-stu-id="1255c-108">If a client is not installed, by default the 2013 version of Lync Web App opens.</span></span>

<span data-ttu-id="1255c-109">如果您希望允许用户通过 Office Communicator 2007 R2 或 Lync 2010 助理加入会议，则可以修改会议加入页面的行为。</span><span class="sxs-lookup"><span data-stu-id="1255c-109">You can modify the behavior of the meeting join page if you want to allow users to join meetings with Office Communicator 2007 R2 or Lync 2010 Attendant.</span></span> <span data-ttu-id="1255c-110">这些配置选项已从 Lync Server 2013 控制面板中删除，但你通过使用 CsWebServiceConfiguration cmdlet 进行配置。</span><span class="sxs-lookup"><span data-stu-id="1255c-110">These configuration options have been removed from the Lync Server 2013 Control Panel, but you configure them by using the CsWebServiceConfiguration cmdlet.</span></span>

### <a name="meeting-join-page-cswebserviceconfiguration-parameters"></a><span data-ttu-id="1255c-111">会议加入页 CsWebServiceConfiguration 参数</span><span class="sxs-lookup"><span data-stu-id="1255c-111">Meeting Join Page CsWebServiceConfiguration Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1255c-112">CsWebServiceConfiguration 参数</span><span class="sxs-lookup"><span data-stu-id="1255c-112">CsWebServiceConfiguration Parameter</span></span></th>
<th><span data-ttu-id="1255c-113">说明</span><span class="sxs-lookup"><span data-stu-id="1255c-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1255c-114">ShowJoinUsingLegacyClientLink</span><span class="sxs-lookup"><span data-stu-id="1255c-114">ShowJoinUsingLegacyClientLink</span></span></p></td>
<td><p><span data-ttu-id="1255c-115">如果设置为 True，则通过使用 Lync 之外的客户端应用程序加入会议的用户将有机会通过使用 Office Communicator 2007 R2 加入会议。</span><span class="sxs-lookup"><span data-stu-id="1255c-115">If set to True, users joining a meeting by using a client application other than Lync will be given the opportunity to join the meeting by using Office Communicator 2007 R2.</span></span> <span data-ttu-id="1255c-116">默认值为 False。</span><span class="sxs-lookup"><span data-stu-id="1255c-116">The default value is False.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1255c-117">ShowAlternateJoinOptionsExpanded</span><span class="sxs-lookup"><span data-stu-id="1255c-117">ShowAlternateJoinOptionsExpanded</span></span></p></td>
<td><p><span data-ttu-id="1255c-118">如果设置为 True，则用于加入联机会议 (（如 Office Communicator 2007 R2) ）的替代选项将自动展开并向用户显示。</span><span class="sxs-lookup"><span data-stu-id="1255c-118">When set to True then alternate options for joining an online conference (such as Office Communicator 2007 R2) will automatically be expanded and shown to users.</span></span> <span data-ttu-id="1255c-119">在设置为 False 时 (默认值) 这些选项将可用，但用户将必须显示其自身的选项列表。</span><span class="sxs-lookup"><span data-stu-id="1255c-119">When set to False (the default value) these options will be available, but the user will have to display the list of options for themselves.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-the-meeting-join-page-by-using-lync-server-2013-management-shell"></a><span data-ttu-id="1255c-120">使用 Lync Server 2013 命令行管理程序配置会议加入页面</span><span class="sxs-lookup"><span data-stu-id="1255c-120">To configure the meeting join page by using Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="1255c-121">启动 Lync Server 2013 命令行管理程序：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server Management Shell**"。</span><span class="sxs-lookup"><span data-stu-id="1255c-121">Start the Lync Server 2013 Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1255c-122">运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1255c-122">Run the following cmdlet:</span></span>
    
        Get-CsWebServiceConfiguration
    
    <span data-ttu-id="1255c-123">此 cmdlet 返回 web 服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="1255c-123">This cmdlet returns the web service configuration settings.</span></span>

3.  <span data-ttu-id="1255c-124">运行以下命令，将参数设置为 True 或 False，具体取决于你的首选项 (有关此 cmdlet 的参数的详细信息，请参阅 Lync Server 2013 管理外壳文档) ：</span><span class="sxs-lookup"><span data-stu-id="1255c-124">Run the following command, with the parameters set to True or False, depending on your preference (for details about the parameters for this cmdlet, see the Lync Server 2013 Management Shell documentation):</span></span>
    
        Set-CsWebServiceConfiguration -Identity global -ShowJoinUsingLegacyClientLink $True

<span data-ttu-id="1255c-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1255c-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

