---
title: กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ
description: บทความนี้แสดงวิธีการสร้างกฎและนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ และจากนั้น กำหนดกฎสำหรับสวัสดิการ
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cc80549eaffa72a22dec51829c86d04a763de96a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114413"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="27eef-103">กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="27eef-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="27eef-104">หัวข้อนี้แสดงวิธีการสร้างกฎและนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ และจากนั้น กำหนดกฎสำหรับสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="27eef-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="27eef-105">สร้างชนิดของกฎนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="27eef-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="27eef-106">ไปที่ **ทรัพยากรบุคคล > สวัสดิการ > สิทธิ์ > ชนิดของกฎนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="27eef-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="27eef-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="27eef-107">Select **New**.</span></span>
3. <span data-ttu-id="27eef-108">ในฟิลด์ **ชื่อกฏ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="27eef-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="27eef-109">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="27eef-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="27eef-110">ในฟิลด์ **ชื่อการสอบถาม** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="27eef-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="27eef-111">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="27eef-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="27eef-112">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="27eef-112">Select **Save**.</span></span>
8. <span data-ttu-id="27eef-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="27eef-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="27eef-114">นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="27eef-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="27eef-115">ไปที่ **ทรัพยากรบุคคล > สวัสดิการ > สิทธิ์ > นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="27eef-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="27eef-116">เลือกนโยบายสวัสดิการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="27eef-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="27eef-117">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="27eef-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="27eef-118">สลับการขยายของส่วน **นโยบายองค์กร**</span><span class="sxs-lookup"><span data-stu-id="27eef-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="27eef-119">คุณสามารถเพิ่มหรือลบองค์กรใดๆที่คุณต้องการที่จะรวมไว้ในนโยบายได้</span><span class="sxs-lookup"><span data-stu-id="27eef-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="27eef-120">ขยายหรือยุบส่วน **กฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="27eef-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="27eef-121">ในรายการ ค้นหาและเลือกกฎนโยบายที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="27eef-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="27eef-122">เลือก **สร้างกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="27eef-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="27eef-123">ในฟิลด์ **วันมีผลบังคับใช้** ป้อนวันที่ที่คุณต้องการให้นโยบายเริ่มมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="27eef-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="27eef-124">การตั้งค่าวันที่สิ้นสุดที่มีผลบังคับใช้ ช่วยให้คุณสามารถทำการเปลี่ยนแปลงกฎนโยบายในอนาคต ดังนั้นคุณไม่จำเป็นต้องการกลับมาสู่นโยบาย เมื่อคุณต้องการให้การเปลี่ยนแปลงนั้นมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="27eef-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="27eef-125">ถ้าต้องการ ให้เพิ่มอนุประโยค where ที่ฟิลด์ **เพิ่มเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="27eef-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="27eef-126">ตัวอย่างเช่นถ้าคุณต้องการให้กฎนำไปใช้ได้เฉพาะกับผู้จัดการฝ่ายขาย คุณสามารถสร้างอนุประโยค Where เพื่อแจ้ง: โดยคำอธิบายตำแหน่งเทียบเท่ากับผู้จัดการฝ่ายขาย</span><span class="sxs-lookup"><span data-stu-id="27eef-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="27eef-127">คุณสามารถใส่ได้หลายประโยค Where พร้อมกันในกฎได้</span><span class="sxs-lookup"><span data-stu-id="27eef-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="27eef-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="27eef-128">Select **OK**.</span></span>
11. <span data-ttu-id="27eef-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="27eef-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="27eef-130">กำหนดกฎเพื่อผลประโยชน์</span><span class="sxs-lookup"><span data-stu-id="27eef-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="27eef-131">ไปที่ **ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="27eef-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="27eef-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="27eef-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="27eef-133">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="27eef-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="27eef-134">ขยายหรือยุบส่วน **กฎการมีสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="27eef-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="27eef-135">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="27eef-135">Select **Edit**.</span></span>
6. <span data-ttu-id="27eef-136">ในฟิลด์ **การมีสิทธิ์** เลือกกฎ</span><span class="sxs-lookup"><span data-stu-id="27eef-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="27eef-137">ในฟิลด์ **ชนิดกฎ** ให้เลือกกฎที่สร้างคุณได้สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="27eef-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="27eef-138">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="27eef-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="27eef-139">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="27eef-139">Select **Save**.</span></span>
11. <span data-ttu-id="27eef-140">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="27eef-140">Close the form.</span></span>

