---
title: 使用 "生成翻译规则" 工具创建或修改翻译规则
description: 使用 "生成翻译规则" 工具创建或修改翻译规则。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a translation rule by using the Build a Translation Rule tool
ms:assetid: ba112df8-3bb4-48e4-a353-4bf9110ccd71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412909(v=OCS.15)
ms:contentKeyID: 48185224
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 116048fff834e797bca76a895f45cd0ebc83ab94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391751"
---
# <a name="create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool-in-lync-server-2013"></a><span data-ttu-id="64376-103">使用 Lync Server 2013 中的 "生成翻译规则" 工具创建或修改翻译规则</span><span class="sxs-lookup"><span data-stu-id="64376-103">Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64376-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64376-104">

<span> </span></span></span>

<span data-ttu-id="64376-105">_**主题上次修改时间：** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="64376-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="64376-106">如果要定义翻译规则，请执行以下步骤：在 " **生成翻译规则** " 工具中输入一组值，并启用 Lync Server "控制面板" 为你生成相应的匹配模式和转换规则。</span><span class="sxs-lookup"><span data-stu-id="64376-106">Follow these steps if you want to define a translation rule by entering a set of values in the **Build a Translation Rule** tool and enabling Lync Server Control Panel to generate the corresponding matching pattern and translation rule for you.</span></span> <span data-ttu-id="64376-107">或者，可以手动编写正则表达式来定义匹配模式和转换规则。</span><span class="sxs-lookup"><span data-stu-id="64376-107">Alternatively, you can a write regular expression manually to define the matching pattern and translation rule.</span></span> <span data-ttu-id="64376-108">有关详细信息，请参阅 [在 Lync Server 2013 中手动创建或修改翻译规则](lync-server-2013-create-or-modify-a-translation-rule-manually.md)。</span><span class="sxs-lookup"><span data-stu-id="64376-108">For details, see [Create or modify a translation rule manually in Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-manually.md).</span></span>

<div>

## <a name="to-define-a-rule-by-using-the-build-a-translation-rule-tool"></a><span data-ttu-id="64376-109">使用“构建转换规则”工具定义规则</span><span class="sxs-lookup"><span data-stu-id="64376-109">To define a rule by using the Build a Translation Rule tool</span></span>

1.  <span data-ttu-id="64376-110">以 RTCUniversalServerAdmins 组成员的身份或者以 CsVoiceAdministrator、CsServerAdministrator 或 CsAdministrator 角色成员的身份登录计算机。</span><span class="sxs-lookup"><span data-stu-id="64376-110">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="64376-111">有关详细信息，请参阅 [在 Lync Server 2013 中委派设置权限](lync-server-2013-delegate-setup-permissions.md)。</span><span class="sxs-lookup"><span data-stu-id="64376-111">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="64376-112">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="64376-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="64376-113">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="64376-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="64376-114">若要开始定义翻译规则，请按照在 Lync server 2013 中的 "通过 [媒体绕过媒体配置主干](lync-server-2013-configure-a-trunk-with-media-bypass.md) " 中的步骤执行步骤10，或在 [lync server 2013 中通过步骤9配置中继而不绕过媒体旁路](lync-server-2013-configure-a-trunk-without-media-bypass.md) 。</span><span class="sxs-lookup"><span data-stu-id="64376-114">To begin defining a translation rule, follow the steps in [Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md) through step 10 or [Configure a trunk without media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md) through step 9.</span></span>

4.  <span data-ttu-id="64376-115">在“新建转换规则”或“编辑转换规则”页上的“名称”下，键入描述要转换的号码模式的名称。</span><span class="sxs-lookup"><span data-stu-id="64376-115">Under **Name** on the **New Translation Rule** or **Edit Translation Rule** page, type a name that describes the number pattern being translated.</span></span>

5.  <span data-ttu-id="64376-116">（可选）在“说明”下，键入转换规则的说明，例如，**US International long-distance dialing**。</span><span class="sxs-lookup"><span data-stu-id="64376-116">(Optional) Under **Description**, type a description of the translation rule, for example **US International long-distance dialing**.</span></span>

6.  <span data-ttu-id="64376-117">在对话框的“构建转换规则”部分的以下字段中输入值：</span><span class="sxs-lookup"><span data-stu-id="64376-117">In the **Build a Translation Rule** section of the dialog box, enter values in the following fields:</span></span>
    
      - <span data-ttu-id="64376-118">**起始数字**：（可选）指定要使模式与之匹配的号码的前导数字。</span><span class="sxs-lookup"><span data-stu-id="64376-118">**Starting digits**: (Optional) Specify the leading digits of numbers you want the pattern to match.</span></span> <span data-ttu-id="64376-119">例如， **+** 在此字段中输入，以匹配 E. 164 格式的数字 (以 +) 开头的数字。</span><span class="sxs-lookup"><span data-stu-id="64376-119">For example, enter **+** in this field to match numbers in E.164 format (which begin with +).</span></span>
    
      - <span data-ttu-id="64376-p105">**长度**：指定匹配模式中的数字位数，并选择希望模式匹配的号码是必须具有此准确长度、至少具有此长度还是可以具有任何长度。例如，输入 **11** 并在下拉列表中选择 **At least** 可匹配长度至少为 11 位的号码。</span><span class="sxs-lookup"><span data-stu-id="64376-p105">**Length**: Specify the number of digits in the matching pattern and select whether you want the pattern to match numbers that are this length exactly, at least this length, or any length. For example, enter **11** and select **At least** in the drop-down list to match numbers that are at least 11 digits in length.</span></span>
    
      - <span data-ttu-id="64376-122">**要删除的数字**：（可选）指定要删除的起始数字的位数。</span><span class="sxs-lookup"><span data-stu-id="64376-122">**Digits to remove**: (Optional) Specify the number of starting digits to be removed.</span></span> <span data-ttu-id="64376-123">例如，输入 " **1** " 将 **+** 从号码的开头去掉。</span><span class="sxs-lookup"><span data-stu-id="64376-123">For example, enter **1** to strip out the **+** from the beginning of the number.</span></span>
    
      - <span data-ttu-id="64376-p107">**要添加的数字**：（可选）指定要附加到转换号码前面的数字。例如，如果要在应用规则时将 011 附加到转换号码的前面，则输入 **011**。</span><span class="sxs-lookup"><span data-stu-id="64376-p107">**Digits to add**: (Optional) Specify digits to be prepended to the translated numbers. For example, enter **011** if you want 011 to be prepended to the translated numbers when the rule is applied.</span></span>
    
    <span data-ttu-id="64376-p108">这些字段中输入的值将反映在“要匹配的模式”和“转换规则”字段中。例如，如果指定前面示例中的值，则“要匹配的模式”字段中生成的正则表达式为：</span><span class="sxs-lookup"><span data-stu-id="64376-p108">The values you enter in these fields are reflected in the **Pattern to match** and **Translation rule** fields. For example, if you specify the preceding example values, the resulting regular expression in the **Pattern to match** field is:</span></span>
    
    <span data-ttu-id="64376-128">**^\\+ (\\ d {9} \\ d +) $**</span><span class="sxs-lookup"><span data-stu-id="64376-128">**^\\+(\\d{9}\\d+)$**</span></span>
    
    <span data-ttu-id="64376-p109">“转换规则”字段指定转换号码格式的模式。该模式由两部分组成：</span><span class="sxs-lookup"><span data-stu-id="64376-p109">The **Translation rule** field specifies a pattern for the format of translated numbers. This pattern has two parts:</span></span>
    
      - <span data-ttu-id="64376-131">代表匹配模式中数字位数的值（例如，**$1**）</span><span class="sxs-lookup"><span data-stu-id="64376-131">A value (for example, **$1**) that represents the number of digits in the matching pattern</span></span>
    
      - <span data-ttu-id="64376-132">（可选）可以通过在“要添加的数字”字段中输入来附加的值</span><span class="sxs-lookup"><span data-stu-id="64376-132">(Optional) A value that you can prepend by entering it in the **Digits to add** field</span></span>
    
    <span data-ttu-id="64376-133">如果使用前面示例中的值，“转换规则”字段中将显示 **011$1**。</span><span class="sxs-lookup"><span data-stu-id="64376-133">Using the preceding example values, **011$1** appears in the **Translation rule** field.</span></span>
    
    <span data-ttu-id="64376-134">应用此转换规则后，+441235551010 将变为 011441235551010。</span><span class="sxs-lookup"><span data-stu-id="64376-134">When this translation rule is applied, +441235551010 becomes 011441235551010.</span></span>

7.  <span data-ttu-id="64376-135">单击“确定”保存转换规则。</span><span class="sxs-lookup"><span data-stu-id="64376-135">Click **OK** to save the translation rule.</span></span>

8.  <span data-ttu-id="64376-136">单击“确定”保存中继配置。</span><span class="sxs-lookup"><span data-stu-id="64376-136">Click **OK** to save the trunk configuration.</span></span>

9.  <span data-ttu-id="64376-137">在“Trunk 配置”页上，单击“提交”，然后单击“全部提交”。</span><span class="sxs-lookup"><span data-stu-id="64376-137">On the **Trunk Configuration** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="64376-138">每当创建或修改转换规则时，都必须运行“全部提交”<STRONG></STRONG>命令以发布配置更改。</span><span class="sxs-lookup"><span data-stu-id="64376-138">Whenever you create or modify a translation rule, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="64376-139">有关详细信息，请参阅操作文档中的 <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Lync Server 2013 中的 "发布待处理的语音路由配置更改"</A> 。</span><span class="sxs-lookup"><span data-stu-id="64376-139">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="64376-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64376-140">See Also</span></span>


[<span data-ttu-id="64376-141">在 Lync Server 2013 中手动创建或修改翻译规则</span><span class="sxs-lookup"><span data-stu-id="64376-141">Create or modify a translation rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-translation-rule-manually.md)  
[<span data-ttu-id="64376-142">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64376-142">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="64376-143">在 Lync Server 2013 中配置不使用 "媒体旁路" 的主干</span><span class="sxs-lookup"><span data-stu-id="64376-143">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)  
[<span data-ttu-id="64376-144">将挂起的更改发布到 Lync Server 2013 中的语音路由配置</span><span class="sxs-lookup"><span data-stu-id="64376-144">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="64376-145">Lync Server 2013 中的全局媒体绕过选项</span><span class="sxs-lookup"><span data-stu-id="64376-145">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
  

<span data-ttu-id="64376-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64376-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

