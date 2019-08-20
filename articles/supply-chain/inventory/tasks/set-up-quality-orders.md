---
title: ตั้งค่าใบสั่งตรวจสอบคุณภาพ
description: 'กระบวนงานนี้แสดงวิธีการเปิดใช้งานกระบวนการจัดการคุณภาพที่ต้องตรวจสอบสินค้าคงคลังขาเข้าทันทีหลังจากการลงทะเบียนการมาถึง '
author: perlynne
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0119ae07e490f048dbb021983e25889cb1cb42b3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845365"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="832a9-103">ตั้งค่าใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="832a9-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="832a9-104">กระบวนงานนี้แสดงวิธีการเปิดใช้งานกระบวนการจัดการคุณภาพที่ต้องตรวจสอบสินค้าคงคลังขาเข้าทันทีหลังจากการลงทะเบียนการมาถึง </span><span class="sxs-lookup"><span data-stu-id="832a9-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="832a9-105">กระบวนงานโดยทั่วไปจะดำเนินการโดยผู้จัดการด้านคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="832a9-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="832a9-106">กระบวนการประกอบด้วยการสร้างกลุ่มคุณภาพ เพื่อกำหนดสินค้าที่กำลังจะถูกทดสอบ และกลุ่มการทดสอบเพื่อจัดกลุ่มการทดสอบที่จะได้รับการทดสอบกับสินค้าในกลุ่มคุณภาพ </span><span class="sxs-lookup"><span data-stu-id="832a9-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="832a9-107">คุณสามารถรันคำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="832a9-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="832a9-108">เปิดใช้งานการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="832a9-108">Enable quality management</span></span>
1. <span data-ttu-id="832a9-109">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการสินค้าคงคลัง > การตั้งค่า > พารามิเตอร์สินค้าคงคลังและการจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="832a9-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="832a9-110">คลิกแท็บ **การจัดการคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="832a9-110">Click the **Quality management** tab.</span></span>
3. <span data-ttu-id="832a9-111">ตั้งค่า **ตัวเลือกใช้การจัดการคุณภาพการ** เป็น 'ใช่'</span><span class="sxs-lookup"><span data-stu-id="832a9-111">Set the **Use quality management option** to 'Yes'.</span></span>
4. <span data-ttu-id="832a9-112">คลิก **การตั้งค่ารายงาน**</span><span class="sxs-lookup"><span data-stu-id="832a9-112">Click **Report setup**.</span></span> <span data-ttu-id="832a9-113">ใน USMF มีกำหนดการตั้งค่ารายงานสำหรับการจัดการคุณภาพแล้ว </span><span class="sxs-lookup"><span data-stu-id="832a9-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="832a9-114">หากไม่ทำเช่นนี้ ให้คุณเพิ่มบรรทัดใหม่ที่นี่สำหรับชนิดรายงานต่าง ๆ และเลือกชนิดของเอกสารที่จะใช้สำหรับแต่ละรายงาน</span><span class="sxs-lookup"><span data-stu-id="832a9-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="832a9-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-115">Close the page.</span></span>
6. <span data-ttu-id="832a9-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="832a9-117">สร้างการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="832a9-117">Create a test</span></span>
1. <span data-ttu-id="832a9-118">ไปที่ **การบริหารสินค้าคงคลัง > การตั้งค่า > การควบคุมคุณภาพ > การทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="832a9-118">Go to **Inventory management > Setup > Quality control > Tests**.</span></span>
2. <span data-ttu-id="832a9-119">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="832a9-119">Click **New**.</span></span>
3. <span data-ttu-id="832a9-120">ในฟิลด์ **การทดสอบ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-120">In the **Test** field, type a value.</span></span>
4. <span data-ttu-id="832a9-121">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-121">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="832a9-122">ในฟิลด์ **ชนิด** ให้เลือก 'ตัวเลือก'</span><span class="sxs-lookup"><span data-stu-id="832a9-122">In the **Type** field, select 'Option'.</span></span> <span data-ttu-id="832a9-123">ในตัวอย่างนี้ เราจะเลือก "เลือก" ซึ่งจะช่วยให้คุณสามารถกำหนดผลการทดสอบโดยยึดตามค่าที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="832a9-124">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="832a9-124">Click **Save**.</span></span>
7. <span data-ttu-id="832a9-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="832a9-126">สร้างตัวแปรการทดสอบเพื่อกำหนดวิธีการบันทึกผลการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="832a9-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="832a9-127">ไปที่ **การบริหารสินค้าคงคลัง > การตั้งค่า > การควบคุมคุณภาพ > การทดสอบตัวแปร**</span><span class="sxs-lookup"><span data-stu-id="832a9-127">Go to **Inventory management > Setup > Quality control > Test variables**.</span></span>
2. <span data-ttu-id="832a9-128">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="832a9-128">Click **New**.</span></span>
3. <span data-ttu-id="832a9-129">ในฟิลด์ **ตัวแปร** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-129">In the **Variable** field, type a value.</span></span>
4. <span data-ttu-id="832a9-130">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-130">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="832a9-131">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="832a9-131">Click **Save**.</span></span>
6. <span data-ttu-id="832a9-132">คลิก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="832a9-132">Click **Outcomes**.</span></span>
7. <span data-ttu-id="832a9-133">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="832a9-133">Click **New**.</span></span>
8. <span data-ttu-id="832a9-134">ในฟิลด์ **ผลลัพธ์** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-134">In the **Outcome** field, type a value.</span></span>
9. <span data-ttu-id="832a9-135">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-135">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="832a9-136">ในฟิลด์ **สถานะของผลลัพธ์** ให้เลือก 'ผ่าน'</span><span class="sxs-lookup"><span data-stu-id="832a9-136">In the **Outcome status** field, select 'Pass'.</span></span>
11. <span data-ttu-id="832a9-137">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="832a9-137">Click **Save**.</span></span>
12. <span data-ttu-id="832a9-138">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="832a9-138">Click **New**.</span></span>
13. <span data-ttu-id="832a9-139">ในฟิลด์ **ผลลัพธ์** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-139">In the **Outcome** field, type a value.</span></span>
14. <span data-ttu-id="832a9-140">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-140">In the **Description** field, type a value.</span></span>
15. <span data-ttu-id="832a9-141">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="832a9-141">Click **Save**.</span></span>
16. <span data-ttu-id="832a9-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-142">Close the page.</span></span>
17. <span data-ttu-id="832a9-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="832a9-144">ตั้งค่าการสุ่มตัวอย่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="832a9-144">Set up item sampling</span></span>
1. <span data-ttu-id="832a9-145">ไปที่ **การบริหารสินค้าคงคลัง > การตั้งค่า > การควบคุมคุณภาพ > การสุ่มตัวอย่างสินค้า**</span><span class="sxs-lookup"><span data-stu-id="832a9-145">Go to **Inventory management > Setup > Quality control > Item sampling**.</span></span>
2. <span data-ttu-id="832a9-146">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="832a9-146">Click **New**.</span></span>
3. <span data-ttu-id="832a9-147">ในฟิลด์ **การสุ่มตัวอย่างสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="832a9-147">In the **Item sampling** field, type a value.</span></span>
4. <span data-ttu-id="832a9-148">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-148">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="832a9-149">ในฟิลด์ **ค่า** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="832a9-149">In the **Value** field, enter a number.</span></span> <span data-ttu-id="832a9-150">ค่านี้เกี่ยวข้องกับข้อกำหนดเกี่ยวกับปริมาณที่ถูกเลือกในฟิลด์ที่อยู่ติดกัน</span><span class="sxs-lookup"><span data-stu-id="832a9-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="832a9-151">ขยายหรือยุบส่วน **กระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="832a9-151">Expand or collapse the **Process** section.</span></span>
7. <span data-ttu-id="832a9-152">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **การบล็อคทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="832a9-152">Select or clear the **Full blocking** check box.</span></span> <span data-ttu-id="832a9-153">ถ้าคุณเลือกตัวเลือกนี้ ปริมาณล็อตหรือรายการใบสั่งทั้งหมดจะถูกบล็อคถ้าการทดสอบล้มเหลว </span><span class="sxs-lookup"><span data-stu-id="832a9-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="832a9-154">ถ้าคุณไม่เลือกตัวเลือกนี้ เฉพาะสินค้าในใบสั่งตรวจสอบคุณภาพจะถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="832a9-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="832a9-155">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="832a9-155">Click **Save**.</span></span>
9. <span data-ttu-id="832a9-156">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="832a9-157">สร้างกลุ่มคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="832a9-157">Create a quality group</span></span>
1. <span data-ttu-id="832a9-158">ไปที่ **การบริหารสินค้าคงคลัง > การตั้งค่า > การควบคุมคุณภาพ > กลุ่มคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="832a9-158">Go to **Inventory management > Setup > Quality control > Quality groups**.</span></span>
2. <span data-ttu-id="832a9-159">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="832a9-159">Click **New**.</span></span>
3. <span data-ttu-id="832a9-160">ในฟิลด์ **กลุ่มคุณภาพ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-160">In the **Quality group** field, type a value.</span></span> <span data-ttu-id="832a9-161">ใช้ชื่อที่เป็นคำอธิบายเพื่อช่วยคุณระบุชนิดของสินค้าที่จะประกอบอยู่ในกลุ่ม (เงื่อนไขการสุ่มตัวอย่างของคุณ)</span><span class="sxs-lookup"><span data-stu-id="832a9-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="832a9-162">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-162">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="832a9-163">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="832a9-163">Click **Save**.</span></span>
6. <span data-ttu-id="832a9-164">คลิก **เพิ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="832a9-164">Click **Add items**.</span></span>
7. <span data-ttu-id="832a9-165">เลือกแถว **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="832a9-165">Select the **Item number** row.</span></span> <span data-ttu-id="832a9-166">ในตัวอย่างนี้ การกรองจะถูกเรียกใช้ตามหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="832a9-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="832a9-167">ในฟิลด์ **เงื่อนไข** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-167">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="832a9-168">ตัวอย่างเช่น พิมพ์ T\* เพื่อกรองหมายเลขสินค้าที่ขึ้นต้นด้วย T</span><span class="sxs-lookup"><span data-stu-id="832a9-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="832a9-169">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="832a9-169">Click **OK**.</span></span>
10. <span data-ttu-id="832a9-170">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="832a9-170">Click **OK**.</span></span>
11. <span data-ttu-id="832a9-171">คลิก **กลุ่มคุณภาพสินค้า**</span><span class="sxs-lookup"><span data-stu-id="832a9-171">Click **Item quality groups**.</span></span>
12. <span data-ttu-id="832a9-172">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-172">Close the page.</span></span>
13. <span data-ttu-id="832a9-173">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="832a9-174">สร้างกลุ่มทดสอบ</span><span class="sxs-lookup"><span data-stu-id="832a9-174">Create a test group</span></span>
1. <span data-ttu-id="832a9-175">ไปที่ **การบริหารสินค้าคงคลัง > การตั้งค่า > การควบคุมคุณภาพ > กลุ่มการทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="832a9-175">Go to **Inventory management > Setup > Quality control > Test groups**.</span></span>
2. <span data-ttu-id="832a9-176">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="832a9-176">Click **New**.</span></span>
3. <span data-ttu-id="832a9-177">ในฟิลด์ **กลุ่มการทดสอบ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="832a9-177">In the **Test group** field, type a value.</span></span> <span data-ttu-id="832a9-178">กำหนดชื่อ **กลุ่มทดสอบ** ที่จะช่วยให้คุณจดจำชนิดของการทดสอบที่กำลังดำเนินการ และกลุ่มคุณภาพที่ควรเกี่ยวข้องด้วย</span><span class="sxs-lookup"><span data-stu-id="832a9-178">Give the **Test group** a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="832a9-179">ตัวอย่างเช่น ใช้กับกลุ่มคุณภาพที่เลือกสินค้าที่ขึ้นต้นด้วย "T" คุณสามารถเรียกว่า "การทดสอบสินค้า T"</span><span class="sxs-lookup"><span data-stu-id="832a9-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="832a9-180">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="832a9-180">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="832a9-181">ในฟิลด์ **การสุ่มตัวอย่างสินค้า** เลือกรายการการสุ่มตัวอย่างสินค้าที่คุณสร้างขึ้นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-181">In the **Item sampling** field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="832a9-182">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="832a9-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="832a9-183">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="832a9-183">Click **Add**.</span></span>
8. <span data-ttu-id="832a9-184">ในฟิลด์ **หมายเลขลำดับ** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="832a9-184">In the **Sequence number** field, enter a number.</span></span>
9. <span data-ttu-id="832a9-185">ในฟิลด์ **การทดสอบ** ให้เลือกการทดสอบที่คุณสร้างไว้ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-185">In the **Test** field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="832a9-186">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="832a9-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="832a9-187">คลิกแท็บ **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="832a9-187">Click the **Test** tab.</span></span>
12. <span data-ttu-id="832a9-188">ในฟิลด์ **ตัวแปร** ให้เลือกตัวแปรการทดสอบที่คุณสร้างไว้ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-188">In the **Variable** field, select the test variable that you created before</span></span>
13. <span data-ttu-id="832a9-189">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="832a9-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="832a9-190">ในฟิลด์ **ผลลัพธ์เริ่มต้น** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="832a9-190">In the **Default outcome** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="832a9-191">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="832a9-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="832a9-192">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="832a9-192">Click **Save**.</span></span>
17. <span data-ttu-id="832a9-193">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="832a9-194">กำหนดเวลาที่จะมีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="832a9-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="832a9-195">ไปที่ **การบริหารสินค้าคงคลัง > การตั้งค่า > การควบคุมคุณภาพ > การเชื่อมโยงคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="832a9-195">Go to **Inventory management > Setup > Quality control > Quality associations**.</span></span>
2. <span data-ttu-id="832a9-196">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="832a9-196">Click **New**.</span></span>
3. <span data-ttu-id="832a9-197">ในฟิลด์ **ชนิดการอ้างอิง** ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="832a9-197">In the **Reference type** field, select an option.</span></span>
4. <span data-ttu-id="832a9-198">ในฟิลด์ **รหัสสินค้า** ให้เลือก 'กลุ่ม'</span><span class="sxs-lookup"><span data-stu-id="832a9-198">In the **Item code** field, select 'Group'.</span></span> <span data-ttu-id="832a9-199">ในตัวอย่างนี้ เราจะเลือก "กลุ่ม" และใช้กลุ่มคุณภาพที่เราได้สร้างขึ้นก่อนหน้า </span><span class="sxs-lookup"><span data-stu-id="832a9-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="832a9-200">คุณยังสามารถตั้งค่านี้เป็น "ตาราง" เพื่อระบุสินค้าด้วยตนเอง หรือเลือก "ทั้งหมด" เพื่อเพิ่มสินค้าทั้งหมดในใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="832a9-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="832a9-201">ในฟิลด์ **สินค้า** ให้เลือกกลุ่มคุณภาพที่คุณสร้างไว้ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-201">In the **Item** field, select the quality group that you created before.</span></span> <span data-ttu-id="832a9-202">ตัวเลือกที่พร้อมใช้งานในฟิลด์สินค้าขึ้นอยู่กับสิ่งที่คุณได้ตั้งค่าในฟิลด์รหัสสินค้า</span><span class="sxs-lookup"><span data-stu-id="832a9-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="832a9-203">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="832a9-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="832a9-204">ขยายหรือยุบส่วนกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="832a9-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="832a9-205">ในฟิลด์ **ชนิดเหตุการณ์** ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="832a9-205">In the **Event type** field, select an option.</span></span> <span data-ttu-id="832a9-206">นี่คือเหตุการณ์ที่ทริกเกอร์การทดสอบ </span><span class="sxs-lookup"><span data-stu-id="832a9-206">This is the event that triggers the test.</span></span> <span data-ttu-id="832a9-207">ความพร้อมใช้งานของตัวเลือกนี้ขึ้นอยู่ในกระบวนการที่คุณเลือกไว้ในฟิลด์ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="832a9-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="832a9-208">ในฟิลด์ **การดำเนินการ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="832a9-208">In the **Execution** field, select an option.</span></span>
10. <span data-ttu-id="832a9-209">ขยายหรือยุบส่วน **กระบวนการของใบสั่งตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="832a9-209">Expand or collapse the **Quality order process** section.</span></span>
11. <span data-ttu-id="832a9-210">ในฟิลด์ **การบล็อคเหตุการณ์** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="832a9-210">In the **Event blocking** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="832a9-211">ฟิลด์นี้แสดงรายการของกระบวนการที่สามารถบล็อคได้ถ้าใบสั่งตรวจสอบคุณภาพยังคงเปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="832a9-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="832a9-212">ตัวเลือกต่างๆขึ้นอยู่กับสิ่งที่คุณเลือกไว้ในฟิลด์ชนิดเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="832a9-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="832a9-213">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="832a9-213">In the list, click the link in the selected row.</span></span> <span data-ttu-id="832a9-214">นี่ขึ้นอยู่กับค่าที่เลือกก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="832a9-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="832a9-215">เลือกว่าต้องบล็อคกระบวนการต่อไปนี้ขณะที่กำลังมีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ที่เชื่อมโยงกับรายการเอกสารต้นทางหรือไม่</span><span class="sxs-lookup"><span data-stu-id="832a9-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="832a9-216">ขยายหรือยุบส่วน **ข้อมูลจำเพาะ**</span><span class="sxs-lookup"><span data-stu-id="832a9-216">Expand or collapse the **Specifications** section.</span></span>
14. <span data-ttu-id="832a9-217">ในฟิลด์ **กลุ่มทดสอบ** ให้เลือกกลุ่มการทดสอบที่คุณสร้างไว้ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-217">In the **Test group** field, select the test group that you created before.</span></span>
15. <span data-ttu-id="832a9-218">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="832a9-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="832a9-219">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="832a9-219">Click **Save**.</span></span>
17. <span data-ttu-id="832a9-220">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="832a9-220">Close the page.</span></span>

