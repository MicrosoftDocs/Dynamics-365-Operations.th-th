---
title: "นิพจน์ข้อจำกัดและข้อจำกัดของตารางในแบบจำลองการจัดโครงแบบผลิตภัณฑ์"
description: "หัวข้อนี้อธิบายการใช้ข้อจำกัดนิพจน์และข้อจำกัดตาราง  ข้อจำกัดถูกใช้ในการควบคุมค่าแอททริบิวต์ที่คุณสามารถเลือกได้เมื่อคุณจัดโครงแบบผลิตภัณฑ์สำหรับใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อ หรือใบสั่งผลิต คุณสามารถใช้ข้อจำกัดนิพจน์หรือข้อจำกัดตาราง ขึ้นอยู่กับวิธีที่คุณต้องการสร้างข้อจำกัด"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e4719ace2247eb95ed711b0c82e7d9bc8ec5c60c
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="799fd-105">นิพจน์ข้อจำกัดและข้อจำกัดของตารางในแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="799fd-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="799fd-106">หัวข้อนี้อธิบายการใช้ข้อจำกัดนิพจน์และข้อจำกัดตาราง </span><span class="sxs-lookup"><span data-stu-id="799fd-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="799fd-107">ข้อจำกัดถูกใช้ในการควบคุมค่าแอททริบิวต์ที่คุณสามารถเลือกได้เมื่อคุณจัดโครงแบบผลิตภัณฑ์สำหรับใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อ หรือใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="799fd-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="799fd-108">คุณสามารถใช้ข้อจำกัดนิพจน์หรือข้อจำกัดตาราง ขึ้นอยู่กับวิธีที่คุณต้องการสร้างข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="799fd-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="799fd-109">ข้อจำกัดถูกใช้ในการควบคุมค่าแอททริบิวต์ที่คุณสามารถเลือกได้เมื่อคุณจัดโครงแบบผลิตภัณฑ์สำหรับใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อ หรือใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="799fd-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="799fd-110">คุณสามารถใช้นิพจน์ข้อจำกัดหรือข้อจำกัดตาราง ขึ้นอยู่กับว่าคุณต้องการสร้างข้อจำกัดอย่างไร</span><span class="sxs-lookup"><span data-stu-id="799fd-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="799fd-111">ข้อจำกัดนิพจน์คืออะไร</span><span class="sxs-lookup"><span data-stu-id="799fd-111">What are expression constraints?</span></span>
<span data-ttu-id="799fd-112">ข้อจำกัดนิพจน์จะถูกกำหนดลักษณะตามนิพจน์ที่ใช้ฟังก์ชันและตัวดำเนินการคณิตศาสตร์และบูลีน</span><span class="sxs-lookup"><span data-stu-id="799fd-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="799fd-113">มีการบันทึกข้อจำกัดนิพจน์สำหรับส่วนประกอบเฉพาะในแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="799fd-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="799fd-114">ไม่สามารถนำมาใช้ใหม่หรือใช้ร่วมกับส่วนประกอบอื่น</span><span class="sxs-lookup"><span data-stu-id="799fd-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="799fd-115">อย่างไรก็ตาม ข้อจำกัดนิพจน์สำหรับส่วนประกอบสามารถอ้างอิงแอททริบิวต์ของส่วนประกอบย่อยของส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="799fd-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="799fd-116">ข้อจำกัดของตารางคืออะไร</span><span class="sxs-lookup"><span data-stu-id="799fd-116">What are table constraints?</span></span>
<span data-ttu-id="799fd-117">ข้อจำกัดตารางแสดงชุดของค่าที่อนุญาตสำหรับแอททริบิวต์เมื่อคุณจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="799fd-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="799fd-118">สามารถใช้คำนิยามข้อจำกัดตารางโดยทั่วไป</span><span class="sxs-lookup"><span data-stu-id="799fd-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="799fd-119">เมื่อคุณสร้างข้อจำกัดตารางสำหรับองค์ประกอบในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ คุณเลือกคำนิยามข้อจำกัดตาราง</span><span class="sxs-lookup"><span data-stu-id="799fd-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="799fd-120">เพื่อสร้างชุดข้อมูลที่ได้รับอนุญาต เพิ่มแอททริบิวต์ของชนิดเฉพาะกับส่วนประกอบต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="799fd-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="799fd-121">แอททริบิวต์แต่ละชนิดมีค่าระบุไว้</span><span class="sxs-lookup"><span data-stu-id="799fd-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="799fd-122">ตัวอย่างข้อจำกัดตาราง</span><span class="sxs-lookup"><span data-stu-id="799fd-122">Example of a table constraint</span></span>

<span data-ttu-id="799fd-123">ตัวอย่างนี้แสดงว่าคุณสามารถจำกัดการตั้งค่าคอนฟิกของลำโพงเพื่อเสร็จสิ้นการ cabinet เฉพาะและ fronts</span><span class="sxs-lookup"><span data-stu-id="799fd-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="799fd-124">ตารางแรกแสดง cabinet เสร็จสิ้นและ fronts ที่พร้อมใช้งานสำหรับการตั้งค่าคอนฟิกโดยทั่วไป</span><span class="sxs-lookup"><span data-stu-id="799fd-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="799fd-125">ค่ากำหนดไว้สำหรับชนิดของแอททริบิวต์ **Cabinet เสร็จสิ้น**และ **grill หน้า**</span><span class="sxs-lookup"><span data-stu-id="799fd-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="799fd-126">ชนิดของแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="799fd-126">Attribute type</span></span> | <span data-ttu-id="799fd-127">ค่า</span><span class="sxs-lookup"><span data-stu-id="799fd-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="799fd-128">cabinet เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="799fd-128">Cabinet finish</span></span> | <span data-ttu-id="799fd-129">สีดำ ไม้โอ้ค Rosewood สีขาว</span><span class="sxs-lookup"><span data-stu-id="799fd-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="799fd-130">Grill หน้า</span><span class="sxs-lookup"><span data-stu-id="799fd-130">Front grill</span></span>    | <span data-ttu-id="799fd-131">สีดำ โลหะ สีขาว</span><span class="sxs-lookup"><span data-stu-id="799fd-131">Black, Metal, White</span></span>         |

<span data-ttu-id="799fd-132">ตารางถัดไปแสดงชุดข้อมูลที่กำหนดโดยข้อจำกัดตาราง **สีและเสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="799fd-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="799fd-133">โดยการใช้ข้อจำกัดตารางนี้ คุณสามารถตั้งค่าคอนฟิกลำโพงที่มีไม้โอ้คเสร็จสิ้น และ grill เป็นสีดำ Rosewood เสร็จสิ้น และ grill เป็นสีขาว และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="799fd-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="799fd-134">เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="799fd-134">Finish</span></span>         | <span data-ttu-id="799fd-135">Grill</span><span class="sxs-lookup"><span data-stu-id="799fd-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="799fd-136">ไม้โอ้ค</span><span class="sxs-lookup"><span data-stu-id="799fd-136">Oak</span></span>            | <span data-ttu-id="799fd-137">สีดำ</span><span class="sxs-lookup"><span data-stu-id="799fd-137">Black</span></span>                       |
| <span data-ttu-id="799fd-138">โรสวูด</span><span class="sxs-lookup"><span data-stu-id="799fd-138">Rosewood</span></span>       | <span data-ttu-id="799fd-139">สีขาว</span><span class="sxs-lookup"><span data-stu-id="799fd-139">White</span></span>                       |
| <span data-ttu-id="799fd-140">สีขาว</span><span class="sxs-lookup"><span data-stu-id="799fd-140">White</span></span>          | <span data-ttu-id="799fd-141">สีดำ</span><span class="sxs-lookup"><span data-stu-id="799fd-141">Black</span></span>                       |
| <span data-ttu-id="799fd-142">สีขาว</span><span class="sxs-lookup"><span data-stu-id="799fd-142">White</span></span>          | <span data-ttu-id="799fd-143">สีขาว</span><span class="sxs-lookup"><span data-stu-id="799fd-143">White</span></span>                       |
| <span data-ttu-id="799fd-144">สีดำ</span><span class="sxs-lookup"><span data-stu-id="799fd-144">Black</span></span>          | <span data-ttu-id="799fd-145">สีดำ</span><span class="sxs-lookup"><span data-stu-id="799fd-145">Black</span></span>                       |
| <span data-ttu-id="799fd-146">สีดำ</span><span class="sxs-lookup"><span data-stu-id="799fd-146">Black</span></span>          | <span data-ttu-id="799fd-147">โลหะ</span><span class="sxs-lookup"><span data-stu-id="799fd-147">Metal</span></span>                       | 

<span data-ttu-id="799fd-148">คุณสามารถสร้างข้อจำกัดตารางการที่กำหนดโดยระบบและโดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="799fd-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="799fd-149">ดูข้อมูลเพิ่มเติม [ข้อจำกัดตารางที่ระบบกำหนดและกำหนดผู้ใช้](system-defined-user-defined-table-constraints.md)</span><span class="sxs-lookup"><span data-stu-id="799fd-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="799fd-150">ไวยากรณ์ใดควรใช้ในการบันทึกข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="799fd-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="799fd-151">คุณต้องใช้ไวยากรณ์ Optimization Modeling Language (OML) เมื่อคุณเขียนข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="799fd-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="799fd-152">ระบบใช้โปรแกรมแก้ปัญหาข้อจำกัด Microsoft Solver Foundation เพื่อแก้ไขข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="799fd-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="799fd-153">ฉันควรใช้ข้อจำกัดตารางหรือข้อจำกัดนิพจน์</span><span class="sxs-lookup"><span data-stu-id="799fd-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="799fd-154">คุณสามารถใช้ทั้งนิพจน์ข้อจำกัดหรือข้อจำกัดตาราง ขึ้นอยู่กับว่าคุณต้องการสร้างข้อจำกัดอย่างไร</span><span class="sxs-lookup"><span data-stu-id="799fd-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="799fd-155">คุณสร้างข้อจำกัดตารางเป็นเมทริกซ์ ในขณะที่ข้อจำกัดนิพจน์เป็นคำสั่งแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="799fd-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="799fd-156">เมื่อคุณจัดโครงแบบผลิตภัณฑ์ ไม่สำคัญว่าจะใช้ชนิดของข้อจำกัดใด</span><span class="sxs-lookup"><span data-stu-id="799fd-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="799fd-157">ตัวอย่างต่อไปนี้จะแสดงความแตกต่างของสองวิธี</span><span class="sxs-lookup"><span data-stu-id="799fd-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="799fd-158">เมื่อคุณจัดโครงแบบผลิตภัณฑ์โดยใช้การตั้งค่าข้อจำกัดต่อไปนี้ ชุดข้อมูลเหล่านี้ได้รับอนุญาต:</span><span class="sxs-lookup"><span data-stu-id="799fd-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="799fd-159">ผลิตภัณฑ์สีดำ และขนาด 30 หรือ 50</span><span class="sxs-lookup"><span data-stu-id="799fd-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="799fd-160">ผลิตภัณฑ์สีแดง และขนาด 20</span><span class="sxs-lookup"><span data-stu-id="799fd-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="799fd-161">การตั้งค่าข้อจำกัดตาราง</span><span class="sxs-lookup"><span data-stu-id="799fd-161">Table constraint setup</span></span>

| <span data-ttu-id="799fd-162">สี</span><span class="sxs-lookup"><span data-stu-id="799fd-162">Color</span></span> | <span data-ttu-id="799fd-163">ขนาด</span><span class="sxs-lookup"><span data-stu-id="799fd-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="799fd-164">สีดำ</span><span class="sxs-lookup"><span data-stu-id="799fd-164">Black</span></span> | <span data-ttu-id="799fd-165">30</span><span class="sxs-lookup"><span data-stu-id="799fd-165">30</span></span>   |
| <span data-ttu-id="799fd-166">สีดำ</span><span class="sxs-lookup"><span data-stu-id="799fd-166">Black</span></span> | <span data-ttu-id="799fd-167">50</span><span class="sxs-lookup"><span data-stu-id="799fd-167">50</span></span>   |
| <span data-ttu-id="799fd-168">สีแดง</span><span class="sxs-lookup"><span data-stu-id="799fd-168">Red</span></span>   | <span data-ttu-id="799fd-169">20</span><span class="sxs-lookup"><span data-stu-id="799fd-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="799fd-170">การตั้งค่าข้อจำกัดนิพจน์</span><span class="sxs-lookup"><span data-stu-id="799fd-170">Expression constraint setup</span></span>

<span data-ttu-id="799fd-171">(สี == "ดำ" & (ขนาด == "30" | ขนาด == "50")) | (สี == "แดง" & ขนาด = "20")</span><span class="sxs-lookup"><span data-stu-id="799fd-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="799fd-172">ฉันควรใช้ตัวดำเนินการ หรือ infix สัญลักษณ์เมื่อฉันเขียนข้อจำกัดนิพจน์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="799fd-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="799fd-173">คุณสามารถเขียนข้อจำกัดนิพจน์ โดยใช้ทั้งตัวดำเนินการคำนำหน้าที่พร้อมใช้งาน หรือ สัญลักษณ์ infix</span><span class="sxs-lookup"><span data-stu-id="799fd-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="799fd-174">สำหรับการดำเนินการ **Min**, **Max** และ **Abs**คุณไม่สามารถใช้สัญลักษณ์ infix ได้</span><span class="sxs-lookup"><span data-stu-id="799fd-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="799fd-175">ตัวดำเนินการเหล่านี้จะรวมเป็นตัวดำเนินการมาตรฐานในภาษาการเขียนโปรแกรมส่วนใหญ่</span><span class="sxs-lookup"><span data-stu-id="799fd-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="799fd-176">ตัวดำเนินการและสัญลักษณ์ infix ใดที่ฉันสามารถใช้เขียนข้อจำกัดนิพจน์</span><span class="sxs-lookup"><span data-stu-id="799fd-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="799fd-177">ตารางต่อไปนี้แสดงรายการตัวดำเนินการและสัญลักษณ์ infix ที่คุณสามารถใช้เมื่อคุณเขียนข้อจำกัดนิพจน์สำหรับส่วนประกอบในแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="799fd-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="799fd-178">ในตัวอย่างในตารางแรกนี้ แสดงวิธีการเขียนนิพจน์โดยใช้สัญลักษณ์ infix หรือตัวดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="799fd-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="799fd-179">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="799fd-179">Operator</span></span></th>
<th><span data-ttu-id="799fd-180">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="799fd-180">Description</span></span></th>
<th><span data-ttu-id="799fd-181">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="799fd-181">Syntax</span></span></th>
<th><span data-ttu-id="799fd-182">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="799fd-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="799fd-183">บ่งชี้</span><span class="sxs-lookup"><span data-stu-id="799fd-183">Implies</span></span></td>
<td><span data-ttu-id="799fd-184">จะเป็นจริงหากเงื่อนไขแรกเป็นเท็จ เงื่อนไขที่สองเป็นจริง หรือทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="799fd-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="799fd-185">บ่งชี้[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="799fd-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="799fd-186"><strong>ตัวดำเนินการ:</strong> หมายถึง [x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="799fd-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="799fd-187"><strong>Infix สัญลักษณ์:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="799fd-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="799fd-188">และ</span><span class="sxs-lookup"><span data-stu-id="799fd-188">And</span></span></td>
<td><span data-ttu-id="799fd-189">จะเป็นจริงหากเงื่อนไขทั้งหมดเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="799fd-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="799fd-190">ถ้าหมายเลขของเงื่อนไขเป็น 0 (ศูนย์) จะให้ผล <strong>จริง</strong></span><span class="sxs-lookup"><span data-stu-id="799fd-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="799fd-191">และ [args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="799fd-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="799fd-192"><strong>ตัวดำเนินการ:</strong> และ [x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="799fd-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="799fd-193"><strong>สัญลักษณ์ Infix:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="799fd-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="799fd-194">หรือ</span><span class="sxs-lookup"><span data-stu-id="799fd-194">Or</span></span></td>
<td><span data-ttu-id="799fd-195">จะเป็นจริงหากเงื่อนไขใดๆ เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="799fd-195">This is true if any condition is true.</span></span> <span data-ttu-id="799fd-196">ถ้าหมายเลขของเงื่อนไขเป็น 0 (ศูนย์) จะให้ผล <strong>เท็จ</strong></span><span class="sxs-lookup"><span data-stu-id="799fd-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="799fd-197">หรือ[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="799fd-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="799fd-198"><strong>ตัวดำเนินการ:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="799fd-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="799fd-199"><strong>สัญลักษณ์ Infix:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="799fd-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="799fd-200">บวก</span><span class="sxs-lookup"><span data-stu-id="799fd-200">Plus</span></span></td>
<td><span data-ttu-id="799fd-201">คือผลรวมเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="799fd-201">This sums its conditions.</span></span> <span data-ttu-id="799fd-202">ถ้าหมายเลขของเงื่อนไขเป็น 0 (ศูนย์) จะให้ผล <strong>0</strong></span><span class="sxs-lookup"><span data-stu-id="799fd-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="799fd-203">บวก[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="799fd-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="799fd-204"><strong>ตัวดำเนินการ:</strong> บวก[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="799fd-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="799fd-205"><strong>สัญลักษณ์ Infix:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="799fd-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="799fd-206">ลบ</span><span class="sxs-lookup"><span data-stu-id="799fd-206">Minus</span></span></td>
<td><span data-ttu-id="799fd-207">ปฏิเสธอาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="799fd-207">This negates its argument.</span></span> <span data-ttu-id="799fd-208">ต้องมีเพียงหนึ่งเงื่อนไขที่ตรงทุกประการ</span><span class="sxs-lookup"><span data-stu-id="799fd-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="799fd-209">ลบ[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="799fd-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="799fd-210"><strong>ตัวดำเนินการ:</strong> ลบ[x] == y</span><span class="sxs-lookup"><span data-stu-id="799fd-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="799fd-211"><strong>สัญลักษณ์ Infix:</strong>-x == y</span><span class="sxs-lookup"><span data-stu-id="799fd-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="799fd-212">Abs</span><span class="sxs-lookup"><span data-stu-id="799fd-212">Abs</span></span></td>
<td><span data-ttu-id="799fd-213">นำค่าสัมบูรณ์ของเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="799fd-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="799fd-214">ต้องมีเพียงหนึ่งเงื่อนไขที่ตรงทุกประการ</span><span class="sxs-lookup"><span data-stu-id="799fd-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="799fd-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="799fd-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="799fd-216"><strong>ตัวดำเนินการ:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="799fd-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="799fd-217">เวลา</span><span class="sxs-lookup"><span data-stu-id="799fd-217">Times</span></span></td>
<td><span data-ttu-id="799fd-218">นำผลิตภัณฑ์ของเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="799fd-218">This takes the product of its conditions.</span></span> <span data-ttu-id="799fd-219">ถ้าหมายเลขของเงื่อนไขเป็น 0 (ศูนย์) จะให้ผล <strong>1</strong></span><span class="sxs-lookup"><span data-stu-id="799fd-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="799fd-220">เวลา[args], infix: a * b * ... * z</span><span class="sxs-lookup"><span data-stu-id="799fd-220">Times[args], infix: a * b * ... * z</span></span></td>
<td><ul>
<li><span data-ttu-id="799fd-221"><strong>ตัวดำเนินการ:</strong> เวลา[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="799fd-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="799fd-222"><strong>สัญลักษณ์ Infix:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="799fd-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="799fd-223">กำลัง</span><span class="sxs-lookup"><span data-stu-id="799fd-223">Power</span></span></td>
<td><span data-ttu-id="799fd-224">นำเลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="799fd-224">This takes an exponential.</span></span> <span data-ttu-id="799fd-225">มีเลขยกกำลังจากขวาไปซ้าย</span><span class="sxs-lookup"><span data-stu-id="799fd-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="799fd-226">(กล่าวอีกอย่างหนึ่งคือ สัมพันธ์ทางขวา) ดังนั้น <strong>กำลัง [a, b, c]</strong> จะเท่ากับ <strong>กำลัง [a, กำลัง [b, c]]</strong></span><span class="sxs-lookup"><span data-stu-id="799fd-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="799fd-227"><strong>กำลัง</strong> สามารถใช้ได้เมื่อการยกกำลังมีค่าเป็นค่าบวกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="799fd-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="799fd-228">กำลัง[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="799fd-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="799fd-229"><strong>ตัวดำเนินการ:</strong> กำลัง[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="799fd-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="799fd-230"><strong>สัญลักษณ์ Infix:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="799fd-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="799fd-231">สูงสุด</span><span class="sxs-lookup"><span data-stu-id="799fd-231">Max</span></span></td>
<td><span data-ttu-id="799fd-232">ก่อให้เกิดเงื่อนไขใหญ่ที่สุด</span><span class="sxs-lookup"><span data-stu-id="799fd-232">This produces the largest condition.</span></span> <span data-ttu-id="799fd-233">ถ้าหมายเลขของเงื่อนไขเป็น 0 (ศูนย์) จะให้ผล <strong>อนันต์</strong></span><span class="sxs-lookup"><span data-stu-id="799fd-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="799fd-234">สูงสุด[args]</span><span class="sxs-lookup"><span data-stu-id="799fd-234">Max[args]</span></span></td>
<td><span data-ttu-id="799fd-235"><strong>ตัวดำเนินการ:</strong> ค่าสูงสุด[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="799fd-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="799fd-236">ต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="799fd-236">Min</span></span></td>
<td><span data-ttu-id="799fd-237">ก่อให้เกิดเงื่อนไขเล็กที่สุด</span><span class="sxs-lookup"><span data-stu-id="799fd-237">This produces the smallest condition.</span></span> <span data-ttu-id="799fd-238">ถ้าหมายเลขของเงื่อนไขเป็น 0 (ศูนย์) จะให้ผล <strong>อนันต์</strong></span><span class="sxs-lookup"><span data-stu-id="799fd-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="799fd-239">ต่ำสุด[args]</span><span class="sxs-lookup"><span data-stu-id="799fd-239">Min[args]</span></span></td>
<td><span data-ttu-id="799fd-240"><strong>ตัวดำเนินการ:</strong> ค่าต่ำสุด[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="799fd-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="799fd-241">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="799fd-241">Not</span></span></td>
<td><span data-ttu-id="799fd-242">ก่อให้เกิดตัวผกผันทางตรรกะของเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="799fd-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="799fd-243">ต้องมีเพียงหนึ่งเงื่อนไขที่ตรงทุกประการ</span><span class="sxs-lookup"><span data-stu-id="799fd-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="799fd-244">ไม่[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="799fd-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="799fd-245"><strong>ตัวดำเนินการ:</strong> ไม่ใช่ [x] &amp; ไม่ใช่ [y == 3]</span><span class="sxs-lookup"><span data-stu-id="799fd-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="799fd-246"><strong>สัญลักษณ์ Infix:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="799fd-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="799fd-247">ตัวอย่างในตารางถัดไปแสดงวิธีการเขียนสัญลักษณ์ Infix</span><span class="sxs-lookup"><span data-stu-id="799fd-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="799fd-248">Infix สัญลักษณ์</span><span class="sxs-lookup"><span data-stu-id="799fd-248">Infix notation</span></span>    | <span data-ttu-id="799fd-249">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="799fd-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="799fd-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="799fd-250">x + y + z</span></span>         | <span data-ttu-id="799fd-251">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="799fd-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="799fd-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="799fd-252">x \* y \* z</span></span>       | <span data-ttu-id="799fd-253">คูณ</span><span class="sxs-lookup"><span data-stu-id="799fd-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="799fd-254">x - y</span><span class="sxs-lookup"><span data-stu-id="799fd-254">x - y</span></span>             | <span data-ttu-id="799fd-255">การลบเลขฐานสองถูกแปลเหมือนกับการเพิ่มเลขฐานสองเมื่อมีวินาทีที่ปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="799fd-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="799fd-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="799fd-256">x ^ y ^ z</span></span>         | <span data-ttu-id="799fd-257">การยกกำลังที่มีทิศทางจากขวาไปซ้าย</span><span class="sxs-lookup"><span data-stu-id="799fd-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="799fd-258">!x</span><span class="sxs-lookup"><span data-stu-id="799fd-258">!x</span></span>                | <span data-ttu-id="799fd-259">ไม่ใช่บูลีน</span><span class="sxs-lookup"><span data-stu-id="799fd-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="799fd-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="799fd-260">x -: y</span></span>            | <span data-ttu-id="799fd-261">การส่อความบูลีน</span><span class="sxs-lookup"><span data-stu-id="799fd-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="799fd-262"> x</span><span class="sxs-lookup"><span data-stu-id="799fd-262">x</span></span> | <span data-ttu-id="799fd-263">y</span><span class="sxs-lookup"><span data-stu-id="799fd-263">y</span></span> | <span data-ttu-id="799fd-264">z</span><span class="sxs-lookup"><span data-stu-id="799fd-264">z</span></span>         | <span data-ttu-id="799fd-265">บูลีนหรือ</span><span class="sxs-lookup"><span data-stu-id="799fd-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="799fd-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="799fd-266">x & y & z</span></span>         | <span data-ttu-id="799fd-267">บูลีนและ</span><span class="sxs-lookup"><span data-stu-id="799fd-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="799fd-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="799fd-268">x == y == z</span></span>       | <span data-ttu-id="799fd-269">ความเท่าเทียม</span><span class="sxs-lookup"><span data-stu-id="799fd-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="799fd-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="799fd-270">x != y != z</span></span>       | <span data-ttu-id="799fd-271">ชัดเจน</span><span class="sxs-lookup"><span data-stu-id="799fd-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="799fd-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="799fd-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="799fd-273">น้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="799fd-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="799fd-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="799fd-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="799fd-275">มากกว่า</span><span class="sxs-lookup"><span data-stu-id="799fd-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="799fd-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="799fd-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="799fd-277">น้อยกว่าหรือเท่ากับ</span><span class="sxs-lookup"><span data-stu-id="799fd-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="799fd-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="799fd-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="799fd-279">มากกว่าหรือเท่ากับ</span><span class="sxs-lookup"><span data-stu-id="799fd-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="799fd-280">(x)</span><span class="sxs-lookup"><span data-stu-id="799fd-280">(x)</span></span>               | <span data-ttu-id="799fd-281">วงเล็บแทนที่ความสำคัญเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="799fd-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="799fd-282">เหตุใดข้อจำกัดนิพจน์ของฉันจึงถูกตรวจสอบไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="799fd-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="799fd-283">คุณไม่สามารถใช้คำสำคัญที่สำรองไว้เป็นชื่อโปรแกรมแก้ปัญหาแอททริบิวต์ ส่วนประกอบ หรือส่วนประกอบย่อยในแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="799fd-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="799fd-284">นี่คือรายการของคำสำคัญที่สำรองไว้ที่คุณไม่สามารถใช้:</span><span class="sxs-lookup"><span data-stu-id="799fd-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="799fd-285">เพดานเงิน</span><span class="sxs-lookup"><span data-stu-id="799fd-285">Ceiling</span></span>
-   <span data-ttu-id="799fd-286">องค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="799fd-286">Element</span></span>
-   <span data-ttu-id="799fd-287">เท่ากับ</span><span class="sxs-lookup"><span data-stu-id="799fd-287">Equal</span></span>
-   <span data-ttu-id="799fd-288">ขั้นต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="799fd-288">Floor</span></span>
-   <span data-ttu-id="799fd-289">ถ้า</span><span class="sxs-lookup"><span data-stu-id="799fd-289">If</span></span>
-   <span data-ttu-id="799fd-290">น้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="799fd-290">Less</span></span>
-   <span data-ttu-id="799fd-291">มากกว่า</span><span class="sxs-lookup"><span data-stu-id="799fd-291">Greater</span></span>
-   <span data-ttu-id="799fd-292">บ่งชี้</span><span class="sxs-lookup"><span data-stu-id="799fd-292">Implies</span></span>
-   <span data-ttu-id="799fd-293">ล็อก</span><span class="sxs-lookup"><span data-stu-id="799fd-293">Log</span></span>
-   <span data-ttu-id="799fd-294">สูงสุด</span><span class="sxs-lookup"><span data-stu-id="799fd-294">Max</span></span>
-   <span data-ttu-id="799fd-295">ต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="799fd-295">Min</span></span>
-   <span data-ttu-id="799fd-296">ลบ</span><span class="sxs-lookup"><span data-stu-id="799fd-296">Minus</span></span>
-   <span data-ttu-id="799fd-297">บวก</span><span class="sxs-lookup"><span data-stu-id="799fd-297">Plus</span></span>
-   <span data-ttu-id="799fd-298">กำลัง</span><span class="sxs-lookup"><span data-stu-id="799fd-298">Power</span></span>
-   <span data-ttu-id="799fd-299">เวลา</span><span class="sxs-lookup"><span data-stu-id="799fd-299">Times</span></span>
-   <span data-ttu-id="799fd-300">ช่อง</span><span class="sxs-lookup"><span data-stu-id="799fd-300">Slot</span></span>
-   <span data-ttu-id="799fd-301">รุ่น</span><span class="sxs-lookup"><span data-stu-id="799fd-301">Model</span></span>
-   <span data-ttu-id="799fd-302">การตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="799fd-302">Decision</span></span>
-   <span data-ttu-id="799fd-303">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="799fd-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="799fd-304">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="799fd-304">See also</span></span>
--------

<span data-ttu-id="799fd-305">[สร้างข้อจำกัดนิพจน์ (คู่มืองาน)(tasks/add-expression-constraint-product-configuration-model.md)</span><span class="sxs-lookup"><span data-stu-id="799fd-305">[Create an expression constraint (Task guide)(tasks/add-expression-constraint-product-configuration-model.md)</span></span>

[<span data-ttu-id="799fd-306">เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="799fd-306">Add a calculation to a product configuration model (Task guide)</span></span>](tasks/add-calculation-product-configuration-model.md)




