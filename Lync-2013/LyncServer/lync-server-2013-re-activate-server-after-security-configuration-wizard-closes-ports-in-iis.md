---
title: 使用安全配置向导在 IIS 中关闭端口后重新激活服务器
description: 安全配置向导在 IIS 中关闭端口后重新激活服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Re-activate server after Security Configuration Wizard closes ports in IIS
ms:assetid: cb8e17cf-f8c1-4099-b63b-c242d656c26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398851(v=OCS.15)
ms:contentKeyID: 48185644
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d824845a7f89c28087a7b5d180a6ed017cb47ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436718"
---
# <a name="re-activate-server-after-security-configuration-wizard-closes-ports-in-iis"></a><span data-ttu-id="50d61-103">使用安全配置向导在 IIS 中关闭端口后重新激活服务器</span><span class="sxs-lookup"><span data-stu-id="50d61-103">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50d61-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50d61-104">

<span> </span></span></span>

<span data-ttu-id="50d61-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="50d61-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="50d61-106">某些 Lync Server 2013 角色在 Internet 信息服务上运行 Web 服务 (IIS) 端口4443。</span><span class="sxs-lookup"><span data-stu-id="50d61-106">Some Lync Server 2013 roles run Web Services on Internet Information Services (IIS) port 4443.</span></span> <span data-ttu-id="50d61-107">运行 Lync Server 部署向导、Bootstrapper.exe 或使用 **Enable-CsComputer** cmdlet 会在防火墙中创建一个例外，并打开该端口。</span><span class="sxs-lookup"><span data-stu-id="50d61-107">Running the Lync Server Deployment Wizard, Bootstrapper.exe, or using the **Enable-CsComputer** cmdlet creates an exception in the firewall and opens the port.</span></span> <span data-ttu-id="50d61-108">如果随后运行的是 Windows Server 2008 R2 安全配置向导 (或其他强化脚本) ，则将阻止端口4443，并且外部客户端将无法联系 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="50d61-108">If you then run the Windows Server 2008 R2 Security Configuration Wizard (or other hardening scripts), port 4443 will be blocked, and external clients will not be able to contact Web Services.</span></span> <span data-ttu-id="50d61-109">若要重新打开该端口，可以直接修改防火墙例外或重新激活服务器。</span><span class="sxs-lookup"><span data-stu-id="50d61-109">To reopen the port you can either modify the firewall exception directly or re-activate the server.</span></span>

<div>

## <a name="to-re-activate-the-server-by-using-the-deployment-wizard"></a><span data-ttu-id="50d61-110">使用部署向导重新激活服务器</span><span class="sxs-lookup"><span data-stu-id="50d61-110">To re-activate the server by using the Deployment Wizard</span></span>

1.  <span data-ttu-id="50d61-111">在 "Lync Server 部署向导" 页面上，单击 **步骤2：设置或删除 Lync Server 组件** 旁边的 "**运行**"。</span><span class="sxs-lookup"><span data-stu-id="50d61-111">On the Lync Server Deployment Wizard page, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

2.  <span data-ttu-id="50d61-112">在 " **安装 Lync 服务器组件** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="50d61-112">On **Setup Lync Server components** page, click **Next**.</span></span>

3.  <span data-ttu-id="50d61-113">在 " **执行命令** " 页面上，当 "任务状态" 显示为 "已完成" 时，单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="50d61-113">On the **Executing Commands** page, when the task status is shown as completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="50d61-114">您也可以使用 bootstrapper.exe 或 <STRONG>Enable-CsComputer</STRONG> 重新激活服务器。</span><span class="sxs-lookup"><span data-stu-id="50d61-114">You can also use bootstrapper.exe or <STRONG>Enable-CsComputer</STRONG> to re-activate the server.</span></span>

    
    <span data-ttu-id="50d61-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50d61-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

