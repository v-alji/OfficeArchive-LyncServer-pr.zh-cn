---
title: Lync Server 2013：更改管理
description: Lync Server 2013：更改管理。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change management
ms:assetid: 73c774f5-c12f-4c72-be73-e07dc745b994
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720336(v=OCS.15)
ms:contentKeyID: 63969618
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69ea019f6366528c40b60a39ca8b646b49b336b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435122"
---
# <a name="change-management-in-lync-server-2013"></a><span data-ttu-id="98e9e-103">Lync Server 2013 中的更改管理</span><span class="sxs-lookup"><span data-stu-id="98e9e-103">Change management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98e9e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98e9e-104">

<span> </span></span></span>

<span data-ttu-id="98e9e-105">_**主题上次修改时间：** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="98e9e-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="98e9e-106">对 IT 环境所做的更改不可避免。</span><span class="sxs-lookup"><span data-stu-id="98e9e-106">Changes to the IT environment are unavoidable.</span></span> <span data-ttu-id="98e9e-107">更改包括新技术、系统、应用程序、硬件、工具、流程和角色和职责方面的更改。</span><span class="sxs-lookup"><span data-stu-id="98e9e-107">Changes include new technologies, systems, applications, hardware, tools, processes, and changes in roles and responsibilities.</span></span> <span data-ttu-id="98e9e-108">有效的更改管理系统让你能够以最少的服务中断快速将更改引入 IT 环境。</span><span class="sxs-lookup"><span data-stu-id="98e9e-108">An effective change management system lets you introduce changes to the IT environment quickly and with minimal service disruption.</span></span> <span data-ttu-id="98e9e-109">更改管理系统将更改系统所涉及的团队汇集到一起。</span><span class="sxs-lookup"><span data-stu-id="98e9e-109">A change management system brings together the teams involved in changing a system.</span></span> <span data-ttu-id="98e9e-110">例如，决定利用 Office Web Apps。</span><span class="sxs-lookup"><span data-stu-id="98e9e-110">For example, deciding to take advantage of the Office Web Apps.</span></span> <span data-ttu-id="98e9e-111">这是一个集成的 Lync 服务应用程序，使用户能够在浏览器中阅读和编辑文档。</span><span class="sxs-lookup"><span data-stu-id="98e9e-111">This is an integrated Lync Service application that enables users to read and edit documents in a browser.</span></span> <span data-ttu-id="98e9e-112">在投入生产后，此服务的实现需要多个团队的参与：</span><span class="sxs-lookup"><span data-stu-id="98e9e-112">The implementation of this service, after you have gone into production, requires the involvement of several teams:</span></span>

  - <span data-ttu-id="98e9e-113">**测试团队**   此团队加载-在提供有关生产服务器的预期使用模式和预期性能的过程中的测试服务器上测试 Office Web Apps。</span><span class="sxs-lookup"><span data-stu-id="98e9e-113">**Test Team**   This team load-tests the Office Web Apps on a test server, in the process providing information about the expected usage patterns and expected performance of the production servers.</span></span>

  - <span data-ttu-id="98e9e-114">**Lync 管理员**   此团队确定部署策略并在可能的情况下为安装脚本。</span><span class="sxs-lookup"><span data-stu-id="98e9e-114">**Lync Administrators**   This team determines the deployment strategy and scripts the installation where it was possible.</span></span> <span data-ttu-id="98e9e-115">团队负责确保更改已部署在生产环境中，并且负责在以后管理。</span><span class="sxs-lookup"><span data-stu-id="98e9e-115">The team is responsible for making sure that the change is deployed on the production environment, and it is responsible for administration afterward.</span></span> <span data-ttu-id="98e9e-116">团队必须了解更改的效果，并在更改投入生产之前将其纳入过程中</span><span class="sxs-lookup"><span data-stu-id="98e9e-116">The team must understand the effect of the changes and incorporate them in procedures before the changes are put into production</span></span>

  - <span data-ttu-id="98e9e-117">**网络团队**   此团队负责更改允许从 Internet 访问内部 Lync 池服务器的防火墙规则。</span><span class="sxs-lookup"><span data-stu-id="98e9e-117">**Network Team**   This team is responsible for changes to firewall rules that allow access from the Internet to the internal Lync pool servers.</span></span> <span data-ttu-id="98e9e-118">团队还负责与 Lync 管理员协作，确保可用带宽能够支持其他负载。</span><span class="sxs-lookup"><span data-stu-id="98e9e-118">The team is also responsible in working with the Lync administrators for making sure that the available bandwidth can support the additional load.</span></span>

  - <span data-ttu-id="98e9e-119">**安全团队**   此团队评估安全性并将风险降至最低。</span><span class="sxs-lookup"><span data-stu-id="98e9e-119">**Security Team**   This team assesses security and minimizes risks.</span></span> <span data-ttu-id="98e9e-120">安全小组必须查看已知漏洞并帮助确保最小化安全风险。</span><span class="sxs-lookup"><span data-stu-id="98e9e-120">The security team must review known vulnerabilities and help ensure that security risks are minimized.</span></span>

  - <span data-ttu-id="98e9e-121">**用户验收团队**   此团队由愿意测试系统并提供改进反馈的用户组成。</span><span class="sxs-lookup"><span data-stu-id="98e9e-121">**User Acceptance Team**   This team is composed of users who are willing to test the system and offer feedback for improvements.</span></span>

<span data-ttu-id="98e9e-122">更改管理过程定义每个团队的职责并安排要执行的工作，并将检查和测试合并到所需的位置。</span><span class="sxs-lookup"><span data-stu-id="98e9e-122">The change management process defines the responsibilities of each team and schedules the work to be performed, incorporating checks and tests where they are required.</span></span> <span data-ttu-id="98e9e-123">根据所做更改的复杂程度和预期效果，更改控件将有所不同。</span><span class="sxs-lookup"><span data-stu-id="98e9e-123">Change controls will vary depending on the complexity and expected effect of a change.</span></span> <span data-ttu-id="98e9e-124">它们可能因小更改的自动审批、更改审阅会议以及整个项目级评论而异。</span><span class="sxs-lookup"><span data-stu-id="98e9e-124">They can vary from automatic approval of minor changes, to change review meetings, to full project-level reviews.</span></span> <span data-ttu-id="98e9e-125">为了更好地解释这种情况，本部分将讨论更改组。</span><span class="sxs-lookup"><span data-stu-id="98e9e-125">To explain this better, the groups of changes are discussed in this section.</span></span>

  - <span data-ttu-id="98e9e-126">**重大更改**   主要更改对系统具有全局影响，可能需要来自不同团队的输入。</span><span class="sxs-lookup"><span data-stu-id="98e9e-126">**Major Changes**   Major changes have a global effect on the system and may require input from various teams.</span></span> <span data-ttu-id="98e9e-127">升级到 Lync Server 2013 的一个示例。</span><span class="sxs-lookup"><span data-stu-id="98e9e-127">An example of this is upgrading to Lync Server 2013.</span></span> <span data-ttu-id="98e9e-128">主要更改影响许多团队和可能不同的系统。</span><span class="sxs-lookup"><span data-stu-id="98e9e-128">Major changes affect many teams and perhaps different systems.</span></span> <span data-ttu-id="98e9e-129">更改管理流程可能包含一个或多个更改评审会议，通知团队将参与更改或受更改影响。</span><span class="sxs-lookup"><span data-stu-id="98e9e-129">The change management process will probably include one or more change review meetings to inform the teams that will be involved in the change or be affected by the change.</span></span>

  - <span data-ttu-id="98e9e-130">**重大更改**   重大更改需要大量资源才能进行规划、构建和实施。</span><span class="sxs-lookup"><span data-stu-id="98e9e-130">**Significant Changes**   Significant changes require significant resources to plan, build, and implement.</span></span> <span data-ttu-id="98e9e-131">应引入相应的变更控件，以确保能够了解更改的效果、测试部署过程以及回滚和应急计划是否已准备就绪。</span><span class="sxs-lookup"><span data-stu-id="98e9e-131">Appropriate change controls should be introduced to help make ensure that the effect of the change is understood, deployment procedures are tested, and the rollback and contingency plans are ready.</span></span> <span data-ttu-id="98e9e-132">一个重大更改的示例是部署新的累积更新。</span><span class="sxs-lookup"><span data-stu-id="98e9e-132">An example of a significant change is deploying a new cumulative update.</span></span>

  - <span data-ttu-id="98e9e-133">**次要更改**   少量更改不会显著影响 IT 环境，例如，通过 "Microsoft Lync Server 2013 控制面板" 更改某些 Lync 策略。</span><span class="sxs-lookup"><span data-stu-id="98e9e-133">**Minor Changes**   Minor changes do not significantly affect the IT environment, for example, changing certain Lync policies via the Microsoft Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="98e9e-134">**标准更改**   标准更改是定期执行的，并且充分理解并记录下来。</span><span class="sxs-lookup"><span data-stu-id="98e9e-134">**Standard Changes**   Standard changes are performed regularly and are well understood and documented.</span></span> <span data-ttu-id="98e9e-135">更改管理过程应检查对过程所做的所有更改。</span><span class="sxs-lookup"><span data-stu-id="98e9e-135">The change management process should review all changes to the procedures.</span></span> <span data-ttu-id="98e9e-136">不应在常规更改（如创建内容数据库或添加用户）时需要它。</span><span class="sxs-lookup"><span data-stu-id="98e9e-136">It should not be needed for routine changes like creating a content database or adding a user.</span></span>

<span data-ttu-id="98e9e-137">下面的更改管理示例检查不同团队的交互方式以及部署新服务包时执行的操作。</span><span class="sxs-lookup"><span data-stu-id="98e9e-137">The following example of change management examines how different teams interact and the actions that are performed when a new service pack is deployed.</span></span> <span data-ttu-id="98e9e-138">这些操作由变更管理流程进行组织和管理。</span><span class="sxs-lookup"><span data-stu-id="98e9e-138">These actions are organized and managed by the change management process.</span></span>

  - <span data-ttu-id="98e9e-139">**引发更改请求**   安全小组已评估了最新的服务包并确认它能够解决生产系统中可能存在的漏洞。</span><span class="sxs-lookup"><span data-stu-id="98e9e-139">**Raise a change request**   The security team has assessed the latest service pack and confirmed that it resolves a possible vulnerability in the production system.</span></span> <span data-ttu-id="98e9e-140">团队引发更改请求，以将新的累积更新应用于运行 Lync Server 的所有服务器。</span><span class="sxs-lookup"><span data-stu-id="98e9e-140">The team raises a change request to have the new cumulative update applied to all servers that are running Lync Server.</span></span>

  - <span data-ttu-id="98e9e-141">**Service pack 发行说明审阅**   Lync 管理员团队查看 service pack 发行说明以识别对系统的影响。</span><span class="sxs-lookup"><span data-stu-id="98e9e-141">**Service pack release notes review**   The Lync administrator team reviews the service pack release notes to identify the effect on the system.</span></span>

  - <span data-ttu-id="98e9e-142">**执行一系列实验室测试**   Lync 管理员团队必须在测试环境中的服务器上执行测试更新，以确定是否可以成功应用服务包，而不会影响任何已安装的应用程序和服务器系统。</span><span class="sxs-lookup"><span data-stu-id="98e9e-142">**A series of lab tests is performed**   The Lync administrator team must perform test updates on a server in a test environment to decide whether the service pack can be applied successfully without affecting any of the installed applications and server systems.</span></span> <span data-ttu-id="98e9e-143">如果存在与在生产环境中使用 Lync Server 的第三方或内部创建的应用程序，也应该对这些应用程序进行测试。</span><span class="sxs-lookup"><span data-stu-id="98e9e-143">If there are third-party or internally created applications that interface with Lync Server in a production environment, these should be also tested.</span></span> <span data-ttu-id="98e9e-144">这些测试还可以用于估计执行升级所需的时间。</span><span class="sxs-lookup"><span data-stu-id="98e9e-144">These tests can also be used to estimate the time that is required to perform the upgrades.</span></span>

  - <span data-ttu-id="98e9e-145">**通知用户停机**   Lync 管理员团队、通信团队或用户帮助桌面通知所有受影响的用户有关计划内维护周期以及服务将不可用的时间。</span><span class="sxs-lookup"><span data-stu-id="98e9e-145">**Users are informed of the outage**   The Lync administrator team, communications team, or user help desk informs all affected users about the planned maintenance cycle and how long the service will be unavailable.</span></span>

  - <span data-ttu-id="98e9e-146">**升级前执行 Lync 的完整备份**   如果服务包安装失败，Lync 管理员团队必须验证是否有有效的备份可用于还原到原始系统状态。</span><span class="sxs-lookup"><span data-stu-id="98e9e-146">**A full backup of Lync is performed before the upgrade**   The Lync administrator team must verify that there is a valid backup that can be used to revert to the original system state if the service pack installation fails.</span></span> <span data-ttu-id="98e9e-147">我们建议将备份还原到备用服务器，以使此系统在出现问题时随时可用。</span><span class="sxs-lookup"><span data-stu-id="98e9e-147">We recommend that the backup be restored to a standby server to have this system readily available if there are issues.</span></span>

  - <span data-ttu-id="98e9e-148">**累积更新已部署**   Lync 管理员团队在计划的维护周期内执行安装。</span><span class="sxs-lookup"><span data-stu-id="98e9e-148">**The cumulative update is deployed**   The Lync administrator team does the installation during the planned maintenance cycle.</span></span>

<div>

## <a name="managing-the-timing-of-changes"></a><span data-ttu-id="98e9e-149">管理更改的计时</span><span class="sxs-lookup"><span data-stu-id="98e9e-149">Managing the timing of changes</span></span>

<span data-ttu-id="98e9e-150">我们建议你实施用于计划更改的过程，以避免工作的重叠部分中断。</span><span class="sxs-lookup"><span data-stu-id="98e9e-150">We recommend that you implement a procedure for scheduling changes to avoid disruptions in overlapping sections of your work.</span></span> <span data-ttu-id="98e9e-151">例如，两个团队可能都在规划对系统的少许更改。</span><span class="sxs-lookup"><span data-stu-id="98e9e-151">For example, two teams may both be planning a minor change to a system.</span></span> <span data-ttu-id="98e9e-152">一个团队可能在另一个团队将旧用户迁移到该池中时在池中应用累积更新。</span><span class="sxs-lookup"><span data-stu-id="98e9e-152">One team may be applying a cumulative update on a pool while another team is migrating legacy users into that pool.</span></span> <span data-ttu-id="98e9e-153">其他团队正在计划的更改不会影响任何团队，并且每个团队可能不一定知道另一个团队正在计划的更改。</span><span class="sxs-lookup"><span data-stu-id="98e9e-153">Neither team is affected by the changes that the other team is planning, and each team may not necessarily know about changes that the other team is planning.</span></span> <span data-ttu-id="98e9e-154">如果同时发生这两个更改，则可能会在执行更改时出现问题。</span><span class="sxs-lookup"><span data-stu-id="98e9e-154">If both changes occurred at the same time, there might be issues implementing the changes.</span></span> <span data-ttu-id="98e9e-155">此外，如果在应用更改后出现问题，例如，如果用户迁移失败，可能很难确定应回滚哪些更改。</span><span class="sxs-lookup"><span data-stu-id="98e9e-155">Also, if there are issues after the changes were applied, for example, if the user migration fails, it may be difficult to decide which change should be rolled back.</span></span> <span data-ttu-id="98e9e-156">应在 IT 和管理之间设置定期维护期间，以测试更改并接受这些更改。</span><span class="sxs-lookup"><span data-stu-id="98e9e-156">There should be regular maintenance periods set up between IT and management to test the changes and accept them.</span></span>

<span data-ttu-id="98e9e-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98e9e-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

