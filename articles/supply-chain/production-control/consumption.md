---
title: "คำนวณปริมาณการใช้วัสดุ"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับตัวเลือกต่างๆ ที่เกี่ยวข้องกับการคำนวณปริมาณการใช้วัสดุ"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3e4010b5abb6b5a871d098422f1489cb2db3a071
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="calculate-material-consumption"></a><span data-ttu-id="a626d-103">คำนวณปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="a626d-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a626d-104">บทความนี้แสดงข้อมูลเกี่ยวกับตัวเลือกต่างๆ ที่เกี่ยวข้องกับการคำนวณปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="a626d-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="a626d-105">ตัวเลือกต่อไปนี้ที่สัมพันธ์กับการคำนวณปริมาณการใช้วัสดุจะพร้อมใช้งานในแท็บ **ตั้งค่า** และ **ปริมาณการใช้ขั้นตอน** ในแท็บด่วน **รายละเอียดรายการ** ของหน้า **สูตรการผลิต**</span><span class="sxs-lookup"><span data-stu-id="a626d-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="a626d-106">ปริมาณการใช้วัสดุแปรผันและคงที่</span><span class="sxs-lookup"><span data-stu-id="a626d-106">Variable and constant consumption</span></span>
<span data-ttu-id="a626d-107">ในฟิลด์ **ปริมาณการใช้คือ** คุณสามารถเลือกว่าควรคำนวณปริมาณการใช้วัสดุเป็นปริมาณคงหรือผันแปรปริมาณได้</span><span class="sxs-lookup"><span data-stu-id="a626d-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="a626d-108">เลือก **คงที่** หากปริมาณหรือปริมาตรคงที่ต้องถูกระบุสำหรับการผลิตโดยไม่คำนึงถึงปริมาณที่มีการผลิต</span><span class="sxs-lookup"><span data-stu-id="a626d-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="a626d-109">เลือก **ตัวแปร**ซึ่งเป็นการตั้งค่าเริ่มต้น ถ้าจำนวนของวัตถุดิบที่ต้องการในสินค้าสำเร็จรูปเป็นสัดส่วนกับจำนวนสินค้าสำเร็จรูปที่มีการผลิต</span><span class="sxs-lookup"><span data-stu-id="a626d-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="a626d-110">การคำนวณปริมาณการใช้วัสดุจากสูตร</span><span class="sxs-lookup"><span data-stu-id="a626d-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="a626d-111">ในฟิลด์ **สูตร** คุณสามารถตั้งค่าสูตรที่หลากหลายสำหรับการคำนวณปริมาณการใช้วัสดุตได้</span><span class="sxs-lookup"><span data-stu-id="a626d-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="a626d-112">ถ้าคุณใช้ค่าเริ่มต้น **มาตรฐาน** ปริมาณการใช้จะไม่ได้คำนวณมาจากสูตร</span><span class="sxs-lookup"><span data-stu-id="a626d-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="a626d-113">สูตรต่อไปนี้ทำงานร่วมกับฟิลด์ **ความสูง****ความกว้าง****ความลึก****ความหนาแน่น** และ **ค่าคงที่**:</span><span class="sxs-lookup"><span data-stu-id="a626d-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="a626d-114">ความสูง \* ค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="a626d-114">Height \* Constant</span></span>
-   <span data-ttu-id="a626d-115">ความสูง \* ความกว้าง \* ค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="a626d-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="a626d-116">ความสูง \* ความกว้าง \* ความลึก \* ค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="a626d-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="a626d-117">(ความสูง \* ความกว้าง \* ความลึก / ความหนาแน่น) \* ค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="a626d-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="a626d-118">การปัดเศษขึ้นและการคูณ</span><span class="sxs-lookup"><span data-stu-id="a626d-118">Rounding up and multiples</span></span>
<span data-ttu-id="a626d-119">ทั้งฟิลด์ **การปัดเศษขึ้น** และ **การคูณ** จะช่วยให้คุณสามารถปัดเศษค่าปริมาณการใช้วัสดุได้</span><span class="sxs-lookup"><span data-stu-id="a626d-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="a626d-120">ตัวอย่างเช่น คุณสามารถปัดเศษค่าตามหน่วยจัดการวัสดุที่วัตถุดิบมีการเบิกสินค้าสำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="a626d-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="a626d-121">ตัวเลือกต่อไปนี้พร้อมใช้งานในฟิลด์ **การปัดเศษขึ้น**: **ปริมาณ** **การวัด**และ **ปริมาณการใช้วัสดุ**</span><span class="sxs-lookup"><span data-stu-id="a626d-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="a626d-122">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a626d-122">Quantity</span></span>

<span data-ttu-id="a626d-123">ถ้าคุณเลือก **ปริมาณ** ให้เป็นกลไกการปัดเศษ ปริมาณต้องเป็นตัวคูณของปริมาณที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a626d-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="a626d-124">ตัวอย่างเช่น ถ้าจำเป็นต้องมีตัวเลขจำนวนเต็ม ให้เลือก **1** ในฟิลด์ **การคูณ**</span><span class="sxs-lookup"><span data-stu-id="a626d-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="a626d-125">จากนั้นหมายเลขจะถูกปัดเศษขึ้นเป็นปริมาณที่สามารถหารด้วย 1 ลงตัว</span><span class="sxs-lookup"><span data-stu-id="a626d-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="a626d-126">การวัด</span><span class="sxs-lookup"><span data-stu-id="a626d-126">Measurement</span></span>

<span data-ttu-id="a626d-127">โดยทั่วไป คุณเลือก **การวัด** ให้เป็นกลไกการปัดเศษขึ้นเมื่อวัตถุดิบอยู่ในมิติเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="a626d-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="a626d-128">ตัวอย่างเช่น ท่อโลหะยาว 2 เมตรจำนวน 1 ชิ้นที่ต้องใช้สำหรับสินค้าสำเร็จรูป และท่อโลหะถูกจัดเก็บในความยาวที่ 4.5 เมตร</span><span class="sxs-lookup"><span data-stu-id="a626d-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="a626d-129">ในกรณีนี้ กลไกการปัดเศษ **การวัด** สามารถใช้เพื่อคำนวณจำนวนท่อโลหะที่จำเป็นต่อการผลิตจำนวนชิ้นที่ต้องการของสินค้าสำเร็จรูปได้</span><span class="sxs-lookup"><span data-stu-id="a626d-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="a626d-130">สำหรับตัวอย่างนี้ ฟิลด์ **สูตร** ถูกตั้งค่าเป็น **ความสูง \* ค่าคงที่**</span><span class="sxs-lookup"><span data-stu-id="a626d-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="a626d-131">ฟิลด์ **ความสูง** ถูกตั้งค่าเป็น **2** เพื่อระบุความยาวของท่อที่จำเป็นสำหรับสินค้าสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="a626d-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="a626d-132">ฟิลด์ **การคูณ** ถูกกำหนดเป็น **4.5** เพื่อบ่งชี้ว่ามีการเบิกท่อที่มีความยาว 4.5 เมตร</span><span class="sxs-lookup"><span data-stu-id="a626d-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="a626d-133">นี่คือการคำนวณ:</span><span class="sxs-lookup"><span data-stu-id="a626d-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="a626d-134">จำนวนเของการคูณที่จำเป็นสำหรับสินค้าสำเร็จรูป 10 ชิ้น: 10 ÷ 2 = 5 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="a626d-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="a626d-135">ปริมาณการใช้วัสดุรวม: 4.5 × 5 = 22.5 เมตรของท่อโลหะ</span><span class="sxs-lookup"><span data-stu-id="a626d-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="a626d-136">มีการสันนิษฐานว่า จะสูญเสียท่อยาว 0.5 เมตรสำหรับการใช้ท่อทุกๆห้าชิ้น</span><span class="sxs-lookup"><span data-stu-id="a626d-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="a626d-137">ปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="a626d-137">Consumption</span></span>

<span data-ttu-id="a626d-138">โดยทั่วไป คุณเลือก**ปริมาณการใช้วัสดุ** ให้เป็นกลไกการปัดเศษขึ้นเมื่อต้องมีการเบิกวัตถุดิบในปริมาณทั้งหมดของหน่วยจัดการวัสดุที่เฉพาะเจาะจงของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a626d-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="a626d-139">ตัวอย่างเช่น สี 2 ควอร์ตจะถูกใช้ในการผลิตสินค้าสำเร็จรูปหนึ่งชิ้น และมีการเบิกสีกระป๋อง 25 ควอร์ต</span><span class="sxs-lookup"><span data-stu-id="a626d-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="a626d-140">ในกรณีนี้ กลไกการปัดเศษ **ปริมาณการใช้วัสดุ** สามารถใช้เพื่อปัดเศษปริมาณการใช้วัสดุเป็นจำนวนเต็มของกระป๋อง 25 ควอร์ตได้</span><span class="sxs-lookup"><span data-stu-id="a626d-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="a626d-141">นี่เป็นการคำนวณจำนวนสีที่ต้องการ ถ้าต้องมีการผลิตสินค้าสำเร็จรูปจำนวน 180 ชิ้น:</span><span class="sxs-lookup"><span data-stu-id="a626d-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="a626d-142">สีที่ต้องการ ซึ่งไม่รวมของเสีย: 180 x 2 = 360 ควอร์ต</span><span class="sxs-lookup"><span data-stu-id="a626d-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="a626d-143">จำนวนของกระป๋อง: 360 ÷ 25 = 14.4 ซึ่งถูกปัดเศษขึ้นเป็น 15</span><span class="sxs-lookup"><span data-stu-id="a626d-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="a626d-144">สีที่ต้องการ ซึ่งรวมของเสีย: 15 x 25 = 375 ควอร์ต</span><span class="sxs-lookup"><span data-stu-id="a626d-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="a626d-145">ปริมาณการใช้ขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="a626d-145">Step consumption</span></span>
<span data-ttu-id="a626d-146">ปริมาณการใช้ขั้นตอนถูกใช้เพื่อคำนวณปริมาณการใช้วัสดุคงที่ในช่วงของปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a626d-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="a626d-147">ถ้าคุณเลือก **ปริมาณการใช้ขั้นตอน** ในฟิลด์ **สูตร** บนแท็บ **ตั้งค่า** คุณสามารถเพิ่มข้อมูลเกี่ยวกับขั้นตอนต่าง ๆ ได้ในแท็บ **ปริมาณการใช้ขั้นตอน** ปริมาณที่ใช้แบบคงที่สามารถถูกตั้งค่าในช่วงของปริมาณที่มีการผลิต</span><span class="sxs-lookup"><span data-stu-id="a626d-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="a626d-148">ตัวอย่างเช่น ปริมาณการใช้ขั้นตอนถูกตั้งค่าดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a626d-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="a626d-149">จากชุด</span><span class="sxs-lookup"><span data-stu-id="a626d-149">From series</span></span> | <span data-ttu-id="a626d-150">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a626d-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="a626d-151">0.00</span><span class="sxs-lookup"><span data-stu-id="a626d-151">0.00</span></span>        | <span data-ttu-id="a626d-152">10.0000</span><span class="sxs-lookup"><span data-stu-id="a626d-152">10.0000</span></span>  |
| <span data-ttu-id="a626d-153">100.00</span><span class="sxs-lookup"><span data-stu-id="a626d-153">100.00</span></span>      | <span data-ttu-id="a626d-154">20.0000</span><span class="sxs-lookup"><span data-stu-id="a626d-154">20.0000</span></span>  |
| <span data-ttu-id="a626d-155">200.00</span><span class="sxs-lookup"><span data-stu-id="a626d-155">200.00</span></span>      | <span data-ttu-id="a626d-156">40.0000</span><span class="sxs-lookup"><span data-stu-id="a626d-156">40.0000</span></span>  |

<span data-ttu-id="a626d-157">ปริมาณของสูตรการผลิต (BOM) คือ 1 และปริมาณการผลิตคือ 110</span><span class="sxs-lookup"><span data-stu-id="a626d-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="a626d-158">สูตรสำหรับปริมาณการใช้คือ จากชุด (ปริมาณ) = ปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="a626d-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="a626d-159">เนื่องจากปริมาณการผลิตคือ 110 จึงอยู่ใน "จาก 100 ชุด"</span><span class="sxs-lookup"><span data-stu-id="a626d-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="a626d-160">ดังนั้น ปริมาณคือ 20</span><span class="sxs-lookup"><span data-stu-id="a626d-160">Therefore, the quantity is 20.</span></span>




