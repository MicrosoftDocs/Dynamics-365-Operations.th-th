---
title: ข้อจำกัดตารางการที่กำหนดโดยระบบและโดยผู้ใช้
description: 'บทความนี้อธิบายถึงตารางสองชนิดของข้อจำกัดตารางที่ระบบกำหนดสำหรับส่วนประกอบในแบบจำลองการจัดโครงแบบผลิตภัณฑ์: ข้อจำกัดตารางที่ผู้ใช้และระบบกำหนด ข้อจำกัดของตารางแสดงเมทริกซ์ของชุดแอททริบิวต์ที่สามารถใช้ได้ ซึ่งแต่ละแถวกำหนดชุดของค่าแอททริบิวต์ที่เป็นไปได้'
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fac49cde1a6098b99e6373bf9221d3357a053a2
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814525"
---
# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="a0a34-104">ข้อจำกัดตารางการที่กำหนดโดยระบบและโดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a0a34-104">System-defined and user-defined table constraints</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0a34-105">บทความนี้อธิบายถึงตารางสองชนิดของข้อจำกัดตารางที่ระบบกำหนดสำหรับส่วนประกอบในแบบจำลองการจัดโครงแบบผลิตภัณฑ์: ข้อจำกัดตารางที่ผู้ใช้และระบบกำหนด</span><span class="sxs-lookup"><span data-stu-id="a0a34-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="a0a34-106">ข้อจำกัดของตารางแสดงเมทริกซ์ของชุดแอททริบิวต์ที่สามารถใช้ได้ ซึ่งแต่ละแถวกำหนดชุดของค่าแอททริบิวต์ที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="a0a34-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="a0a34-107">ข้อจำกัดของตารางแสดงเมทริกซ์ของการรวมแอททริบิวต์ที่จะใช้ได้สำหรับส่วนประกอบในแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a0a34-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="a0a34-108">แต่ละแถวในตารางกำหนดชุดของค่าแอททริบิวต์ที่เป็นไปได้ชุดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a0a34-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="a0a34-109">คุณสามารถประกาศข้อจำกัดสองชนิดในแบบจำลองการจัดโครงแบบผลิตภัณฑ์:</span><span class="sxs-lookup"><span data-stu-id="a0a34-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="a0a34-110">**ข้อจำกัดนิพจน์**– สร้างนิพจน์ที่กำหนดความสัมพันธ์ระหว่างแอททริบิวต์เพื่อรับประกันว่า สามารถเลือกค่าที่เข้ากันได้เท่านั้นในระหว่างการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a0a34-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="a0a34-111">**ข้อจำกัดของตาราง**– สร้างตารางที่กำหนดชุดทั้งหมดที่ได้รับอนุญาตสำหรับชุดแอตทริบิวต์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a0a34-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="a0a34-112">ข้อจำกัดตารางสองชนิดพร้อมใช้งาน: ข้อจำกัดตารางที่ผู้ใช้กำหนดและข้อจำกัดตารางที่ระบบกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="a0a34-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="a0a34-113">บทความนี้อธิบายถึงข้อจำกัดตารางที่ผู้ใช้กำหนดเและข้อจำกัดตารางที่ระบบกำหนดสำหรับส่วนประกอบในแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a0a34-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="a0a34-114">ข้อจำกัดตารางที่ผู้ใช้กำหนด</span><span class="sxs-lookup"><span data-stu-id="a0a34-114">User-defined table constraints</span></span>
<span data-ttu-id="a0a34-115">ข้อจำกัดตารางที่ผู้ใช้กำหนดเป็นชนิดของเมทริกซ์ที่ใช้เพื่ออธิบายชุดของค่าแอททริบิวต์ที่กำหนดโดยชนิดแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="a0a34-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="a0a34-116">ตัวอย่างเช่น ถ้าคุณจัดทำลำโพง คุณสามารถรวมคอลัมน์สำหรับเสร็จสิ้น cabinet และ grill หน้าในข้อจำกัดตารางที่ผู้ใช้กำหนด</span><span class="sxs-lookup"><span data-stu-id="a0a34-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="a0a34-117">ชนิดแอททริบิวต์สำหรับเสร็จสิ้น cabinet มีสี่ค่า และชนิดแอททริบิวต์สำหรับ grill หน้ามีสามค่า</span><span class="sxs-lookup"><span data-stu-id="a0a34-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="a0a34-118">ดังนั้น ถ้าไม่ได้ใช้ข้อจำกัด จะมี 4 × 3 = 12 ชุดที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="a0a34-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="a0a34-119">อย่างไรก็ตาม ในตัวอย่างนี้ ได้เฉพาะหกชุด ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a0a34-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="a0a34-120">ข้อมูลนี้จะปรากฏในแท็บ **ชุดที่ได้รับอนุญาต** บนหน้า **แก้ไขข้อจำกัดตาราง**</span><span class="sxs-lookup"><span data-stu-id="a0a34-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="a0a34-121">เสร็จสิ้น cabinet</span><span class="sxs-lookup"><span data-stu-id="a0a34-121">Cabinet finish</span></span> | <span data-ttu-id="a0a34-122">Grill หน้า</span><span class="sxs-lookup"><span data-stu-id="a0a34-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="a0a34-123">สีดำ</span><span class="sxs-lookup"><span data-stu-id="a0a34-123">Black</span></span>          | <span data-ttu-id="a0a34-124">สีดำ</span><span class="sxs-lookup"><span data-stu-id="a0a34-124">Black</span></span>       |
| <span data-ttu-id="a0a34-125">สีดำ</span><span class="sxs-lookup"><span data-stu-id="a0a34-125">Black</span></span>          | <span data-ttu-id="a0a34-126">โลหะ</span><span class="sxs-lookup"><span data-stu-id="a0a34-126">Metal</span></span>       |
| <span data-ttu-id="a0a34-127">ไม้โอ้ค</span><span class="sxs-lookup"><span data-stu-id="a0a34-127">Oak</span></span>            | <span data-ttu-id="a0a34-128">สีดำ</span><span class="sxs-lookup"><span data-stu-id="a0a34-128">Black</span></span>       |
| <span data-ttu-id="a0a34-129">โรสวูด</span><span class="sxs-lookup"><span data-stu-id="a0a34-129">Rosewood</span></span>       | <span data-ttu-id="a0a34-130">สีขาว</span><span class="sxs-lookup"><span data-stu-id="a0a34-130">White</span></span>       |
| <span data-ttu-id="a0a34-131">สีขาว</span><span class="sxs-lookup"><span data-stu-id="a0a34-131">White</span></span>          | <span data-ttu-id="a0a34-132">สีดำ</span><span class="sxs-lookup"><span data-stu-id="a0a34-132">Black</span></span>       |
| <span data-ttu-id="a0a34-133">สีขาว</span><span class="sxs-lookup"><span data-stu-id="a0a34-133">White</span></span>          | <span data-ttu-id="a0a34-134">สีขาว</span><span class="sxs-lookup"><span data-stu-id="a0a34-134">White</span></span>       |

<span data-ttu-id="a0a34-135">ข้อจำกัดตารางที่ผู้ใช้กำหนดจะถูกกำหนดโดยข้อมูลป้อนเข้าจากตารางแบบคงที่ี่ที่ทำงานในลักษณะเดียวกับข้อจำกัดนิพจน์</span><span class="sxs-lookup"><span data-stu-id="a0a34-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="a0a34-136">เมื่อคุณใช้ข้อจำกัดตารางที่ผู้ใช้กำหนด ข้อดีคือ ตารางมักสามารถสร้าง เข้าใจ และรักษาไว้ได้ง่ายกว่าข้อจำกัดนิพจน์ที่ยาว</span><span class="sxs-lookup"><span data-stu-id="a0a34-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="a0a34-137">ข้อจำกัดตารางที่ระบบกำหนด</span><span class="sxs-lookup"><span data-stu-id="a0a34-137">System-defined table constraints</span></span>
<span data-ttu-id="a0a34-138">ข้อจำกัดตารางที่ระบบกำหนดสร้างแม็ปไดนามิกระหว่างชนิดแอททริบิวต์และฟิลด์ในตาราง</span><span class="sxs-lookup"><span data-stu-id="a0a34-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="a0a34-139">เมื่อข้อจำกัดตารางที่ระบบกำหนดถูกรวมอยู่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ การแม็ปรับรองว่า ข้อมูลในตารางจะแสดงแทนค่าของชนิดแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="a0a34-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="a0a34-140">ผลลัพธ์มีข้อจำกัดแบบไดนามิก เนื่องจากสามารถปรับเปลี่ยนเนื้อหาของตาราง (ตัวอย่างเช่น ตามโมดูลอื่น)</span><span class="sxs-lookup"><span data-stu-id="a0a34-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="a0a34-141">เมื่อคุณสร้างข้อจำกัดตารางที่กำหนดโดยระบบ คุณเลือกตาราง หรือกำหนดแบบสอบถามที่ใช้ และจากนั้นเชื่อมโยงชนิดแอททริบิวต์ไปยังฟิลด์ในตารางที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a0a34-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="a0a34-142">ชนิดของฟิลด์ต้องตรงกับชนิดของชนิดแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="a0a34-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="a0a34-143">ก่อนข้อจำกัดตารางสามารถมีผลกับแบบจำลองการจัดโครงแบบผลิตภัณฑ์ ข้อจำกัดตารางต้องรวมอยู่ในข้อจำกัดของส่วนประกอบของแบบจำลองหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a0a34-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="a0a34-144">ขั้นตอนคือเพื่อสร้างข้อจำกัดใหม่ เลือกชนิดของข้อจำกัดตาราง และจากนั้นเลือกคำนิยามข้อจำกัดตารางที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="a0a34-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="a0a34-145">ในตอนท้าย ฟิลด์ทั้งหมดในตารางข้อจำกัดต้องแม็ปกับแอททริบิวต์ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a0a34-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a0a34-146">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a0a34-146">Additional resources</span></span>
--------

[<span data-ttu-id="a0a34-147">ภาพรวมแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a0a34-147">Product configuration models overview</span></span>](product-configuration-models.md)



