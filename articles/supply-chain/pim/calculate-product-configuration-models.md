---
title: FAQ เกี่ยวกับการคำนวณแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: หัวข้อนี้อธิบายถึงการคำนวณสำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และอธิบายถึงวิธีการใช้การคำนวณร่วมกับข้อจำกัดต่างๆ
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee92f7f5cc7cbbb4af8455bdcaf1b2265102ad7c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209501"
---
# <a name="calculations-for-product-configuration-models-faq"></a><span data-ttu-id="78641-103">FAQ เกี่ยวกับการคำนวณแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="78641-103">Calculations for product configuration models FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78641-104">หัวข้อนี้อธิบายถึงการคำนวณสำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และอธิบายถึงวิธีการใช้การคำนวณร่วมกับข้อจำกัดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="78641-104">This topic describes calculations for product configuration models and explains how to use calculations together with constraints.</span></span>

<span data-ttu-id="78641-105">การคำนวณถูกใช้สำหรับการดำเนินการทางคณิตศาสตร์หรือตรรกะ</span><span class="sxs-lookup"><span data-stu-id="78641-105">Calculations can be used for arithmetic or logical operations.</span></span> <span data-ttu-id="78641-106">พวกเขานิพจน์ข้อจำกัดในแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="78641-106">They complement expression constraints in product configuration models.</span></span> <span data-ttu-id="78641-107">คุณสามารถกำหนดการคำนวณในหน้า **รายละเอียดแบบจำลองการจัดโครงแบบผลิตภัณฑ์ตามข้อจำกัด** และจากนั้น สร้างนิพจน์สำหรับการคำนวณในโปรแกรมแก้ไขนิพจน์ได้</span><span class="sxs-lookup"><span data-stu-id="78641-107">You can define calculations on the **Constraint-based product configuration model details** page and then build expressions for the calculations in the expression editor.</span></span> <span data-ttu-id="78641-108">สำหรับข้อมูลเพิ่มเติมให้ดูที่การสร้างการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="78641-108">For more information, see Create calculations.</span></span>

## <a name="what-is-a-calculation"></a><span data-ttu-id="78641-109">การคำนวณคืออะไร</span><span class="sxs-lookup"><span data-stu-id="78641-109">What is a calculation?</span></span>
<span data-ttu-id="78641-110">การคำนวณจะมีองค์ประกอบที่คุณสามารถใช้ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="78641-110">A calculation is an element that you can use in a product configuration model.</span></span> <span data-ttu-id="78641-111">การคำนวณเพิ่มข้อจำกัด โดยให้คุณใช้เลขทศนิยมเพื่อคำนวณค่าเมื่อคุณจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="78641-111">Calculations complement constraints by letting you use decimal numbers to calculate values when you configure a product.</span></span> <span data-ttu-id="78641-112">นอกจากนี้ คำนวณได้มากกว่าชุดของตัวดำเนินการพร้อมใช้งานมากกว่าข้อจำกัดที่มี</span><span class="sxs-lookup"><span data-stu-id="78641-112">Additionally, calculations have a larger set of available operators than constraints have.</span></span>  

<span data-ttu-id="78641-113">เหมือนกับข้อจำกัด การคำนวณเชื่อมโยงกับส่วนประกอบที่ระบุเจาะจงในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และไม่สามารถนำมาใช้ใหม่โดย หรือใช้ร่วมกับส่วนประกอบอื่น</span><span class="sxs-lookup"><span data-stu-id="78641-113">Like a constraint, a calculation is associated with a specific component in a product configuration model, and can’t be reused by or shared with another component.</span></span> <span data-ttu-id="78641-114">ความสำคัญหนึ่งความแตกต่างระหว่างการคำนวณและข้อจำกัดคือคำนวณที่เป็นคำสั่ง (ไม่มีทิศทาง), ในขณะที่ข้อจำกัดคือ declarative (ทิศทาง)</span><span class="sxs-lookup"><span data-stu-id="78641-114">One important difference between calculations and constraints is that calculations are imperative (unidirectional), whereas constraints are declarative (bi-directional).</span></span> <span data-ttu-id="78641-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับข้อจำกัด ดู [นิพจน์ข้อจำกัด และข้อจำกัดตาราง ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์](expression-constraints-table-constraints-product-configuration-models.md)</span><span class="sxs-lookup"><span data-stu-id="78641-115">For more information about constraints, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>  

<span data-ttu-id="78641-116">การคำนวณประกอบด้วยแอททริบิวต์เป้าหมายและนิพจน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="78641-116">A calculation consists of a target attribute and a calculation expression.</span></span>

## <a name="what-is-a-target-attribute"></a><span data-ttu-id="78641-117">แอททริบิวต์เป้าหมายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="78641-117">What is a target attribute?</span></span>
<span data-ttu-id="78641-118">แอททริบิวต์เป้าหมายคือแอททริบิวต์ที่ได้รับผลลัพธ์ของการคำนวณในนิพจน์</span><span class="sxs-lookup"><span data-stu-id="78641-118">A target attribute is an attribute that receives the result of the calculation expression.</span></span>  

<span data-ttu-id="78641-119">ในนิพจน์ต่อไปนี้ แอตทริบิวต์เป้าหมาย คือ การวัดผ้าปูโต๊ะ</span><span class="sxs-lookup"><span data-stu-id="78641-119">In the following expression, the target attribute is a tablecloth measurement:</span></span>  

<span data-ttu-id="78641-120">**นิพจน์:** If\[(decimalAttribute1 &lt;= decimalAttribute2) < 1, True, False\]</span><span class="sxs-lookup"><span data-stu-id="78641-120">**Expression:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span></span>  

<span data-ttu-id="78641-121">**DecimalAttribute1** คือ ความยาวของโต๊ะ และ **decimalAttribute2** คือ ความยาวของผ้าปูโต๊ะ</span><span class="sxs-lookup"><span data-stu-id="78641-121">**DecimalAttribute1** is the table length, and **decimalAttribute2** is the tablecloth length.</span></span> <span data-ttu-id="78641-122">นิพจน์ที่ส่งกลับค่า **เป็นจริง** กับแอททริบิวต์เป้าหมายถ้า **decimalAttribute2** มากกว่า หรือเท่ากับ **decimalAttribute1**</span><span class="sxs-lookup"><span data-stu-id="78641-122">The expression returns the value **True** to the target attribute if **decimalAttribute2** is greater than or equal to **decimalAttribute1**.</span></span> <span data-ttu-id="78641-123">มิฉะนั้น นิพจน์ส่งกลับค่า **False**</span><span class="sxs-lookup"><span data-stu-id="78641-123">Otherwise, the expression returns **False**.</span></span> <span data-ttu-id="78641-124">ดังนั้น การวัด tablecloth จะยอมรับได้ถ้าความยาว tablecloth เท่ากับ หรือเกินกว่าความยาวของตาราง</span><span class="sxs-lookup"><span data-stu-id="78641-124">Therefore, the tablecloth measurement is acceptable if the tablecloth length is the same as or exceeds the length of the table.</span></span>

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a><span data-ttu-id="78641-125">แอตทริบิวต์ชนิดใดที่สามารถกำหนดให้แอตทริบิวต์เป้าหมายได้</span><span class="sxs-lookup"><span data-stu-id="78641-125">What attribute types can be set to target attributes?</span></span>
<span data-ttu-id="78641-126">แอททริบิวต์ทุกชนิดที่เป็นตัวจัดโครงแบบผลิตภัณฑ์จะได้รับการสนับสนุนสำหรับสามารถกำหนดเป็นแอตทริบิวต์เป้าหมายได้ ยกเว้นข้อความที่ไม่มีรายการที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="78641-126">All attribute types that the product configurator supports can be set to target attributes, except text without a fixed list.</span></span>

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a><span data-ttu-id="78641-127">ค่าสำหรับเป้าหมายสามารถจำกัดค่าสำหรับแอททริบิวต์ที่ป้อนเข้าในการคำนวณได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="78641-127">Can the value of a target attribute restrict the values of the input attributes in a calculation?</span></span>
<span data-ttu-id="78641-128">ไม่ได้ ค่าสำหรับเป้าหมายไม่สามารถจำกัดค่าสำหรับแอททริบิวต์ที่ป้อนเข้าในการคำนวณได้เพราะการคำนวณไปในทิศทางเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="78641-128">No, the value of a target attribute can’t restrict the values of the input attributes, because calculations are unidirectional.</span></span> <span data-ttu-id="78641-129">ดังนั้น ค่าของแอตทริบิวต์เป้าหมายถูกกำหนดตามการเปลี่ยนแปลงค่าของแอททริบิวต์อินพุท แต่การเปลี่ยนแปลงในค่าของเป้าหมายไม่มีผลต่อค่าของแอททริบิวต์ที่ป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="78641-129">Therefore, the value of the target attribute is set based on changes in the value of the input attributes, but a change in the value of the target doesn’t affect the value of the input attributes.</span></span> <span data-ttu-id="78641-130">ลักษณะการทำงานนี้แตกต่างจากลักษณะการทำงานสำหรับข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="78641-130">This behavior differs from the behavior for constraints.</span></span> <span data-ttu-id="78641-131">ข้อจำกัดเกิดขึ้นในทั้งสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="78641-131">Constraints occur in both directions.</span></span>

### <a name="example"></a><span data-ttu-id="78641-132">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="78641-132">Example</span></span>

<span data-ttu-id="78641-133">ในนิพจน์ต่อไปนี้ เป้าหมายสำหรับการคำนวณ คือ ความยาวของสายไฟ และค่าที่ป้อน คือ สี:</span><span class="sxs-lookup"><span data-stu-id="78641-133">In the following expression, the target for the calculation is the length of a power cord, and the input value is a color:</span></span>  

<span data-ttu-id="78641-134">**นิพจน์:** \[If Color == "Green", 1.5, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="78641-134">**Expression:** \[If Color == "Green", 1.5, 1.0\]</span></span>  

<span data-ttu-id="78641-135">เมื่อคุณกำหนดค่ารายการ ความยาวของสายไฟตั้งค่าเป็น **1.5** ถ้าคุณระบุ **สีเขียว** เป็นค่าของแอตทริบิวต์สี</span><span class="sxs-lookup"><span data-stu-id="78641-135">When you configure the item, the length of the power cord is set to **1.5** if you specify **Green** as the value of color attribute.</span></span> <span data-ttu-id="78641-136">ถ้าคุณระบุสีอื่น ๆ ความยาวถูกตั้งค่าเป็น **1.0**</span><span class="sxs-lookup"><span data-stu-id="78641-136">If you specify any other color, the length is set to **1.0**.</span></span> <span data-ttu-id="78641-137">อย่างไรก็ตาม เนื่องจากการคำนวณจะไม่มีทิศทาง การคำนวณไม่ได้ตั้งค่าของแอททริบิวต์สีเป็น **สีเขียว** ถ้าคุณระบุความยาว **1.5**</span><span class="sxs-lookup"><span data-stu-id="78641-137">However, because calculations are unidirectional, the calculation doesn't set the value of the color attribute to **Green** if you specify a length of **1.5**.</span></span>

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a><span data-ttu-id="78641-138">จะเกิดอะไรขึ้นถ้าการคำนวณมีแอททริบิวต์เป้าหมายของชนิดจำนวนเต็ม แต่การคำนวณแสดงตัวเลขฐานสิบ</span><span class="sxs-lookup"><span data-stu-id="78641-138">What happens if a calculation has a target attribute of the integer type but a calculation generates a decimal number?</span></span>
<span data-ttu-id="78641-139">ถ้าแอตทริบิวต์เป้าหมายมีชนิดเป็นจำนวนเต็ม แต่การคำนวณสร้างตัวเลขฐานสิบ มีการส่งคืนเฉพาะส่วนจำนวนเต็มของผลการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="78641-139">If a target attribute is of the integer type, but a calculation generates a decimal number, only the integer part of the calculated result is returned.</span></span> <span data-ttu-id="78641-140">ส่วนทศนิยมจะถูกลบออก และผลลัพธ์ไม่ได้ปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="78641-140">The decimal part is removed, and the result isn't rounded.</span></span> <span data-ttu-id="78641-141">ตัวอย่างเช่น ผลลัพธ์ของ 12.70 จะแสดงขึ้นเป็น 12</span><span class="sxs-lookup"><span data-stu-id="78641-141">For example, a result of 12.70 is shown as 12.</span></span>

## <a name="when-do-calculations-occur"></a><span data-ttu-id="78641-142">การคำนวณจะเกิดขึ้นเมื่อไหร่</span><span class="sxs-lookup"><span data-stu-id="78641-142">When do calculations occur?</span></span>
<span data-ttu-id="78641-143">การคำนวณเกิดขึ้นเมื่อมีการให้ค่าสำหรับแอททริบิวต์ที่ป้อนข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="78641-143">Calculations occur when a value has been provided for all input attributes.</span></span>

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a><span data-ttu-id="78641-144">ฉันสามารถบันทึกทับค่าที่คำนวณได้สำหรับแอททริบิวต์เป้าหมายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="78641-144">Can I overwrite the value that is calculated for the target attribute?</span></span>
<span data-ttu-id="78641-145">คุณสามารถบันทึกทับค่าที่คำนวณได้สำหรับแอททริบิวต์เป้าหมาย ยกเว้นว่ามีการตั้งค่าแอททริบิวต์เป้าหมายให้ ซ่อนอยู่ หรือ อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="78641-145">You can overwrite the value that is calculated for the target attribute, unless the target attribute is set as hidden or read-only.</span></span>

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a><span data-ttu-id="78641-146">ฉันจะตั้งแอททริบิวต์เป้าหมายให้เป็น ซ่อนอยู่ หรือ อ่านอย่างเดียว ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="78641-146">How do I set a target attribute as hidden or read-only?</span></span>
<span data-ttu-id="78641-147">ในการตั้งค่าแอททริบิวต์ให้ ซ่อนอยู่ หรือ อ่านอย่างเดียว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="78641-147">To set an attribute as hidden or read-only, follow these steps.</span></span>

1.  <span data-ttu-id="78641-148">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ทั่วไป** &gt; **แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="78641-148">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="78641-149">เลือกแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และในบานหน้างต่างการดำเนินการ ให้คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="78641-149">Select a product configuration model, and then, on the Action Pane, click **Edit**.</span></span>
3.  <span data-ttu-id="78641-150">ในหน้า **ในหน้ารายละเอียดแบบจำลองการจัดโครงแบบผลิตภัณฑ์ตามข้อจำกัด** เลือกแอททริบิวต์เพื่อใช้เป็นแอททริบิวต์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="78641-150">On the **Constraint-based product configuration model details** page, select the attribute to use as a target attribute.</span></span>
4.  <span data-ttu-id="78641-151">ในฟาสแท็ป **แอททริบิวต์** เลือก **ซ่อน** หรือ **แบบอ่านอย่างเดียว**</span><span class="sxs-lookup"><span data-stu-id="78641-151">On the **Attributes** FastTab, select **Hidden** or **Read-only**.</span></span>

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a><span data-ttu-id="78641-152">การคำนวณสามารถบันทึกทับค่าที่ฉันตั้งได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="78641-152">Can a calculation overwrite the values that I set?</span></span>
<span data-ttu-id="78641-153">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="78641-153">No.</span></span> <span data-ttu-id="78641-154">ค่าที่คุณตั้งค่าเมื่อคุณจัดโครงแบบผลิตภัณฑ์เป็นค่าที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="78641-154">The values that you set when you configure a product are the values that are used.</span></span> <span data-ttu-id="78641-155">การคำนวณที่เกิดขึ้นเมื่อมีการเปลี่ยนแปลงมูลค่าที่ป้อนในการคำนวณ ไม่สามารถบันทึกทับค่าที่คุณระบุสำหรับแอททริบิวต์เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="78641-155">The calculation that occurs when the input values in a calculation are changed can’t overwrite the values that you provide for a specific attribute.</span></span>

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a><span data-ttu-id="78641-156">จะเกิดอะไรขึ้นถ้าฉันลบค่าป้อนเข้าในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="78641-156">What happens if I remove an input value in a calculation?</span></span>
<span data-ttu-id="78641-157">ถ้าคุณลบค่าป้อนเข้าในการคำนวณ ค่าของแอตทริบิวต์เป้าหมายจะถูกลบออกด้วย</span><span class="sxs-lookup"><span data-stu-id="78641-157">If you remove an input value in a calculation, the value of the target attribute is also removed.</span></span>

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a><span data-ttu-id="78641-158">เหตุใดฉันจึงได้รับข้อความแสดงข้อผิดพลาดว่า แบบจำลองของฉันมีความขัดแย้ง</span><span class="sxs-lookup"><span data-stu-id="78641-158">Why do I receive an error message that says that my model is in contradiction?</span></span>
<span data-ttu-id="78641-159">ข้อความนี้จะแสดงขึ้นเมื่อการคำนวณมีข้อผิดพลาด หรือเมื่อความขัดแย้งที่อยู่ในข้อจำกัดอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="78641-159">This message is shown when a calculation includes an error, or when a contradiction exists in one or more constraints.</span></span> <span data-ttu-id="78641-160">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความขัดแย้งในข้อจำกัด ดู [นิพจน์ข้อจำกัด และข้อจำกัดตาราง ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์](expression-constraints-table-constraints-product-configuration-models.md)</span><span class="sxs-lookup"><span data-stu-id="78641-160">For more information about contradictions in constraints, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span> <span data-ttu-id="78641-161">นี่คือบางสถานการณ์ที่อาจเกิดข้อผิดพลาดในการคำนวณ:</span><span class="sxs-lookup"><span data-stu-id="78641-161">Here are some situations where errors can occur in calculations:</span></span>

-   <span data-ttu-id="78641-162">ค่าจะถูกหารด้วยศูนย์</span><span class="sxs-lookup"><span data-stu-id="78641-162">A value is divided by 0 (zero).</span></span>
-   <span data-ttu-id="78641-163">มีความขัดแย้งระหว่างสององค์ประกอบเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="78641-163">A conflict exists between the following two elements:</span></span>
    -   <span data-ttu-id="78641-164">ค่าที่พร้อมใช้งานสำหรับแอททริบิวต์และถูกจำกัดโดยข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="78641-164">The values that are available for an attribute and are limited by a constraint</span></span>
    -   <span data-ttu-id="78641-165">ค่าที่สร้างขึ้นโดยการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="78641-165">A value that is generated by a calculation</span></span>
-   <span data-ttu-id="78641-166">ค่าที่ส่งคืนโดยการคำนวณอยู่นอกโดเมนของแอททริบิวต์ </span><span class="sxs-lookup"><span data-stu-id="78641-166">The values that are returned by the calculation are outside the domain of the attribute.</span></span> <span data-ttu-id="78641-167">ตัวอย่างเช่น จำนวนเต็มจาก \[1..10\] ที่คำนวณได้เป็น 0</span><span class="sxs-lookup"><span data-stu-id="78641-167">An example is an integer from \[1..10\] that is calculated to 0.</span></span>

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a><span data-ttu-id="78641-168">เหตุใดฉันจึงได้รับข้อผิดพลาดแม้ว่าฉันตรวจสอบแบบจำลองผลิตภัณฑ์ของฉันเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="78641-168">Why do I receive an error message even though I successfully validated my product model?</span></span>
<span data-ttu-id="78641-169">คำนวณไม่ได้รวมอยู่ในการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="78641-169">Calculations aren't included in the validation.</span></span> <span data-ttu-id="78641-170">คุณต้องทดสอบการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์จำลองเพื่อหาข้อผิดพลาดในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="78641-170">You must test the product configuration model to find errors in calculations.</span></span> <span data-ttu-id="78641-171">ขั้นตอนต่อไปนี้อธิบายวิธีการทดสอบแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="78641-171">To test a product configuration model, follow these steps.</span></span>

1.  <span data-ttu-id="78641-172">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ทั่วไป** &gt; **แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="78641-172">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="78641-173">เลือกแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และจากนั้นในบานหน้าต่างการดำเนินการ ในกลุ่ม **รัน** ให้คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="78641-173">Select a product configuration model, and then, on the Action Pane, in the **Run** group, click **Test**.</span></span>




