---
title: การดำเนินงานสำหรับความไม่สอดคล้องกัน
description: หัวข้อนี้จะอธิบายวิธีการสร้างและใช้การดำเนินงานของความไม่สอดคล้องกัน
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6454a56323ea66369696dd6e3310a41b4eb9ee58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956855"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="79ddc-103">การดำเนินงานสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79ddc-104">หัวข้อนี้จะอธิบายวิธีการสร้างและใช้การดำเนินงานของความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="79ddc-105">คุณใช้หน้า **ดำเนินงาน** เพื่อกำหนดการจัดประเภทของงานที่สามารถดำเนินการสำหรับความไม่สอดคล้องที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="79ddc-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="79ddc-106">เมื่อคุณกำหนดการดำเนินงานที่เกี่ยวข้องให้กับความไม่สอดคล้องกัน คุณยังสามารถกำหนดรายละเอียด เช่น วัสดุที่สัมพันธ์กัน ชั่วโมงแรงงาน และค่าธรรมเนียมที่จำเป็นต้องใช้ในการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="79ddc-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="79ddc-107">ระบบใช้ข้อมูลนี้ในการคำนวณต้นทุนที่ประเมินสำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="79ddc-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="79ddc-108">ข้อมูลรายละเอียดและต้นทุนที่ประเมินมีสำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="79ddc-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="79ddc-109">การดำเนินงานที่เกี่ยวข้องสำหรับคุณภาพจะแตกต่างจากการดำเนินงานที่สามารถกำหนดให้กับกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="79ddc-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="79ddc-110">แม้ว่าคุณจะสามารถติดตามต้นทุน เวลา และสินค้าที่ใช้ในการดําเนินงานที่เกี่ยวข้องกับความไม่สอดคล้องกัน แต่ข้อมูลที่คุณป้อนเพียงแต่ให้ข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="79ddc-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="79ddc-111">ซึ่งไม่ได้รวมเข้ากับบัญชีแยกประเภททั่วไป บัญชีแยกประเภทย่อยของสินค้าคงคลัง หรือโมดูล **เวลาและการเข้างาน** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="79ddc-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="79ddc-112">ตัวอย่างของการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="79ddc-112">Examples of operations</span></span>

<span data-ttu-id="79ddc-113">คุณร่วมงานกับบริษัทผู้ผลิต</span><span class="sxs-lookup"><span data-stu-id="79ddc-113">You work for a manufacturing company.</span></span> <span data-ttu-id="79ddc-114">ความไม่สอดคล้องกันมีการสร้างและอนุมัติของสินค้าที่ไม่ผ่านการทดสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="79ddc-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="79ddc-115">การแก้ไขถูกสร้างขึ้นเพื่อบ่งชี้ว่าปัญหาเกี่ยวข้องกับปัญหาไม่ดีบนเครื่อง</span><span class="sxs-lookup"><span data-stu-id="79ddc-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="79ddc-116">ในหลายขั้นตอนต้องเปลี่ยนความรับผิดชอบใหม่ และความรับผิดชอบของแต่ละขั้นตอนจะถูกติดตาม</span><span class="sxs-lookup"><span data-stu-id="79ddc-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="79ddc-117">ตัวอย่างเช่น อาจต้องใช้ขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="79ddc-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="79ddc-118">สายการผลิตถูกหยุด และชุดนอกจะถูกปฏิบัติ</span><span class="sxs-lookup"><span data-stu-id="79ddc-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="79ddc-119">บุคลากรการบํารุงรักษาแทนที่บุคลากรใหม่</span><span class="sxs-lookup"><span data-stu-id="79ddc-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="79ddc-120">บุคลากรการรับรองคุณภาพจะตรวจสอบเครื่องจักรก่อนจึงจะเปิดใช้งานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="79ddc-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="79ddc-121">สำหรับตัวอย่างนี้ การดําเนินงานต่อไปนี้สามารถสร้างเพื่อแสดงถึงงานที่ต้องดําเนินการเสร็จสิ้นได้</span><span class="sxs-lookup"><span data-stu-id="79ddc-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="79ddc-122">หยุดสายการผลิต</span><span class="sxs-lookup"><span data-stu-id="79ddc-122">Stop the production line.</span></span>
- <span data-ttu-id="79ddc-123">ล้างข้อมูลสายการผลิต</span><span class="sxs-lookup"><span data-stu-id="79ddc-123">Clean out the production line.</span></span>
- <span data-ttu-id="79ddc-124">ดำเนินการบำรุงรักษาเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="79ddc-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="79ddc-125">ตรวจสอบเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="79ddc-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="79ddc-126">สร้างการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="79ddc-126">Create an operation</span></span>

1. <span data-ttu-id="79ddc-127">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การจัดการคุณภาพ \> การดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="79ddc-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="79ddc-128">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="79ddc-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="79ddc-129">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="79ddc-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="79ddc-130">**การดำเนินงาน** – ป้อนรหัสหรือชื่อเฉพาะสำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="79ddc-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="79ddc-131">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="79ddc-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="79ddc-132">**ชนิด** – ถ้าสามารถใช้การดําเนินงานกับความไม่สอดคล้องกันที่เกี่ยวข้องกับชนิดของใบสั่งเฉพาะเท่านั้น ให้เลือกชนิดใบสั่ง (*ใบสั่งซื้อ* หรือ *ใบสั่งขาย*)</span><span class="sxs-lookup"><span data-stu-id="79ddc-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="79ddc-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="79ddc-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79ddc-134">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="79ddc-134">Additional resources</span></span>

- [<span data-ttu-id="79ddc-135">ภาพรวมของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="79ddc-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="79ddc-136">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="79ddc-137">สร้างและประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="79ddc-138">ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="79ddc-139">โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="79ddc-140">ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="79ddc-141">ค่าธรรมเนียมคุณภาพสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="79ddc-142">ชนิดของปัญหาสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79ddc-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="79ddc-143">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="79ddc-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
