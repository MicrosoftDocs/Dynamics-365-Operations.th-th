---
title: การทดสอบการจัดการคุณภาพ
description: หัวข้อนี้จะอธิบายวิธีการสร้างการทดสอบเพื่อให้สามารถใช้กับใบสั่งตรวจสอบคุณภาพใน Microsoft Dynamics 365 Supply Chain Management
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021695"
---
# <a name="quality-management-tests"></a><span data-ttu-id="ef0ed-103">การทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef0ed-104">หัวข้อนี้จะอธิบายวิธีการสร้างการทดสอบเพื่อให้สามารถใช้กับใบสั่งตรวจสอบคุณภาพใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ef0ed-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ef0ed-105">คุณใช้หน้า **การทดสอบ** เพื่อกำหนดและดูการทดสอบต่างๆ ที่ระบุว่าผลิตภัณฑ์ของคุณตรงตามข้อมูลจำเพาะเกี่ยวกับคุณภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ef0ed-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="ef0ed-106">คุณสามารถกำหนดรายการทดสอบแต่ละรายการกับกลุ่มการทดสอบอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="ef0ed-107">ในกรณีนี้ คุณระบุข้อมูลเฉพาะตัวของการทดสอบ เช่นค่าการประเมินที่ยอมรับได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="ef0ed-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="ef0ed-108">ค่าการวัดจะใช้ในการทดสอบเชิงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="ef0ed-109">สำหรับการทดสอบเชิงคุณภาพ จะใช้ตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="ef0ed-110">ในการทดสอบเชิงคุณภาพ ฟิลด์ **ชนิด** ถูกตั้งค่าเป็น *เลขจำนวนเต็ม* หรือ *เศษส่วน*</span><span class="sxs-lookup"><span data-stu-id="ef0ed-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="ef0ed-111">นอกจากนี้ยังระบุหน่วยวัดอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="ef0ed-111">A unit of measure is also specified.</span></span> <span data-ttu-id="ef0ed-112">ข้อมูลจำเพาะเกี่ยวกับคุณภาพและผลการทดสอบแสดงเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ef0ed-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="ef0ed-113">สำหรับการทดสอบเชิงคุณภาพ ฟิลด์ **ชนิด** ถูกตั้งค่าเป็น *ตัวเลือก*</span><span class="sxs-lookup"><span data-stu-id="ef0ed-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="ef0ed-114">การทดสอบเชิงคุณภาพต้องการข้อมูลเพิ่มเติมเกี่ยวกับตัวแปรการทดสอบที่วัดและตัวเลือกที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="ef0ed-115">ข้อมูลจำเพาะเกี่ยวกับคุณภาพและผลการทดสอบแสดงตามผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="ef0ed-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="ef0ed-116">หรือคุณอาจสามารถกำหนดเครื่องมือทดสอบให้กับการทดสอบได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="ef0ed-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="ef0ed-117">อย่างไรก็ตาม เครื่องมือทดสอบไม่พยายามที่จะสร้างและใช้การทดสอบกับใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="ef0ed-118">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เครื่องมือทดสอบการจัดการคุณภาพ](quality-test-instruments.md)</span><span class="sxs-lookup"><span data-stu-id="ef0ed-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="ef0ed-119">คุณยังสามารถระบุหน่วยของการทดสอบเพื่อระบุหน่วยวัดที่จะบันทึกผลการทดสอบได้</span><span class="sxs-lookup"><span data-stu-id="ef0ed-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="ef0ed-120">ตัวอย่างเช่น การทดสอบอุณหภูมิอาจรวมถึงหน่วยขององศาฟาเรนไฮต์ หรือองศาเซลเซียส</span><span class="sxs-lookup"><span data-stu-id="ef0ed-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="ef0ed-121">ตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-121">Example of a test</span></span>

<span data-ttu-id="ef0ed-122">บริษัทผู้ผลิตดำเนินการทดสอบวัสดุที่ซื้อสองแบบ: การทดสอบเชิงปริมาณเกี่ยวกับคุณภาพวัสดุและการทดสอบเชิงคุณภาพเกี่ยวกับความเสียหายของบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ef0ed-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="ef0ed-123">บริษัทกำหนดข้อมูลเพิ่มเติมเกี่ยวกับการทดสอบเชิงคุณภาพเพื่อระบุตัวแปรการทดสอบ (ตัวอย่างเช่น บรรจุภัณฑ์ที่เสียหาย) และผลที่ได้</span><span class="sxs-lookup"><span data-stu-id="ef0ed-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="ef0ed-124">บริษัทใช้หน้า **กลุ่มทดสอบ** เพื่อกำหนดการทดสอบทั้งสองให้กับกลุ่มการทดสอบและเพื่อระบุข้อมูลเฉพาะตัวของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="ef0ed-125">กลุ่มทดสอบจะถูกกำหนดให้ใบสั่งตรวจสอบคุณภาพ เพื่อให้บริษัทสามารถรายงานผลการทดสอบสำหรับการทดสอบทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="ef0ed-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="ef0ed-126">สร้างการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-126">Create a test</span></span>

<span data-ttu-id="ef0ed-127">ทำตามขั้นตอนเหล่านี้เพื่อสร้างการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="ef0ed-128">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> การทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="ef0ed-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="ef0ed-129">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="ef0ed-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ef0ed-130">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="ef0ed-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ef0ed-131">**การทดสอบ** – ป้อนรหัสหรือชื่อเฉพาะสำหรับการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="ef0ed-132">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="ef0ed-133">**ชนิด** – เลือกชนิดของผลลัพธ์ที่การทดสอบผลิต</span><span class="sxs-lookup"><span data-stu-id="ef0ed-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="ef0ed-134">ในการทดสอบเชิงคุณภาพ เลือก *เศษส่วน* หรือ *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="ef0ed-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="ef0ed-135">ในการทดสอบเชิงคุณภาพ เลือก *ตัวเลือก*</span><span class="sxs-lookup"><span data-stu-id="ef0ed-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="ef0ed-136">**เครื่องมือทดสอบ** – เลือก [เครื่องมือทดสอบ](quality-test-instruments.md) ที่ควรใช้ในการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="ef0ed-137">**หน่วย** – ถ้าคุณเลือก *เศษส่วน* หรือ *จํานวนเต็ม* ในฟิลด์ **ชนิด** (นั่นคือ ถ้าการทดสอบเป็นการทดสอบเชิงปริมาณ) ให้เลือกหน่วยวัดที่ควรจะบันทึกผลการทดสอบไว้</span><span class="sxs-lookup"><span data-stu-id="ef0ed-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="ef0ed-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ef0ed-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="ef0ed-139">หลังจากที่คุณบันทึกการทดสอบแล้ว คุณจะไม่สามารถแก้ไขฟิลด์ **ชนิด** ในกริดได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="ef0ed-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="ef0ed-140">ถ้าคุณต้องเปลี่ยนชนิดของผลการทดสอบที่จะบันทึกการทดสอบ ให้เลือกเปลี่ยน **ชนิดของการทดสอบคุณภาพ** ในบานหน้าต่างการดําเนินการ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="ef0ed-141">ในกล่องโต้ตอบ **เปลี่ยนชนิดของการทดสอบคุณภาพ** ให้ตั้งค่าฟิลด์ **ชนิดใหม่** เป็นชนิดที่ต้องการ แล้วเลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef0ed-142">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ef0ed-142">Additional resources</span></span>

- [<span data-ttu-id="ef0ed-143">เครื่องมือการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="ef0ed-144">กลุ่มการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="ef0ed-145">ตัวแปรการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="ef0ed-146">ความสัมพันธ์ของคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ef0ed-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
