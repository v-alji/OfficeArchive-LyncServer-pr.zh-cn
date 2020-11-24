---
title: Lync Server 2013：删除电话拨入式会议接入号码
description: Lync Server 2013：删除电话拨入式会议接入号码。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a dial-in conferencing access number
ms:assetid: 199c5d9c-0489-4ad5-a7f1-ca59fe0e6ac7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520956(v=OCS.15)
ms:contentKeyID: 48183522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa5bed6099f7464884c3bcde8e4ee86ad4207222
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392391"
---
# <a name="delete-a-dial-in-conferencing-access-number-in-lync-server-2013"></a><span data-ttu-id="7f536-103">删除 Lync Server 2013 中的电话拨入式会议接入号码</span><span class="sxs-lookup"><span data-stu-id="7f536-103">Delete a dial-in conferencing access number in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f536-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f536-104">

<span> </span></span></span>

<span data-ttu-id="7f536-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="7f536-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="7f536-106">请按照以下步骤删除电话拨入式会议接入号码。</span><span class="sxs-lookup"><span data-stu-id="7f536-106">Follow these steps to delete a dial-in conferencing access number.</span></span>

<div>

## <a name="to-delete-a-dial-in-conferencing-access-number"></a><span data-ttu-id="7f536-107">删除电话拨入式会议接入号码</span><span class="sxs-lookup"><span data-stu-id="7f536-107">To delete a dial-in conferencing access number</span></span>

1.  <span data-ttu-id="7f536-108">从属于 RTCUniversalServerAdmins 组成员的用户帐户 (或具有等效的用户权限) 或分配给 CsServerAdministrator 或 CsAdministrator 角色，请登录到你部署 Lync Server 2013 的网络中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="7f536-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="7f536-109">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="7f536-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7f536-110">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="7f536-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7f536-111">在左侧导航栏中，单击“**会议**”，然后单击“**拨入访问号码**”。</span><span class="sxs-lookup"><span data-stu-id="7f536-111">In the left navigation bar, click **Conferencing**, and then click **Dial-in Access Number**.</span></span>

4.  <span data-ttu-id="7f536-112">在页面上，单击列表中要删除的电话拨入式号码，再单击“**编辑**”，然后单击“**删除**”。</span><span class="sxs-lookup"><span data-stu-id="7f536-112">On the page, click the dial-in number you want to delete in the list, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="7f536-113">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="7f536-113">Click **OK**.</span></span>

</div>

<div>

## <a name="removing-dial-in-conferencing-access-numbers-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="7f536-114">使用 Windows PowerShell Cmdlet 删除电话拨入式会议访问号码</span><span class="sxs-lookup"><span data-stu-id="7f536-114">Removing Dial-in Conferencing Access Numbers by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="7f536-115">可以使用 Windows PowerShell 和 **CsDialInConferencingAccessNumber** cmdlet 删除电话拨入式会议访问号码。</span><span class="sxs-lookup"><span data-stu-id="7f536-115">Dial-in conferencing access numbers can be deleted by using Windows PowerShell and the **Remove-CsDialInConferencingAccessNumber** cmdlet.</span></span> <span data-ttu-id="7f536-116">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="7f536-116">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="7f536-117">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="7f536-117">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specific-dial-in-conferencing-access-number"></a><span data-ttu-id="7f536-118">删除特定的电话拨入式会议访问号码</span><span class="sxs-lookup"><span data-stu-id="7f536-118">To remove a specific dial-in conferencing access number</span></span>

  - <span data-ttu-id="7f536-119">此命令将删除具有标识 sip:RedmondDialInAccess@litwareinc.com 的电话拨入式会议访问号码：</span><span class="sxs-lookup"><span data-stu-id="7f536-119">This command deletes the dial-in conferencing access number with Identity sip:RedmondDialInAccess@litwareinc.com:</span></span>
    
        Remove-CsDialInConferencingAccessNumber -Identity "sip:RedmondDialInAccess@litwareinc.com"

</div>

<div>

## <a name="to-remove-all-the-dial-in-conferencing-access-numbers-assigned-to-a-specific-region"></a><span data-ttu-id="7f536-120">删除分配给特定区域的所有拨入式会议访问号码</span><span class="sxs-lookup"><span data-stu-id="7f536-120">To remove all the dial-in conferencing access numbers assigned to a specific region</span></span>

  - <span data-ttu-id="7f536-121">此命令将删除与西北地区相关联的所有拨入式会议访问号码：</span><span class="sxs-lookup"><span data-stu-id="7f536-121">This command deletes all the dial-in conferencing access numbers associated with the Northwest region:</span></span>
    
        Get-CsDialInConferencingAccessNumber -Region "Northwest" | Remove-CsDialInConferencingAccessNumber

</div>

<div>

## <a name="to-remove-dial-in-conferencing-access-numbers-based-on-primary-language"></a><span data-ttu-id="7f536-122">删除基于主要语言的电话拨入式会议访问号码</span><span class="sxs-lookup"><span data-stu-id="7f536-122">To remove dial-in conferencing access numbers based on primary language</span></span>

  - <span data-ttu-id="7f536-123">此命令将删除意大利语是主要语言的所有电话拨入式会议访问号码：</span><span class="sxs-lookup"><span data-stu-id="7f536-123">This command deletes all the dial-in conferencing access numbers where Italian is the primary language:</span></span>
    
        Get-CsDialInConferencingAccessNumber | Where-Object {$_.PrimaryLanguage -eq "it-IT"} | Remove-CsDialInConferencingAccessNumber

</div>

<span data-ttu-id="7f536-124">有关详细信息，请参阅 [CsDialInConferencingAccessNumber](https://docs.microsoft.com/powershell/module/skype/Remove-CsDialInConferencingAccessNumber) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="7f536-124">For more information, see the help topic for the [Remove-CsDialInConferencingAccessNumber](https://docs.microsoft.com/powershell/module/skype/Remove-CsDialInConferencingAccessNumber) cmdlet.</span></span>

<span data-ttu-id="7f536-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f536-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

