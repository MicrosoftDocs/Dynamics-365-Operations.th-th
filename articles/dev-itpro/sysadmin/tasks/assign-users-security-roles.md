---
title: กำหนดผู้ใช้ให้กับบทบาทความปลอดภัย
description: เพื่อเข้าถึง Microsoft Dynamics 365 for Finance and Operations Enterprise edition ผู้ใช้ต้องได้รับมอบหมายไปยัง Security role
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556720"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="b884a-103">กำหนดผู้ใช้ให้กับบทบาทความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="b884a-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b884a-104">เพื่อเข้าถึง Microsoft Dynamics 365 for Finance and Operations Enterprise edition ผู้ใช้ต้องได้รับมอบหมายไปยัง Security role</span><span class="sxs-lookup"><span data-stu-id="b884a-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="b884a-105">กระบวนงานนี้อธิบายวิธีที่ผู้ดูแลระบบสามารถมอบหมายผู้ใช้ให้กับบทบาทโดยอัตโนมัติ ตามข้อมูลทางธุรกิจ </span><span class="sxs-lookup"><span data-stu-id="b884a-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="b884a-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="b884a-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="b884a-107">กำหนดผู้ใช้ให้กับบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b884a-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="b884a-108">ไปที่ การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท</span><span class="sxs-lookup"><span data-stu-id="b884a-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="b884a-109">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="b884a-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="b884a-110">เลือกบทบาทที่คุณต้องการตั้งค่าคอนฟิกกฎ </span><span class="sxs-lookup"><span data-stu-id="b884a-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="b884a-111">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="b884a-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="b884a-112">คลิกเพิ่มบทบาทเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b884a-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="b884a-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b884a-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b884a-114">เลือกการสอบถามที่จะใช้สำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="b884a-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="b884a-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b884a-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b884a-116">(คลิกแก้ไขการสอบถาม)</span><span class="sxs-lookup"><span data-stu-id="b884a-116">Click Edit query.</span></span>
    * <span data-ttu-id="b884a-117">แก้ไขการสอบถาม เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b884a-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="b884a-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b884a-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="b884a-119">ชแยกผู้ใช้ออกจากการกำหนดบทบาทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b884a-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="b884a-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b884a-120">Close the page.</span></span>
2. <span data-ttu-id="b884a-121">ไปที่ การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท</span><span class="sxs-lookup"><span data-stu-id="b884a-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="b884a-122">ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'</span><span class="sxs-lookup"><span data-stu-id="b884a-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="b884a-123">เลือกบทบาท</span><span class="sxs-lookup"><span data-stu-id="b884a-123">Select a role.</span></span> <span data-ttu-id="b884a-124">ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="b884a-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="b884a-125">คลิกกำหนด / แยกผู้ใช้ ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b884a-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="b884a-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b884a-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b884a-127">เลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b884a-127">Select a user.</span></span>  
6. <span data-ttu-id="b884a-128">คลิกแยกออกจากบทบาท</span><span class="sxs-lookup"><span data-stu-id="b884a-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="b884a-129">คลิกการแยกออกจากบทบาท เพื่อแยกผู้ใช้ที่เลือกออกจากบทบาท </span><span class="sxs-lookup"><span data-stu-id="b884a-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="b884a-130">เพื่อลบการแยก ให้เลือกผู้ใช้ที่คุณต้องการลบการแยก แล้วคลิกสถานะรีเซ็ต </span><span class="sxs-lookup"><span data-stu-id="b884a-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="b884a-131">เมื่อคุณลบการแยกโดยการรีเซ็ตสถานะของผู้ใช้ บทบาทของผู้ใช้จะถูกมอบหมายโดยอัตโนมัติอีกครั้ง </span><span class="sxs-lookup"><span data-stu-id="b884a-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="b884a-132">อย่างไรก็ตาม ผู้ใช้จะไม่ถูกมอบหมายในทันทีให้กับบทบาท หรือถูกแยกจากบทบาทเมื่อคุณรีเซ็ตสถานะ </span><span class="sxs-lookup"><span data-stu-id="b884a-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="b884a-133">ผู้ใช้จะถูกมอบหมายให้กับบทบาทหรือถูกลบออกจากบทบาทในครั้งต่อไป อย่างใดอย่างหนึ่งแทน ซึ่งกฎสำหรับการมอบหมายบทบาทโดยอัตโนมัติจะถูกรัน</span><span class="sxs-lookup"><span data-stu-id="b884a-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

