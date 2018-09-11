--- 
title: "กำหนดผู้ใช้ให้กับบทบาทความปลอดภัย"
description: "เพื่อเข้าถึง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ผู้ใช้ต้องถูกมอบหมายให้กับบทบาทความปลอดภัย"
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c08c9ee27bef3ec8c51df558766f55d3ea4ac48a
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="b4655-103">กำหนดผู้ใช้ให้กับบทบาทความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="b4655-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4655-104">เพื่อเข้าถึง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ผู้ใช้ต้องถูกมอบหมายให้กับบทบาทความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="b4655-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="b4655-105">กระบวนงานนี้อธิบายวิธีที่ผู้ดูแลระบบสามารถมอบหมายผู้ใช้ให้กับบทบาทโดยอัตโนมัติ ตามข้อมูลทางธุรกิจ </span><span class="sxs-lookup"><span data-stu-id="b4655-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="b4655-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="b4655-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="b4655-107">กำหนดผู้ใช้ให้กับบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b4655-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="b4655-108">ไปที่ การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท</span><span class="sxs-lookup"><span data-stu-id="b4655-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="b4655-109">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="b4655-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="b4655-110">เลือกบทบาทที่คุณต้องการตั้งค่าคอนฟิกกฎ </span><span class="sxs-lookup"><span data-stu-id="b4655-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="b4655-111">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="b4655-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="b4655-112">คลิกเพิ่มบทบาทเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b4655-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="b4655-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b4655-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b4655-114">เลือกการสอบถามที่จะใช้สำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="b4655-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="b4655-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4655-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b4655-116">(คลิกแก้ไขการสอบถาม)</span><span class="sxs-lookup"><span data-stu-id="b4655-116">Click Edit query.</span></span>
    * <span data-ttu-id="b4655-117">แก้ไขการสอบถาม เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b4655-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="b4655-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b4655-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="b4655-119">ชแยกผู้ใช้ออกจากการกำหนดบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b4655-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="b4655-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b4655-120">Close the page.</span></span>
2. <span data-ttu-id="b4655-121">ไปที่ การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท</span><span class="sxs-lookup"><span data-stu-id="b4655-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="b4655-122">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="b4655-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="b4655-123">เลือกบทบาท</span><span class="sxs-lookup"><span data-stu-id="b4655-123">Select a role.</span></span> <span data-ttu-id="b4655-124">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="b4655-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="b4655-125">คลิกกำหนด / แยกผู้ใช้ ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b4655-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="b4655-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4655-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b4655-127">เลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4655-127">Select a user.</span></span>  
6. <span data-ttu-id="b4655-128">คลิกแยกออกจากบทบาท</span><span class="sxs-lookup"><span data-stu-id="b4655-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="b4655-129">คลิกการแยกออกจากบทบาท เพื่อแยกผู้ใช้ที่เลือกออกจากบทบาท </span><span class="sxs-lookup"><span data-stu-id="b4655-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="b4655-130">เพื่อลบการแยก ให้เลือกผู้ใช้ที่คุณต้องการลบการแยก แล้วคลิกสถานะรีเซ็ต </span><span class="sxs-lookup"><span data-stu-id="b4655-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="b4655-131">เมื่อคุณลบการแยกโดยการรีเซ็ตสถานะของผู้ใช้ บทบาทของผู้ใช้จะถูกมอบหมายโดยอัตโนมัติอีกครั้ง </span><span class="sxs-lookup"><span data-stu-id="b4655-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="b4655-132">อย่างไรก็ตาม ผู้ใช้จะไม่ถูกมอบหมายในทันทีให้กับบทบาท หรือถูกแยกจากบทบาทเมื่อคุณรีเซ็ตสถานะ </span><span class="sxs-lookup"><span data-stu-id="b4655-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="b4655-133">ผู้ใช้จะถูกมอบหมายให้กับบทบาทหรือถูกลบออกจากบทบาทในครั้งต่อไป อย่างใดอย่างหนึ่งแทน ซึ่งกฎสำหรับการมอบหมายบทบาทโดยอัตโนมัติจะถูกรัน</span><span class="sxs-lookup"><span data-stu-id="b4655-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


