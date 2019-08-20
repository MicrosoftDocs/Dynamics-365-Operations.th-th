---
title: กำหนดผู้ใช้ให้กับบทบาทความปลอดภัย
description: เพื่อเข้าถึง Microsoft Dynamics 365 for Finance and Operations Enterprise edition ผู้ใช้ต้องได้รับมอบหมายไปยัง Security role
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851370"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="54b46-103">กำหนดผู้ใช้ให้กับบทบาทความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="54b46-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54b46-104">เพื่อเข้าถึง Microsoft Dynamics 365 for Finance and Operations Enterprise edition ผู้ใช้ต้องได้รับมอบหมายไปยัง Security role</span><span class="sxs-lookup"><span data-stu-id="54b46-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="54b46-105">กระบวนงานนี้อธิบายวิธีที่ผู้ดูแลระบบสามารถมอบหมายผู้ใช้ให้กับบทบาทโดยอัตโนมัติ ตามข้อมูลทางธุรกิจ </span><span class="sxs-lookup"><span data-stu-id="54b46-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="54b46-106">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="54b46-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="54b46-107">กำหนดผู้ใช้ให้กับบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="54b46-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="54b46-108">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="54b46-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="54b46-109">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="54b46-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="54b46-110">เลือกบทบาทที่คุณต้องการตั้งค่าคอนฟิกกฎ </span><span class="sxs-lookup"><span data-stu-id="54b46-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="54b46-111">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="54b46-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="54b46-112">คลิก **เพิ่มบทบาท** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="54b46-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="54b46-113">ในรายการ **เลือกการสอบถาม** ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54b46-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="54b46-114">เลือกการสอบถามที่จะใช้สำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="54b46-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="54b46-115">ในรายการนี้ **ชื่อกฎการเป็นสมาชิก** ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="54b46-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="54b46-116">คลิก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54b46-116">Click **Edit query**.</span></span> <span data-ttu-id="54b46-117">แก้ไขการสอบถาม เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="54b46-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="54b46-118">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="54b46-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="54b46-119">ชแยกผู้ใช้ออกจากการกำหนดบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="54b46-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="54b46-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54b46-120">Close the page.</span></span>
2. <span data-ttu-id="54b46-121">ไปที่ **บานหน้าต่างนำทาง > โมดูล >การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท**</span><span class="sxs-lookup"><span data-stu-id="54b46-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="54b46-122">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="54b46-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="54b46-123">เลือกบทบาท</span><span class="sxs-lookup"><span data-stu-id="54b46-123">Select a role.</span></span> <span data-ttu-id="54b46-124">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="54b46-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="54b46-125">ในเมนู **ผู้ใช้ที่กำหนดให้กับบทบาท** ให้เลือก **กำหนด / แยกผู้ใช้ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="54b46-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="54b46-126">ในรายการ **กำหนดผู้ใช้ให้กับหรือแยกผู้ใช้ออกจากบทบาท** ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="54b46-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="54b46-127">เลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="54b46-127">Select a user.</span></span>  
6. <span data-ttu-id="54b46-128">ใน **บานหน้าต่างการดำเนินการ** ให้เลือก **แยกออกจากบทบาท**</span><span class="sxs-lookup"><span data-stu-id="54b46-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="54b46-129">คลิก **แยกออกจากบทบาท** เพื่อแยกผู้ใช้ที่เลือกออกจากบทบาท</span><span class="sxs-lookup"><span data-stu-id="54b46-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="54b46-130">เพื่อลบการแยก ให้เลือกผู้ใช้ที่คุณต้องการลบการแยก แล้วคลิก **สถานะรีเซ็ต**</span><span class="sxs-lookup"><span data-stu-id="54b46-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="54b46-131">เมื่อคุณลบการแยกโดยการรีเซ็ตสถานะของผู้ใช้ บทบาทของผู้ใช้จะถูกมอบหมายโดยอัตโนมัติอีกครั้ง </span><span class="sxs-lookup"><span data-stu-id="54b46-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="54b46-132">อย่างไรก็ตาม ผู้ใช้จะไม่ถูกมอบหมายในทันทีให้กับบทบาท หรือถูกแยกจากบทบาทเมื่อคุณรีเซ็ตสถานะ </span><span class="sxs-lookup"><span data-stu-id="54b46-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="54b46-133">ผู้ใช้จะถูกมอบหมายให้กับบทบาทหรือถูกลบออกจากบทบาทในครั้งต่อไป อย่างใดอย่างหนึ่งแทน ซึ่งกฎสำหรับการมอบหมายบทบาทโดยอัตโนมัติจะถูกรัน</span><span class="sxs-lookup"><span data-stu-id="54b46-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
