---
title: กำหนดบทบาทความปลอดภัยให้กับผู้ใช้
description: เพื่อเข้าถึงแอป Finance and Operations ผู้ใช้ต้องได้รับมอบหมายไปยังบทบาทความปลอดภัย
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f78c24e8c2ffe5418ce119e19b7c0193f01f64b8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679875"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="92d01-103">กำหนดบทบาทความปลอดภัยให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="92d01-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92d01-104">หากต้องการใช้งานฟังก์ชั่นที่มากกว่าความสามารถทั่วไปในแอป Finance and Operations ต้องกำหนดบทบาทความปลอดภัยให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="92d01-104">To use anything other than common capabilities in Finance and Operations apps, users must be assigned to security roles.</span></span> <span data-ttu-id="92d01-105">คุณสามารถกําหนดผู้ใช้ให้กับบทบาทโดยอัตโนมัติ ตามกฎและข้อมูลธุรกิจ ไม่รวมผู้ใช้จากการกำหนดบทบาทอัตโนมัติ หรือเพิ่มผู้ใช้ให้กับบทบาทด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="92d01-105">You can assign users to roles automatically, based on rules and business data, exclude users from automatic role assignment, or add users to roles manually.</span></span>

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="92d01-106">กำหนดผู้ใช้ให้กับบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="92d01-106">Automatically assign users to roles</span></span>
<span data-ttu-id="92d01-107">กระบวนงานนี้อธิบายวิธีที่ผู้ดูแลระบบสามารถมอบหมายบทบาทให้กับผู้ใช้โดยอัตโนมัติตามข้อมูลทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="92d01-107">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 
1. <span data-ttu-id="92d01-108">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="92d01-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="92d01-109">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="92d01-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="92d01-110">เลือกบทบาทที่คุณต้องการตั้งค่าคอนฟิกกฎ </span><span class="sxs-lookup"><span data-stu-id="92d01-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="92d01-111">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="92d01-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="92d01-112">เลือก **เพิ่มกฎ** เพื่อเปิดเมนูกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="92d01-112">Select **Add rule** to open the dialog menu.</span></span>
4. <span data-ttu-id="92d01-113">ในรายการ **เลือกการสอบถาม** ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="92d01-113">In the **Select a query** list, find and select the desired record.</span></span> <span data-ttu-id="92d01-114">เลือกการสอบถามที่จะใช้สำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="92d01-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="92d01-115">ในรายการนี้ **ชื่อกฎการเป็นสมาชิก** ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="92d01-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="92d01-116">เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92d01-116">Select **Edit query**.</span></span> <span data-ttu-id="92d01-117">แก้ไขการสอบถาม เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="92d01-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="92d01-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="92d01-118">Select **OK**.</span></span>
8. <span data-ttu-id="92d01-119">เลือก **เรียกใช้การกำหนดบทบาทอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="92d01-119">Select **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="92d01-120">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการระบบ > ผู้ใช้ > ผู้ใช้** (ในแท็บเบราว์เซอร์แยกต่างหาก)</span><span class="sxs-lookup"><span data-stu-id="92d01-120">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="92d01-121">ตรวจทานบทบาทที่กำหนดให้กับผู้ใช้ต่างๆ เพื่อยืนยันว่าการสอบถามการกำหนดบทบาทถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="92d01-121">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="92d01-122">ปรับปรุงและรันใหม่ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="92d01-122">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="92d01-123">ชแยกผู้ใช้ออกจากการกำหนดบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="92d01-123">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="92d01-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="92d01-124">Close the page.</span></span>
2. <span data-ttu-id="92d01-125">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="92d01-125">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="92d01-126">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="92d01-126">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="92d01-127">เลือกบทบาท</span><span class="sxs-lookup"><span data-stu-id="92d01-127">Select a role.</span></span> <span data-ttu-id="92d01-128">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="92d01-128">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="92d01-129">ในเมนู **ผู้ใช้ที่กำหนดให้กับบทบาท** ให้เลือก **กำหนด / แยกผู้ใช้ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="92d01-129">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="92d01-130">ในรายการ **กำหนดผู้ใช้ให้กับหรือแยกผู้ใช้ออกจากบทบาท** ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="92d01-130">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="92d01-131">เลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="92d01-131">Select a user.</span></span>  
6. <span data-ttu-id="92d01-132">ใน **บานหน้าต่างการดำเนินการ** ให้เลือก **แยกออกจากบทบาท**</span><span class="sxs-lookup"><span data-stu-id="92d01-132">On the **Action pane**, select **Exclude from role**.</span></span>
7. <span data-ttu-id="92d01-133">เลือก **แยกออกจากบทบาท** เพื่อแยกผู้ใช้ที่เลือกออกจากบทบาท</span><span class="sxs-lookup"><span data-stu-id="92d01-133">Select **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="92d01-134">เพื่อลบการแยก ให้เลือกผู้ใช้ที่คุณต้องการลบการแยก แล้วคลิก **สถานะรีเซ็ต**</span><span class="sxs-lookup"><span data-stu-id="92d01-134">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="92d01-135">เมื่อคุณลบการแยกโดยการรีเซ็ตสถานะของผู้ใช้ บทบาทของผู้ใช้จะถูกมอบหมายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="92d01-135">When you remove an exclusion by resetting the user's status, the user's role is assigned automatically.</span></span> <span data-ttu-id="92d01-136">อย่างไรก็ตาม ผู้ใช้จะไม่ถูกมอบหมายในทันทีให้กับบทบาท หรือถูกแยกจากบทบาทเมื่อคุณรีเซ็ตสถานะ </span><span class="sxs-lookup"><span data-stu-id="92d01-136">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="92d01-137">ผู้ใช้จะถูกมอบหมายให้กับบทบาทหรือถูกลบออกจากบทบาทในครั้งต่อไป อย่างใดอย่างหนึ่งแทน ซึ่งกฎสำหรับการมอบหมายบทบาทโดยอัตโนมัติจะถูกรัน</span><span class="sxs-lookup"><span data-stu-id="92d01-137">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

## <a name="manually-assign-users-to-roles"></a><span data-ttu-id="92d01-138">กำหนดบทบาทให้กับผู้ใช้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="92d01-138">Manually assign users to roles</span></span>
<span data-ttu-id="92d01-139">ผู้ใช้ที่ถูกกําหนดให้กับบทบาทความปลอดภัยด้วยตนเองต้องถูกเอาออกโดยผู้ดูแลระบบด้วยตนเองด้วย</span><span class="sxs-lookup"><span data-stu-id="92d01-139">Users who are manually assigned to security roles must also be manually removed by the administrator.</span></span> <span data-ttu-id="92d01-140">ผู้ใช้เหล่านี้จะไม่ถูกเอาออกจากบทบาทตามกฎสําหรับการกําหนดบทบาทอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="92d01-140">These users are not removed from roles by rules for automatic role assignment.</span></span>

1. <span data-ttu-id="92d01-141">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="92d01-141">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="92d01-142">ในแผนภูมิ เลือกบทบาท ในเมนู **ผู้ใช้ที่กำหนดให้กับบทบาท** ให้เลือก **กำหนด / แยกผู้ใช้ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="92d01-142">In the tree, select a role, and in the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
4. <span data-ttu-id="92d01-143">ใน **กําหนดผู้ใช้ให้ หรือแยกผู้ใช้ออกจากบทบาท** ผู่ใช้ที่ยังไม่ถูกกำหนดบทบาทจะถูกแสดงด้วย **โหมดการกำหนด** ตั้งค่าเป็น **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="92d01-143">In the **Assign users to or exclude users from role**, users that have not been assigned the role are listed with the **Assignment mode** set to **None**.</span></span> <span data-ttu-id="92d01-144">เลือกผู้ใช้หนึ่งคนขึ้นไปที่ควรกำหนดบทบาทให้</span><span class="sxs-lookup"><span data-stu-id="92d01-144">Select one or more users that should be assigned the role.</span></span>
5. <span data-ttu-id="92d01-145">ใน **บานหน้าต่างการดำเนินการ** ให้เลือก **กำหนดให้บทบาท**</span><span class="sxs-lookup"><span data-stu-id="92d01-145">On the **Action pane**, select **Assign to role**.</span></span> <span data-ttu-id="92d01-146">**โหมดการกําหนด** ถูกปรับปรุงเป็น **ด้วยตนเอง** และผู้ใช้มีบทบาทใหม่ที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="92d01-146">The **Assignment mode** is updated to **Manual** and the users now have a new role assigned.</span></span>
