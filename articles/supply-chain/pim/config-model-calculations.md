---
title: การคำนวณแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: หัวข้อนี้อธิบายวิธีสร้างการคำนวณสำหรับแอททริบิวต์ในผลิตภัณฑ์ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829629"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="b66a4-103">การคำนวณแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b66a4-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b66a4-104">หัวข้อนี้อธิบายวิธีสร้างการคำนวณสำหรับแอททริบิวต์ในผลิตภัณฑ์ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b66a4-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b66a4-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="b66a4-105">Prerequisites</span></span>

<span data-ttu-id="b66a4-106">สามารถใช้การคำนวณในแบบจำลองการจัดโครงแบบผลิตภัณฑ์เพื่อคำนวณค่าคอนฟิกสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b66a4-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="b66a4-107">ก่อนที่คุณจะสามารถเริ่มตั้งค่าการคํานวณได้ ต้องมีแบบจำลองการจัดโครงแบบผลิตภัณฑ์ที่เกี่ยวข้องอยู่</span><span class="sxs-lookup"><span data-stu-id="b66a4-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="b66a4-108">หากต้องการดูภาพรวมของกระบวนการตั้งค่าโมเดลการจัดโครงแบบและภารกิจที่เกี่ยวข้อง โปรดดูที่ [ตั้งค่าแบบจำลองการจัดโครงแบบผลิตภัณฑ์](set-up-maintain-product-configuration-model.md)</span><span class="sxs-lookup"><span data-stu-id="b66a4-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="b66a4-109">สร้างการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b66a4-109">Create a calculation</span></span>

<span data-ttu-id="b66a4-110">การคำนวณประกอบด้วยนิพจน์และแอททริบิวต์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="b66a4-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="b66a4-111">สำหรับข้อมูลเพิ่มเติม ดูที่ [คำถามที่พบบ่อยเกี่ยวกับการคำนวณเกี่ยวกับแบบจำลองการจัดโครงแบบผลิตภัณฑ์](calculate-product-configuration-models.md)</span><span class="sxs-lookup"><span data-stu-id="b66a4-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="b66a4-112">หากต้องการสร้างการคํานวณให้กับแบบจำลองผลิตภัณฑ์ที่มีอยู่ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b66a4-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="b66a4-113">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ทั่วไป \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="b66a4-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="b66a4-114">เปิดแบบจำลองการจัดโครงแบบผลิตภัณฑ์ แล้วเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b66a4-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="b66a4-115">บน FastTab **การคํานวณ** ให้เลือก **เพิ่ม** เพื่อเพิ่มการคํานวณ และตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b66a4-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="b66a4-116">**ชื่อ** – ป้อนชื่อสำหรับการคํานวณ</span><span class="sxs-lookup"><span data-stu-id="b66a4-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="b66a4-117">**คำอธิบาย** – ป้อนคำอธิบายเกี่ยวกับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b66a4-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="b66a4-118">**แอททริบิวต์เป้าหมาย** – เลือกแอททริบิวต์ที่คุณต้องการคํานวณ</span><span class="sxs-lookup"><span data-stu-id="b66a4-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="b66a4-119">เลือก **แก้ไขนิพจน์**</span><span class="sxs-lookup"><span data-stu-id="b66a4-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="b66a4-120">ในกล่องโต้ตอบ **ป้อนการคํานวณ** ให้เพิ่มแอททริบิวต์ ตัวปฏิบัติการ และค่าที่ต้องใช้ลงในนิพจน์</span><span class="sxs-lookup"><span data-stu-id="b66a4-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="b66a4-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้งานองค์ประกอบเหล่านี้ ดู [นิพจน์ข้อจำกัด และข้อจำกัดตาราง ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์](expression-constraints-table-constraints-product-configuration-models.md)</span><span class="sxs-lookup"><span data-stu-id="b66a4-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="b66a4-122">เมื่อนิพจน์ของคุณพร้อมแล้ว ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b66a4-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="b66a4-123">ตัวอย่างของการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b66a4-123">Calculation examples</span></span>

<span data-ttu-id="b66a4-124">ส่วนนี้มีตัวอย่างที่เกี่ยวกับวิธีการคํานวณงาน</span><span class="sxs-lookup"><span data-stu-id="b66a4-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="b66a4-125">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="b66a4-125">Example 1</span></span>

<span data-ttu-id="b66a4-126">แอตทริบิวต์เป้าหมายเป็นชนิดบูลีน และการคำนวณใช้นิพจน์เงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b66a4-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="b66a4-127">นิพจน์นี้ส่งคืนค่า *True* มายังแอททริบิวต์เป้าหมายถ้า `decimalAttribute2` มีค่ามากกว่าหรือเท่ากับ `decimalAttribute1`</span><span class="sxs-lookup"><span data-stu-id="b66a4-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="b66a4-128">มิฉะนั้น จะส่งคืนค่า บูลีน เป็น *False*</span><span class="sxs-lookup"><span data-stu-id="b66a4-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="b66a4-129">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="b66a4-129">Example 2</span></span>

<span data-ttu-id="b66a4-130">ตัวอย่างนี้ใช้แอททริบิวต์ข้อความ `textFixedList` เป็นแอททริบิวต์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="b66a4-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="b66a4-131">แอททริบิวต์นี้จะมีรายการคงที่ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b66a4-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="b66a4-132">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="b66a4-132">Value</span></span> | <span data-ttu-id="b66a4-133">ค่าของโปรแกรมแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="b66a4-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="b66a4-134">A</span><span class="sxs-lookup"><span data-stu-id="b66a4-134">A</span></span> | <span data-ttu-id="b66a4-135">1a</span><span class="sxs-lookup"><span data-stu-id="b66a4-135">1a</span></span> |
| <span data-ttu-id="b66a4-136">B</span><span class="sxs-lookup"><span data-stu-id="b66a4-136">B</span></span> | <span data-ttu-id="b66a4-137">2b</span><span class="sxs-lookup"><span data-stu-id="b66a4-137">2b</span></span> |
| <span data-ttu-id="b66a4-138">C</span><span class="sxs-lookup"><span data-stu-id="b66a4-138">C</span></span> | <span data-ttu-id="b66a4-139">2c</span><span class="sxs-lookup"><span data-stu-id="b66a4-139">2c</span></span> |

<span data-ttu-id="b66a4-140">ภาพหน้าจอต่อไปนี้จะแสดงว่าการตั้งค่าต่างๆ ของแอททริบิวต์นี้อาจมีลักษณะอย่างไรในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="b66a4-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="b66a4-141">![การตั้งค่าชนิดแอททริบิวต์สำหรับตัวอย่าง 2](media/model-calculations-example2.png "การตั้งค่าชนิดแอททริบิวต์สำหรับตัวอย่าง 2")</span><span class="sxs-lookup"><span data-stu-id="b66a4-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="b66a4-142">แอททริบิวต์จะใช้ในคำสั่งแบบมีเงื่อนไขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b66a4-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="b66a4-143">ถ้า `integerAttribute` น้อยกว่า 150 ข้อความนี้จะส่งคืนค่าข้อความของเรกคอร์ดแรกในรายการคงที่ *A* มิฉะนั้นจะส่งคืนค่าข้อความของเรกคอร์ดที่สามในรายการคงที่ *C*</span><span class="sxs-lookup"><span data-stu-id="b66a4-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="b66a4-144">รายการคงที่เทียบเท่ากับการแจงจํานวนศูนย์ (enum) และค่าเข้าถึงโดยค่าจํานวนเต็มที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="b66a4-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="b66a4-145">ดังนั้น ค่ารายการคงที่แรก (*A*) จะถูกจับคู่เป็น *0* ค่าที่สอง (*B*) จะถูกจับคู่กับ *1* และจับคู่ค่าที่สาม (*C*) เป็น *2*</span><span class="sxs-lookup"><span data-stu-id="b66a4-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="b66a4-146">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="b66a4-146">Example 3</span></span>

<span data-ttu-id="b66a4-147">ตัวอย่างนี้ใช้แอททริบิวต์เป้าหมาย `textFixedList` จากตัวอย่างก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b66a4-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="b66a4-148">คุณยังสามารถใช้แอททริบิวต์ข้อความ `textAttribute` อื่นที่มีรายการคงที่ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b66a4-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="b66a4-149">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="b66a4-149">Value</span></span> | <span data-ttu-id="b66a4-150">ค่าของโปรแกรมแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="b66a4-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="b66a4-151">AA</span><span class="sxs-lookup"><span data-stu-id="b66a4-151">AA</span></span> | <span data-ttu-id="b66a4-152">1aa</span><span class="sxs-lookup"><span data-stu-id="b66a4-152">1aa</span></span> |
| <span data-ttu-id="b66a4-153">BB</span><span class="sxs-lookup"><span data-stu-id="b66a4-153">BB</span></span> | <span data-ttu-id="b66a4-154">2bb</span><span class="sxs-lookup"><span data-stu-id="b66a4-154">2bb</span></span> |

<span data-ttu-id="b66a4-155">ภาพหน้าจอต่อไปนี้จะแสดงว่าการตั้งค่าต่างๆ ของแอททริบิวต์นี้อาจมีลักษณะอย่างไรในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="b66a4-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="b66a4-156">![การตั้งค่าชนิดแอททริบิวต์สำหรับตัวอย่าง 3](media/model-calculations-example3.png "การตั้งค่าชนิดแอททริบิวต์สำหรับตัวอย่าง 3")</span><span class="sxs-lookup"><span data-stu-id="b66a4-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="b66a4-157">ค่าแอททริบิวต์ `textFixedList` ถูกคํานวณโดยใช้ข้อความแบบมีเงื่อนไขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b66a4-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="b66a4-158">ถ้าค่า `textAttribute` มีค่าโปรแกรมแก้ปัญหาเท่ากับ *1aa* นิพจน์นี้จะส่งคืนค่าข้อความของเรกคอร์ดแรกในรายการคงที่ `textFixedList` *A* มิฉะนั้นจะส่งคืนค่าข้อความของเรกคอร์ดที่สามในรายการคงที่ `textFixedList` *C*</span><span class="sxs-lookup"><span data-stu-id="b66a4-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="b66a4-159">ใบแจ้งยอดแบบมีเงื่อนไขต้องใช้ค่าโปรแกรมแก้ปัญหาของแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="b66a4-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="b66a4-160">สามารถใช้ได้เฉพาะแอททริบิวต์ข้อความรายการคงที่เท่านั้นในการคํานวณ</span><span class="sxs-lookup"><span data-stu-id="b66a4-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="b66a4-161">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b66a4-161">See also</span></span>

- [<span data-ttu-id="b66a4-162">FAQ เกี่ยวกับการคำนวณแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b66a4-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="b66a4-163">เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b66a4-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="b66a4-164">ภาพรวมแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b66a4-164">Product configuration models overview</span></span>](product-configuration-models.md)
