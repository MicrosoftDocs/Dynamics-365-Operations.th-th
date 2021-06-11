---
title: ตั้งค่ารหัสเหตุผล
description: Dynamics 365 Human Resources ใช้รหัสเหตุผลเพื่ออธิบายว่าเหตุใดสวัสดิการของพนักงานจึงเปลี่ยนไป
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc641233a1bd217de5b9eb6e06560b989f91c7b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056359"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="c3f9c-103">ตั้งค่ารหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="c3f9c-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c3f9c-104">Dynamics 365 Human Resources ใช้รหัสเหตุผลเพื่ออธิบายว่าเหตุใดสวัสดิการของพนักงานจึงเปลี่ยนไป</span><span class="sxs-lookup"><span data-stu-id="c3f9c-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="c3f9c-105">ณ วันที่ 2021 มกราคม รหัสเหตุผลย้ายไปยังพื้นที่ทำงาน **การจัดการบุคลากร** แทนพื้นที่ทำงาน **การจัดการสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="c3f9c-106">สำหรับข้อมูลเพิ่มเติม ให้ดู [ย้ายรหัสเหตุผลไปยังการจัดการบุคลากรด้วยตนเอง](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management)</span><span class="sxs-lookup"><span data-stu-id="c3f9c-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="c3f9c-107">สร้างรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="c3f9c-107">Create reason codes</span></span>

1. <span data-ttu-id="c3f9c-108">ในพื้นที่ทำงาน **การจัดการบุคลากร** (หรือพื้นที่ทำงาน **การจัดการสวัสดิการ** ถ้ารหัสเหตุผลของคุณยังไม่ได้ย้าย) เลือก **ลิงค์** แล้วเลือก **รหัสเหตุผล**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="c3f9c-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-109">Select **New**.</span></span>

3. <span data-ttu-id="c3f9c-110">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c3f9c-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c3f9c-111">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c3f9c-111">Field</span></span> | <span data-ttu-id="c3f9c-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c3f9c-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c3f9c-113">**รหัสเหตุผล**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-113">**Reason code**</span></span> | <span data-ttu-id="c3f9c-114">ชื่อเฉพาะเพื่อระบุเหตุผลที่พนักงานจะเปลี่ยนแปลงการลงทะเบียนแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c3f9c-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="c3f9c-115">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-115">**Description**</span></span> | <span data-ttu-id="c3f9c-116">คำอธิบายเกี่ยวกับรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="c3f9c-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="c3f9c-117">ภายใต้ **สถานการณ์ที่ใช้ได้** ให้ตั้งค่า **การจัดการสวัสดิการ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="c3f9c-118">(ไม่เกี่ยวข้องถ้ารหัสเหตุผลของคุณยังไม่ได้ย้ายไปยังพื้นที่ทำงาน **การจัดการบุคลากร**)</span><span class="sxs-lookup"><span data-stu-id="c3f9c-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="c3f9c-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="c3f9c-120">ย้ายรหัสเหตุผลไปยังการจัดการบุคลากรด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c3f9c-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="c3f9c-121">ณ วันที่ 2021 มกราคม รหัสเหตุผลย้ายไปยังพื้นที่ทำงาน **การจัดการบุคลากร** แทนพื้นที่ทำงาน **การจัดการสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="c3f9c-122">ข้อมูลรหัสเหตุผลส่วนใหญ่จะย้ายโดยอัตโนมัติในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="c3f9c-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="c3f9c-123">ข้อมูลรหัสเหตุผลบางอย่างอาจไม่ย้าย</span><span class="sxs-lookup"><span data-stu-id="c3f9c-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="c3f9c-124">ตัวอย่างเช่น ขณะนี้รหัสเหตุผลมีอักขระสูงสุด 15 อักขระ ดังนั้น รหัสเหตุผลที่ยาวกว่า 15 อักขระจะไม่ย้ายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c3f9c-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="c3f9c-125">คุณจะเห็นพนักงานทั่วไปในหน้า **ลิงค์** ของพื้นที่ทำงาน **การจัดการสวัสดิการ** เพื่อแจ้งให้ทราบเกี่ยวกับการย้ายข้อมูลและรหัสเหตุผลไม่ได้ย้ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c3f9c-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="c3f9c-126">เลือก **รหัสเหตุผล** เพื่อดูรายละเอียดเกี่ยวกับสถานะการย้าย</span><span class="sxs-lookup"><span data-stu-id="c3f9c-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="c3f9c-127">[![รหัสเหตุผล](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="c3f9c-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="c3f9c-128">เลือกรหัสเหตุผลที่ไม่สามารถย้ายได้</span><span class="sxs-lookup"><span data-stu-id="c3f9c-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="c3f9c-129">[![สถานะการย้ายรหัสเหตุผล](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="c3f9c-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="c3f9c-130">เลือก **ย้ายรหัสเหตุผล**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="c3f9c-131">[![ย้ายรหัสเหตุผล](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="c3f9c-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="c3f9c-132">ในบานหน้าต่าง **การย้ายรหัสเหตุผลของสวัสดิการ** คุณมีตัวเลือกสองตัวเลือกในการแม็ปกับรหัสเหตุผลของการจัดการบุคลากร:</span><span class="sxs-lookup"><span data-stu-id="c3f9c-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="c3f9c-133">เมื่อต้องการใช้รหัสเหตุผลที่มีอยู่ในการจัดการบุคลากร ให้เลือกรหัสเหตุผลใดรหัสหนึ่งจากรายการแบบหล่นลง **ใช้รหัสเหตุผลที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="c3f9c-134">คุณสามารถใช้รหัสเหตุผลที่มีอยู่ในการจัดการบุคลากรได้เฉพาะเมื่อรหัสเหตุผลของการจัดการสวัสดิการอื่นยังไม่ได้ย้ายไปยังรหัสนั้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="c3f9c-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="c3f9c-135">เมื่อต้องการสร้างรหัสเหตุผลใหม่ในการจัดการบุคลากร ให้ป้อนรหัสใหม่ใน **เหตุผลใหม่** แล้วป้อนอธิบายใน **คำอธิบายใหม่**</span><span class="sxs-lookup"><span data-stu-id="c3f9c-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="c3f9c-136">[![แม็ปกับรหัสเหตุผลในการจัดการบุคลากร](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="c3f9c-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="c3f9c-137">หลังจากรหัสเหตุผลย้ายไปยังการจัดการบุคลากร ตัวเลือกในการใช้รหัสเหตุผลในการจัดการสวัสดิการจะถูกตั้งค่าเป็น **ใช่** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c3f9c-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="c3f9c-138">[![ใช้รหัสเหตุผลของการจัดการสวัสดิการ](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="c3f9c-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]