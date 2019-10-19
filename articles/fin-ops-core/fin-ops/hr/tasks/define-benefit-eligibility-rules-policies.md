---
title: กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ
description: 'การบันทึกนี้จะแสดงวิธีการสร้างกฎและนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ และจากนั้น กำหนดกฎสำหรับสวัสดิการ   '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d35266c95cfbf3473a14fec47a1c748229dd25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190568"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="d89e9-103">กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d89e9-103">Define benefit eligibility rules and policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d89e9-104">การบันทึกนี้จะแสดงวิธีการสร้างกฎและนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ และจากนั้น กำหนดกฎสำหรับสวัสดิการ   </span><span class="sxs-lookup"><span data-stu-id="d89e9-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="d89e9-105">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างการบันทึกนี้คือ USMF </span><span class="sxs-lookup"><span data-stu-id="d89e9-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="d89e9-106">สร้างชนิดของกฎนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d89e9-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="d89e9-107">ไปที่ ทรัพยากรบุคคล > สวัสดิการ > สิทธิ์ > ชนิดของกฎนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d89e9-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="d89e9-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d89e9-108">Click New.</span></span>
3. <span data-ttu-id="d89e9-109">ในฟิลด์ชื่อกฎ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d89e9-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="d89e9-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d89e9-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d89e9-111">ในฟิลด์ชื่อการสอบถาม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d89e9-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d89e9-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d89e9-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d89e9-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d89e9-113">Click Save.</span></span>
8. <span data-ttu-id="d89e9-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d89e9-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="d89e9-115">นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d89e9-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="d89e9-116">ไปที่ ทรัพยากรบุคคล > สวัสดิการ > สิทธิ์ > นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d89e9-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="d89e9-117">เลือกนโยบายสวัสดิการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d89e9-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="d89e9-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d89e9-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d89e9-119">สลับการขยายของส่วนนโยบายองค์กร </span><span class="sxs-lookup"><span data-stu-id="d89e9-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="d89e9-120">ที่นี่คุณสามารถเพิ่มหรือลบองค์กรใดๆที่คุณต้องการที่จะรวมไว้ในนโยบายได้</span><span class="sxs-lookup"><span data-stu-id="d89e9-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="d89e9-121">ขยายหรือยุบส่วนของกฎนโยบายองค์กร</span><span class="sxs-lookup"><span data-stu-id="d89e9-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="d89e9-122">ในรายการ ค้นหาและเลือกกฎนโยบายที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="d89e9-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="d89e9-123">คลิกสร้างกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="d89e9-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="d89e9-124">ในฟิลด์วันมีผลบังคับใช้ ป้อนวันที่ที่คุณต้องการให้นโยบายเริ่มมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="d89e9-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="d89e9-125">การตั้งค่าวันที่มีผลบังคับใช้และวันที่สิ้นสุด ช่วยให้คุณสามารถทำการเปลี่ยนแปลงกฎนโยบายในอนาคตและลบความต้องการกลับมาสู่นโยบาย เมื่อคุณต้องการให้การเปลี่ยนแปลงนั้นมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="d89e9-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="d89e9-126">ตัวอย่างเช่นถ้าคุณต้องการให้กฎนำไปใช้ได้เฉพาะกับผู้จัดการฝ่ายขาย คุณสามารถสร้างอนุประโยค Where เพื่อแจ้ง: โดยคำอธิบายตำแหน่งเทียบเท่ากับผู้จัดการฝ่ายขาย</span><span class="sxs-lookup"><span data-stu-id="d89e9-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="d89e9-127">คุณสามารถใส่และหรือ หรือได้หลายประโยค Where พร้อมกันในกฎได้</span><span class="sxs-lookup"><span data-stu-id="d89e9-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="d89e9-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d89e9-128">Click OK.</span></span>
11. <span data-ttu-id="d89e9-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d89e9-129">Close the page.</span></span>
12. <span data-ttu-id="d89e9-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d89e9-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="d89e9-131">กำหนดกฎเพื่อผลประโยชน์</span><span class="sxs-lookup"><span data-stu-id="d89e9-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="d89e9-132">ไปที่ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d89e9-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="d89e9-133">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d89e9-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d89e9-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d89e9-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d89e9-135">ขยายหรือยุบส่วนของกฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="d89e9-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="d89e9-136">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="d89e9-136">Click Edit.</span></span>
6. <span data-ttu-id="d89e9-137">ในฟิลด์การมีสิทธิ์ เลือกกฎตามรายการ</span><span class="sxs-lookup"><span data-stu-id="d89e9-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="d89e9-138">ในฟิลด์ชนิดของกฎ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d89e9-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="d89e9-139">ในรายการ ค้นหาและเลือกกฎที่สร้างท่านได้สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="d89e9-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="d89e9-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d89e9-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d89e9-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d89e9-141">Click Save.</span></span>
11. <span data-ttu-id="d89e9-142">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="d89e9-142">Close the form.</span></span>

