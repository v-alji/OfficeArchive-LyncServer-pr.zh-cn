---
title: Lync Server 2013：配置 Lync Phone Edition 的安全设置
description: Lync Server 2013：配置 Lync Phone Edition 的安全设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure security settings for Lync Phone Edition
ms:assetid: 6e7cec17-8a79-4428-9300-8821256c46cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521014(v=OCS.15)
ms:contentKeyID: 48184464
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82e6a6488db66a8497930ee6b2d1aec6fc8b0b2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433764"
---
# <a name="configure-security-settings-for-lync-phone-edition-in-lync-server-2013"></a><span data-ttu-id="20392-103">在 Lync Server 2013 中配置 Lync Phone Edition 的安全设置</span><span class="sxs-lookup"><span data-stu-id="20392-103">Configure security settings for Lync Phone Edition in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20392-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20392-104">

<span> </span></span></span>

<span data-ttu-id="20392-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="20392-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="20392-106">通过 SIP 安全设置和电话锁定设置，帮助提高运行 Lync Phone Edition 的设备的安全性。</span><span class="sxs-lookup"><span data-stu-id="20392-106">Help improve the security of devices running Lync Phone Edition via your SIP security setting and phone lock settings.</span></span>

<div>

## <a name="to-configure-security-settings-for-lync-phone-edition"></a><span data-ttu-id="20392-107">配置 Lync Phone 版本的安全设置</span><span class="sxs-lookup"><span data-stu-id="20392-107">To configure security settings for Lync Phone Edition</span></span>

1.  <span data-ttu-id="20392-108">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="20392-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="20392-109">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="20392-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="20392-110">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="20392-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="20392-111">在左侧导航栏中，单击 " **客户端**"，然后单击 " **设备配置**"。</span><span class="sxs-lookup"><span data-stu-id="20392-111">In the left navigation bar, click **Clients**, and then click **Device Configuration**.</span></span>

4.  <span data-ttu-id="20392-112">在 " **设备配置** " 页面上的设备配置列表中，双击要更改其安全设置的配置。</span><span class="sxs-lookup"><span data-stu-id="20392-112">On the **Device Configuration** page, in the list of device configurations, double-click the configuration for which you want to change security settings.</span></span>

5.  <span data-ttu-id="20392-113">在 " **编辑设备配置**" 的 " **sip 安全**" 中，指定 sip 安全级别。</span><span class="sxs-lookup"><span data-stu-id="20392-113">In **Edit Device Configuration**, in **SIP security**, specify the SIP security level.</span></span> <span data-ttu-id="20392-114">默认级别为 " **高**"，我们建议使用。</span><span class="sxs-lookup"><span data-stu-id="20392-114">The default level is **High**, which we recommend using.</span></span>

6.  <span data-ttu-id="20392-115">在 " **编辑设备配置**" 下的 " **电话锁定**" 下，选中或清除 " **强制设备锁定** " 复选框，默认情况下 (选中 "默认情况下) "，并指定默认的最小 PIN 长度 (默认) 和超时期限 (10 分钟) 。</span><span class="sxs-lookup"><span data-stu-id="20392-115">In **Edit Device Configuration**, under **Phone Lock**, select or clear the **Enforce device locking** check box (selected by default) and specify the minimum PIN length (6 characters by default) and timeout period (10 minutes by default).</span></span> <span data-ttu-id="20392-116">我们建议使用这些默认值或增加 PIN 长度和/或减少超时时间。</span><span class="sxs-lookup"><span data-stu-id="20392-116">We recommend using these defaults or increasing the PIN length and/or decreasing the timeout period.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="20392-117">有关详细信息，请参阅 <A href="lync-server-2013-enforce-phone-locking.md">在 Lync Server 2013 中强制执行电话锁定</A>。</span><span class="sxs-lookup"><span data-stu-id="20392-117">For details, see <A href="lync-server-2013-enforce-phone-locking.md">Enforce phone locking in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-security-settings-for-lync-phone-edition-phones-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="20392-118">使用 Windows PowerShell Cmdlet 为 Lync Phone Edition 手机配置安全设置</span><span class="sxs-lookup"><span data-stu-id="20392-118">Configuring Security Settings for Lync Phone Edition Phones by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="20392-119">可以使用 Lync Server 命令行管理程序和 **CsUCPhoneConfiguration** cmdlet 管理安全设置。</span><span class="sxs-lookup"><span data-stu-id="20392-119">Security settings can be managed by using Lync Server Management Shell and the **Get-CsUCPhoneConfiguration** cmdlet.</span></span> <span data-ttu-id="20392-120">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="20392-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="20392-121">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="20392-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-modify-the-sip-security-mode"></a><span data-ttu-id="20392-122">修改 SIP 安全模式</span><span class="sxs-lookup"><span data-stu-id="20392-122">To modify the SIP security mode</span></span>

  - <span data-ttu-id="20392-123">此命令将 UC 电话设置的全局集合的 SIPSecurityMode 设置为 "中"。</span><span class="sxs-lookup"><span data-stu-id="20392-123">This command sets the SIPSecurityMode for the global collection of UC phone settings to Medium.</span></span> <span data-ttu-id="20392-124">SIP 安全性还可以设置为 "低" 或 "高" (默认值) 。</span><span class="sxs-lookup"><span data-stu-id="20392-124">SIP security could also be set to Low or High (the default value).</span></span>
    
        Set-CsUCPhoneConfiguration -Identity global -SIPSecurityMode "Medium"

</div>

<div>

## <a name="to-modify-the-minimum-pin-length"></a><span data-ttu-id="20392-125">修改最小 PIN 长度</span><span class="sxs-lookup"><span data-stu-id="20392-125">To modify the minimum PIN length</span></span>

  - <span data-ttu-id="20392-126">在此示例中，所有 UC 电话设置均已修改为要求7位的最小 PIN 长度。</span><span class="sxs-lookup"><span data-stu-id="20392-126">In this example, all the UC phone settings are modified to require a minimum PIN length of 7 digits.</span></span>
    
        Get-CsUCPhoneConfiguration | Set-CsUCPhoneConfiguration -MinPhonePinLength 7

</div>

<span data-ttu-id="20392-127">有关详细信息，请参阅 [CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration)。</span><span class="sxs-lookup"><span data-stu-id="20392-127">For details, see [Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="20392-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="20392-128">See Also</span></span>


[<span data-ttu-id="20392-129">管理 Lync Server 2013 身份验证</span><span class="sxs-lookup"><span data-stu-id="20392-129">Managing Lync Server 2013 authentication</span></span>](lync-server-2013-managing-lync-server-authentication.md)  


[<span data-ttu-id="20392-130">在 Lync Server 2013 中管理设备、电话和客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="20392-130">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="20392-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20392-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

