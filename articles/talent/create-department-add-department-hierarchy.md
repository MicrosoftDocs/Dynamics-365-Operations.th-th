---
title: "สร้างแผนกและเชื่อมโยงกับลำดับชั้นของแผนก"
description: "แผนกเป็นหน่วยปฏิบัติงานที่แสดงถึงประเภทหรือพื้นที่ทำงานขององค์กร แผนกจะรับผิดชอบพื้นที่เฉพาะขององค์กร เช่น การขาย การบัญชี หรือทรัพยากรบุคคล คุณสามารถใช้แผนกต่างๆเพื่อรายงานพื้นที่ทำงาน แผนกอาจมีความรับผิดชอบกำไรและขาดทุน"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: adf3dbf8b7ffa906c872a6b66d9cb43eb8e02805
ms.contentlocale: th-th
ms.lasthandoff: 06/29/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a><span data-ttu-id="45f44-106">สร้างแผนกและเชื่อมโยงกับลำดับชั้นของแผนก</span><span class="sxs-lookup"><span data-stu-id="45f44-106">Create a department and associate it with the department hierarchy</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="45f44-107">แผนกเป็นหน่วยปฏิบัติงานที่แสดงถึงประเภทหรือพื้นที่ทำงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="45f44-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="45f44-108">แผนกจะรับผิดชอบพื้นที่เฉพาะขององค์กร เช่น การขาย การบัญชี หรือทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45f44-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="45f44-109">คุณสามารถใช้แผนกต่างๆเพื่อรายงานพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="45f44-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="45f44-110">แผนกอาจมีความรับผิดชอบกำไรและขาดทุน</span><span class="sxs-lookup"><span data-stu-id="45f44-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="45f44-111">แผนกยังอาจรวมถึงกลุ่มของศูนย์ต้นทุนด้วย</span><span class="sxs-lookup"><span data-stu-id="45f44-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="45f44-112">ตำแหน่งสามารถถูกกำหนดไปยังแผนกต่าง ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="45f44-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="45f44-113">เมื่อต้องการสร้างแผนก คลิก **ทรัพยากรบุคคล** &gt; **แผนกต่างๆ** &gt; **แผนกต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="45f44-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="45f44-114">ตารางต่อไปนี้อธิบายถึงฟิลด์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="45f44-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="45f44-115">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="45f44-115">Field</span></span>               | <span data-ttu-id="45f44-116">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="45f44-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f44-117">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="45f44-117">Name</span></span>                | <span data-ttu-id="45f44-118">ป้อนชื่อสำหรับแผนก</span><span class="sxs-lookup"><span data-stu-id="45f44-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="45f44-119">หมายเลขแผนก</span><span class="sxs-lookup"><span data-stu-id="45f44-119">Department number</span></span>   | <span data-ttu-id="45f44-120">ค่าเริ่มต้นอาจถูกสร้างขึ้นโดยอัตโนมัติถ้ารหัสลำดับหมายเลขถูกกำหนดใน **หมายเลของค์กร** อ้างอิงจากหน้า **ลำดับหมายเลข** </span><span class="sxs-lookup"><span data-stu-id="45f44-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="45f44-121">ชื่อสำหรับค้นหา</span><span class="sxs-lookup"><span data-stu-id="45f44-121">Search name</span></span>         | <span data-ttu-id="45f44-122">ป้อนชื่อหรือชื่อย่อที่สามารถถูกใช้ในการค้นหาแผนก</span><span class="sxs-lookup"><span data-stu-id="45f44-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="45f44-123">บันทึก</span><span class="sxs-lookup"><span data-stu-id="45f44-123">Memo</span></span>                | <span data-ttu-id="45f44-124">ป้อนข้อมูลเพิ่มเติมใด ๆ ที่นี่</span><span class="sxs-lookup"><span data-stu-id="45f44-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45f44-125">ในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="45f44-125">In hierarchy</span></span>        | <span data-ttu-id="45f44-126">กล่องกาเครื่องหมายที่ถูกเลือกบ่งชี้ว่าแผนกนั้นถูกรวมอยู่ในลำดับชั้นของแผนก</span><span class="sxs-lookup"><span data-stu-id="45f44-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="45f44-127">สำหรับข้อมูลเกี่ยวกับวิธีการเพิ่มแผนกในลำดับชั้นของแผนก ดูข้อมูลในบทความนี้หลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="45f44-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="45f44-128">หมายเลข DUNS</span><span class="sxs-lookup"><span data-stu-id="45f44-128">DUNS number</span></span>         | <span data-ttu-id="45f44-129">DUNS หมายถึง ระบบหมายเลขข้อมูลสากล</span><span class="sxs-lookup"><span data-stu-id="45f44-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="45f44-130">นี่เป็นตัวเลขเก้าหลัก ที่ออกโดย Dun & Bradstreet</span><span class="sxs-lookup"><span data-stu-id="45f44-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="45f44-131">ผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="45f44-131">Manager</span></span>             | <span data-ttu-id="45f44-132">ป้อนลักษณะที่จัดการแผนก</span><span class="sxs-lookup"><span data-stu-id="45f44-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="45f44-133">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="45f44-133">Addresses</span></span>           | <span data-ttu-id="45f44-134">เพิ่มข้อมูลที่อยู่สำหรับแผนกนี้</span><span class="sxs-lookup"><span data-stu-id="45f44-134">Add the address information for the department.</span></span> <span data-ttu-id="45f44-135">ตัวอย่างเช่น เพิ่มที่อยู่ทางไปรษณีย์สำหรับอาคารที่แผนกนั้นตั้งอยู่</span><span class="sxs-lookup"><span data-stu-id="45f44-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="45f44-136">ข้อมูลการติดต่อ</span><span class="sxs-lookup"><span data-stu-id="45f44-136">Contact information</span></span> | <span data-ttu-id="45f44-137">เพิ่มข้อมูลผู้ติดต่อสำหรับแผนกนี้</span><span class="sxs-lookup"><span data-stu-id="45f44-137">Add contact information for the department.</span></span> <span data-ttu-id="45f44-138">ตัวอย่างเช่น เพิ่มหมายเลขโทรศัพท์สำหรับโต๊ะบริการในแผนก</span><span class="sxs-lookup"><span data-stu-id="45f44-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="45f44-139">การเพิ่มแผนกในลำดับชั้นของแผนก ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="45f44-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="45f44-140">คลิก **ทรัพยากรบุคคล** &gt; **แผนกต่างๆ** &gt; **ลำดับชั้นของแผนก**</span><span class="sxs-lookup"><span data-stu-id="45f44-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="45f44-141">คลิก **แก้ไข** แล้วเลือกองค์กรที่แผนกนั้นควรอยู่ภายใต้</span><span class="sxs-lookup"><span data-stu-id="45f44-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="45f44-142">คลิก **แทรก** แล้วเลือก **แผนก** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="45f44-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="45f44-143">ในรายการของแผนกต่างๆที่ปรากฏ เลือกแผนกเพื่อที่จะเพิ่มลงในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="45f44-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="45f44-144">บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="45f44-144">Save your changes.</span></span> <span data-ttu-id="45f44-145">คุณจะได้รับข้อความว่ารุ่นแบบร่างของลำดับชั้นถูกสร้างขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="45f44-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="45f44-146">เมื่อคุณพร้อม คลิก **เผยแพร่** ในโปรแกรมออกแบบลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="45f44-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="45f44-147">คุณสามารถป้อนวันที่มีผลบังคับใช้ที่บ่งชี้ว่าลำดับชั้นควรถูกเผยแพร่เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="45f44-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="45f44-148">ตัวอย่างเช่น การเพิ่มแผนกใหม่ที่จุดเริ่มต้นของปีปฏิทินถัดไป ตั้งค่าวันที่มีผลบังคับใช้เป็นวันที่ 1 มกราคมของปีปฏิทินใหม่</span><span class="sxs-lookup"><span data-stu-id="45f44-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="45f44-149">การเปลี่ยนแปลงลำดับชั้นจะมีผลในวันที่ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="45f44-149">The changes to the hierarchy will take effect on that date.</span></span>





