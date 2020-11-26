---
title: Lync Server 2013：XMPP 联盟伙伴的协商设置
description: Lync Server 2013： XMPP 联盟合作伙伴的协商设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Negotiation settings for XMPP federated partners
ms:assetid: ef773942-ef92-4f71-85a1-738dfebdfa00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552456(v=OCS.15)
ms:contentKeyID: 48679567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ac3d9c69d407dc750a1afb35f0a448869a88f09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445581"
---
# <a name="negotiation-settings-for-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="ea8c1-103">Lync Server 2013 中 XMPP 联盟伙伴的协商设置</span><span class="sxs-lookup"><span data-stu-id="ea8c1-103">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea8c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea8c1-104">

<span> </span></span></span>

<span data-ttu-id="ea8c1-105">_**主题上次修改时间：** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="ea8c1-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="ea8c1-106">XMPP 合作伙伴配置中的协商类型的设置有多种可能的组合。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-106">The settings for the negotiation types in the configuration of an XMPP Partner have a wide variety of possible combinations.</span></span> <span data-ttu-id="ea8c1-107">并非所有这些组合都有效。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-107">Not all of these combinations are valid.</span></span> <span data-ttu-id="ea8c1-108">本主题中所述的表将定义有效和无效的设置。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-108">The table detailed in this topic will define the valid and not valid settings.</span></span> <span data-ttu-id="ea8c1-109">常见配置显示在第一个表中，第二个表介绍了所有可能的组合。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-109">Common configurations are presented in the first table, the second table detailing all possible combinations.</span></span> <span data-ttu-id="ea8c1-110">请注意，不能 (SASL) 具有 *简单的身份验证和安全层* ， **除非** 也提供了 (TLS) 的 *传输层安全性* 。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-110">Note that you cannot have *Simple Authentication and Security Layer* (SASL) **unless** *Transport Layer Security* (TLS) is also available.</span></span> <span data-ttu-id="ea8c1-111">将以未加密的 (可读) 格式发送 SASL，除非受到另一种方式（如 TLS）保护，否则切勿传输。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-111">SASL is sent in an unencrypted (readable) format and should never be transmitted unless protected by another means, such as TLS.</span></span>

### <a name="common-xmpp-federation-negotiation-methods"></a><span data-ttu-id="ea8c1-112">常见的 XMPP 联盟协商方法</span><span class="sxs-lookup"><span data-stu-id="ea8c1-112">Common XMPP Federation Negotiation Methods</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea8c1-113"> (TLS) 的传输层安全性</span><span class="sxs-lookup"><span data-stu-id="ea8c1-113">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="ea8c1-114">简单身份验证和安全层 (SASL) </span><span class="sxs-lookup"><span data-stu-id="ea8c1-114">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="ea8c1-115">回拨身份验证</span><span class="sxs-lookup"><span data-stu-id="ea8c1-115">Dialback Authentication</span></span></th>
<th><span data-ttu-id="ea8c1-116"> (s) 的预期身份验证方法</span><span class="sxs-lookup"><span data-stu-id="ea8c1-116">Expected Authentication Method(s)</span></span></th>
<th><span data-ttu-id="ea8c1-117">注释</span><span class="sxs-lookup"><span data-stu-id="ea8c1-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-118">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-118">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-119">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-119">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-120">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-120">False</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-121">TLS 上的 SASL</span><span class="sxs-lookup"><span data-stu-id="ea8c1-121">SASL over TLS</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-122">TLS 和 SASL 所需有助于确保 SASL 消息流的安全。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-122">TLS and SASL required helps to ensure that the SASL message stream is secure.</span></span> <span data-ttu-id="ea8c1-123">如果 XMPP 联盟合作伙伴未将 TLS 设置为必需或可选，则回拨不可用，也不能用于回退方法。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-123">Dialback is not available and cannot be used for a fallback method if the XMPP federated partner has not set TLS to required or optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-124">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-124">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-125">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-126">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-126">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-127">TLS 上的 SASL，TLS 回拨，TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-127">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-128">如果 XMPP 联盟合作伙伴已将 SASL 设置为 "可选" 或 "所需的 SASL"，则需要使用 TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-128">By requiring TLS, if the XMPP federated partner has set SASL to optional or required SASL is used.</span></span> <span data-ttu-id="ea8c1-129">如果 SASL 不可用，将使用通过 TLS 的回拨。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-129">If SASL is not available, Dialback over TLS will be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-130">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-131">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-132">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-132">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-133">TLS 上的 SASL，TLS 回拨，TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-133">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-134">在提供的协商方法中非常灵活，这些设置依赖于 XMPP 联盟伙伴的设置。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-134">While very flexible in the negotiation methods offered, these settings rely on the XMPP federation partner’s settings.</span></span> <span data-ttu-id="ea8c1-135">如果合作伙伴具有 TLS 可选或必需，但不支持 SASL，TLS 回拨将可用。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-135">If the partner has TLS optional or required but SASL is not supported, TLS Dialback will be available.</span></span> <span data-ttu-id="ea8c1-136">如果合作伙伴将 TLS 和 SASL 设置为 "可选" 或 "所需"，则使用通过 SASL 的最佳选择。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-136">If the partner has TLS and SASL set to optional or required, the optimal selection of TLS over SASL is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-137">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-137">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-138">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-138">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-139">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-139">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-140">TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-140">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-141">在许多情况下，TCP 回拨是唯一可行的解决方案。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-141">In many cases, TCP Dialback is the only possible solution.</span></span> <span data-ttu-id="ea8c1-142">比其他选项更少，它提供一定级别的信任。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-142">Less desirable than other options, it does provide some level of trust.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="xmpp-federation-negotiation-methods-matrix---complete"></a><span data-ttu-id="ea8c1-143">XMPP 联盟协商方法矩阵-完成</span><span class="sxs-lookup"><span data-stu-id="ea8c1-143">XMPP Federation Negotiation Methods Matrix - Complete</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea8c1-144"> (TLS) 的传输层安全性</span><span class="sxs-lookup"><span data-stu-id="ea8c1-144">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="ea8c1-145">简单身份验证和安全层 (SASL) </span><span class="sxs-lookup"><span data-stu-id="ea8c1-145">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="ea8c1-146">回拨身份验证</span><span class="sxs-lookup"><span data-stu-id="ea8c1-146">Dialback Authentication</span></span></th>
<th><span data-ttu-id="ea8c1-147">预期的身份验证方法</span><span class="sxs-lookup"><span data-stu-id="ea8c1-147">Expected Authentication Method</span></span></th>
<th><span data-ttu-id="ea8c1-148">无效配置的备注、警告或错误</span><span class="sxs-lookup"><span data-stu-id="ea8c1-148">Notes, Warning or Error for Not Valid Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-149">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-149">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-150">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-150">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-151">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-151">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-152">TLS 上的 SASL</span><span class="sxs-lookup"><span data-stu-id="ea8c1-152">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-153">如果需要 SASL 和 TLS，则回拨不会运行。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-153">Dialback will not operate if both SASL and TLS are required.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-154">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-154">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-155">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-155">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-156">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-156">False</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-157">TLS 上的 SASL</span><span class="sxs-lookup"><span data-stu-id="ea8c1-157">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-158">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-158">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-159">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-159">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-160">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-160">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-161">TLS 上的 SASL，TLS 回拨，TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-161">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-162">SASL 需要 TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-162">SASL requires TLS.</span></span> <span data-ttu-id="ea8c1-163">允许 TLS 是可选的可能会导致会话协商失败。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-163">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-164">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-164">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-165">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-165">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-166">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-166">False</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-167">TLS 上的 SASL</span><span class="sxs-lookup"><span data-stu-id="ea8c1-167">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-168">SASL 需要 TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-168">SASL requires TLS.</span></span> <span data-ttu-id="ea8c1-169">允许 TLS 是可选的可能会导致会话协商失败。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-169">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-170">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-170">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-171">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-171">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-172">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-172">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-173">TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-173">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-174">SASL 需要 TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-174">SASL requires TLS.</span></span> <span data-ttu-id="ea8c1-175">允许 TLS 是可选的可能会导致会话协商失败。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-175">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-176">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-176">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-177">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-177">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-178">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-178">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-179">配置无效</span><span class="sxs-lookup"><span data-stu-id="ea8c1-179">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-180">由于 SASL 需要 TLS，并且 TLS 不可用，因此不能成功使用 SASL/TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-180">Because SASL requires TLS, and TLS is not available, SASL/TLS cannot succeed.</span></span> <span data-ttu-id="ea8c1-181">TCP 回拨已设置为 false，无法使用。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-181">TCP Dialback is set to false, and cannot be used.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-182">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-182">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-183">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-183">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-184">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-184">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-185">TLS 上的 SASL，TLS 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-185">SASL over TLS, TLS Dialback</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-186">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-186">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-187">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-187">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-188">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-188">False</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-189">TLS 上的 SASL</span><span class="sxs-lookup"><span data-stu-id="ea8c1-189">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-190">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-190">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-191">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-191">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-192">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-192">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-193">TLS 上的 SASL，TLS 回拨，TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-193">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-194">SASL 需要 TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-194">SASL requires TLS.</span></span> <span data-ttu-id="ea8c1-195">允许 TLS 是可选的可能会导致会话协商失败。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-195">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-196">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-196">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-197">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-197">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-198">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-198">False</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-199">TLS 上的 SASL</span><span class="sxs-lookup"><span data-stu-id="ea8c1-199">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-200">SASL 需要 TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-200">SASL requires TLS.</span></span> <span data-ttu-id="ea8c1-201">允许 TLS 是可选的可能会导致会话协商失败。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-201">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-202">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-202">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-203">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-203">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-204">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-204">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-205">TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-205">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-206">SASL 需要 TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-206">SASL requires TLS.</span></span> <span data-ttu-id="ea8c1-207">允许 TLS 是可选的可能会导致会话协商失败。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-207">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-208">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-208">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-209">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-209">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-210">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-210">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-211">配置无效</span><span class="sxs-lookup"><span data-stu-id="ea8c1-211">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-212">SASL 需要 TLS。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-212">SASL requires TLS.</span></span> <span data-ttu-id="ea8c1-213">允许 TLS 是可选的可能会导致会话协商失败。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-213">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-214">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-214">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-215">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-215">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-216">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-216">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-217">TLS 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-217">TLS Dialback</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-218">配置允许 TLS 回拨。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-218">Configuration allows for TLS Dialback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-219">必需</span><span class="sxs-lookup"><span data-stu-id="ea8c1-219">Required</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-220">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-220">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-221">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-221">False</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-222">配置无效</span><span class="sxs-lookup"><span data-stu-id="ea8c1-222">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-223">必须启用 SASL 或回拨。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-223">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-224">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-224">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-225">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-225">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-226">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-226">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-227">TLS 回拨，TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-227">TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-228">根据其他终结点的协商选项，将接受 TCP 或 TLS 回拨。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-228">Based on negotiation choices of the other end point, TCP or TLS Dialback will be accepted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-229">可选</span><span class="sxs-lookup"><span data-stu-id="ea8c1-229">Optional</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-230">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-230">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-231">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-231">False</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-232">配置无效</span><span class="sxs-lookup"><span data-stu-id="ea8c1-232">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-233">必须启用 SASL 或回拨。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-233">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea8c1-234">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-234">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-235">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-235">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-236">True</span><span class="sxs-lookup"><span data-stu-id="ea8c1-236">True</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-237">TCP 回拨</span><span class="sxs-lookup"><span data-stu-id="ea8c1-237">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-238">TCP 回拨是唯一可用的协商方法</span><span class="sxs-lookup"><span data-stu-id="ea8c1-238">TCP Dialback is the only negotiation method available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea8c1-239">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-239">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-240">否</span><span class="sxs-lookup"><span data-stu-id="ea8c1-240">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-241">False</span><span class="sxs-lookup"><span data-stu-id="ea8c1-241">False</span></span></p></td>
<td><p><span data-ttu-id="ea8c1-242">配置无效</span><span class="sxs-lookup"><span data-stu-id="ea8c1-242">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="ea8c1-243">必须启用 SASL 或回拨。</span><span class="sxs-lookup"><span data-stu-id="ea8c1-243">SASL or Dialback must be enabled.</span></span>


<span data-ttu-id="ea8c1-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea8c1-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

