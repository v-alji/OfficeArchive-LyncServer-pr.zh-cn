---
title: Lync Server 2013：为智能卡身份验证配置企业 CA
description: Lync Server 2013：为智能卡身份验证配置企业 CA。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise CA for smart card authentication
ms:assetid: c24e0891-e108-4cb6-9902-c6a4c8e68455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308571(v=OCS.15)
ms:contentKeyID: 54973692
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98044c96dd04d02fd87609918f309cf65227b133
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433148"
---
# <a name="configuring-enterprise-ca-for-smart-card-authentication-in-lync-server-2013"></a><span data-ttu-id="41cec-103">在 Lync Server 2013 中配置用于智能卡身份验证的企业 CA</span><span class="sxs-lookup"><span data-stu-id="41cec-103">Configuring Enterprise CA for smart card authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41cec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41cec-104">

<span> </span></span></span>

<span data-ttu-id="41cec-105">_**主题上次修改时间：** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="41cec-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="41cec-106">以下部分介绍了如何配置企业根证书颁发机构 (CA) 以支持智能卡身份验证。</span><span class="sxs-lookup"><span data-stu-id="41cec-106">The following section describes how to configure an Enterprise Root Certification Authority (CA) to support smart card authentication.</span></span> <span data-ttu-id="41cec-107">有关如何安装企业根 CA 的详细信息，请参阅在以下位置安装企业根证书颁发机构 [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364) 。</span><span class="sxs-lookup"><span data-stu-id="41cec-107">For information on how to install an Enterprise Root CA, see Install an Enterprise Root Certification Authority at [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364).</span></span>

<div>

## <a name="configuring-an-enterprise-root-certificate-authority-to-support-smart-card-authentication"></a><span data-ttu-id="41cec-108">配置企业根证书颁发机构以支持智能卡身份验证</span><span class="sxs-lookup"><span data-stu-id="41cec-108">Configuring an Enterprise Root Certificate Authority to Support Smart Card Authentication</span></span>

<span data-ttu-id="41cec-109">以下步骤介绍如何配置企业根 CA 以支持智能卡身份验证：</span><span class="sxs-lookup"><span data-stu-id="41cec-109">The following steps describe how to configure an Enterprise Root CA to support Smart Card Authentication:</span></span>

1.  <span data-ttu-id="41cec-110">使用域管理员帐户登录到企业 CA 计算机。</span><span class="sxs-lookup"><span data-stu-id="41cec-110">Log in to the Enterprise CA computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="41cec-111">启动系统管理器，并验证是否已安装“证书颁发机构 Web 注册”角色。</span><span class="sxs-lookup"><span data-stu-id="41cec-111">Launch System Manager, and verify that the Certificate Authority Web Enrollment role is installed.</span></span>

3.  <span data-ttu-id="41cec-112">从“管理工具”菜单中，打开“证书颁发机构”管理控制台。</span><span class="sxs-lookup"><span data-stu-id="41cec-112">From the **Administrative Tools** menu, open the **Certification Authority** management console.</span></span>

4.  <span data-ttu-id="41cec-113">在导航窗格中，展开“证书颁发机构”。</span><span class="sxs-lookup"><span data-stu-id="41cec-113">In the Navigation pane, expand **Certification Authority**.</span></span>

5.  <span data-ttu-id="41cec-114">右键单击“证书模板”，选择“新建”，然后选择“要颁发的证书模板”。</span><span class="sxs-lookup"><span data-stu-id="41cec-114">Right click on **Certificate Templates**, select **New**, then select **Certificate Template to Issue**.</span></span>

6.  <span data-ttu-id="41cec-115">选择“注册代理”、“智能卡用户”和“智能卡登录”。</span><span class="sxs-lookup"><span data-stu-id="41cec-115">Select **Enrollment Agent**, **Smartcard User**, and **Smartcard Logon**.</span></span>

7.  <span data-ttu-id="41cec-116">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="41cec-116">Click **OK**.</span></span>

8.  <span data-ttu-id="41cec-117">右键单击“证书模板”。</span><span class="sxs-lookup"><span data-stu-id="41cec-117">Right click on **Certificate Templates**.</span></span>

9.  <span data-ttu-id="41cec-118">选择“管理”。</span><span class="sxs-lookup"><span data-stu-id="41cec-118">Select **Manage**.</span></span>

10. <span data-ttu-id="41cec-119">打开智能卡用户模板的属性。</span><span class="sxs-lookup"><span data-stu-id="41cec-119">Open the properties of the Smartcard User template.</span></span>

11. <span data-ttu-id="41cec-120">单击“安全”选项卡。</span><span class="sxs-lookup"><span data-stu-id="41cec-120">Click on the **Security** tab.</span></span>

12. <span data-ttu-id="41cec-121">更改权限，如下所示：</span><span class="sxs-lookup"><span data-stu-id="41cec-121">Change the permissions as follows:</span></span>
    
      - <span data-ttu-id="41cec-122">添加具有读取/注册（允许）权限的各个用户 AD 帐户，或者</span><span class="sxs-lookup"><span data-stu-id="41cec-122">Add individual user AD accounts with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="41cec-123">添加具有读取/注册（允许）权限且包含智能卡用户的安全组，或者</span><span class="sxs-lookup"><span data-stu-id="41cec-123">Add a security group containing smart card users with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="41cec-124">添加具有读取/注册（允许）权限的域用户组</span><span class="sxs-lookup"><span data-stu-id="41cec-124">Add the Domain Users group with Read/Enroll (Allow) permissions</span></span>

<span data-ttu-id="41cec-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41cec-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

