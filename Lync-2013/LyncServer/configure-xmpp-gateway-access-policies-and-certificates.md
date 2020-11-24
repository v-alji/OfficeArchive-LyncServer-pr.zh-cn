---
title: 配置 XMPP 网关访问策略和证书
description: 配置 XMPP 网关访问策略和证书。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure XMPP gateway access policies and certificates
ms:assetid: fac02f4e-d14d-4be3-b53c-74c82436fd93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721945(v=OCS.15)
ms:contentKeyID: 49733882
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e958100501ad9ca87d1ab970162f4be8c7692a99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391887"
---
# <a name="configure-xmpp-gateway-access-policies-and-certificates"></a><span data-ttu-id="2c762-103">配置 XMPP 网关访问策略和证书</span><span class="sxs-lookup"><span data-stu-id="2c762-103">Configure XMPP gateway access policies and certificates</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c762-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c762-104">

<span> </span></span></span>

<span data-ttu-id="2c762-105">_**主题上次修改时间：** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="2c762-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="2c762-106">XMPP federation 根据可扩展消息和状态协议 (XMPP) 定义外部部署。</span><span class="sxs-lookup"><span data-stu-id="2c762-106">XMPP federation defines an external deployment based on the eXtensible Messaging and Presence Protocol (XMPP).</span></span> <span data-ttu-id="2c762-107">XMPP 配置允许 Lync 用户通过以下方式访问 XMPP 域用户：</span><span class="sxs-lookup"><span data-stu-id="2c762-107">An XMPP configuration allows Lync users access to XMPP domain users by:</span></span>

  - <span data-ttu-id="2c762-108">IM 和状态-仅限人员</span><span class="sxs-lookup"><span data-stu-id="2c762-108">IM and Presence – person to person only</span></span>

  - <span data-ttu-id="2c762-109">在 Lync 客户端中创建 XMPP 联盟联系人</span><span class="sxs-lookup"><span data-stu-id="2c762-109">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="2c762-110">配置策略以支持可扩展消息和状态协议 (XMPP) 联盟伙伴时，这些策略适用于 XMPP 联盟域的用户，但不适用于会话初始协议的用户 (SIP) 即时消息 (服务提供商) 例如，Windows Live (或 SIP 联盟域。</span><span class="sxs-lookup"><span data-stu-id="2c762-110">When you configure policies for support of extensible messaging and presence protocol (XMPP) federated partners, the policies apply to users of XMPP federated domains, but not to users of session initiation protocol (SIP) instant messaging (IM) service providers (for example, Windows Live), or SIP federated domains.</span></span> <span data-ttu-id="2c762-111">为你希望允许用户添加联系人并与之通信的每个 XMPP 联盟域配置 XMPP 联盟合作伙伴。</span><span class="sxs-lookup"><span data-stu-id="2c762-111">You configure an XMPP Federated Partner for each XMPP federated domain that you want to allow your users to add contacts and communicate with.</span></span> <span data-ttu-id="2c762-112">策略准备好后，您需要配置 XMPP 网关证书。</span><span class="sxs-lookup"><span data-stu-id="2c762-112">Once the policies are in place, you need to configure the XMPP Gateway certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2c762-113">若要开始 XMPP 网关迁移，你需要部署 Lync Server 2013 XMPP 网关，并配置访问策略以启用 Lync Server 2013 XMPP 网关的用户。</span><span class="sxs-lookup"><span data-stu-id="2c762-113">To begin the XMPP Gateway migration, you need to deploy the Lync Server 2013 XMPP Gateway, and configure access policies to enable users for Lync Server 2013 XMPP Gateway.</span></span> <span data-ttu-id="2c762-114">在执行这些步骤之前，必须将所有用户移到 Lync Server 2013 部署。</span><span class="sxs-lookup"><span data-stu-id="2c762-114">All users must be moved to the Lync Server 2013 deployment before you perform these steps.</span></span> <span data-ttu-id="2c762-115">有关详细信息，请参阅 <A href="configure-xmpp-gateway-on-lync-server-2013.md">在 Lync Server 2013 上配置 XMPP 网关</A>。</span><span class="sxs-lookup"><span data-stu-id="2c762-115">For details, see <A href="configure-xmpp-gateway-on-lync-server-2013.md">Configure XMPP gateway on Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="configure-an-external-access-policy-to-enable-users-for-lync-server-2013-xmpp-gateway"></a><span data-ttu-id="2c762-116">将外部访问策略配置为启用 Lync Server 2013 XMPP 网关的用户</span><span class="sxs-lookup"><span data-stu-id="2c762-116">Configure an External Access Policy to Enable Users for Lync Server 2013 XMPP Gateway</span></span>

1.  <span data-ttu-id="2c762-117">打开“Lync Server 控制面板”。</span><span class="sxs-lookup"><span data-stu-id="2c762-117">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="2c762-118">在左侧导航栏中，单击 " **联盟和外部访问**"，然后单击 " **外部访问策略**"。</span><span class="sxs-lookup"><span data-stu-id="2c762-118">In the left navigation bar, click **Federation and External Access**, and then click **External Access Policy**.</span></span>

3.  <span data-ttu-id="2c762-119">单击 " **新建** "，然后单击 " **用户策略**"。</span><span class="sxs-lookup"><span data-stu-id="2c762-119">Click **New** and then click **User policy**.</span></span>

4.  <span data-ttu-id="2c762-120">输入外部 access 用户策略的名称。</span><span class="sxs-lookup"><span data-stu-id="2c762-120">Enter a name for the external access user policy.</span></span>

5.  <span data-ttu-id="2c762-121">提供外部 access 用户策略的说明。</span><span class="sxs-lookup"><span data-stu-id="2c762-121">Provide a description for external access user policy.</span></span>

6.  <span data-ttu-id="2c762-122">选择 " **启用与联盟用户的通信**"。</span><span class="sxs-lookup"><span data-stu-id="2c762-122">Select **Enable communications with federated users**.</span></span>

7.  <span data-ttu-id="2c762-123">选择 " **启用与 XMPP 联盟用户的通信**"。</span><span class="sxs-lookup"><span data-stu-id="2c762-123">Select **Enable communications with XMPP federated users**.</span></span>

8.  <span data-ttu-id="2c762-124">单击 " **提交** " 将更改保存到 "网站" 或 "用户策略"。</span><span class="sxs-lookup"><span data-stu-id="2c762-124">Click **Commit** to save your changes to the site or user policy.</span></span>

<span data-ttu-id="2c762-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c762-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

