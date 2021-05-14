---
title: ตัวแปรการทดสอบการจัดการคุณภาพ
description: หัวข้อนี้จะอธิบายวิธีการสร้างตัวแปรทดสอบเพื่อให้สามารถใช้การทดสอบเชิงคุณภาพกับใบสั่งตรวจสอบคุณภาพใน Microsoft Dynamics 365 Supply Chain Management
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956849"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="00ae8-103">ตัวแปรการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="00ae8-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00ae8-104">หัวข้อนี้จะอธิบายวิธีการสร้างตัวแปรทดสอบเพื่อให้สามารถใช้การทดสอบเชิงคุณภาพกับใบสั่งตรวจสอบคุณภาพใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="00ae8-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="00ae8-105">สำหรับการทดสอบแต่ละเชิงคุณภาพที่กำหนดในหน้า **ทดสอบ** คุณต้องกำหนดตัวแปรและผลของตัวแปรที่เป็นไปได้นั้น (ผลลัพธ์)</span><span class="sxs-lookup"><span data-stu-id="00ae8-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="00ae8-106">(สำหรับการทดสอบเชิงคุณภาพ ฟิลด์ **ชนิด** บนหน้า **การทดสอบ** ถูกตั้งค่าเป็น *ตัวเลือก*)</span><span class="sxs-lookup"><span data-stu-id="00ae8-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="00ae8-107">คุณใช้หน้า **ตัวแปรทดสอบ** เพื่อตั้งค่า แก้ไข และดูผลที่เป็นไปได้สำหรับตัวแปรทดสอบที่เกี่ยวข้องกับการทดสอบเชิงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="00ae8-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="00ae8-108">สำหรับแต่ละผลลัพธ์ คุณต้องกําหนดสถานะผลที่ได้เป็น *ผ่าน* หรือ *ไม่ผ่าน* เพื่อบ่งชี้ว่าการทดสอบผ่านหรือล้มเหลว เมื่อเลือกผลที่ได้เป็นผลการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="00ae8-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="00ae8-109">คุณใช้หน้า **กลุ่มทดสอบ** เพื่อกำหนดตัวแปรทดสอบและผลลัพธ์เริ่มต้นไปยังการทดสอบเชิงคุณภาพแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="00ae8-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="00ae8-110">ให้กับตัวแปรทดสอบทุกตัว ขอแนะนำว่าคุณควรกําหนดผลที่ได้อย่างน้อยสองรายการ: ตัวแปรที่มีสถานะผลที่ได้เป็น *ผ่าน* และตัวแปรที่มีสถานะเป็น *ล้มเหลว*</span><span class="sxs-lookup"><span data-stu-id="00ae8-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="00ae8-111">ไม่มีขีดจํากัดจํานวนรวมของตัวแปรหรือผลที่ได้ที่สามารถกําหนดได้</span><span class="sxs-lookup"><span data-stu-id="00ae8-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="00ae8-112">นอกจากนี้ การทดสอบต่าง ๆ ยังสามารถใช้ตัวแปรทดสอบเดียวกันเพื่อบันทึกผลที่ได้</span><span class="sxs-lookup"><span data-stu-id="00ae8-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="00ae8-113">ตัวอย่างตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="00ae8-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="00ae8-114">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="00ae8-114">Example 1</span></span>

<span data-ttu-id="00ae8-115">บริษัทผู้ผลิตจะทดสอบวัสดุที่ผลิตสองรายการ</span><span class="sxs-lookup"><span data-stu-id="00ae8-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="00ae8-116">ในการทดสอบหนึ่ง ระดับ pH จะเชื่อมโยงกับแถบสี</span><span class="sxs-lookup"><span data-stu-id="00ae8-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="00ae8-117">ระดับ pH ที่ยอมรับได้อยู่ในสีที่อ่อนกว่า และระดับ pH ที่ยอมรับไม่ได้อยู่ในสีเข้ม</span><span class="sxs-lookup"><span data-stu-id="00ae8-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="00ae8-118">ในการทดสอบอื่น มีการตรวจสอบด้วยภาพต่าง ๆ และผู้ปฏิบัติงานด้านคุณภาพใช้การจัดการคุณภาพเพื่อระบุว่าสินค้าจะผ่านหรือไม่ผ่านการตรวจสอบด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="00ae8-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="00ae8-119">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="00ae8-119">Example 2</span></span>

<span data-ttu-id="00ae8-120">บริษัทผู้ผลิตซึ่งผลิตคุกกี้ใช้การทดสอบตรวจสอบสำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="00ae8-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="00ae8-121">การทดสอบตรวจสอบนี้มีหลายตัวแปร</span><span class="sxs-lookup"><span data-stu-id="00ae8-121">This inspection test has several variables.</span></span> <span data-ttu-id="00ae8-122">ตัวแปรเป็นรส และผลลัพธ์ที่เป็นไปได้สำหรับตัวแปรนี้คืออร่อยและไม่อร่อย</span><span class="sxs-lookup"><span data-stu-id="00ae8-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="00ae8-123">ตัวแปรที่สองคือสี และผลลัพธ์ที่เป็นไปได้คือเข้มเกินไป อ่อนเกินไป และพอดี</span><span class="sxs-lookup"><span data-stu-id="00ae8-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="00ae8-124">การสร้างตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="00ae8-124">Create a test variable</span></span>

<span data-ttu-id="00ae8-125">ให้ทำตามขั้นตอนเหล่านี้เพื่อสร้างตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="00ae8-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="00ae8-126">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> การทดสอบตัวแปร**</span><span class="sxs-lookup"><span data-stu-id="00ae8-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="00ae8-127">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="00ae8-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="00ae8-128">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="00ae8-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="00ae8-129">**ตัวแปร** – ป้อนรหัสหรือชื่อเฉพาะสำหรับตัวแปร</span><span class="sxs-lookup"><span data-stu-id="00ae8-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="00ae8-130">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของตัวแปร</span><span class="sxs-lookup"><span data-stu-id="00ae8-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="00ae8-131">ขณะที่ยังคงเลือกแถวใหม่อยู่ ให้เลือก **ผลลัพธ์** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="00ae8-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="00ae8-132">บนหน้า **ผลลัพธ์ของตัวแปรทดสอบ** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="00ae8-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="00ae8-133">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="00ae8-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="00ae8-134">**ผลลัพธ์** – ป้อนรหัสหรือชื่อเฉพาะสำหรับผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="00ae8-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="00ae8-135">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="00ae8-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="00ae8-136">**สำหรับแต่ละสถานะผลลัพธ์** – เลือก *ผ่าน* หรือ *ไม่ผ่าน* เพื่อบ่งชี้ว่าการทดสอบผ่านหรือล้มเหลว เมื่อเลือกผลที่ได้เป็นผลการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="00ae8-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="00ae8-137">ทําซ้ําขั้นตอนก่อนหน้านี้ของผลลัพธ์ที่ได้เพิ่มเติมแต่ละผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="00ae8-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="00ae8-138">ตรวจสอบให้แน่ใจว่าผลลัพธ์ที่ได้อย่างน้อยหนึ่งรายการมีสถานะเป็น *ผ่าน* และอย่างน้อยหนึ่งรายการมีสถานะผลลัพธ์ที่ได้เป็น *ล้มเหลว*</span><span class="sxs-lookup"><span data-stu-id="00ae8-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="00ae8-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="00ae8-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00ae8-140">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="00ae8-140">Additional resources</span></span>

- [<span data-ttu-id="00ae8-141">เครื่องมือการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="00ae8-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="00ae8-142">การทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="00ae8-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="00ae8-143">กลุ่มการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="00ae8-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
