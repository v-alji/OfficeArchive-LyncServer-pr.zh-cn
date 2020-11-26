---
title: Lync Server 2013：管理组织的 XMPP 联盟伙伴
description: Lync Server 2013：管理你的组织的 XMPP 联盟合作伙伴。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage XMPP federated partners for your organization
ms:assetid: 48681433-725d-457f-926b-f91d95bcf082
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552450(v=OCS.15)
ms:contentKeyID: 48679561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37d6fb4104c35ffc7db9649656f7786568a48b61
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426023"
---
# <a name="manage-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="24714-103">在 Lync Server 2013 中管理组织的 XMPP 联盟伙伴</span><span class="sxs-lookup"><span data-stu-id="24714-103">Manage XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24714-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24714-104">

<span> </span></span></span>

<span data-ttu-id="24714-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="24714-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="24714-106">本文档是预备文档，可能随时更改。</span><span class="sxs-lookup"><span data-stu-id="24714-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="24714-107">空白主题均以占位符的形式包含在内。</span><span class="sxs-lookup"><span data-stu-id="24714-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="24714-108">若要管理对 XMPP 联盟域的用户的支持，您需要执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="24714-108">To manage support for users of XMPP federated domains, you need to do the following:</span></span>

  - <span data-ttu-id="24714-109">配置一个或多个外部访问策略以支持 XMPP 联盟域的用户。</span><span class="sxs-lookup"><span data-stu-id="24714-109">Configure one or more external access policies to support users of XMPP federated domains.</span></span>

  - <span data-ttu-id="24714-110">配置访问边缘配置策略以支持联盟。</span><span class="sxs-lookup"><span data-stu-id="24714-110">Configure Access Edge Configuration policy to support federation.</span></span>

  - <span data-ttu-id="24714-111">创建 XMPP 联盟合作伙伴定义。</span><span class="sxs-lookup"><span data-stu-id="24714-111">Create XMPP Federated Partners definitions.</span></span>

  - <span data-ttu-id="24714-112">了解可用于 XMPP 联合身份验证的协商设置。</span><span class="sxs-lookup"><span data-stu-id="24714-112">Understand negotiation settings available for XMPP federation.</span></span>

<span data-ttu-id="24714-113">若要执行这些任务，请使用本节中的过程。</span><span class="sxs-lookup"><span data-stu-id="24714-113">To perform these tasks, use the procedures in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="24714-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="24714-114">In This Section</span></span>

  - [<span data-ttu-id="24714-115">在 Lync Server 2013 中创建或编辑 XMPP 合作伙伴配置</span><span class="sxs-lookup"><span data-stu-id="24714-115">Create or edit XMPP partner configuration in Lync Server 2013</span></span>](lync-server-2013-create-or-edit-xmpp-partner-configuration.md)

  - [<span data-ttu-id="24714-116">Lync Server 2013 中 XMPP 联盟伙伴的协商设置</span><span class="sxs-lookup"><span data-stu-id="24714-116">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md)

  - [<span data-ttu-id="24714-117">Lync Server 2013 中的示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="24714-117">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)

<span data-ttu-id="24714-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24714-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

