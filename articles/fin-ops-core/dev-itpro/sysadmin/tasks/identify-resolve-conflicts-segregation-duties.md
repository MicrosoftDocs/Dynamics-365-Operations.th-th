---
title: ระบุและแก้ไขความขัดแย้งในการแบ่งแยกหน้าที่
description: หัวข้อนี้อธิบายวิธีการระบุและแก้ไขความขัดแย้งในการแบ่งแยกหน้าที่
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deff97c7728db91089d3ea834d15de738da500fa
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826379"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="73792-103">ระบุและแก้ไขความขัดแย้งในการแบ่งแยกหน้าที่</span><span class="sxs-lookup"><span data-stu-id="73792-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73792-104">หัวข้อนี้อธิบายวิธีการระบุและแก้ไขความขัดแย้งในการแบ่งแยกหน้าที่</span><span class="sxs-lookup"><span data-stu-id="73792-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="73792-105">คุณสามารถตั้งค่ากฎเพื่อหน้าที่ที่ต้องดำเนินการโดยผู้ใช้ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="73792-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="73792-106">แนวคิดนี้มีชื่อว่าการแบ่งแยกหน้าที่ </span><span class="sxs-lookup"><span data-stu-id="73792-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="73792-107">เมื่อมีการกำหนดของบทบาทความปลอดภัยหรือการกำหนดบทบาทของผู้ใช้ที่ละเมิดกฎ ความขัดแย้งจะถูกบันทึกไว้ </span><span class="sxs-lookup"><span data-stu-id="73792-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="73792-108">ต้องมีแก้ไขความขัดแย้งทั้งหมดโดยผู้ดูแลระบบ </span><span class="sxs-lookup"><span data-stu-id="73792-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="73792-109">ปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อระบุ และแก้ไขข้อขัดแย้ง </span><span class="sxs-lookup"><span data-stu-id="73792-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="73792-110">หลังจากที่เพิ่มกฎแล้ว ให้ตรวจสอบว่าบทบาทที่มีอยู่ทั้งหมดว่าสอดคล้องกับบทบาท</span><span class="sxs-lookup"><span data-stu-id="73792-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="73792-111">ตรวจสอบว่าบทบาทและหน้าที่ที่มีอยู่เป็นไปตามกฎใหม่ของการแบ่งแยกหน้าที่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="73792-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="73792-112">ไปที่ **การดูแลระบบ** > **ความปลอดภัย** > **การแบ่งแยกหน้าที่** > **กฎการแบ่งแยกหน้าที่**</span><span class="sxs-lookup"><span data-stu-id="73792-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="73792-113">เลือก **ตรวจสอบความถูกต้องของหน้าที่และบทบาท**</span><span class="sxs-lookup"><span data-stu-id="73792-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="73792-114">ถ้าบทบาทใดๆ ละเมิดกฎ ข้อความจะปรากฏขึ้นซึ่งจะประกอบด้วยชื่อของกฎ กฎ และชื่อของการแบ่งแยกหน้าที่ที่ขัดแย้งกัน</span><span class="sxs-lookup"><span data-stu-id="73792-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="73792-115">ต้องแก้ไขบทบาทที่ขัดแย้งกัน โดยใช้ **การตั้งค่าคอนฟิกความปลอดภัย** และต้องไม่รวมหน้าที่ที่ขัดแย้งกัน</span><span class="sxs-lookup"><span data-stu-id="73792-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="73792-116">ถ้าไม่มีบทบาทใดละเมิดกฎที่เลือก ข้อความจะบ่งชี้ว่าบทบาททั้งหมดสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="73792-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="73792-117">จะมีการตรวจสอบความถูกต้องเฉพาะกับกฎที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="73792-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="73792-118">เป็นสิ่งสําคัญที่ต้องตรวจสอบความถูกต้องของกฎแต่ละข้อ</span><span class="sxs-lookup"><span data-stu-id="73792-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="73792-119">เมื่อคุณสร้างหรือปรับเปลี่ยนบทบาท กฎสำหรับการแบ่งแยกหน้าที่จะถูกบังคับใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="73792-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="73792-120">คุณไม่สามารถกําหนดหน้าที่ที่ขัดแย้งกับบทบาท</span><span class="sxs-lookup"><span data-stu-id="73792-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="73792-121">จากนั้น ให้ตรวจสอบว่าการมอบหมายบทบาทที่มีอยู่ทั้งหมด สอดคล้องกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="73792-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="73792-122">ตรวจสอบว่าการกำหนดบทบาทผู้ใช้เป็นไปตามกฎใหม่ สำหรับการแบ่งแยกหน้าที่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="73792-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="73792-123">ไปที่ **การจัดการระบบ > ความปลอดภัย > การแบ่งแยกหน้าที่ > การตรวจสอบการปฏิบัติตามกฎระเบียบสำหรับการกำหนดบทบาทผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="73792-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="73792-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="73792-124">Select **OK**.</span></span> <span data-ttu-id="73792-125">การแจ้งเตือนแสดงผลลัพธ์ของการตรวจสอบ </span><span class="sxs-lookup"><span data-stu-id="73792-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="73792-126">การบันทึกความขัดแย้งในหน้า **ความขัดแย้งของการแบ่งแยกหน้าที่ที่ยังไม่ได้แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="73792-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="73792-127">เมื่อคุณกำหนดผู้ใช้กับบทบาท กฎสำหรับการแบ่งแยกหน้าที่จะถูกบังคับใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="73792-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="73792-128">หากคุณพยายามกําหนดผู้ใช้ให้กับบทบาทที่มีหน้าที่ที่ขัดแย้งกัน คุณจะได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="73792-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="73792-129">จากนั้นคุณต้องแก้ไขความขัดแย้ง โดยปฏิเสธหรืออนุญาตการมอบหมายบทบาทเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="73792-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="73792-130">บทบาทเพิ่มเติมจะถูกมอบหมายหลังจากอนุญาตให้มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="73792-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="73792-131">ขณะนี้ไม่มีการตรวจสอบความขัดแย้งของผู้ใช้ที่ได้รับการมอบหมายบทบาทตามกลุ่ม Active Directory Domain</span><span class="sxs-lookup"><span data-stu-id="73792-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="73792-132">ดูและแก้ไขการกำหนดบทบาทผู้ใช้ที่ขัดแย้งกัน</span><span class="sxs-lookup"><span data-stu-id="73792-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="73792-133">ไปที่ **การจัดการระบบ** > **ความปลอดภัย** > **การแบ่งแยกหน้าที่** > **ความขัดแย้งการแบ่งแยกหน้าที่ที่ยังไม่ได้แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="73792-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="73792-134">เลือกความขัดแย้ง แล้วเลือกการดำเนินการหนึ่งรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="73792-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="73792-135">**ปฏิเสธการกำหนด**: ตัวเลือกนี้จะปฏิเสธการกำหนดผู้ใช้ให้กับบทบาทความปลอดภัยเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="73792-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="73792-136">ถ้าคุณปฏิเสธการกำหนดบทบาทแบบอัตโนมัติ ผู้ใช้จะถูกทำเครื่องหมายเป็นถูกแยกออกจากบทบาท </span><span class="sxs-lookup"><span data-stu-id="73792-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="73792-137">ผู้ใช้ที่ถูกแยกออกจะไม่ได้รับอนุญาตให้เข้าถึงการเข้าถึงที่สัมพันธ์กับบทบาท และไม่สามารถกำหนดบทบาทได้จนกว่าผู้ดูแลระบบจะลบข้อยกเว้นนั้น</span><span class="sxs-lookup"><span data-stu-id="73792-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="73792-138">**อนุญาตให้มีการกำหนด**: ตัวเลือกนี้จะแทนที่ความขัดแย้ง และอนุญาตให้ผู้ใช้ถูกกำหนดให้กับบทบาทความปลอดภัยเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="73792-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="73792-139">ถ้าคุณแทนที่ความขัดแย้ง คุณต้องป้อนเหตุผลในฟิลด์ **เหตุผลสำหรับการแทนที่**</span><span class="sxs-lookup"><span data-stu-id="73792-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="73792-140">สามารถดูการมอบหมายบทบาทที่แทนที่ทั้งหมด บนหน้า **ความขัดแยังของการแบ่งแยกหน้าที่**</span><span class="sxs-lookup"><span data-stu-id="73792-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="73792-141">ถ้ามีความขัดแย้งหลายอย่างแสดงรายการไว้สำหรับผู้ใช้รายเดียวกัน ให้เลือกเรกคอร์ดผู้ใช้ และกำหนดบทบาทบนหน้า **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="73792-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="73792-142">เมื่อต้องการหลีกเลี่ยงความขัดแย้งนี้ ให้ตรวจสอบความถูกต้องของกฎแต่ละกฎ หลังจากที่เพิ่มหรือแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="73792-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>
