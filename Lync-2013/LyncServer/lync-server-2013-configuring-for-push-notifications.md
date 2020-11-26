---
title: Lync Server 2013：配置推送通知
description: Lync Server 2013：配置推送通知。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring for push notifications
ms:assetid: d77f2c06-0fe6-45d5-8f08-808ab871b3e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690047(v=OCS.15)
ms:contentKeyID: 48185574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24c22ff42f666add9eac4966134c88b9bf680046
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433079"
---
# <a name="configuring-for-push-notifications-in-lync-server-2013"></a><span data-ttu-id="28d40-103">在 Lync Server 2013 中配置推送通知</span><span class="sxs-lookup"><span data-stu-id="28d40-103">Configuring for push notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28d40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28d40-104">

<span> </span></span></span>

<span data-ttu-id="28d40-105">_**主题上次修改时间：** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="28d40-105">_**Topic Last Modified:** 2013-02-12_</span></span>

<span data-ttu-id="28d40-106">即使移动应用处于非活动状态，推送通知（以锁屏提醒、图标或警报形式）也可以发送到移动设备。</span><span class="sxs-lookup"><span data-stu-id="28d40-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a mobile device even when the mobile application is inactive.</span></span> <span data-ttu-id="28d40-107">推送通知通知用户诸如新的或错过的 IM 邀请和语音邮件等事件。</span><span class="sxs-lookup"><span data-stu-id="28d40-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="28d40-108">Lync Server 2013 移动服务将通知发送到基于云的 Lync Server 推送通知服务，然后将通知发送到运行 Lync 2010 移动客户) 端的 Apple 设备的 apple 推送通知服务 (APNS)  (，对于运行 Lync 2010 移动版或 Lync 2013 移动客户端 (的 Windows Phone 设备，请使用 Microsoft 推送通知服务) MPNS () 。</span><span class="sxs-lookup"><span data-stu-id="28d40-108">The Lync Server 2013 Mobility Service sends the notifications to the cloud-based Lync Server Push Notification Service, which then sends the notifications to the Apple Push Notification Service (APNS) (for an Apple device running the Lync 2010 Mobile client) or the Microsoft Push Notification Service (MPNS) (for a Windows Phone device running the Lync 2010 Mobile or the Lync 2013 Mobile client).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="28d40-109">如果您将 Windows Phone 与 Lync 2010 移动版或 Lync 2013 移动客户端配合使用，推送通知是重要的考虑因素。</span><span class="sxs-lookup"><span data-stu-id="28d40-109">If you use Windows Phone with Lync 2010 Mobile or Lync 2013 Mobile client, push notification is an important consideration.</span></span><BR><span data-ttu-id="28d40-110">如果在 Apple 设备上使用 Lync 2010 Mobile，推送通知是重要的考虑因素。</span><span class="sxs-lookup"><span data-stu-id="28d40-110">If you use Lync 2010 Mobile on Apple devices, push notification is an important consideration.</span></span><BR><span data-ttu-id="28d40-111">如果在 Apple 设备上使用 Lync 2013 Mobile，则不再需要推送通知。</span><span class="sxs-lookup"><span data-stu-id="28d40-111">If you use Lync 2013 Mobile on Apple devices, you no longer need push notification.</span></span>



</div>

<span data-ttu-id="28d40-112">通过执行下列操作配置拓扑以支持推送通知：</span><span class="sxs-lookup"><span data-stu-id="28d40-112">Configure your topology to support push notifications by doing the following:</span></span>

  - <span data-ttu-id="28d40-113">如果你的环境具有 Lync Server 2010 或 Lync Server 2013 Edge 服务器，你需要添加新的托管提供商和 Microsoft Lync Online，然后在你的组织和 Lync Online 之间设置托管提供商联合身份验证。</span><span class="sxs-lookup"><span data-stu-id="28d40-113">If your environment has a Lync Server 2010 or Lync Server 2013 Edge Server, you need to add a new hosting provider, Microsoft Lync Online, and then set up hosting provider federation between your organization and Lync Online.</span></span>

  - <span data-ttu-id="28d40-114">如果你的环境具有 Office 通信服务器 2007 R2 Edge 服务器，你需要使用 push.lync.com 设置直接 SIP 联合身份验证。</span><span class="sxs-lookup"><span data-stu-id="28d40-114">If your environment has a Office Communications Server 2007 R2 Edge Server, you need to set up direct SIP federation with push.lync.com.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="28d40-115">Push.lync.com 是推送通知服务的 Microsoft Office 365 域。</span><span class="sxs-lookup"><span data-stu-id="28d40-115">Push.lync.com is a Microsoft Office 365 domain for Push Notification Service.</span></span>

    
    </div>

  - <span data-ttu-id="28d40-116">若要启用推送通知，你需要运行 **CsPushNotificationConfiguration** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28d40-116">To enable push notifications, you need to run the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="28d40-117">默认情况下，推送通知已关闭。</span><span class="sxs-lookup"><span data-stu-id="28d40-117">By default, push notifications are turned off.</span></span>

  - <span data-ttu-id="28d40-118">测试联合身份验证配置和推送通知。</span><span class="sxs-lookup"><span data-stu-id="28d40-118">Test the federation configuration and push notifications.</span></span>

<div>

## <a name="to-configure-for-push-notifications-with-lync-server-2013-or-lync-server-2010-edge-server"></a><span data-ttu-id="28d40-119">要配置 Lync Server 2013 或 Lync Server 2010 Edge 服务器的推送通知</span><span class="sxs-lookup"><span data-stu-id="28d40-119">To configure for push notifications with Lync Server 2013 or Lync Server 2010 Edge Server</span></span>

1.  <span data-ttu-id="28d40-120">登录到安装了 Lync Server 命令行管理器和 Ocscore 的计算机作为 RtcUniversalServerAdmins 组的成员。</span><span class="sxs-lookup"><span data-stu-id="28d40-120">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="28d40-121">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="28d40-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="28d40-122">添加 Lync Server online 托管提供商。</span><span class="sxs-lookup"><span data-stu-id="28d40-122">Add a Lync Server online hosting provider.</span></span> <span data-ttu-id="28d40-123">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="28d40-123">At the command line, type:</span></span>
    
        New-CsHostingProvider -Identity <unique identifier for Lync Online hosting provider> -Enabled $True -ProxyFqdn <FQDN for the Access Server used by the hosting provider> -VerificationLevel UseSourceVerification
    
    <span data-ttu-id="28d40-124">例如：</span><span class="sxs-lookup"><span data-stu-id="28d40-124">For example:</span></span>
    
        New-CsHostingProvider -Identity "LyncOnline" -Enabled $True -ProxyFqdn "sipfed.online.lync.com" -VerificationLevel UseSourceVerification
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="28d40-125">一个托管提供程序不能有多个联合关系。</span><span class="sxs-lookup"><span data-stu-id="28d40-125">You cannot have more than one federation relationship with a single hosting provider.</span></span> <span data-ttu-id="28d40-126">也就是说，如果你已设置与 sipfed.online.lync.com 的联合关系的托管提供商，请不要为其添加另一个托管提供程序，即使托管提供程序的标识是 LyncOnline 以外的其他内容。</span><span class="sxs-lookup"><span data-stu-id="28d40-126">That is, if you have already set up a hosting provider that has a federation relationship with sipfed.online.lync.com, do not add another hosting provider for it, even if the identity of the hosting provider is something other than LyncOnline.</span></span>

    
    </div>

4.  <span data-ttu-id="28d40-127">在 Lync Online 上设置你的组织和推送通知服务之间的托管提供程序联合身份验证。</span><span class="sxs-lookup"><span data-stu-id="28d40-127">Set up hosting provider federation between your organization and the Push Notification Service at Lync Online.</span></span> <span data-ttu-id="28d40-128">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="28d40-128">At the command line, type:</span></span>
    
        New-CsAllowedDomain -Identity "push.lync.com"

</div>

<div>

## <a name="to-configure-for-push-notifications-with-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="28d40-129">配置 Office 通信服务器 2007 R2 Edge 服务器的推送通知</span><span class="sxs-lookup"><span data-stu-id="28d40-129">To configure for push notifications with Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="28d40-130">以 RtcUniversalServerAdmins 组成员的身份登录到边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="28d40-130">Log on to the Edge Server as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="28d40-131">单击 " **开始**"，单击 " **所有程序**"，单击 " **管理工具**"，然后单击 " **计算机管理**"。</span><span class="sxs-lookup"><span data-stu-id="28d40-131">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Computer Management**.</span></span>

3.  <span data-ttu-id="28d40-132">在控制台树中，展开 " **服务和应用程序**"，右键单击 " **Microsoft Office 通信服务器 2007 R2**"，然后单击 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="28d40-132">In the console tree, expand **Services and Applications**, right-click **Microsoft Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="28d40-133">在 " **允许** " 选项卡上，单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="28d40-133">On the **Allow** tab, click **Add**.</span></span>

5.  <span data-ttu-id="28d40-134">在 " **添加联盟合作伙伴** " 对话框中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="28d40-134">In the **Add Federated Partner** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="28d40-135">在 " **联盟伙伴域名**" 中，键入 **push.lync.com**。</span><span class="sxs-lookup"><span data-stu-id="28d40-135">In **Federated partner domain name**, type **push.lync.com**.</span></span>
    
      - <span data-ttu-id="28d40-136">在 " **联盟伙伴访问边缘服务器**" 中，键入 **sipfed.online.lync.com**。</span><span class="sxs-lookup"><span data-stu-id="28d40-136">In **Federated partner Access Edge Server**, type **sipfed.online.lync.com**.</span></span>
    
      - <span data-ttu-id="28d40-137">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="28d40-137">Click **OK**.</span></span>

</div>

<div>

## <a name="to-enable-push-notifications"></a><span data-ttu-id="28d40-138">启用推送通知</span><span class="sxs-lookup"><span data-stu-id="28d40-138">To enable push notifications</span></span>

1.  <span data-ttu-id="28d40-139">登录到 Lync Server Management Shell 和 Ocscore 作为 CsAdministrator 角色的成员进行安装的计算机。</span><span class="sxs-lookup"><span data-stu-id="28d40-139">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="28d40-140">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="28d40-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="28d40-141">启用推送通知。</span><span class="sxs-lookup"><span data-stu-id="28d40-141">Enable push notifications.</span></span> <span data-ttu-id="28d40-142">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="28d40-142">At the command line, type:</span></span>
    
        Set-CsPushNotificationConfiguration -EnableApplePushNotificationService $True -EnableMicrosoftPushNotificationService $True

4.  <span data-ttu-id="28d40-143">启用联盟。</span><span class="sxs-lookup"><span data-stu-id="28d40-143">Enable federation.</span></span> <span data-ttu-id="28d40-144">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="28d40-144">At the command line, type:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

</div>

<div>

## <a name="to-test-federation-and-push-notifications"></a><span data-ttu-id="28d40-145">测试联盟和推送通知</span><span class="sxs-lookup"><span data-stu-id="28d40-145">To test federation and push notifications</span></span>

1.  <span data-ttu-id="28d40-146">登录到 Lync Server Management Shell 和 Ocscore 作为 CsAdministrator 角色的成员进行安装的计算机。</span><span class="sxs-lookup"><span data-stu-id="28d40-146">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="28d40-147">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="28d40-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="28d40-148">测试联合身份验证配置。</span><span class="sxs-lookup"><span data-stu-id="28d40-148">Test the federation configuration.</span></span> <span data-ttu-id="28d40-149">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="28d40-149">At the command line, type:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn <FQDN of Access Edge server used for federated SIP traffic> -Domain <FQDN of federated domain> -ProxyFqdn <FQDN of the Access Edge server used by the federated organization>
    
    <span data-ttu-id="28d40-150">例如：</span><span class="sxs-lookup"><span data-stu-id="28d40-150">For example:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn accessproxy.contoso.com -Domain push.lync.com -ProxyFqdn sipfed.online.lync.com

4.  <span data-ttu-id="28d40-151">测试推送通知。</span><span class="sxs-lookup"><span data-stu-id="28d40-151">Test push notifications.</span></span> <span data-ttu-id="28d40-152">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="28d40-152">At the command line, type:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn <Access Edge service FQDN>
    
    <span data-ttu-id="28d40-153">例如：</span><span class="sxs-lookup"><span data-stu-id="28d40-153">For example:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn accessproxy.contoso.com

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="28d40-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="28d40-154">See Also</span></span>


[<span data-ttu-id="28d40-155">Test-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="28d40-155">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
[<span data-ttu-id="28d40-156">Test-CsMcxPushNotification</span><span class="sxs-lookup"><span data-stu-id="28d40-156">Test-CsMcxPushNotification</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification)  
  

<span data-ttu-id="28d40-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28d40-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

