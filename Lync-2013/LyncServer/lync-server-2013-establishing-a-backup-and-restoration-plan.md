---
title: Lync Server 2013：建立备份和还原计划
description: Lync Server 2013：建立备份和还原计划。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Establishing a backup and restoration plan
ms:assetid: 9f562ef1-3804-41e2-b3e4-d45b2e8c63c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202183(v=OCS.15)
ms:contentKeyID: 51541499
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06d93c713364bf6b5f230b255b68a2c1dfe1d04a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428459"
---
# <a name="establishing-a-backup-and-restoration-plan-for-lync-server-2013"></a><span data-ttu-id="bc4ec-103">为 Lync Server 2013 建立备份和还原计划</span><span class="sxs-lookup"><span data-stu-id="bc4ec-103">Establishing a backup and restoration plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc4ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc4ec-104">

<span> </span></span></span>

<span data-ttu-id="bc4ec-105">_**主题上次修改时间：** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="bc4ec-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="bc4ec-106">创建备份和还原计划涉及以下步骤：</span><span class="sxs-lookup"><span data-stu-id="bc4ec-106">Creating a backup and restoration plan involves the following steps:</span></span>

  - <span data-ttu-id="bc4ec-107">制定计划。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-107">Developing the plan.</span></span>

  - <span data-ttu-id="bc4ec-108">实施计划。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-108">Implementing the plan.</span></span>

  - <span data-ttu-id="bc4ec-109">维护计划。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-109">Maintaining the plan.</span></span>

<div>

## <a name="developing-a-backup-and-restoration-plan"></a><span data-ttu-id="bc4ec-110">开发备份和还原计划</span><span class="sxs-lookup"><span data-stu-id="bc4ec-110">Developing a Backup and Restoration Plan</span></span>

<span data-ttu-id="bc4ec-111">开发 Lync Server 的备份和还原策略后，请使用它来记录详细的备份和还原计划。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-111">After you develop your backup and restoration strategy for Lync Server, use it to document a detailed backup and restoration plan.</span></span> <span data-ttu-id="bc4ec-112">你的计划应清楚地传达备份数据和设置的优先级和要求。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-112">Your plan should clearly convey the priorities and requirements for backing up data and settings.</span></span> <span data-ttu-id="bc4ec-113">你可以使用在[lync server 2013 的备份和还原工作表](lync-server-2013-backup-and-restoration-worksheets.md)中为[lync server 2013 和工作表建立备份和还原策略](lync-server-2013-establishing-a-backup-and-restoration-strategy.md)的信息，以便为你的策略提供文档。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-113">You can use the information in [Establishing a backup and restoration strategy for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-strategy.md) and the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md) to facilitate the documentation of your strategy.</span></span> <span data-ttu-id="bc4ec-114">你的计划还应包含用于确定何时以及如何还原服务的条件。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-114">Your plan should also contain criteria for deciding when and how to restore service.</span></span>

<span data-ttu-id="bc4ec-115">开发计划时，您需要考虑以下事项和帐户：</span><span class="sxs-lookup"><span data-stu-id="bc4ec-115">As you develop your plan, you need to consider, and account for, the following:</span></span>

  - <span data-ttu-id="bc4ec-116">将在新硬件上恢复服务器的方式。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-116">How you will recover servers on new hardware.</span></span>

  - <span data-ttu-id="bc4ec-117">如何恢复需要在多个业务领域或部门中执行操作的服务。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-117">How you will recover services that require action on the part of multiple business areas or departments.</span></span>

  - <span data-ttu-id="bc4ec-118">如何快速获取备用服务器。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-118">How you can acquire spare servers quickly.</span></span>

  - <span data-ttu-id="bc4ec-119">使用你的策略进行恢复所需的时间。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-119">The time it takes to recover by using your strategy.</span></span> <span data-ttu-id="bc4ec-120">考虑组织对恢复时间目标 (RTO) 的要求。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-120">Consider your organization’s requirements for recovery time objective (RTO).</span></span>

<span data-ttu-id="bc4ec-121">修改本主题中的备份和还原过程，根据需要添加和删除过程，以反映部署中的服务器和组件。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-121">Modify the backup and restoration procedures in this topic, adding and deleting procedures as appropriate, to reflect the servers and components in your deployment.</span></span> <span data-ttu-id="bc4ec-122">你还可以将相应的详细信息（如备份计划）添加到相应的过程，以确保信息不会被忽略。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-122">You can also add appropriate details, such as the backup schedule, to the appropriate procedures to make sure that the information is not overlooked.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bc4ec-123">最好为尽可能多的步骤创建脚本，以帮助确保过程的质量和 reproducibility。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-123">It is good practice to create scripts for as many steps as possible, to help ensure the quality and reproducibility of procedures.</span></span>



</div>

<span data-ttu-id="bc4ec-124">在你的计划中，指定负责检查计划的人员，负责测试和验证任何新过程或工具的人员，以及必须批准对计划和相关过程的任何更改的人员。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-124">In your plan, specify who is responsible for reviewing the plan, who is responsible for testing and validating any new procedures or tools, and who must approve any changes to the plan and related procedures.</span></span>

<span data-ttu-id="bc4ec-125">为确保你的备份和还原计划完全符合所有既定的目标和优先级，请在实施计划之前，获取组织中相应的业务决策制定者和技术决策者的批准。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-125">To make sure that your backup and restoration plan fully meets all established goals and priorities, get the approval of the appropriate business decision makers and technical decision makers in your organization before you implement the plan.</span></span>

</div>

<div>

## <a name="implementing-the-backup-and-restoration-plan"></a><span data-ttu-id="bc4ec-126">实施备份和还原计划</span><span class="sxs-lookup"><span data-stu-id="bc4ec-126">Implementing the Backup and Restoration Plan</span></span>

<span data-ttu-id="bc4ec-127">实现备份和还原计划需要执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="bc4ec-127">Implementing a backup and restoration plan requires the following steps:</span></span>

  - <span data-ttu-id="bc4ec-128">测试和验证计划。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-128">Testing and validating the plan.</span></span>

  - <span data-ttu-id="bc4ec-129">传达计划。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-129">Communicating the plan.</span></span>

  - <span data-ttu-id="bc4ec-130">验证备份和还原操作。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-130">Validating backup and restoration operations.</span></span>

<div>

## <a name="testing-and-validating-the-plan"></a><span data-ttu-id="bc4ec-131">测试和验证计划</span><span class="sxs-lookup"><span data-stu-id="bc4ec-131">Testing and Validating the Plan</span></span>

<span data-ttu-id="bc4ec-132">此处介绍的过程在实验室环境中经过测试和验证。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-132">The procedures described here have been tested and validated in a lab environment.</span></span> <span data-ttu-id="bc4ec-133">若要确保这些或任何其他过程在你的环境中正常工作，你应该测试并验证你要实现的每个过程。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-133">To make sure that these or any other procedures work in your environment, you should test and validate each procedure you intend to implement.</span></span> <span data-ttu-id="bc4ec-134">在提交最终审批计划之前完成测试和验证。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-134">Complete the testing and the validation before you submit your plan for final approval.</span></span>

</div>

<div>

## <a name="communicating-the-plan"></a><span data-ttu-id="bc4ec-135">传达计划</span><span class="sxs-lookup"><span data-stu-id="bc4ec-135">Communicating the Plan</span></span>

<span data-ttu-id="bc4ec-136">你的备份和还原计划应清楚地描述执行过程的执行者和执行步骤的分步说明。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-136">Your backup and restoration plan should clearly describe who implements procedures and step-by-step instructions for carrying out the procedures.</span></span> <span data-ttu-id="bc4ec-137">你应该确保负责备份和还原的任何方面的人了解计划、它的实现方式以及其角色。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-137">You should make sure that everyone responsible for any aspect of backup and restoration understands the plan, how it is to be implemented, and what their role is.</span></span> <span data-ttu-id="bc4ec-138">这包括以下各项的所有实现要求：</span><span class="sxs-lookup"><span data-stu-id="bc4ec-138">This includes all implementation requirements for the following:</span></span>

  - <span data-ttu-id="bc4ec-139">池和服务器备份。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-139">Pool and server backup.</span></span>

  - <span data-ttu-id="bc4ec-140">还原服务。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-140">Restoration of service.</span></span>

<span data-ttu-id="bc4ec-141">**池和服务器备份**</span><span class="sxs-lookup"><span data-stu-id="bc4ec-141">**Pool and server backup**</span></span>

<span data-ttu-id="bc4ec-142">备份和还原计划应包括定期完成备份过程所需的所有信息。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-142">The backup and restoration plan should include all information required to complete backup procedures on an ongoing basis.</span></span> <span data-ttu-id="bc4ec-143">要传达给负责团队成员的主要信息包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="bc4ec-143">The primary information to be communicated to responsible team members includes the following:</span></span>

  - <span data-ttu-id="bc4ec-144">团队或个人 (指定为负责备份每台服务器的个人或角色) 。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-144">Team or person (specified as an individual or role) responsible for backing up each server.</span></span>

  - <span data-ttu-id="bc4ec-145">备份每台服务器的特定计划。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-145">Specific schedules for backing up each server.</span></span>

  - <span data-ttu-id="bc4ec-146"> (设置、数据库和文件共享) 的每种数据类型的备份位置。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-146">Backup locations for each type of data (settings, database, and file shares).</span></span>

  - <span data-ttu-id="bc4ec-147">要使用的备份过程，包括完成每个过程所需的工具。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-147">Backup procedures to be used, including the tools required to complete each procedure.</span></span>

  - <span data-ttu-id="bc4ec-148">完成备份所需的信息，如 [Lync Server 2013 的备份和还原工作表](lync-server-2013-backup-and-restoration-worksheets.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-148">Information required to complete backups, as covered in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

  - <span data-ttu-id="bc4ec-149">用于帮助确保数据和设置得到适当备份并可供还原的验证方法，其中包括定期审核和测试还原。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-149">Validation methods to be used to help ensure that data and settings are appropriately backed up and available for restoration, which can include periodic audits and test restorations.</span></span>

<span data-ttu-id="bc4ec-150">**还原服务**</span><span class="sxs-lookup"><span data-stu-id="bc4ec-150">**Restoration of service**</span></span>

<span data-ttu-id="bc4ec-151">备份和还原计划应包括还原服务所需的所有信息，以防一个或多个服务器遇到导致服务不可用的损失。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-151">The backup and restoration plan should include all information required to restore service, in case one or more servers experience a loss that makes service unavailable.</span></span> <span data-ttu-id="bc4ec-152">要传达给负责团队成员的主要信息包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="bc4ec-152">The primary information to be communicated to responsible team members includes the following:</span></span>

  - <span data-ttu-id="bc4ec-153">团队或个人 (指定为负责确定何时需要还原服务的个人或角色) ，以及用于还原服务的过程以及负责为每个还原方案实施过程的团队或人员。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-153">Team or person (specified as an individual or a role) that is responsible for determining when restoration of service is required and the procedures to be used to restore service, and also the team or person responsible for implementing procedures for each restoration scenario.</span></span>

  - <span data-ttu-id="bc4ec-154">确定哪种还原过程最适合特定情况的标准。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-154">Criteria for determining which restoration procedures are most appropriate for a specific situation.</span></span>

  - <span data-ttu-id="bc4ec-155">有关还原服务和恢复时间目标的时间估计 (每个还原方案中的 RTO) 。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-155">Time estimates for restoration of service and recovery time objective (RTO) in each restoration scenario.</span></span>

  - <span data-ttu-id="bc4ec-156">要使用的还原过程，包括完成每个过程所需的工具。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-156">Restoration procedures to be used, including the tools required to complete each procedure.</span></span>

  - <span data-ttu-id="bc4ec-157">还原数据和设置所需的信息。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-157">Information required to restore data and settings.</span></span> <span data-ttu-id="bc4ec-158">在 [Lync Server 2013 的备份和还原工作表](lync-server-2013-backup-and-restoration-worksheets.md)中提供了工作表。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-158">Worksheets are provided in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

</div>

<div>

## <a name="validating-backup-and-restoration-operations"></a><span data-ttu-id="bc4ec-159">验证备份和还原操作</span><span class="sxs-lookup"><span data-stu-id="bc4ec-159">Validating Backup and Restoration Operations</span></span>

<span data-ttu-id="bc4ec-160">在你的生产环境中和指定的时间间隔内完成初始备份工作后， (在你的备份和还原计划) 中介绍的内容，应验证以下各项：</span><span class="sxs-lookup"><span data-stu-id="bc4ec-160">After completing initial backup efforts in your production environment and at specified intervals (as covered in your backup and restoration plan), you should verify the following:</span></span>

  - <span data-ttu-id="bc4ec-161">根据需要进行备份。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-161">Backups are occurring as required.</span></span>

  - <span data-ttu-id="bc4ec-162">备份的数据和设置可访问。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-162">Backed-up data and settings are accessible.</span></span>

  - <span data-ttu-id="bc4ec-163">可以在恢复时间目标中执行还原过程， (在备份和还原计划中指定的 RTO) 时间，结果满足所有业务需求。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-163">Restoration procedures can be performed within the recovery time objective (RTO) times specified in the backup and restoration plan, and the results meet all business requirements.</span></span>

  - <span data-ttu-id="bc4ec-164">备份工作表已完成并经过验证，它们存储在安全位置。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-164">Backup worksheets have been completed and verified, and they are stored in a secure location.</span></span> <span data-ttu-id="bc4ec-165">这些工作表在 [Lync Server 2013 的备份和还原工作表](lync-server-2013-backup-and-restoration-worksheets.md)中提供。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-165">These worksheets are provided in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

  - <span data-ttu-id="bc4ec-166">还原过程经测试和验证为按预期工作，如备份和还原计划中所指定。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-166">Restoration procedures have been tested and verified to work as expected, as specified in your backup and restoration plan.</span></span>

</div>

</div>

<div>

## <a name="maintaining-the-backup-and-restoration-plan"></a><span data-ttu-id="bc4ec-167">维护备份和还原计划</span><span class="sxs-lookup"><span data-stu-id="bc4ec-167">Maintaining the Backup and Restoration Plan</span></span>

<span data-ttu-id="bc4ec-168">Lync Server 拓扑是与你的组织更改的动态环境。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-168">A Lync Server topology is a dynamic environment that changes with your organization.</span></span> <span data-ttu-id="bc4ec-169">重新评估你的组织更改的备份和还原计划，并定期检查，以确保它能够继续满足你的业务需求。</span><span class="sxs-lookup"><span data-stu-id="bc4ec-169">Reassess your backup and restoration plan as your organization changes, and review it periodically to make sure that it continues to meet the needs of your business.</span></span>

<span data-ttu-id="bc4ec-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc4ec-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

