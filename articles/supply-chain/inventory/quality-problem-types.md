---
title: ชนิดของปัญหาสำหรับความไม่สอดคล้องกัน
description: หัวข้อนี้จะอธิบายวิธีการสร้างและใช้ชนิดปัญหาของความไม่สอดคล้องกัน
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022167"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="ff548-103">ชนิดของปัญหาสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff548-104">หัวข้อนี้จะอธิบายวิธีการสร้างและใช้ชนิดปัญหาของความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="ff548-105">คุณใช้หน้า **ชนิดปัญหา** เพื่อกำหนดการจัดประเภทของปัญหาด้านคุณภาพ ซึ่งพบในความไม่สอดคล้องกันชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="ff548-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="ff548-106">สำหรับแต่ละปัญหาที่คุณสร้าง คุณต้องระบุชนิดของความไม่สอดคล้องกันที่สามารถใช้ชนิดของปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="ff548-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="ff548-107">คุณสามารถตั้งค่าชนิดของความไม่สอดคล้องกันต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ff548-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="ff548-108">**ภายใน** – ความไม่สอดคล้องกันของชนิดนี้เกี่ยวข้องกับปริมาณคงคลังคงเหลือ (ตัวอย่างเช่น ใบสั่งตรวจสอบคุณภาพหรือใบสั่งตรวจสอบสินค้า)</span><span class="sxs-lookup"><span data-stu-id="ff548-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="ff548-109">**ลูกค้า** – ความไม่สอดคล้องกันของชนิดนี้เกี่ยวข้องกับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="ff548-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="ff548-110">**ผู้จัดจำหน่าย** – ความไม่สอดคล้องกันของชนิดนี้เกี่ยวข้องกับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="ff548-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="ff548-111">**คำขอการบริการ** – ความไม่สอดคล้องกันของชนิดนี้เกี่ยวข้องกับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ff548-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="ff548-112">**การผลิต** – ความไม่สอดคล้องกันของชนิดนี้เกี่ยวข้องกับใบสั่งชุดงานหรือใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="ff548-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="ff548-113">**การผลิตสินค้าร่วม** – ความไม่สอดคล้องกันของชนิดนี้เกี่ยวข้องกับใบสั่งชุดงานสำหรับสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="ff548-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="ff548-114">เมื่อคุณสร้างชนิดปัญหาใหม่ ให้เลือก **ชนิดความไม่สอดคล้องกันใน** บานหน้าต่างการดำเนินการเพื่อสร้างรายการชนิดของความไม่สอดคล้องกันหนึ่งชนิดหรือมากกว่าที่ได้รับอนุมัติสำหรับชนิดของปัญหา</span><span class="sxs-lookup"><span data-stu-id="ff548-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="ff548-115">ตัวอย่างเช่น ชนิดปัญหาเกี่ยวกับรหัสความบกพร่องอาจนำไปใช้กับความไม่สอดคล้องกันได้ทุกชนิด</span><span class="sxs-lookup"><span data-stu-id="ff548-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="ff548-116">อย่างไรก็ตาม ชนิดของปัญหาที่เกี่ยวข้องกับร้องเรียนของลูกค้าอาจมีผลใช้กับความไม่สอดคล้องกันชนิด **ลูกค้า** และ **คำขอการบริการ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ff548-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="ff548-117">ตัวอย่างของชนิดปัญหา</span><span class="sxs-lookup"><span data-stu-id="ff548-117">Examples of problem types</span></span>

<span data-ttu-id="ff548-118">ต่อไปนี้เป็นตัวอย่างสถานการณ์ของชนิดปัญหาที่สามารถใช้กับความไม่สอดคล้องกันชนิดต่าง ๆ ได้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="ff548-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="ff548-119">**ลูกค้า:** ลูกค้ายื่นเรื่องร้องเรียน ลูกค้าส่งสินค้าส่งคืน หรือมีข้อมูลเฉพาะเกี่ยวกับคุณภาพไม่ตรงตามข้อเพาะ</span><span class="sxs-lookup"><span data-stu-id="ff548-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="ff548-120">**ผู้ผู้จัดจำหน่าย:** ผลิตภัณฑ์ได้รับความเสียหาย ข้อมูลเพาะเกี่ยวกับคุณภาพไม่ตรงตามหรือได้รับผลิตภัณฑ์ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ff548-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="ff548-121">**คำขอบริการ:** ไม่ตรงตามข้อเพาะเกี่ยวกับคุณภาพ ลูกค้าต้องยื่นร้องเรียนหรือการรักษาเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="ff548-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="ff548-122">**การผลิต:** ไม่ตรงตามข้อมูลเพาะเกี่ยวกับคุณภาพ ต้องบํารุงรักษาเครื่องจักร หรือผลิตภัณฑ์ได้รับความเสียหาย</span><span class="sxs-lookup"><span data-stu-id="ff548-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="ff548-123">**การผลิตสินค้าร่วม:** ไม่ตรงตามข้อมูลเพาะเกี่ยวกับคุณภาพ ต้องบํารุงรักษาเครื่องจักร หรือผลิตภัณฑ์ได้รับความเสียหาย</span><span class="sxs-lookup"><span data-stu-id="ff548-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="ff548-124">สร้างชนิดของปัญหาและกําหนดให้กับชนิดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="ff548-125">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การจัดการคุณภาพ \> ชนิดปัญหา**</span><span class="sxs-lookup"><span data-stu-id="ff548-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="ff548-126">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="ff548-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ff548-127">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="ff548-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ff548-128">**ชนิดปัญหา** – ป้อนรหัสหรือชื่อเฉพาะสำหรับชนิดปัญหา</span><span class="sxs-lookup"><span data-stu-id="ff548-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="ff548-129">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของชนิดปัญหา</span><span class="sxs-lookup"><span data-stu-id="ff548-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="ff548-130">ขณะที่ยังคงเลือกแถวใหม่อยู่ ให้เลือก **ชนิดของความไม่สอดคล้องกัน** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="ff548-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="ff548-131">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="ff548-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ff548-132">จากนั้นให้ตั้งค่าฟิลด์ **ชนิดของความไม่สอดคล้องกัน** เป็นชนิดของความไม่สอดคล้องกันที่คุณต้องการอนุญาตในชนิดของปัญหา</span><span class="sxs-lookup"><span data-stu-id="ff548-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="ff548-133">ทําซ้ําขั้นตอนก่อนหน้านี้ให้กับชนิดของความไม่สอดคล้องกันเพิ่มเติมแต่ละชนิดที่คุณต้องการอนุมัติชนิดของปัญหา</span><span class="sxs-lookup"><span data-stu-id="ff548-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="ff548-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff548-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff548-135">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ff548-135">Additional resources</span></span>

- [<span data-ttu-id="ff548-136">ภาพรวมของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ff548-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="ff548-137">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="ff548-138">ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="ff548-139">โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="ff548-140">ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="ff548-141">ค่าธรรมเนียมคุณภาพสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="ff548-142">การดำเนินงานสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ff548-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="ff548-143">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ff548-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
