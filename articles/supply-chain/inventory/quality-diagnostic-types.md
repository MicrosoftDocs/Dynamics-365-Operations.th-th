---
title: ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน
description: หัวข้อนี้จะอธิบายวิธีการใช้และสร้างชนิดการวิเคราะห์ที่สามารถใช้กับความไม่สอดคล้องกันได้
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19fcd57e28efabd6ca32c444ab961b876bde424d
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956843"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="43051-103">ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="43051-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43051-104">หัวข้อนี้จะอธิบายวิธีการใช้และสร้างชนิดการวิเคราะห์ที่สามารถใช้กับความไม่สอดคล้องกันได้</span><span class="sxs-lookup"><span data-stu-id="43051-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="43051-105">คุณใช้หน้า **ชนิดการวินิจฉัย** เพื่อกำหนดการจัดประเภทการดำเนินการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="43051-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="43051-106">จากนั้น เมื่อคุณสร้างการแก้ไขความไม่สอดคล้องกัน คุณจะเลือกการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="43051-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="43051-107">การแก้ไขระบุชนิดของการดำเนินการวินิจฉัยซึ่งควรจะดำเนินการสำหรับความไม่สอดคล้องที่ได้รับอนุมัติ และใครที่ควรดำเนินการนั้น</span><span class="sxs-lookup"><span data-stu-id="43051-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="43051-108">ยังระบุวันเสร็จสมบูรณ์ที่ร้องขอและวันเสร็จสมบูรณ์ที่วางแผนไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="43051-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="43051-109">ตัวอย่างชนิดของการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="43051-109">Examples of diagnostic types</span></span>

<span data-ttu-id="43051-110">คุณร่วมงานกับบริษัทผู้ผลิต และสินค้าหลายรายการไม่ผ่านการทดสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="43051-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="43051-111">สินค้าเหล่านั้นจะถูกย้ายไปยังพื้นที่ตรวจสอบสินค้าและถูกทำเครื่องหมายเป็นผลิตภัณฑ์ที่ไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="43051-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="43051-112">มีการสร้างเรกคอร์ดความไม่สอดคล้องกันใน Microsoft Dynamics 365 Supply Chain Management เพื่อติดตามรายละเอียดโดยผ่านการแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="43051-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="43051-113">ในกรณีนี้ ปัญหาด้านคุณภาพเกิดขึ้นเนื่องจากการส่งให้ในเครื่องจักรซึ่งบรรจุสินค้าเสียหายและร้อนเกินไป</span><span class="sxs-lookup"><span data-stu-id="43051-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="43051-114">การแก้ไขนี้คือการแทนที่อะไหล่ในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="43051-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="43051-115">เมื่อคุณตั้งค่าคอนฟิกชนิดการวินิจฉัย คุณสามารถสร้างเรกคอร์ดได้หลายเรกคอร์ด ซึ่งแต่ละเรกคอร์ดแสดงถึงปัญหาชนิดอื่นที่เครื่องอาจมี</span><span class="sxs-lookup"><span data-stu-id="43051-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="43051-116">หรือคุณสามารถสร้างชนิดการวินิจฉัยทั่วไปหนึ่งชนิดที่แสดงถึงการซ่อมแซมเครื่อง</span><span class="sxs-lookup"><span data-stu-id="43051-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="43051-117">สร้างชนิดการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="43051-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="43051-118">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การจัดการคุณภาพ \> ชนิดการวินิจฉัย**</span><span class="sxs-lookup"><span data-stu-id="43051-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="43051-119">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="43051-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="43051-120">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="43051-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="43051-121">**การวินิจฉัย** – ป้อนรหัสหรือชื่อเฉพาะสำหรับชนิดการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="43051-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="43051-122">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของชนิดการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="43051-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="43051-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="43051-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43051-124">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="43051-124">Additional resources</span></span>

- [<span data-ttu-id="43051-125">ภาพรวมของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="43051-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="43051-126">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="43051-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="43051-127">ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="43051-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="43051-128">โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="43051-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="43051-129">ชนิดของปัญหาสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="43051-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="43051-130">ค่าธรรมเนียมคุณภาพสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="43051-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="43051-131">การดำเนินงานสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="43051-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="43051-132">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="43051-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
