---
title: Lync Server 2013：创建 Kerberos 身份验证帐户
description: Lync Server 2013：创建 Kerberos 身份验证帐户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a Kerberos authentication account
ms:assetid: 63f0cef6-562a-4209-ae25-71f8dc7c7295
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398449(v=OCS.15)
ms:contentKeyID: 48184348
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f8e87a8ffcc95af4a44e516ac4e1f4d635d737
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432175"
---
# <a name="create-a-kerberos-authentication-account-in-lync-server-2013"></a><span data-ttu-id="176a7-103">在 Lync Server 2013 中创建 Kerberos 身份验证帐户</span><span class="sxs-lookup"><span data-stu-id="176a7-103">Create a Kerberos authentication account in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="176a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="176a7-104">

<span> </span></span></span>

<span data-ttu-id="176a7-105">_**主题上次修改时间：** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="176a7-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="176a7-106">若要成功完成此过程，你应至少作为域管理员组的成员登录到服务器或域。</span><span class="sxs-lookup"><span data-stu-id="176a7-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group.</span></span>

<span data-ttu-id="176a7-107">你可以为每个网站创建 Kerberos 身份验证帐户，也可以创建单个 Kerberos 身份验证帐户并将其用于所有网站。</span><span class="sxs-lookup"><span data-stu-id="176a7-107">You can create Kerberos authentication accounts for each site or you can create a single Kerberos authentication account and use it for all sites.</span></span> <span data-ttu-id="176a7-108">你可以使用 Windows PowerShell cmdlet 来创建和管理帐户，包括标识分配给每个网站的帐户。</span><span class="sxs-lookup"><span data-stu-id="176a7-108">You use Windows PowerShell cmdlets to create and manage the accounts, including identifying the accounts assigned to each site.</span></span> <span data-ttu-id="176a7-109">拓扑生成器和 Lync Server 2013 "控制面板" 不显示 Kerberos 身份验证帐户。</span><span class="sxs-lookup"><span data-stu-id="176a7-109">Topology Builder and the Lync Server 2013 Control Panel do not display Kerberos authentication accounts.</span></span> <span data-ttu-id="176a7-110">使用以下过程创建要用于 Kerberos 身份验证的一个或多个用户帐户。</span><span class="sxs-lookup"><span data-stu-id="176a7-110">Use the following procedure to create one or more user accounts to be used for Kerberos authentication.</span></span>

<div>

## <a name="to-create-a-kerberos-account"></a><span data-ttu-id="176a7-111">创建 Kerberos 帐户</span><span class="sxs-lookup"><span data-stu-id="176a7-111">To create a Kerberos account</span></span>

1.  <span data-ttu-id="176a7-112">作为域管理员组的成员，请登录到运行 Lync Server 2013 的域中的计算机或登录到安装了管理工具的计算机。</span><span class="sxs-lookup"><span data-stu-id="176a7-112">As a member of the Domain Admins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="176a7-113">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="176a7-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="176a7-114">从命令行运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="176a7-114">From the command line, run the following command:</span></span>
    
        New-CsKerberosAccount -UserAccount "Domain\UserAccount" -ContainerDN "CN=Users,DC=DomainName,DC=DomainExtension"
    
    <span data-ttu-id="176a7-115">例如：</span><span class="sxs-lookup"><span data-stu-id="176a7-115">For example:</span></span>
    
        New-CsKerberosAccount -UserAccount "Contoso\KerbAuth" -ContainerDN "CN=Users,DC=contoso,DC=com"

4.  <span data-ttu-id="176a7-116">通过打开 "Active Directory 用户和计算机" 确认是否创建了计算机对象，展开 " **用户** " 容器，然后确认该用户帐户的计算机对象位于容器中。</span><span class="sxs-lookup"><span data-stu-id="176a7-116">Confirm that the Computer object was created by opening Active Directory User and Computers, expand the **Users** container, and then confirm that the Computer object for the user account is in the container.</span></span>

<span data-ttu-id="176a7-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="176a7-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

