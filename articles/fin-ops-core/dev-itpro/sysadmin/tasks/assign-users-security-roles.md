---
title: กำหนดบทบาทความปลอดภัยให้กับผู้ใช้
description: หากต้องการเข้าถึงแอพ Finance and Operations ต้องมีการมอบหมายบทบาทความปลอดภัยให้กับผู้ใช้ก่อน
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
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
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180978"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="b6b2c-103">กำหนดบทบาทความปลอดภัยให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b6b2c-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6b2c-104">หากต้องการใช้งานฟังก์ชั่นที่มากกว่าความสามารถทั่วไป ต้องกำหนดบทบาทความปลอดภัยให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b6b2c-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="b6b2c-105">กระบวนงานนี้อธิบายวิธีที่ผู้ดูแลระบบสามารถมอบหมายบทบาทให้กับผู้ใช้โดยอัตโนมัติตามข้อมูลทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="b6b2c-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="b6b2c-106">กำหนดผู้ใช้ให้กับบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b6b2c-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="b6b2c-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="b6b2c-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="b6b2c-108">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="b6b2c-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="b6b2c-109">เลือกบทบาทที่คุณต้องการตั้งค่าคอนฟิกกฎ </span><span class="sxs-lookup"><span data-stu-id="b6b2c-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="b6b2c-110">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="b6b2c-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="b6b2c-111">คลิก **เพิ่มบทบาท** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b6b2c-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="b6b2c-112">ในรายการ **เลือกการสอบถาม** ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b6b2c-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="b6b2c-113">เลือกการสอบถามที่จะใช้สำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="b6b2c-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="b6b2c-114">ในรายการนี้ **ชื่อกฎการเป็นสมาชิก** ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b6b2c-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b6b2c-115">คลิก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="b6b2c-115">Click **Edit query**.</span></span> <span data-ttu-id="b6b2c-116">แก้ไขการสอบถาม เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b6b2c-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="b6b2c-117">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b6b2c-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="b6b2c-118">ชแยกผู้ใช้ออกจากการกำหนดบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b6b2c-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="b6b2c-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b6b2c-119">Close the page.</span></span>
2. <span data-ttu-id="b6b2c-120">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="b6b2c-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="b6b2c-121">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="b6b2c-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="b6b2c-122">เลือกบทบาท</span><span class="sxs-lookup"><span data-stu-id="b6b2c-122">Select a role.</span></span> <span data-ttu-id="b6b2c-123">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="b6b2c-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="b6b2c-124">ในเมนู **ผู้ใช้ที่กำหนดให้กับบทบาท** ให้เลือก **กำหนด / แยกผู้ใช้ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="b6b2c-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="b6b2c-125">ในรายการ **กำหนดผู้ใช้ให้กับหรือแยกผู้ใช้ออกจากบทบาท** ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b6b2c-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="b6b2c-126">เลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b6b2c-126">Select a user.</span></span>  
6. <span data-ttu-id="b6b2c-127">ใน **บานหน้าต่างการดำเนินการ** ให้เลือก **แยกออกจากบทบาท**</span><span class="sxs-lookup"><span data-stu-id="b6b2c-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="b6b2c-128">คลิก **แยกออกจากบทบาท** เพื่อแยกผู้ใช้ที่เลือกออกจากบทบาท</span><span class="sxs-lookup"><span data-stu-id="b6b2c-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="b6b2c-129">เพื่อลบการแยก ให้เลือกผู้ใช้ที่คุณต้องการลบการแยก แล้วคลิก **สถานะรีเซ็ต**</span><span class="sxs-lookup"><span data-stu-id="b6b2c-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="b6b2c-130">เมื่อคุณลบการแยกโดยการรีเซ็ตสถานะของผู้ใช้ บทบาทของผู้ใช้จะถูกมอบหมายโดยอัตโนมัติอีกครั้ง </span><span class="sxs-lookup"><span data-stu-id="b6b2c-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="b6b2c-131">อย่างไรก็ตาม ผู้ใช้จะไม่ถูกมอบหมายในทันทีให้กับบทบาท หรือถูกแยกจากบทบาทเมื่อคุณรีเซ็ตสถานะ </span><span class="sxs-lookup"><span data-stu-id="b6b2c-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="b6b2c-132">ผู้ใช้จะถูกมอบหมายให้กับบทบาทหรือถูกลบออกจากบทบาทในครั้งต่อไป อย่างใดอย่างหนึ่งแทน ซึ่งกฎสำหรับการมอบหมายบทบาทโดยอัตโนมัติจะถูกรัน</span><span class="sxs-lookup"><span data-stu-id="b6b2c-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
