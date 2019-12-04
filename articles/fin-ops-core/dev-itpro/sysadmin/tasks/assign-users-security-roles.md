---
title: กำหนดบทบาทความปลอดภัยให้กับผู้ใช้
description: หากต้องการเข้าถึงแอพ Finance and Operations ต้องมีการมอบหมายบทบาทความปลอดภัยให้กับผู้ใช้ก่อน
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808007"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="57a7e-103">กำหนดบทบาทความปลอดภัยให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="57a7e-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57a7e-104">หากต้องการใช้งานฟังก์ชั่นที่มากกว่าความสามารถทั่วไป ต้องกำหนดบทบาทความปลอดภัยให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="57a7e-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="57a7e-105">กระบวนงานนี้อธิบายวิธีที่ผู้ดูแลระบบสามารถมอบหมายบทบาทให้กับผู้ใช้โดยอัตโนมัติตามข้อมูลทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="57a7e-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="57a7e-106">กำหนดผู้ใช้ให้กับบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="57a7e-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="57a7e-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="57a7e-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="57a7e-108">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="57a7e-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="57a7e-109">เลือกบทบาทที่คุณต้องการตั้งค่าคอนฟิกกฎ </span><span class="sxs-lookup"><span data-stu-id="57a7e-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="57a7e-110">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="57a7e-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="57a7e-111">คลิก **เพิ่มบทบาท** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="57a7e-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="57a7e-112">ในรายการ **เลือกการสอบถาม** ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="57a7e-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="57a7e-113">เลือกการสอบถามที่จะใช้สำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="57a7e-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="57a7e-114">ในรายการนี้ **ชื่อกฎการเป็นสมาชิก** ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="57a7e-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="57a7e-115">คลิก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="57a7e-115">Click **Edit query**.</span></span> <span data-ttu-id="57a7e-116">แก้ไขการสอบถาม เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="57a7e-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="57a7e-117">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="57a7e-117">Click **OK**.</span></span>
8. <span data-ttu-id="57a7e-118">คลิก **รันการกำหนดบทบาทอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="57a7e-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="57a7e-119">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการระบบ > ผู้ใช้ > ผู้ใช้** (ในแท็บเบราว์เซอร์แยกต่างหาก)</span><span class="sxs-lookup"><span data-stu-id="57a7e-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="57a7e-120">ตรวจทานบทบาทที่กำหนดให้กับผู้ใช้ต่างๆ เพื่อยืนยันว่าการสอบถามการกำหนดบทบาทถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="57a7e-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="57a7e-121">ปรับปรุงและรันใหม่ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="57a7e-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="57a7e-122">ชแยกผู้ใช้ออกจากการกำหนดบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="57a7e-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="57a7e-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="57a7e-123">Close the page.</span></span>
2. <span data-ttu-id="57a7e-124">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="57a7e-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="57a7e-125">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="57a7e-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="57a7e-126">เลือกบทบาท</span><span class="sxs-lookup"><span data-stu-id="57a7e-126">Select a role.</span></span> <span data-ttu-id="57a7e-127">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="57a7e-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="57a7e-128">ในเมนู **ผู้ใช้ที่กำหนดให้กับบทบาท** ให้เลือก **กำหนด / แยกผู้ใช้ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="57a7e-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="57a7e-129">ในรายการ **กำหนดผู้ใช้ให้กับหรือแยกผู้ใช้ออกจากบทบาท** ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="57a7e-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="57a7e-130">เลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="57a7e-130">Select a user.</span></span>  
6. <span data-ttu-id="57a7e-131">ใน **บานหน้าต่างการดำเนินการ** ให้เลือก **แยกออกจากบทบาท**</span><span class="sxs-lookup"><span data-stu-id="57a7e-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="57a7e-132">คลิก **แยกออกจากบทบาท** เพื่อแยกผู้ใช้ที่เลือกออกจากบทบาท</span><span class="sxs-lookup"><span data-stu-id="57a7e-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="57a7e-133">เพื่อลบการแยก ให้เลือกผู้ใช้ที่คุณต้องการลบการแยก แล้วคลิก **สถานะรีเซ็ต**</span><span class="sxs-lookup"><span data-stu-id="57a7e-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="57a7e-134">เมื่อคุณลบการแยกโดยการรีเซ็ตสถานะของผู้ใช้ บทบาทของผู้ใช้จะถูกมอบหมายโดยอัตโนมัติอีกครั้ง </span><span class="sxs-lookup"><span data-stu-id="57a7e-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="57a7e-135">อย่างไรก็ตาม ผู้ใช้จะไม่ถูกมอบหมายในทันทีให้กับบทบาท หรือถูกแยกจากบทบาทเมื่อคุณรีเซ็ตสถานะ </span><span class="sxs-lookup"><span data-stu-id="57a7e-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="57a7e-136">ผู้ใช้จะถูกมอบหมายให้กับบทบาทหรือถูกลบออกจากบทบาทในครั้งต่อไป อย่างใดอย่างหนึ่งแทน ซึ่งกฎสำหรับการมอบหมายบทบาทโดยอัตโนมัติจะถูกรัน</span><span class="sxs-lookup"><span data-stu-id="57a7e-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
