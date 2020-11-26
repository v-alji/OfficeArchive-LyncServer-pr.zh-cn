---
title: Lync Server 2013：远程呼叫控制和电话号码规范化
description: Lync Server 2013：远程呼叫控制和电话号码规范化。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remote call control and phone number normalization
ms:assetid: 291d9e87-4c65-4ea2-888f-517741391de5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558630(v=OCS.15)
ms:contentKeyID: 48183696
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: edcb50678da7111aba066745bce5e356dd1ac7f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436501"
---
# <a name="remote-call-control-and-phone-number-normalization-in-lync-server-2013"></a><span data-ttu-id="b1583-103">Lync Server 2013 中的远程呼叫控制和电话号码规范化</span><span class="sxs-lookup"><span data-stu-id="b1583-103">Remote call control and phone number normalization in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1583-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1583-104">

<span> </span></span></span>

<span data-ttu-id="b1583-105">_**主题上次修改时间：** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="b1583-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="b1583-106">Lync 客户端会在通讯簿服务 (ABS) 文件下载中下载电话号码规范化规则。</span><span class="sxs-lookup"><span data-stu-id="b1583-106">Lync clients download phone number normalization rules as part of the Address Book Service (ABS) file download.</span></span> <span data-ttu-id="b1583-107">在远程呼叫控制方案中，通讯簿服务电话号码规范化规则同时应用于传入和传出远程呼叫控制调用。</span><span class="sxs-lookup"><span data-stu-id="b1583-107">In remote call control scenarios, Address Book Service phone number normalization rules are applied to both incoming and outgoing remote call control calls.</span></span> <span data-ttu-id="b1583-108">对于启用了远程呼叫控制的用户的传入呼叫，呼叫方的电话号码首先通过 SIP/CSTA 网关或专用分支 exchange （ (PBX) ）正常化为 E. 164 格式。</span><span class="sxs-lookup"><span data-stu-id="b1583-108">For incoming calls to a remote call control-enabled user, the phone number of the caller is first normalized to E.164 format by either the SIP/CSTA gateway or private branch exchange (PBX).</span></span> <span data-ttu-id="b1583-109">当 Lync Server 2013 从网关接收呼叫时，将对呼叫者的电话号码进行反向号码查找)  (对被呼叫者的 Microsoft Office Outlook 联系人列表中的标准号码或通讯簿服务中存储的全球通讯簿 (GAL) 。</span><span class="sxs-lookup"><span data-stu-id="b1583-109">When Lync Server 2013 receives the call from the gateway, it performs reverse number lookup (RNL) on the phone number of the caller against the normalized number in the callee’s Microsoft Office Outlook Contacts list or the global address list (GAL) that is stored in the Address Book Service.</span></span> <span data-ttu-id="b1583-110">如果 "反向号码查找" 成功找到匹配项，则呼叫者将按名称在传入呼叫通知中标识。</span><span class="sxs-lookup"><span data-stu-id="b1583-110">If reverse number lookup successfully finds a match, the caller is identified by name in the incoming call notification.</span></span>

<span data-ttu-id="b1583-111">对于传出的远程呼叫控制呼叫，在将呼叫路由到 SIP/CSTA 网关之前，Lync 会将通讯簿服务电话号码规范化规则应用到已拨打的号码。</span><span class="sxs-lookup"><span data-stu-id="b1583-111">For outgoing remote call control calls, Lync applies the Address Book Service phone number normalization rules to the dialed number before routing the call to the SIP/CSTA gateway.</span></span>

<span data-ttu-id="b1583-112">有关为远程呼叫控制创建电话号码规范化规则的详细信息，请参阅规划文档中的 [Lync Server 2013 中的 "拨号计划和规范规则](lync-server-2013-dial-plans-and-normalization-rules.md) "。</span><span class="sxs-lookup"><span data-stu-id="b1583-112">For details about creating phone number normalization rules for remote call control, see [Dial plans and normalization rules in Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) in the Planning documentation.</span></span>

<div>

## <a name="migrating-phone-number-normalization-rules"></a><span data-ttu-id="b1583-113">迁移电话号码规范化规则</span><span class="sxs-lookup"><span data-stu-id="b1583-113">Migrating Phone Number Normalization Rules</span></span>

<span data-ttu-id="b1583-114">如果你正在迁移以前为远程呼叫控制启用的用户，请参阅迁移文档中的以下主题：</span><span class="sxs-lookup"><span data-stu-id="b1583-114">If you are migrating users previously enabled for remote call control, see the following topics in the Migration documentation:</span></span>

  - <span data-ttu-id="b1583-115">对于 Lync Server 2010，请参阅迁移文档中的 " [迁移通讯簿](migrate-address-book.md) "。</span><span class="sxs-lookup"><span data-stu-id="b1583-115">For Lync Server 2010, see [Migrate Address Book](migrate-address-book.md) in the Migration documentation.</span></span>

  - <span data-ttu-id="b1583-116">有关通信服务器 2007 R2 的详细说明，请参阅迁移文档中的 " [迁移通讯簿](migrate-address-book.md) "。</span><span class="sxs-lookup"><span data-stu-id="b1583-116">For Communications Server 2007 R2, see [Migrate Address Book](migrate-address-book.md) in the Migration documentation.</span></span>

<span data-ttu-id="b1583-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1583-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

