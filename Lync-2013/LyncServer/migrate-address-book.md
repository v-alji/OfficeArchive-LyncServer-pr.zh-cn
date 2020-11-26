---
title: 迁移通讯簿
description: 迁移通讯簿。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Address Book
ms:assetid: ac7f0f39-4c6d-4702-8e25-93a73e3d800f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205160(v=OCS.15)
ms:contentKeyID: 48185064
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad6acd8cca58aa4e09e21b9b45cbdddec527b5f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438608"
---
# <a name="migrate-address-book"></a><span data-ttu-id="5e162-103">迁移通讯簿</span><span class="sxs-lookup"><span data-stu-id="5e162-103">Migrate Address Book</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e162-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e162-104">

<span> </span></span></span>

<span data-ttu-id="5e162-105">_**主题上次修改时间：** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="5e162-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="5e162-106">通常情况下，Lync Server 2010 通讯簿与拓扑的其余部分一起迁移。</span><span class="sxs-lookup"><span data-stu-id="5e162-106">In general, the Lync Server 2010 Address Book is migrated along with the rest of your topology.</span></span> <span data-ttu-id="5e162-107">但是，如果您在 Lync Server 2010 环境中自定义以下迁移步骤，则可能需要执行一些迁移后步骤：</span><span class="sxs-lookup"><span data-stu-id="5e162-107">However, you might need to perform some post-migration steps if you customized the following in your Lync Server 2010 environment:</span></span>

  - <span data-ttu-id="5e162-108">将 **PartitionbyOU** WMI 属性设置为按组织单位 (OU) 分组通讯簿条目。</span><span class="sxs-lookup"><span data-stu-id="5e162-108">Set the **PartitionbyOU** WMI property to group Address Book entries by organizational unit (OU).</span></span>

  - <span data-ttu-id="5e162-109">自定义通讯簿规范化规则。</span><span class="sxs-lookup"><span data-stu-id="5e162-109">Customized the Address Book normalization rules.</span></span>

  - <span data-ttu-id="5e162-110">将 **UseNormalizationRules** 参数的默认值更改为 False。</span><span class="sxs-lookup"><span data-stu-id="5e162-110">Changed the default value for the **UseNormalizationRules** parameter to False.</span></span>

<span data-ttu-id="5e162-111">**分组通讯簿条目**</span><span class="sxs-lookup"><span data-stu-id="5e162-111">**Grouped Address Book Entries**</span></span>

<span data-ttu-id="5e162-112">如果将 **PartitionbyOU** WMI 属性设置为 True 以为每个 OU 创建通讯簿，则需要在用户和联系人上设置 **msRTCSIP-GroupingId** Active Directory 属性（如果要继续分组通讯簿条目）。</span><span class="sxs-lookup"><span data-stu-id="5e162-112">If you set the **PartitionbyOU** WMI property to True to create address books for each OU, you need to set the **msRTCSIP-GroupingId** Active Directory attribute on users and contacts if you want to continue grouping address book entries.</span></span> <span data-ttu-id="5e162-113">您可能希望对通讯簿条目进行分组以限制通讯簿搜索的范围。</span><span class="sxs-lookup"><span data-stu-id="5e162-113">You might want to group address book entries to limit the scope of Address Book searches.</span></span> <span data-ttu-id="5e162-114">若要使用 **msRTCSIP-GroupingId** 属性，请编写脚本来填充该属性，为要组合在一起的所有用户分配相同的值。</span><span class="sxs-lookup"><span data-stu-id="5e162-114">To use the **msRTCSIP-GroupingId** attribute, write a script to populate the attribute, assigning the same value for all of the users that you want to group together.</span></span> <span data-ttu-id="5e162-115">例如，为 OU 中的所有用户分配单个值。</span><span class="sxs-lookup"><span data-stu-id="5e162-115">For example, assign a single value for all the users in an OU.</span></span>

<span data-ttu-id="5e162-116">**通讯簿规范化规则**</span><span class="sxs-lookup"><span data-stu-id="5e162-116">**Address Book Normalization Rules**</span></span>

<span data-ttu-id="5e162-117">如果你在 Lync Server 2010 环境中自定义了通讯簿规范化规则，则必须将自定义规则迁移到你的试点池。</span><span class="sxs-lookup"><span data-stu-id="5e162-117">If you customized Address Book normalization rules in your Lync Server 2010 environment, you must migrate the customized rules to your pilot pool.</span></span> <span data-ttu-id="5e162-118">如果您没有自定义通讯簿规范化规则，则不能为通讯簿服务迁移任何内容。</span><span class="sxs-lookup"><span data-stu-id="5e162-118">If you did not customize Address Book normalization rules, you have nothing to migrate for Address Book service.</span></span> <span data-ttu-id="5e162-119">Lync Server 2013 的默认规范化规则与 Lync Server 2010 的默认规则相同。</span><span class="sxs-lookup"><span data-stu-id="5e162-119">The default normalization rules for Lync Server 2013 are the same as the default rules for Lync Server 2010.</span></span> <span data-ttu-id="5e162-120">按照本部分后面的过程迁移自定义的规范化规则。</span><span class="sxs-lookup"><span data-stu-id="5e162-120">Follow the procedure later in this section to migrate customized normalization rules.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5e162-121">如果您的组织使用远程呼叫控制，并且您自定义了通讯簿规范化规则，则必须先执行本主题中的过程，然后才能使用远程呼叫控制。</span><span class="sxs-lookup"><span data-stu-id="5e162-121">If your organization uses remote call control and you customized Address Book normalization rules, you must perform the procedure in this topic before you can use remote call control.</span></span> <span data-ttu-id="5e162-122">该过程需要 RTCUniversalServerAdmins 组或等效权限中的成员身份。</span><span class="sxs-lookup"><span data-stu-id="5e162-122">The procedure requires membership in the RTCUniversalServerAdmins group or equivalent rights.</span></span>



</div>

<span data-ttu-id="5e162-123">**UseNormalizationRules 设置为 False**</span><span class="sxs-lookup"><span data-stu-id="5e162-123">**UseNormalizationRules Set to False**</span></span>

<span data-ttu-id="5e162-124">如果将 **UseNormalizationRules** 的值设置为 False，以便用户可以使用在 Active Directory 域服务中定义的电话号码，而无需使用 Lync Server 2013 应用规范化规则，则需要将 **UseNormalizationRules** 和 **IgnoreGenericRules** 参数设置为 True。</span><span class="sxs-lookup"><span data-stu-id="5e162-124">If you set the value for **UseNormalizationRules** to False so that users can use phone numbers as they are defined in Active Directory Domain Services without having Lync Server 2013 apply normalization rules, you need to set the **UseNormalizationRules** and **IgnoreGenericRules** parameters to True.</span></span> <span data-ttu-id="5e162-125">按照本部分后面的过程将这些参数设置为 True。</span><span class="sxs-lookup"><span data-stu-id="5e162-125">Follow the procedure later in this section to set these parameters to True.</span></span>

<div>

## <a name="to-migrate-address-book-customized-normalization-rules"></a><span data-ttu-id="5e162-126">迁移通讯簿自定义规范化规则</span><span class="sxs-lookup"><span data-stu-id="5e162-126">To migrate Address Book customized normalization rules</span></span>

1.  <span data-ttu-id="5e162-127">\_ \_ \_ \_ 在 "通讯簿" 共享文件夹的根中查找公司电话号码规范化Rules.txt 文件，并将其复制到 Lync Server 2013 试验池中的 "通讯簿" 共享文件夹的根。</span><span class="sxs-lookup"><span data-stu-id="5e162-127">Find the Company\_Phone\_Number\_Normalization\_Rules.txt file in the root of the Address Book shared folder, and copy it to the root of the Address Book shared folder in your Lync Server 2013 pilot pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5e162-128">示例通讯簿规范化规则已安装在你的 ABS Web 组件文件目录中。</span><span class="sxs-lookup"><span data-stu-id="5e162-128">The sample Address Book normalization rules have been installed in your ABS Web component file directory.</span></span> <span data-ttu-id="5e162-129">路径为 <STRONG>$installedDriveLetter： \Program Files\Microsoft Lync Server 2013 \ Web Components\Address Book Files\Files\ Sample_Company_Phone_Number_Normalization_Rules.txt，</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="5e162-129">The path is <STRONG>$installedDriveLetter:\Program Files\Microsoft Lync Server 2013\Web Components\Address Book Files\Files\ Sample_Company_Phone_Number_Normalization_Rules.txt,</STRONG>.</span></span> <span data-ttu-id="5e162-130">可以将此文件作为Company_Phone_Number_Normalization_Rules.txt复制和重命名为 &nbsp; <STRONG>Company_Phone_Number_Normalization_Rules.txt</STRONG> &nbsp; 通讯簿共享文件夹的根目录。</span><span class="sxs-lookup"><span data-stu-id="5e162-130">This file can be copied and renamed as &nbsp;<STRONG>Company_Phone_Number_Normalization_Rules.txt</STRONG> &nbsp;to the address book shared folder’s root directory.</span></span> <span data-ttu-id="5e162-131">例如， <STRONG>$serverX</STRONG>中共享的通讯簿， &nbsp; 路径将类似于： <STRONG> \\ $serverX \LyncFileShare\2-WebServices-1\ABFiles</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="5e162-131">For example, the address book shared in <STRONG>$serverX</STRONG>,&nbsp;the path will be similar to: <STRONG>\\$serverX \LyncFileShare\2-WebServices-1\ABFiles</STRONG>.</span></span>

    
    </div>

2.  <span data-ttu-id="5e162-132">使用文本编辑器（如记事本）打开公司 \_ 电话 \_ 号码 \_ 规范化 \_Rules.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5e162-132">Use a text editor, such as Notepad, to open the Company\_Phone\_Number\_Normalization\_Rules.txt file.</span></span>

3.  <span data-ttu-id="5e162-133">某些类型的条目在 Lync Server 2013 中将无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="5e162-133">Certain types of entries will not work correctly in Lync Server 2013.</span></span> <span data-ttu-id="5e162-134">查看该文件以了解本步骤中所述的条目类型，根据需要对其进行编辑，并将更改保存到你的试点池中的 "通讯簿" 共享文件夹中。</span><span class="sxs-lookup"><span data-stu-id="5e162-134">Look through the file for the types of entries described in this step, edit them as necessary, and save the changes to the Address Book shared folder in your pilot pool.</span></span>
    
    <span data-ttu-id="5e162-135">包含所需的空格或标点的字符串将导致规范化规则失败，因为这些字符将从输入到规范化规则的字符串中去除。</span><span class="sxs-lookup"><span data-stu-id="5e162-135">Strings that include required whitespace or punctuation cause normalization rules to fail because these characters are stripped out of the string that is input to the normalization rules.</span></span> <span data-ttu-id="5e162-136">如果你有包含必需的空格或标点的字符串，则需要修改这些字符串。</span><span class="sxs-lookup"><span data-stu-id="5e162-136">If you have strings that include required whitespace or punctuation, you need to modify the strings.</span></span> <span data-ttu-id="5e162-137">例如，以下字符串将导致规范化规则失败：</span><span class="sxs-lookup"><span data-stu-id="5e162-137">For example, the following string would cause the normalization rule to fail:</span></span>
    
        \s*\(\s*\d\d\d\s*\)\s*\-\s*\d\d\d\s*\-\s*\d\d\d\d
    
    <span data-ttu-id="5e162-138">以下字符串不会导致规范化规则失败：</span><span class="sxs-lookup"><span data-stu-id="5e162-138">The following string would not cause the normalization rule to fail:</span></span>
    
        \s*\(?\s*\d\d\d\s*\)?\s*\-?\s*\d\d\d\s*\-?\s*\d\d\d\d

</div>

<div>

## <a name="to-set-usenormalizationrules-and-ignoregenericrules-to-true"></a><span data-ttu-id="5e162-139">将 UseNormalizationRules 和 IgnoreGenericRules 设置为 true</span><span class="sxs-lookup"><span data-stu-id="5e162-139">To set UseNormalizationRules and IgnoreGenericRules to true</span></span>

1.  <span data-ttu-id="5e162-140">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="5e162-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="5e162-141">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="5e162-141">Do one of the following:</span></span>
    
      - <span data-ttu-id="5e162-142">如果你的部署仅包括 Lync Server 2013，请在全局级别上运行以下 cmdlet，将 **UseNormalizationRules** 和 **IgnoreGenericRules** 的值更改为 True：</span><span class="sxs-lookup"><span data-stu-id="5e162-142">If your deployment includes only Lync Server 2013, run the following cmdlet at the global level to change the values for **UseNormalizationRules** and **IgnoreGenericRules** to True:</span></span>
        
            Set-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true
    
      - <span data-ttu-id="5e162-143">如果你的部署包括 Lync Server 2013 和 Lync Server 2010 或 Office 通信服务器 2007 R2 的组合，请运行以下 cmdlet，并将其分配给拓扑中的每个 Lync Server 2013 池：</span><span class="sxs-lookup"><span data-stu-id="5e162-143">If your deployment includes a combination of Lync Server 2013 and Lync Server 2010 or Office Communications Server 2007 R2, run the following cmdlet and assign it to each Lync Server 2013 pool in the topology:</span></span>
        
            New-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true

3.  <span data-ttu-id="5e162-144">等待中央管理存储复制在所有池上发生。</span><span class="sxs-lookup"><span data-stu-id="5e162-144">Wait for Central Management store replication to occur on all pools.</span></span>

4.  <span data-ttu-id="5e162-145">为你的部署修改电话规范化规则文件 "公司 \_ 电话 \_ 号码 \_ 规范化 \_Rules.txt" 以清除内容。</span><span class="sxs-lookup"><span data-stu-id="5e162-145">Modify the phone normalization rules file, "Company\_Phone\_Number\_Normalization\_Rules.txt", for your deployment to clear the content.</span></span> <span data-ttu-id="5e162-146">该文件位于每个 Lync Server 2013 池的文件共享中。</span><span class="sxs-lookup"><span data-stu-id="5e162-146">The file is on the file share of each Lync Server 2013 pool.</span></span> <span data-ttu-id="5e162-147">如果文件不存在，则创建一个名为 "公司 \_ 电话 \_ 号码 \_ 规范化 \_Rules.txt" 的空文件。</span><span class="sxs-lookup"><span data-stu-id="5e162-147">If the file is not present, then create an empty file named "Company\_Phone\_Number\_Normalization\_Rules.txt".</span></span>

5.  <span data-ttu-id="5e162-148">请等待几分钟，让所有前端池读取新文件。</span><span class="sxs-lookup"><span data-stu-id="5e162-148">Wait several minutes for all Front End pools to read the new files.</span></span>

6.  <span data-ttu-id="5e162-149">在部署中的每个 Lync Server 2013 池中运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="5e162-149">Run the following cmdlet on each Lync Server 2013 pool in your deployment:</span></span>
    
        Update-CsAddressBook

<span data-ttu-id="5e162-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e162-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

