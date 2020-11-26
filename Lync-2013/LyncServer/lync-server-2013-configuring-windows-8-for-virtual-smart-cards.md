---
title: Lync Server 2013：为虚拟智能卡配置 Windows 8
description: Lync Server 2013：为虚拟智能卡配置 Windows 8。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Windows 8 for Virtual Smart Cards
ms:assetid: 4916c167-4ee3-4f3e-b65c-33e588595112
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308564(v=OCS.15)
ms:contentKeyID: 54973684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 112047f91a20dd552c628fb33eba7bb9ad3d0f01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432315"
---
# <a name="configuring-windows-8-for-using-virtual-smart-cards-with-lync-server-2013"></a><span data-ttu-id="2343a-103">配置用于将虚拟智能卡与 Lync Server 2013 结合使用的 Windows 8</span><span class="sxs-lookup"><span data-stu-id="2343a-103">Configuring Windows 8 for using Virtual Smart Cards with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2343a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2343a-104">

<span> </span></span></span>

<span data-ttu-id="2343a-105">_**主题上次修改时间：** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="2343a-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="2343a-106">部署双重身份验证和智能卡技术时要考虑的一个因素是实施成本。</span><span class="sxs-lookup"><span data-stu-id="2343a-106">One factor to consider when deploying two-factor authentication and smart card technology is the cost of implementation.</span></span> <span data-ttu-id="2343a-107">Windows 8 提供了许多新的安全功能，最有趣的新增功能之一是支持虚拟智能卡。</span><span class="sxs-lookup"><span data-stu-id="2343a-107">Windows 8 provides a number of new security capabilities, and one of the most interesting new features is support for virtual smart cards.</span></span>

<span data-ttu-id="2343a-108">对于配备了符合规范版本 1.2 要求的受信任的平台模块 (TPM) 芯片的计算机，组织现在可以享受智能卡登录带来的好处，不必在硬件方面做任何额外投资。</span><span class="sxs-lookup"><span data-stu-id="2343a-108">For computers equipped with a Trusted Platform Module (TPM) chip that meets specification version 1.2, organizations can now get the benefits of smart card logon without making any additional investments in hardware.</span></span> <span data-ttu-id="2343a-109">有关详细信息，请参阅在 Windows 8 中使用虚拟智能卡 [https://go.microsoft.com/fwlink/p/?LinkId=313365](https://go.microsoft.com/fwlink/p/?linkid=313365) 。</span><span class="sxs-lookup"><span data-stu-id="2343a-109">For more information, see Using Virtual Smart Cards with Windows 8 at [https://go.microsoft.com/fwlink/p/?LinkId=313365](https://go.microsoft.com/fwlink/p/?linkid=313365).</span></span>

<div>

## <a name="to-configure-windows-8-for-virtual-smart-cards"></a><span data-ttu-id="2343a-110">为 Windows 8 配置虚拟智能卡</span><span class="sxs-lookup"><span data-stu-id="2343a-110">To Configure Windows 8 for Virtual Smart Cards</span></span>

1.  <span data-ttu-id="2343a-111">使用启用了 Lync 的用户的凭据登录到 Windows 8 计算机。</span><span class="sxs-lookup"><span data-stu-id="2343a-111">Log in to the Windows 8 computer using the credentials of a Lync-enabled user.</span></span>

2.  <span data-ttu-id="2343a-112">在 Windows 8“开始”屏幕中，将您的光标移动到屏幕右下角。</span><span class="sxs-lookup"><span data-stu-id="2343a-112">At the Windows 8 Start screen, move your cursor to the bottom right corner of the screen.</span></span>

3.  <span data-ttu-id="2343a-113">选择“搜索”选项，然后搜索 **Command Prompt**。</span><span class="sxs-lookup"><span data-stu-id="2343a-113">Select the **Search** option, and then search for **Command Prompt**.</span></span>

4.  <span data-ttu-id="2343a-114">右键单击“命令提示符”，然后选择“以管理员身份运行”。</span><span class="sxs-lookup"><span data-stu-id="2343a-114">Right click on **Command Prompt**, and then select **Run as Administrator**.</span></span>

5.  <span data-ttu-id="2343a-115">通过以下命令打开受信任的平台模块 (TPM) 管理控制台：</span><span class="sxs-lookup"><span data-stu-id="2343a-115">Open the Trusted Platform Module (TPM) Management console by running the following command:</span></span>
    
        Tpm.msc

6.  <span data-ttu-id="2343a-116">从 TPM 管理控制台中，验证您的 TPM 规范版本是否至少为 1.2</span><span class="sxs-lookup"><span data-stu-id="2343a-116">From the TPM management console, verify that your TPM specification version is at least 1.2</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2343a-117">如果您收到一个对话框表明找不到兼容的受信任的平台模块 (TPM)，请验证计算机是否具有兼容的 TPM 模块以及是否在系统 BIOS 中启用了它。</span><span class="sxs-lookup"><span data-stu-id="2343a-117">If you receive a dialog stating that a Compatible Trust Platform Module (TPM) cannot be found, verify that the computer has a compatible TPM module and that it is enabled in the system BIOS.</span></span>

    
    </div>

7.  <span data-ttu-id="2343a-118">关闭 TPM 管理控制台</span><span class="sxs-lookup"><span data-stu-id="2343a-118">Close the TPM management console</span></span>

8.  <span data-ttu-id="2343a-119">从命令提示符处，使用以下命令创建新的虚拟智能卡：</span><span class="sxs-lookup"><span data-stu-id="2343a-119">From the command prompt, create a new virtual smart card using the following command:</span></span>
    
        TpmVscMgr create /name MyVSC /pin default /adminkey random /generate
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2343a-120">要在创建虚拟智能卡时提供自定义 PIN 值，请使用 /pin 提示符。</span><span class="sxs-lookup"><span data-stu-id="2343a-120">To provide a custom PIN value when creating the virtual smart card, use /pin prompt instead.</span></span>

    
    </div>

9.  <span data-ttu-id="2343a-121">从命令提示符处，通过运行以下命令来打开计算机管理控制台：</span><span class="sxs-lookup"><span data-stu-id="2343a-121">From the command prompt, open the Computer Management console by running the following command:</span></span>
    
        CompMgmt.msc

10. <span data-ttu-id="2343a-122">在计算机管理控制台中，选择“设备管理”。</span><span class="sxs-lookup"><span data-stu-id="2343a-122">In the Computer Management console, select **Device Management**.</span></span>

11. <span data-ttu-id="2343a-123">展开“智能卡读取器”。</span><span class="sxs-lookup"><span data-stu-id="2343a-123">Expand **Smart card readers**.</span></span>

12. <span data-ttu-id="2343a-124">验证是否已成功创建新的智能卡读取器。</span><span class="sxs-lookup"><span data-stu-id="2343a-124">Verify that the new virtual smart card reader has been created successfully.</span></span>

<span data-ttu-id="2343a-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2343a-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

