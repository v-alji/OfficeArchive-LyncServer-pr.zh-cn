---
title: 将 Lync Server 2010 会议目录移动到 Lync Server 2013
description: 将 Lync Server 2010 会议目录移动到 Lync Server 2013。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move Conference Directories
ms:assetid: 659867e0-ce91-4a95-9787-b1c1566460a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727126(v=OCS.15)
ms:contentKeyID: 62387565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12ac58ac0ab6f1908e7eac3e5824bf2304256632
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440344"
---
# <a name="move-conference-directories"></a><span data-ttu-id="d9f3f-103">移动会议目录</span><span class="sxs-lookup"><span data-stu-id="d9f3f-103">Move Conference Directories</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9f3f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9f3f-104">

<span> </span></span></span>

<span data-ttu-id="d9f3f-105">_**主题上次修改时间：** 2014-05-28_</span><span class="sxs-lookup"><span data-stu-id="d9f3f-105">_**Topic Last Modified:** 2014-05-28_</span></span>

<span data-ttu-id="d9f3f-106">在取消池之前，必须针对 Lync Server 2010 池中的每个会议目录执行以下过程。</span><span class="sxs-lookup"><span data-stu-id="d9f3f-106">Before decommissioning a pool you must perform the following procedure for each conference directory in your Lync Server 2010 pool.</span></span>

<div>

## <a name="to-move-a-conference-directory-to-lync-server-2013"></a><span data-ttu-id="d9f3f-107">将会议目录移动到 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9f3f-107">To Move a Conference Directory to Lync Server 2013</span></span>

1.  <span data-ttu-id="d9f3f-108">打开 Lync Server 命令行管理程序。</span><span class="sxs-lookup"><span data-stu-id="d9f3f-108">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="d9f3f-109">若要获取组织中的会议目录的标识，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d9f3f-109">To obtain the identity of the conference directories in your organization, run the following command:</span></span>
    
        Get-CsConferenceDirectory
    
    <span data-ttu-id="d9f3f-110">上面的命令返回你的组织中的所有会议目录。</span><span class="sxs-lookup"><span data-stu-id="d9f3f-110">The preceding command returns all the conference directories in your organization.</span></span> <span data-ttu-id="d9f3f-111">因此，你可能希望将结果限制为即将停止的池。</span><span class="sxs-lookup"><span data-stu-id="d9f3f-111">Because of that, you might want to limit the results to the pool being decommissioned.</span></span> <span data-ttu-id="d9f3f-112">例如，如果你使用完全限定的域名解除池 (FQDN) pool01.contoso.net，请使用此命令将返回的数据限制为来自该池中的会议目录：</span><span class="sxs-lookup"><span data-stu-id="d9f3f-112">For example, if you are decommissioning the pool with the fully qualified domain name (FQDN) pool01.contoso.net, use this command to limit the returned data to conference directories from that pool:</span></span>
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"}
    
    <span data-ttu-id="d9f3f-113">该命令仅返回 ServiceID 属性包含 FQDN pool01.contoso.net 的会议目录。</span><span class="sxs-lookup"><span data-stu-id="d9f3f-113">That command returns only the conference directories where the ServiceID property contains the FQDN pool01.contoso.net.</span></span>

3.  <span data-ttu-id="d9f3f-114">若要移动会议目录，请对池中的每个会议目录运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d9f3f-114">To move conference directories, run the following command for each conference directory in the pool:</span></span>
    
        Move-CsConferenceDirectory -Identity <Numeric identity of conference directory> -TargetPool <FQDN of pool where ownership is to be transitioned>
    
    <span data-ttu-id="d9f3f-115">例如，若要移动会议目录3，请使用此命令，将 Lync Server 2013 池指定为 TargetPool：</span><span class="sxs-lookup"><span data-stu-id="d9f3f-115">For example, to move conference directory 3 use this command, specifying a Lync Server 2013 pool as the TargetPool:</span></span>
    
        Move-CsConferenceDirectory -Identity 3 -TargetPool "pool02.contoso.net"
    
    <span data-ttu-id="d9f3f-116">如果要移动池中的所有会议目录，请使用类似于以下内容的命令：</span><span class="sxs-lookup"><span data-stu-id="d9f3f-116">If you want to move all the conference directories on a pool then use a command similar to the following:</span></span>
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"} | Move-CsConferenceDirectory -TargetPool "pool02.contoso.net"

<span data-ttu-id="d9f3f-117">请参阅文档 "卸载 Microsoft Lync Server 2010 和删除服务器角色" (可从) 下载该文档， [https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227) 以获取有关取消 Lync 2010 池的全面的分步说明。</span><span class="sxs-lookup"><span data-stu-id="d9f3f-117">Please see the document "Uninstalling Microsoft Lync Server 2010 and Removing Server Roles" (which can be downloaded from [https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227)) for comprehensive, step-by-step instructions on decommissioning Lync 2010 pools.</span></span>

<span data-ttu-id="d9f3f-118">移动会议目录时，可能会遇到以下错误：</span><span class="sxs-lookup"><span data-stu-id="d9f3f-118">When moving conference directories you might encounter the following error:</span></span>

    WARNING: Move operation failed for conference directory with ID "5". Cannot perform a rollback because data migration might have already started. Retry the operation.
    WARNING: Before using the -Force parameter, ensure that you have exported the conference directory data using DBImpExp.exe and imported the data on the target pool. Refer to the DBImpExp-Readme.htm file for more information.
    Move-CsConferenceDirectory : Unable to cast COM object of type 'System._ComObject' to interface type 'Microsoft.Rtc.Interop.User.IRtcConfDirManagement'. 
    This operation failed because the QueryInterface call on the COM component for the interface with SID '{4262B886-503F-4BEA-868C-04E8DF562CEB}' failed due to the following error: The specified module could not be found.

<span data-ttu-id="d9f3f-119">此错误通常在 Lync Server Management Shell 需要更新的 Active Directory 权限集以便完成任务时出现。</span><span class="sxs-lookup"><span data-stu-id="d9f3f-119">This error typically occurs when the Lync Server Management Shell requires an updated set of Active Directory permissions in order to complete a task.</span></span> <span data-ttu-id="d9f3f-120">若要解决此问题，请关闭该命令行管理程序的当前实例，然后打开一个新的 Shell 实例并重新运行该命令，以便移动会议目录。</span><span class="sxs-lookup"><span data-stu-id="d9f3f-120">To resolve the problem, close the current instance of the Management Shell, then open a new instance of the shell and re-run the command in order to move the conference directory.</span></span>

<span data-ttu-id="d9f3f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9f3f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

