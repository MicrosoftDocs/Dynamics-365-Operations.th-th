---
title: Add-in การมองเห็นสินค้าคงคลัง
description: หัวข้อนี้จะอธิบายวิธีการติดตั้งและตั้งค่าคอนฟิกAdd-in การมองเห็นสินค้าคงคลังสำหรับ Dynamics 365 Supply Chain Management
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e294ada8dd3e764987aa363adb2614416986575b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821140"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="2f9d2-103">Add-in การมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="2f9d2-104">Add-in การมองเห็นสินค้าคงคลังเป็น microservice อิสระและปรับสเกลได้อย่างมาก ซึ่งเปิดใช้งานการติดตามปริมาณคงคลังคงเหลือในเวลาจริง จึงให้มุมมองส่วนกลางของการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="2f9d2-105">ข้อมูลทั้งหมดที่เกี่ยวข้องกับปริมาณคงคลังคงเหลือจะถูกส่งออกไปยังบริการใกล้เคียงเวลาจริงผ่านการรวม SQL ในระดับต่ำ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="2f9d2-106">ระบบภายนอกเข้าถึงบริการผ่าน RESTful APIs เพื่อสอบถามข้อมูลปริมาณคงคลังคงเหลือในชุดของมิติที่กำหนด ดังนั้นจึงดึงข้อมูลรายการของตำแหน่งในปริมาณคงคลังคงเหลือที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="2f9d2-107">การแสดงผลสินค้าคงคลังเป็น microservice ที่สร้างขึ้นบน Microsoft Dataverse ซึ่งหมายความว่า คุณสามารถขยายได้โดยการสร้าง Power Apps และการใช้ Power BI เพื่อให้ฟังก์ชันการทำงานที่กำหนดเองตรงกับความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="2f9d2-108">นอกจากนี้ คุณยังสามารถอัปเกรดดัชนีเพื่อทำการสอบถามสินค้าคงคลังได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="2f9d2-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="2f9d2-109">ความสามารถในการมองเห็นสินค้าคงคลังจะให้ตัวเลือกการตั้งค่าคอนฟิกซึ่งช่วยให้สามารถรวมกับระบบต่างๆ ของบุคคลที่สามได้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="2f9d2-110">ซึ่งสนับสนุนมิติสินค้าคงคลังมาตรฐาน ความสามารถที่กำหนดเอง และปริมาณที่มีการคำนวณซึ่งสามารถตั้งค่าคอนฟิกได้แบบมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="2f9d2-111">หัวข้อนี้จะอธิบายวิธีการติดตั้งและตั้งค่าคอนฟิก Add-in ความสามารถในการมองเห็นสินค้าคงคลังสำหรับ Dynamics 365 Supply Chain Management และวิธีใช้ Application Programming Interface (API)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="2f9d2-112">ติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="2f9d2-113">คุณจำเป็นต้องติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลังโดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="2f9d2-114">LCS เป็นพอร์ทัลการทำงานร่วมกันที่ให้สภาพแวดล้อมและชุดของบริการที่อัปเดตเป็นประจำ ซึ่งช่วยให้คุณสามารถจัดการวงจรการใช้งานแอปพลิเคชันของแอป Dynamics 365 Finance and Operations ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="2f9d2-115">สำหรับข้อมูลเพิ่มเติม ให้ดู [ทรัพยากร Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="2f9d2-116">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-116">Prerequisites</span></span>

<span data-ttu-id="2f9d2-117">ก่อนที่คุณจะสามารถติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง คุณต้องดำเนินการขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="2f9d2-118">รับโครงการสำหรับการใช้งาน LCS โดยมีสภาพแวดล้อมที่ปรับใช้อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="2f9d2-119">โปรดตรวจสอบให้แน่ใจว่ามีการตั้งค่า Add-in ของข้อกำหนดเบื้องต้น ใน [ภาพรวมของ Add-in](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) เสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="2f9d2-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="2f9d2-120">Inventory Visibility ไม่ต้องการการเชื่อมโยงแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="2f9d2-121">ติดต่อ Inventory Visibility Team ที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับไฟล์ที่ต้องการสามไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="2f9d2-122">`Inventory Visibility Integration.zip` (ถ้าเวอร์ชันของ Supply Chain Management ที่คุณรันอยู่เป็นรุ่นก่อนหน้าเวอร์ชัน 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="2f9d2-123">ประเทศและภูมิภาคที่ได้รับการสนับสนุนในปัจจุบัน ได้แก่ แคนาดา สหรัฐอเมริกา และสหภาพยุโรป (EU)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="2f9d2-124">ถ้าคุณมีคำถามใดๆ เกี่ยวกับข้อกำหนดเบื้องต้นเหล่านี้ โปรดติดต่อทีมงานผลิตภัณฑ์ของความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="2f9d2-125">ตั้งค่า Dataverse</span><span class="sxs-lookup"><span data-stu-id="2f9d2-125">Set up Dataverse</span></span>

<span data-ttu-id="2f9d2-126">ให้ดำเนินการตามขั้นตอนต่อไปนี้เพื่อตั้งค่า Dataverse</span><span class="sxs-lookup"><span data-stu-id="2f9d2-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="2f9d2-127">เพิ่มหลักการบริการให้กับผู้เช่าของคุณ:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="2f9d2-128">ติดตั้ง Azure AD PowerShell Module v2 ตามที่อธิบายไว้ใน [ติดตั้ง Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="2f9d2-129">โดยรันคำสั่ง PowerShell ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="2f9d2-130">สร้างผู้ใช้แอพลิเคชัน สำหรับ Inventory Visibility ใน Dataverse:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="2f9d2-131">เปิด URL ของสภาพแวดล้อม Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="2f9d2-132">ไปที่ **การตั้งค่าขั้นสูง \> ระบบ \> ความปลอดภัย \> ผู้ใช้** และสร้างผู้ใช้แอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="2f9d2-133">ใช้เมนูมุมมองเพื่อเปลี่ยนมุมมองหน้าเป็น **ผู้ใช้แอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="2f9d2-134">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-134">Select **New**.</span></span> <span data-ttu-id="2f9d2-135">ตั้งค่ารหัสแอพลิเคชัน เป็น *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*</span><span class="sxs-lookup"><span data-stu-id="2f9d2-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="2f9d2-136">(รหัสออบเจ็กต์จะถูกโหลดโดยอัตโนมัติเมื่อคุณบันทึกการเปลี่ยนแปลง) คุณสามารถปรับแต่งชื่อได้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="2f9d2-137">ตัวอย่างเช่น คุณสามารถเปลี่ยนเป็น *Inventory Visibility*</span><span class="sxs-lookup"><span data-stu-id="2f9d2-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="2f9d2-138">เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="2f9d2-139">เลือก **กําหนดบทบาท** แล้วเลือก **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="2f9d2-140">ถ้ามีบทบาทที่มีชื่อ **ผู้ใช้ Common Data Service** ให้เลือกบทบาทนั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="2f9d2-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="2f9d2-141">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างผู้ใช้แอพลิเคชัน](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="2f9d2-142">นําเข้าไฟล์ `Inventory Visibility Dataverse Solution.zip` ซึ่งประกอบด้วย เอนทิตี้ที่เกี่ยวข้องกับการตั้งค่าคอนฟิก Dataverse และ Power Apps</span><span class="sxs-lookup"><span data-stu-id="2f9d2-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="2f9d2-143">ไปที่หน้า **โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="2f9d2-144">เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-144">Select **Import**.</span></span>

1. <span data-ttu-id="2f9d2-145">นําเข้าโฟลว์ทริกเกอร์การอัปเกรดการตั้งค่าคอนฟิก:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="2f9d2-146">ไปที่หน้า Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="2f9d2-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="2f9d2-147">ตรวจสอบให้แน่ใจว่ามีการเชื่อมต่อที่ชื่อ *Dataverse (ดั้งเดิม)* อยู่</span><span class="sxs-lookup"><span data-stu-id="2f9d2-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="2f9d2-148">(ถ้าไม่มี ให้สร้างใหม่)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="2f9d2-149">นำเข้าไฟล์ `Inventory Visibility Configuration Trigger.zip`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="2f9d2-150">หลังจากนําเข้าแล้ว ทริกเกอร์จะปรากฏขึ้นภายใต้ **โฟลว์ของฉัน**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="2f9d2-151">เริ่มต้นตัวแปรสี่ตัวต่อไปนี้ ตามข้อมูลสภาพแวดล้อม:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="2f9d2-152">รหัสผู้เช่า Azure</span><span class="sxs-lookup"><span data-stu-id="2f9d2-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="2f9d2-153">รหัสไคลเอนต์แอปพลิเคชัน Azure</span><span class="sxs-lookup"><span data-stu-id="2f9d2-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="2f9d2-154">ข้อมูลลับไคลเอนต์แอปพลิเคชัน Azure</span><span class="sxs-lookup"><span data-stu-id="2f9d2-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="2f9d2-155">ปลายทางการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="2f9d2-156">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวแปรนี้ โปรดดูที่ส่วน [ตั้งค่าการรวมการแสดงผลสินค้าคงคลัง](#setup-inventory-visibility-integration) ในตอนท้ายของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="2f9d2-157">![ทริกเกอร์การตั้งค่าคอนฟิก](media/configuration-trigger.png "ทริกเกอร์การตั้งค่าคอนฟิก")</span><span class="sxs-lookup"><span data-stu-id="2f9d2-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="2f9d2-158">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="2f9d2-159">ติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="2f9d2-159">Install the add-in</span></span>

<span data-ttu-id="2f9d2-160">เพื่อติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง ต้องดำเนินการขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="2f9d2-161">ลงชื่อเข้าใช้พอร์ทัล [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="2f9d2-162">บนโฮมเพจ ให้เลือกโครงการที่มีการปรับใช้สภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="2f9d2-163">บนหน้าโครงการ ให้เลือกสภาพแวดล้อมที่คุณต้องการติดตั้ง add-in</span><span class="sxs-lookup"><span data-stu-id="2f9d2-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="2f9d2-164">ในหน้าสภาพแวดล้อม ให้เลื่อนลงจนกว่าคุณจะเห็นส่วน **Add-in ของสภาพแวดล้อม** ในส่วน **Power Platform การรวม** ที่คุณสามารถค้นหาชื่อสภาพแวดล้อม Dataverse ได้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="2f9d2-165">ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="2f9d2-166">![หน้าสภาพแวดล้อมใน LCS](media/inventory-visibility-environment.png "หน้าสภาพแวดล้อมใน LCS")</span><span class="sxs-lookup"><span data-stu-id="2f9d2-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="2f9d2-167">เลือกลิงก์ **ติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="2f9d2-168">รายการของ add-in ที่พร้อมใช้งานจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="2f9d2-169">เลือก **การแสดงผลสินค้าคงคลัง** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="2f9d2-170">ป้อนค่าสำหรับฟิลด์ต่อไปนี้สำหรับสภาพแวดล้อมของคุณ:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="2f9d2-171">**รหัส (ไคลเอนต์) แอปพลิเคชัน AAD**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="2f9d2-172">**รหัสผู้เช่า AAD**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="2f9d2-173">![หน้าการตั้งค่าของ Add in](media/inventory-visibility-setup.png "หน้าการตั้งค่าของ Add in")</span><span class="sxs-lookup"><span data-stu-id="2f9d2-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="2f9d2-174">ยอมรับข้อกำหนดและเงื่อนไขโดยเลือกกล่องกาเครื่องหมาย **ข้อกำหนดและเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="2f9d2-175">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-175">Select **Install**.</span></span> <span data-ttu-id="2f9d2-176">สถานะของ add-in จะแสดงเป็น **กำลังติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="2f9d2-177">เมื่อเสร็จสิ้นแล้ว ให้รีเฟรชหน้าเพื่อดูการเปลี่ยนแปลงสถานะเป็น **ติดตั้งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="2f9d2-178">ถอนการติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="2f9d2-178">Uninstall the add-in</span></span>

<span data-ttu-id="2f9d2-179">เมื่อต้องการถอนการติดตั้ง add-in ให้เลือก **ถอนการติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="2f9d2-180">เมื่อคุณรีเฟรช LCS และ Add-in การแสดงผลสินค้าคงคลังจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="2f9d2-181">กระบวนการถอนการติดตั้งจะลบการลงทะเบียน Add-in และยังเริ่มต้นงานเพื่อล้างข้อมูลทางธุรกิจทั้งหมดที่จัดเก็บไว้ในบริการด้วย</span><span class="sxs-lookup"><span data-stu-id="2f9d2-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="2f9d2-182">ใช้ข้อมูลปริมาณคงคลังคงเหลือจาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2f9d2-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="2f9d2-183">ปรับใช้แพคเกจการรวมการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="2f9d2-184">ถ้าคุณรัน Supply Chain Management เวอร์ชัน 10.0.17 หรือก่อนหน้านั้น ให้ติดต่อทีมสนับสนุนการแสดงผลสินค้าคงคลัง ที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับไฟล์แพคเกจ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="2f9d2-185">แล้วปรับใช้แพคเกจใน LCS</span><span class="sxs-lookup"><span data-stu-id="2f9d2-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="2f9d2-186">ถ้าเกิดข้อผิดพลาดที่ไม่ตรงกันของเวอร์ชันระหว่างการปรับใช้ คุณต้องนําเข้าโครงการ X++ ด้วยตนเอง ลงในสภาพแวดล้อมการพัฒนาของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="2f9d2-187">จากนั้นสร้างแพคเกจที่สามารถปรับใช้งานได้ในสภาพแวดล้อมการพัฒนาของคุณ และปรับใช้ในสภาพแวดล้อมการทำงานจริงของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="2f9d2-188">รหัสถูกรวมอยู่กับ Supply Chain Management เวอร์ชัน 10.0.18</span><span class="sxs-lookup"><span data-stu-id="2f9d2-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="2f9d2-189">ถ้าคุณรันเวอร์ชันนั้นอยู่หรือเวอร์ชันที่ใหม่กว่า ไม่ต้องมีการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="2f9d2-190">ตรวจสอบให้แน่ใจว่าคุณลักษณะต่อไปนี้ได้เปิดใช้งานอยู่ในสภาพแวดล้อม Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="2f9d2-191">(โดยค่าเริ่มต้น จะเปิดใช้งาน)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="2f9d2-192">คำอธิบายลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-192">Feature description</span></span> | <span data-ttu-id="2f9d2-193">เวอร์ชันรหัส</span><span class="sxs-lookup"><span data-stu-id="2f9d2-193">Code version</span></span> | <span data-ttu-id="2f9d2-194">สลับคลาส</span><span class="sxs-lookup"><span data-stu-id="2f9d2-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="2f9d2-195">เปิดใช้งานหรือปิดใช้งานการใช้มิติสินค้าคงคลังในตาราง InventSum</span><span class="sxs-lookup"><span data-stu-id="2f9d2-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="2f9d2-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="2f9d2-196">10.0.11</span></span> | <span data-ttu-id="2f9d2-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="2f9d2-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="2f9d2-198">เปิดใช้งานหรือปิดใช้งานการใช้มิติสินค้าคงคลังในตาราง InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="2f9d2-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="2f9d2-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="2f9d2-199">10.0.12</span></span> | <span data-ttu-id="2f9d2-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="2f9d2-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="2f9d2-201">ตั้งค่าการรวมการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="2f9d2-202">ใน Supply Chain Management ให้เปิดพื้นที่ทำงาน **[การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** และเปิดคุณลักษณะ **การรวมการแสดงผลสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="2f9d2-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="2f9d2-203">ไปที่ **การจัดการสินค้าคงคลัง \> ตั้งค่า \> พารามิเตอร์การรวมการแสดงผลสินค้าคงคลัง** และป้อน URL ของสภาพแวดล้อมที่คุณรันการแสดงผลสินค้าคงคลังอยู่</span><span class="sxs-lookup"><span data-stu-id="2f9d2-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="2f9d2-204">ค้นหาภูมิภาค Azure ของสภาพแวดล้อม LCS ของคุณ แล้วป้อน URL</span><span class="sxs-lookup"><span data-stu-id="2f9d2-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="2f9d2-205">URL มีฟอร์มต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="2f9d2-206">ตัวอย่างเช่น ถ้าคุณอยู่ในยุโรป สภาพแวดล้อมของคุณจะมี URL อย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="2f9d2-207">ภูมิภาคต่อไปนี้พร้อมใช้งานในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="2f9d2-208">ภูมิภาคของ Azure</span><span class="sxs-lookup"><span data-stu-id="2f9d2-208">Azure region</span></span> | <span data-ttu-id="2f9d2-209">ชื่อย่อของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="2f9d2-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="2f9d2-210">ออสเตรเลียตะวันออก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-210">Australia east</span></span> | <span data-ttu-id="2f9d2-211">eau</span><span class="sxs-lookup"><span data-stu-id="2f9d2-211">eau</span></span> |
    | <span data-ttu-id="2f9d2-212">ออสเตรเลียตะวันออกเฉียงใต้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-212">Australia southeast</span></span> | <span data-ttu-id="2f9d2-213">seau</span><span class="sxs-lookup"><span data-stu-id="2f9d2-213">seau</span></span> |
    | <span data-ttu-id="2f9d2-214">แคนาดากลาง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-214">Canada central</span></span> | <span data-ttu-id="2f9d2-215">cca</span><span class="sxs-lookup"><span data-stu-id="2f9d2-215">cca</span></span> |
    | <span data-ttu-id="2f9d2-216">แคนาดาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-216">Canada east</span></span> | <span data-ttu-id="2f9d2-217">eca</span><span class="sxs-lookup"><span data-stu-id="2f9d2-217">eca</span></span> |
    | <span data-ttu-id="2f9d2-218">ยุโรปเหนือ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-218">North Europe</span></span> | <span data-ttu-id="2f9d2-219">neu</span><span class="sxs-lookup"><span data-stu-id="2f9d2-219">neu</span></span> |
    | <span data-ttu-id="2f9d2-220">ยุโรปตะวันตก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-220">West Europe</span></span> | <span data-ttu-id="2f9d2-221">weu</span><span class="sxs-lookup"><span data-stu-id="2f9d2-221">weu</span></span> |
    | <span data-ttu-id="2f9d2-222">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-222">East US</span></span> | <span data-ttu-id="2f9d2-223">eus</span><span class="sxs-lookup"><span data-stu-id="2f9d2-223">eus</span></span> |
    | <span data-ttu-id="2f9d2-224">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-224">West US</span></span> | <span data-ttu-id="2f9d2-225">wus</span><span class="sxs-lookup"><span data-stu-id="2f9d2-225">wus</span></span> |

1. <span data-ttu-id="2f9d2-226">ไปที่ **การจัดการสินค้าคงคลัง \> ประจำงวด \> การรวมการแสดงผลสินค้าคงคลัง** และเปิดใช้งานงาน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="2f9d2-227">ขณะนี้เหตุการณ์การเปลี่ยนแปลงสินค้าคงคลังทั้งหมดจาก Supply Chain Management จะถูกลงรายการบัญชีไปยังการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="2f9d2-228">API สาธารณะของ Add-in การแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="2f9d2-229">REST API สาธารณะของ Add-in การแสดงผลสินค้าคงคลัง แสดงถึงปลายทางเฉพาะสำหรับการรวมหลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="2f9d2-230">ซึ่งสนับสนุนชนิดการโต้ตอบหลักสามชนิด:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="2f9d2-231">การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปที่ add-in จากระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="2f9d2-232">การสอบถามปริมาณคงคลังคงเหลือปัจจุบันจากระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="2f9d2-233">การซิงโครไนส์อัตโนมัติกับ Supply Chain Management สินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="2f9d2-234">การซิงโครไนส์อัตโนมัติไม่ได้เป็นส่วนหนึ่งของ API สาธารณะ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="2f9d2-235">แต่จะถูกจัดการในพื้นหลังของสภาพแวดล้อมซึ่งเปิดใช้งาน Add-in ของการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="2f9d2-236">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-236">Authentication</span></span>

<span data-ttu-id="2f9d2-237">โทเคนความปลอดภัยของแพลตฟอร์มจะใช้ในการเรียก Add-in ของการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="2f9d2-238">ดังนั้น คุณจึงต้องสร้างโทเคน *Azure Active Directory (Azure AD)* โดยใช้แอพลิเคชัน Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="2f9d2-239">จากนั้นคุณต้องใช้โทเคน Azure AD เพื่อรับ *การเข้าถึงโทเคน* จากบริการความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="2f9d2-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="2f9d2-240">รับโทเคนบริการรักษาความปลอดภัย โดยทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="2f9d2-241">ล็อกอินเข้าสู่พอร์ทัล Azure และใช้งาน เพื่อค้นหา `clientId` และ `clientSecret` สำหรับแอพลิเคชัน Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="2f9d2-242">การดึงข้อมูลโทเค็น Azure Active Directory (`aadToken`) โดยการส่งการร้องขอ HTTP มีคุณสมบัติต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="2f9d2-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="2f9d2-244">**วิธีการ** - `GET`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="2f9d2-245">**ตัวเนื้อหา (ข้อมูลแบบฟอร์ม)**:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="2f9d2-246">คีย์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-246">key</span></span> | <span data-ttu-id="2f9d2-247">ค่า</span><span class="sxs-lookup"><span data-stu-id="2f9d2-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="2f9d2-248">รหัส_ไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-248">client_id</span></span> | <span data-ttu-id="2f9d2-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="2f9d2-249">${aadAppId}</span></span> |
        | <span data-ttu-id="2f9d2-250">ข้อมูลลับ_ไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-250">client_secret</span></span> | <span data-ttu-id="2f9d2-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="2f9d2-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="2f9d2-252">ชนิด_การให้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-252">grant_type</span></span> | <span data-ttu-id="2f9d2-253">ข้อมูลประจำตัว_ไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-253">client_credentials</span></span> |
        | <span data-ttu-id="2f9d2-254">ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2f9d2-254">resource</span></span> | <span data-ttu-id="2f9d2-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="2f9d2-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="2f9d2-256">คุณควรได้รับ `aadToken` ในการตอบสนอง ซึ่งคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="2f9d2-257">สร้างการร้องขอ JSON ที่คล้ายกับสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-257">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="2f9d2-258">ที่ใด:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-258">Where:</span></span>
    - <span data-ttu-id="2f9d2-259">ค่า `client_assertion` ต้องเป็น `aadToken` ที่คุณได้รับในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="2f9d2-260">ค่า `context` ต้องเป็นรหัสสภาพแวดล้อมที่คุณต้องการปรับใช้ Add-in</span><span class="sxs-lookup"><span data-stu-id="2f9d2-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="2f9d2-261">ตั้งค่าอื่นๆ ทั้งหมด ตามที่แสดงในตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="2f9d2-262">ส่งการร้องขอ HTTP ที่มีคุณสมบัติต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="2f9d2-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="2f9d2-264">**วิธีการ** - `POST`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="2f9d2-265">**ส่วนหัว HTTP** - รวมถึงเวอร์ชันของ API (คีย์คือ `Api-Version` และค่าเป็น `1.0`)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="2f9d2-266">**ตัวเนื้อหา** - รวมถึงการร้องขอ JSON ที่คุณสร้างในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="2f9d2-267">คุณจะได้รับ `access_token` ในการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="2f9d2-268">นี่คือสิ่งที่คุณต้องการในฐานะโทเคนผู้ถือสิทธิ์เพื่อเรียก API ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="2f9d2-269">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="2f9d2-270">ตั้งค่าคอนฟิก API ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="2f9d2-271">ก่อนที่จะใช้บริการ คุณต้องทำการตั้งค่าคอนฟิกที่อธิบายไว้ในส่วนย่อยต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="2f9d2-272">การตั้งค่าคอนฟิกอาจแตกต่างกันไปตามรายละเอียดของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="2f9d2-273">ส่วนใหญ่แล้วประกอบด้วยสี่ส่วน:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="2f9d2-274">การแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="2f9d2-275">การตั้งค่าคอนฟิกมิติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="2f9d2-276">การจัดทำดัชนี</span><span class="sxs-lookup"><span data-stu-id="2f9d2-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="2f9d2-277">การวัดแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="2f9d2-278">การแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-278">Partitioning</span></span>

<span data-ttu-id="2f9d2-279">การแบ่งพาร์ติชันสามารถมีผลกระทบต่อประสิทธิภาพการทำงานของ API ความสามารถในการมองเห็นสินค้าคงคลังได้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="2f9d2-280">ขอแนะนำให้คุณกำหนดโครงร่างที่อนุญาตให้มีการจัดกลุ่มข้อมูลเล็กๆ ในขณะที่ยังคงอนุญาตให้มีการสอบถามข้อมูลที่มีความหมาย</span><span class="sxs-lookup"><span data-stu-id="2f9d2-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="2f9d2-281">`organizationId` (`dataAreaId` ใน Supply Chain Management) จะเป็นส่วนหนึ่งของการแบ่งพาร์ติชันเสมอ และตามค่าเริ่มต้น ความสามารถในการมองเห็นสินค้าคงคลังจะถูกตั้งค่าเป็นพาร์ติชันตามมิติเป็น *ไซต์ + สถานที่*</span><span class="sxs-lookup"><span data-stu-id="2f9d2-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="2f9d2-282">นี่หมายความว่าบริการต้องมีการสอบถามเสมอด้วยมิติเหล่านี้ที่กำหนดไว้ในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="2f9d2-283">*ไซต์* และ *สถานที่* เป็นมิติเริ่มต้นทั่วไปสองมิติในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="2f9d2-284">ใน Supply Chain Management มิติเหล่านี้เรียกว่า *ไซต์* (`InventSiteId`) และ *คลังสินค้า* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="2f9d2-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="2f9d2-285">การตั้งค่าคอนฟิกมิติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-285">Dimension configurations</span></span>

<span data-ttu-id="2f9d2-286">ความสามารถในการมองเห็นสินค้าคงคลังจะแสดงรายการของมิติเริ่มต้นทั่วไป เพื่อเปิดใช้งานการรวมระบบแหล่งที่มาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="2f9d2-287">ตารางต่อไปนี้แสดงรายการมิติสินค้าคงคลังที่จะเป็นชื่อมิติเริ่มต้นในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="2f9d2-288">ชนิดมิติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-288">Dimension type</span></span> | <span data-ttu-id="2f9d2-289">ชื่อมิติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="2f9d2-290">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="2f9d2-291">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="2f9d2-292">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="2f9d2-293">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="2f9d2-294">การติดตาม</span><span class="sxs-lookup"><span data-stu-id="2f9d2-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="2f9d2-295">การติดตาม</span><span class="sxs-lookup"><span data-stu-id="2f9d2-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="2f9d2-296">ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="2f9d2-297">ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="2f9d2-298">สถานะของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="2f9d2-299">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="2f9d2-300">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="2f9d2-301">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="2f9d2-302">ชนิดของมิติที่แสดงรายการอยู่ในตารางก่อนหน้านี้ใช้สำหรับการอ้างอิงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="2f9d2-303">คุณไม่จำเป็นต้องกำหนดชนิดมิติในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="2f9d2-304">ถ้ามีมิติที่กำหนดเองอยู่และจำเป็นต้องโฟลว์ไปยังค่าเริ่มต้น เมื่อมีการใช้งานโดยความสามารถในการมองเห็นสินค้าคงคลัง คุณสามารถตั้งค่าคอนฟิก **ชื่อมิติที่กำหนดเอง** ในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="2f9d2-305">ระบบภายนอกเข้าถึงความสามารถในการมองเห็นสินค้าคงคลังผ่าน RESTful APIs ที่เปิดใช้งานข้อมูลปริมาณคงคลังคงเหลือในชุดที่กำหนดของมิติที่จะมีการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="2f9d2-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="2f9d2-306">สำหรับการรวม ความสามารถในการมองเห็นสินค้าคงคลังจะช่วยให้คุณสามารถตั้งค่าคอนฟิก *แหล่งข้อมูลช่องทางภายนอก* และมิติแหล่งที่มาเป็น *มิติเป้าหมาย* ในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="2f9d2-307">มิติเป้าหมายควรเป็นหนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="2f9d2-308">มิติเริ่มต้นในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="2f9d2-309">มิติที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-309">Custom dimensions</span></span>

<span data-ttu-id="2f9d2-310">วัตถุประสงค์ของการตั้งค่าคอนฟิกมิติคือ การกำหนดมาตรฐานการรวมหลายระบบสำหรับการสอบถามบนมิติและเหตุการณ์การโพสต์กับมิติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="2f9d2-311">การจัดทำดัชนี</span><span class="sxs-lookup"><span data-stu-id="2f9d2-311">Indexing</span></span>

<span data-ttu-id="2f9d2-312">ส่วนใหญ่การสอบถามปริมาณคงคลังคงเหลือไม่เพียงแค่อยู่ที่ระดับ "ยอดรวม" สูงสุด แต่คุณอาจต้องการดูผลลัพธ์ที่รวมโดยยึดตามมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="2f9d2-313">ความสามารถในการมองเห็นสินค้าคงคลังให้ความยืดหยุ่นโดยการอนุญาตให้คุณตั้งค่าดัชนี ซึ่งขึ้นอยู่กับมิติหรือชุดของมิติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="2f9d2-314">ในขณะนี้ คุณสามารถตั้งค่าคอนฟิกดัชนีได้สูงสุดห้ารายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="2f9d2-315">คุณต้องคำนึงถึงมิติหรือชุดของมิติที่คุณจะใช้ก่อนที่จะดำเนินการ เพื่อให้มั่นใจว่าจะตอบสนองความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="2f9d2-316">ตัวอย่างเช่น ถ้าคุณต้องการสอบถามผลิตภัณฑ์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="2f9d2-317">สอบถามปริมาณคงคลังคงเหลือของผลิตภัณฑ์แบบรวมตามมิติ *สี* และ *ขนาด*</span><span class="sxs-lookup"><span data-stu-id="2f9d2-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="2f9d2-318">ในบางกรณี คุณต้องการสอบถามเกี่ยวกับผลิตภัณฑ์โดยรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="2f9d2-319">คุณจะกำหนดดัชนีสองรายการดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="2f9d2-320">วงเล็บที่ว่างเปล่าจะรวมกันตามรหัสผลิตภัณฑ์ภายในการแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="2f9d2-321">การจัดทำดัชนีจะกำหนดวิธีการที่คุณสามารถจัดกลุ่มผลลัพธ์ของคุณตามการตั้งค่าการสอบถาม `groupBy`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="2f9d2-322">ในกรณีนี้ ถ้าคุณไม่ได้กำหนดค่า `groupBy` ใดๆ คุณจะได้รับผลรวมตาม `productid`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="2f9d2-323">มิฉะนั้น ถ้าคุณกำหนด `groupBy` เป็น `groupBy=ColorId&groupBy=SizeId` คุณจะได้รับบรรทัดหลายบรรทัดที่ส่งคืน โดยยึดตามชุดสีและขนาดต่างๆ ในระบบ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="2f9d2-324">คุณสามารถกำหนดเกณฑ์การสอบถามของคุณในเนื้อหาของคำขอ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="2f9d2-325">ต่อไปนี้เป็นการสอบถามตัวอย่างเกี่ยวกับผลิตภัณฑ์ที่มีชุดสีและขนาด</span><span class="sxs-lookup"><span data-stu-id="2f9d2-325">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="2f9d2-326">การวัดแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-326">Custom measurement</span></span>

<span data-ttu-id="2f9d2-327">ปริมาณการประเมินเริ่มต้นจะเชื่อมโยงกับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2f9d2-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="2f9d2-328">อย่างไรก็ตาม คุณอาจต้องการมีปริมาณที่รวมกันของชุดการประเมินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="2f9d2-329">เมื่อต้องการดำเนินการนี้ คุณสามารถมีการตั้งค่าคอนฟิกของปริมาณที่กำหนดเอง ซึ่งจะถูกเพิ่มเข้าไปในผลลัพธ์ของการสอบถามปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="2f9d2-330">ฟังก์ชันนี้จะช่วยให้คุณสามารถกำหนดชุดของการวัดที่จะเพิ่ม และ/หรือชุดของการวัดที่จะถูกลบ เพื่อสร้างการวัดที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="2f9d2-331">ตัวอย่างเช่น ด้วยเงื่อนไขการสอบถามต่อไปนี้ คุณจะตั้งค่าคอนฟิกปริมาณการวัดแบบกำหนดเองเป็น `MyCustomAvailableforReservation` ที่จะใช้โดยระบบปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="2f9d2-332">ระบบปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-332">Consumption system</span></span> | <span data-ttu-id="2f9d2-333">ผู้วัดที่มีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-333">Calculated measurers</span></span> | <span data-ttu-id="2f9d2-334">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2f9d2-334">Data source</span></span> | <span data-ttu-id="2f9d2-335">ตัวแก้ไข</span><span class="sxs-lookup"><span data-stu-id="2f9d2-335">Modifier</span></span> | <span data-ttu-id="2f9d2-336">ชนิดการคำนวณของตัวแก้ไข</span><span class="sxs-lookup"><span data-stu-id="2f9d2-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="2f9d2-337">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="2f9d2-338">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="2f9d2-339">การลบ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="2f9d2-340">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="2f9d2-341">การลบ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="2f9d2-342">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="2f9d2-343">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="2f9d2-344">การลบ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="2f9d2-345">การลบ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-345">Subtraction</span></span> |

<span data-ttu-id="2f9d2-346">การสอบถามในปริมาณการวัดที่กำหนดเองจะส่งคืนผลลัพธ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="2f9d2-347">ผลลัพธ์ `MyCustomAvailableforReservation` จะขึ้นอยู่กับการตั้งค่าการคำนวณในการวัดที่กำหนดเองเป็น:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="2f9d2-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="2f9d2-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="2f9d2-349">การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-349">Posting on-hand changes</span></span>

<span data-ttu-id="2f9d2-350">URL ที่แน่นอนซึ่งจะมีการโพสต์เหตุการณ์ จะขึ้นอยู่กับภูมิภาคทางภูมิศาสตร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="2f9d2-351">ซึ่งจะใช้ฟอร์ม:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="2f9d2-352">เมื่อมีการพิสูจน์ตัวจริง สามารถใช้ URL นี้พร้อมกับวิธีการ HTTP `POST` เพื่อส่งเหตุการณ์ของการเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปยังบริการ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="2f9d2-353">ส่วนหัวพิเศษจะถูกใช้สำหรับการสื่อสารกับบริการ Dynamics 365 ผ่านคำขอ HTTP ซึ่งแสดงรหัสสภาพแวดล้อมของอินสแตนซ์ Supply Chain Management ที่ข้อมูลถูกลิงค์ไปถึง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="2f9d2-354">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="2f9d2-355">การโพสต์ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือ 1</span><span class="sxs-lookup"><span data-stu-id="2f9d2-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="2f9d2-356">ตัวอย่างนี้แสดงสถานการณ์จำลองที่คุณจะตั้งค่าการตั้งค่าคอนฟิกมิติใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="2f9d2-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="2f9d2-357">ใช้การสอบถามต่อไปนี้เพื่อตั้งค่าคอนฟิกการแม็ปมิติใน Power Apps:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="2f9d2-358">ขณะนี้คุณสามารถระบุ `dimensionDataSource` และใช้มิติที่กำหนดเองในการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="2f9d2-359">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="2f9d2-360">การโพสต์ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือ 2</span><span class="sxs-lookup"><span data-stu-id="2f9d2-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="2f9d2-361">ตัวอย่างนี้แสดงสถานการณ์จำลองที่ไม่มีการตั้งค่าการแม็ปสำหรับการตั้งค่าคอนฟิกมิติใน Power Apps ดังนั้นการโพสต์ยังควรใช้มิติพื้นฐานด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="2f9d2-362">มิติทั้งหมดต้องเป็นมิติฐาน เมื่อฟิลด์ `dimensionDataSource` เป็น null ว่างเปล่า หรือช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="2f9d2-363">คุณสมบัติฟิลด์ของเอกสาร JSON</span><span class="sxs-lookup"><span data-stu-id="2f9d2-363">JSON document field properties</span></span>

<span data-ttu-id="2f9d2-364">ฟิลด์จากตัวอย่างการสอบถาม JSON ที่ให้ไว้ก่อนหน้านี้ มีคุณสมบัติที่แสดงรายการอยู่ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="2f9d2-365">ฟิลด์ ID</span><span class="sxs-lookup"><span data-stu-id="2f9d2-365">Field ID</span></span> | <span data-ttu-id="2f9d2-366">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2f9d2-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="2f9d2-367">รหัสเฉพาะสำหรับเหตุการณ์การเปลี่ยนแปลงเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="2f9d2-368">รหัสนี้จะใช้เพื่อให้แน่ใจว่า ถ้าการสื่อสารกับบริการล้มเหลวในระหว่างการโพสต์ การส่งเหตุการณ์อีกครั้งจะไม่มีผลในเหตุการณ์เดียวกันที่ถูกนับสองครั้งในระบบ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="2f9d2-369">ตัวระบุขององค์กรที่ลิงก์ไปยังเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="2f9d2-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="2f9d2-370">นี่จะแม็ปไปยังองค์กร Supply Chain Management หรือรหัสพื้นที่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2f9d2-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="2f9d2-371">ตัวระบุของผลิตภัณฑ์ที่สงสัย</span><span class="sxs-lookup"><span data-stu-id="2f9d2-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="2f9d2-372">ปริมาณที่ต้องมีการเปลี่ยนแปลงปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="2f9d2-373">ตัวอย่างเช่น ถ้าตัวอย่างเช่น เบเกิลใหม่ 10 ชิ้นถูกเพิ่มไปยังชั้นวาง ค่านี้จะเป็น 10</span><span class="sxs-lookup"><span data-stu-id="2f9d2-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="2f9d2-374">ถ้าเบเกิล 3 ชิ้นถูกเอาออกจากชั้นวางหรือขายแล้ว ค่านี้จะเป็น -3</span><span class="sxs-lookup"><span data-stu-id="2f9d2-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="2f9d2-375">แหล่งข้อมูลของมิติที่ใช้ในการโพสต์เหตุการณ์การเปลี่ยนแปลงและการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="2f9d2-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="2f9d2-376">ถ้าคุณระบุแหล่งข้อมูล คุณสามารถใช้มิติที่กำหนดเองจากแหล่งข้อมูลที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="2f9d2-377">ด้วยการตั้งค่าคอนฟิกมิติ ความสามารถในการมองเห็นสินค้าคงคลังสามารถแม็ปมิติที่กำหนดเองกับมิติเริ่มต้นทั่วไป</span><span class="sxs-lookup"><span data-stu-id="2f9d2-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="2f9d2-378">ถ้าไม่มีการระบุ `dimensionDataSource` คุณสามารถใช้มิติเริ่มต้นทั่วไปในการสอบถามของคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2f9d2-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="2f9d2-379">ถุงแบบไดนามิกของคู่คีย์/ค่า</span><span class="sxs-lookup"><span data-stu-id="2f9d2-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="2f9d2-380">การทำเช่นนี้จะแม็ปกับบางมิติใน Supply Chain Management แต่คุณยังสามารถเพิ่มมิติที่กำหนดเองได้ด้วย (เช่น *แหล่งที่มา*) ซึ่งอาจแสดงว่าเหตุการณ์นี้มาจาก Supply Chain Management หรือระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="2f9d2-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="2f9d2-381">การสอบถามปริมาณคงคลังคงเหลือปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-381">Querying current on-hand</span></span>

<span data-ttu-id="2f9d2-382">ปลายทางสำหรับการสอบถามปริมาณคงคลังคงเหลือปัจจุบันจะมี URL ที่คล้ายกัน:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="2f9d2-383">ซึ่งจะมีการสอบถามด้วยวิธีการ HTTP `POST`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="2f9d2-384">ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือปัจจุบัน 1</span><span class="sxs-lookup"><span data-stu-id="2f9d2-384">Current on-hand query example 1</span></span>

<span data-ttu-id="2f9d2-385">ตัวอย่างนี้แสดงสถานการณ์จำลองที่คุณดำเนินการการตั้งค่าคอนฟิกมิติเสร็จสมบูรณ์แล้วใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="2f9d2-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="2f9d2-386">ใช้การสอบถามต่อไปนี้เพื่อตั้งค่าคอนฟิกการแม็ปมิติใน Power Apps:</span><span class="sxs-lookup"><span data-stu-id="2f9d2-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="2f9d2-387">ขณะนี้คุณสามารถระบุ `dimensionDataSource` และใช้มิติที่กำหนดเองในการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="2f9d2-388">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="2f9d2-389">คุณสามารถระบุ `DimensionDataSource` ใน `filters` และระบุมิติที่กำหนดเองในทั้ง `filters` และ `groupByValues`</span><span class="sxs-lookup"><span data-stu-id="2f9d2-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="2f9d2-390">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2f9d2-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="2f9d2-391">ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือปัจจุบัน 2</span><span class="sxs-lookup"><span data-stu-id="2f9d2-391">Current on-hand query example 2</span></span>

<span data-ttu-id="2f9d2-392">ตัวอย่างนี้แสดงสถานการณ์จำลองที่ไม่มีการตั้งค่าการแม็ปสำหรับการตั้งค่าคอนฟิกมิติใน Power Apps ดังนั้นการโพสต์ยังควรใช้มิติพื้นฐานด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="2f9d2-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="2f9d2-393">มิติทั้งหมดต้องเป็นมิติฐาน เมื่อฟิลด์ `dimensionDataSource` ภายใต้ `filters` เป็น null ว่างเปล่า หรือช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="2f9d2-394">ผลลัพธ์การส่งคืนตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-394">Example return result</span></span>

<span data-ttu-id="2f9d2-395">การสอบถามที่แสดงในตัวอย่างก่อนหน้านี้ อาจส่งผลให้เกิดผลลัพธ์ดังนี้</span><span class="sxs-lookup"><span data-stu-id="2f9d2-395">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="2f9d2-396">โปรดสังเกตว่าฟิลด์ปริมาณมีการจัดโครงสร้างเป็นพจนานุกรมของการวัดและค่าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2f9d2-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
